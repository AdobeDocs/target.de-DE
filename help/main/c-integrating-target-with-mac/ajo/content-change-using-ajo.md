---
keywords: Optimierung;Personalisierung;Adobe Journey Optimizer;Ajo;Anwendungsfälle;Szenarien;Inhaltsänderung/ab-Test;Profilattribut;Bild ändern;Bild tauschen
description: Entsperren Sie die Geheimnisse für wirksame Inhaltsänderungen von A/B-Tests in Adobe Journey Optimizer.
title: Inhaltsänderungen durch A/B-Tests in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: bbf56b2d041ea6537116d900278242a7a679dedd
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 2%

---

# Inhaltsänderungen durch A/B-Tests in [!DNL Adobe Journey Optimizer]

In diesem Anwendungsfall können Sie die Geheimnisse entsperren, um die Inhaltsänderungen in [!DNL Adobe Journey Optimizer] von A/B-Tests zu überprüfen.

## Szenario

Ein Bekleidungsunternehmen steigerte die Konversionen, indem verschiedene Bilder getestet und Kampagnen-Landingpages mit den Vornamen der Benutzer aus ihren Profilattributen personalisiert wurden.

## Vorteile und Wert

* **Optimieren Sie die Effektivität des Inhalts**: Finden Sie heraus, welche Inhaltsvarianten und Elemente bei Ihren Kunden am meisten ankommen, was zu höherer Interaktion und Konversionen führt.
* **Datenbasierte Entscheidungen**: Nutzen Sie Daten, um fundierte Entscheidungen über Ihre Inhaltsstrategie hinweg zu treffen und so eine maximale Wirkung sicherzustellen.
* **Personalisiertes Benutzererlebnis**: Passen Sie Inhalte an, um die einzigartigen Voreinstellungen und Anforderungen aller Zielgruppensegmente zu erfüllen.

## Schrittweise Anleitungen

Führen Sie die folgenden Schritte aus, um eine Webseite zu optimieren, indem Sie verschiedene Bilder testen und Nachrichten mit den Vornamen der Benutzer personalisieren:

1. Klicken Sie in [!DNL Adobe Journey Optimizer] in der linken Leiste auf **Kampagnen** , um die Seite [!UICONTROL Campaigns] anzuzeigen.

   ![Adobe Journey Optimizer-Landingpage mit hervorgehobenem Kampagnen-Tab.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Klicken Sie oben rechts auf der Seite [!UICONTROL Campaigns] auf **[!UICONTROL Create Campaign]** .

1. Wählen Sie &quot;**[!UICONTROL Scheduled - Marketing]**&quot;(Standardeinstellung) und klicken Sie dann auf &quot;**Erstellen**&quot;, um die Detailseite &quot;[!UICONTROL Campaign]&quot;anzuzeigen.

   ![Kampagnendetailseite in Adobe Journey Optimizer](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. Geben Sie einen beschreibenden Namen und eine optionale Beschreibung für die Kampagne ein.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Select Audience]** und wählen Sie die gewünschten Zielgruppen aus.

   Für diesen Anwendungsfall haben wir ausgewählt, die Kampagne für alle Besucher zu aktivieren (Standardeinstellung).

1. Wählen Sie **[!UICONTROL Web]** aus der Dropdownliste **[!UICONTROL Action]** und wählen Sie dann eine neue Webkonfiguration aus oder erstellen Sie sie.

   Eine Webkonfiguration oder Kanaloberfläche ist eine Konfiguration, die von einem Systemadministrator definiert wurde. Die Webkonfiguration enthält alle technischen Parameter zum Senden der Nachricht, z. B. Kopfzeilenparameter, Subdomäne, mobile Apps usw.

   Weitere Informationen finden Sie unter [Einrichten von Kanaloberflächen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie auf **[!UICONTROL Edit Content]** , um Ihre Website im Webdesigner [!DNL Journey Optimizer] zu öffnen.

   ![Yoga-Landingpage auf der LUMA-Website](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Klicken Sie in der rechten Leiste auf &quot;**[!UICONTROL Edit Web Page]**&quot;.

   ![Seite &quot;Inhalt bearbeiten&quot;auf der Yoga-Landingpage](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Um das Hero-Bild zu ändern, klicken Sie auf das Bild, das Sie ändern möchten, und klicken Sie dann auf die Schaltfläche **[!UICONTROL Choose Image]** .

   ![Bildschaltfläche auswählen](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Suchen Sie das gewünschte Bild, wählen Sie es aus und klicken Sie auf **[!UICONTROL Use This Image]**.

   ![Neues Hero-Bild auf der Yoga-Seite](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Um die Nachricht mit den Vornamen der Benutzer mithilfe von Profilattributen zu personalisieren, klicken Sie auf den Text, den Sie personalisieren möchten, und klicken Sie dann auf **[!UICONTROL Add Personalization]** , um die Seite [!UICONTROL Add Personalization] anzuzeigen.

   ![Schaltfläche &quot;Personalization hinzufügen&quot;.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

1. Suchen Sie nach dem Profilattribut &quot;Vorname&quot;, wählen Sie es aus, passen Sie den Text wie gewünscht an und klicken Sie dann auf **[!UICONTROL Save]**.

   ![Profilattribut für Namen hinzufügen](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   Weitere Informationen finden Sie unter [Erste Schritte mit dem Personalisierungs-Editor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie in der oberen linken Ecke auf den Pfeil nach hinten , um zum Webdesigner zurückzukehren.

   ![Pfeil nach hinten](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Klicken Sie auf &quot;**[!UICONTROL Review to Activate]**&quot;, stellen Sie sicher, dass alles erwartungsgemäß aussieht, und klicken Sie dann auf &quot;**Aktivieren**&quot;.

>[!MORELIKETHIS]
>
>[Bearbeiten des Webinhalts](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content){target=_blank} in der *Journey Optimizer-Dokumentation*
>[Anleitungsvideo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/web-spa#video){target=_blank} in der *Journey Optimizer-Dokumentation*
>[Erstellen einer Kampagne](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Journey Optimizer-Tutorials*

