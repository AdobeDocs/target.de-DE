---
description: Mit der neuen SDK-Bibliothek von Target müssen Entwickler die Einrichtung nur einmal für ihre Android-Apps durchführen, damit die Funktionen des Mobile Visual Experience Composer (VEC) für Marketing-Experten verfügbar sind.
keywords: mobile vec; Visual Experience Composer für Mobilgeräte; Mobile Experience Composer-Optionen; Einrichten; Android
seo-description: Mit der neuen SDK-Bibliothek von Target müssen Entwickler die Einrichtung nur einmal für ihre Android-Apps durchführen, damit die Funktionen des Mobile Visual Experience Composer (VEC) für Marketing-Experten verfügbar sind.
seo-title: Android – Einrichten der App
solution: Target
title: Android – Einrichten der App
topic: Standard
uuid: 39938ec2-b12e-44cf-9218-69195fba0ff7
translation-type: tm+mt
source-git-commit: 2588a7c251e58193b969d57f91a7c3f640318fbf

---


# Android – Einrichten der App{#android-set-up-the-mobile-app}

Mit dem Adobe Target Mobile App Visual Experience Composer (VEC) von können Entwickler einmalige Einrichtung in ihren Android-Apps durchführen und Marketingexperten die Funktionen des Mobile App VEC nutzen.

Weitere Informationen zum Aktivieren der Adobe Target VEC-Erweiterung finden Sie unter [Adobe Target - Visual Experience Composer](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec) in den *mobilen SDKs von Adobe Experience Platform*.

## Mobile SDK und Target-Bibliothek einschließen {#sdk-library}

1. Informationen zur Initialisierung von SDK-Version 5 finden Sie unter [Initialisieren des SDK und Einrichten des Trackings](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk).
1. Fügen Sie folgende Zeile zum Abschnitt der Abhängigkeiten hinzu:

   ```
   implementation 'com.adobe.marketing.mobile:target:1.+'
   implementation 'com.adobe.marketing.mobile:target-vec:1.+'
   ```

1. Für die mobile Anwendung VEC müssen die folgenden Artefakte als Abhängigkeiten in `build.gradle`einbezogen werden.

   ```
    implementation 'android.arch.lifecycle:extensions:1.1.1'
    implementation 'io.github.sac:SocketclusterClientJava:1.7.5'
    implementation 'com.android.support:support-compat:28.0.0'
    implementation 'com.android.support:support-fragment:28.0.0'
   ```

1. Fügen Sie einen Intent-Filter in Ihrer Datei `AndroidManifest.XML` hinzu, indem Sie ein eindeutiges Deep-Link-Schema für die Erstellung in Mobile Anwendung VEC auswählen (beispielsweise `[sdkbetabus://com.adobe.sdkbetabus](sdkbetabus://com.adobe.sdkbetabus)`):

   ```
   <activity 
       android:name=".listing.MoviesListingActivity" 
       android:launchMode="singleTask"> 
       <intent-filter> 
           <action android:name="android.intent.action.VIEW" /> 
   
           <category android:name="android.intent.category.DEFAULT" /> 
           <category android:name="android.intent.category.BROWSABLE" /> 
   
           <data 
               android:host="com.adobe.sdkbetabus" 
               android:scheme="sdkbetabus" /> 
       </intent-filter> 
   </activity>
   ```

1. Wechseln Sie zu Ihrem mobilen Projekt und fügen Sie folgende Zeilen am Ende von `Application::onCreate override` ein:

   ```
   public class SDKTest extends MultiDexApplication { 
   
       @Override 
       public void onCreate() { 
           /* Put Your App's implementation */ 
           MobileCore.setApplication(this); 
           MobileCore.setLogLevel(LoggingMode.DEBUG); 
           MobileCore.configureWithAppID("YOUR_ADOBE_LAUNCH_APP_ID"); 
   
           ... 
           try { 
               TargetVEC.registerExtension(); //Single line code to initialize TargetVEC
               Target.registerExtension();
               Identity.registerExtension();
               Lifecycle.registerExtension();
               Signal.registerExtension();
               MobileCore.start(null);
           } catch (InvalidInitException e) { 
             .. 
           }
       }
   
   /* Rest of Application test goes here ... */
   ```

1. Wenn Ihr Build nicht funktioniert, sehen Sie sich die nachstehenden Beispielprojekte an, für die sofort ein Build möglich sein sollte, und überprüfen Sie folgende Stellen auf Änderungen:

   1. `Application::OnCreate override`
   1. `AndroidManifest.XML`
   1. `build.gradle` der Android-App

## Target-Ansichten in Ihrer App einrichten {#views}

Das Adobe Mobile SDK stellt eine neue Methode für Entwickler bereit, die ausgelöst werden kann, sobald eine neue Ansicht gerendert wird. Als Entwickler müssen Sie sicherstellen, dass die Ansichten eindeutig benannt sind und sich der `targetView`-Aufruf im UI-Hauptthread befindet. In diesem Abschnitt wird zunächst anhand von zwei verschiedenen Demo-Apps gezeigt, wie diese Aufrufe eingefügt werden. Anschließend erhalten Sie einige allgemeine Richtlinien dazu, wie Sie Aufrufe der Target-Ansichts-API in beliebigen Android-Apps richtig einfügen können.

