---
keywords: cja4t;Customer Journey Analytics;Customer Journey Analytics für Target;Customer Journey Analytics-Berichtsquelle;Customer Journey Analytics als Berichtsquelle für Target
description: Verwenden Sie [!DNL Adobe Customer Journey Analytics] für [!DNL Target] (A4T), um Aktivitäten basierend auf Konversionsmetriken und Zielgruppensegmenten von  [!DNL Customer Journey Analytics]  zu erstellen, und untersuchen Sie die Ergebnisse mithilfe von  [!DNL Customer Journey Analytics] -Berichten.
title: Was ist [!DNL Adobe Customer Journey Analytics] für [!DNL Target] (CJA4T)?
feature: Integrations
hide: true
hidefromtoc: true
exl-id: 67b20bf6-ffbe-4220-9455-cb3886bb9227
source-git-commit: 034d95dd797a7a9cb323094ce5bea0c78b1426ab
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 82%

---

# [!DNL Adobe Customer Journey Analytics] fungiert als Berichtsquelle für [!DNL Adobe Target] (CJA4T)

Die [!DNL Customer Journey Analytics for Target]-(CJA4T)-Integration zwischen [Adobe Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/docs/customer-journey-analytics.html?lang=de){target=_blank} und [!DNL Target] bietet leistungsstarke Analyse- und Zeitersparnis-Tools für Ihr Optimierungsprogramm.

Die wichtigsten Vorteile der Verwendung von [!DNL Customer Journey Analytics] als Berichtsquelle für [!DNL Target] sind:

