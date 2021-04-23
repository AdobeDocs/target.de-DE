---
keywords: email;adbox;email image adbox
description: Erfahren Sie, wie Sie mit Adobe [!DNL Target] dynamisch Bilder in E-Mails testen und diese Bilder sogar spontan ändern können, wenn jemand die E-Mail öffnet.
title: Wie teste ich eine E-Mail-Image-AdBox?
feature: E-Mail implementieren
role: Developer
exl-id: 87a918d7-83dc-4277-821b-d90302c59736
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 90%

---

# Testen einer E-Mail-Bild-AdBox

Testen Sie dynamisch Bilder in E-Mails und ändern Sie diese Bilder gegebenenfalls im Handumdrehen, wenn jemand die E-Mail öffnet.

Weiterleitungen in E-Mails können genutzt werden, um Klicks nachzuverfolgen und dynamisch zu steuern, auf welche Landingpages Personen geleitet werden.

Zum Testen von E-Mail-Bildern werden modifizierte Versionen von AdBoxes verwendet. Da E-Mail-Clients keine Cookies zulassen, muss für jede E-Mail eine eindeutige Kennung erzeugt werden. Diese Nummer wird an die AdBox-URL und sämtliche in der E-Mail verwendeten Weiterleitungen angehängt, um Klicks aus der E-Mail zurückzuverfolgen.

>[!NOTE]
>
>Obwohl Target die Bildoptimierung aus technischer Sicht zum Zeitpunkt der Öffnung durchführen kann, verarbeitet jeder E-Mail-Client das Caching unterschiedlich, sodass der Erfolg dieser Methode variieren kann. Unabhängig von dem verwenden E-Mail-Anbieter bestimmt der vom Endbenutzer zum Öffnen der E-Mail verwendete Client (Gmail-App, Outlook, Hotmail usw.), ob das Bild tatsächlich beim Öffnen abgerufen wird. Gmail speichert beispielsweise fast alles zwischen, sodass es davon abhängt, wann Gmail ein Bild abruft und speichert, welches Bild Benutzern angezeigt wird.

**Beispielcode für eine Bild-AdBox in einer E-Mail:**

```
<img src="https://{clientcode}.tt.omtrdc.net/m2/​{clientcode}/ubox/​image?
mbox={email_header}&
mboxDefault=​{http%3A%2F%2Fwww.domain.com%2Fheader.jpg}&
mboxXDomain=disabled&
mboxSession={123456}&
mboxPC={123456}” border=:"0"/>
```

Hierbei sind die unten stehenden Werte spezifisch für Sie:

| Wert | Beschreibung |
|--- |--- |
| clientcode | Clientcode Ihres Unternehmens. In at.js oder mbox.js ist dies als `clientCode='yourclientcode'` gelistet. Er besteht ausschließlich aus Kleinbuchstaben ohne Sonderzeichen. |
| image | Der Angebotstyp. Er ist immer „image“ für Grafikanzeigen und „page“ für Weiterleitungen. |
| email_header | Der Name der AdBox. |
| `mboxDefault=http%3A%2F%2Fwww.domain.com%2Fheader.jpg` | Erforderlich. Ersetzen Sie die URL durch den entsprechenden Standardinhalt für Ihre AdBox. Hierbei muss es sich um einen URL-codierten, absoluten Verweis handeln. |
| `mboxXDomain=disabled` | Weist Target an, kein Cookie zu setzen. |
| `mboxSession=123456` und `mboxPC=123456` | Zwei Werte, die von Target benötigt werden, um dieses Benutzerprofil mit seinem bestehenden Profil für Ihre Site zusammenzuführen. 123456 ist die eindeutige Kennung, die für die E-Mail erzeugt wird. Fügen sie diesen Wert dynamisch in jede AdBox- und Weiterleitungs-URL ein. Diese Nummer muss für jede gesendete E-Mail eindeutig sein. Wird eine wöchentliche E-Mail an 1.000 Personen gesendet, müssen also 1.000 eindeutige Kennungen erzeugt werden.<br>Die eindeutige E-Mail-Kennung muss mboxSession und mboxPC in jeder AdBox- und Weiterleitungs-URL zugewiesen werden. Zeitstempel-NNNNN ist das empfohlene Format für diese Kennzeichnung, wobei NNNNN eine zufällige fünfstellige Zahl ist. Jedes alphanumerische Format ist zulässig. Einige Services für Massen-E-Mails sowie jede Programmiersprache sind zur Erzeugung dieser eindeutigen Kennung in der Lage. |
