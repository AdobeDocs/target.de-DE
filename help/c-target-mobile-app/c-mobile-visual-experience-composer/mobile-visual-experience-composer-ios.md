---
description: Mit dem Visual Experience Composer (VEC) von Adobe Target können Entwickler eine einmalige Einrichtung auf ihren mobilen ios-Apps durchführen und Marketingexperten die Verwendung der Funktionen der Mobile App VEC ermöglichen.
keywords: Mobile App VEC; Visual Experience Composer für Mobilgeräte; Mobile Experience Composer-Optionen; einrichten; ios; Apple
seo-description: Mit dem Visual Experience Composer (VEC) von Adobe Target können Entwickler eine einmalige Einrichtung auf ihren mobilen ios-Apps durchführen und Marketingexperten die Verwendung der Funktionen der Mobile App VEC ermöglichen.
seo-title: iOS – Einrichten der App
solution: Target
title: iOS – Einrichten der App
topic: Standard
uuid: 6db4f06a-d8f4-4192-af6f-917594e721e6
translation-type: tm+mt
source-git-commit: 5f58e6dc0e91a3341d73273edf953206a95d6450

---


# iOS – Einrichten der App{#ios-set-up-the-mobile-app}

Mit dem Visual Experience Composer (VEC) von Adobe Target Mobile Comp können Entwickler eine einmalige Einrichtung auf ihren mobilen ios-Apps durchführen und Marketingexperten die Verwendung der Funktionen der Mobile App-VEC ermöglichen.

Weitere Informationen zum Aktivieren der Adobe Target VEC-Erweiterung finden Sie unter [Adobe Target - Visual Experience Composer](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec) in den *mobilen sdks von Adobe Experience Platform*.

## Einschließen des mobilen SDK und der Target-Bibliothek {#sdk-library}

1. Add the library to your project via your Cocoapods [!DNL Podfile] by adding pod &#39;`ACPTargetVEC`&#39;.
1. Öffnen Sie Ihr Objective-C-Anwendungsprojekt in XCode.
1. Wechseln Sie zu Ihren Projekterstellungseinstellungen und legen Sie &quot;Schnelle Einbettung schnell eingebettet&quot; auf&quot; Ja&quot; fest, wenn bereits nicht festgelegt.
1. Suchen Sie in den Projekterstellungseinstellungen nach „Andere Linker-Flags“ und fügen Sie `$(inherited)` hinzu, sollte dies noch nicht geschehen sein.
1. Nur für Objective-C-Projekte: Erstellen Sie eine Swift-Datei, um die Bridging-Kopfzeile zu erstellen. Sie richtet Ihre Anwendungsumgebung für Swift ein.
1. Fügen Sie den Deeplink-Handler hinzu:

   1. Klicken Sie in den Einstellungen Ihres Anwendungsprojekts auf **[!UICONTROL Info]**.
   1. Klicken Sie unter **[!UICONTROL URL-Typen]** auf das Dreieck, um es zu öffnen, und klicken Sie dann auf das Pluszeichen, um ein neues Feld hinzuzufügen.
   1. Fügen Sie folgende Informationen hinzu:

      * ID: `com.adobe.sdktest`
      * URL-Schemas: `vectester`
      * Rolle: Editor
   1. Schließen Sie die Registerkarte **[!UICONTROL Allgemein der Einstellungen Ihres Anwendungsprojekts]**.
   1. Öffnen Sie die Registerkarte **[!UICONTROL Info]in den Einstellungen Ihres Anwendungsprojekts, um sicherzustellen, dass die Einstellungen gespeichert wurden.**

      Mit dem Beispiel-URL-Typ lautet das URL-Schema für Ihre Anwendung:

      ```
      vectester://com.adobe.sdktest
      ```


1. Öffnen Sie in XCode die [!DNL AppDelegate]-Datei.
1. Fügen Sie oben in der Datei folgende Zeile am Ende Ihrer Importe hinzu:

   `#import "ACPTargetVEC.h"`

   Wenn Sie Swift verwenden, fügen Sie die folgende Zeile hinzu:

   `import ACPTargetVEC`

