---
keywords: Optimierung;Personalisierung;Adobe Journey Optimizer;AJO;Anwendungsfälle;Szenarien;Inhaltsänderung/AB-Test;Profilattribut;Bild ändern;Bild austauschen
description: Entsperren Sie die Geheimnisse für effektive Inhaltsänderungen bei A/B-Tests in Adobe Journey Optimizer
title: Inhaltsänderungen durch A/B-Tests in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
feature: Integrations
hide: true
hidefromtoc: true
exl-id: e5aed7cd-7701-4133-ac7c-98e528c8a763
source-git-commit: b66abe9649f8c257891c1cd8e5736b7f91501c13
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 1%

---

# Inhaltsänderungen durch A/B-Tests in [!DNL Adobe Journey Optimizer]

In diesem Anwendungsbeispiel werden die geheimen Daten für effektive Inhaltsänderungen in A/B-Tests in [!DNL Adobe Journey Optimizer] freigeschaltet.

In diesem Anwendungsbeispiel wird gezeigt, wie vertraute Aufgaben, wie z. B. A/B-Tests mit einer [A/B](/help/main/c-activities/t-test-ab/test-ab.md)Testaktivität, in [!DNL Adobe Target] ausgeführt werden, indem [!DNL Journey Optimizer] anstelle von [!DNL Adobe Target] verwendet wird.

## Vorteile und Nutzen

* **Effektivität von Inhalten optimieren**: Finden Sie heraus, welche Inhaltsvarianten und -elemente bei Ihren Kunden am meisten Anklang finden und zu höherer Interaktion und höheren Konversionen führen.
* **Datengestützte Entscheidungen**: Nutzen Sie Daten, um fundierte Entscheidungen in Ihrer gesamten Inhaltsstrategie zu treffen, und sorgen Sie so für maximale Wirkung.
* **Personalisiertes Benutzererlebnis**: Passen Sie Inhalte an die individuellen Präferenzen und Bedürfnisse aller Ihrer Zielgruppensegmente an.

## Mögliche Szenarien

* Ein Bekleidungsunternehmen steigerte die Konversionen, indem es verschiedene Bilder testete und die Landingpages der Kampagnen mit den Vornamen der Benutzer im Text der Handlungsaufforderung personalisierte.

* Ein E-Commerce-Unternehmen stellte fest, dass seine Mitglieder des Treueprogramms Gold höhere Konversionsraten aufwiesen, indem sie verschiedene Produktbeschreibungen und Bilder auf einer Landingpage von Kampagnen testeten, was zu höheren Umsätzen führte.

## Schritte

