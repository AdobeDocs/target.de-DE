---
keywords: Bericht;Berichte;Berichte;Erlebnis-Cloud-Lösung;Zeitzone;Zeitzone;Währung;IPs ausschließen;geschätzte Umsatzsteigerung;Umsatz;Umsatzsteigerung;Feinabstimmung der Prioritäten;Feinkörnig
description: Verwenden Sie Zielgruppe oder Adobe Analytics als Berichte-Quelle, geben Sie das standardmäßige Zeitzone- und Währungsformat an, fügen Sie IP-Adressen hinzu, die vom Berichte ausgeschlossen werden sollen, und vieles mehr.
title: Wie konfiguriere ich Berichte in Zielgruppe?
feature: Administration & Configuration
role: Administrator
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 31%

---


# Berichte in Zielgruppe konfigurieren

Konfigurieren Sie allgemeine Einstellungen für [!DNL Adobe Target]-Berichte, die für Ihr gesamtes [!DNL Target]-Konto gelten.

Um auf die Konfigurationsseite [!UICONTROL Berichte] zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Berichte].**

Auf dieser Seite können Sie die folgenden Einstellungen festlegen:

* Adobe Experience Cloud-Lösung für den Berichte
* Die für den Berichte zu verwendende Zeitzone
* Die für den Berichte zu verwendende Währung
* IP-Adressen, die vom Berichte ausgeschlossen werden
* Zeigt eine geschätzte Umsatzsteigerung im Berichte an
* Eignung für genau festgelegte Prioritäten

>[!NOTE]
>
>Beachten Sie, dass die Zeitzone, Währung und IP-Adressen zum Ausschließen von Einstellungen für Aktivitäten gelten, die [!DNL Target]-Berichte verwenden. Diese Einstellungen gelten nicht für Aktivitäten, die [Analytics for Zielgruppe (A4T)] als Berichte-Quelle (/help/c-integrating-target-with-mac/a4t/a4t.md) verwenden.

![Berichte](/help/administrating-target/assets/reporting.png)

## Berichte Cloud-Lösung

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

Wählen Sie die Berichterstellungsquelle für Ihre Aktivitäten aus; zur Wahl stehen [!DNL Target] und [!DNL Adobe Analytics]. Sie können die Berichtsquelle auch für jede Aktivität neu auswählen.

Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:

* Wenn die Berichtsquelle hier auf **[!DNL Target]** festgelegt ist, dürfen Sie Aktivitäten, die als Berichtsquelle verwenden, nicht aktivieren. [!DNL Analytics] Sie müssen die Berichte-Quelle in Ihrer Aktivität in [!DNL Target] ändern oder die Berichte-Quelle in **[!UICONTROL Pro Aktivität]** in **[!UICONTROL Administration] > [!UICONTROL Berichte]** ändern.
* Wenn die Berichte-Quelle hier auf **[!DNL Analytics]** eingestellt ist, ist es nicht zulässig, eine Aktivität zu aktivieren, die [!DNL Target] als Berichte-Quelle verwendet (die Berichte-Quelle wird als **[!UICONTROL Zielgruppe pro Aktivität] angegeben)**. Sie müssen die Berichte-Quelle in Ihrer Aktivität in [!DNL Analytics] ändern oder die Berichte-Engine in **[!UICONTROL Pro Aktivität]** in **[!UICONTROL Administration] > [!UICONTROL Berichte]** ändern.
* Wenn die Berichte-Quelle hier auf **[!UICONTROL Pro Aktivität]** auswählen eingestellt ist, können Sie Aktivitäten erstellen, aktivieren und deaktivieren, die von der ausgewählten Berichte-Quelle unterstützt werden. Eine Matrix der unterstützten Aktivitäten finden Sie unter [Unterstützte Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichte-Quelle für Adobe Target (A4t)*.
* [!UICONTROL Die Erstellung, Aktivierung und Deaktivierung von Automated Personalization] -Aktivitäten (AP) sind unabhängig von der ausgewählten Berichte-Quelle zulässig. Automated Personalization-Aktivitäten werden nicht unterstützt, wenn Sie [Adobe Analytics als Berichte-Quelle für Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) auswählen. Auch wenn Sie [!DNL Analytics] als Quelle des Berichte angeben, wird [!DNL Target] als Berichte für Automated Personalization-Aktivitäten verwendet. Weitere Informationen finden Sie unter [Unterstützte Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichte-Quelle für Adobe Target (A4t)*.

## Zeitzone für Berichte

Geben Sie die Zeitzone für den Berichte an.

## Währung für Berichte

Geben Sie die Währung für den Berichte an.

## IPs, die von den Daten des Berichte der Zielgruppe ausgeschlossen werden sollen

Geben Sie alle IP-Adressen an, die von den Daten des Berichte ausgeschlossen werden sollen. So können Sie z. B. durch das Ausschließen von Adressen interner Firmen sicherstellen, dass Ihre Berichte-Daten die Interaktionen Ihrer Kunden auf Ihrer Website widerspiegeln.

Geben Sie jede IP-Adresse in eine neue Zeile ein.

## Geschätzte Umsatzsteigerung anzeigen

Sie können die geschätzte Umsatzsteigerung anzeigen, wenn Sie einen Geldwert für Ihr Ziel eingeben. [!DNL Target] kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden. Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert.

Nur [!DNL Experience Cloud] Admin-Benutzer können diese Funktion aktivieren oder deaktivieren. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.

Ausführliche Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Aktivieren der feinjustierten Prioritäten

Lassen Sie numerische Einträge für den Prioritätsbereich von 0-999 zu.

Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.