1. Fügen Sie in Ihrer Datei [!DNL AppDelegate] die folgende Zeile zu `AppDelegate::application:didFinishLaunchingWithOptions:` hinzu. Wenn die Delegate-Funktionen nicht definiert sind, erstellen Sie sie und fügen Sie folgende Zeile für die Objective-C- bzw. die Swift-Anwendung hinzu:

   ```
   // CONFIGURATION LINE FOR OBJECTIVE C ONLY (Skip any framework which is not applicable for you): 
   [ACPCore configureWithAppId:@"YOUR_ADOBE_LAUNCH_APP_ID"]; 
   [ACPCore setLogLevel:ACPMobileLogLevelDebug]; 
   [ACPLifecycle registerExtension]; 
   [ACPIdentity registerExtension]; 
   [ACPUserProfile registerExtension]; 
   [ACPTarget registerExtension];
   
   [ACPTargetVEC registerExtension];
   [ACPCore start:^{
        [ACPCore lifecycleStart:nil];
   }];
   
   // CONFIGURATION LINE FOR SWIFT ONLY: 
   ACPCore.configure(withAppId: "YOUR_ADOBE_LAUNCH_APP_ID") 
   ACPCore.setLogLevel(ACPMobileLogLevel.debug) 
   ACPLifecycle.registerExtension() 
   ACPIdentity.registerExtension() 
   ACPUserProfile.registerExtension() 
   ACPTarget.registerExtension() 
   
   ACPTargetVEC.registerExtension() 
   
   ACPCore.start {
     ACPCore.lifecycleStart(nil)
   }
   ```

   Die Methode sollte folgendem Beispiel ähneln:

   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY: 
   - (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions { 
        // Override point for customization after application launch. 
       [ACPCore configureWithAppId:@"YOUR_ADOBE_LAUNCH_APP_ID"]; 
       [ACPCore setLogLevel:ACPMobileLogLevelDebug]; 
       [ACPLifecycle registerExtension]; 
       [ACPIdentity registerExtension]; 
       [ACPUserProfile registerExtension]; 
       [ACPTarget registerExtension]; 
   
       [ACPTargetVEC registerExtension]; 
   
       [ACPCore start:nil]; 
       [ACPCore lifecycleStart:nil]; 
   
      return YES; 
   } 
   
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY: 
   func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]? = nil) 
   { 
       ACPCore.configure(withAppId: "YOUR_ADOBE_LAUNCH_APP_ID") 
       ACPCore.setLogLevel(ACPMobileLogLevel.debug) 
       ACPLifecycle.registerExtension() 
       ACPIdentity.registerExtension() 
       ACPUserProfile.registerExtension() 
       ACPTarget.registerExtension() 
   
       ACPTargetVEC.registerExtension() 
   
       ACPCore.start(nil) 
       ACPCore.lifecycleStart(nil)
   
       return true 
   
   }
   ```

1. Fügen Sie die folgende Zeile am Anfang von `AppDelegate:application:openURL` hinzu. Wenn die Delegate-Funktionen nicht definiert sind, erstellen Sie sie und fügen Sie folgende Zeile hinzu:

   ```
   // URL HANDLER LINE FOR OBJECTIVE C ONLY: 
   [ACPTargetVEC handleDeepLink:url];
   
   // URL HANDLER LINE FOR SWIFT ONLY: 
   ACPTargetVEC.handleDeepLink(url)
   ```

   Die Methode sollte folgendem Beispiel ähneln:

   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY:
   -  (BOOL)application:(UIApplication *)application openURL:(NSURL *)url options:(NSDictionary<NSString *, id> *)options {
    [ACPTargetVEC handleDeepLink:url];
    return YES;
   }
   
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY:
   func application(_ app: UIApplication, open url: URL, options: [UIApplication.OpenURLOptionsKey : Any] = [:]) -> Bool {
      ACPTargetVEC.handleDeepLink(url)
      return true;
   }
   ```

1. Erstellen Sie Ihre Anwendung und führen Sie sie aus, um Mobile App-VEC-Funktionen zu testen.

