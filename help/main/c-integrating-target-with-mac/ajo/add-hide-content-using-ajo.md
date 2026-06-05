---
keywords: Optimierung;Personalisierung;Adobe Journey Optimizer;AJO;Anwendungsfälle;Szenarien;Inhalt hinzufügen;Inhalt ausblenden;Komponenten hinzufügen;Komponenten ausblenden
description: Erfahren Sie, wie Sie mithilfe von Komponenten zu einer Web-Seite hinzufügen oder  [!DNL Adobe Journey Optimizer].
title: Hinzufügen oder Ausblenden von Komponenten zu einer Web-Seite in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
feature: Integrations
hide: true
hidefromtoc: true
exl-id: 8c4fba88-908e-4742-ac4b-bdf7f4c882db
TQID: https://experienceleague.adobe.com/sTvR771HCE-lkk9Fg7wXkP2p2ORPYehO23d76hVCOZU
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 16fb7a1902ea76cab56a93fa141a32a3c6bc4467
workflow-type: tm+mt
source-wordcount: 687
ht-degree: 2%

---

# Hinzufügen oder Ausblenden von Komponenten zu einer Web-Seite

In diesem Anwendungsbeispiel werden die geheimen Daten für effektive Inhaltsänderungen in A/B-Tests in [!DNL Adobe Journey Optimizer] freigeschaltet.

In diesem Anwendungsbeispiel wird gezeigt, wie vertraute Aufgaben, wie z. B. A/B-Tests mit einer [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md)-Aktivität, mithilfe von [!DNL Journey Optimizer] statt [!DNL Adobe Target] durchgeführt werden können.

In diesem Anwendungsbeispiel wird gezeigt, wie Sie mit [!DNL Adobe Target], A/B-Tests mit einer [A/B-Test-Aktivität, &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md) mit [!DNL Journey Optimizer] vertraute Aufgaben ausführen können.

## Vorteile und Nutzen

* **Verbesserung der Benutzerinteraktion**: Erwecken Sie die Aufmerksamkeit der Benutzer mit einem optimierten Seitendesign, das relevante Informationen wie Werbeaktionen hervorhebt.
* **Auffindbarkeit verbessern**: Strategische Platzierung neuer Komponenten oder Inhalte auf Web- oder mobilen Apps, um Aktionen zu optimieren und die Navigation zu verbessern.
* **Zusätzliche Touchpoints erhöhen**: Führen Sie Benutzer effektiv zu Konversionsereignissen und -zielen, um die Geschäftsauswirkungen zu beschleunigen.

## Mögliche Szenarien

* Ein Finanzdienstleister plant, auf seiner Homepage eine neue Kachel hinzuzufügen, um schnell auf den Darlehensrechner zugreifen zu können, die Suchzeit zu verkürzen und die Zahl der Kreditanträge zu erhöhen.

* Ein Bekleidungsunternehmen erhöhte die Konversionen, indem es auf seiner Webseite eine neue Schaltfläche für call-to-action hinzufügte.

## Schritte

>[!NOTE]
>
>Die Anweisungen in diesem Abschnitt heben die erforderlichen Schritte zum Ändern eines Bildes und zum Verwenden von Profilattributen zum Personalisieren von Textnachrichten hervor. Weitere Informationen zu den verfügbaren Optionen im [!DNL Journey Optimizer]-Web-Designer finden Sie unter [Arbeiten mit dem Web-Designer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in der *Journey Optimizer-Dokumentation*.
>
>Das Video unten auf der Seite ist besonders hilfreich.

Führen Sie die folgenden Schritte aus, um Komponenten hinzuzufügen oder Komponenten auf Ihrer Web-Seite auszublenden:

1. Klicken Sie [!DNL Adobe Journey Optimizer] in der linken Leiste auf **Kampagnen**, um die Seite [!UICONTROL Kampagnen] anzuzeigen.

   ![Adobe Journey Optimizer-Landingpage mit hervorgehobener Registerkarte „Kampagnen“.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Klicken Sie **[!UICONTROL Kampagne erstellen]** in der oberen rechten Ecke der Seite [!UICONTROL Kampagnen].

1. Wählen Sie **[!UICONTROL Geplant - Marketing]** (Standard) aus und klicken Sie dann auf **Erstellen**, um die Detailseite [!UICONTROL Kampagne] anzuzeigen.

   ![Seite mit Kampagnendetails in Adobe Journey Optimizer](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. Geben **[!UICONTROL im Abschnitt]** einen beschreibenden Namen und eine optionale Beschreibung für die Kampagne ein.

1. (Bedingt) Klicken Sie im Abschnitt **[!UICONTROL Zielgruppe]** auf **[!UICONTROL Zielgruppe]** und wählen Sie die gewünschte Zielgruppe aus.

   In diesem Anwendungsfall können Sie die Kampagne für &quot;[!UICONTROL &#x200B; Besucher“ aktivieren &#x200B;]Standard).

1. Wählen Sie im **[!UICONTROL Aktion]**-Abschnitt **[!UICONTROL Web]** aus der Dropdown-Liste **[!UICONTROL Aktion]** aus und wählen oder erstellen Sie dann eine neue Web-Konfiguration.

   Eine Web-Konfiguration oder Kanaloberfläche ist eine Konfiguration, die von einem Systemadministrator definiert wird. Die Web-Konfiguration enthält alle technischen Parameter zum Senden der Nachricht, z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw.

   Weitere Informationen finden Sie unter [Einrichten von Kanaloberflächen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie im **[!UICONTROL Aktion]**-Abschnitt auf **[!UICONTROL Inhalt bearbeiten]**, um Ihre Website im [!DNL Journey Optimizer]-Web-Designer zu öffnen.

   ![Yoga-Landingpage auf der LUMA-Website](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Um ein Element zum Ausblenden hinzuzufügen, klicken Sie **[!UICONTROL der rechten Leiste auf]** Web-Seite bearbeiten“.

1. Klicken Sie auf das Element, das Sie ausblenden möchten, und dann auf die Schaltfläche [!UICONTROL Ausblenden] in der rechten Leiste.

   In der rechten Leiste werden Optionen angezeigt, die Sie für das ausgewählte Element ausführen können. Diese Optionen variieren je nach ausgewähltem Element.

   ![Schaltfläche „Element ausblenden](/help/main/c-integrating-target-with-mac/ajo/assets/hide-element.png)

1. Klicken Sie auf den Rückwärtspfeil in der oberen linken Ecke, um zum Web-Designer zurückzukehren.

   ![Rückwärtspfeil](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Klicken Sie auf **[!UICONTROL Zum Aktivieren überprüfen]**, stellen Sie sicher, dass alles erwartungsgemäß aussieht, und klicken Sie dann auf **Aktivieren**.

## Anzeigen von Berichten

Klicken Sie auf [!UICONTROL Berichte] und dann auf den gewünschten Berichtszeitraum:

* [!UICONTROL Alle Zeitberichte anzeigen]
* [!UICONTROL Letzten 24-Stunden-Bericht anzeigen]

Weitere Informationen finden Sie unter [Erste Schritte mit der neuen Berichterstellungsoberfläche](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} in der *Dokumentation zu Journey Optimizer*.

>[!MORELIKETHIS]
>
>[Arbeiten mit dem Web-Designer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in der *Dokumentation zu Journey Optimizer*
>[Erstellen einer Kampagne](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Journey Optimizer-Tutorials*
