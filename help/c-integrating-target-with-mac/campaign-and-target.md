---
keywords: Übersicht und Referenz
description: Erfahren Sie, wie Sie Adobe [!DNL Target] mit Adobe Campaign verwenden, um E-Mail-Inhalte zu optimieren.
title: Wie integriere ich [!DNL Target] mit Adobe Campaign?
feature: Integrationen
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
translation-type: tm+mt
source-git-commit: f3a9ee9827d635d335cb9707d3d92d0de1bd0304
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 31%

---

# [!DNL Target] mit Adobe Campaign integrieren

Verwenden Sie [!DNL Target] mit [!DNL Adobe Campaign], um den E-Mail-Inhalt zu optimieren.

Zur Optimierung Ihres E-Mail-Inhalts können Sie ein Umleitungs-Angebot in [!DNL Target] erstellen und dann [!DNL Adobe Campaign] verwenden, um die E-Mail-Angebot zu verwalten. Sie können beispielsweise unterschiedliche Angebot für männliche und weibliche Empfänger anzeigen.

Die Integration erfolgt, wenn die E-Mail geöffnet wird. Wenn der Kunde die E-Mail öffnet, wird [!DNL Target] aufgerufen und eine dynamische Version des Inhalts wird angezeigt. Der Inhalt besteht aus einem statischen Bild, das von allen Browsern unterstützt wird. [!DNL Target] verfolgt die Reaktion auf das Angebot auf Audiencen- oder Sitzungsebene und diese Daten stehen in  [!DNL Target] Berichten zur Verfügung.

[!DNL Target] kann folgende Daten verfolgen:

* Benutzeragent
* IP-Adresse
* Geografischer Standort
* Mit der ID des Besuchers verknüpftes Segment in [!DNL Target] (vorbehaltlich der rechtlichen Genehmigung)
* Daten von [!DNL Campaign] Datamart

Es gibt mehrere Einschränkungen:

* Da nur ein Bild verwendet werden darf, können Inhalte nicht personalisiert werden.
* Die Verfolgung wird in [!DNL Adobe Campaign] nicht konsolidiert.
* Keine einheitliche Benutzererfahrung

Verwenden Sie sowohl [!DNL Target] als auch [!DNL Campaign], um verschiedene Teile der Integration einzurichten:

    * Das Rohfeld und das Erlebnis in [!DNL Target]
    
    >[!HINWEIS]
    >
    >Bei Verwendung einer Rawbox und [!DNL Target], see the important security notice under [Create allowlists that specify hosts that are authorized to send mbox calls to Target] (/help/administrating-target/hosts.md#Zulassungsliste).
    
    * Der Versand in [!DNL Campaign]

## Voraussetzungen {#section_FF19BF1BCA064260930BF6C141313B0E}

Bevor Sie [!DNL Adobe Campaign] verwenden, um Ihre zielgerichteten E-Mail-Angebot einzurichten, richten Sie Folgendes in [!DNL Target] ein:

* Zwei oder mehr [!DNL Target] Umleitungs-Angebot

   Siehe [Umleitungs-Angebot erstellen](/help/c-experiences/c-manage-content/offer-redirect.md).

* Eine [!DNL Target]-Aktivität mit einem Erlebnis für jedes Angebot und der gewünschten [Erfolgsmetrik](/help/c-activities/r-success-metrics/success-metrics.md).

   Weitere Informationen finden Sie unter [Zu einer URL umleiten](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Beginn Sie die Aktivität in [!DNL Target], bevor Sie den [!DNL Campaign]-Integrationsteil einrichten.

## Ein [!DNL Target]-Angebot in eine [!DNL Adobe Campaign] E-Mail {#section_B201BBE27A704E18AF0D553F35695837} einschließen

1. Erstellen Sie eine E-Mail in [!DNL Adobe Campaign].
1. Klicken Sie in den E-Mail-Eigenschaften auf **[!UICONTROL Einschließen]** > **[!UICONTROL Dynamisches Bild bereitgestellt von Adobe Target]**.
1. Wählen Sie aus den gemeinsamen Assets das Standardbild aus.
1. Geben Sie den Speicherort an (Rawbox).
1. Geben Sie andere entscheidende Parameter an, zum Beispiel das Geschlecht des Empfängers.
1. Erstellen Sie eine Vorschau für die E-Mail und wählen Sie mindestens einen Empfänger für jedes Angebot aus (in diesem Fall einen männlichen und einen weiblichen Empfänger).
1. Definieren Sie in [!DNL Campaign] den Edge-Server, den Sie verwenden, um die Aktivität und den Namen des Mandanten zu steuern.[!DNL Target]
1. Geben Sie das für das [!DNL Adobe Experience Cloud] verwendete Externe Konto an, damit Sie auf die Ressourcen im [!DNL Experience Cloud] zugreifen können.

Weitere Informationen finden Sie in der Dokumentation zu [!DNL Adobe Campaign].

## Video: [!DNL Target] mit [!DNL Campaign] integrieren

>[!VIDEO](https://video.tv.adobe.com/v/35149)