## Einrichten von Target-Ansichten auf Ihrer mobilen App {#views}

Das Adobe Mobile SDK stellt eine neue Methode für Entwickler bereit, die ausgelöst werden kann, sobald eine neue Ansicht gerendert wird. Lesen Sie die allgemeinen Richtlinien zum korrekten Einfügen der Target View API-Aufrufe für eine ios-App. In iOS sind alle Target-Ansichten in Abhängigkeit zu dem `UIViewController` definiert, in dem sie enthalten sind. Im Gegensatz zu Android ist die Einfügung von `TargetViews` also auf folgende Aufrufe beschränkt.

Die Adobe Mobile App VEC Extension generiert automatisch Namen für Ihre `UIViewControllers` Interaktion innerhalb des mobilen App-VEC-Frameworks, basierend auf dem Klassennamen der Unterklasse `UIViewController`. Wenn Sie diese Namen überschreiben möchten, können Sie die folgende Methode in `viewWillAppear` der Liste `ViewController`aufrufen.

```
// TARGET VIEW LINE FOR OBJECTIVE C ONLY 
[ACPTargetVEC setTargetView:@"exampleViewController"]; 
   
// TARGET VIEW LINE FOR SWIFT ONLY 
ACPTargetVEC.setTargetView("exampleViewController")
```

Das Adobe Mobile SDK bietet auch eine alternative Methode für Entwickler, während der Laufzeit benutzerspezifische Ansichten anzusteuern. Als Entwickler müssen Sie sicherstellen, dass die Ansichten eindeutige Namen aufweisen. Rufen Sie die folgende Methode auf, bevor Sie die Ansicht dem folgenden `superview`hinzufügen:

```
// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN OBJECTIVE C 
CustomPopupView *popupView = [[CustomPopupView alloc] initWithFrame:CGRectMake(0, 0, 300, 200)]; 
[ACPTargetVEC setTargetView:@"myCustomPopupView" forView:popupView];

// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN SWIFT 
let popupView = CustomPopupView.init(frame: CGRect(x: 0, y: 0, width: 300, height: 200)) 
ACPTargetVEC.setTargetView("myCustomPopupView", for: popupView)
```

## Einrichten von Profilparametern und anderen globalen Parametern {#parameters}

Wir unterstützen jetzt die Festlegung globaler Parameter, die in jedem einzelnen API-Aufruf übergeben werden, sowie die Übergabe von mbox-/anzeigen-Parametern an die entsprechenden Ansichten.

Diese Parameter umfassen:

* Mbox-/Anzeige-Parameter
* Profilparameter
* Produktparameter
* Bestellparameter

**Globale Parameterunterstützung:**

```
//For Objective-c 
NSDictionary *mboxParams = @{@"mboxparam1":@"mboxvalue1"}; //mbox or view params 
NSDictionary *profileParams = @{@"profilekey1":@"profilevalue1"}; //profile params 
  
ACPTargetProduct *product = [ACPTargetProduct targetProductWithId:@"1234" categoryId:@"furniture"]; 
ACPTargetOrder *order = [ACPTargetOrder targetOrderWithId:@"12343" total:@(123.45) purchasedProductIds:@[@"100",@"200"]]; 
ACPTargetParameters *targetParams = [ACPTargetParameters targetParametersWithParameters:mboxParams 
                                                                      profileParameters:profileParams 
                                                                                product:product 
                                                                                  order:order]; 
[ACPTargetVEC setGlobalRequestParameters:targetParams];

//For Swift 
var mboxParams = ["mboxparam1":"mboxvalue1"] 
var profileParams = ["profilekey1":"profilevalue1"] 
var product : ACPTargetProduct = ACPTargetProduct.init(id: "1234", categoryId: "furniture") 
var order : ACPTargetOrder = ACPTargetOrder.init(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"]) 
var targetParams : ACPTargetParameters = ACPTargetParameters.init(parameters: mboxParams, profileParameters: profileParams, product: product, order: order) 
ACPTargetVEC.setGlobalRequest(targetParams)
```