>[!NOTE]
>
>Die Anweisungen in diesem Abschnitt heben die erforderlichen Schritte zum Ändern eines Bildes und zum Verwenden von Profilattributen zum Personalisieren von Textnachrichten hervor. Weitere Informationen zu den verfügbaren Optionen im [!DNL Journey Optimizer]-Web-Designer finden Sie unter [Arbeiten mit dem Web-Designer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in der *Journey Optimizer-Dokumentation*.
>
>Das Video unten auf der Seite ist besonders hilfreich.

So optimieren Sie eine Web-Seite, indem Sie verschiedene Bilder testen und Nachrichten mithilfe eines Profilskripts mit den Vornamen der Benutzer personalisieren:

1. Klicken Sie [!DNL Journey Optimizer] in der linken Leiste auf **Kampagnen**, um die [!UICONTROL Campaigns] anzuzeigen.

1. Klicken Sie oben rechts auf der [!UICONTROL Campaigns] auf **[!UICONTROL Create Campaign]** .

1. Wählen Sie **[!UICONTROL Scheduled - Marketing]** (Standard) aus und klicken Sie dann auf **Erstellen** um die Seite mit den [!UICONTROL Campaign] anzuzeigen.

1. Geben Sie im Abschnitt **[!UICONTROL Properties]** einen beschreibenden Namen und eine optionale Beschreibung für die Kampagne ein.

1. (Bedingt) Klicken Sie im Abschnitt **[!UICONTROL Audience]** auf **[!UICONTROL Select Audience]** und wählen Sie die gewünschte Zielgruppe aus.

   Für diesen Anwendungsfall können Sie die Kampagne für [!UICONTROL All Visitors] aktivieren (Standard).

1. Wählen Sie im Abschnitt **[!UICONTROL Action]** die Option **[!UICONTROL Web]** aus der Dropdown-Liste **[!UICONTROL Action]** aus und wählen oder erstellen Sie dann eine neue Web-Konfiguration.

   Eine Web-Konfiguration oder Kanaloberfläche ist eine Konfiguration, die von einem Systemadministrator definiert wird. Die Web-Konfiguration enthält alle technischen Parameter zum Senden der Nachricht, z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw.

   Weitere Informationen finden Sie unter [Einrichten von Kanaloberflächen](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie im Abschnitt **[!UICONTROL Action]** auf **[!UICONTROL Edit Content]** , um Ihre Website im [!DNL Journey Optimizer]-Web-Designer zu öffnen.

   Für A/B-Tests sind zwei oder mehr Experimente erforderlich. Sie können Ihre vorhandene Startseite als erstes Experiment verwenden. In den nachfolgenden Schritten wird beschrieben, wie Sie ein zweites Experiment einrichten.

   ![Yoga-Landingpage auf der LUMA-Website](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Um ein Experiment zu erstellen und festzustellen, welche Inhalte eine bessere Leistung erbringen, klicken Sie auf **[!UICONTROL Create Experiment]**.

   Mit Inhaltsexperimenten können Sie den Inhalt, den Betreff oder den Absender der Nachricht variieren, um mehrere Behandlungen zu definieren und die beste Kombination für Ihre Zielgruppen zu bestimmen. Weitere Informationen finden Sie unter [Erstellen eines Inhaltsexperiments](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Wählen Sie eine Erfolgsmetrik aus und klicken Sie auf Aktion.

   Klicken Sie auf die Hilfesymbole, um weitere Informationen und Links zu relevanten Artikeln zu erhalten.

1. Klicken Sie auf **[!UICONTROL Add Treatment]** und dann auf **[!UICONTROL Create]**.

   Für diesen Anwendungsfall können Sie die Verteilung für jedes Experiment bei 50 % belassen.

1. Klicken Sie auf der Seite mit den [!UICONTROL Campaign] unter **[!UICONTROL Action]** auf **[!UICONTROL Edit Content]**.

1. Klicken Sie unter Abwandlung B auf Web .

   Behalten Sie für diesen Anwendungsfall [!UICONTROL Treatment A] unverändert bei, um das ursprüngliche Erlebnis als erstes Erlebnis im A/B-Test zu verwenden.

1. Klicken Sie in der rechten Leiste auf **[!UICONTROL Edit Web Page]** .

   ![Bearbeiten von Inhalten auf der Yoga-Landingpage](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Um das Hero-Bild zu ändern, klicken Sie auf das Bild, das Sie ändern möchten, und klicken Sie dann auf die Schaltfläche **[!UICONTROL Choose Image]** .

   ![Schaltfläche „Bild auswählen“](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Navigieren Sie zu und wählen Sie das gewünschte Bild aus und klicken Sie dann auf **[!UICONTROL Use This Image]**.

   ![Neues Hero-Bild auf der Yoga-Seite](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Um die Nachricht mithilfe von Profilattributen mit den Vornamen der Benutzer zu personalisieren, klicken Sie auf den zu personalisierenden Text und dann auf **[!UICONTROL Add Personalization]** , um die [!UICONTROL Add Personalization] anzuzeigen.

   ![Schaltfläche &quot;Personalization hinzufügen“](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Weitere Informationen zu Profilattributen finden Sie unter [Erste Schritte mit dem Personalisierungseditor](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in der *Dokumentation zu Journey Optimizer*.

1. Suchen Sie nach dem Profilattribut „Vorname“ und klicken Sie darauf, um es hinzuzufügen. Passen Sie den Text nach Bedarf an und klicken Sie dann auf &quot;**[!UICONTROL Save]**&quot;.

   ![Profilattribut für Namen hinzufügen](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   Weitere Informationen finden Sie unter [Erste Schritte mit dem Personalisierungseditor](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in der *Dokumentation zu Journey Optimizer*.

1. Klicken Sie auf den Rückwärtspfeil in der oberen linken Ecke, um zum Web-Designer zurückzukehren.

   ![Rückwärtspfeil](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Klicken Sie auf **[!UICONTROL Review to Activate]**, stellen Sie sicher, dass alles erwartungsgemäß aussieht, und klicken Sie dann auf **Aktivieren**.

## Anzeigen von Berichten

Klicken Sie auf die Schaltfläche [!UICONTROL Reports] und dann auf den gewünschten Berichtszeitraum:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

Weitere Informationen finden Sie unter [Erste Schritte mit der neuen Berichterstellungsoberfläche](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} in der *Dokumentation zu Journey Optimizer*.

>[!MORELIKETHIS]
>
>[Arbeiten mit dem Web-Designer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in der Dokumentation zu *Journey Optimizer*
>[Erstellen einer Kampagne](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Journey Optimizer-Tutorials*
