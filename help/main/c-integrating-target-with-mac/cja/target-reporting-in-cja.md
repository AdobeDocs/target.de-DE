---
keywords: Customer Journey Analytics;Customer Journey Analytics for Target;Customer Journey Analytics-Berichtsquelle;Customer Journey Analytics als Berichtsquelle für Target;Target-Reporting in CJA;Target-Reporting in Customer Journey Analytics
description: Verwenden  [!DNL Target]  In- [!DNL Adobe Customer Journey Analytics] -Berichten, um Aktivitäten basierend auf Konversionsmetriken  [!DNL Customer Journey Analytics]  Zielgruppensegmenten zu erstellen, und  [!DNL Customer Journey Analytics]  zur Untersuchung der Ergebnisse.
title: Was ist  [!DNL Target]  Reporting in [!DNL Adobe Customer Journey Analytics]?
feature: Integrations
exl-id: 67b20bf6-ffbe-4220-9455-cb3886bb9227
source-git-commit: 52f11998149cddeb4245a0f07280562d79332a04
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 57%

---

# [!DNL Target] in [!DNL Adobe Customer Journey Analytics]

Die Integration zwischen [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/customer-journey-analytics){target=_blank} und [!DNL Target] bietet leistungsstarke Analysen und zeitsparende Tools für Ihr Optimierungsprogramm.

Die wichtigsten Vorteile des Verwendens von [!DNL Customer Journey Analytics] als Berichtsquelle für [!DNL Target] sind folgende:

* Marketing-Fachleute können jederzeit dynamisch [!DNL Customer Journey Analytics]-Erfolgsmetriken auf [!DNL Target] Aktivitätsberichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Marketing-Fachleute können die Funktionen von [!DNL Customer Journey Analytics] wie z. B. das [Bedienfeld „Experimentieren“](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank} nutzen, um ihre Website-Personalisierung weitergehend zu analysieren.
* Marketingexperten können über eine zentrale Berichtsquelle für [!DNL Adobe Journey Optimizer] und [!DNL Target] verfügen. Beide Personalisierungsprodukte können mit [!DNL Customer Journey Analytics] verbunden werden, um eine ganzheitlichere Ansicht Ihrer Web-Personalisierung zu bieten.

## Zu beachten

Beachten Sie die folgenden Informationen, bevor Sie die Integration von [!DNL Customer Journey Analytics] und [!DNL Target] verwenden:

