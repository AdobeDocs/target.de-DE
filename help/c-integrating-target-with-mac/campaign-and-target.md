---
keywords: Overview and Reference
description: Verwenden Sie Target mit Adobe Campaign, um E-Mail-Inhalte zu optimieren.
title: Integration von Target in Adobe Campaign
feature: campaign
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 46%

---


# Integration von Target in Adobe Campaign{#integrate-target-with-adobe-campaign}

Use [!DNL Target] with [!DNL Adobe Campaign] to optimize email content.

To optimize your email content--for example, to display different offers for male and female recipients--you can create a redirect offer in [!DNL Target], then use [!DNL Adobe Campaign] to manage the email offers.

Die Integration erfolgt, wenn die E-Mail geöffnet wird. When the customer opens the email, a call is made to [!DNL Target] and a dynamic version of the content appears. Der Inhalt besteht aus einem statischen Bild, das von allen Browsern unterstützt wird. [!DNL Target] verfolgt die Reaktion auf das Angebot auf Audiencen- oder Sitzungsebene und diese Daten stehen in [!DNL Target] Berichten zur Verfügung.

Target kann folgende Daten verfolgen:

* Benutzeragent
* IP-Adresse
* Geografischer Standort
* Segment, das mit der Besucher-ID in Target verknüpft ist (vorbehaltlich der rechtlichen Genehmigung)
* Data from [!DNL Campaign] Datamart

Es gibt mehrere Einschränkungen:

* Da nur ein Bild verwendet werden darf, können Inhalte nicht personalisiert werden.
* Tracking is not consolidated in [!DNL Adobe Campaign].
* Keine einheitliche Benutzererfahrung

   You must use both [!DNL Target] and [!DNL Campaign] to set up different parts of the integration:

   * Die Rawbox und das Erlebnis in [!DNL Target]
   >[!NOTE]
   >
   >Wenn Sie eine Rawbox verwenden und [!DNL Target]lesen Sie den wichtigen Sicherheitshinweis unter Zulassungslisten [erstellen, die Hosts angeben, die zum Senden von Mbox-Aufrufen an die Zielgruppe](/help/administrating-target/hosts.md#allowlist)berechtigt sind.

   * The delivery in [!DNL Campaign]



## Vorabinformationen  {#section_FF19BF1BCA064260930BF6C141313B0E}

Before you use [!DNL Adobe Campaign] to set up your targeted email offers, set up the following in [!DNL Target]:

* Two or more [!DNL Target] redirect offers

   See [Create redirect offer](/help/c-experiences/c-manage-content/offer-redirect.md).
* Eine Target-Aktivität mit einem Erlebnis für jedes Angebot und der gewünschten [Erfolgsmetrik](/help/c-activities/r-success-metrics/success-metrics.md).

   Weitere Informationen finden Sie unter [Zu einer URL umleiten](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Start the activity in [!DNL Target] before setting up the [!DNL Campaign] portion of the integration.

## Ein Target-Angebot in eine Adobe Campaign-E-Mail übernehmen  {#section_B201BBE27A704E18AF0D553F35695837}

1. Create an email in [!DNL Adobe Campaign].
1. Klicken Sie in den E-Mail-Eigenschaften auf **[!UICONTROL Einschließen]** > **[!UICONTROL Dynamisches Bild bereitgestellt von Adobe Target]**.
1. Wählen Sie aus den gemeinsamen Assets das Standardbild aus.
1. Geben Sie den Speicherort an (Rawbox).
1. Geben Sie andere entscheidende Parameter an, zum Beispiel das Geschlecht des Empfängers.
1. Erstellen Sie eine Vorschau für die E-Mail und wählen Sie mindestens einen Empfänger für jedes Angebot aus (in diesem Fall einen männlichen und einen weiblichen Empfänger).
1. In [!DNL Campaign], define the [!DNL Target] Edge server you are using to control the activity and the name of the tenant.
1. Specify the external account used for the [!DNL Adobe Experience Cloud] so you can access the resources in the [!DNL Experience Cloud].

For more information, refer to the [!DNL Adobe Campaign] documentation.
