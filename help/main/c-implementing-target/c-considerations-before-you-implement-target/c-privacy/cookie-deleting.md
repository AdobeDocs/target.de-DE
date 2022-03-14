---
keywords: Cookie;Cookies;Cookie löschen;Target-Cookie löschen;Google Chrome;Chrome;Mozilla Firefox;Firefox;Microsoft Edge;Safari
description: Erfahren Sie, wie Sie Ihre [!DNL Target] Browsercookies verwenden, damit Sie Ihre Erlebnisse überprüfen können.
title: Wie lösche ich die [!DNL Target] Cookie?
feature: Privacy & Security
role: Developer
exl-id: f2bc079e-593a-4689-a7cd-dfc6f86f6bb4
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Löschen Sie die [!DNL Target] Cookie

Sie können Ihre [!DNL Adobe Target] Browser-Cookie (Mbox) verwenden, damit Sie alle Ihre Erlebnisse während des Tests validieren können.

Wenn keine [!DNL Target] -Cookie (Mbox), werden Sie als neuer Besucher betrachtet und erhalten ein neues Erlebnis. Es gibt mehrere Möglichkeiten, Ihre Mbox zu löschen, ohne alle Browser-Cookies zu löschen.

>[!NOTE]
>
>Die folgenden Anweisungen gelten für die aufgeführten Browser und Versionen. Suchen Sie im Internet nach Anweisungen für Ihren spezifischen Browser oder Ihre jeweilige Version.

## Löschen Sie die [!DNL Target] Cookie von Google Chrome

Version 84.0.4147.105

1. Klicken Sie auf **Chrome** Menü > **Voreinstellungen**.
1. Klicken Sie auf **Datenschutz und Sicherheit** Registerkarte.
1. Klicken **Cookies und andere Site-Daten**.
1. Klicken **Alle Cookies und Site-Daten anzeigen**.
1. Erweitern Sie die `adobe.com` auswählen, wählen Sie die **mbox** Cookie und klicken Sie dann auf das Löschsymbol (X).

## Löschen Sie die [!DNL Target] Cookie von Mozilla Firefox

Version 79.0

### Löschen Sie alle Cookies, die mit `adobe.com`

1. Klicken Sie auf **Firefox** Menü > **Voreinstellungen**.
1. Klicken Sie auf **Datenschutz und Sicherheit** Registerkarte.
1. under **Cookies und Site-Daten** klicken **Daten verwalten**.
1. Wählen Sie die `adobe.com` Site, klicken Sie auf **Auswahl entfernen**.

   >[!NOTE]
   >
   >Dadurch werden alle Cookies gelöscht, die mit dem `adobe.com` Site. Wenn Sie ein einzelnes Cookie für eine Site löschen möchten, folgen Sie den unten stehenden Anweisungen.

### Löschen eines einzelnen Cookies (mbox)

1. Klicken Sie in Firefox auf **Instrumente** > **Webentwickler** > **Speicherinspektor**.
1. Klicken Sie auf **Erweitert** Registerkarte.
1. Navigieren Sie zu der Webseite, die das Cookie enthält, das Sie löschen möchten.
1. Erweitern Sie die **Cookies** und klicken Sie auf `https://experience.adobe.com`.
1. Klicken Sie mit der rechten Maustaste auf die **mbox** Cookie, und klicken Sie dann auf **Löschen**.

## Löschen Sie die [!DNL Target] Cookie von Microsoft Edge

Version 84.0.522.52

1. Klicken Sie auf **Microsoft Edge** Menü > **Voreinstellungen**.
1. Klicken Sie auf **Site-Berechtigungen** Registerkarte.
1. Klicken **Cookies und Site-Daten**.
1. Klicken **Alle Cookies und Site-Daten anzeigen**.
1. Erweitern Sie die `adobe.com` auswählen, wählen Sie die **mbox** Cookie und klicken Sie dann auf das Löschsymbol (X).

## Löschen Sie die [!DNL Target] Cookie von Apple Safari

Version 13.1.2

### Löschen Sie alle Cookies, die mit `adobe.com`

1. Klicken Sie auf **Safari** Menü > **Voreinstellungen**.
1. Klicken Sie auf **Datenschutz** Registerkarte.
1. Klicken **Website-Daten verwalten**.
1. Wählen Sie die Sites für die Cookies aus, die Sie löschen möchten, und klicken Sie auf **Entfernen**.

   >[!NOTE]
   >
   >Dadurch werden alle Cookies gelöscht, die mit dem `adobe.com` Site. Wenn Sie ein einzelnes Cookie für eine Site löschen möchten, folgen Sie den unten stehenden Anweisungen.

### Löschen eines einzelnen Cookies (mbox)

1. Klicken Sie auf **Safari** Menü > **Voreinstellungen**.
1. Klicken Sie auf **Erweitert** Registerkarte.
1. Wählen Sie die **Menü &quot;Entwickeln&quot;in der Menüleiste anzeigen** -Option.
1. Navigieren Sie zu der Webseite, die das Cookie enthält, das Sie löschen möchten.
1. Klicken Sie auf **Entwickeln** Menü > **Webinspektor anzeigen**.
1. Klicken Sie auf **Speicherung** Registerkarte.
1. Erweitern Sie die **Cookies** und klicken Sie auf `www.adobe.com`.
1. Klicken Sie mit der rechten Maustaste auf die **mbox** Cookie, und klicken Sie dann auf **Löschen**.
