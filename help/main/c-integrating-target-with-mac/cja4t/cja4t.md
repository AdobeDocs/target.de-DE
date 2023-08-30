---
keywords: cja4t; Customer Journey Analytics; Customer Journey Analytics für Target; Customer Journey Analytics-Berichtsquelle; Customer Journey Analytics als Berichtsquelle für Target
description: Verwenden Sie  [!DNL Adobe Customer Journey Analytics]  für  [!DNL Target]  (A4T), um Aktivitäten basierend auf Konversionsmetriken und Zielgruppensegmenten von  [!DNL Customer Journey Analytics]  zu erstellen, und untersuchen Sie die Ergebnisse mithilfe  [!DNL Customer Journey Analytics] -Berichten.
title: Was ist [!DNL Adobe Customer Journey Analytics] für [!DNL Target] (CJA4T)?
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: ea113d1e4df68868bd9512b098ee6b17335a3e1c
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 15%

---

# [!DNL Adobe Customer Journey Analytics] als Berichtsquelle für [!DNL Adobe Target] (CJA4T)

[!DNL Customer Journey Analytics for Target] (CJA4T) ist eine lösungsübergreifende Integration, mit der Sie Aktivitäten basierend auf [Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/docs/customer-journey-analytics.html){target=_blank} Konversionsmetriken. Mithilfe der CJA4T-Integration können Sie [!DNL Customer Journey Analytics] Berichte, um Ihre Ergebnisse zu überprüfen. Wenn Sie [!DNL Customer Journey Analytics] als Berichtsquelle für eine Aktivität verwenden, basieren alle Berichte für diese Aktivität auf [!DNL Customer Journey Analytics] Datenerfassung.

## Überblick

Die [!DNL Customer Journey Analytics for Target]-Integration zwischen [!DNL Customer Journey Analytics] und [!DNL Target] bietet leistungsstarke Analysen und Tools, die Ihnen helfen, Zeit zu sparen und Ihr Marketing-Programm zu optimieren.

Die Verwendung von [!DNL Customer Journey Analytics]-Daten in [!DNL Target] bietet drei grundlegende Vorteile:

* Marketer können dynamisch [!DNL Customer Journey Analytics] Erfolgsmetriken zu [!DNL Target] Aktivitätsberichte. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Eine einzige Datenquelle minimiert die Varianz, die bei der Datenerfassung in zwei separaten Systemen auftritt.
* Ihre vorhandene [!DNL Customer Journey Analytics] -Implementierung erfasst alle erforderlichen Daten. Es ist nicht notwendig, Mboxes auf Seiten zu implementieren, nur um Daten für Berichte zu erfassen.

Beachten Sie bei der Verwendung von CJA4T die folgenden Punkte:

* Zur Verwendung von [!DNL Customer Journey Analytics] als Berichtsquelle für [!DNL Target] müssen Sie und Ihr Unternehmen Zugriff auf [!DNL Customer Journey Analytics] und [!DNL Target] haben. Wenn Sie Zugriff auf eine der Lösungen benötigen, wenden Sie sich an den Administrator Ihrer Organisation oder an Ihren Kundenbetreuer.
* Erstellen von [!DNL Target] Aktivitäten mit [!DNL Customer Journey Analytics] Berichte erstellen, müssen Sie entweder über eine[!UICONTROL Genehmiger]&quot; oder &quot;[!UICONTROL Bearbeiter]&quot; Rolle in [!DNL Target].
   * Wenn Sie [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) -Konto, siehe [Rollen und Berechtigungen festlegen](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Benutzer*.
   * Wenn Sie [Target Premium](/help/main/c-intro/intro.md#premium) -Konto, siehe [Rollen und Berechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Berechtigungen für Unternehmensbenutzer*.

* Je nach Ihren Einstellungen kann die Berichterstellung pro Aktivität oder auf Unternehmensebene geändert werden. Siehe [Reporting Cloud-Lösung](/help/main/administrating-target/reporting.md#solution) in *Konfigurieren von Berichten in Target*.
* Sie können eine der beiden Berichtsquellen verwenden. Es ist nicht möglich, Daten für eine einzelne Aktivität zu mehreren Berichtsquellen zu erfassen.
* Wenn Sie [!DNL Customer Journey Analytics] als Berichtsquelle angeben, werden Sie aufgefordert, die Sandbox für die Berichterstellung anzugeben. Während der Konfiguration sehen Sie nur die Sandboxes, auf die Sie Zugriff haben.
* Vorhandene [!DNL Target] weiterhin [!DNL Target] Datenerfassung und sind von der Aktivierung von CJA4T nicht betroffen.
* CJA4T ist nur verfügbar, wenn Sie [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html){target=_blank} and [!DNL Target] implemented through the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}. Die Unterstützung für Analytics Data Connector ist für die Zukunft geplant.
* Fragen zum Timing finden Sie unter [Latenzaspekte](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#latency){target=_blank} in *Häufig gestellte Fragen* im *Adobe Customer Analytics-Anleitung*.

## Unterstützte Aktivitätstypen

Bei Verwendung der Variablen [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} or [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank}:

| Aktivitätstypen | Kompatibel mit CJA4T? |
|--- |--- |
| [A/B-Aktivität mit manueller Traffic-Aufteilung](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [A/B-Aktivität mit automatisierter Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nein |
| [A/B-Aktivität mit automatischem Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nein |
| [Erlebnis-Targeting (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |
| [Multivarianz-Tests (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja |
| [AP-Aktivität (Automated Personalization)](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nein |
| [Recommendations-Aktivität](/help/main/c-recommendations/recommendations.md) | Ja |

## Erstellen Sie eine Aktivität, die [!DNL Customer Journey Analytics] als Berichtsquelle

Erstellen einer [!DNL Target] -Aktivität, die [!DNL Customer Journey Analytics] da die Berichtsquelle der Einrichtung einer regulären [!DNL Target] -Aktivität.

1. Aus dem **[!UICONTROL Tätigkeiten]** Liste, klicken Sie **[!UICONTROL Aktivität erstellen]**, wählen Sie dann den Aktivitätstyp aus (entsprechend dem oben unterstützten Aktivitätendiagramm) und beginnen Sie mit der Einrichtung der Aktivität.
1. Wenn Sie zur **[!UICONTROL Ziele und Einstellungen]** Seite des dreiteiligen Workflows zur Aktivitätserstellung auswählen **[!DNL Customer Journey Analytics]** als Berichtsquelle.

   ![Customer Journey Analytics als Berichtsquellenoption](/help/main/c-integrating-target-with-mac/cja4t/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >Die Berichtsquelle kann nach einer [!DNL Target] Aktivität wird live geschaltet.

1. Sandbox auswählen.

   In dieser Dropdownliste können Sie nur die Sandboxes sehen, auf die Sie Zugriff haben. Wenn eine oder mehrere Sandboxes, auf die Sie Zugriff haben, nicht in der Liste enthalten sind, überprüfen Sie, ob Sie Zugriff auf die Sandbox haben. Kontakt [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) wenn weiterhin Probleme auftreten.

   ![Sandbox-Option auswählen](/help/main/c-integrating-target-with-mac/cja4t/assets/sandbox.png)

1. Legen Sie das Aktivitätsziel fest.

   Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Sie können einen der [!DNL Target] Konversionsmetriken oder eine [!DNL Customer Journey Analytics] Metrik.

   ![Customer Journey Analytics-Metrikoption unter Zielmetrik verwenden](/help/main/c-integrating-target-with-mac/cja4t/assets/goal-metric.png)

1. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]**.

## Richten Sie eine [!DNL Customer Journey Analytics] connection

Nach [!DNL Target] -Aktivität erstellt wurde, müssen Sie eine Verbindung in [!DNL Customer Journey Analytics]. Wenn Sie bereits eine Verbindung eingerichtet haben, können Sie Ihre vorhandene Verbindung verwenden und zu Schritt 4 unten springen. Die Verbindung ermöglicht [!DNL Customer Journey Analytics] , um Daten aus dem Datensatz für die Berichterstellung abzurufen.

1. In [!DNL Customer Journey Analytics]auf **[!UICONTROL Verbindungen]** Seite, klicken **[!UICONTROL Neue Verbindung erstellen]**.

   ![Neuen Verbindungslink auf Customer Journey Analytics erstellen](/help/main/c-integrating-target-with-mac/cja4t/assets/create-connection.png)

1. Konfigurieren Sie Ihre [Verbindungs- und Dateneinstellungen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html){target=_blank} mit den richtigen Informationen.
1. Fügen Sie den Ereignis-Datensatz hinzu, den Sie beim Konfigurieren Ihres Datenspeichers verwendet haben.
1. Fügen Sie die **[!UICONTROL Adobe Target-Klassifizierungsereignisse]** Datensatz nachschlagen und auf **[!UICONTROL Nächste]**.

   ![Dialogfeld &quot;Datensätze hinzufügen&quot;im Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/add-datasets.png)

1. Konfigurieren Sie Ihren Ereignisdatensatz.

   Weitere Informationen finden Sie unter [Hinzufügen und Konfigurieren von Datensätzen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#add-dataset){target=_blank} in *Verbindung erstellen* im *Adobe Customer Journey Analytics-Anleitung*.

1. Konfigurieren Sie Ihren Lookup-Datensatz mit dem Schlüsselfeld als &quot;Schlüssel&quot; und dem Feld Übereinstimmungsschlüssel mit dem folgenden Pfad:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Adobe Target Classifications-Ereignisdialogfeld beim Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/classifications-events.png)

1. Klicks **[!UICONTROL Hinzufügen von Datensätzen]** Klicken Sie auf **[!UICONTROL Speichern]** auf dem nächsten Bildschirm, um Ihre Verbindung zu beenden.

## Datenansichten einrichten

Einrichten einer Datenansicht in [!DNL Customer Journey Analytics]. Eine Datenansicht stellt sicher, dass die Daten aus Ihrer Verbindung ordnungsgemäß verwendet werden können.

1. Richten Sie Ihre Datenansicht ein und vergewissern Sie sich, dass sie auf die oben erstellte Verbindung verweist.

   Weitere Informationen finden Sie unter [Datenansicht erstellen oder bearbeiten](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target=_blank} im *Adobe Customer Journey Analytics-Anleitung*.

1. So zeigen Sie Ihre [!DNL Target] Daten in [!DNL Customer Journey Analytics]müssen Sie die folgenden Felder aus Ihrem Lookup-Datensatz als Dimensionen hinzufügen:

   * Erlebnisname
   * Erlebnis-ID
   * Aktivitätsname
   * Aktivitäts-ID

   ![Namen- und ID-Optionen im Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Schließen Sie die Einrichtung anderer Felder ab und klicken Sie auf **[!UICONTROL Speichern und fortfahren]** wann geschehen.