>[!IMPORTANT]
>
>Diese Integration unterscheidet sich von [[!UICONTROL Adobe Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Die unterstützten Implementierungs- und Aktivitätstypen unterscheiden sich. Lesen Sie diesen Artikel sorgfältig durch, bevor Sie diese Integration für Ihre [!DNL Target] verwenden.

* Zur Verwendung von [!DNL Customer Journey Analytics] als Berichtsquelle für [!DNL Target] müssen Sie und Ihr Unternehmen Zugriff auf [!DNL Customer Journey Analytics] und [!DNL Target] haben. Wenn Sie Zugriff auf eine der Lösungen benötigen, wenden Sie sich an die Admins Ihrer Organisation oder an Ihre Kundenkontaktperson.
* Um [!DNL Target] Aktivitäten mit [!DNL Customer Journey Analytics] Reporting zu erstellen, benötigen Sie [!DNL Target] entweder die Rolle &quot;[!UICONTROL Approver]&quot; oder &quot;[!UICONTROL Editor]&quot;.
   * Wenn Sie ein [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905)-Konto besitzen, lesen Sie [Festlegen von Rollen und Berechtigungen](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Benutzende*.
   * Wenn Sie ein [Target Premium](/help/main/c-intro/intro.md#premium)-Konto besitzen, lesen Sie [Rollen und Berechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Berechtigungen für Unternehmensbenutzende*.

* Sie müssen Teil einer Rolle in [!DNL Adobe Experience Platform] sein, um eine [!DNL Target]-Aktivität mit [!DNL Customer Journey Analytics] als Berichtsquelle einzurichten. Weitere Informationen finden Sie unter [Hinzufügen einer Rolle in [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/de/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/configure-permissions#add-a-role-in-adobe-experience-platform-requires-a-system-administrator-or-product-admin){target=_blank} unter *Berechtigungen konfigurieren* im *Tutorial für Datenarchitektinnen bzw. -architekten und Dateningenieurinnen bzw. -ingenieure.*
* Je nach Ihren Einstellungen kann das Reporting pro Aktivität oder auf Unternehmensebene geändert werden. Weitere Informationen finden Sie unter [Berichte zur Cloud-Lösung](/help/main/administrating-target/reporting.md#solution) in *Konfigurieren von Berichten in Target*.
* Sie können eine der beiden Berichtsquellen verwenden. Es ist nicht möglich, Daten für eine einzelne Aktivität für mehrere Berichtsquellen zu sammeln.
* Wenn Sie [!DNL Customer Journey Analytics] als Berichtsquelle angeben, werden Sie aufgefordert, die Sandbox für das Reporting anzugeben. Während der Konfiguration sehen Sie nur die Sandboxes, auf die Sie Zugriff haben.
* Bestehende [!DNL Target] verwenden weiterhin [!DNL Target] Datenerfassung und sind von der Aktivierung dieser Integration nicht betroffen.
* Um diese Integration zu verwenden, ist die bevorzugte Implementierungsmethode, [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/de/docs/experience-platform){target=_blank} und [!DNL Target] über die [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/de/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} implementiert zu haben.

  Wenn Sie die [!DNL Adobe Experience Platform Web SDK] derzeit nicht implementiert haben, können Sie auch eine [[!DNL Adobe Analytics] Quellverbindung“ erstellen](https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics) um die Daten in [!DNL Adobe Experience Platform] zu bringen. Wenn Sie diese Methode verwenden möchten, müssen Sie eine [!DNL Analytics] Report Suite neben der [!DNL Adobe Experience Platform] Sandbox auswählen, die Sie mit [!DNL Customer Journey Analytics] verwenden.

  ![Sandbox-Option im Dialogfeld „Reporting-Einstellungen“](/help/main/c-integrating-target-with-mac/cja/assets/aep-sandbox.png)

  >[!NOTE]
  >
  >Wenn Sie eine [!DNL Adobe Analytics] Quellverbindung verwenden, verfügen Sie über Berichte sowohl in [!DNL Adobe Analytics] als auch in [!DNL Customer Journey Analytics]. Aufgrund unterschiedlicher Algorithmen zwischen diesen beiden Lösungen ist es jedoch unwahrscheinlich, dass die Ergebnisse übereinstimmen.

* Bei Fragen zum Timing siehe [Überlegungen zur Latenz](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-overview/cja-faq#latency){target=_blank} unter *Häufig gestellte Fragen* im *[!DNL Adobe Customer Analytics]Adobe Customer Analytics-Handbuch*.

## Unterstützte Aktivitätstypen {#supported-activities}

Die folgenden Aktivitätstypen werden bei der Verwendung der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} oder der [at.js](https://experienceleague.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/overview){target=_blank} JavaScript-Bibliothek unterstützt:

| Aktivitätstypen  | Unterstützt? |
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

>[!TIP]
>
>Sie können auch festlegen, dass [!DNL Target] die Berichterstellung in [!DNL Customer Journey Analytics] für alle in Ihrem Konto erstellten Aktivitäten verwendet (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]** > **[!UICONTROL Reporting Experience Cloud Solution]**). Weitere Informationen finden Sie unter *Reporting-Cloud* in [Konfigurieren von Berichten in [!DNL Target]](/help/main/administrating-target/reporting.md#solution).

1. Klicken Sie in der Liste **[!UICONTROL Activities]** auf **[!UICONTROL Create Activity]**, wählen Sie dann den Aktivitätstyp aus (gemäß dem [unterstützten Aktivitätsdiagramm oben](#supported-activities)) und beginnen Sie mit der Einrichtung der Aktivität.
1. Wenn Sie zur **[!UICONTROL Goals & Settings]** Seite des dreiteiligen Arbeitsablaufs für die Erstellung von Aktivitäten gelangen, wählen Sie **[!DNL Customer Journey Analytics]** als Berichtsquelle aus.

   ![Customer Journey Analytics als Berichtsquellenoption](/help/main/c-integrating-target-with-mac/cja/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >Die Berichtsquelle kann nicht mehr geändert werden, nachdem eine [!DNL Target]-Aktivität live geschaltet wurde.

1. Wählen Sie eine Sandbox aus.

   In dieser Dropdown-Liste werden nur die Sandboxes angezeigt, auf die Sie Zugriff haben. Wenn eine oder mehrere Sandboxes, auf die Sie Zugriff haben, nicht in der Liste enthalten sind, überprüfen Sie, ob Sie Zugriff auf die Sandbox haben. Kontaktieren Sie die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), wenn weiterhin Probleme auftreten.

   ![Option „Sandbox auswählen“](/help/main/c-integrating-target-with-mac/cja/assets/sandbox.png)

1. Legen Sie das Aktivitätsziel fest.

   Wählen Sie eine Erfolgsmetrik aus, die als Ziel für jede Aktivität verwendet werden soll. Sie können eine der [!DNL Target]-Konversionsmetriken wählen oder eine [!DNL Customer Journey Analytics]-Metrik verwenden.

   ![Verwenden Sie eine Customer Journey Analytics-Metrikoption unter Zielmetrik](/help/main/c-integrating-target-with-mac/cja/assets/goal-metric.png)

1. Klicken Sie auf **[!UICONTROL Save & Close]**.

## Einrichten einer [!DNL Customer Journey Analytics]-Verbindung

Nachdem eine [!DNL Target]-Aktivität erstellt wurde, müssen Sie eine Verbindung in [!DNL Customer Journey Analytics] erstellen. Wenn Sie bereits eine Verbindung eingerichtet haben, können Sie Ihre vorhandene Verbindung verwenden und zu Schritt 4 übergehen. Die Verbindung ermöglicht es [!DNL Customer Journey Analytics], Daten aus dem Datensatz für das Reporting zu ziehen.

1. Klicken Sie in [!DNL Customer Journey Analytics] auf der **[!UICONTROL Connections]** Seite auf **[!UICONTROL Create a new connection]**.

   ![Erstellen eines neuen Verbindungslinks in [!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/assets/create-connection.png)

1. Konfigurieren Sie Ihre [Verbindungs- und Dateneinstellungen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-connections/overview){target=_blank} mit den richtigen Informationen.
1. Fügen Sie den Ereignis-Datensatz hinzu, den Sie beim Konfigurieren Ihres Datenstroms verwendet haben.
1. Fügen Sie den **[!UICONTROL Adobe Target Classification Events]** Lookup-Datensatz hinzu und klicken Sie dann auf **[!UICONTROL Next]**.

   ![Dialogfeld zum Hinzufügen von Datensätzen in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/assets/add-datasets.png)

1. Konfigurieren Sie Ihren Ereignisdatensatz.

   Weitere Informationen finden Sie unter [Hinzufügen und Konfigurieren von Datensätzen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-connections/create-connection#add-dataset){target=_blank} in *Erstellen einer Verbindung* im *[!DNL Adobe Customer Journey Analytics]Handbuch*.

1. Konfigurieren Sie Ihren Lookup-Datensatz mit dem [!UICONTROL Key] Feld als „Schlüssel“ und dem Feld &quot;[!UICONTROL Matching] Schlüssel“ mit dem folgenden Pfad:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Adobe Target-Klassifizierungen-Ereignisdialogfeld in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/assets/classifications-events.png)

1. Klicken Sie auf **[!UICONTROL Add datasets]** und dann auf **[!UICONTROL Save]** im nächsten Bildschirm, um die Verbindung abzuschließen.

## Einrichten von Datenansichten

Richten Sie eine Datenansicht in [!DNL Customer Journey Analytics] ein. Eine Datenansicht stellt sicher, dass die Daten aus Ihrer Verbindung ordnungsgemäß verwendet werden können.

1. Richten Sie Ihre Datenansicht ein und vergewissern Sie sich, dass sie auf die oben erstellte Verbindung verweist.

   Weitere Informationen finden Sie unter [Erstellen oder Bearbeiten einer Datenansicht](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/create-dataview){target=_blank} im *[!DNL Adobe Customer Journey Analytics]Handbuch*.

1. Um Ihre [!DNL Target]-Daten in [!DNL Customer Journey Analytics] richtig anzuzeigen, müssen Sie die folgenden Felder aus Ihrem Lookup-Datensatz als Dimensionen hinzufügen:

   * [!UICONTROL Experience Name]
   * [!UICONTROL Experience ID]
   * [!UICONTROL Activity Name]
   * [!UICONTROL Activity ID]

   ![Namen- und ID-Optionen in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Um [!DNL Target] Dimensionen im Bedienfeld &quot;[!UICONTROL Experimentation]&quot; zu verwenden, richten Sie die folgenden Kontextbeschriftungen ein:

   * Verwenden Sie [!UICONTROL Activity Name] „Experimentierexperiment“.
   * Verwenden Sie [!UICONTROL Experience Name] „Experimentvariante“.

   ![Kontextbeschriftungen im Bedienfeld „Experimentierung“](/help/main/c-integrating-target-with-mac/cja/assets/context-labels.png){width="600" zoomable="yes"}

1. Richten Sie alle anderen Felder ein und klicken Sie abschließend auf **[!UICONTROL Save and continue]**.
