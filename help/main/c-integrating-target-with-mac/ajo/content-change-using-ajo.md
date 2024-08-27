---
keywords: Optimierung;Personalisierung;Adobe Journey Optimizer;Ajo;Anwendungsfälle;Szenarien;Inhaltsänderung/ab-Test;Profilattribut;Bild ändern;Bild tauschen
description: Entsperren Sie die Geheimnisse für wirksame Inhaltsänderungen von A/B-Tests in Adobe Journey Optimizer.
title: Inhaltsänderungen durch A/B-Tests in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: 7cf9a9425b9fb17c6e9595cedb7395f6610006ec
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%

---

# Inhaltsänderungen durch A/B-Tests in [!DNL Adobe Journey Optimizer]

In diesem Anwendungsfall können Sie die Geheimnisse entsperren, um die Inhaltsänderungen in [!DNL Adobe Journey Optimizer] von A/B-Tests zu überprüfen.

Dieser Anwendungsfall soll zeigen, wie vertraute Aufgaben in [!DNL Adobe Target], A/B-Tests mit einer [A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/test-ab.md), jedoch mit [!DNL Journey Optimizer] ausgeführt werden.

## Mögliche Szenarien

* Ein Bekleidungsunternehmen steigerte die Konversionen, indem verschiedene Bilder getestet und Kampagnen-Landingpages mit den Vornamen der Benutzer aus ihren Profilattributen personalisiert wurden.

* Durch das Testen verschiedener Produktbeschreibungen und Bilder auf einer Kampagnen-Landingpage stellte ein E-Commerce-Unternehmen fest, dass seine Mitglieder der Goldloyalität höhere Konversionsraten aufwiesen, was zu einem Anstieg des Umsatzes führte.

## Vorteile und Wert

* **Optimieren Sie die Effektivität des Inhalts**: Finden Sie heraus, welche Inhaltsvarianten und Elemente bei Ihren Kunden am meisten ankommen, was zu höherer Interaktion und Konversionen führt.
* **Datenbasierte Entscheidungen**: Nutzen Sie Daten, um fundierte Entscheidungen über Ihre Inhaltsstrategie hinweg zu treffen und so eine maximale Wirkung sicherzustellen.
* **Personalisiertes Benutzererlebnis**: Passen Sie Inhalte an, um die einzigartigen Voreinstellungen und Anforderungen aller Zielgruppensegmente zu erfüllen.

## Schritte

>[!NOTE]
>
>In den Anweisungen in diesem Abschnitt werden die erforderlichen Schritte zum Ändern eines Bildes und zum Verwenden von Profilattributen zur Personalisierung von Textnachrichten beschrieben. Weitere Informationen zu den verfügbaren Optionen im [!DNL Journey Optimizer] Webdesigner finden Sie unter [Webinhalt bearbeiten](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} in der *Journey Optimizer-Dokumentation*. Das Video am unteren Seitenrand ist besonders hilfreich.

Führen Sie die folgenden Schritte aus, um eine Webseite zu optimieren, indem Sie verschiedene Bilder testen und Nachrichten mit den Vornamen der Benutzer mithilfe eines Profilskripts personalisieren:

