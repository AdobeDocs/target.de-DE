---
keywords: Recommendations; Angebot
description: Erfahren Sie, wie Sie Adobe Empfehlungen als Angebot in A/B-Test-Aktivitäten (einschließlich automatischer Zuordnung und automatischen Targetings) und Erlebnis-Targeting(XT)-Aktivitäten nutzen.
title: Wie verwende ich Empfehlungen als Angebot in anderen Aktivitätstypen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
TQID: 'https://experienceleague.adobe.com/ZMOb5RdY6bES331INSM7VF-w4be-5Xmjqon0YvfuNG4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 12%
---
# Empfehlungen als Angebot {#recommendations-as-an-offer}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine Recommendation als Angebot in A/B-Test[!UICONTROL  - und [!UICONTROL Experience Targeting] (XT) -Aktivitäten hinzufügen] bearbeiten und löschen.

>[!ENDSHADEBOX]

Zusätzlich zu [!UICONTROL Recommendations]-Aktivitäten können Recommendations in [!UICONTROL A/B-Test]-Aktivitäten (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) und [!UICONTROL Experience Targeting] (XT) einbezogen werden. Dies ermöglicht Folgendes:

* Testen und Targeting von Empfehlungen und Inhalt ohne Recommendations innerhalb derselben Aktivität.
* Experimentieren Sie mit der Platzierung von Recommendations auf der Seite, einschließlich der Reihenfolge mehrerer Recommendations.
* Übertragen Sie Traffic automatisch auf die Empfehlungen mit der besten Leistung mit **[!UICONTROL Automatische Zuordnung]**.
* Dynamische Zuweisung von Besuchern zu benutzerspezifischen Recommendations-Erlebnissen basierend auf ihrem Profil mit **[!UICONTROL automatischem Targeting]**.

## Hinzufügen einer Empfehlung als Angebot {#add-recs-offer}

Eine Empfehlung wird als Angebot hinzugefügt, während ein Erlebnis mit dem [!UICONTROL Visual Experience Composer] (VEC) in einer A/B[!UICONTROL Test- ] XT-Aktivität erstellt wird.

1. Starten Sie den in drei Schritten durchgeführten Workflow des VEC zum Erstellen einer [A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)- oder [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)-Aktivität (XT).

   >[!NOTE]
   >
   >Bei A/B-Tests leitet [ Option „Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) den Traffic automatisch an die Empfehlungen mit der besten Leistung weiter, und die Option [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) weist Besuchern auf der Grundlage ihres Profils maßgeschneiderte Recommendations-Erlebnisse zu.

1. Fügen Sie beim Erstellen [Erlebnisses](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) die Empfehlung auf eine der folgenden Arten als Angebot hinzu:

   * Klicken Sie auf das Element, dem die Empfehlung hinzugefügt wird, klicken Sie auf **[!UICONTROL Inhalt ersetzen]** und wählen Sie dann **[!UICONTROL Empfehlung]** aus.

     ![Visual Experience Composer mit ausgewählter Überschrift und hervorgehobener Option „Empfehlung“ im Menü neben den HTML-Angebots- und Experience Fragment-Optionen](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

   * Wählen Sie in der **[!UICONTROL Komponenten]**-Leiste **[!UICONTROL Empfehlung]** unter **[!UICONTROL Dynamisch]** aus, bewegen Sie den Mauszeiger über ein vorhandenes Element auf der Seite und klicken Sie dann auf **[!UICONTROL Einfügen vor]** oder **[!UICONTROL Einfügen nach]**, um die Empfehlung vor oder nach diesem Element zu platzieren.

1. Rufen Sie das Menü **[!UICONTROL Eigenschaften anzeigen]** auf und klicken Sie auf **[!UICONTROL Empfehlung auswählen]**.

1. Wählen Sie die gewünschten [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md) aus und klicken Sie dann auf **[!UICONTROL Weiter]**.

1. Wählen Sie das gewünschte [Design](/help/main/c-recommendations/c-design-overview/design-overview.md) aus und klicken Sie dann auf **[!UICONTROL Weiter]**.

1. Geben **[!UICONTROL im Dialogfeld]** Optionen“ Folgendes an:

   * Wählen Sie eine [Sammlung](/help/main/c-recommendations/c-products/collections.md) aus.
   * Konfigurieren Sie bei Bedarf die Optionen [Frontend-Promotion und ](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)-Promotion“.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Schließen Sie die Konfiguration der [!UICONTROL A/B]Test- oder XT-Aktivität mit dem Drei-Schritte-Workflow ab.

## Bearbeiten eines Recommendations-Angebots {#edit-recs-offer}

Die Kriterien, das Design, die Sammlung und die Promotions eines Recommendations-Angebots können nach dem Hinzufügen des Angebots im Bereich **[!UICONTROL Recommendation]** geändert werden.

1. Klicken Sie auf das Angebot, um es zu bearbeiten, und durchsuchen Sie die Optionen im Menü im rechten Bereich.

   ![Empfehlungsbereich mit den Kriterien, dem Design und den Sammlungsnamen sowie der Schaltfläche Promotion hinzufügen des ausgewählten Angebots](assets/create_reco_7.png)

1. Wählen Sie eine der folgenden Optionen aus:

   * [Kriterien ändern](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Design ändern](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Sammlung ändern](/help/main/c-recommendations/c-products/collections.md)
   * [Change-Promotion](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Nehmen Sie die Änderungen vor.

## Empfehlungsangebot löschen {#delete-recs-offer}

Ein nicht mehr benötigtes Recommendations-Angebot kann aus dem Bereich **[!UICONTROL Recommendation]** gelöscht werden.

Klicken Sie auf das zu entfernende Angebot und dann auf das Bin-Symbol ( ![Bin-Symbol](assets/Smock_Delete_18_N.svg) ) im Bereich **[!UICONTROL Empfehlung]**.

![Empfehlungsbereich mit hervorgehobenem Bin-Symbol](assets/create_reco_8.png)

## Anzeigen des Status eines Recommendations-Angebots {#status}

Der Status des Recommendations-Angebots (Algorithmus) wird unten auf der Seite **[!UICONTROL Übersicht]** für [!UICONTROL A/B-Test] und XT-Aktivitäten angezeigt, die Recommendations-Angebote enthalten. Der Status ist einer der folgenden:

* **[!UICONTROL Ergebnisse bereit]**
* **[!UICONTROL Ergebnisse nicht bereit]**
* **[!UICONTROL Feed-Fehler]**

## Schulungsvideo: Empfehlungen als Angebot ![Übersichts-Badge](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
