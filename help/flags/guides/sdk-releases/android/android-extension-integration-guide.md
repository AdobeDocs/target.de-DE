---
title: Flags-Erweiterung für Android-Integrationshandbuch
description: Erfahren Sie, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in Android integrieren.
badge: label="Beta" type="Informative"
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: c1fafcfcd7d5d22781abdd10e6eb3c2b84136c2d
workflow-type: tm+mt
source-wordcount: '1379'
ht-degree: 4%
---
# Flags-Erweiterung für Android {#android-extension-integration-guide}

In diesem Handbuch wird beschrieben, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in Android integrieren.

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Implementierung der Flags-Erweiterung Folgendes sicher:

* Eine Mobile-Eigenschaft, die in der Datenerfassung von [Adobe Experience Platform konfiguriert ist](https://experience.adobe.com/#/data-collection)
* Die Adobe Flags-Erweiterung ist in Ihrer Mobile-Eigenschaft installiert und konfiguriert
* Eine Adobe Experience Cloud-Organisations-ID
* Ein in Ihrer Mobile-Eigenschaft konfigurierter Edge Network-Datenstrom für den Empfang von Exposure Analytics
* Android API 21 (Android 5.0 Lollipop) oder höher
* Mobile Core 3.6.0 oder höher (in `sdk-bom` 3.17.0 und höher enthalten)

## Abhängigkeiten der Erweiterung {#extension-dependencies}

Die Flags-Erweiterung erfordert die folgenden Adobe Experience Platform-Erweiterungen:

| Erweiterung | Beschreibung | Erforderlich |
|---|---|---|
| [Mobile Core](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | Bietet Konfiguration, Ereignisverarbeitung und SDK-Initialisierung | Ja |
| [Lebenszyklus](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | Berichte, wenn die App in den Vordergrund oder Hintergrund wechselt | Ja |
| [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Sendet Exposure Analytics an Adobe Experience Platform | Ja |
| [Identität für Edge Network](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | Stellt die Identitäten bereit, mit denen Benutzende Varianten zugewiesen werden | Ja |

Stellen Sie sicher, dass diese Erweiterungen in Ihrer Datenerfassungs-Eigenschaft für Mobilgeräte installiert und in Ihren App-Abhängigkeiten enthalten sind.

## Konfigurieren der Flags-Erweiterung in der Datenerfassung {#configure}

### Installieren der Erweiterung {#install-extension}

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/#/data-collection) an.

1. Wählen Sie im Menü **[!UICONTROL Tags]** Ihre Mobile-Eigenschaft aus.

1. Navigieren Sie **[!UICONTROL Erweiterungen]** > **[!UICONTROL Katalog]**.

1. Suchen Sie nach **[!DNL Adobe Flags]** und wählen Sie **[!UICONTROL Installieren]** aus.

   ![](../assets/extension-install.png)

1. Konfigurieren Sie die Erweiterungseinstellungen:

   * **[!UICONTROL Sandbox]**: Die Adobe Experience Platform-Sandbox, die Ihre Flags-Konfiguration enthält.
   * **[!UICONTROL Anwendungs-ID]**: Die Kennung Ihrer Anwendung in Flags.

1. Wählen Sie **[!UICONTROL Speichern]** aus.

1. Befolgen Sie den [Veröffentlichungsprozess](https://experienceleague.adobe.com/de/docs/experience-platform/tags/publish/overview), um Ihre Konfiguration zu aktualisieren.

### Abrufen der Umgebungsdatei-ID {#environment-file-id}

1. Navigieren Sie in Ihrer Mobile-Eigenschaft zu **[!UICONTROL Umgebungen]**.

1. Aktivieren Sie das Feldsymbol in der Spalte **[!UICONTROL Installieren]** der ausgewählten Umgebung.

   ![](../assets/extension-install-2.png)

1. Kopieren Sie **[!UICONTROL Dialogfeld „Mobile-]**&quot; die **[!UICONTROL Umgebungsdatei-ID]**.

   ![](../assets/extension-install-3.png)

## Hinzufügen der Flags-Erweiterung zur App {#add-to-app}

### Hinzufügen von Abhängigkeiten {#add-dependencies}

>[!IMPORTANT]
>
>Die Flags-Erweiterung ist nicht Teil der SDK-Stückliste für Mobilgeräte. Ersetzen Sie `<latest-version>` durch die neueste Version von Maven Central. Ohne eine Version kann Gradle die Abhängigkeit nicht auflösen.
>
></br>
>&gt;Für Produktionsanwendungen empfiehlt Adobe die Verwendung expliziter Versionsnummern anstelle dynamischer Versionen wie „3.+". Weitere Informationen finden Sie unter [Verwalten von Gradle-Abhängigkeiten](https://docs.gradle.org/current/userguide/dependency_management.html).

Fügen Sie die folgenden Abhängigkeiten zur `build.gradle.kts` (Kotlin) oder `build.gradle` (Groovy) Ihrer App hinzu:

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation(platform("com.adobe.marketing.mobile:sdk-bom:3.+"))

    // Required extensions (versions managed by the BOM)
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")

    // Flags extension (not managed by the BOM; specify the version)
    implementation("com.adobe.marketing.mobile:flags:<latest-version>")
}
```

>[!TAB groovy]

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation platform('com.adobe.marketing.mobile:sdk-bom:3.+')

    // Required extensions (versions managed by the BOM)
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'

    // Flags extension (not managed by the BOM; specify the version)
    implementation 'com.adobe.marketing.mobile:flags:<latest-version>'
}
```

>[!ENDTABS]

### SDK initialisieren {#initialize-sdk}

>[!IMPORTANT]
>
>Verwenden Sie für Produktions-Apps nur `LoggingMode.ERROR`. Verwenden Sie `DEBUG` oder `VERBOSE` nicht in Release-Builds.

Initialisieren Sie die Mobile SDK in Ihrer `Application`-Klasse, bevor Sie APIs für Flags-Erweiterungen aufrufen. Verwenden Sie die Umgebungsdatei-ID aus Ihrer Mobile-Eigenschaft, damit die App die Flags-Einstellungen übernimmt, die Sie in der Datenerfassung veröffentlicht haben.

`MobileCore.initialize` registriert jede Adobe-Erweiterung, die in Ihren Gradle-Abhängigkeiten enthalten ist, einschließlich der Flags-Erweiterung.

Beachten Sie, dass Sie bei Verwendung von `MobileCore.initialize` nicht auch `MobileCore.registerExtensions`, `MobileCore.lifecycleStart` oder `MobileCore.lifecyclePause` aufrufen dürfen. Diese werden für Sie bearbeitet.

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

>[!TAB Java]

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID");
    }
}
```

>[!ENDTABS]

### Registrieren der Application-Klasse {#register-application}

Registrieren Sie Ihre `Application` in `AndroidManifest.xml`:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

### Wenn Sie Erweiterungen manuell registrieren {#register-manually}

Wenn Ihre App `MobileCore.initialize` nicht verwenden kann und Erweiterungen bei `MobileCore.registerExtensions` registriert, fügen Sie `Flag.EXTENSION` zur Liste hinzu. Verwenden Sie die Identity for Edge Network-Klasse `com.adobe.marketing.mobile.edge.identity.Identity`, nicht die Legacy-`com.adobe.marketing.mobile.Identity`.

```kotlin
import com.adobe.marketing.mobile.Edge
import com.adobe.marketing.mobile.Lifecycle
import com.adobe.marketing.mobile.MobileCore
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.flags.Flag

MobileCore.setApplication(this)
MobileCore.configureWithAppID("YOUR_ENVIRONMENT_FILE_ID")
MobileCore.registerExtensions(
    listOf(Lifecycle.EXTENSION, Identity.EXTENSION, Edge.EXTENSION, Flag.EXTENSION)
) { }
```

Bei diesem Setup wird der Lebenszyklus nicht automatisch verfolgt. Rufen Sie `MobileCore.lifecycleStart(null)` in den `onResume` und `MobileCore.lifecyclePause()` jeder Aktivität in ihrer `onPause` auf. Ohne diese Aufrufe aktualisiert die Erweiterung die Flags, während sich die App im Hintergrund befindet, und die Belichtungsanalysen werden später gesendet.

## Auswertungskontext {#evaluation-context}

`FeatureEvaluationContext` enthält die Zielgruppenattribute, die Ihre Markierungsregeln verwenden. Keine Identität übergeben: Die Erweiterung liest sie bei jeder Auswertung aus „Identity for Edge Network&quot;. Siehe [Benutzerdefinierte Identität](#custom-identity).

| Methode | Erforderlich | Beschreibung |
|---|---|---|
| `withAttributes(map)` | Nein | `Map<String, List<String>>`. Jeder Schlüssel ist ein Attributname, der von Ihren Flag-Regeln verwendet wird (z. B. `locale` oder `appVersion`). Jeder Wert ist die Liste der Werte für den aktuellen Benutzer (z. B. `["en_US"]`). |

* Für jede Auswertung ist ein Kontext erforderlich. Wenn Sie keine Attribute haben, übergeben Sie `FeatureEvaluationContext.builder().build()`.
* Rufen Sie `withAttributes` höchstens einmal pro Builder auf.
* Ein erstellter Kontext kann nicht geändert werden, sodass Sie ihn für alle Auswertungen wiederverwenden können.

### Verwendung {#evaluation-context-usage}

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(
        mapOf(
            "locale" to listOf("en_US"),
            "platform" to listOf("ANDROID")
        )
    )
    .build()
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext;
import java.util.Arrays;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

Map<String, List<String>> attrs = new HashMap<>();
attrs.put("locale", Arrays.asList("en_US"));
attrs.put("platform", Arrays.asList("ANDROID"));

FeatureEvaluationContext ctx = FeatureEvaluationContext.builder()
        .withAttributes(attrs)
        .build();
```

>[!ENDTABS]

### Beispiele für Zielgruppenattribute {#sample-attributes}

| Attribut | Beschreibung | Beispielwerte |
|---|---|---|
| `locale` | Gebietsschema des Benutzers | `["en_US"]`, `["fr_FR"]` |
| `platform` | Plattform | `["ANDROID"]` |
| `appVersion` | Anwendungsversion | `["3.0.0"]` |
| `deviceType` | Gerätetyp | `["phone"]`, `["tablet"]` |

Attributnamen und -werte müssen mit den in Ihren Markierungsregeln verwendeten übereinstimmen.

## Benutzerdefinierte Identität {#custom-identity}

Die Erweiterung „Flags“ verwendet die Erweiterung „Identität für Edge Network[&#128279;](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) für die Identitätsauflösung. Eine Feature Flag kann für eine benutzerdefinierte Identität, z. B. eine CRM-ID oder eine Treueprogramm-ID, kombiniert werden, sodass Variantenaufspaltungen und Analysen mit der Identität verknüpft sind, die für Ihr Programm wichtig ist.

Der benutzerdefinierte Identity-Namespace muss in der Benutzeroberfläche „Flags“ ausgewählt werden, wenn das Feature Flag erstellt wird. Um ein Flag für diese Identität auszuwerten, muss dieselbe Identität im Edge Identity `identityMap` auf dem Gerät vorhanden sein und den entsprechenden Namespace verwenden. Bereitstellen zur Laufzeit mit der Identity for Edge Network `updateIdentities`-API.

### Hinzufügen der benutzerdefinierten Identität zur Identitätszuordnung {#add-identity}

Fügen Sie die Identität unter demselben Namespace hinzu, der für das Feature Flag konfiguriert wurde, bevor Sie das Flag auswerten.

Beachten Sie Folgendes, wenn Sie die Identität hinzufügen:

* Der Namespace muss genau übereinstimmen, einschließlich der Groß-/Kleinschreibung.
* Wenn der Namespace mehr als eine Identität hat, wird die als primär markierte Identität verwendet. Andernfalls wird das erste verwendet.
* Wenn die Identität beim Auswerten des Flags fehlt, wird der Benutzerin bzw. dem Benutzer eine temporäre ID zugewiesen, die sich beim Start der App ändert. Die Benutzervariante kann sich dann zwischen den Programmstarts ändern. Legen Sie die Identität immer fest, bevor Sie Flags auswerten, die sie verwenden.

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.edge.identity.IdentityItem
import com.adobe.marketing.mobile.edge.identity.IdentityMap

val identityMap = IdentityMap()
identityMap.addItem(
    IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
    "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(identityMap)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

IdentityMap identityMap = new IdentityMap();
identityMap.addItem(
        new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
        "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

>[!ENDTABS]

## API-Referenz {#api-reference}

### Rückrufe und Fehlerbehandlung {#callbacks-errors}

Diese Regeln gelten für `isFeatureEnabled` und `getFeature`:

* Bieten Sie immer ein Standarderlebnis. Übergeben Sie ein `AdobeCallbackWithError` und zeigen Sie Ihr Standarderlebnis in `fail` an. Bei einem einfachen `AdobeCallback` wird beim Auftreten eines Fehlers nichts aufgerufen.

* Die Erweiterung lädt Flag-Definitionen vorab, wenn die App gestartet wird. Danach werden die Flags auf dem Gerät ausgewertet.

* Andere Fehler: `fail` wird mit `AdobeError.UNEXPECTED_ERROR` aufgerufen, wenn:

  * Der Funktionstaste ist leer,
  * die Flags-Einstellungen oder die Experience Cloud-Organisations-ID in der veröffentlichten Konfiguration fehlen oder
  * Flag-Definitionen konnten beim Start der App nicht heruntergeladen werden (z. B. wenn das Gerät offline war). Die Erweiterung versucht es beim nächsten Konfigurationsupdate erneut, normalerweise beim nächsten App-Start.

### isFeatureEnabled {#is-feature-enabled}

Gibt zurück, ob eine Funktion für den aktuellen Benutzer aktiviert ist.

**Signatur**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

>[!TAB Java]

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

>[!ENDTABS]

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Schlüssel der auszuwertenden Funktion |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute. Verwenden Sie `FeatureEvaluationContext.builder().build()`, wenn Sie keine haben. Siehe [Evaluierungskontext](#evaluation-context). |
| `callback` | AdobeCallback&lt;Boolean> | Wird mit `true` aufgerufen, wenn die Funktion für den Benutzer aktiviert ist. Wird mit `false` aufgerufen, wenn die Funktion nicht gefunden wird, die Zielgruppenbestimmungsregeln nicht übereinstimmen oder der Benutzer zur Kontrollgruppe gehört. Übergeben Sie eine `AdobeCallbackWithError<Boolean>`, um auch Fehler zu erhalten. |

**Beispiele**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<Boolean> {
        override fun call(isEnabled: Boolean?) {
            runOnUiThread {
                if (isEnabled == true) showNewCheckout() else showDefaultCheckout()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultCheckout() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            runOnUiThread(() -> {
                if (Boolean.TRUE.equals(isEnabled)) {
                    showNewCheckout();
                } else {
                    showDefaultCheckout();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultCheckout());
        }
    }
);
```

>[!ENDTABS]

### getFeature {#get-feature}

Gibt die ausgewertete Funktion für den aktuellen Benutzer aus, einschließlich der Metadaten. Verwenden Sie diese API, wenn Sie mehr als aktivierte oder deaktivierte benötigen.

**Signatur**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

>[!TAB Java]

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

>[!ENDTABS]

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Schlüssel der auszuwertenden Funktion |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute. Verwenden Sie `FeatureEvaluationContext.builder().build()`, wenn Sie keine haben. Siehe [Evaluierungskontext](#evaluation-context). |
| `callback` | AdobeCallback&lt;FeatureEvaluationResult> | Wird mit der ausgewerteten Funktion aufgerufen oder mit `null`, wenn die Funktion dem Benutzer nicht bereitgestellt wird: Der Schlüssel ist unbekannt, die Zielgruppenkriterien sind nicht erfüllt oder der Benutzer befindet sich in einer Kontrollkohorte. `null` ist ein normales Ergebnis, kein Fehler. Kontrollkohorten-Expositionen werden weiterhin an Analytics gemeldet. Übergeben Sie einen `AdobeCallbackWithError<FeatureEvaluationResult>`, um `fail(...)` für echte Fehler wie Zeitüberschreitungen zu erhalten. |

Behandeln Sie ein `null` Ergebnis als „Funktion ausgeschaltet“ und zeigen Sie Ihr Standarderlebnis an. Zeigen Sie auch das Standarderlebnis beim Aufruf von `fail` an, was nur bei echten Fehlern geschieht, z. B. Zeitüberschreitungen.

**Antwort**

*FeatureEvaluationResult*

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | int | Funktions-ID |
| `key` | Zeichenfolge | Funktionsschlüssel |
| `featureGroupKey` | Zeichenfolge? | Funktionsgruppenschlüssel, wenn die Funktion zu einer Gruppe gehört |
| `meta` | Zeichenfolge? | Metadaten, die für die Funktion konfiguriert sind, als reiner Text oder `null`, wenn keine festgelegt ist. Wenn Sie JSON gespeichert haben, analysieren Sie die Zeichenfolge in Ihrer App. |
| `analyticsParam` | AnalyticsParam? | Analytics-Details für die Auswertung |

*AnalyticsParam*

| Feld | Typ | Beschreibung |
|---|---|---|
| `featureGroupId` | int | Funktionsgruppen-ID |
| `featureId` | int | Funktions-ID |
| `variantId` | Zeichenfolge? | ID der Variante, der der Benutzer zugewiesen wurde |

**Beispiele**

>[!BEGINTABS]

>[!TAB Kotlin]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            runOnUiThread {
                if (!meta.isNullOrEmpty()) applyExperience(meta) else showDefaultExperience()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultExperience() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            final String meta = feature != null ? feature.getMeta() : null;
            runOnUiThread(() -> {
                if (meta != null && !meta.isEmpty()) {
                    applyExperience(meta);
                } else {
                    showDefaultExperience();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultExperience());
        }
    }
);
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Gibt die Version der Flags-Erweiterung zurück.

**Syntax**

```kotlin
Flag.extensionVersion(): String
```

**Beispiel**

*Kotlin*

```kotlin
val version = Flag.extensionVersion()
```

*Java*

```java
String version = Flag.extensionVersion();
```

## API-Zusammenfassung {#api-summary}

| API | Rückgaben |
|---|---|
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. Siehe [isFeatureEnabled](#is-feature-enabled). | Boolescher Wert über Callback |
| `getFeature(featureKey, evaluationContext, callback)`. Siehe [getFeature](#get-feature). | FeatureEvaluationResult über Callback |
| `extensionVersion()` | String |

## Debugging {#debugging}

Um zu debuggen, legen Sie `MobileCore.setLogLevel(LoggingMode.DEBUG)` in einem Debug-Build fest und filtern Sie Logcat nach `Flags`. Sie sollten eine `Discovered extension` von MobileCore für `com.adobe.marketing.mobile.flags.FlagExtension` sehen.


