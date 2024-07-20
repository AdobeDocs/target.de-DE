---
keywords: Übersicht und Referenz
description: Erfahren Sie, wie Sie mit Adobe Campaign Adobe [!DNL Target] verwenden können, um E-Mail-Inhalte zu optimieren.
title: Wie integriere ich [!DNL Target] in Adobe Campaign?
feature: Integrations
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 32%

---

# Integrieren von [!DNL Target] in Adobe Campaign

Verwenden Sie [!DNL Target] mit [!DNL Adobe Campaign] , um den E-Mail-Inhalt zu optimieren.

Um Ihren E-Mail-Inhalt zu optimieren, können Sie ein Umleitungsangebot in [!DNL Target] erstellen und dann mit [!DNL Adobe Campaign] die E-Mail-Angebote verwalten. Beispielsweise können Sie für männliche und weibliche Empfänger unterschiedliche Angebote anzeigen.

Die Integration erfolgt, wenn die E-Mail geöffnet wird. Wenn der Kunde die E-Mail öffnet, wird [!DNL Target] aufgerufen und eine dynamische Version des Inhalts wird angezeigt. Der Inhalt besteht aus einem statischen Bild, das von allen Browsern unterstützt wird. [!DNL Target] verfolgt die Reaktion auf das Angebot auf Zielgruppen- oder Sitzungsebene und diese Daten sind in [!DNL Target] -Berichten verfügbar.

[!DNL Target] kann die folgenden Daten verfolgen:

* Benutzeragent
* IP-Adresse
* Geografischer Standort
* Segment, das mit der Besucher-ID in [!DNL Target] verknüpft ist (vorbehaltlich der rechtlichen Genehmigung)
* Daten aus [!DNL Campaign] Datamart

Es gibt mehrere Einschränkungen:

* Da nur ein Bild verwendet werden darf, können Inhalte nicht personalisiert werden.
* Das Tracking ist in [!DNL Adobe Campaign] nicht konsolidiert.
* Keine einheitliche Benutzererfahrung

Verwenden Sie sowohl [!DNL Target] als auch [!DNL Campaign], um verschiedene Teile der Integration einzurichten:

* Die Raw-Box und das Erlebnis in [!DNL Target]

>[!NOTE]
>
>Wenn Sie eine Rawbox mit [!DNL Target] verwenden, lesen Sie den wichtigen Sicherheitshinweis unter [Erstellen von Zulassungslisten mit Hosts, die autorisiert sind, Mbox-Aufrufe an Target zu senden](/help/main/administrating-target/hosts.md#allowlist).

* Der Versand in [!DNL Campaign]

## Bevor Sie beginnen {#section_FF19BF1BCA064260930BF6C141313B0E}

Bevor Sie [!DNL Adobe Campaign] verwenden, um Ihre zielgerichteten E-Mail-Angebote einzurichten, richten Sie Folgendes in [!DNL Target] ein:

* Zwei oder mehr [!DNL Target] Umleitungsangebote

  Siehe [Umleitungsangebot erstellen](/help/main/c-experiences/c-manage-content/offer-redirect.md).

* Eine [!DNL Target] -Aktivität mit einem Erlebnis für jedes Angebot und der gewünschten [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md).

  Weitere Informationen finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

Starten Sie die Aktivität in [!DNL Target] , bevor Sie den Abschnitt [!DNL Campaign] der Integration einrichten.

## Ein [!DNL Target] Angebot in eine [!DNL Adobe Campaign] E-Mail einschließen {#section_B201BBE27A704E18AF0D553F35695837}

1. Erstellen Sie eine E-Mail in [!DNL Adobe Campaign].
1. Klicken Sie in den E-Mail-Eigenschaften auf **[!UICONTROL Include]** > **[!UICONTROL Dynamic image served by Adobe Target]**.
1. Wählen Sie aus den gemeinsamen Assets das Standardbild aus.
1. Geben Sie den Speicherort an (Rawbox).
1. Geben Sie andere entscheidende Parameter an, zum Beispiel das Geschlecht des Empfängers.
1. Erstellen Sie eine Vorschau für die E-Mail und wählen Sie mindestens einen Empfänger für jedes Angebot aus (in diesem Fall einen männlichen und einen weiblichen Empfänger).
1. Definieren Sie in &quot;[!DNL Campaign]&quot;den Edge-Server &quot;[!DNL Target]&quot;, den Sie zur Steuerung der Aktivität und des Mandantennamens verwenden.
1. Geben Sie das externe Konto an, das für den [!DNL Adobe Experience Cloud] verwendet wird, damit Sie auf die Ressourcen im [!DNL Experience Cloud] zugreifen können.

Weitere Informationen finden Sie in der Dokumentation zu [!DNL Adobe Campaign] .

## Video: Integrieren von [!DNL Target] mit [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
