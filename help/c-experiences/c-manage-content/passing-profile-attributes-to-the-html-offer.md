---
keywords: dynamische Daten;Assets;Daten;Angebote;personalisierte Angebote;persönliche Angebote;Token ersetzen
description: Erfahren Sie, wie Sie dynamische Daten an Adoben [!DNL Target] Angebot weitergeben. Untersuchen Sie Geschäftsfälle, die aufzeigen, warum Sie möglicherweise dynamische Angebot und Ansichten und Implementierungsinformationen verwenden möchten.
title: Wie übergebe ich dynamische Daten an Angebot?
feature: Erlebnisse und Angebot
exl-id: b8f9c6eb-1000-41a2-aa3f-bc42c1ef5669
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 77%

---

# Übergeben dynamischer Daten in Angebote

Sie können Besucher-Informationen, die im Profil [!DNL Adobe Target] gespeichert sind, dynamisch anzeigen. Ebenso können Aktivitätsinformationen (wie der Name der Aktivität oder der Name des Erlebnisses) auch verwendet werden, um ein einzelnes Angebot zu erstellen, das personalisierte Inhalte dynamisch basierend auf den Interessen des Besuchers, dem vergangenem Verhalten und Gesamtprofil zurückgibt.

## Geschäftsfälle

* Fördern Sie ein Angebot mit Rabatt, um das zuletzt gekaufte Produkt „erneut aufzufüllen“ oder „nachzufüllen“. Anstatt ein separates Angebot für jedes Element in Ihrem Katalog zu erstellen, können Sie ein Angebot mit dynamischem Text erstellen, das das „zuletzt gekaufte Produkt“ aus dem Profil liest und einen Link im Angebot anzeigt.
* Ein Besucher gelangt über `keyword=world` `cup` auf Ihre Landingpage. Der Begriff *World cup* wird im Angebot angezeigt.
* Personalisieren Sie eine Empfehlungsbeschriftung mit Informationen wie (1) dem letzten Artikel, der dem Einkaufswagen eines Besuchers hinzugefügt wurde (Nike Air Max 1000s), (2) der Farbvoreinstellungen des Besuchers (schwarz) und (3) der bevorzugten Kategorie des Besuchers (Hoodies). Beispiel: „Ergänzen Sie Ihre ‚Nike Air Max 1000s‘ mit diesen coolen ‚schwarzen‘ Hoodies!“

## Technische Vorteile

Da benutzerspezifische Voreinstellungen, Verhaltensweisen, Status usw. im Profil des Benutzers gespeichert sind, können Sie diese Nachricht bei seinem nächsten Besuch wiederholen. Dynamische Angebote ermöglichen eine größere Reichweite, da Sie ein einzelnes Angebot innerhalb einer Aktivität einrichten können, das personalisierte Nachrichten für alle Besucher anzeigt. Wenn sich die Absicht des Benutzers ändert, werden die Änderungen automatisch in Ihre Website-Inhalte übernommen.

## Beispiel

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* HTML-Angebotscode: `Get your ${profile.keyword} information here!`
* Der Benutzer liest: Hier finden Sie Informationen zum World Cup!

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

Weitere Informationen zu Empfehlungsdesigns finden Sie in den weiteren Beispielen in [der Designübersicht](/help/c-recommendations/c-design-overview/design-overview.md).

## Implementierung

Verwenden Sie für an eine mbox weitergegebene Profil-Parameter die folgende Syntax:

`${profile.parameter}`

Verwenden Sie für in einem Profil-Skript erstellte Profil-Parameter die folgende Syntax:

`${user.parameter}`

Wenn Sie dynamische Attribute in einem [!DNL Recommendations]-Design verwenden, müssen Sie einen umgekehrten Schrägstrich ( \ ) vor dem Dollarzeichen ( $ ) einfügen, damit der dynamische Wert korrekt dargestellt wird:

`\${user.endpoint.lastViewedEntity}`

Da diese Variablen serverseitig durch den entsprechenden Wert ersetzt werden, werden für eine ordnungsgemäße Anzeige weder Anführungszeichen noch weiteres JavaScript benötigt.

Für Werte, die Sie Angeboten bereitstellen möchten, können auch Standardwerte angegeben werden. Die Syntax lautet wie folgt:

`${user.testAttribute default="All Items!"}`

Wenn `testAttribute` nicht vorhanden oder leer ist, wird „Alle Objekte!“ angegeben. Wenn ein leerer Attributwert gültig ist und Sie ihn ausschreiben möchten, anstatt den Standardwert anzuzeigen, können Sie Folgendes verwenden:

`${user.testAttribute default="All Items!" show_blank="true"}`

Sie können auch einen Escape und Unescape für anzuzeigende Werte durchführen. Wenn Ihr Wert z. B. über ein Apostroph verfügt, würden Sie eine Escape-Funktion für den Wert verwenden, damit das JavaScript auf der Seite nicht unterbrochen wird. (Angebote werden in JavaScript geschrieben, deshalb könnte ein Apostroph mit einem einfachen Anführungszeichen verwechselt werden.) Beispiel:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`
