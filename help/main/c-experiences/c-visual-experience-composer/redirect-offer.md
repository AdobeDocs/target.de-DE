---
keywords: Umleiten;Umleitungs-URL;An andere Seite senden
description: Erfahren Sie, wie Sie die Option Zu URL umleiten in Adobe [!DNL Target] verwenden, wenn Sie den Besucher zu einer anderen Seite senden möchten, anstatt Inhalte auf derselben Seite anzuzeigen.
title: Kann ich eine Seite an eine andere URL umleiten?
feature: Visual Experience Composer (VEC)
exl-id: bd448482-0079-4689-aa24-65ecbb31b8ae
TQID: 'https://experienceleague.adobe.com/8Bh5z7SRWw3QqKQMHZck01GKVBtMufwLbw9JxLsSACU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 2%
---
# Zu einer URL umleiten {#redirect-to-url}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie mit der Option **[!UICONTROL Zu URL umleiten]** Besucher zu einer anderen Seite senden, anstatt Inhalte auf derselben Seite anzuzeigen.

>[!ENDSHADEBOX]

Die Option **[!UICONTROL Umleiten zur URL]** in [!DNL Adobe Target] sendet einen Besucher zu einer anderen Seite, anstatt Inhalte auf derselben Seite anzuzeigen. Es eignet sich für den Vergleich von zwei völlig verschiedenen Seiten, im Gegensatz zu Änderungen an Inhaltsfragmenten innerhalb einer Seite. Ein A/B-Test vergleicht dann Seite A mit Seite B: ein Erlebnis verweist auf die Standardseite A, und das andere leitet zu Seite B weiter.

Ein Umleitungsangebot führt den JavaScript-Code aus, der den Browser umleitet. Der Code verwendet die `window.location.replace();`-Methode, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browser-Verlauf gespeichert wird. Der Besucher kann daher weiterhin die Zurück-Schaltfläche des Browsers verwenden.

## Umleitungsangebot erstellen {#create-redirect-offer}

Das umgeleitete Erlebnis definiert die Seite, an die Besucher gesendet werden, und optional die Bedingungen der Umleitung.

1. Erstellen Sie ein Erlebnis.

1. Klicken Sie im **[!UICONTROL Erlebnisse]** auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) für das Erlebnis, das umleitet.

1. Klicken Sie auf **[!UICONTROL Zu URL umleiten]**.

   ![Symbol „Mehr Aktionen“](assets/redirect_1.png)

1. Geben **[!UICONTROL im Dialogfeld Umleiten zur URL]** die URL von Seite B ein.

   ![Symbol „Mehr Aktionen“](assets/redirect_2.png)

1. (Optional) Wählen Sie die Option aus, um die aktuellen Abfrageparameter einzuschließen.

   Wenn diese Option ausgewählt ist, wird alles, was nach dem `?` in der URL des Besuchers liegt, zum Zeitpunkt der Umleitung an die Umleitungs-URL angehängt.

## Einschränkungen

Umleitungsangebote weisen die folgenden Einschränkungen auf:

* **A4T:** Ein Umleitungsangebot in einer Aktivität, die A4T verwendet, erfordert eine Implementierung, die bestimmte Mindestanforderungen erfüllt, und es gelten andere wichtige Informationen. Siehe [Umleitungsangebote - Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
* **Form-Based Experience Composer:** verwenden kein Umleitungsangebot in Mboxes, die Teil der Seite sind. Verwenden Sie ein Umleitungsangebot nur von einem Skript-Tag aus, das Teil der HTML-`<head>` ist, und verwenden Sie immer die automatische Erstellung und legen Sie das Umleitungsangebot für die globale Mbox fest.

>[!NOTE]
>
>Um den Referrer-Wert der Landingpage zu übergeben, verwenden Sie ein HTML-Angebot anstelle eines Umleitungsangebots.

## Bekannte Probleme

Umleitungsaktivitäten in at.js-Implementierungen können dazu führen, dass die Vorschau-URL in eine Schleife gerät, wobei das Angebot wiederholt bereitgestellt wird. Verwenden Sie [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) um die Aktivität stattdessen in der Vorschau anzuzeigen und zu testen. Dieses Problem hat keine Auswirkungen auf die tatsächliche Bereitstellung des Angebots. (TGT-23019)
