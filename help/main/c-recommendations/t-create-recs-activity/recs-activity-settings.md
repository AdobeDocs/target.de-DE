---
keywords: Empfehlungen; Einstellungen; Name; Ziel; Priorität; Dauer; Berichterstellungseinstellungen; andere Metadaten
description: Erfahren Sie, wie Sie die Einstellungen konfigurieren, die zur Beschreibung und Steuerung einer Recommendations-Aktivität in Adobe Target verwendet werden.
title: Wie konfiguriere ich Einstellungen für Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
TQID: 'https://experienceleague.adobe.com/pfMAvl6MmLCtH3PZfOR4Ve-WFIc3e2iN2Bh-cIzjeC0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 13%
---
# Einstellungen für Recommendations-Aktivitäten {#recs-activity-settings}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie mehr über die Einstellungen, die eine [!DNL Recommendations] in [!DNL Adobe Target] beschreiben und steuern.

>[!ENDSHADEBOX]

Aktivitätseinstellungen identifizieren eine [!DNL Recommendations] Aktivität, steuern, wann und wo sie angezeigt wird, und definieren, wie ihre Ergebnisse berichtet werden.

## Name

Klicken Sie auf das Symbol Mehr Aktionen ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallListVert.svg) ) und klicken Sie dann auf **[!UICONTROL Umbenennen]**, um der Aktivität einen beschreibenden Namen zu geben, der ihr die Identifizierung erleichtert.

Die folgenden Zeichen sind in einem Aktivitätsnamen nicht zulässig: `/`, `?`, `#`, `:`, `=`, `+`, `-` und `@`.

Wenn der Name einer [!DNL Recommendations] Aktivität bereits für eine andere Aktivität in [!UICONTROL Recommendations Classic] vorhanden ist, wird die neue Aktivität mit einem neuen Namen neu synchronisiert. Der neue Name ist der ursprüngliche Name mit einem Zeitstempel, der angehängt wird, um ihn eindeutig zu machen. Er wird sowohl in [!DNL Target Standard/Premium] als auch in [!UICONTROL Recommendations Classic] angezeigt.

## Ziel

(Optional) Beschreiben Sie das Ziel der Aktivität.

## Priorität

Stellen Sie mit dem Schieberegler die Prioritätsstufe ein.

Die Priorität wird verwendet, wenn demselben Standort mit derselben Zielgruppe mehrere Aktivitäten zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

## Dauer

Legen Sie die Dauer der Aktivität fest.

Die Aktivität kann bei Aktivierung oder zu einem bestimmten Datum und zu einer bestimmten Uhrzeit beginnen. Ebenso kann sie beendet werden, wenn sie deaktiviert wird, oder zu einem bestimmten Datum und zu einer bestimmten Uhrzeit.

Die Zeitauswahl verwendet eine 24-Stunden-Uhr, wobei 00:00 Uhr Mitternacht entspricht. Die Zeitzone ist die im Browser konfigurierte. Wenn Sie eine andere Zeitzone verwenden möchten, legen Sie diese Zeitzone als Browser fest und starten Sie den Browser neu.

## Berichterstellungseinstellungen

Die folgenden Einstellungen definieren, wie die Ergebnisse der Aktivität gemeldet werden.

* **[!UICONTROL Reporting-Source]:** Gibt die Lösung an, aus der die Daten erfasst werden: [!DNL Adobe Target], [!DNL Adobe Analytics] oder [!DNL Adobe Customer Journey Analytics].

  Wenn in den [Kontoeinstellungen“ eine Berichtslösung angegeben ist](/help/main/administrating-target/reporting.md) wird diese Lösung verwendet und diese Einstellung ist nicht sichtbar. Die Berichtsquelle kann nach der Live-Schaltung der Aktivität nicht geändert werden, um die Konsistenz der Berichte zu gewährleisten.

  **[!DNL Adobe Analytics]**: Siehe [[!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) für die Unterschiede zwischen den Berichtslösungen und deren Vorteile. Informationen zur Auswahl der [!DNL Analytics] Report Suite und des Tracking-Servers finden Sie unter [Reporting Source](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source).

  **[!DNL Adobe Customer Journey Analytics]**: Siehe [[!DNL Target] Reporting in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) für weitere Informationen zur Integration zwischen [!DNL Adobe Customer Journey Analytics] und [!DNL Target].

* **[!UICONTROL Zielmetrik]:** Wählt die Erfolgsmetrik aus, die bestimmt, ob die Aktivität erfolgreich war.
* **[!UICONTROL Zusätzliche Metriken]:** Konfiguriert zusätzliche Erfolgsmetriken für die Berichte.
* **[!UICONTROL Zielgruppen für die Berichterstellung]:** Definiert Zielgruppen, die zum Filtern der Berichte verwendet werden können.

## Sonstige Metadaten

Notizen zur Aktivität eingeben.

## Schulungsvideo: Aktivitätseinstellungen (3:02) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video werden die folgenden Aktivitätseinstellungen behandelt:

* Geben Sie ein Ziel für die Aktivität ein.
* Legt die Prioritätsstufe der Aktivität fest.
* Planen Sie die Start- und Endzeiten.
* Audiences für das Reporting hinzufügen, um Berichtsfilter zu erstellen.
* Notizen für die Aktivität eingeben.

>[!VIDEO](https://video.tv.adobe.com/v/17381)
