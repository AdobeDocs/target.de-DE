---
title: Flags-Erweiterung für Web-Integrationshandbuch
description: Erfahren Sie, wie Sie die Flags-Erweiterung in Adobe Experience Platform Web SDK (Alloy) für Web-Anwendungen integrieren.
badge: label="Beta" type="Informative"
hide: true
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 7%

---

# Flags-Erweiterung für Web {#web-extension-integration-guide}

In diesem Handbuch wird beschrieben, wie Sie die Flags-Erweiterung in Adobe Experience Platform Web SDK (Alloy) für Web-Anwendungen integrieren. Die Flags-Erweiterung ermöglicht die Verwaltung von Feature Flags und kontrollierte Rollouts für Web-Erlebnisse.

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Implementierung der Flags-Erweiterung Folgendes sicher:

* Eine in der Datenerfassung von [Adobe Experience Platform konfigurierte Web-Eigenschaft](https://experience.adobe.com/#/data-collection)
* Die installierte Adobe Experience Platform Web SDK-Erweiterung
* Eine Adobe Experience Cloud-Organisations-ID
* Zugriff auf Flags in Ihrer Organisation

### Erforderliche Berechtigungen {#required-permissions}

Stellen Sie sicher, dass Sie über die folgenden Eigenschaftsrechte verfügen:

* Entwickeln
* Erweiterungen verwalten

## Abhängigkeiten der Erweiterung {#extension-dependencies}

Die Flags-Erweiterung erfordert die folgende Adobe Experience Platform-Erweiterung:

| Erweiterung | Beschreibung | Erforderlich |
|---|---|---|
| Adobe Experience Platform Web SDK | Bietet Kernfunktionen, einschließlich Edge Network-Kommunikation und Identitätsverwaltung | Ja |

Stellen Sie sicher, dass diese Erweiterung in Ihrer Datenerfassungs-Web-Eigenschaft installiert ist, bevor Sie die Flags-Erweiterung installieren.

## Konfigurieren der Flags-Erweiterung in der Datenerfassung {#configure}

### Installieren der Erweiterung {#install-extension}

1. Melden Sie sich mit Ihren Adobe ID[Anmeldeinformationen bei ](https://experience.adobe.com)experience.adobe.com) an.
1. Navigieren Sie **Datenerfassung** > **Tags**.
1. Wählen Sie die gewünschte Tag-Eigenschaft aus.
1. Navigieren Sie **Erweiterungen** > **Katalog**.
1. Suchen Sie nach **Flags** und wählen Sie die Erweiterungskarte aus.
1. Wählen Sie **Installieren** aus.

### Konfigurieren von Erweiterungseinstellungen {#configure-settings}

Wenn Sie die Flags-Erweiterung installieren, werden Sie zur Konfigurationsseite weitergeleitet. Konfigurieren Sie die folgenden Einstellungen:

| Einstellung | Beschreibung | Erforderlich |
|---|---|---|
| Client-ID | Eine eindeutige Kennung für Ihre Anwendung in Flags. | Ja |

### Speichern und veröffentlichen {#save-publish}

1. Wählen **Speichern**, um die Erweiterungskonfiguration zu speichern.
1. Befolgen Sie den Veröffentlichungsablauf, um Ihre Änderungen bereitzustellen:
   1. Fügen Sie die Erweiterung einer Bibliothek hinzu.
   1. Erstellen Sie in Ihrer Entwicklungsumgebung.
   1. Validieren mit Adobe Experience Platform Debugger.
   1. Zur Staging- und Produktionsumgebung weiterleiten.

## Hinzufügen des Tag-Einbettungs-Codes zu Ihrer Website {#embed-code}

Nachdem Sie Ihre Tags-Bibliothek veröffentlicht haben, müssen Sie den Einbettungs-Code zu Ihrer Website hinzufügen. Der Einbettungs-Code ist ein `<script>`-Tag, das die Tags-Bibliothek und alle konfigurierten Erweiterungen lädt, einschließlich der Flags-Erweiterung.

### Kopieren des Einbettungs-Codes {#copy-embed-code}

1. Navigieren Sie in der Datenerfassung zu Ihrer Web-Eigenschaft.
1. Wählen **Umgebungen** im linken Navigationsbereich aus.
1. Aktivieren Sie in der Zeile für Ihre Zielumgebung (Entwicklung, Staging oder Produktion) das Kästchen-Symbol unter der Spalte **Installieren**.
1. Im Dialogfeld **Web-Installationsanweisungen** ist für Tags standardmäßig der asynchrone Einbettungs-Code festgelegt.
1. Wählen Sie das **Kopieren**-Symbol aus, um den Einbettungs-Code in die Zwischenablage zu kopieren.
1. Wählen Sie **Schließen** aus, um das Modal zu schließen.

>[!NOTE]
>
>Jede Umgebung verfügt über eine eindeutige Einbettungs-Code-URL. Weitere Informationen finden Sie unter Umgebungen .

### Implementieren des Einbettungs-Codes {#implement-embed-code}

Fügen Sie den Einbettungs-Code in das `<head>` Ihrer HTML-Seiten ein. Der Einbettungs-Code sollte vor anderen Skripten platziert werden, die von der Tag-Bibliothek abhängig sind:

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Website</title>

  <!-- Adobe Experience Platform Tags embed code -->
  <script src="https://assets.adobedtm.com/yourcompany/your-property/launchENxxxxxxxxxxx.min.js" async></script>
</head>
<body>
  <!-- Your page content -->
</body>
</html>
```

>[!NOTE]
>
>Ersetzen Sie die `src`-URL durch den tatsächlichen Einbettungs-Code auf der Seite Umgebungen . Die URL enthält Ihre Unternehmens-, Eigenschaften- und Umgebungskennung (z. B. `launch-EN123456789abcdef.min.js`).

### Auswerten von Flags mit Tags-Komponenten {#tags-components}

Die Flags-Erweiterung stellt Tag-native Auswertungsoberflächen bereit.

| Komponente | Typ | Beschreibung |
|---|---|---|
| Funktion ist aktiviert | Bedingung | Gibt zurück, ob eine Funktion für den aktuellen Benutzer/Kontext aktiviert ist |
| Feature Flag | Datenelement | Gibt ein boolesches oder vollständiges Funktionsobjekt zurück. |

## SDK initialisieren {#initialize-sdk}

Die Flags-Erweiterung wird automatisch initialisiert, wenn die Tag-Bibliothek geladen wird. Die Erweiterung stellt den Client für Folgendes bereit:

```javascript
window._flagClient
```

### Auf Client-Bereitschaft warten {#client-readiness}

Tags werden asynchron geladen. Bevor Sie SDK-Methoden aus benutzerdefiniertem Code aufrufen, warten Sie, bis der Client initialisiert wurde:

```javascript
window.flagClientReady
  .then(function () {
    const enabled = window._flagClient.isFeatureEnabled('my-feature', context);
    // Use enabled to select the feature or fallback behavior.
  })
  .catch(function (error) {
    console.error('Flags initialization failed:', error);
  });
```

## Auswertungskontext {#evaluation-context}

`FeatureEvaluationContext` umfasst Identitätsattribute (erforderlich für Auswertung, A/B-Bucketing und Analyse) und optionale Zielgruppenattribute (verwendet für den Regelabgleich).

| Eigenschaft | Erforderlich | Beschreibung |
|---|---|---|
| `identityNamespace` | Ja | Identity-Namespace (siehe [Adobe Identity-Namespaces](https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces)). Allgemeine Werte: `ECID`, `Email`, `CRMId`. |
| `identityId` | Ja | Identitätswert für den aktuellen Benutzer. |
| `attributes` | Nein | `Record<string, string[]>`. Der Schlüssel ist der von Ihren Flag-Regeln verwendete Kontextattributname (z. B. `locale`, `platform`). Wert ist die Liste der möglichen Attributwerte für diesen Schlüssel. |

Legen Sie in den Tags-Komponenten Identitätsstandardwerte in der Benutzeroberfläche für Bedingungen oder Datenelemente fest. Das Datenelement „Feature Flag“ akzeptiert auch Laufzeitattribute über `getVar(name, attributes)`, wenn das zweite Argument eine flache Attributzuordnung ist.

### Verwendung {#usage}

```javascript
const context = {
  identityNamespace: 'ECID',
  identityId: 'your-visitor-ecid',
  attributes: {
    locale: ['en-US'],
    platform: ['web']
  }
};
```

## API-Referenz {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` gibt zurück, ob eine Flags-Funktion für den angegebenen Kontext aktiviert oder deaktiviert ist. Übergeben Sie `featureKey` und ein `FeatureEvaluationContext`. Siehe [Evaluierungskontext](#evaluation-context). Verwenden Sie die **Funktion ist aktiviert** Tags-Bedingung oder rufen Sie nach der Initialisierung `window._flagClient.isFeatureEnabled(...)` aus benutzerdefiniertem Code auf.

**Signatur**

```javascript
isFeatureEnabled(featureKey: string, context: FeatureEvaluationContext): boolean
```

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | string | Funktionsschlüssel zur Auswertung in Flags |
| `context` | FeatureEvaluationContext | Identitäts- (erforderlich) und optionale Zielgruppenattribute. Siehe [Evaluierungskontext](#evaluation-context). |

### Erstellen eines Feature Flag-Datenelements {#create-data-element}

Verwenden Sie ein Datenelement, wenn Sie einen Markierungswert benötigen, der in Regeln oder benutzerdefiniertem Code verfügbar `%Data Element Name%`.

**Schritte**

1. Wechseln Sie in Ihrer Eigenschaft zu **Datenelemente** und wählen Sie **Datenelement hinzufügen** aus.
1. Konfigurieren **auf dem Bildschirm Datenelement** erstellen) die Felder Tags :

   | Feld | Wert |
   |---|---|
   | Name | Ein beschreibender Name (z. B. `checkout flag`) |
   | Erweiterung | Markierungen |
   | Datenelementtyp | Feature Flag |

1. Konfigurieren Sie die **Flags** Erweiterungsfelder:

   | Feld | Erforderlich | Beschreibung |
   |---|---|---|
   | Funktionsschlüssel | Ja | Eindeutiger Kennzeichnungsschlüssel (z. B. `checkout_flag`) |
   | Rückgabetyp | Ja | **Boolesch (true/false)** — aktiviert/deaktiviert oder **Objekt (vollständige Details)** — vollständige Payload einschließlich `meta` |

1. Wählen Sie **Speichern** aus.

**Rückgabetypen**

| Rückgabetyp | Auflösungen auf |
|---|---|
| Boolescher Wert (true/false) | `true`, falls aktiviert, andernfalls `false` |
| Objekt der Funktion (vollständige Details) | Volle ausgewertete Funktions-Payload oder `null`, wenn Regeln nicht eingehalten werden |

### Verwenden des Datenelements {#use-data-element}

In einer Regel - Verweis nach Namen, z. B. `%Test Flag%`.

In benutzerdefiniertem Code - Verwenden Sie `_satellite.getVar`. Übergeben Sie bei Laufzeitattributen eine einfache Attributzuordnung als zweites auszuwertendes Argument:

```javascript
var isEnabled = _satellite.getVar('Test Flag', {
  locale: ['en-US'],
  platform: ['web']
});

if (isEnabled) {
  // your custom code
} else {
  // your default code
}
```

### getFeature {#get-feature}

`getFeature` gibt die ausgewertete Funktions-Payload zurück, wenn Metadaten benötigt werden, die über das Aktivierte/Deaktivierte hinausgehen.

Verwenden Sie ein **Feature Flag**-Datenelement mit **Rückgabetyp: Feature Object (vollständige Details)** - siehe [Erstellen eines Feature Flag-Datenelements](#create-data-element) - oder rufen Sie `window._flagClient.getFeature(...)` aus benutzerdefiniertem Code auf, nachdem `flagClientReady` aufgelöst wurde.

**Signatur**

```javascript
getFeature(featureKey: string, context: FeatureEvaluationContext): FeatureResult | null
```

**Parameter**

| Parameter | Typ | Beschreibung |
|---|---|---|
| `featureKey` | string | Funktionsschlüssel zur Auswertung in Flags |
| `context` | FeatureEvaluationContext | Identitäts- (erforderlich) und Zielgruppenattribute. Siehe [Evaluierungskontext](#evaluation-context). |

**Antwort**

*FeatureResult*

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | Anzahl | Numerische Funktionskennung. `-1` für Kontroll-Sentinel auf Funktionsebene. |
| `key` | Zeichenfolge \| null | Funktionsschlüssel. `null` für Kontroll-Sentinel auf Funktionsebene. |
| `featureGroupKey` | Zeichenfolge \| null | Funktionsgruppenschlüssel, falls verfügbar |
| `meta` | Zeichenfolge \| null | Funktionsmetadaten, falls verfügbar |
| `analyticsParam` | AnalyticsParam \| null | Analytics-Details für die ausgewertete Funktion |

*AnalyticsParam*

| Feld | Typ | Beschreibung |
|---|---|---|
| `featureGroupId` | Anzahl | Numerische Merkmalgruppen-Kennung |
| `featureId` | Anzahl | Numerische Funktionskennung |
| `variantId` | Zahl \| null | Variantenkennung (für Kontrolle `0`) |

**Verhalten der Kontrollgruppe**

| Szenario | isFeatureEnabled | getFeature | Analytics-Ereignis isFeatureEnabled | Analytics-Ereignis-getFeature |
|---|---|---|---|---|
| Abwandlung | `true` | Normales Ergebnis | Ja | Ja |
| Steuerung auf Funktionsebene | `false` | Sentinel (`id: -1`, `key: null`) | Ja (`variantId: 0`) | Ja |
| Nicht übereinstimmende/nicht gefundene Kriterien | `false` | `null` | Nein | Nein |

**Beispiel**

```javascript
var feature = _flagClient.getFeature('new-testflag', {
  identityNamespace: 'ECID',
  identityId: visitorEcid,
  attributes: {
    locale: ['en-US']
  }
});

var meta = feature && feature.meta;
if (meta) {
  // your custom code
} else {
  // your default code
}
```

### extensionVersion {#extension-version}

Gibt die Versionszeichenfolge der Flags-Erweiterung zurück.

**Signatur**

```javascript
_flagClient.extensionVersion(): string
```

**Beispiel**

```javascript
const version = _flagClient.extensionVersion();
console.log(`Flags extension version: ${version}`);
```

## API-Zusammenfassung {#api-summary}

| API | Rückgaben |
|---|---|
| Feature Flag (Tags-Datenelement, boolesch) | Boolescher Wert |
| Feature Flag (Tags, Datenelement, Objekt) | Objekt oder `null` der Funktion |
| `window.flagClientReady` | Promise — auf Initialisierung der Erweiterung warten |
| `window._flagClient.isFeatureEnabled(featureKey, context)` | Boolescher Wert |
| `window._flagClient.getFeature(featureKey, context)` | Objekt oder `null` der Funktion |
| `window._flagClient.extensionVersion()` | Versionszeichenfolge der Erweiterung |

## Fehlerbehandlung {#error-handling}

Die Erweiterung behandelt Fehler kontrolliert:

| Szenario | Verhalten |
|---|---|
| Netzwerk bei Initialisierung nicht verfügbar | Der SDK versucht den ersten Abruf dreimal erneut, wobei der Backoff und die Initialisierung fehlschlagen. `window.flagClientReady` und `_satellite.getVar(...)` lehnt mit `Failed to initialize Flag` ab; `window._flagClient` bleibt `undefined`. |
| Fehlende Identität im Kontext | Die Auswertung erzeugt einen Fehler. Geben Sie `identityNamespace` und `identityId` an. |
| Funktion nicht gefunden | `getFeature` gibt `null` zurück; `isFeatureEnabled` gibt `false` zurück |

```javascript
try {
  const isEnabled = _flagClient.isFeatureEnabled('my-feature', context);
  // Use the result
} catch (error) {
  console.error('Evaluation failed:', error.message);
  // Use default value
}
```

## Best Practices {#best-practices}

### Konsistente Identität {#consistent-identity}

Verwenden Sie denselben Identity-Namespace und dieselbe ID in allen Auswertungen, um bei prozentualen Rollouts ein konsistentes Bucketing zu erzielen.

```javascript
const context = {
  identityNamespace: 'ECID',
  identityId: identity,
  attributes: {
    locale: ['en-US'],
    platform: ['web']
  }
};

const isEnabled = _flagClient.isFeatureEnabled('my-feature', context);
```

### Fehlende Funktionen pfleglich behandeln {#handle-missing}

Geben Sie immer ein Fallback-Verhalten an, wenn eine Funktion nicht gefunden wird oder die Auswertung fehlschlägt.

```javascript
const feature = _flagClient.getFeature('new-testflag', context);

if (feature && feature.meta) {
  // your custom code
} else {
  // Feature not enabled - use default code
}
```

### Nach Seitenladen auswerten {#evaluate-after-load}

Stellen Sie sicher, dass die Tag-Bibliothek und die Flags-Erweiterung initialisiert wurden, bevor Sie -APIs aufrufen. Verwenden Sie das **Library Loaded**-Ereignis in Regeln, einem **Feature Flag**-Datenelement oder warten Sie auf `flagClientReady`:

```javascript
window.flagClientReady.then(function () {
  var isEnabled = window._flagClient.isFeatureEnabled('my-feature', context);
  // Use the result
});
```

## Siehe auch {#see-also}

* [Erstellen des ersten Feature Flags](../../feature-flags/create-your-first-feature-flag.md)
* [Zielgruppe in Feature Flags und Feature Groups](../../audience/audience-in-feature-flags-and-feature-groups.md)
* [Berichterstellung](../../feature-flags/reporting.md)

<!-- -->
