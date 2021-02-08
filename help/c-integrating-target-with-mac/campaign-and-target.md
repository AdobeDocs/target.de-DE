---
keywords: Übersicht und Referenz
description: Erfahren Sie, wie Sie mit Adobe Target und Adobe Campaign E-Mail-Inhalte optimieren können.
title: Wie integriere ich Zielgruppe in Adobe Campaign?
feature: Integrations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 42%

---


# Integration von Target in Adobe Campaign{#integrate-target-with-adobe-campaign}

Verwenden Sie [!DNL Target] mit [!DNL Adobe Campaign], um den E-Mail-Inhalt zu optimieren.

Zur Optimierung Ihres E-Mail-Inhalts - z. B. zur Anzeige verschiedener Angebot für männliche und weibliche Empfänger - können Sie ein Umleitungs-Angebot in [!DNL Target] erstellen und dann [!DNL Adobe Campaign] verwenden, um die E-Mail-Angebot zu verwalten.

Die Integration erfolgt, wenn die E-Mail geöffnet wird. Wenn der Kunde die E-Mail öffnet, wird [!DNL Target] aufgerufen und eine dynamische Version des Inhalts wird angezeigt. Der Inhalt besteht aus einem statischen Bild, das von allen Browsern unterstützt wird. [!DNL Target] verfolgt die Reaktion auf das Angebot auf Audiencen- oder Sitzungsebene und diese Daten stehen in  [!DNL Target] Berichten zur Verfügung.

Target kann folgende Daten verfolgen:

* Benutzeragent
* IP-Adresse
* Geografischer Standort
* Segment, das mit der Besucher-ID in Target verknüpft ist (vorbehaltlich der rechtlichen Genehmigung)
* Daten von [!DNL Campaign] Datamart

Es gibt mehrere Einschränkungen:

* Da nur ein Bild verwendet werden darf, können Inhalte nicht personalisiert werden.
* Die Verfolgung wird in [!DNL Adobe Campaign] nicht konsolidiert.
* Keine einheitliche Benutzererfahrung

   Sie müssen sowohl [!DNL Target] als auch [!DNL Campaign] verwenden, um verschiedene Teile der Integration einzurichten:

   * Die Rawbox und das Erlebnis in [!DNL Target]
   >[!NOTE]
   >
   >Wenn Sie eine Rawbox und [!DNL Target] verwenden, lesen Sie den wichtigen Sicherheitshinweis unter [Zulassungslisten erstellen, die Hosts angeben, die zum Senden von Mbox-Aufrufen an Zielgruppe](/help/administrating-target/hosts.md#allowlist) berechtigt sind.

   * Der Versand in [!DNL Campaign]



## Vorabinformationen   {#section_FF19BF1BCA064260930BF6C141313B0E}

Bevor Sie [!DNL Adobe Campaign] verwenden, um Ihre zielgerichteten E-Mail-Angebot einzurichten, richten Sie Folgendes in [!DNL Target] ein:

* Zwei oder mehr [!DNL Target] Umleitungs-Angebot

   Siehe [Umleitungs-Angebot erstellen](/help/c-experiences/c-manage-content/offer-redirect.md).
* Eine Target-Aktivität mit einem Erlebnis für jedes Angebot und der gewünschten [Erfolgsmetrik](/help/c-activities/r-success-metrics/success-metrics.md).

   Weitere Informationen finden Sie unter [Zu einer URL umleiten](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Beginn Sie die Aktivität in [!DNL Target], bevor Sie den [!DNL Campaign]-Integrationsteil einrichten.

## Ein Target-Angebot in eine Adobe Campaign-E-Mail übernehmen   {#section_B201BBE27A704E18AF0D553F35695837}

1. Erstellen Sie eine E-Mail in [!DNL Adobe Campaign].
1. Klicken Sie in den E-Mail-Eigenschaften auf **[!UICONTROL Einschließen]** > **[!UICONTROL Dynamisches Bild bereitgestellt von Adobe Target]**.
1. Wählen Sie aus den gemeinsamen Assets das Standardbild aus.
1. Geben Sie den Speicherort an (Rawbox).
1. Geben Sie andere entscheidende Parameter an, zum Beispiel das Geschlecht des Empfängers.
1. Erstellen Sie eine Vorschau für die E-Mail und wählen Sie mindestens einen Empfänger für jedes Angebot aus (in diesem Fall einen männlichen und einen weiblichen Empfänger).
1. Definieren Sie in [!DNL Campaign] den Edge-Server, den Sie verwenden, um die Aktivität und den Namen des Mandanten zu steuern.[!DNL Target]
1. Geben Sie das für das [!DNL Adobe Experience Cloud] verwendete Externe Konto an, damit Sie auf die Ressourcen im [!DNL Experience Cloud] zugreifen können.

Weitere Informationen finden Sie in der Dokumentation zu [!DNL Adobe Campaign].