1. Klicken Sie in [!DNL Adobe Journey Optimizer] in der linken Leiste auf **Kampagnen** , um die Seite [!UICONTROL Campaigns] anzuzeigen.

   ![Adobe Journey Optimizer-Landingpage mit hervorgehobenem Kampagnen-Tab.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Klicken Sie oben rechts auf der Seite [!UICONTROL Campaigns] auf **[!UICONTROL Create Campaign]** .

1. Wählen Sie &quot;**[!UICONTROL Scheduled - Marketing]**&quot;(Standardeinstellung) und klicken Sie dann auf &quot;**Erstellen**&quot;, um die Detailseite &quot;[!UICONTROL Campaign]&quot;anzuzeigen.

   ![Kampagnendetailseite in Adobe Journey Optimizer](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. Geben Sie im Abschnitt **[!UICONTROL Properties]** einen beschreibenden Namen und eine optionale Beschreibung für die Kampagne ein.

1. (Bedingt) Klicken Sie im Abschnitt **[!UICONTROL Audience]** auf **[!UICONTROL Select Audience]** und wählen Sie die gewünschte Zielgruppe aus.

   Für diesen Anwendungsfall haben wir ausgewählt, die Kampagne für [!UICONTROL All Visitors] zu aktivieren (Standardeinstellung).

1. Wählen Sie im Abschnitt **[!UICONTROL Action]** die Option **[!UICONTROL Web]** aus der Dropdownliste **[!UICONTROL Action]** und wählen Sie dann eine neue Webkonfiguration aus oder erstellen Sie sie.

   Eine Webkonfiguration oder Kanaloberfläche ist eine von einem Systemadministrator definierte Konfiguration. Die Webkonfiguration enthält alle technischen Parameter zum Senden der Nachricht, z. B. Kopfzeilenparameter, Subdomäne, mobile Apps usw.

   Weitere Informationen finden Sie unter [Einrichten von Kanaloberflächen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie im Abschnitt **[!UICONTROL Action]** auf **[!UICONTROL Edit Content]** , um Ihre Website im Webdesigner [!DNL Journey Optimizer] zu öffnen.

   Für A/B-Tests sind zwei oder mehr Experimente erforderlich. Sie können Ihre vorhandene Startseite als erstes Experiment verwenden. Die folgenden Schritte erläutern, wie ein zweites Experiment eingerichtet wird.

   ![Yoga-Landingpage auf der LUMA-Website](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Um ein Experiment zu erstellen, um zu testen, welcher Inhalt besser funktioniert, klicken Sie auf **[!UICONTROL Create Experiment]**.

   Mithilfe von Inhaltsexperimenten können Sie den Nachrichteninhalt, den Betreff oder den Absender variieren, um mehrere Behandlungen zu definieren und die beste Kombination für Ihre Zielgruppen zu bestimmen. Weitere Informationen finden Sie unter [Erstellen eines Inhaltsexperiments](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie in der rechten Leiste auf &quot;**[!UICONTROL Edit Web Page]**&quot;.

   ![Seite &quot;Inhalt bearbeiten&quot;auf der Yoga-Landingpage](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Um das Hero-Bild zu ändern, klicken Sie auf das Bild, das Sie ändern möchten, und klicken Sie dann auf die Schaltfläche **[!UICONTROL Choose Image]** .

   ![Bildschaltfläche auswählen](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Suchen Sie das gewünschte Bild, wählen Sie es aus und klicken Sie auf **[!UICONTROL Use This Image]**.

   ![Neues Hero-Bild auf der Yoga-Seite](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Um die Nachricht mit den Vornamen der Benutzer mithilfe von Profilattributen zu personalisieren, klicken Sie auf den Text, den Sie personalisieren möchten, und klicken Sie dann auf **[!UICONTROL Add Personalization]** , um die Seite [!UICONTROL Add Personalization] anzuzeigen.

   ![Schaltfläche &quot;Personalization hinzufügen&quot;.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Weitere Informationen zu Profilattributen finden Sie unter [Erste Schritte mit dem Personalisierungs-Editor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Suchen Sie nach dem Profilattribut &quot;Vorname&quot;, wählen Sie es aus, passen Sie den Text wie gewünscht an und klicken Sie dann auf **[!UICONTROL Save]**.

   ![Profilattribut für Namen hinzufügen](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   Weitere Informationen finden Sie unter [Erste Schritte mit dem Personalisierungs-Editor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie in der oberen linken Ecke auf den Pfeil nach hinten , um zum Webdesigner zurückzukehren.

   ![Pfeil nach hinten](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Klicken Sie auf &quot;**[!UICONTROL Review to Activate]**&quot;, stellen Sie sicher, dass alles erwartungsgemäß aussieht, und klicken Sie dann auf &quot;**Aktivieren**&quot;.

## Berichte anzeigen

Klicken Sie auf die Schaltfläche Berichte und dann auf den gewünschten Berichtszeitraum:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

Weitere Informationen finden Sie unter [Erste Schritte mit der neuen Berichterstellungsschnittstelle](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} in der *Journey Optimizer-Dokumentation*.

>[!MORELIKETHIS]
>
>[Bearbeiten des Webinhalts](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} in der *Journey Optimizer-Dokumentation*
>[Anleitungsvideo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content#video){target=_blank} in der *Journey Optimizer-Dokumentation*
>[Erstellen einer Kampagne](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Journey Optimizer-Tutorials*

