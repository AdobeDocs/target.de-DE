---
keywords: Optimierung;Personalisierung;Adobe Journey Optimizer;AJO;Anwendungsfälle;Szenarien;Inhaltsänderung/AB-Test;Profilattribut;Bild ändern;Bild austauschen
description: Entsperren Sie die Geheimnisse für effektive Inhaltsänderungen bei A/B-Tests in Adobe Journey Optimizer
title: Inhaltsänderungen durch A/B-Tests in [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
feature: Integrations
hide: true
hidefromtoc: true
exl-id: e5aed7cd-7701-4133-ac7c-98e528c8a763
TQID: https://experienceleague.adobe.com/IqNBAHefm8J-DEo2fU-Nj19AhcZg-FUPLccs2eC9yPQ
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eebid: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094id: fc314d1d-7cb9-4a38-8dbd-8f9b6478f40d
source-git-commit: 16fb7a1902ea76cab56a93fa141a32a3c6bc4467
workflow-type: tm+mt
source-wordcount: 954
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

* Ein Bekleidungsunternehmen steigerte die Konversionen, indem es verschiedene Bilder testete und die Landingpages mit den Vornamen der Benutzenden im call-to-action-Text personalisierte.

* Ein E-Commerce-Unternehmen stellte fest, dass seine Mitglieder des Treueprogramms Gold höhere Konversionsraten aufwiesen, indem sie verschiedene Produktbeschreibungen und Bilder auf einer Landingpage von Kampagnen testeten, was zu höheren Umsätzen führte.

## Schritte

>[!NOTE]
>
>Die Anweisungen in diesem Abschnitt heben die erforderlichen Schritte zum Ändern eines Bildes und zum Verwenden von Profilattributen zum Personalisieren von Textnachrichten hervor. Weitere Informationen zu den verfügbaren Optionen im [!DNL Journey Optimizer]-Web-Designer finden Sie unter [Arbeiten mit dem Web-Designer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in der *Journey Optimizer-Dokumentation*.
>
>Das Video unten auf der Seite ist besonders hilfreich.

So optimieren Sie eine Web-Seite, indem Sie verschiedene Bilder testen und Nachrichten mithilfe eines Profilskripts mit den Vornamen der Benutzer personalisieren:

1. Klicken Sie [!DNL Journey Optimizer] in der linken Leiste auf **Kampagnen**, um die Seite [!UICONTROL Kampagnen] anzuzeigen.

1. Klicken Sie **[!UICONTROL Kampagne erstellen]** in der oberen rechten Ecke der Seite [!UICONTROL Kampagnen].

1. Wählen Sie **[!UICONTROL Geplant - Marketing]** (Standard) aus und klicken Sie dann auf **Erstellen**, um die Detailseite [!UICONTROL Kampagne] anzuzeigen.

1. Geben **[!UICONTROL im Abschnitt]** einen beschreibenden Namen und eine optionale Beschreibung für die Kampagne ein.

1. (Bedingt) Klicken Sie im Abschnitt **[!UICONTROL Zielgruppe]** auf **[!UICONTROL Zielgruppe]** und wählen Sie die gewünschte Zielgruppe aus.

   In diesem Anwendungsfall können Sie die Kampagne für &quot;[!UICONTROL  Besucher“ aktivieren ]Standard).

1. Wählen Sie im **[!UICONTROL Aktion]**-Abschnitt **[!UICONTROL Web]** aus der Dropdown-Liste **[!UICONTROL Aktion]** aus und wählen oder erstellen Sie dann eine neue Web-Konfiguration.

   Eine Web-Konfiguration oder Kanaloberfläche ist eine Konfiguration, die von einem Systemadministrator definiert wird. Die Web-Konfiguration enthält alle technischen Parameter zum Senden der Nachricht, z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw.

   Weitere Informationen finden Sie unter [Einrichten von Kanaloberflächen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Klicken Sie im **[!UICONTROL Aktion]**-Abschnitt auf **[!UICONTROL Inhalt bearbeiten]**, um Ihre Website im [!DNL Journey Optimizer]-Web-Designer zu öffnen.

   Für A/B-Tests sind zwei oder mehr Experimente erforderlich. Sie können Ihre vorhandene Startseite als erstes Experiment verwenden. In den nachfolgenden Schritten wird beschrieben, wie Sie ein zweites Experiment einrichten.

   ![Yoga-Landingpage auf der LUMA-Website](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Um ein Experiment zu erstellen und festzustellen, welche Inhalte eine bessere Leistung erbringen, klicken Sie auf **[!UICONTROL Experiment erstellen]**.

   Mit Inhaltsexperimenten können Sie den Inhalt, den Betreff oder den Absender der Nachricht variieren, um mehrere Behandlungen zu definieren und die beste Kombination für Ihre Zielgruppen zu bestimmen. Weitere Informationen finden Sie unter [Erstellen eines Inhaltsexperiments](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} in der *Journey Optimizer-Dokumentation*.

1. Wählen Sie eine Erfolgsmetrik aus und klicken Sie auf Aktion.

   Klicken Sie auf die Hilfesymbole, um weitere Informationen und Links zu relevanten Artikeln zu erhalten.

1. Klicken Sie **[!UICONTROL Abwandlung hinzufügen]** und dann auf **[!UICONTROL Erstellen]**.

   Für diesen Anwendungsfall können Sie die Verteilung für jedes Experiment bei 50 % belassen.

1. Klicken Sie auf [!UICONTROL  Detailseite ]Kampagne“ unter **[!UICONTROL Aktion]** auf **[!UICONTROL Inhalt bearbeiten]**.

1. Klicken Sie unter Abwandlung B auf Web .

   Behalten Sie für diesen Anwendungsfall [!UICONTROL Abwandlung A] unverändert bei, um das ursprüngliche Erlebnis als erstes Erlebnis im A/B-Test zu verwenden.

1. Klicken Sie **[!UICONTROL der rechten Leiste auf]** Webseite bearbeiten“.

   ![Bearbeiten von Inhalten auf der Yoga-Landingpage](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Um das Hero-Bild zu ändern, klicken Sie auf das Bild, das Sie ändern möchten, und klicken Sie dann auf die Schaltfläche **[!UICONTROL Bild auswählen]**.

   ![Schaltfläche „Bild auswählen“](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Navigieren Sie zum gewünschten Bild, wählen Sie es aus und klicken Sie dann auf **[!UICONTROL Dieses Bild verwenden]**.

   ![Neues Hero-Bild auf der Yoga-Seite](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Um die Nachricht mithilfe von Profilattributen mit den Vornamen der Benutzer zu personalisieren, klicken Sie auf den zu personalisierenden Text und anschließend auf **[!UICONTROL Personalization hinzufügen]**, um die Seite [!UICONTROL Personalization hinzufügen] anzuzeigen.

   ![Schaltfläche &quot;Personalization hinzufügen“](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Weitere Informationen zu Profilattributen finden Sie unter [Erste Schritte mit dem Personalisierungseditor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in der *Dokumentation zu Journey Optimizer*.

1. Suchen Sie nach dem Profilattribut „Vorname“ und klicken Sie auf das Pluszeichen, um es hinzuzufügen. Passen Sie den Text nach Bedarf an und klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![Profilattribut für Namen hinzufügen](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png)

   Weitere Informationen finden Sie unter [Erste Schritte mit dem Personalisierungseditor](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in der *Dokumentation zu Journey Optimizer*.

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
