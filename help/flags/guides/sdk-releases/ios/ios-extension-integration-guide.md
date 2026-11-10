---
title: Flags-Erweiterung für iOS-Integrationshandbuch
description: Erfahren Sie, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in iOS integrieren.
badge: label="Beta" type="Informative"
hide: true
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: c1fafcfcd7d5d22781abdd10e6eb3c2b84136c2d
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 3%
---
# Flags-Erweiterung für iOS {#ios-extension-integration-guide}

In diesem Handbuch wird beschrieben, wie Sie die Flags-Erweiterung in Adobe Experience Platform Mobile SDK in iOS integrieren. Der Quell-Code ist im Repository [aepsdk-flags-](https://github.com/adobe/aepsdk-flags-ios)) verfügbar.

## Voraussetzungen {#prerequisites}

Bevor Sie beginnen, stellen Sie Folgendes sicher:

* iOS 12.0 oder höher und Swift 5.7 oder höher
* Eine Mobile-Eigenschaft in der Datenerfassung von [Adobe Experience Platform](https://experience.adobe.com/#/data-collection)
* Diese Erweiterungen werden in der Mobile-Eigenschaft installiert und konfiguriert:

  | Erweiterung | Beschreibung | SDK-Mindestversion |
  |---|---|---|
  | [Mobile Core](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | Konfiguration und Ereignisverarbeitung | AEPCore 5.8.0 |
  | [Lebenszyklus](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | Lebenszyklusdaten der Anwendung | Wie AEPCore |
  | [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Kommunikation mit Adobe Experience Platform Edge Network. Erfordert einen Datenstrom. | AEPEdge 5.0.2 |
  | [Identität für Edge Network](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | Identitätsverwaltung für Edge Network | AEPEdgeIdentity 5.0.0 |
  | [Flags](https://experienceleague.adobe.com/en/docs/target/flags/home) | Auswertung der Feature Flag | Siehe [Installation](#installation) |

## Konfigurieren von Flags in der Datenerfassung {#configure}

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

1. Befolgen Sie den [Veröffentlichungsprozess](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview), um Ihre Konfiguration zu aktualisieren.

### Abrufen der Umgebungsdatei-ID {#environment-file-id}

1. Navigieren Sie in Ihrer Mobile-Eigenschaft zu **[!UICONTROL Umgebungen]**.

1. Aktivieren Sie das Feldsymbol in der Spalte **[!UICONTROL Installieren]** der ausgewählten Umgebung.

   ![](../assets/extension-install-2.png)

1. Kopieren Sie **[!UICONTROL Dialogfeld „Mobile-]**&quot; die **[!UICONTROL Umgebungsdatei-ID]**.

   ![](../assets/extension-install-3.png)

## Installation {#installation}

Fügen Sie die Erweiterung entweder mit Swift Package Manager oder einem XCF-Framework hinzu. Verwenden Sie eine Methode pro App-Ziel.

### Swift Package Manager {#swift-package-manager}

In Xcode:

1. Wählen Sie **Datei** > **Paketabhängigkeiten hinzufügen**.

1. Package-URL eingeben: `https://github.com/adobe/aepsdk-flags-ios.git`

1. Wählen Sie für die Versionsregel die Option **Exakte Version** und geben Sie die neueste Version auf der Seite [Versionen](https://github.com/adobe/aepsdk-flags-ios/releases) ein.

1. Fügen Sie die `AEPFlags`-Bibliothek zu Ihrem App-Ziel hinzu.

1. Fügen Sie die Adobe-Pakete hinzu, von denen die Erweiterung abhängt, und fügen Sie ihre Bibliotheken zu Ihrem App-Ziel hinzu:

   * `https://github.com/adobe/aepsdk-core-ios.git`: `AEPCore`, `AEPLifecycle` und `AEPServices`
   * `https://github.com/adobe/aepsdk-edge-ios.git`: `AEPEdge`
   * `https://github.com/adobe/aepsdk-edgeidentity-ios.git`: `AEPEdgeIdentity`

Wenn Ihr Projekt eine `Package.swift`-Datei verwendet, fügen Sie stattdessen die Abhängigkeiten dort hinzu. Ersetzen Sie `<latest-version>` durch die neueste Version auf der Seite Versionen .

```swift
dependencies: [
    .package(url: "https://github.com/adobe/aepsdk-flags-ios.git", exact: "<latest-version>"),
    .package(url: "https://github.com/adobe/aepsdk-core-ios.git", .upToNextMajor(from: "5.8.0")),
    .package(url: "https://github.com/adobe/aepsdk-edge-ios.git", .upToNextMajor(from: "5.0.2")),
    .package(url: "https://github.com/adobe/aepsdk-edgeidentity-ios.git", .upToNextMajor(from: "5.0.0"))
],
targets: [
    .target(
        name: "YourTarget",
        dependencies: [
            .product(name: "AEPFlags", package: "aepsdk-flags-ios"),
            .product(name: "AEPCore", package: "aepsdk-core-ios"),
            .product(name: "AEPLifecycle", package: "aepsdk-core-ios"),
            .product(name: "AEPServices", package: "aepsdk-core-ios"),
            .product(name: "AEPEdge", package: "aepsdk-edge-ios"),
            .product(name: "AEPEdgeIdentity", package: "aepsdk-edgeidentity-ios")
        ]
    )
]
```

### XCF-Framework {#xcframework}

1. Laden Sie auf der [Versionsseite](https://github.com/adobe/aepsdk-flags-ios/releases) die `AEPFlags-<version>.xcframework.zip` herunter und entpacken Sie sie.

1. Laden Sie die XCF-Frameworks, von denen die Erweiterung abhängt, von der jeweiligen Repository-Versionsseite herunter:

   * [aepsdk-core-ios](https://github.com/adobe/aepsdk-core-ios/releases): `AEPCore`, `AEPServices`, `AEPLifecycle` und `AEPRulesEngine`
   * [aepsdk-edge-ios releases](https://github.com/adobe/aepsdk-edge-ios/releases): `AEPEdge`
   * [aepsdk-edgeidentity-ios-Versionen](https://github.com/adobe/aepsdk-edgeidentity-ios/releases): `AEPEdgeIdentity`

1. Wählen Sie in Xcode Ihr App-Ziel aus und öffnen Sie dann **Allgemein** > **Frameworks, Bibliotheken und eingebettete Inhalte**.

1. Fügen Sie `AEPFlags.xcframework` und alle abhängigen XCF-Frameworks hinzu.

1. Setzen Sie jedes Framework auf **Einbetten und Signieren**.

## SDK initialisieren {#initialize-sdk}

Registrieren Sie die Flags-Erweiterung und initialisieren Sie dann SDK mit der Umgebungsdatei-ID aus Ihrer Mobile-Eigenschaft. `MobileCore.initialize` registriert die Flags-Erweiterung nicht für Sie, registrieren Sie sie also zuerst.

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
import AEPCore
import AEPFlags
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([Flag.self])
        MobileCore.initialize(appId: "<your-environment-file-id>")
        return true
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPFlags;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[AEPMobileFlag.class] completion:nil];
    [AEPMobileCore initializeWithAppId:@"<your-environment-file-id>" completion:nil];
    return YES;
}
```

>[!ENDTABS]

### Manuelles Registrieren von Erweiterungen {#register-manually}

Wenn Sie Erweiterungen selbst registrieren, registrieren Sie alle. Rufen Sie `MobileCore.lifecycleStart` auf, wenn die App in den Vordergrund eintritt, und `MobileCore.lifecyclePause`, wenn sie in den Hintergrund eintritt.

Wenn Ihre App Szenen verwendet, führen Sie diese Aufrufe stattdessen in `sceneWillEnterForeground(_:)` und `sceneDidEnterBackground(_:)` durch.

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
import AEPCore
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import AEPLifecycle
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([
            Lifecycle.self,
            Edge.self,
            AEPEdgeIdentity.Identity.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "<your-environment-file-id>")
            DispatchQueue.main.async {
                if application.applicationState != .background {
                    MobileCore.lifecycleStart(additionalContextData: nil)
                }
            }
        }
        return true
    }

    func applicationWillEnterForeground(_ application: UIApplication) {
        MobileCore.lifecycleStart(additionalContextData: nil)
    }

    func applicationDidEnterBackground(_ application: UIApplication) {
        MobileCore.lifecyclePause()
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;
@import AEPLifecycle;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[
        AEPMobileLifecycle.class,
        AEPMobileEdge.class,
        AEPMobileEdgeIdentity.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"<your-environment-file-id>"];
        dispatch_async(dispatch_get_main_queue(), ^{
            if (application.applicationState != UIApplicationStateBackground) {
                [AEPMobileCore lifecycleStart:nil];
            }
        });
    }];
    return YES;
}

- (void)applicationWillEnterForeground:(UIApplication *)application {
    [AEPMobileCore lifecycleStart:nil];
}

- (void)applicationDidEnterBackground:(UIApplication *)application {
    [AEPMobileCore lifecyclePause];
}
```

>[!ENDTABS]

## Auswertungskontext {#evaluation-context}

Jeder Auswertungsaufruf dauert eine `FeatureEvaluationContext`. Es enthält die Attribute, die die Targeting-Regeln Ihrer Flags verwenden.

| Parameter | Erforderlich | Beschreibung |
|---|---|---|
| `attributes` | Nein | `[String: [String]]`. Jeder Schlüssel ist ein Attributname, der von Ihren Zielgruppenbestimmungsregeln für Flag verwendet wird. Jeder Wert ist die Liste der Werte für den aktuellen Benutzer. |

* Verwenden Sie Attributnamen und -werte, die den in Flags definierten Zielgruppenbestimmungsregeln entsprechen.
* Rufen Sie `withAttributes` höchstens einmal pro Builder auf. Mit einem zweiten Aufruf wird die App beendet.
* Um ohne Attribute auszuwerten, rufen Sie `build()` auf, ohne `withAttributes` aufzurufen.

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
import AEPFlags

let context = FeatureEvaluationContext.builder()
    .withAttributes([
        "locale": ["en_US"],
        "appVersion": ["3.0.0"]
    ])
    .build()
```

>[!TAB Objective-C]

```objc
@import AEPFlags;

AEPFeatureEvaluationContext *context = [[[AEPFeatureEvaluationContext builder]
    withAttributes:@{
        @"locale": @[@"en_US"],
        @"appVersion": @[@"3.0.0"]
    }]
    build];
```

>[!ENDTABS]

## Benutzerdefinierte Identität {#custom-identity}

Die Flags-Erweiterung verwendet die Identity for Edge Network-Erweiterung für die Identitätsauflösung. Eine Feature Flag kann für eine benutzerdefinierte Identität (z. B. eine CRM-ID oder eine Treueprogramm-ID) kohortiert werden, sodass Variantenaufspaltungen und Analysen an die Identität gebunden sind, die für Ihr Programm wichtig ist.

Der benutzerdefinierte Identity-Namespace muss in der Benutzeroberfläche „Flags“ ausgewählt werden, wenn das Feature Flag erstellt wird. Um ein Flag für diese Identität auszuwerten, muss dieselbe Identität im Edge Identity `identityMap` auf dem Gerät vorhanden sein und den entsprechenden Namespace verwenden. Bereitstellen zur Laufzeit mit der Identity for Edge Network `updateIdentities`-API.

### Hinzufügen der benutzerdefinierten Identität zur Identity Map {#add-identity}

Fügen Sie die Identität unter demselben Namespace hinzu, der für das Feature Flag konfiguriert wurde.

Beachten Sie das folgende Verhalten:

* Der Namespace muss mit dem im Flag konfigurierten genau übereinstimmen, einschließlich Groß- und Kleinbuchstaben.
* Wenn der Namespace mehrere Identitäten enthält, wird die als primär markierte Identität verwendet. Wenn keine als primär markiert ist, wird die erste verwendet.
* Wenn die Identität fehlt, schlägt der Aufruf nicht fehl. Der Benutzer wird nur für die aktuelle Programmsitzung zufällig einer Variante zugewiesen und kann nach dem Neustart der App einer anderen Variante zugewiesen werden. Legen Sie die Identität fest, bevor Sie Flags auswerten, die sie verwenden.

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(
    item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
    withNamespace: "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(with: identityMap)
```

>[!TAB Objective-C]

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc] initWithId:@"1111"
                                         authenticatedState:AEPAuthenticatedStateAuthenticated
                                                    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

>[!ENDTABS]


## API-Referenz {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

Prüft, ob eine Funktion für den aktuellen Benutzer aktiviert ist. Das Ergebnis wird `true`, wenn die Funktion vorhanden ist, die Benutzerin bzw. der Benutzer den Zielgruppenbestimmungsregeln entspricht und sich die Person nicht in einer Kontrollgruppe befindet. Andernfalls wird das Ergebnis `false`.

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
              completion:(void (^)(BOOL))completion
           errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Funktionsschlüssel zur Auswertung in Flags |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute nach Bedarf einschließen; `FeatureEvaluationContext.builder().build()` für einen leeren Kontext verwenden. Siehe [Evaluierungskontext](#evaluation-context). |
| `completion` | `(Bool) -> Void` | Wird mit `true` aufgerufen, wenn die Funktion aktiviert ist, andernfalls `false`. |
| `errorCallback` | `((AEPError) -> Void)?` | Optional. Wird nur bei echten Fehlern aufgerufen, z. B. bei einem leeren Schlüssel, fehlender Konfiguration, einer fehlgeschlagenen Auswertung oder einer Zeitüberschreitung. |

**Beispiele**

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
Flag.isFeatureEnabled("new-flag", evaluationContext: context) { isEnabled in
    DispatchQueue.main.async {
        if isEnabled {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:context
                     completion:^(BOOL isEnabled) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (isEnabled) {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### getFeature {#get-feature}

>[!IMPORTANT]
>
>In früheren Versionen wurde der Fehler Callback mit `AEPError.unexpected` aufgerufen, wenn eine Funktion nicht bereitgestellt wurde. Wenn Ihre App diesen Fehler als „fehlende Funktion“ behandelt, behandeln Sie `nil` stattdessen in der Fertigstellung.

Gibt die Details einer Funktion für den aktuellen Benutzer zurück, einschließlich der Metadaten und der Variante, der der Benutzer zugewiesen ist. Verwenden Sie es, wenn Sie mehr als aktiviert oder deaktiviert benötigen.

Der Abschluss wird nur dann mit einem Ergebnis aufgerufen, wenn die Funktion dem Benutzer bereitgestellt wird. Wenn die Funktion nicht bereitgestellt wird, wird der Abschluss mit `nil` aufgerufen. Dies ist ein normales Ergebnis, kein Fehler, und der Fehler-Callback wird nicht aufgerufen. Der Abschluss wird mit `nil` aufgerufen, wenn:

* Keine Funktion verfügt über diesen Schlüssel.
* Der Benutzer entspricht nicht den Zielgruppenbestimmungsregeln.
* Der Benutzer gehört zu einer Kontrollgruppe.

Der Fehler-Callback wird nur dann mit `AEPError.unexpected` (oder einem anderen `AEPError`) aufgerufen, wenn etwas schiefgeht: Der Funktionsschlüssel ist leer, ein erforderlicher Konfigurationswert fehlt, die Auswertung schlägt fehl, die Antwort kann nicht gelesen werden oder die Anfrage kommt mit einer Zeitüberschreitung aus.

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion
     errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | Zeichenfolge | Funktionsschlüssel zur Auswertung in Flags |
| `evaluationContext` | FeatureEvaluationContext | Zielgruppenattribute nach Bedarf einschließen; `FeatureEvaluationContext.builder().build()` für einen leeren Kontext verwenden. Siehe [Evaluierungskontext](#evaluation-context). |
| `completion` | `(FeatureEvaluationResult?) -> Void` | Wird mit der ausgewerteten Funktion Payload aufgerufen. Wird mit `nil` aufgerufen, wenn die Funktion dem Benutzer nicht bereitgestellt wird (unbekannter Schlüssel, Zielgruppenbestimmung nicht zugeordnet oder Kontrollgruppe). `nil` ist kein Fehler. |
| `errorCallback` | `((AEPError) -> Void)?` | Optional. Wird nur bei echten Fehlern aufgerufen, z. B. bei einem leeren Schlüssel, fehlender Konfiguration, einer fehlgeschlagenen Auswertung oder einer Zeitüberschreitung. Wird nicht aufgerufen, wenn die Funktion nicht bereitgestellt wird. |

**Antwort**

*FeatureEvaluationResult*

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | int | Die Funktions-ID |
| `key` | String | Der Funktionstaste |
| `featureGroupKey` | Zeichenfolge? | Der Schlüssel der Funktionsgruppe, die das Feature enthält |
| `meta` | Zeichenfolge? | Die für die Funktion konfigurierten Metadaten als Text. Wenn Ihre Metadaten JSON sind, decodieren Sie sie in Ihrer App. |
| `analyticsParam` | AnalyticsParam? | Kennungen der Funktion und der Variante des Benutzers |

**Beispiele**

>[!BEGINTABS]

>[!TAB SWIFT]

```swift
Flag.getFeature("new-flag", evaluationContext: context) { feature in
    DispatchQueue.main.async {
        guard let meta = feature?.meta, !meta.isEmpty else {
            // The feature is not served to this user (feature is nil), or it has no metadata.
            // Run the default behavior
            return
        }
        // Use the metadata to drive the feature behavior
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // A genuine failure occurred. Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:context
               completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (feature.meta.length > 0) {
            // Use the metadata to drive the feature behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Gibt die Version der Flags-Erweiterung zurück.

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
| `isFeatureEnabled(_:evaluationContext:completion:errorCallback:)` | Boolescher Wert bis zum Abschluss |
| `getFeature(_:evaluationContext:completion:errorCallback:)` | FeatureEvaluationResult? bis zur Fertigstellung |
| `extensionVersion` | String |
