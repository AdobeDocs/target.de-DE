---
description: Löschen Sie Ihre Target-Browsercookies, sodass Sie alle Ihre Erlebnisse validieren können.
title: Löschen des Adobe Target-Cookies
topic: Standard
uuid: 6e95ee4d-dbf2-4432-8abe-cfd9bc928f0c
translation-type: tm+mt
source-git-commit: 79bcd452a9faa0883272d2e686efd7c4ddfa34a2
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# Löschen des Target-Cookies{#delete-the-target-cookie}

Sie können Ihr [!DNL Target] Browser-Cookie (Mbox) löschen, damit Sie alle Erlebnisse während des Tests validieren können.

If there is no [!DNL Target] cookie (mbox), you are considered a new visitor and shown a new experience. There are several ways to delete your [!DNL Target] cookies without deleting all of your browser cookies.

>[!NOTE]
>
>Die folgenden Anweisungen gelten für die aufgelisteten Browser und Versionen. Suchen Sie im Internet nach Anweisungen für Ihren Browser oder Ihre Version.

## Löschen Sie das Cookie &quot;Zielgruppe&quot;aus Google Chrome

Version 84.0.4147.105

1. Klicken Sie auf das **Chrome** -Menü > **Voreinstellungen**.
1. Klicken Sie auf die Registerkarte **Datenschutz und Sicherheit** .
1. Klicken Sie auf **Cookies und andere Site-Daten**.
1. Klicken Sie auf Alle Cookies und Site-Daten **anzeigen**.
1. Erweitern Sie den `adobe.com` Abschnitt, wählen Sie das **mbox** -Cookie und klicken Sie dann auf das Löschsymbol (X).

## Löschen Sie das Cookie &quot;Zielgruppe&quot;aus Mozilla Firefox

Version 79.0

1. Klicken Sie auf das **Firefox** -Menü > **Voreinstellungen**.
1. Klicken Sie auf die Registerkarte **Datenschutz und Sicherheit** .
1. Klicken Sie unter **Cookies und Site-Daten** auf Daten **verwalten**.
1. Wählen Sie die `adobe.com` Site aus und klicken Sie dann auf Ausgewählte **entfernen**.

   >[!NOTE]
   >
   >Dadurch werden alle mit der `adobe.com` Site verknüpften Cookies gelöscht. Wenn Sie einzelne Cookies für eine Site löschen oder bearbeiten möchten, können Sie dies im [Datenspeicherung-Inspektor der Entwicklerwerkzeuge](https://developer.mozilla.org/en-US/docs/Tools/Storage_Inspector)tun. Das spezifische Cookie, das Sie löschen sollten, heißt &quot;mbox&quot;.

## Löschen des Zielgruppen-Cookies aus Microsoft Edge

Version 84.0.522.52

1. Klicken Sie auf das Menü **Microsoft Edge** > **Voreinstellungen**.
1. Click the **Site Permissions** tab.
1. Klicken Sie auf **Cookies und Site-Daten**.
1. Klicken Sie auf Alle Cookies und Site-Daten **anzeigen**.
1. Erweitern Sie den `adobe.com` Abschnitt, wählen Sie das **mbox** -Cookie und klicken Sie dann auf das Löschsymbol (X).

## Löschen Sie das Zielgruppen-Cookie aus Apple Safari

Version 13.1.2

1. Klicken Sie auf das **Safari** -Menü > **Voreinstellungen**.
1. Click the **Privacy** tab.
1. Klicken Sie auf Website-Daten **verwalten**.
1. Wählen Sie die Sites für die Cookies aus, die Sie löschen möchten, und klicken Sie dann auf **Entfernen**.

>[!NOTE]
>
>Dadurch werden alle mit der `adobe.com` Site verknüpften Cookies gelöscht. Wenn Sie ein einzelnes Cookie für eine Site löschen möchten, befolgen Sie die folgenden Anweisungen:

1. Klicken Sie auf das **Safari** -Menü > **Voreinstellungen**.
1. Click the **Advanced** tab.
1. Wählen Sie in der Menüleiste die Option &quot;Entwicklung **anzeigen&quot;** .
1. Navigieren Sie zu der Webseite, auf der sich das zu löschende Cookie befindet.
1. Klicken Sie auf das **Entwicklungsmenü** > Web-Inspektor **anzeigen**.
1. Click the **Storage** tab.
1. Erweitern Sie den Abschnitt **Cookies** und klicken Sie auf `www.adobe.com`.
1. Klicken Sie mit der rechten Maustaste auf das **mbox** -Cookie und dann auf **Löschen**.