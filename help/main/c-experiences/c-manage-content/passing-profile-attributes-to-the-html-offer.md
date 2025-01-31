---
keywords: dynamische Daten;Assets;Daten;Angebote;personalisierte Angebote;persönliche Angebote;Token ersetzen
description: Erfahren Sie, wie Sie in dynamische Daten an Angebote  [!DNL Adobe Target].
title: Wie übergebe ich dynamische Daten in Angebote?
feature: Experiences and Offers
exl-id: b8f9c6eb-1000-41a2-aa3f-bc42c1ef5669
source-git-commit: 2e607b92e9d3408c1e91abd4646fe8eb840f2c30
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 52%

---

# Übergeben dynamischer Daten in Angebote

Sie können Besucherinformationen, die im [!DNL Adobe Target] gespeichert sind, dynamisch anzeigen. Ebenso können Aktivitätsinformationen (wie der Name der Aktivität oder der Name des Erlebnisses) auch verwendet werden, um ein einzelnes Angebot zu erstellen, das personalisierte Inhalte dynamisch basierend auf den Interessen des Besuchers, dem vergangenem Verhalten und Gesamtprofil zurückgibt.

## Business Cases

* Fördern Sie ein Angebot mit Rabatt, um das zuletzt gekaufte Produkt „erneut aufzufüllen“ oder „nachzufüllen“. Anstatt ein separates Angebot für jedes Element in Ihrem Katalog zu erstellen, können Sie ein Angebot mit dynamischem Text erstellen, das das „zuletzt gekaufte Produkt“ aus dem Profil liest und einen Link im Angebot anzeigt.
* Ein Besucher gelangt über `keyword=world` `cup` auf Ihre Landingpage. Der Begriff *World cup* wird im Angebot angezeigt.
* Personalisieren Sie ein Recommendations-Label mit Informationen wie (1) dem letzten Artikel, der zum Warenkorb eines Besuchers hinzugefügt wurde (Nike Air Max 1000s), (2) der Farbpräferenz des Besuchers (schwarz) und (3) der bevorzugten Nicht-Schuh-Kategorie des Besuchers (Hoodies). Beispiel: „Ergänzen Sie Ihre ‚Nike Air Max 1000s‘ mit diesen coolen ‚schwarzen‘ Hoodies!“

## Technische Vorteile

Da besucherspezifische Voreinstellungen, Verhaltensweisen und Status im Besucherprofil gespeichert werden können, können Sie diese Nachricht bei den nächsten Besuchen wiederholen. Dynamische Angebote ermöglichen eine größere Reichweite, da Sie ein einzelnes Angebot innerhalb einer Aktivität einrichten können, das personalisierte Nachrichten für alle Besucher anzeigt. Wenn sich die Absicht des Benutzers ändert, werden die Änderungen automatisch in Ihre Website-Inhalte übernommen.

## Beispiel

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* HTML-Angebotscode: `Get your ${profile.keyword} information here!`
* Besucher sieht: Hier erhalten Sie Ihre WM-Infos!

Bei folgenden Werten ist eine Tokenersetzung möglich:

| Wert | Beispiele |
|--- |--- |
| In-Mbox-Profilparameter | `${profile.age}` |
| Skript-Profilparameter | `${user.lifetimeSpend}` |
| mbox-Parameter | `${mbox.favoriteColor}` |
| Kampagneninformationen | `${campaign.name}`, `${campaign.recipe.name}`, `${campaign.id}`, `${campaign.recipe.id}`, und `${campaign.recipe.trafficType}` |
| Unique Visitor-ID | `${user.pcId}` |
| Eindeutige Sitzungs-ID | `${user.sessionId}` |
| Erste Sitzung des Besuchers (TRUE oder FALSE) | `${user.isFirstSession}` |
| Vergangenes Verhalten | `${user.endpoint.lastPurchasedEntity}`, `${user.endpoint.lastViewedEntity}`, `${user.endpoint.mostViewedEntity}`, `${user.endpoint.categoryAffinity}` |

Informationen in der Konsole zum Debugging, wie `${campaign.name}`, `${campaign.id}`, `${campaign.recipe.name}`, `${campaign.recipe.id}`, `${offer.name}`, `${offer.id}`, `${campaign.name}`

Weitere Beispiele für [!DNL Recommendations]-Designs finden Sie unter [Design-Übersicht](/help/main/c-recommendations/c-design-overview/design-overview.md).

## Implementierung

Verwenden Sie für Profilparameter, die an eine Mbox übergeben werden, die Syntax:

`${profile.parameter}`

Verwenden Sie für in einem Profilskript erstellte Profilparameter die Syntax :

`${user.parameter}`

Bei Verwendung dynamischer Attribute in einem [!DNL Recommendations] müssen Sie einen umgekehrten Schrägstrich ( \ ) vor dem Dollarzeichen ( $ ) einfügen, damit der dynamische Wert ordnungsgemäß gerendert werden kann:

`\${user.endpoint.lastViewedEntity}`

Da diese Variablen serverseitig durch den entsprechenden Wert ersetzt werden, werden für eine ordnungsgemäße Anzeige weder Anführungszeichen noch weiteres JavaScript benötigt.

Standardwerte können auch für Werte angegeben werden, die für Angebote verfügbar gemacht werden sollen. Die Syntax lautet wie folgt:

`${user.testAttribute default="All Items!"}`

Wenn `testAttribute` nicht vorhanden oder leer ist, „Alle Elemente!“ wird ausgeschrieben. Wenn ein leerer Attributwert gültig ist und Sie ihn ausschreiben möchten, anstatt den Standardwert anzuzeigen, können Sie Folgendes verwenden:

`${user.testAttribute default="All Items!" show_blank="true"}`

Sie können auch einen Escape und Unescape für anzuzeigende Werte durchführen. Wenn Ihr Wert beispielsweise über ein Apostroph verfügt, können Sie den Wert mit Escape-Zeichen versehen, damit der JavaScript auf der Seite nicht beschädigt wird. (Angebote werden in JavaScript geschrieben, sodass ein einzelnes Apostroph für ein Angebot verwechselt werden kann.) Beispiel:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`

Für Angebotsparameter (offer.name, offer.id), die im Inhalt eines Angebots verwendet werden:

Wenn dieses Angebot eines von mehreren Angeboten ist, die für ein Erlebnis festgelegt wurden, wird der Wert des zuletzt hinzugefügten Angebots in den Parameterwert eingefügt. Das bedeutet, dass diese Parameter auf Erlebnisebene ausgewertet werden.