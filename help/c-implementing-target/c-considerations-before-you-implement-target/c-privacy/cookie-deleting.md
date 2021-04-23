---
keywords: Cookie;Cookies;Löschen von Cookies;Löschen von Zielgruppen-Cookies;Google-Chrome;Chrome;Mozilla Firefox;Firefox;Microsoft edge;Safari
description: Erfahren Sie, wie Sie Ihre  [!DNL Target] Browser-Cookies löschen, damit Sie Ihre Erlebnisse validieren können.
title: Wie lösche ich das [!DNL Target] Cookie?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: f2bc079e-593a-4689-a7cd-dfc6f86f6bb4
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Löschen Sie das [!DNL Target]-Cookie

Sie können Ihr [!DNL Adobe Target] Browser-Cookie (mbox) löschen, damit Sie alle Erlebnisse während des Tests validieren können.

Wenn kein [!DNL Target]-Cookie (mbox) vorhanden ist, werden Sie als neuer Besucher betrachtet und ein neues Erlebnis angezeigt. Es gibt mehrere Möglichkeiten, Ihre Mbox zu löschen, ohne alle Cookies im Browser zu löschen.

>[!NOTE]
>
>Die folgenden Anweisungen gelten für die aufgelisteten Browser und Versionen. Suchen Sie im Internet nach Anweisungen für Ihren Browser oder Ihre Version.

## Löschen Sie das [!DNL Target]-Cookie aus Google Chrome

Version 84.0.4147.105

1. Klicken Sie auf das Menü **Chrome** > **Voreinstellungen**.
1. Klicken Sie auf die Registerkarte **Datenschutz und Sicherheit**.
1. Klicken Sie auf **Cookies und andere Site-Daten**.
1. Klicken Sie auf **Alle Cookies und Site-Daten** anzeigen.
1. Erweitern Sie den Abschnitt `adobe.com`, wählen Sie das **mbox**-Cookie und klicken Sie dann auf das Löschen-Symbol (X).

## Löschen Sie das [!DNL Target]-Cookie aus Mozilla Firefox

Version 79.0

### Löschen Sie alle mit `adobe.com` verknüpften Cookies

1. Klicken Sie auf das Menü **Firefox** > **Voreinstellungen**.
1. Klicken Sie auf die Registerkarte **Datenschutz und Sicherheit**.
1. Klicken Sie unter **Cookies und Site-Daten** auf **Daten verwalten**.
1. Wählen Sie die Site `adobe.com` und klicken Sie dann auf **Auswahl entfernen**.

   >[!NOTE]
   >
   >Dadurch werden alle mit der `adobe.com`-Site verknüpften Cookies gelöscht. Wenn Sie ein einzelnes Cookie für eine Site löschen möchten, befolgen Sie die unten stehenden Anweisungen.

### Löschen eines einzelnen Cookies (mbox)

1. Klicken Sie in Firefox auf **Tools** > **Webentwickler** > **Datenspeicherung-Inspektor**.
1. Klicken Sie auf die Registerkarte **Erweitert**.
1. Navigieren Sie zu der Webseite, auf der sich das zu löschende Cookie befindet.
1. Erweitern Sie den Abschnitt **Cookies** und klicken Sie dann auf `https://experience.adobe.com`.
1. Klicken Sie mit der rechten Maustaste auf das Cookie **mbox** und klicken Sie dann auf **Löschen**.

## [!DNL Target]-Cookie aus Microsoft Edge löschen

Version 84.0.522.52

1. Klicken Sie auf das Menü **Microsoft Edge** > **Voreinstellungen**.
1. Klicken Sie auf die Registerkarte **Site-Berechtigungen**.
1. Klicken Sie auf **Cookies und Site-Daten**.
1. Klicken Sie auf **Alle Cookies und Site-Daten** anzeigen.
1. Erweitern Sie den Abschnitt `adobe.com`, wählen Sie das **mbox**-Cookie und klicken Sie dann auf das Löschen-Symbol (X).

## Löschen Sie das [!DNL Target]-Cookie aus Apple Safari

Version 13.1.2

### Löschen Sie alle mit `adobe.com` verknüpften Cookies

1. Klicken Sie auf das Menü **Safari** > **Voreinstellungen**.
1. Klicken Sie auf die Registerkarte **Datenschutz**.
1. Klicken Sie auf **Website-Daten verwalten**.
1. Wählen Sie die Sites für die Cookies aus, die Sie löschen möchten, und klicken Sie dann auf **Entfernen**.

   >[!NOTE]
   >
   >Dadurch werden alle mit der `adobe.com`-Site verknüpften Cookies gelöscht. Wenn Sie ein einzelnes Cookie für eine Site löschen möchten, befolgen Sie die unten stehenden Anweisungen.

### Löschen eines einzelnen Cookies (mbox)

1. Klicken Sie auf das Menü **Safari** > **Voreinstellungen**.
1. Klicken Sie auf die Registerkarte **Erweitert**.
1. Wählen Sie die Option **Entwicklungsmenü in der Menüleiste** anzeigen.
1. Navigieren Sie zu der Webseite, auf der sich das zu löschende Cookie befindet.
1. Klicken Sie auf das Menü **Entwicklung** > **Webinspektor anzeigen**.
1. Klicken Sie auf die Registerkarte **Datenspeicherung**.
1. Erweitern Sie den Abschnitt **Cookies** und klicken Sie dann auf `www.adobe.com`.
1. Klicken Sie mit der rechten Maustaste auf das Cookie **mbox** und klicken Sie dann auf **Löschen**.
