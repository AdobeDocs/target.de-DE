---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configure the Adobe Target Visual Experience Composer (VEC) by specifying its general settings, mobile viewport configuration, and CSS selectors.
title: Berichte in Adobe Target konfigurieren
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 33%

---


# Berichte in Zielgruppe konfigurieren

Konfigurieren Sie allgemeine Einstellungen, die in [!DNL Adobe Target] Berichte verwendet werden, die für Ihr gesamtes [!DNL Target] Konto gelten.

Um auf die Konfigurationsseite des [!UICONTROL Berichte] zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Berichte].**

Auf dieser Seite können Sie die folgenden Einstellungen festlegen:

* Adobe Experience Cloud-Lösung für den Berichte
* Die für den Berichte zu verwendende Zeitzone
* Die für den Berichte zu verwendende Währung
* IP-Adressen, die vom Berichte ausgeschlossen werden
* Zeigt eine geschätzte Umsatzsteigerung im Berichte an
* Eignung für genau festgelegte Prioritäten

>[!NOTE]
>
>Beachten Sie, dass die Zeitzone, Währung und IP-Adressen zum Ausschließen von Einstellungen für Aktivitäten gelten, die [!DNL Target] Berichte verwenden. Diese Einstellungen gelten nicht für Aktivitäten, die [Analytics für die Zielgruppe (A4T)] als Berichte-Quelle verwenden (/help/c-integrating-target-with-mac/a4t/a4t.md).

![Berichte](/help/administrating-target/assets/reporting.png)

## Berichte Cloud-Lösung

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

Wählen Sie die Berichterstellungsquelle für Ihre Aktivitäten aus; zur Wahl stehen [!DNL Target] und [!DNL Adobe Analytics]. Sie können die Berichtsquelle auch für jede Aktivität neu auswählen.

Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:

* Wenn die Berichtsquelle hier auf **[!DNL Target]** festgelegt ist, dürfen Sie Aktivitäten, die als Berichtsquelle verwenden, nicht aktivieren. [!DNL Analytics] You must change the reporting source to [!DNL Target] in your activity or change the reporting source to **[!UICONTROL Select per activity]** in **[!UICONTROL Administration]>[!UICONTROL Reporting]**.
* If the reporting source is set to **[!DNL Analytics]** here, you are not allowed to activate an activity that uses [!DNL Target] as the reporting source (the reporting source is specified as **[!UICONTROL Target per activity])**. You must change the reporting source to[!DNL Analytics]in your activity or change the reporting engine to**[!UICONTROL Select per activity ]**in**[!UICONTROL Administration]>[!UICONTROL Reporting ]**.
* If the reporting source is set to **[!UICONTROL Select per activity]** here, you can create, activate, and deactivate activities that are supported by the selected reporting source. For a matrix of supported activities, see [Supported activity types](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics as the reporting source for Adobe Target (A4t)*.
* [!UICONTROL Automated Personalization] (AP) activity creation, activation, and deactivation are allowed irrespective of the reporting source selected. Automated Personalization activities are not supported when you choose [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Even if you specify [!DNL Analytics] as your reporting source, [!DNL Target] is used as the reporting source for Automated Personalization activities. For more information, see [Supported activity types](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics as the reporting source for Adobe Target (A4t)*.

## Zeitzone für Berichte

Geben Sie die Zeitzone für den Berichte an.

## Währung für Berichte

Geben Sie die Währung für den Berichte an.

## IPs, die von den Daten des Berichte der Zielgruppe ausgeschlossen werden sollen

Specify any IP addresses that you want to exclude from reporting data. For example, excluding internal company addresses is a good way to ensure that your reporting data reflects customer interactions on your website.

Enter each IP address on a new line.

## Geschätzte Umsatzsteigerung anzeigen

You can choose to show the estimated lift in revenue if you enter a monetary value for your goal. [!DNL Target] kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden. Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert.

Only [!DNL Experience Cloud] Admin users can enable or disable this feature. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.

Ausführliche Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Aktivieren der feinjustierten Prioritäten

Lassen Sie numerische Einträge für den Prioritätsbereich von 0-999 zu.

Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.