>[!NOTE]
>
>Wenn `targetView function` nicht ausgelöst wird, versucht die VEC-Erweiterung, die Ansicht über die Android-Aktivität zu identifizieren. Bei Apps ohne dynamische Ansichten kann dies ein optionaler Schritt sein.

Eine Target-Ansicht kann mit einem Funktionsaufruf ausgelöst werden. Alle Targeting-Parameter können optional mit der Ansicht bereitgestellt werden.

```
public class TargetVEC { 
   
   /** 
    * Marks a view hierarchy for editing in Mobile App VEC.  Call must insert when the view hierarchy 
    * is memory and committed to being shown, but not yet shown on the screen. 
    * 
    * @param viewName the unique Target View Name 
    */ 
   public static void targetView(String viewName); 
  
  /** 
   * Trigger Target view 
   * Triggering a Target view may cause Target offers to be applied on the current container component. 
   * Note that Target offers are applied from local Target cache, so flicker should be negligible. 
   * 
   * @param viewName Mandatory Target View name, which must be unique at app level 
   * @param parameters Parameters to be included in the next Target call 
   */ 
  
    public static void targetView(String viewName, TargetParameters parameters); 
}
```

In unserem ersten Beispielprojekt erstellen wir eine Testanwendung zur Planung von Busfahrten. Einrichten der App zur Verwendung im Mobile App VEC:

