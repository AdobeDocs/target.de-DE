---
keywords: Bericht;Berichte;Reporting;Experience Cloud-Lösung;Zeitzone;Zeitzone;Währung;IP ausschließen;geschätzte Steigerung des Umsatzes;Umsatz;Steigerung des Umsatzes;detailliertere Prioritäten;detailliert
description: Verwenden Sie  [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics]  Berichtsquelle, geben Sie das standardmäßige Zeitzonen- und Währungsformat an, fügen Sie IP-Adressen hinzu, die aus dem Reporting ausgeschlossen werden sollen, und vieles mehr.
title: Wie konfiguriere ich Reporting in [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: ea9513c4310d13e1e7899aa7e228b4d7ecdf0748
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 22%

---

# Konfigurieren der Berichterstellung in [!DNL Target]

Konfigurieren Sie allgemeine Einstellungen, die für [!DNL Adobe Target] Reporting-Berichte verwendet werden und für Ihr gesamtes [!DNL Target]-Konto gelten.

Um auf die Seite mit der [!UICONTROL Reporting]-Konfiguration zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

Sie können die folgenden Einstellungen auf dieser Seite festlegen:

* Die Adobe Experience Cloud-Lösung für das Reporting
* Die für das Reporting zu verwendende Zeitzone
* Die für das Reporting zu verwendende Währung
* Auszuschließende IP-Adressen aus Berichten
* Ob die geschätzte Steigerung des Umsatzes im Reporting angezeigt werden soll
* Ob differenzierte Prioritäten aktiviert werden sollen

>[!NOTE]
>
>Beachten Sie, dass die Einstellungen für Zeitzone, Währung und IP-Adressen zum Ausschließen für Aktivitäten gelten, die [!DNL Target] Reporting verwenden. Diese Einstellungen gelten nicht für Aktivitäten, die [Analytics for Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) oder [!DNL Customer Journey Analytics] als Berichtsquelle verwenden.

![Berichterstellungsseite](/help/main/administrating-target/assets/reporting.png)

## Reporting Cloud-Lösung {#solution}

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

Wählen Sie die Berichtsquelle für Ihre Aktivitäten aus, entweder [!DNL Target], [!DNL Adobe Analytics] oder [!DNL Adobe Customer Journey Analytics]. Sie können bei der Erstellung der Aktivität auch die Berichtsquelle pro Aktivität als Teil eines dreiteiligen geleiteten Workflows auswählen.

Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:

* **[!DNL Adobe Target]**: Wenn die Berichtsquelle hier auf **[!DNL Target]** festgelegt ist, dürfen Sie keine Aktivität erstellen oder aktivieren, die [!DNL Analytics] oder [!DNL Customer Journey Analytics] als Berichtsquelle verwendet. Sie müssen die Berichtsquelle in **[!UICONTROL Select per activity]** ändern.
* **[!DNL Adobe Analytics]**: Wenn die Berichtsquelle hier auf **[!DNL Analytics]** festgelegt ist, dürfen Sie keine Aktivität erstellen oder aktivieren, die [!DNL Target] oder [!DNL Customer Journey Analytics] als Berichtsquelle verwendet. Sie müssen die Berichtsquelle in **[!UICONTROL Select per activity]** ändern.
* **[!DNL Adobe Customer Journey Analytics]**: Wenn die Berichtsquelle hier auf **[!DNL Customer Journey Analytics]** festgelegt ist, dürfen Sie keine Aktivität erstellen oder aktivieren, die [!DNL Target] oder [!DNL Analytics] als Berichtsquelle verwendet. Sie müssen die Berichtsquelle in **[!UICONTROL Select per activity]** ändern.
* **Pro Aktivität auswählen**: Wenn die Berichtsquelle auf **[!UICONTROL Select per activity]** hier festgelegt ist, können Sie Aktivitäten erstellen und aktivieren, die von der ausgewählten Berichtsquelle unterstützt werden.

Beachten Sie bei der Bestimmung Ihrer Berichtsquelle die folgenden Informationen:

* **[!DNL Analytics]**: Eine Matrix der unterstützten Aktivitäten, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden, finden Sie unter [Unterstützte Aktivitätstypen](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als Berichtsquelle für Adobe Target (A4T)*.

  Die Erstellung und Aktivierung von [!UICONTROL Automated Personalization] (AP)-Aktivitäten ist unabhängig von der ausgewählten Berichtsquelle zulässig. [!UICONTROL Automated Personalization] Aktivitäten werden nicht unterstützt, wenn Sie [Adobe Analytics als Berichtsquelle für Adobe Target (A4T) auswählen](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

  Selbst wenn Sie [!DNL Analytics] als Berichtsquelle angeben, wird [!DNL Target] als Berichtsquelle für [!DNL Automated Personalization] Aktivitäten verwendet.

* **[!DNL Customer Journey Analytics]**: Eine Matrix der unterstützten Aktivitäten unter Verwendung der [!DNL Target]-Berichterstellung in [!DNL Customer Journey Analytics] finden Sie [Unterstützte Aktivitätstypen](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md#supported-activities) in *[!DNL Target]Berichterstellung in[!DNL Adobe Customer Journey Analytics]*.

  [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] Erstellung und Aktivierung von Aktivitäten sind unabhängig von der ausgewählten Berichtsquelle zulässig. Diese Aktivitäten werden nicht unterstützt, wenn Sie [Adobe Customer Journey Analytics als Berichtsquelle ](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

  Selbst wenn Sie [!DNL Customer Journey Analytics] als Berichtsquelle angeben, wird [!DNL Target] als Berichtsquelle für [!DNL Automated Personalization] Aktivitäten verwendet.

  Wenn Sie [!DNL Customer Journey Analytics] als Berichtsquelle für [!UICONTROL Auto-Allocate] oder [!UICONTROL Auto-Target] Aktivitäten angeben, können [!DNL Target] oder [!DNL Analytics] als Berichtsquelle verwendet werden.

## Zeitzone für die Berichterstellung

Geben Sie die Zeitzone für das Reporting an.

## Währung für Berichte

Geben Sie die Währung an, die für das Reporting verwendet werden soll.

## Auszuschließende IPs aus [!DNL Target] Berichtsdaten

Geben Sie alle IP-Adressen an, die Sie aus den Berichtsdaten ausschließen möchten. Beispielsweise können Sie durch den Ausschluss interner Unternehmensadressen sicherstellen, dass Ihre Berichtsdaten die Kundeninteraktionen auf Ihrer Website widerspiegeln.

Geben Sie jede IP-Adresse in einer neuen Zeile ein.

## Geschätzte Umsatzsteigerung anzeigen

Sie können die geschätzte Steigerung des Umsatzes anzeigen, wenn Sie einen Geldwert für Ihr Ziel eingeben. [!DNL Target] kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden. Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert.

Diese Funktion kann nur von [!DNL Experience Cloud] Admin-Benutzern aktiviert oder deaktiviert werden. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.

Ausführliche Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Aktivieren der feinjustierten Prioritäten

Lassen Sie numerische Einträge für den Prioritätsbereich von 0-999 zu.

Je nach Ihren Einstellungen variieren die Benutzeroberfläche und die Optionen für die Priorität . Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.
