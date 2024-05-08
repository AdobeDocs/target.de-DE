---
keywords: Bericht; Berichte; Berichterstellung; Experience Cloud-Lösung; Zeitzone; Zeitzone; Währung; Ausschluss von IPs; geschätzte Umsatzsteigerung; Umsatz; Umsatzsteigerung; differenzierte Prioritäten; genauer abgestufte Prioritäten
description: Verwendung [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics] als Berichtsquelle angeben, das standardmäßige Zeitzonen- und Währungsformat angeben, IP-Adressen hinzufügen, die aus der Berichterstellung ausgeschlossen werden sollen, und vieles mehr.
title: Konfigurieren der Berichterstellung in [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: ea9513c4310d13e1e7899aa7e228b4d7ecdf0748
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 22%

---

# Konfigurieren der Berichterstellung in [!DNL Target]

Konfigurieren allgemeiner Einstellungen zur Verwendung in [!DNL Adobe Target] Berichte, die für Ihre gesamte [!DNL Target] -Konto.

So greifen Sie auf die [!UICONTROL Reporting] Konfigurationsseite, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

Sie können die folgenden Einstellungen auf dieser Seite angeben:

* Die für die Berichterstellung zu verwendende Adobe Experience Cloud-Lösung
* Die für die Berichterstellung zu verwendende Zeitzone
* Die Währung für die Berichterstellung
* Von der Berichterstellung auszuschließende IP-Adressen
* Ob die geschätzte Umsatzsteigerung in Berichten angezeigt wird
* Ob differenzierte Prioritäten möglich sind

>[!NOTE]
>
>Beachten Sie, dass die Zeitzone, Währung und IP-Adressen zum Ausschließen von Einstellungen für Aktivitäten gelten, die [!DNL Target] Berichterstellung. Diese Einstellungen gelten nicht für Aktivitäten, die [Analytics for Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) oder [!DNL Customer Journey Analytics] als Berichtsquelle.

![Berichtseite](/help/main/administrating-target/assets/reporting.png)

## Reporting Cloud-Lösung {#solution}

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

Wählen Sie die Berichtsquelle für Ihre Aktivitäten aus, entweder [!DNL Target], [!DNL Adobe Analytics]oder [!DNL Adobe Customer Journey Analytics]. Sie können bei der Erstellung der Aktivität auch die Berichtsquelle pro Aktivität als Teil eines dreiteiligen geführten Workflows auswählen.

Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:

* **[!DNL Adobe Target]**: Wenn die Berichtsquelle auf **[!DNL Target]** Sie dürfen hier keine Aktivität erstellen oder aktivieren, die [!DNL Analytics] oder [!DNL Customer Journey Analytics] als Berichtsquelle. Sie müssen die Berichtsquelle in **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Analytics]**: Wenn die Berichtsquelle auf **[!DNL Analytics]** Sie dürfen hier keine Aktivität erstellen oder aktivieren, die [!DNL Target] oder [!DNL Customer Journey Analytics] als Berichtsquelle. Sie müssen die Berichtsquelle in **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Customer Journey Analytics]**: Wenn die Berichtsquelle auf **[!DNL Customer Journey Analytics]** Sie dürfen hier keine Aktivität erstellen oder aktivieren, die [!DNL Target] oder [!DNL Analytics] als Berichtsquelle. Sie müssen die Berichtsquelle in **[!UICONTROL Select per activity]**.
* **Pro Aktivität auswählen**: Wenn die Berichtsquelle auf **[!UICONTROL Select per activity]** Hier können Sie Aktivitäten erstellen und aktivieren, die von der ausgewählten Berichtsquelle unterstützt werden.

Beachten Sie bei der Bestimmung Ihrer Berichtsquelle die folgenden Informationen:

* **[!DNL Analytics]**: Für eine Matrix unterstützter Aktivitäten mit [!DNL Analytics] als Berichtsquelle (A4T) angeben, siehe [Unterstützte Aktivitättypen](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichtsquelle für Adobe Target (A4T)*.

  [!UICONTROL Automated Personalization] (AP) Die Erstellung und Aktivierung von Aktivitäten sind unabhängig von der ausgewählten Berichtsquelle zulässig. [!UICONTROL Automated Personalization] Aktivitäten werden bei der Auswahl von [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

  Auch wenn [!DNL Analytics] als Berichtsquelle verwenden, [!DNL Target] wird als Berichtsquelle für [!DNL Automated Personalization] Aktivitäten.

* **[!DNL Customer Journey Analytics]**: Für eine Matrix unterstützter Aktivitäten mit [!DNL Target] Reporting in [!DNL Customer Journey Analytics], siehe [Unterstützte Aktivitättypen](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md#supported-activities) in *[!DNL Target]Reporting in[!DNL Adobe Customer Journey Analytics]*.

  [!UICONTROL Automated Personalization] AP, [!UICONTROL Auto-Allocate], und [!UICONTROL Auto-Target] Die Erstellung und Aktivierung von Aktivitäten sind unabhängig von der ausgewählten Berichtsquelle zulässig. Diese Aktivitäten werden bei der Auswahl von [Adobe Customer Journey Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

  Auch wenn [!DNL Customer Journey Analytics] als Berichtsquelle verwenden, [!DNL Target] wird als Berichtsquelle für [!DNL Automated Personalization] Aktivitäten.

  Wenn Sie [!DNL Customer Journey Analytics] als Berichtsquelle für [!UICONTROL Auto-Allocate] oder [!UICONTROL Auto-Target] Aktivitäten, [!DNL Target] oder [!DNL Analytics] kann als Berichtsquelle verwendet werden.

## Zeitzone für Reporting

Geben Sie die Zeitzone an, die für die Berichterstellung verwendet werden soll.

## Währung für die Berichterstellung

Geben Sie die Währung für die Berichterstellung an.

## Auszuschließende IPs [!DNL Target] Berichtsdaten

Geben Sie alle IP-Adressen an, die Sie aus den Berichtsdaten ausschließen möchten. Beispielsweise ist das Ausschließen interner Unternehmensadressen eine gute Möglichkeit, sicherzustellen, dass Ihre Berichtsdaten Kundeninteraktionen auf Ihrer Website widerspiegeln.

Geben Sie jede IP-Adresse in eine neue Zeile ein.

## Geschätzte Umsatzsteigerung anzeigen

Sie können die geschätzte Umsatzsteigerung anzeigen lassen, wenn Sie einen Geldwert für Ihr Ziel eingeben. [!DNL Target] kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden. Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert.

Nur [!DNL Experience Cloud] Administratoren können diese Funktion aktivieren oder deaktivieren. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.

Ausführliche Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Aktivieren der feinjustierten Prioritäten

Lassen Sie numerische Einträge für den Prioritätsbereich von 0-999 zu.

Abhängig von Ihren Einstellungen variieren die Optionen und die Benutzeroberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.