1. Öffnen Sie das Projekt mit der Datei `build.gradle` im Paketunterverzeichnis `BusBooking` in Android Studio.
1. Fügen Sie in der `DemoApplication::OnCreate`-Methode `TargetVEC.registerExtension()` hinzu, um die Target VEC-Erweiterung zusammen mit anderen Erweiterungen zu registrieren.
1. Kompilieren und starten Sie die Applikation.
1. Um in den Erstellungsmodus des Mobile App VEC zu wechseln, verwenden Sie [!DNL sdkbetabus://com.adobe.sdkbetabus] als URL-Schema und öffnen Sie den generierten Deep Link auf dem Gerät (siehe Anweisungen unten).

In dieser einfachen Anwendung zur Planung von Busfahrten werden alle automatisch generierten Target-Ansichten verwendet, die mit dem Lebenszyklus der Aktivität verbunden sind. Darüber hinaus wird so die Flexibilität der API veranschaulicht, indem die Target-Ansichts-API über ein benutzerdefiniertes Ansichtselement aufgerufen wird, das dynamisch hinzugefügt wird, sobald auf eine versteckte Schaltfläche geklickt wird (das Angebotsbild auf dem Bildschirm). Die neue Target-Ansicht wird implementiert, indem ein API-Aufruf bei `OfferDetailsActivity.java:40` in den Code eingefügt wird. Durch Klicken auf die versteckte Schaltfläche wird ein neues Target-Ansichtsereignis mit dem Namen „SURPRISE_VIEW“ ausgelöst, das Marketing-Experten eine zielgerichtetere Änderung des Applikationserlebnisses ermöglicht.

Gezielte Einfügung einer dynamischen Ansicht:

```
package com.adobe.target.examples.bus; 
   
import android.app.DialogFragment; 
import android.os.Bundle; 
import android.os.Handler; 
import android.support.v7.app.AppCompatActivity; 
import android.support.v7.widget.Toolbar; 
import android.view.View; 
import android.view.ViewGroup; 
import android.widget.LinearLayout; 
import android.widget.Toast; 
   
import com.adobe.target.mobile.TargetVEC; 
   
/** 
 * This activity class is responsible to show offer details 
 */ 
public class OfferDetailsActivity extends AppCompatActivity { 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        setContentView(R.layout.activity_offer_details); 
        setUpToolBar(); 
        final Handler mainHandler = new Handler(getApplicationContext().getMainLooper()); 
   
        final View surpriseView = getLayoutInflater().inflate(R.layout.suprise_layout, 
                (ViewGroup) findViewById(android.R.id.content), false); 
   
        final View imagePresentView = this.findViewById(R.id.image_present); 
        final LinearLayout currentLayout = this.findViewById(R.id.offer_layout); 
   
        imagePresentView.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                Toast.makeText(getApplicationContext(),"Surprise!", Toast.LENGTH_SHORT).show(); 
                mainHandler.post(new Runnable() { 
                    @Override 
                    public void run() { 
                        currentLayout.addView(surpriseView); 
                        TargetVEC.targetView("SURPRISE_VIEW"); 
                        currentLayout.invalidate(); 
                    } 
                }); 
                // One-shot.  Remove clicker afterwards. 
                imagePresentView.setOnClickListener(null); 
            } 
        }); 
    } 
   
    private void setUpToolBar() { 
        Toolbar toolbar = findViewById(R.id.toolbar); 
        toolbar.setNavigationIcon(R.drawable.abc_ic_ab_back_material); 
        toolbar.setTitle("Buy 1 Get 1"); 
        toolbar.setNavigationOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                onBackPressed(); 
            } 
        }); 
    } 
   
    @Override 
    protected void onPause() { 
        super.onPause();
        MobileCore.lifecyclePause();
    } 
   
    @Override 
    protected void onResume() { 
        super.onResume();
        MobileCore.lifecycleStart(null);
    } 
}
```

## Einrichten von Profil- und anderen globalen Parametern {#parameters}

Wir unterstützen jetzt die Einrichtung globaler Parameter, die in jedem API-Aufruf übergeben werden, sowie die Übergabe von Mbox-/Anzeige-Parametern an die entsprechenden Ansichten.

Diese Parameter umfassen:

* Mbox-/Anzeige-Parameter
* Profilparameter
* Produktparameter
* Bestellparameter

**Globale Parameterunterstützung:**

```
Map<String, String> mboxParams = new HashMap<>();  //Mbox or view params 
mboxParams.put("mboxparam1", "mboxvalue1"); 
Map<String, String> profileParams = new HashMap<>();  //Profile params 
profileParams.put("profilekey1", "profilevalue1"); 
  
TargetVEC.setGlobalRequestParameters(new TargetParameters.Builder() 
        .parameters(mboxParams) 
        .profileParameters(profileParams) 
        .product(new TargetProduct("1234", "furniture")) 
        .order(new TargetOrder("12343", 123.45, Arrays.asList("100", "200"))) 
        .build());
```

**Übergabe von Parametern für die Auslösung der nächsten Ansicht:**

Wir bieten einige automatische Ansichten, die standardmäßig erstellt werden, wie z. B. „`AUTO_<activity|fragment name>`“ für jede Aktivität und jedes Fragment in Ihrer App. Um diese Parameter zu übergeben, können Sie folgende API aufrufen:

```
Map<String, String> mboxParams = new HashMap<>();  //Mbox or view params 
mboxParams.put("viewKey1", "viewparam1"); 
Map<String, String> profileParams = new HashMap<>();  //Profile params 
profileParams.put("profilekeyforview1", "profilevalueforview1"); 
  
TargetVEC.setRequestParameters(new TargetParameters.Builder() 
        .parameters(mboxParams) 
        .profileParameters(profileParams) 
        .product(new TargetProduct("1234", "furniture")) 
        .order(new TargetOrder("12343", 123.45, Arrays.asList("100", "200"))) 
        .build());
```

**Übergabe von Parametern an bestimmte Ansichten:**

Wir haben gesehen, wie die API Ansichten durch `TargetVEC.targetView("view_name")` auslöst. Sie können auch Parameter übergeben, die spezifisch für die jeweilige Ansicht sind:

```
Map<String, String> profileParams = new HashMap<>(); 
profileParams.put("surprisekey1", "surprisevalue1");  //ProfileParams 
TargetVEC.targetView("SURPRISE_VIEW", 
        new TargetParameters.Builder() 
                .profileParameters(profileParams) 
                .product(new TargetProduct("3354", "kitchen")) 
                .build());
```

## Explizites Aufrufen der Vorabruf-API {#section_2D02B74558474D3BA9F25E4D25E7C7E3}

Es gibt bestimmte Szenarien, in denen Sie die Vorabruf-API erneut aufrufen müssen, um die im Cache gespeicherten Angebote zu aktualisieren. Hierfür sind folgende APIs verfügbar:

* **prefetchOffers**

   ```
   /** 
    * Prefetch Target offers. 
    * Note that calling this will pre-hide the current layout, until Target offers are prefetched 
    * and applied to currently visible Target views, possibly causing flicker, thus it's recommended 
    * to call this method inside the containing component's onCreate() lifecycle method 
    */ 
   public static void prefetchOffers();
   ```

* **prefetchOffersBackground**

   ```
   /** 
    * Prefetch Target offers in the background. 
    * Note, that in contrast to prefetchOffers(), calling this method will NOT pre-hide 
    * the current layout, instead prefetched Target offers will be only be cached and will subsequently 
    * be applied as Target Views are being triggered. 
    */ 
   public static void prefetchOffersBackground();
   ```

## Lernprogramm: Implementieren der Experience Cloud in Mobile Android-Anwendungen {#tutorial}

* [Implementieren der Experience Cloud in Mobile Android-Anwendungen](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-android-apps-with-launch/index.html)

Nach Abschluss dieses Übung können Sie:

* Mobile Launch-Eigenschaft erstellen
* Installieren einer Starteigenschaft in einer Android-App
* Implementieren Sie die folgenden Adobe Experience Cloud-Lösungen:
   * Experience Cloud ID-Dienst
   * Adobe Target
   * Adobe Analytics
   * Adobe Audience Manager

* Veröffentlichen von Änderungen im Start über Entwicklungs-, Staging- und Produktionsumgebungen
