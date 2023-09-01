---
keywords: Bericht; Berichte; Berichterstellung; Experience Cloud-Lösung; Zeitzone; Zeitzone; Währung; Ausschluss von IPs; geschätzte Umsatzsteigerung; Umsatz; Umsatzsteigerung; differenzierte Prioritäten; genauer abgestufte Prioritäten
description: Verwendung [!DNL Target] oder Adobe Analytics als Berichtsquelle verwenden, geben Sie das standardmäßige Zeitzonen- und Währungsformat an, fügen Sie IP-Adressen hinzu, die aus der Berichterstellung ausgeschlossen werden sollen, und vieles mehr.
title: Wie konfiguriere ich die Berichterstellung in Target?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: 273143c5b2157948eee464ee0514e04a0105e978
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 31%

---

# Konfigurieren von Berichten in Target

Konfigurieren allgemeiner Einstellungen zur Verwendung in [!DNL Adobe Target] Berichte, die für Ihre gesamte [!DNL Target] -Konto.

So greifen Sie auf die [!UICONTROL Berichterstellung] Konfigurationsseite, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Berichterstellung].**

Sie können die folgenden Einstellungen auf dieser Seite angeben:

* Die für die Berichterstellung zu verwendende Adobe Experience Cloud-Lösung
* Die für die Berichterstellung zu verwendende Zeitzone
* Die Währung für die Berichterstellung
* Von der Berichterstellung auszuschließende IP-Adressen
* Ob die geschätzte Umsatzsteigerung in Berichten angezeigt wird
* Ob differenzierte Prioritäten möglich sind

>[!NOTE]
>
>Beachten Sie, dass die Zeitzone, Währung und IP-Adressen zum Ausschließen von Einstellungen für Aktivitäten gelten, die [!DNL Target] Berichterstellung. Diese Einstellungen gelten nicht für Aktivitäten, die [Analytics for Target (A4T)] als Berichtsquelle (/help/main/c-integrating-target-with-mac/a4t/a4t.md).

![Berichtseite](/help/main/administrating-target/assets/reporting.png)

## Reporting Cloud-Lösung {#solution}

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

Wählen Sie die Berichterstellungsquelle für Ihre Aktivitäten aus; zur Wahl stehen [!DNL Target] und [!DNL Adobe Analytics]. Sie können die Berichtsquelle auch für jede Aktivität neu auswählen.

Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:

* Wenn die Berichtsquelle hier auf **[!DNL Target]** festgelegt ist, dürfen Sie Aktivitäten, die als Berichtsquelle verwenden, nicht aktivieren. [!DNL Analytics] Sie müssen die Berichtsquelle in [!DNL Target] in Ihrer Aktivität oder ändern Sie die Berichtsquelle in **[!UICONTROL Pro Aktivität auswählen]** in **[!UICONTROL Administration] > [!UICONTROL Berichterstellung]**.
* Wenn die Berichtsquelle auf **[!DNL Analytics]** Sie dürfen hier keine Aktivität aktivieren, die [!DNL Target] als Berichtsquelle angeben (die Berichtsquelle wird angegeben als **[!UICONTROL Zielgruppe pro Aktivität])**. Sie müssen die Berichtsquelle in [!DNL Analytics] in Ihrer Aktivität oder ändern Sie die Reporting-Engine in **[!UICONTROL Pro Aktivität auswählen]** in **[!UICONTROL Administration] > [!UICONTROL Berichterstellung]**.
* Wenn die Berichtsquelle auf **[!UICONTROL Pro Aktivität auswählen]** Sie können hier Aktivitäten erstellen, aktivieren und deaktivieren, die von der ausgewählten Berichtsquelle unterstützt werden. Eine Matrix der unterstützten Aktivitäten finden Sie unter [Unterstützte Aktivitättypen](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichtsquelle für Adobe Target (A4T)*.
* [!UICONTROL Automated Personalization] (AP) Die Erstellung, Aktivierung und Deaktivierung von Aktivitäten sind unabhängig von der ausgewählten Berichtsquelle zulässig. Automated Personalization-Aktivitäten werden bei der Auswahl von [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md). Auch wenn [!DNL Analytics] als Berichtsquelle verwenden, [!DNL Target] wird als Berichtsquelle für Automated Personalization-Aktivitäten verwendet. Weitere Informationen finden Sie unter [Unterstützte Aktivitättypen](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichtsquelle für Adobe Target (A4T)*.

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

Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.
