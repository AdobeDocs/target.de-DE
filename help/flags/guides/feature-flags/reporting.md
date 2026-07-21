---
title: Berichterstellung
description: Erfahren Sie, wie Sie Feature Flag-Berichte in Flags mithilfe von Customer Journey Analytics anzeigen.
hide: true
exl-id: edddca99-f263-461b-a16f-b46ee7c15f6c
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 2%

---

# Berichterstellung {#reporting}

Flags ermöglicht Berichte über **Customer Journey Analytics (CJA)**. Eine **Bericht**-Registerkarte ist auf jeder Detailseite für Feature Flag und Feature Group verfügbar. Damit können Sie einen CJA-Bericht anzeigen, der sich auf diese bestimmte Markierung oder Gruppe bezieht und direkt in die Seite eingebettet ist.

>[!NOTE]
>
>Berichte werden standardmäßig mit einem **30 Tage** Berichtsfenster geöffnet. Sie können den Bereich in der Panel-Kopfzeile anpassen.

## Voraussetzungen {#prerequisites}

Bevor Sie Berichte anzeigen können, stellen Sie Folgendes sicher:

1. Das Reporting ist für Ihre Anwendung eingerichtet - siehe [Einrichten des Reportings mit Customer Journey Analytics](#setup).
1. Das Feature Flag oder die Feature Group ist aktiv und enthält gesammelte Daten.

## Anzeigen eines Berichts {#view-report}

### Öffnen Sie die Registerkarte Bericht und wählen Sie eine Datenansicht {#open-report-tab}

1. Öffnen Sie ein Feature Flag oder eine Feature Group und wählen Sie die Registerkarte **Bericht** aus.
1. Ein **Datenansicht auswählen** wird geöffnet, in dem die für Sie verfügbaren CJA-Datenansichten aufgelistet sind. Die erste ist standardmäßig ausgewählt.
1. Wählen Sie die gewünschte Datenansicht aus und klicken Sie auf **Bericht anzeigen**. Klicken Sie **Abbrechen**, um das Dialogfeld zu schließen, ohne einen Bericht zu laden.
1. Der Bericht wird innerhalb der Registerkarte geladen und umfasst die Entitäts-ID dieses Flags oder dieser Gruppe.

![Registerkarte „Bericht“ auf der Detailseite eines Feature Flags](assets/report-tab.png)

>[!NOTE]
>
>Im Dialogfeld werden nur die Datenansichten aufgelistet, auf die Sie in der aktuellen Sandbox Zugriff haben. Wenn keine verfügbar sind, wird im Dialogfeld eine Meldung angezeigt und **Bericht anzeigen** bleibt deaktiviert - Überprüfen Sie Ihre Datenansichtsberechtigungen oder wechseln Sie die Sandbox.

![Dialogfeld „Datenansicht auswählen“](assets/select-dataview.png)

### Anzeigen des Leistungsberichts {#view-performance-report}

Das eingebettete Dashboard **Übersicht über Flags** wird angezeigt:

* **Personen insgesamt**, **Personenbeteiligung nach Tag** und **Personenbeteiligung nach Variante** (Kontrollgruppe vs. Varianten-IDs)
* Eine **Übersicht**-Tabelle, in der jede Variante mit der Personenzahl und dem Beteiligungsprozentsatz aufgelistet ist

Passen Sie den Datumsbereich in der Kopfzeile des Bedienfelds an, um ihn für ein anderes Fenster erneut darzustellen (standardmäßig 30 Tage).

![Flags-Leistungsbericht - Übersicht](assets/performance-report.png)

### Experimentergebnisse anzeigen {#explore-experimentation-results}

1. Im Bedienfeld **Experimentieren** werden **Experiment** (Flag- oder Gruppenentitäts-ID) und **Kontrollvariante** vorausgewählt.
1. Fügen Sie **Erfolgsmetrik** mit **Metrik hinzufügen** hinzu und wählen Sie eine **Normalisierungsmetrik** (Standard **Personen**), basierend auf dem Diagramm, das Sie plotten möchten.
1. Aktivieren Sie optional **Obere/Untere Konfidenzgrenzen einschließen**.
1. Wählen Sie **Erstellen**, um **Steigerung**, **Konfidenz** und **Konversionsrate** für die ausgewählte Metrik zu berechnen.

![Experimentier-Bedienfeld mit Selektoren für Experimente, Kontrollvarianten und Metriken](assets/experimentation-selection.png)

Weitere Informationen [ Berechnung dieser Metriken finden ](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/panels/experimentation) in der Dokumentation zum Experimentier Bedienfeld .

![Experimentergebnisse mit Steigerung, Konfidenz und Konversionsrate nach Variante](assets/experimentation.png)

### Analysieren in CJA (optional) {#analyze-in-cja}

Nachdem ein Bericht geladen wurde **wird oben rechts auf der Registerkarte „Bericht** eine Schaltfläche „Analysieren in CJA&quot; angezeigt. Wenn Sie den Bericht auswählen, wird dieselbe vollständige Berichtseite in Customer Journey Analytics in einer neuen Browser-Registerkarte geöffnet, auf der Sie über das vollständige CJA-Toolset für eine tiefer gehende Ad-hoc-Analyse verfügen.

![Markiert den im Customer Journey Analytics-Arbeitsbereich geöffneten Übersichtsbericht](assets/cja-workspace.png)

>[!IMPORTANT]
>
>Der Bericht wird als temporäres, nicht gespeichertes Projekt geöffnet. Wenn Sie sie in CJA anpassen (Metriken hinzufügen, Bedienfelder ändern, Filter anpassen usw.) und diese Änderungen beibehalten möchten, speichern Sie sie mit **Projekt > Als Vorlage speichern**. Andernfalls gehen Ihre Änderungen beim Schließen des Berichts verloren.

![Menü „Projekt“ mit hervorgehobener Option „Als Vorlage speichern“](assets/save-as-template.png)

## Einrichten von Berichten mit Customer Journey Analytics {#setup}

Für das Reporting ist ein Customer Journey Analytics-Datensatz erforderlich, der mit Ihrer Flags-Anwendung verbunden ist. Wenden Sie sich an den Flags-Support oder an Ihren Adobe-Support, um das Reporting für Ihre Anwendung zu aktivieren.

>[!NOTE]
>
>Die in der Funktionsanfrage übergebene Identität muss nicht mit einem Profil verknüpft sein. Die Auswertung erfolgt zur Laufzeit und das Ereignis wird an Customer Journey Analytics gesendet.

## Siehe auch {#see-also}

* [Erstellen des ersten Feature Flags](create-your-first-feature-flag.md)
* [A/B-Tests mit Feature Flags](a-b-testing.md)
* [Erstellen einer Funktionsgruppe](create-a-feature-group.md)

<!-- -->
