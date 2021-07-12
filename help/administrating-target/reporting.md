---
keywords: Bericht; Berichte; Berichterstellung; Experience Cloud-Lösung; Zeitzone; Zeitzone; Währung; Ausschluss von IPs; geschätzte Umsatzsteigerung; Umsatz; Umsatzsteigerung; differenzierte Prioritäten; genauer abgestufte Prioritäten
description: Verwenden Sie [!DNL Target] oder Adobe Analytics als Berichtsquelle, geben Sie das standardmäßige Zeitzonen- und Währungsformat an, fügen Sie IP-Adressen hinzu, die aus der Berichterstellung ausgeschlossen werden sollen, und vieles mehr.
title: Wie konfiguriere ich die Berichterstellung in Target?
feature: Administration und Konfiguration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: be7b5478006af231aae2b78e4a8c0066e3cb4a5b
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 31%

---

# Konfigurieren von Berichten in Target

Konfigurieren Sie allgemeine Einstellungen für die Verwendung in [!DNL Adobe Target]-Berichten, die für Ihr gesamtes [!DNL Target]-Konto gelten.

Um auf die Konfigurationsseite [!UICONTROL Reporting] zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

Sie können die folgenden Einstellungen auf dieser Seite angeben:

* Die für die Berichterstellung zu verwendende Adobe Experience Cloud-Lösung
* Die für die Berichterstellung zu verwendende Zeitzone
* Die Währung für die Berichterstellung
* Von der Berichterstellung auszuschließende IP-Adressen
* Ob die geschätzte Umsatzsteigerung in Berichten angezeigt wird
* Ob differenzierte Prioritäten möglich sind

>[!NOTE]
>
>Beachten Sie, dass die Zeitzone, Währung und IP-Adressen zum Ausschließen von Einstellungen für Aktivitäten gelten, die [!DNL Target]-Berichte verwenden. Diese Einstellungen gelten nicht für Aktivitäten, die [Analytics for Target (A4T)] als Berichtsquelle verwenden (/help/c-integrating-target-with-mac/a4t/a4t.md).

![Berichtseite](/help/administrating-target/assets/reporting.png)

## Reporting Cloud-Lösung

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

Wählen Sie die Berichterstellungsquelle für Ihre Aktivitäten aus; zur Wahl stehen [!DNL Target] und [!DNL Adobe Analytics]. Sie können die Berichtsquelle auch für jede Aktivität neu auswählen.

Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:

* Wenn die Berichtsquelle hier auf **[!DNL Target]** festgelegt ist, dürfen Sie Aktivitäten, die als Berichtsquelle verwenden, nicht aktivieren. [!DNL Analytics] Sie müssen die Berichtsquelle in Ihrer Aktivität zu [!DNL Target] ändern oder die Berichtsquelle zu **[!UICONTROL Pro Aktivität auswählen]** in **[!UICONTROL Administration] > [!UICONTROL Berichterstellung]** ändern.
* Wenn die Berichtsquelle hier auf **[!DNL Analytics]** festgelegt ist, dürfen Sie Aktivitäten, die [!DNL Target] als Berichtsquelle verwenden, nicht aktivieren (die Berichtsquelle ist angegeben als **[!UICONTROL Ziel pro Aktivität])**. Sie müssen die Berichtsquelle in Ihrer Aktivität zu [!DNL Analytics] oder die Reporting-Engine zu **[!UICONTROL Pro Aktivität auswählen]** in **[!UICONTROL Administration] > [!UICONTROL Berichterstellung]** ändern.
* Wenn die Berichtsquelle hier auf **[!UICONTROL Pro Aktivität auswählen]** festgelegt ist, können Sie Aktivitäten erstellen, aktivieren und deaktivieren, die von der ausgewählten Berichtsquelle unterstützt werden. Eine Tabelle unterstützter Aktivitäten finden Sie unter [Unterstützte Aktivitätstypen](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichtsquelle für Adobe Target (A4t)*.
* [!UICONTROL Die Erstellung, Aktivierung und Deaktivierung von Automated Personalization] -Aktivitäten (AP) sind unabhängig von der ausgewählten Berichtsquelle zulässig. Automated Personalization-Aktivitäten werden nicht unterstützt, wenn Sie [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) auswählen. Selbst wenn Sie [!DNL Analytics] als Berichtsquelle angeben, wird [!DNL Target] als Berichtsquelle für Automated Personalization-Aktivitäten verwendet. Weitere Informationen finden Sie unter [Unterstützte Aktivitätstypen](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichtsquelle für Adobe Target (A4t)*.

## Zeitzone für die Berichterstellung

Geben Sie die Zeitzone für die Berichterstellung an.

## Währung für die Berichterstellung

Geben Sie die Währung für die Berichterstellung an.

## Von den Berichtsdaten auszuschließende IPs[!DNL Target]

Geben Sie alle IP-Adressen an, die Sie aus den Berichtsdaten ausschließen möchten. Beispielsweise ist das Ausschließen interner Unternehmensadressen eine gute Möglichkeit, sicherzustellen, dass Ihre Berichtsdaten Kundeninteraktionen auf Ihrer Website widerspiegeln.

Geben Sie jede IP-Adresse in eine neue Zeile ein.

## Geschätzte Umsatzsteigerung anzeigen

Sie können die geschätzte Umsatzsteigerung anzeigen lassen, wenn Sie einen Geldwert für Ihr Ziel eingeben. [!DNL Target] kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden. Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert.

Nur [!DNL Experience Cloud] Admin-Benutzer können diese Funktion aktivieren oder deaktivieren. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.

Ausführliche Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Aktivieren der feinjustierten Prioritäten

Lassen Sie numerische Einträge für den Prioritätsbereich von 0-999 zu.

Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.
