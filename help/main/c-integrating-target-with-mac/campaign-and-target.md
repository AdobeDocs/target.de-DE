---
keywords: Übersicht und Referenz
description: Erfahren Sie, wie Sie Adobe verwenden [!DNL Target] mit Adobe Campaign , um E-Mail-Inhalte zu optimieren.
title: Integration [!DNL Target] mit Adobe Campaign?
feature: Integrations
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 37%

---

# Integrieren [!DNL Target] mit Adobe Campaign

Verwendung [!DNL Target] mit [!DNL Adobe Campaign] zur Optimierung des E-Mail-Inhalts.

Um Ihren E-Mail-Inhalt zu optimieren, können Sie ein Umleitungsangebot in [!DNL Target], verwenden Sie dann [!DNL Adobe Campaign] zur Verwaltung der E-Mail-Angebote. Beispielsweise können Sie für männliche und weibliche Empfänger unterschiedliche Angebote anzeigen.

Die Integration erfolgt, wenn die E-Mail geöffnet wird. Wenn der Kunde die E-Mail öffnet, wird ein Aufruf an [!DNL Target] und eine dynamische Version des Inhalts angezeigt. Der Inhalt besteht aus einem statischen Bild, das von allen Browsern unterstützt wird. [!DNL Target] verfolgt die Reaktion auf das Angebot auf Zielgruppen- oder Sitzungsebene und stellt fest, dass Daten in [!DNL Target] Berichte.

[!DNL Target] kann folgende Daten verfolgen:

* Benutzeragent
* IP-Adresse
* Geografischer Standort
* Segment, das mit der Besucher-ID in verknüpft ist [!DNL Target] (vorbehaltlich der rechtlichen Genehmigung)
* Daten aus [!DNL Campaign] Datamart

Es gibt mehrere Einschränkungen:

* Da nur ein Bild verwendet werden darf, können Inhalte nicht personalisiert werden.
* Das Tracking ist nicht in konsolidiert [!DNL Adobe Campaign].
* Keine einheitliche Benutzererfahrung

Verwenden Sie beide [!DNL Target] und [!DNL Campaign] , um verschiedene Teile der Integration einzurichten:

* Die Raw-Box und das Erlebnis in [!DNL Target]

>[!NOTE]
>
>Wenn Sie eine Rawbox mit [!DNL Target] verwenden, lesen Sie den wichtigen Sicherheitshinweis unter [Erstellen von Zulassungslisten mit Hosts, die autorisiert sind, Mbox-Aufrufe an Target zu senden](/help/main/administrating-target/hosts.md#allowlist).

* Der Versand in [!DNL Campaign]

## Voraussetzungen {#section_FF19BF1BCA064260930BF6C141313B0E}

Vor der Verwendung von [!DNL Adobe Campaign] Um Ihre zielgerichteten E-Mail-Angebote einzurichten, richten Sie Folgendes ein in [!DNL Target]:

* Zwei oder mehr [!DNL Target] Umleitungsangebote

   Siehe [Umleitungsangebot erstellen](/help/main/c-experiences/c-manage-content/offer-redirect.md).

* A [!DNL Target] -Aktivität mit einem Erlebnis für jedes Angebot und dem gewünschten [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md).

   Weitere Informationen finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

Starten Sie die Aktivität in [!DNL Target] vor der Einrichtung der [!DNL Campaign] Teil der Integration.

## Einfügen einer [!DNL Target] Angebot in einer [!DNL Adobe Campaign] email {#section_B201BBE27A704E18AF0D553F35695837}

1. E-Mail erstellen in [!DNL Adobe Campaign].
1. Klicken Sie in den E-Mail-Eigenschaften auf **[!UICONTROL Einschließen]** > **[!UICONTROL Dynamisches Bild bereitgestellt von Adobe Target]**.
1. Wählen Sie aus den gemeinsamen Assets das Standardbild aus.
1. Geben Sie den Speicherort an (Rawbox).
1. Geben Sie andere entscheidende Parameter an, zum Beispiel das Geschlecht des Empfängers.
1. Erstellen Sie eine Vorschau für die E-Mail und wählen Sie mindestens einen Empfänger für jedes Angebot aus (in diesem Fall einen männlichen und einen weiblichen Empfänger).
1. In [!DNL Campaign], definieren Sie die [!DNL Target] Der Edge-Server, den Sie verwenden, um die Aktivität und den Namen des Mandanten zu steuern.
1. Geben Sie das externe Konto an, das für die [!DNL Adobe Experience Cloud] , damit Sie auf die Ressourcen im [!DNL Experience Cloud].

Weitere Informationen finden Sie im Abschnitt [!DNL Adobe Campaign] Dokumentation.

## Video: Integrieren [!DNL Target] mit [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
