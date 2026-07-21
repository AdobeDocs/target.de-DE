---
title: Flags-Erweiterung für Android-Integrationshandbuch
description: Erfahren Sie, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in Android integrieren.
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 4%

---

# Flags-Erweiterung für Android {#android-extension-integration-guide}

In diesem Handbuch wird beschrieben, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in Android integrieren.

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Implementierung der Flags-Erweiterung Folgendes sicher:

* Eine Mobile-Eigenschaft, die in der Datenerfassung von [Adobe Experience Platform konfiguriert ist](https://experience.adobe.com/#/data-collection)
* Die in Ihrer Mobile-Eigenschaft installierte und konfigurierte Flags-Erweiterung
* Eine Adobe Experience Cloud-Organisations-ID
* Minimum SDK: API 21 (Android 5.0 Lollipop)

## Abhängigkeiten der Erweiterung {#extension-dependencies}

Die Flags-Erweiterung erfordert die folgenden Adobe Experience Platform-Erweiterungen:

| Erweiterung | Beschreibung | Erforderlich |
|---|---|---|
| Core für Mobilgeräte | Bietet Kernfunktionen, einschließlich Konfiguration und Ereignisverarbeitung | Ja |
| Lebenszyklus | Erfasst Anwendungslebenszyklus- und Sitzungsdaten für die Mobile SDK | Ja |
| Edge Network | Ermöglicht die Kommunikation mit Adobe Experience Platform Edge Network | Ja |
| Edge-Identität | Aktiviert die Identitätsverwaltung über eine Mobile App bei Verwendung der Edge Network-Erweiterung | Ja |

Stellen Sie sicher, dass diese Erweiterungen in Ihrer Datenerfassungs-Eigenschaft für Mobilgeräte installiert und in Ihren App-Abhängigkeiten enthalten sind.

## Konfigurieren der Flags-Erweiterung in der Datenerfassung {#configure}

### Installieren der Erweiterung {#install-extension}

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/#/data-collection) an.
1. Wählen Sie die Registerkarte **Tags** und dann Ihre Mobile-Eigenschaft aus.
1. Navigieren Sie **Erweiterungen** > **Katalog**.
1. Suchen Sie nach **Flags-Erweiterung** und wählen Sie **Installieren** aus.
1. Konfigurieren Sie die Erweiterungseinstellungen:

   | Einstellung | Beschreibung |
   |---|---|
   | Anwendungs-ID | Eine eindeutige Kennung für Ihre Anwendung in Flags |

1. Wählen Sie **Speichern** aus.
1. Befolgen Sie den [Veröffentlichungsprozess](https://experienceleague.adobe.com/de/docs/experience-platform/tags/publish/overview), um Ihre Konfiguration zu aktualisieren.

### Abrufen der Umgebungsdatei-ID {#environment-file-id}

1. Navigieren Sie in Ihrer Mobile-Eigenschaft zu **Umgebungen**.
1. Wählen Sie das Kästchen-Symbol unter der Spalte **Installieren** für Ihre Umgebung aus.
1. Kopieren Sie **Dialogfeld „Mobile-**&quot; die **Umgebungsdatei-ID**.

## Hinzufügen der Flags-Erweiterung zur App {#add-to-app}

### Hinzufügen von Abhängigkeiten {#add-dependencies}

Fügen Sie die Mobile SDK-Abhängigkeiten zu Ihrem Projekt hinzu. Die Flags-Erweiterung erfordert Mobile Core und die unten aufgeführten Edge-bezogenen Erweiterungen.

#### Gradle mit Stückliste verwenden (empfohlen) {#gradle-bom}

Fügen Sie der `build.gradle.kts`-Datei Ihrer App die folgenden Abhängigkeiten hinzu:

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation(platform("com.adobe.marketing.mobile:sdkbom:3.+"))

    // Required extensions
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")
}
```

#### Gradle (Groovy) benutzen {#gradle-groovy}

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation platform('com.adobe.marketing.mobile:sdkbom:3.+')

    // Required extensions
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'
}
```

>[!IMPORTANT]
>
>Für Produktionsanwendungen empfiehlt Adobe die Verwendung expliziter Versionsnummern anstelle von dynamischen Versionen. Weitere Informationen finden [&#x200B; unter „Verwalten &#x200B;](https://docs.gradle.org/current/userguide/dependency_management.html) Gradle-Abhängigkeiten“.

### Hinzufügen der Flags-Abhängigkeit {#add-flags-dependency}

#### Verwenden des gehosteten Maven-Repositorys (empfohlen) {#hosted-maven}

Fügen Sie das Maven-Repository mit den Flags zum `repositories` in `settings.gradle.kts` hinzu:

```kotlin
maven {
    url = uri("<HTTPS Flags Maven repository URL>")
}
```

Für eine groovy `settings.gradle`-Datei:

```groovy
maven {
    url = uri('<HTTPS Flags Maven repository URL>')
}
```

Ersetzen Sie `<HTTPS Flags Maven repository URL>` durch die sichere Repository-URL, die für die Flags-Erweiterung bereitgestellt wird.

Fügen Sie dann die versionierte Flags-Abhängigkeit zum `build.gradle.kts` Ihrer App hinzu:

```kotlin
implementation("com.adobe.marketing.mobile:flags:<version>")
```

Für eine groovy `build.gradle`-Datei:

```groovy
implementation 'com.adobe.marketing.mobile:flags:<version>'
```

Ersetzen Sie `<version>` durch die exakte Flags-Erweiterungsversion, die für Ihre Version bereitgestellt wird.

#### Verwenden des Flags-Verteilungspakets {#distribution-package}

Das Flags-Erweiterungspaket umfasst Folgendes:

* `flags-3.x.aar`
* `flags-3.x.module`
* `flags-3.x.pom`

Stellen Sie die Erweiterung mithilfe einer der folgenden Methoden für Ihr Android-Projekt zur Verfügung:

* Veröffentlichen Sie alle Dateien aus dem Verteilungspaket in einem lokalen oder privaten Maven-Repository und konfigurieren Sie Ihr Projekt für die Verwendung dieses Repositorys.
* Fügen Sie `flags-3.x.aar` direkt zu Ihrem Projekt hinzu und deklarieren Sie die in `flags-3.x.pom` angegebenen transitiven Abhängigkeiten.

### Hinzufügen von Berechtigungen {#add-permissions}

Fügen Sie Ihrer `AndroidManifest.xml`-Datei die folgenden Berechtigungen hinzu:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

### SDK initialisieren {#initialize-sdk}

Initialisieren Sie die Mobile SDK in Ihrer `Application`-Klasse, bevor Sie APIs für Flags-Erweiterungen aufrufen. Verwenden Sie die Umgebungsdatei-ID aus Ihrer Mobile-Eigenschaft mit `MobileCore.initialize`, damit die App die in der Datenerfassung veröffentlichten Flags-Einstellungen übernimmt.

#### Verwenden von MobileCore.initialize {#mobile-core-initialize}

Diese API ist ab Android BOM Version 3.8.0 verfügbar und initialisiert die SDK mit Ihrer Datenerfassungsumgebungsdatei.

>[!IMPORTANT]
>
>Verwenden Sie für Produktions-Apps nur `LoggingMode.ERROR`. Verwenden Sie keine `DEBUG` oder `VERBOSE` in Release-Builds.

**Kotlin**

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

**Java**

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID", null);
    }
}
```

### Registrieren der Application-Klasse {#register-application}

Registrieren Sie Ihre `Application` in `AndroidManifest.xml`:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

## Auswertungskontext {#evaluation-context}

`FeatureEvaluationContext` Klasse enthält Zielgruppenattribute (für die Zuordnung von Markierungsregeln verwendet).

| Methode | Erforderlich | Beschreibung |
|---|---|---|
| `withAttributes(map)` | Nein | `Map<String, List<String>>`. Der Schlüssel ist der von Ihren Flag-Regeln verwendete Kontextattributname (z. B. `locale`, `platform`, `appVersion`, `deviceType`). Wert ist die Liste der möglichen Attributwerte für diesen Schlüssel für den aktuellen Benutzer/die aktuelle Sitzung (z. B. `["en_US"]` oder `["phone"]`). |

**Kotlin**

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val attrs = mapOf(
    "locale" to listOf("en_US"),
    "platform" to listOf("ANDROID")
)

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Java**

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

### Benutzerdefinierte Identität {#custom-identity}

Die Flags-Erweiterung verwendet die Identity for Edge Network-Erweiterung für die Identitätsauflösung. Eine Feature Flag kann für eine benutzerdefinierte Identität (z. B. eine CRM-ID oder eine Treueprogramm-ID) kohortiert werden, sodass Variantenaufspaltungen und Analysen an die Identität gebunden sind, die für Ihr Programm wichtig ist.

Der benutzerdefinierte Identity-Namespace muss in der Benutzeroberfläche „Flags“ ausgewählt werden, wenn das Feature Flag erstellt wird. Um ein Flag für diese Identität auszuwerten, muss dieselbe Identität im Edge Identity `identityMap` auf dem Gerät vorhanden sein und den entsprechenden Namespace verwenden. Bereitstellen zur Laufzeit mit der Identity for Edge Network `updateIdentities`-API.

#### Hinzufügen der benutzerdefinierten Identität zur Identity Map {#add-identity}

Fügen Sie die Identität unter demselben Namespace hinzu, der für das Feature Flag konfiguriert wurde.

**Kotlin**

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

**Java**

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

final IdentityItem item = new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true);
final IdentityMap identityMap = new IdentityMap();
identityMap.addItem(item, "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

## API-Referenz {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` gibt zurück, ob eine Flags-Funktion für den angegebenen Kontext aktiviert oder deaktiviert ist. Übergeben Sie `featureKey`, einen `FeatureEvaluationContext` (optionale Zielgruppenattribute) und einen Callback. Siehe [Evaluierungskontext](#evaluation-context).

**Signatur**

*Kotlin*

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

*Java*

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Funktionsschlüssel zur Auswertung in Flags |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute nach Bedarf einschließen; `FeatureEvaluationContext.builder().build()` für einen leeren Kontext verwenden. Siehe [Evaluierungskontext](#evaluation-context). |
| `callback` | AdobeCallback&lt;Boolean> | Wird mit `true` aufgerufen, wenn die Funktion aktiviert ist, andernfalls `false`. Sie können auch `AdobeCallbackWithError<Boolean>` zur Handhabung von `fail(...)` übergeben. |

**Beispiele**

*Kotlin*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    object : AdobeCallback<Boolean> {
        override fun call(isEnabled: Boolean?) {
            if (isEnabled == true) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    new AdobeCallback<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            if (Boolean.TRUE.equals(isEnabled)) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
);
```

### getFeature {#get-feature}

`getFeature` gibt die ausgewertete Funktions-Payload für den angegebenen Kontext zurück. Verwenden Sie diese API, wenn Sie mehr als aktivierte/deaktivierte Funktionen benötigen und Funktionsmetadaten oder -werte benötigen.

**Signatur**

*Kotlin*

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

*Java*

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Funktionsschlüssel zur Auswertung in Flags |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute nach Bedarf einschließen; `FeatureEvaluationContext.builder().build()` für einen leeren Kontext verwenden. Siehe [Evaluierungskontext](#evaluation-context). |
| `callback` | AdobeCallback&lt;FeatureEvaluationResult> | Wird mit der ausgewerteten Funktion Payload aufgerufen. Kann `null` werden, wenn die Funktion nicht gefunden wird. Sie können auch `AdobeCallbackWithError<FeatureEvaluationResult>` zur Handhabung von `fail(...)` übergeben. |

**Antwort**

*FeatureEvaluationResult*

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | int | Numerische Funktionskennung |
| `key` | Zeichenfolge | Funktionsschlüssel |
| `featureGroupKey` | Zeichenfolge? | Funktionsgruppenschlüssel, falls verfügbar |
| `meta` | Zeichenfolge? | Metadaten als JSON-Zeichenfolge kennzeichnen, sofern verfügbar |
| `analyticsParam` | AnalyticsParam? | Analytics-Details für die ausgewertete Funktion |

*AnalyticsParam*

| Feld | Typ | Beschreibung |
|---|---|---|
| `featureGroupId` | int | Numerische Merkmalgruppen-Kennung |
| `featureId` | int | Numerische Funktionskennung |
| `variantId` | Zeichenfolge? | Variantenkennung |

**Beispiele**

*Kotlin*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-flag",
    ctx,
    object : AdobeCallback<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            if (!meta.isNullOrEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-flag",
    ctx,
    new AdobeCallback<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            String meta = feature != null ? feature.getMeta() : null;
            if (meta != null && !meta.isEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
);
```

### extensionVersion {#extension-version}

Gibt die Versionszeichenfolge der Flags-Erweiterung zurück.

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
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. `FeatureEvaluationContext` enthält Zielgruppenattribute für Regeln. Siehe [Funktionsauswertung](#is-feature-enabled). | Boolescher Wert über Callback |
| `getFeature(featureKey, evaluationContext, callback)`. Gibt die ausgewertete Funktions-Payload für den angegebenen Kontext zurück. Siehe [getFeature](#get-feature). | FeatureEvaluationResult über Callback |
| `extensionVersion()` | Zeichenfolge |

## Siehe auch {#see-also}

* [Apps](../../integrate/mobile-applications.md)
* [SDKs](../../integrate/sdks.md)

<!-- -->
