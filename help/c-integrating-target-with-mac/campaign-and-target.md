---
description: Verwenden Sie Target mit Adobe Campaign, um E-Mail-Inhalte zu optimieren.
keywords: Übersicht und Referenz
seo-description: Verwenden Sie Target mit Adobe Campaign, um E-Mail-Inhalte zu optimieren.
seo-title: Integration von Target in Adobe Campaign
solution: Target
title: Integration von Target in Adobe Campaign
topic: Standard
uuid: 1a5b70e6-d501-4b52-bec8-4ae2c419d331
translation-type: tm+mt
source-git-commit: 74a6f402bc0c9dae6f89cbdb632d7dbc53743593

---


# Integration von Target in Adobe Campaign{#integrate-target-with-adobe-campaign}

Verwenden Sie Target mit Adobe Campaign, um E-Mail-Inhalte zu optimieren.

Um Ihre E-Mail-Inhalte beispielsweise so zu optimieren, dass verschiedene Angebote für männliche und weibliche Empfänger angezeigt werden, können Sie in Target ein Umleitungsangebot erstellen und anschließend mit Adobe Campaign die E-Mail-Angebote verwalten.

Die Integration erfolgt, wenn die E-Mail geöffnet wird. Wenn der Kunde die E-Mail öffnet, wird in Target ein Aufruf gestartet, und es wird eine dynamische Version des Inhalts angezeigt. Der Inhalt besteht aus einem statischen Bild, das von allen Browsern unterstützt wird. Target verfolgt die Reaktion auf das Angebot auf Zielgruppen- oder Sitzungsebene, und diese Daten werden in Target-Berichten zur Verfügung gestellt.

Target kann folgende Daten verfolgen:

* Benutzeragent
* IP-Adresse
* Geografischer Standort
* Segment, das mit der Besucher-ID in Target verknüpft ist (vorbehaltlich der rechtlichen Genehmigung)
* Daten von Campaign Datamart

Es gibt mehrere Einschränkungen:

* Da nur ein Bild verwendet werden darf, können Inhalte nicht personalisiert werden.
* Die Verfolgung wird in Adobe Campaign nicht unterstützt.
* Keine einheitliche Benutzererfahrung

   Sie müssen sowohl Target als auch Campaign verwenden, um verschiedene Teile der Integration zu erstellen:

   * Die Rawbox und das Erlebnis in Target
   * Die Bereitstellung in Campaign

## Vorabinformationen   {#section_FF19BF1BCA064260930BF6C141313B0E}

Bevor Sie Adobe Campaign verwenden, um ihre zielgerichteten E-Mail-Angebote einzurichten, legen Sie in Target Folgendes fest:

* Mindestens zwei Target-Umleitungsangebote

   Siehe [Umleitungsangebot erstellen](https://marketing.adobe.com/resources/help/en_US/target/target/t_offer_redirect.html)
* Eine Target-Aktivität mit einem Erlebnis für jedes Angebot und der gewünschten [Erfolgsmetrik](https://marketing.adobe.com/resources/help/en_US/target/target/r_success_metrics.html).

   Weitere Informationen finden Sie unter [Zu einer URL umleiten](https://marketing.adobe.com/resources/help/en_US/target/target/t_redirect_offer.html).

Starten Sie die Aktivität in Target, bevor Sie den Kampagnenteil der Integration einrichten.

## Ein Target-Angebot in eine Adobe Campaign-E-Mail übernehmen   {#section_B201BBE27A704E18AF0D553F35695837}

1. Erstellen Sie eine E-Mail in Adobe Campaign.
1. Klicken Sie in den E-Mail-Eigenschaften auf **[!UICONTROL Einschließen]** &gt; **[!UICONTROL Dynamisches Bild bereitgestellt von Adobe Target]**.
1. Wählen Sie aus den gemeinsamen Assets das Standardbild aus.
1. Geben Sie den Speicherort an (Rawbox).
1. Geben Sie andere entscheidende Parameter an, zum Beispiel das Geschlecht des Empfängers.
1. Erstellen Sie eine Vorschau für die E-Mail und wählen Sie mindestens einen Empfänger für jedes Angebot aus (in diesem Fall einen männlichen und einen weiblichen Empfänger).
1. Definieren Sie in Campaign den Target Edge-Server, den Sie zum Steuern der Aktivität und für den Namen des Mandanten verwenden.
1. Geben Sie das externe Konto für Experience Cloud an, damit Sie auf die Ressourcen in Experience Cloud zugreifen können.

Weitere Informationen finden Sie in der Adobe Campaign-Dokumentation.
