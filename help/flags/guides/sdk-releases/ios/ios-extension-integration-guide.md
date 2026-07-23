---
title: Flags-Erweiterung für iOS-Integrationshandbuch
description: Erfahren Sie, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in iOS integrieren.
badge: label="Beta" type="Informative"
hide: true
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 5%

---

# Flags-Erweiterung für iOS {#ios-extension-integration-guide}

In diesem Handbuch wird beschrieben, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in iOS integrieren.

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Implementierung der Flags-Erweiterung Folgendes sicher:

* Eine Mobile-Eigenschaft, die in der Datenerfassung von [Adobe Experience Platform konfiguriert ist](https://experience.adobe.com/#/data-collection)
* Die in Ihrer Mobile-Eigenschaft installierte und konfigurierte Flags-Erweiterung
* Eine Adobe Experience Cloud-Organisations-ID
* Mindestziel für die Bereitstellung: iOS 12.0

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

#### Verwenden von Swift Package Manager {#swift-package-manager}

Wählen Sie in Xcode **Datei** > **Pakete hinzufügen** und fügen Sie die folgenden Paket-URLs für Adobe Experience Platform Mobile SDK hinzu:

| Package | URL |
|---|---|
| AEPCore | `https://github.com/adobe/aepsdk-core-ios.git` |
| AEPEdge | `https://github.com/adobe/aepsdk-edge-ios.git` |
| AEPEdgeIdentity | `https://github.com/adobe/aepsdk-edgeidentity-ios.git` |

Wenn Sie dazu aufgefordert werden, wählen Sie die folgenden Bibliotheken aus, die Sie Ihrer Zielgruppe hinzufügen möchten:

* `AEPCore`, `AEPLifecycle` (ab `aepsdk-core-ios`)
* `AEPEdge` (von `aepsdk-edge-ios`)
* `AEPEdgeIdentity` (von `aepsdk-edgeidentity-ios`)

Verwenden Sie AEPCore 5.8.0 oder höher.

>[!NOTE]
>
>Wenn Sie ein Paket in Xcode hinzufügen, wählen Sie eine Abhängigkeitsregel für jedes Paket (z. B. **Bis zur nächsten Hauptversion**), die neue Nebenversionen und Patch-Versionen automatisch aufnimmt, während die nächste Hauptversion ausgeschlossen wird. Die neuesten veröffentlichten Versionen finden Sie auf der Versionsseite jeder Erweiterung auf GitHub.

### Hinzufügen des Flags-Pakets {#add-flags-package}

Verwenden Sie entweder das Swift-Paket oder die XCF-Framework-Integrationsmethode für ein App-Ziel, nicht beides.

#### Für ein Xcode-Projekt ohne Package.swift-Datei {#xcode-project}

1. Wählen Sie in Xcode **Datei** > **Pakete hinzufügen**.
1. Wählen Sie **Lokal hinzufügen** aus.
1. Wählen Sie das bereitgestellte `Packages/AEPFlags`-Verzeichnis aus, das `Package.swift` enthält.
1. Fügen Sie die `AEPFlags`-Bibliothek zu Ihrem Anwendungsziel hinzu.

Xcode speichert den lokalen Paketverweis im Projekt, sodass Ihre Anwendung keine eigene `Package.swift`-Datei benötigt.

#### Für ein Projekt mit einer Package.swift-Datei {#package-swift-project}

Fügen Sie in Ihrem vorhandenen Manifest `AEPFlags` zu Ihren Anwendungszielabhängigkeiten hinzu und fügen Sie das Binärziel mithilfe der URL und der Prüfsumme aus dem bereitgestellten Manifest hinzu:

```swift
targets: [
    .target(
        name: "YourApp",
        dependencies: [
            "AEPFlags"
        ]
    ),
    .binaryTarget(
        name: "AEPFlags",
        url: "<AEPFlags binary URL>",
        checksum: "<AEPFlags binary checksum>"
    )
]
```

Swift Package Manager löst das Binärziel für lokale Xcode-, CI- und Archiv-Builds auf.

#### Direktes Hinzufügen des XCF-Frameworks {#xcframework}

Alternativ können Sie die bereitgestellte `AEPFlags.xcframework` in den Xcode-Projekt-Navigator ziehen und dem Anwendungsziel hinzufügen. Legen **unter** > **Frameworks, Libraries und Embedded Content** das Framework auf **Embed &amp; Sign** fest.

### SDK initialisieren {#initialize-sdk}

Registrieren Sie die Mobile SDK-Erweiterungen in Ihrem `AppDelegate`, bevor Sie Flags-APIs aufrufen. Registrieren Sie sich `Flag` nach Identity, Edge und Lifecycle und konfigurieren Sie dann die SDK mit der Umgebungsdatei-ID aus Ihrer Mobile-Eigenschaft.

#### Registrieren und Konfigurieren von Erweiterungen {#register-configure}

>[!IMPORTANT]
>
>Verwenden Sie für Produktions-Apps nur `.error` Protokollebene. Verwenden Sie keine `.debug` oder `.trace` in Release-Builds.

**SWIFT**

```swift
// AppDelegate.swift
import AEPCore
import AEPLifecycle
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import UIKit

final class AppDelegate: NSObject, UIApplicationDelegate {

    func application(_: UIApplication,
                      didFinishLaunchingWithOptions _: [UIApplication.LaunchOptionsKey: Any]? = nil) -> Bool {
        // Production: use .error only. Do not use .debug or .trace in release builds.
        MobileCore.setLogLevel(.error)

        MobileCore.registerExtensions([
            Identity.self,
            Edge.self,
            Lifecycle.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "YOUR_ENVIRONMENT_FILE_ID")
            MobileCore.lifecycleStart(additionalContextData: nil)
        }

        return true
    }
}
```

**Objective-C**

```objc
// AppDelegate.m
#import "AppDelegate.h"
@import AEPCore;
@import AEPLifecycle;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;

@implementation AppDelegate

- (BOOL)application:(UIApplication *)application
    didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {

    // Production: use AEPLogLevelError only. Do not use Debug or Trace in release builds.
    [AEPMobileCore setLogLevel:AEPLogLevelError];

    [AEPMobileCore registerExtensions:@[
        AEPMobileEdgeIdentity.class,
        AEPMobileEdge.class,
        AEPMobileLifecycle.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"YOUR_ENVIRONMENT_FILE_ID"];
        [AEPMobileCore lifecycleStart:nil];
    }];

    return YES;
}

@end
```

## Auswertungskontext {#evaluation-context}

`FeatureEvaluationContext` umfasst Zielgruppenattribute (für den Abgleich von Markierungsregeln verwendet).

| Parameter | Erforderlich | Beschreibung |
|---|---|---|
| `attributes` | Nein | `[String: [String]]`. Der Schlüssel ist der von Ihren Flag-Regeln verwendete Kontextattributname (z. B. `locale`, `platform`, `appVersion`, `deviceType`). Wert ist die Liste der möglichen Attributwerte für diesen Schlüssel für den aktuellen Benutzer/die aktuelle Sitzung (z. B. `["en_US"]` oder `["phone"]`). |

**SWIFT**

```swift
import AEPFlags

let attrs: [String: [String]] = [
    "locale": ["en_US"],
    "platform": ["IOS"],
    "appVersion": ["3.0.0"]
]

let ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Objective-C**

```objc
@import AEPFlags;

NSDictionary<NSString *, NSArray<NSString *> *> *attrs = @{
    @"locale": @[@"en_US"],
    @"platform": @[@"IOS"],
    @"appVersion": @[@"3.0.0"]
};

AEPFeatureEvaluationContextBuilder *builder = [AEPFeatureEvaluationContext builder];
AEPFeatureEvaluationContext *ctx = [[builder withAttributes:attrs] build];
```

### Beispiele für Zielgruppenattribute {#sample-attributes}

| Attribut | Beschreibung | Beispielwerte |
|---|---|---|
| `locale` | Gebietsschema/Sprache des Benutzers | `["en_US"]`, `["fr_FR"]` |
| `platform` | Plattformkennung | `["IOS"]` |
| `appVersion` | Anwendungsversion | `["3.0.0"]` |
| `deviceType` | Gerätetyp | `["phone"]`, `["tablet"]` |

### Benutzerdefinierte Identität {#custom-identity}

Die Flags-Erweiterung verwendet die Identity for Edge Network-Erweiterung für die Identitätsauflösung. Eine Feature Flag kann für eine benutzerdefinierte Identität (z. B. eine CRM-ID oder eine Treueprogramm-ID) kohortiert werden, sodass Variantenaufspaltungen und Analysen an die Identität gebunden sind, die für Ihr Programm wichtig ist.

Der benutzerdefinierte Identity-Namespace muss in der Benutzeroberfläche „Flags“ ausgewählt werden, wenn das Feature Flag erstellt wird. Um ein Flag für diese Identität auszuwerten, muss dieselbe Identität im Edge Identity `identityMap` auf dem Gerät vorhanden sein und den entsprechenden Namespace verwenden. Bereitstellen zur Laufzeit mit der Identity for Edge Network `updateIdentities`-API.

#### Hinzufügen der benutzerdefinierten Identität zur Identity Map {#add-identity}

Fügen Sie die Identität unter demselben Namespace hinzu, der für das Feature Flag konfiguriert wurde.

**SWIFT**

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
                 withNamespace: "userCRMId") // must match the namespace configured on the feature flag
Identity.updateIdentities(with: identityMap)
```

**Objective-C**

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc]
    initWithId:@"1111"
    authenticatedState:AEPAuthenticatedStateAuthenticated
    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

