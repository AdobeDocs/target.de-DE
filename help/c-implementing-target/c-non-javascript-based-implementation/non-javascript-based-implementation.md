---
keywords: Implementation;mbox.js non javascript;adbox;redirector;mbox
description: Informationen zum Implementieren von Target in Nicht-JavaScript-Szenarien, beispielsweise AdBox- oder Weiterleitungsverwendung.
title: E-Mail Target-Implementierung
feature: email implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 82%

---


# E-Mail: Target-Implementierung{#email-implement-target}

Informationen zum Implementieren von Target in Nicht-JavaScript-Szenarien, beispielsweise AdBox- oder Weiterleitungsverwendung.

Sie können Besuche von Werbeanzeigen und anderen Offsite-Inhalten nachverfolgen. Darüber hinaus können Sie denselben Benutzer beim Besuchen und Verlassen Ihrer Site verfolgen und das gesamte Web-Erlebnis für ihn konsistent gestalten. Mithilfe einer einzelnen URL gestattet die AdBox das Testen ohne JavaScript oder [!DNL at.js] oder [!DNL mbox.js].

Eine AdBox ist hilfreich für Sites ohne [!DNL at.js] oder [!DNL mbox.js], beispielsweise Affiliates. Wenn für Ihre Aktivität dynamische Werbeinhalte benötigt werden (Sie also beispielsweise ein Produkt in der Werbeanzeige zeigen möchten, das im Warenkorb gelassen wurde), kann eine AdBox nicht verwendet werden.

AdBox-Anzeigen und Weiterleitungen können mit jeder beliebigen Aktivität verwendet werden. In der folgenden Tabelle werden AdBox und Weiterleitungen verglichen, und es wird angegeben, wann sie verwendet werden sollten:

|  | Zielsetzung | Verwendungsbereiche | URL-Struktur | Angebotstyp | Angebotsinhalt |
|--- |--- |--- |--- |--- |--- |
| AdBox | Gibt verschiedene Bilder für die Werbeanzeige aus | Um die Inhalte einer Werbeanzeige zu ändern | `clientcode&#x200B;.tt.&#x200B;omtrdc&#x200B;.net/&#x200B;m2&#x200B;/&#x200B;clientcode/ubox/&#x200B;image?` | Umleitungsangebot | URL für ein Bild |
| Weiterleitung | Leitet einen Besucher an eine andere Webseite weiter | Um die Landingpage einer Werbeanzeige zu ändern | `clientcode&#x200B;.tt.omtrdc.net/&#x200B;m2/clientcode&#x200B;/ubox/page?` | Umleitungsangebot | URL für eine Seite |

## Best Practices zur Sicherheit {#security}

Beachten Sie, dass Sie mit der Weiterleitung dem Risiko einer Open-Redirect-Verwundbarkeit ausgesetzt sein können. Um die unbefugte Verwendung von Weiterleitungs-Links durch Dritte zu vermeiden, empfehlen wir die Verwendung von &quot;autorisierten Hosts&quot;, um die Standard-URL-Domänen für die Weiterleitung zu Zulassungslisten. Zielgruppe verwendet Hosts für Zulassungslisten-Domänen, zu denen Sie Umleitungen zulassen möchten. Weitere Informationen finden Sie unter Zulassungslisten [erstellen, die Hosts angeben, die zum Senden von Mbox-Aufrufen an die Zielgruppe](/help/administrating-target/hosts.md#allowlist) in *Hosts* berechtigt sind.

## Einschränkungen {#section_38F559DCF1324271926608BCD4AB1227}

* Es gibt keinen clientseitigen Timeout wie bei Standard-Mboxes. Wenn Target vollständig ausfällt, sehen Besucher keine Inhalte der Werbeanzeige, auch keine Standardinhalte.
* Die Besuche werden mithilfe von Drittanbieter-Cookies nachverfolgt. Unterscheiden sich die PCIDs, wird das Drittanbieterprofil des Besuchers standardmäßig mit bestehenden Erstanbieterprofilen zusammengeführt.
* Um Erstanbieter-Cookies für die AdBox selbst zu verwenden, müssen Sie die mBox-Sitzung in die URL aufnehmen. Ihr Kundenbetreuer gibt Ihnen gerne weiterführende Informationen zu diesem Thema.
* Um Erstanbieter-Cookies zur Verfolgung von Werbeanzeigen-Klicks zu verwenden, müssen Sie die Mbox-Sitzung in die URL aufnehmen. Ihr Kundenbetreuer gibt Ihnen gerne weiterführende Informationen zu diesem Thema.
* Um mehr als eine AdBox auf derselben Seite zu verwenden, müssen Sie die Mbox-Sitzung in die URL aufnehmen. Ihr Kundenbetreuer gibt Ihnen gerne weiterführende Informationen zu diesem Thema. Sie können eine AdBox und einen Weiterleitungslink auf derselben Seite haben (da es sich bei einer Weiterleitung eigentlich um eine zweite Seite handelt).