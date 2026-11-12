---
keywords: MVT;Multivariater Test;Multivariater Test erstellen;Erstellen von Multivariater Tests;MVT-Erstellung;Erstellen von MVT;wie MVT;wie Multivariater Tests
description: Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] verwenden, um einen [!UICONTROL Multivarianz-Test] (MVT) zu erstellen.
title: Wie erstelle ich einen [!UICONTROL Multivarianz-]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
TQID: 'https://experienceleague.adobe.com/gxrnY43A7OWsiW48Rlq1Orp7ZxBswdAPZEAbRQrCDZA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: aad553690f1f399177214c94a2276d038f46d9cb
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 16%
---
# Erstellen eines Multivarianz-Tests {#create-mvt}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie einen **[!UICONTROL Multivarianz-Test]** (MVT) im **[!UICONTROL Visual Experience Composer]** (VEC) erstellen. Sie erstellen die Aktivität, erstellen und überprüfen die Erlebnisse, legen die Zielgruppenbestimmung fest und konfigurieren dann Ziele und Einstellungen.

>[!ENDSHADEBOX]

Mit **[!UICONTROL Visual Experience Composer]** (VEC) in [!DNL Adobe Target] können Sie einfach einen **[!UICONTROL Multivarianz-Test]** erstellen und Teile der Seite innerhalb von [!DNL Target] ändern.

Mit dem [!DNL Target] Point-and-Click-Editor können Sie eine beliebige Stelle auswählen und mehrere Angebote hinzufügen.

Der **[!UICONTROL Multivarianz-Test]** (MVT) erstellt einen Seitenerstbericht. Anders ausgedrückt bedeutet das, dass der Test auf einer spezifischen URL ausgeführt wird, mit den Erlebnissen, die Sie für diese Seite entwerfen.

Gehen Sie wie folgt vor, um einen **[!UICONTROL Multivarianz-Test]** (MVT) zu erstellen:

1. [Erstellen der Aktivität](#create-activity)
1. [Erstellen und Überprüfen der Erlebnisse](#build-experiences)
1. [Zielgruppenbestimmung festlegen](#set-targeting)
1. [Ziele und Einstellungen konfigurieren](#configure-goals-and-settings)

## Erstellen der Aktivität {#create-activity}

Wählen Sie den Aktivitätstyp und den Versandtyp aus, geben Sie die zu testende Seite an und benennen Sie die Aktivität.

1. Klicken Sie **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Multivarianz-Test]**.

   Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

   ![](../../assets/create-mvt-1.png)

1. Wählen Sie den Versandtyp aus: **[!UICONTROL Web]**, **[!UICONTROL Mobile]**, **[!UICONTROL Email]** oder **[!UICONTROL Other/API]**.

1. (Bedingt) Wenn Sie [Target Premium](/help/main/c-intro/intro.md#premium)-Kunde sind, wählen [einen Arbeitsbereich aus](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Geben Sie die URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#ab-activity-url) für die Seite an, die Sie testen möchten. Verwenden Sie eine vollständige URL, einschließlich HTTP oder HTTPS, am Anfang.

1. Klicken Sie dann auf **[!UICONTROL Erstellen]**. Der **[!UICONTROL Visual Experience Composer]** wird geöffnet.

1. Um die Aktivität zu benennen, klicken Sie auf das Symbol **[!UICONTROL Bearbeiten]** ( ![Bearbeiten-Symbol](/help/main/assets/icons/Edit.svg) ), geben Sie einen beschreibenden Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

   {{activity-name-rules}}

   ![](../../assets/create-mvt-2.png)

## Erstellen und Überprüfen der Erlebnisse {#build-experiences}

Fügen Sie jedem Standort Angebote hinzu, zeigen Sie eine Vorschau der resultierenden Erlebnisse an und überprüfen Sie, ob Ihr Testplan durchführbar ist.

1. [Erstellen Sie die Angebote an jedem Ort](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   Sie können folgende Angebotsarten hinzufügen:

   * HTML
   * Bild
   * Text

1. Klicken Sie auf **[!UICONTROL Vorschau]**, um [eine Vorschau Ihrer Erlebnisse anzuzeigen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. Klicken Sie auf **[!UICONTROL Erlebnisse anzeigen]** (Symbol ![Erlebnisse anzeigen](/help/main/assets/icons/WebPages.svg) ), um die Liste aller Erlebnisse im linken Rahmen anzuzeigen, und klicken Sie dann auf ein bestimmtes Erlebnis in der Liste, um dieses Erlebnis anzuzeigen.

1. [Verwenden Sie die Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um die Umsetzbarkeit Ihres Testplans zu überprüfen.

### Ausschließen von Erlebnissen (optional) {#exclude-experiences}

Sie können Erlebnisse ausschließen, die widersprüchliche Varianten aufweisen oder optisch nicht ansprechend wirken.

1. Klicken Sie auf das **[!UICONTROL Inhalt verwalten]**-Symbol ( ![Symbol Erlebnisse verwalten](/help/main/assets/icons/Experience.svg) ), um das Dialogfeld **[!UICONTROL Erlebnisse verwalten]** anzuzeigen.

1. Um ein Erlebnis auszuschließen, klicken Sie auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) neben diesem Erlebnis und klicken Sie dann auf **[!UICONTROL Ausschließen]**.

1. Um mehrere Erlebnisse auszuschließen, aktivieren Sie die Kontrollkästchen für die gewünschten Erlebnisse und klicken Sie dann auf **[!UICONTROL Ausschließen]**.

## Zielgruppenbestimmung festlegen {#set-targeting}

Wählen Sie aus, welche Besucher in den Test eintreten, und überprüfen Sie die Testzusammenfassung.

1. Klicken Sie **[!UICONTROL Weiter]**, um auf die Seite **[!UICONTROL Targeting]** zuzugreifen.

   Das Flussdiagramm führt Sie durch die Schritte Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, Auswählen der Traffic-Zuordnungsmethode und Festlegen der Traffic-Zuordnung für jedes Erlebnis in der Aktivität.

1. (Bedingt) Klicken Sie auf das Steuerelement **[!UICONTROL Alle Besucher]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die **[!UICONTROL Alle Besucher]**-Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt. Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

   +++ Schritte zur Auswahl einer anderen Audience

   Daraufhin wird der rechte Rahmen angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Prozentsatz der Besuchenden für die Aktivität zuweisen können.

   1. Um die Audience zu ändern, klicken Sie auf **[!UICONTROL Ersetzen]**-Symbol ( ![Ersetzen-Symbol](/help/main/assets/icons/Retweet.svg) ) im rechten Rahmen.
   1. Wählen Sie **[!UICONTROL Dialogfeld]** Zielgruppe hinzufügen[&#x200B; die gewünschte Zielgruppe aus &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) klicken Sie dann auf **[!UICONTROL Zielgruppe zuweisen]**.

      Um eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert, klicken Sie auf **[!UICONTROL Zielgruppen kombinieren]**. Weitere Informationen finden Sie unter [Kombinieren mehrerer Zielgruppen](/help/main/c-target/combining-multiple-audiences.md).

      Um eine neue Zielgruppe zu erstellen, die sich noch nicht in der **[!UICONTROL Zielgruppenbibliothek]** befindet, klicken Sie auf **[!UICONTROL Zielgruppe erstellen]**. Wählen Sie [&#x200B; Workflow „Zielgruppe erstellen](/help/main/c-target/c-audiences/audiences.md) eine der folgenden Optionen:

      * **[!UICONTROL Zielgruppenbibliothek]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der **[!UICONTROL Zielgruppenbibliothek]** gespeichert und in anderen Aktivitäten wiederverwendet werden kann.
      * **[!UICONTROL Nur diese Aktivität]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht in der **[!UICONTROL Zielgruppenbibliothek]** gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann.

   1. Klicken Sie **[!UICONTROL rechten Feld auf]** Besucherprozentsatz) und wählen Sie dann den Prozentsatz der qualifizierten Besucher aus, die Sie in die Aktivität eingeben möchten.

   +++

1. [Überprüfen Sie die Testzusammenfassung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) nehmen Sie die gewünschten Änderungen vor und klicken Sie dann auf **[!UICONTROL Weiter]**.

## Ziele und Einstellungen konfigurieren {#configure-goals-and-settings}

Auf der Seite **[!UICONTROL Ziele und Einstellungen]** geben Sie [!DNL Target] an, wie der Test gemessen werden soll. Die verfügbaren Einstellungen hängen davon ab, ob Sie [!DNL Target] oder [!DNL Analytics] als Berichtsquelle verwenden.

1. Überprüfen Sie die Abschnitte der Seite und legen Sie fest, was Sie benötigen. Siehe [Was Sie auf der Seite Ziele und Einstellungen festgelegt haben](#goals-settings-overview).


   | Abschnitt | Was Sie festgelegt haben |
   |---|---|
   | **[!UICONTROL Aktivitätseinstellungen]** | Ein optionales Ziel, die **[!UICONTROL Priorität]** (verwendet, wenn mehrere Aktivitäten einen Standort und eine Zielgruppe gemeinsam haben) und die **[!UICONTROL Dauer]** (Start- und Enddatum). |
   | **[!UICONTROL Berichterstellungseinstellungen]** | Die Berichtsquelle, die Zielmetrik (z. B. eine **[!UICONTROL Konversion]**-Metrik), zusätzliche Metriken und Zielgruppen für das Reporting. Erweiterte Einstellungen für die Zielmetrik sind ebenfalls hier verfügbar. |
   | **[!UICONTROL Sonstige Metadaten]** | Hinweise zu den Aktivitäten, die für Sie oder andere Team-Mitglieder nützlich sind. |

1. Klicken Sie auf **[!UICONTROL Speichern und schließen]** um die Aktivität zu erstellen.

Einzelheiten zu jeder Option finden Sie unter [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#ab-goals-and-settings).

## Schulungsvideo: Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie Sie mit dem [!DNL Target] dreistufigen Workflow einen Multivarianz-Test planen und erstellen.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/17395)