## API-Referenz {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` gibt zurück, ob eine Flags-Funktion für den angegebenen Kontext aktiviert oder deaktiviert ist. Übergeben Sie `featureKey`, einen `FeatureEvaluationContext` (optionale Zielgruppenattribute) und einen Abschlussabschluss. Siehe [Evaluierungskontext](#evaluation-context).

**Signatur**

*SWIFT*

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void
)
```

*Objective-C*

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
               completion:(void (^)(BOOL))completion;
```

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Funktionsschlüssel zur Auswertung in Flags |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute nach Bedarf einschließen; `FeatureEvaluationContext.builder().build()` für einen leeren Kontext verwenden. Siehe [Evaluierungskontext](#evaluation-context). |
| `completion` | `(Bool) -> Void` | Wird mit `true` aufgerufen, wenn die Funktion aktiviert ist, andernfalls `false`. |

**Beispiele**

*SWIFT*

```swift
import AEPFlags

Flag.isFeatureEnabled(
    "new-flag",
    evaluationContext: ctx
) { isEnabled in
    if isEnabled {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:ctx
                      completion:^(BOOL isEnabled) {
    if (isEnabled) {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}];
```

### getFeature {#get-feature}

`getFeature` gibt die ausgewertete Funktions-Payload für den angegebenen Kontext zurück. Verwenden Sie diese API, wenn Sie mehr als aktivierte/deaktivierte Funktionen benötigen und Funktionsmetadaten oder -werte benötigen.

**Signatur**

*SWIFT*

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void
)
```

*Objective-C*

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion;
```

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Funktionsschlüssel zur Auswertung in Flags |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute nach Bedarf einschließen; `FeatureEvaluationContext.builder().build()` für einen leeren Kontext verwenden. Siehe [Evaluierungskontext](#evaluation-context). |
| `completion` | `(FeatureEvaluationResult?) -> Void` | Wird mit der ausgewerteten Feature-Payload aufgerufen, `nil` wenn die Funktion nicht gefunden wird. |

**Antwort**

*FeatureEvaluationResult*

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | int | Numerische Funktionskennung |
| `key` | Zeichenfolge | Funktionsschlüssel |
| `featureGroupKey` | Zeichenfolge? | Funktionsgruppenschlüssel, falls verfügbar |
| `meta` | Zeichenfolge? | Opake Funktionsmetadaten, falls verfügbar |
| `analyticsParam` | AnalyticsParam? | Analytics-Details für die ausgewertete Funktion |

*AnalyticsParam*

| Feld | Typ | Beschreibung |
|---|---|---|
| `featureGroupId` | int | Numerische Merkmalgruppen-Kennung |
| `featureId` | int | Numerische Funktionskennung |
| `variantId` | Zeichenfolge? | Variantenkennung |

**Beispiele**

*SWIFT*

```swift
import AEPFlags

Flag.getFeature(
    "new-flag",
    evaluationContext: ctx
) { feature in
    guard let meta = feature?.meta, !meta.isEmpty else {
        // No metadata available: fall back to the default behavior
        return
    }
    // Feature metadata is available: use it to drive the feature behavior
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:ctx
                completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    NSString *meta = feature.meta;
    if (meta.length > 0) {
        // Feature metadata is available: use it to drive the feature behavior
    } else {
        // No metadata available: fall back to the default behavior
    }
}];
```

### extensionVersion {#extension-version}

Gibt die Versionszeichenfolge der Flags-Erweiterung zurück.

**Syntax**

*SWIFT*

```swift
static var extensionVersion: String
```

*Objective-C*

```objc
+ (nonnull NSString *)flagExtensionVersion;
```

**Beispiel**

*SWIFT*

```swift
let version = Flag.extensionVersion
```

*Objective-C*

```objc
NSString *version = [AEPMobileFlag flagExtensionVersion];
```

## API-Zusammenfassung {#api-summary}

| API | Rückgaben |
|---|---|
| `isFeatureEnabled(_:evaluationContext:completion:)`. `FeatureEvaluationContext` enthält Zielgruppenattribute für Regeln. Siehe [isFeatureEnabled](#is-feature-enabled). | Boolescher Wert durch Abschluss |
| `getFeature(_:evaluationContext:completion:)`. Gibt die ausgewertete Funktions-Payload für den angegebenen Kontext zurück. Siehe [getFeature](#get-feature). | FeatureEvaluationResult? über Verschluss |
| `extensionVersion` | Zeichenfolge |

## Siehe auch {#see-also}

* [Apps](../../integrate/mobile-applications.md)
* [SDKs](../../integrate/sdks.md)
* [Handbuch zur Integration von Android-Erweiterungen](../android/android-extension-integration-guide.md)

<!-- -->