**Übergabe von Parametern für die Auslösung der nächsten Ansicht:**

Wir haben einige automatische Ansichten bereitgestellt, die standardmäßig erstellt werden, z. B. &quot;`AUTO_<viewControllerName>`für jeden Ansichtscontroller in Ihrer App. Um diese Parameter zu übergeben, können Sie folgende API aufrufen:

```
//For Objective-c 
NSDictionary *mboxParams = @{@"viewparam1":@"viewvalue1"}; //mbox or view params 
NSDictionary *profileParams = @{@"profilekeyforview1":@"profilevalueforview1"}; //profile params 
  
ACPTargetProduct *product = [ACPTargetProduct targetProductWithId:@"1234" categoryId:@"furniture"]; 
ACPTargetOrder *order = [ACPTargetOrder targetOrderWithId:@"12343" total:@(123.45) purchasedProductIds:@[@"100",@"200"]]; 
ACPTargetParameters *targetParams = [ACPTargetParameters targetParametersWithParameters:mboxParams 
                                                                      profileParameters:profileParams 
                                                                                product:product 
                                                                                  order:order]; 
[ACPTargetVEC setGlobalRequestParameters:targetParams];

//For Swift 
var mboxParams = ["mboxparam1":"mboxvalue1"] 
var profileParams = ["profilekey1":"profilevalue1"] 
var product : ACPTargetProduct = ACPTargetProduct.init(id: "1234", categoryId: "furniture") 
var order : ACPTargetOrder = ACPTargetOrder.init(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"]) 
var targetParams : ACPTargetParameters = ACPTargetParameters.init(parameters: mboxParams, profileParameters: profileParams, product: product, order: order) 
ACPTargetVEC.setRequest(targetParams)
```

**Übergabe von Parametern an bestimmte Ansichten:**

We have seen the API trigger Views via `TargetVEC.targetView("view_name")`. Sie können auch Parameter übergeben, die spezifisch für die jeweilige Ansicht sind:

```
//For Objective-c 
[ACPTargetVEC setTargetView:@"VIEW_NAME" withParameters:TARGET_PARAMS];

//FOR SWIFT 
ACPTargetVEC.setTargetView("VIEW_NAME", with: TARGET_PARAMS)
```

## Explizit aufrufen der Prefetch-API {#section_373DB4527FC649C58FBA3DF0C18C9836}

Es gibt bestimmte Szenarien, in denen Sie die Vorabruf-API erneut aufrufen müssen, um die im Cache gespeicherten Angebote zu aktualisieren. Hierfür sind folgende APIs verfügbar:

**Angebote vorab abrufen:**

```
/** 
 * Prefetch all offers for all views in the cache. It will remove existing offers and changes for the current view will be 
 refreshed only when the view is triggered. This call happens on the main thread blocking the UI. 
 */ 
+ (void) prefetchOffers;
```

**Angebote im Hintergrund vorab abrufen:**

```
/** 
 * Prefetch all offers for all views in the cache. It will remove existing offers and changes for the current view will be 
 refreshed only when the view is triggered. This call happens on the background thread so doesn't block UI. 
 */ 
+ (void) prefetchOffersBackground;
```

## Übungen: Implementieren der Experience Cloud in Mobile ios-Anwendungen Objective-C und Swift {#tutorial}

* [Implementieren der Experience Cloud in Mobile ios-Target-C-Anwendungen](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-objective-c-apps-with-launch/index.html)
* [Implementieren der Experience Cloud in Mobile ios Swift-Anwendungen](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-swift-apps-with-launch/index.html)

Nach Abschluss dieser Übungen können Sie:

* Mobile Launch-Eigenschaft erstellen
* Installieren einer Start-Eigenschaft in einer Target-C- oder Swift-App
* Implementieren Sie die folgenden Adobe Experience Cloud-Lösungen:
   * Experience Cloud ID-Dienst
   * Adobe Target
   * Adobe Analytics
   * Adobe Audience Manager

* Veröffentlichen von Änderungen im Start über Entwicklungs-, Staging- und Produktionsumgebungen