---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Konfigurieren Sie den Adobe Target Visual Experience Composer (VEC), indem Sie seine allgemeinen Einstellungen, die Konfiguration des mobilen Viewports und CSS-Selektoren angeben.
title: Berichte in Adobe Target konfigurieren
topic: Standard
translation-type: tm+mt
source-git-commit: 44d9024cb9c1f6a1e28845f9545fed0d56fe176a
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 65%

---


# Berichte in Target konfigurieren

Konfigurieren Sie allgemeine Einstellungen, die im Target-Berichte verwendet werden, der für Ihr gesamtes [!DNL Target] Konto gilt.

>[!NOTE]
>
>Die Informationen in diesem Thema wurden aktualisiert, um Ihnen einen kurzen Höhepunkt bei den UI-Änderungen zu geben, die in der Target Standard/Premium-Version 20.6.1 (Juli 2020) erscheinen. Die meisten der in diesem Thema dargestellten Informationen gelten für die aktuelle Benutzeroberfläche; Die Optionen befinden sich jedoch möglicherweise an etwas anderen Orten.

Um auf die Konfigurationsseite des [!UICONTROL Berichte] zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Berichte].**

Auf dieser Seite können Sie die folgenden Einstellungen festlegen:

* Die Adobe Experience Cloud-Lösung für Berichte
* Die für den Berichte zu verwendende Zeitzone
* Die für den Berichte zu verwendende Währung
* IP-Adressen, die vom Berichte ausgeschlossen werden
* Zeigt eine geschätzte Umsatzsteigerung im Berichte an
* Eignung für genau festgelegte Prioritäten

![Berichte](/help/administrating-target/assets/reporting.png)

## Berichte Cloud-Lösung

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

Wählen Sie die Berichterstellungsquelle für Ihre Aktivitäten aus; zur Wahl stehen [!DNL Target] und Adobe Analytics. Sie können die Berichtsquelle auch für jede Aktivität neu auswählen.

Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:

* Die Erstellung, Aktivierung und Deaktivierung von Aktivitäten der Typen [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting] und [!UICONTROL Automatische Personalisierung] sind unabhängig von der ausgewählten Berichtsquelle zulässig. Diese Aktivitätstypen werden nicht unterstützt, wenn Sie [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) auswählen. Selbst wenn Sie Analytics als Berichtsquelle angeben, wird für diese Aktivitätstypen [!DNL Target] als Quelle verwendet.
* Wenn die Berichtsquelle hier auf Analytics festgelegt ist, dürfen Sie Aktivitäten, die [!DNL Target] als Berichtsquelle verwenden (Target wurde pro Aktivität als Berichtsquelle angegeben), nicht aktivieren. Sie müssen die Berichtsquelle in Ihrer Aktivität zu „Analytics“ oder die Reporting-Engine unter „Setup“ > „Voreinstellungen“ zu „Pro Aktivität auswählen“ ändern.
* Wenn die Berichtsquelle hier auf [!DNL Target] festgelegt ist, dürfen Sie Aktivitäten, die Analytics als Berichtsquelle verwenden, nicht aktivieren. Sie müssen die Berichtsquelle in Ihrer Aktivität zu [!DNL Target]„ “ oder die Berichtsquelle unter „Setup“ > „Voreinstellungen“ zu „Pro Aktivität auswählen“ ändern.
* Wenn die Berichtsquelle auf Pro Aktivität auswählen festgelegt ist, können Sie Aktivitäten erstellen, aktivieren und deaktivieren, die von der ausgewählten Berichtsquelle unterstützt werden. Eine Tabelle unterstützter Aktivitätstypen finden Sie unter [Adobe Analytics als Berichtsquelle für Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Wenn Sie von manuellen A/B-Aktivitäten zu Aktivitäten mit [!UICONTROL automatischer Zuordnung] oder AT-Aktivitäten ([!UICONTROL Automatisches Targeting]) wechseln, gehen alle Metriken und Reporting-Zielgruppen verloren, wenn die Berichtsquelle der manuellen A/B-Aktivität nicht von der [!UICONTROL Aktivität zu automatischer Zuordnung] bzw. der [!UICONTROL AT-Aktivität] unterstützt wird.

## Zeitzone für Berichte

Geben Sie die Zeitzone für den Berichte an.

## Währung für Berichte

Geben Sie die Währung für den Berichte an.

## IPs, die von Target-Berichte-Daten ausgeschlossen werden sollen

Geben Sie alle IP-Adressen an, die von den Daten des Berichte ausgeschlossen werden sollen. So können Sie z. B. durch das Ausschließen von Adressen interner Firmen sicherstellen, dass Ihre Berichte-Daten die Interaktionen Ihrer Kunden auf Ihrer Website widerspiegeln.

Geben Sie jede IP-Adresse in eine neue Zeile ein.

## Geschätzte Umsatzsteigerung anzeigen

Sie können die geschätzte Umsatzsteigerung anzeigen, wenn Sie einen Geldwert für Ihr Ziel eingeben. [!DNL Target] kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden. Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert.

Experience Cloud-Administratoren können diese Funktion aktivieren bzw. deaktivieren. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.

Ausführliche Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Aktivieren der feinjustierten Prioritäten

Lassen Sie numerische Einträge für den Prioritätsbereich von 0-999 zu.

Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.