* Marketing-Fachleute können jederzeit dynamisch [!DNL Customer Journey Analytics]-Erfolgsmetriken auf [!DNL Target] Aktivitätsberichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Nutzen Sie Customer Journey Analytics-Funktionen wie [Experimentierbereich](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/experimentation.html?lang=en#:~:text=The%20Experimentation%20panel%20lets%20analysts%20compare%20different%20user,which%20is%20best%20at%20driving%20a%20specific%20outcome.) , um die Personalisierung Ihrer Website weiter zu analysieren.
* Verwenden Sie eine einzige Quelle für die Berichterstellung für [Adobe Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/cja-ajo.html?lang=en) und Target. Beide Personalisierungsprodukte können mit Customer Journey Analytics verbunden werden, um eine umfassendere Ansicht Ihrer Web-Personalisierung zu erhalten.

## Zu beachten

Beachten Sie die folgenden Informationen vor Verwendung der CJA4T-Integration:

* Zur Verwendung von [!DNL Customer Journey Analytics] als Berichtsquelle für [!DNL Target] müssen Sie und Ihr Unternehmen Zugriff auf [!DNL Customer Journey Analytics] und [!DNL Target] haben. Wenn Sie Zugriff auf eine der Lösungen benötigen, wenden Sie sich an die Admins Ihrer Organisation oder an Ihre Kundenkontaktperson.
* Um [!DNL Target]-Aktivitäten mit [!DNL Customer Journey Analytics]-Berichten zu erstellen, müssen Sie entweder die Rolle „[!UICONTROL Genehmigende Person]“ oder „[!UICONTROL Bearbeiterin bzw. Bearbeiter]“ in [!DNL Target] haben.
   * Wenn Sie ein [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905)-Konto besitzen, lesen Sie [Festlegen von Rollen und Berechtigungen](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Benutzende*.
   * Wenn Sie ein [Target Premium](/help/main/c-intro/intro.md#premium)-Konto besitzen, lesen Sie [Rollen und Berechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Berechtigungen für Unternehmensbenutzende*.

* Sie müssen Teil einer Rolle in [!DNL Adobe Experience Platform] zur Einrichtung einer [!DNL Target] Aktivität mit [!DNL Customer Journey Analytics] als Berichtsquelle. Weitere Informationen finden Sie unter [Eine Rolle hinzufügen in [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/configure-permissions.html){target=_blank} in *Berechtigungen konfigurieren* im *Tutorial für Datenarchitekten und -ingenieure.*
* Je nach Ihren Einstellungen kann das Reporting pro Aktivität oder auf Unternehmensebene geändert werden. Weitere Informationen finden Sie unter [Berichte zur Cloud-Lösung](/help/main/administrating-target/reporting.md#solution) in *Konfigurieren von Berichten in Target*.
* Sie können eine der beiden Berichtsquellen verwenden. Es ist nicht möglich, Daten für eine einzelne Aktivität für mehrere Berichtsquellen zu sammeln.
* Wenn Sie [!DNL Customer Journey Analytics] als Berichtsquelle angeben, werden Sie aufgefordert, die Sandbox für das Reporting anzugeben. Während der Konfiguration sehen Sie nur die Sandboxes, auf die Sie Zugriff haben.
* Alle bestehenden [!DNL Target]-Aktivitäten verwenden weiterhin die [!DNL Target]-Datenerfassung und sind von der Aktivierung von CJA4T nicht betroffen.
* Die Verwendung von CJA4T wird von der bevorzugten Implementierungsmethode [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=de){target=_blank} and [!DNL Target] implemented through the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}. Wenn Sie derzeit kein Adobe Experience Platform Web SDK implementiert haben, können Sie auch eine [Adobe Analytics-Quellverbindung](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) , um die Daten in Adobe Experience Platform zu importieren.
* Bei Fragen zum Timing siehe [Überlegungen zur Latenz](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=de#latency){target=_blank} unter *Häufig gestellte Fragen* im *Adobe Customer Analytics-Handbuch*.

## Unterstützte Aktivitätstypen {#supported-activities}

Die folgenden Aktivitätstypen werden bei Verwendung der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} or the [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=de){target=_blank}-JavaScript-Bibliothek unterstützt:

| Aktivitätstypen | Kompatibel mit CJA4T? |
|--- |--- |
| [A/B-Aktivität mit manueller Traffic-Aufteilung](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [A/B-Aktivität mit automatisierter Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nein |
| [A/B-Aktivität mit automatischem Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nein |
| [Erlebnis-Targeting (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |
| [Multivarianz-Tests (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja |
| [AP-Aktivität (Automated Personalization)](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nein |
| [Recommendations-Aktivität](/help/main/c-recommendations/recommendations.md) | Ja |

## Erstellen einer Aktivität, die [!DNL Customer Journey Analytics] als Berichtsquelle verwendet

Das Erstellen einer [!DNL Target]-Aktivität, die [!DNL Customer Journey Analytics] als Berichtsquelle verwendet, ähnelt dem Einrichten einer regulären [!DNL Target]-Aktivität.

1. Klicken Sie in der Liste **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]**, wählen Sie dann die Art der Aktivität aus (gemäß der obigen Tabelle der [unterstützten Aktivitäten](#supported-activities)) und beginnen Sie mit der Einrichtung der Aktivität.
1. Wenn Sie die Seite **[!UICONTROL Ziele und Einstellungen]** des dreiteiligen Workflows zur Erstellung von Aktivitäten aufrufen, wählen Sie **[!DNL Customer Journey Analytics]** als Berichtsquelle.

   ![Customer Journey Analytics als Berichtsquellenoption](/help/main/c-integrating-target-with-mac/cja4t/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >Die Berichtsquelle kann nicht mehr geändert werden, nachdem eine [!DNL Target]-Aktivität live geschaltet wurde.

1. Wählen Sie eine Sandbox aus.

   In dieser Dropdown-Liste können Sie nur die Sandboxes sehen, auf die Sie Zugriff haben. Wenn eine oder mehrere Sandboxes, auf die Sie Zugriff haben, nicht in der Liste enthalten sind, überprüfen Sie, ob Sie Zugriff auf die Sandbox haben. Kontaktieren Sie die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), wenn weiterhin Probleme auftreten.

   ![Option „Sandbox auswählen“](/help/main/c-integrating-target-with-mac/cja4t/assets/sandbox.png)

1. Legen Sie das Aktivitätsziel fest.

   Wählen Sie eine Erfolgsmetrik aus, die als Ziel für jede Aktivität verwendet werden soll. Sie können eine der [!DNL Target]-Konversionsmetriken wählen oder eine [!DNL Customer Journey Analytics]-Metrik verwenden.

   ![Verwenden Sie eine Customer Journey Analytics-Metrikoption unter Zielmetrik](/help/main/c-integrating-target-with-mac/cja4t/assets/goal-metric.png)

1. Klicken Sie auf **[!UICONTROL Speichern und Schließen]**.

## Einrichten einer [!DNL Customer Journey Analytics]-Verbindung

Nachdem eine [!DNL Target]-Aktivität erstellt wurde, müssen Sie eine Verbindung in [!DNL Customer Journey Analytics] erstellen. Wenn Sie bereits eine Verbindung eingerichtet haben, können Sie Ihre vorhandene Verbindung verwenden und zu Schritt 4 übergehen. Die Verbindung ermöglicht es [!DNL Customer Journey Analytics], Daten aus dem Datensatz für das Reporting zu ziehen.

1. Klicken Sie in [!DNL Customer Journey Analytics] auf der Seite **[!UICONTROL Verbindungen]** auf **[!UICONTROL Neue Verbindung erstellen]**.

   ![Erstellen eines neuen Verbindungs-Links in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/create-connection.png)

1. Konfigurieren Sie Ihre [Verbindungs- und Dateneinstellungen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html?lang=de){target=_blank} mit den richtigen Informationen.
1. Fügen Sie den Ereignis-Datensatz hinzu, den Sie beim Konfigurieren Ihres Datenstroms verwendet haben.
1. Fügen Sie den Lookup-Datensatz **[!UICONTROL Adobe Target Classification Events]** hinzu und klicken Sie dann auf **[!UICONTROL Next]**.

   ![Dialogfeld zum Hinzufügen von Datensätzen in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/add-datasets.png)

1. Konfigurieren Sie Ihren Ereignisdatensatz.

   Weitere Informationen finden Sie unter [Hinzufügen und Konfigurieren von Datensätzen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=de#add-dataset){target=_blank} unter *Erstellen einer Verbindung* im *Adobe Customer Journey Analytics-Handbuch*.

1. Konfigurieren Sie Ihren Lookup-Datensatz mit dem Feld [!UICONTROL Schlüssel] als „Schlüssel“ und dem Feld „Übereinstimmender Schlüssel“ mit dem folgenden Pfad:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Adobe Target-Klassifizierungen-Ereignisdialogfeld in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/classifications-events.png)

1. Klicken Sie auf **[!UICONTROL Datensätze hinzufügen]** und dann auf **[!UICONTROL Speichern]** auf dem nächsten Bildschirm, um die Verbindung zu beenden.

## Einrichten von Datenansichten

Richten Sie eine Datenansicht in [!DNL Customer Journey Analytics] ein. Eine Datenansicht stellt sicher, dass die Daten aus Ihrer Verbindung ordnungsgemäß verwendet werden können.

1. Richten Sie Ihre Datenansicht ein und vergewissern Sie sich, dass sie auf die oben erstellte Verbindung verweist.

   Weitere Informationen finden Sie unter [Erstellen oder Bearbeiten einer Datenansicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=de){target=_blank} im *Adobe Customer Journey Analytics-Handbuch*.

1. Um Ihre [!DNL Target]-Daten in [!DNL Customer Journey Analytics] richtig anzuzeigen, müssen Sie die folgenden Felder aus Ihrem Lookup-Datensatz als Dimensionen hinzufügen:

   * Erlebnisname
   * Erlebnis-ID
   * Aktivitätsname
   * Aktivitäts-ID

   ![Namen- und ID-Optionen in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Beenden Sie die Eingabe aller anderen Felder und klicken Sie dann auf **[!UICONTROL Speichern und weiter]**, wenn Sie fertig sind.
