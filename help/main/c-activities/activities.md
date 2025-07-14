---
keywords: Aktivitätenliste;Aktivitäten;Aktivität;Aktivitätstypen;Aktivität bearbeiten;Aktivitätsaktionen;Aktivitätsattribut;Aktivitätslistenfilter;Aktivitätsbeschränkungen;personalisieren;Personalisierung
description: Personalisieren von Inhalten und Testen von Seitendesigns für bestimmte Zielgruppen mit  [!DNL Adobe Target]  Aktivitäten.
title: Wie kann ich Inhalts- und Testseiten-Designs mit personalisieren [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: 5012c2b849d6b415f08fcaa3be85508637e30481
workflow-type: tm+mt
source-wordcount: '2292'
ht-degree: 25%

---

# Aktivitäten – Überblick

Personalisieren Sie mit [!DNL Adobe Target] Aktivitäten die Inhalts- und Testseitendesigns für bestimmte Zielgruppen.

Sie können z. B. eine Aktivität entwerfen, die zwei verschiedene Landingpages testet: eine, die Informationen zu Sommerschuhen für Damen hervorhebt, und eine andere Landingpage, die allgemein Sommerbekleidung bewirbt. Die Aktivität bestimmt die Bedingungen, die steuern, wann jede dieser Landingpages angezeigt wird, und die Metriken, die bestimmen, welche Seite erfolgreicher ist. Die Aktivität ist so konfiguriert, dass sie beginnt und endet, wenn bestimmte Bedingungen erfüllt sind, z. B. zwischen bestimmten Daten. Sie können auch festlegen, dass der Vorgang beginnt, wenn die Aktivität genehmigt ist, und endet, wenn sie deaktiviert ist.

Sie sollten den Entwurf einer Aktivität sorgfältig planen. Bestimmen Sie, wann die Aktivität beginnen soll und wie lange sie dauern soll. Führen Sie dann Ihre Angebote auf, und weisen Sie jedem dieser Angebote eine Zielgruppe zu.

## Aktivitätenliste {#section_DE8E2DB30D534962A931EF8BB48240F5}

Die [!UICONTROL Activities] ist die Standardansicht beim Öffnen von [!DNL Target]. Sie können Aktivitäten auf dieser Seite erstellen und vorhandene Aktivitäten verwalten.

Sie können die [!UICONTROL Activities] auch anzeigen, indem Sie oben in der [!UICONTROL Activities]-Benutzeroberfläche auf die Registerkarte [!DNL Target] klicken.

Die [!UICONTROL Activities] bietet einen Überblick über alle Aktivitäten in Ihrer [!DNL Target]-Implementierung und ermöglicht die Durchführung verschiedener Aktionen.

Die folgende Tabelle hilft Ihnen, die verschiedenen Elemente der [!UICONTROL Activities] in der [!DNL Target] Benutzeroberfläche zu verstehen:

| Element | Beschreibung |
|--- |--- |
| Symbol [!UICONTROL Show filters]<P>![Symbol „Filter anzeigen“](/help/main/assets/icons/Filter.svg) | Greifen Sie auf Filter zu, indem Sie auf das Symbol **[!UICONTROL Show Filters]** oben in der Liste klicken, um Aktivitäten nach [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], [!UICONTROL Decisioning Source], [!UICONTROL Activity Source] und [!UICONTROL Properties] zu filtern.<P>Filter, die Sie konfigurieren, sind für die gesamte aktuelle Sitzung persistent.<P>Weitere Informationen finden Sie [Anwenden von Filtern auf die [!UICONTROL Activities] Liste](#filters) unten. |
| Suchfelder | Schnelles Auffinden einer Aktivität oder Reduzieren der Anzahl der in der [!UICONTROL Activity] angezeigten Aktivitäten. Sie können über die Dropdown-Liste nach [!UICONTROL Activity Name], [!UICONTROL URL] oder [!UICONTROL ID] suchen.<P>Die von Ihnen konfigurierten Suchoptionen sind in der gesamten aktuellen Sitzung persistent. |
| [!UICONTROL Create Activity] | Erstellen Sie eine Aktivität.<P>Weitere Informationen zur Erstellung der verschiedenen Aktivitätstypen finden Sie unter: <ul><li>[Erstellen einer [!UICONTROL A/B Test] Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Erstellen einer [!UICONTROL Auto-Allocate] Aktivität](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Erstellen einer [!UICONTROL Auto-Target] Aktivität](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Erstellen einer [!UICONTROL Automated Personalization] Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Erstellen einer [!UICONTROL Experience Targeting] Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Erstellen einer Aktivität](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Erstellen einer [!UICONTROL Recommendations] Aktivität](/help/main/c-recommendations/recommendations.md)</li></ul>Weitere Informationen zu den einzelnen Typen finden Sie [Aktivitätstypen](#types) unten. |
| [!UICONTROL Create mobile preview link]<P>![Menü „Mehr Aktionen“](/help/main/assets/icons/MoreVertical.svg) | Verwenden Sie [Vorschaulinks für Mobilgeräte](https://experienceleague.adobe.com/de/docs/target-dev/developer/mobile-apps/target-mobile-preview) um eine einfache End-to-End-QA für Aktivitäten von Mobile Apps durchzuführen.<P>Klicken Sie auf das Symbol **Weitere Optionen**, wählen Sie den Link **Mobile Vorschau erstellen** und wählen Sie dann die Aktivitäten aus, die Sie auf Mobilgeräten testen möchten. |
| Tabelle anpassen<P>![Symbol „Tabelle anpassen“](/help/main/assets/icons/ColumnSetting.svg) | Sie können ändern, welche Spalten in der [!UICONTROL Activity] angezeigt werden, indem Sie auf das **[!UICONTROL Customize Table]** oben rechts auf der Seite klicken und dann die gewünschten Spalten auswählen oder die Auswahl aufheben.<P>Die Änderungen werden auf Ihr Konto angewendet und bleiben auch nach der Abmeldung von [!DNL Target] aktiv. |
| Kontrollkästchen für Massenvorgänge<P>![Symbol für Massenvorgänge](/help/main/assets/icons/Rectangle.svg) | Führen Sie Massenvorgänge für alle Aktivitäten oder für ausgewählte Aktivitäten durch.<P>Eine Liste der verfügbaren Aktionen (abhängig von Ihren Berechtigungen und dem Aktivitätsstatus) finden Sie [Ausführen von Schnellaktionen](#quick-actions) unten. |
| [!UICONTROL Type] | Der Aktivitätstyp. In der Spalte [!UICONTROL Type] können Sie jede Aktivität schnell nach Typ identifizieren. <ul><li>**AB-M**: manuelle [!UICONTROL A/B Test]</li><li>**AB-AA**: [!UICONTROL Auto-Allocate]</li><li>**AB-AT**: [!UICONTROL Auto-Target]</li><li>**AP**: [!UICONTROL Automated Personalization]</li><li>**XT**: [!UICONTROL Experience Targeting]</li><li>**MVT**: [!UICONTROL Multivariate Test]</li><li>**REC**: [!UICONTROL Recommendations]</li></ul>Weitere Informationen zu den einzelnen Typen finden Sie [Aktivitätstypen](#types) unten. |
| [!UICONTROL Name] | Der Name der Aktivität. Klicken Sie auf das **[!UICONTROL Quick Info]** ( ![Schnellinfo-Symbol](/help/main/assets/icons/InfoOutline.svg) ) neben jedem Aktivitätsnamen, um weitere Informationen zu dieser Aktivität in einer Popup-Karte anzuzeigen, einschließlich [!UICONTROL Activity ID], [!UICONTROL Activity Objective], [!UICONTROL Activity Location], [!UICONTROL Goal] und [!UICONTROL Status].<P>Klicken Sie neben jedem Aktivitätsnamen auf das **[!UICONTROL More actions]**-Symbol ![Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ), um ein Menü zu öffnen, in dem Sie Schnellaktionen für eine Aktivität durchführen können. Die folgenden Aktionen sind verfügbar (abhängig von Ihren Berechtigungen und dem Aktivitätsstatus): [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete] und [!UICONTROL Archive].<P>Weitere Informationen zu den einzelnen Aktionen finden Sie [Ausführen von Schnellaktionen](#quick-actions) unten.<P>Klicken Sie auf die Tabellenkopfzeile, um die Liste alphabetisch nach Namen in auf- oder absteigender Reihenfolge zu sortieren. |
| [!UICONTROL Status] | Der Status der Aktivität kann wie folgt lauten:<ul><li>**[!UICONTROL Live]**: Die Aktivität wird derzeit ausgeführt.</li><li>**[!UICONTROL Scheduled]**: Die Aktivität kann aktiviert werden, wenn das angegebene Startdatum und die angegebene Startzeit eintreffen.</li><li>**[!UICONTROL Inactive]**: Die Aktivität wurde angehalten oder deaktiviert.</li><li>**[!UICONTROL Ended]**: Das angegebene Enddatum und die angegebene Uhrzeit der Aktivität wurden erreicht, und die Aktivität wird nicht mehr bereitgestellt.</li><li>**[!UICONTROL Archived]**: Die Aktivität wurde archiviert. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.</li></ul>**Hinweis**: Wenn Sie bestimmte Aktionen durchführen, wie z. B. eine Aktivität außerhalb der [!DNL Target]-Benutzeroberfläche mithilfe von API-Methoden aktivieren, kann es bis zu 10 Minuten dauern, bis die Aktualisierung bis zur [!DNL Target]-Benutzeroberfläche propagiert wird. |
| [!UICONTROL Last Updated] | Datum und Uhrzeit der letzten Aktualisierung der Aktivität und von wem.<P>Klicken Sie auf die Tabellenkopfzeile, um die Liste in auf- oder absteigender Reihenfolge nach Datum zu sortieren. |
| [!UICONTROL Priority] | Die Priorität der Aktivität.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Je nach Ihren [Einstellungen](/help/main/administrating-target/reporting.md) variieren die [!DNL Target] Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die Legacy-Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren.<P>Weitere Informationen zu Prioritätseinstellungen finden Sie unter [Priorität](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC) unter *Aktivitätseinstellungen* in *Ziele und Einstellungen*. |
| [!UICONTROL Property] | Zeigt die [Eigenschaft](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) für die Aktivität an.<P>Berechtigungen für Unternehmensbenutzer sind eine [Target Premium](/help/main/c-intro/intro.md#premium)-Funktion. |
| [!UICONTROL Estimated Lift in Revenue] | Zeigt die voraussichtliche Umsatzsteigerung an, wenn 100 % der Zielgruppe das erfolgreichste Erlebnis sehen.<P>Zur Berechnung wird folgende Formel verwendet:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Diese Zahl wird auf maximal eine Dezimalstelle gerundet, wenn die gekürzte Form vor der Dezimalstelle nur eine Ziffer enthält. Beispiele: 1,6 Mio. $, 60 K $, 900 $, 8,5 K $, 205 K $<P>Diese Zeile zeigt „---“ für Aktivitäten, die nicht genügend Daten haben, um eine Gewinnershow anzuberaumen, oder keine Kostenschätzung haben.<P>Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md). |
| [!UICONTROL Source] | Zeigt an, wo die Aktivität erstellt wurde: [!DNL Adobe Target], [Adobe Target-API](https://experienceleague.adobe.com/de/docs/target-dev/developer/overview), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=de), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=de) oder [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Author] | Der Name der Person, die die Aktivität erstellt hat. |
| [!UICONTROL Decisioning Method] | Die in den einzelnen Aktivitäten verwendete Entscheidungsmethode: [Server-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=de) oder [Client-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html?lang=de). |

<!--|[!UICONTROL Location]|The URL for the activity identifies where the activity is displayed. This column helps you quickly identify an activity and determine whether a particular page already has an activity running on it.<P>If an activity runs on multiple URLs, a link shows how many more URLs are used. Click the link to view the complete list of URLs for that activity.<P>You can search based on the URL. Use the drop-down list next to the search box and select [!UICONTROL URL].|-->

## Aktivitätstypen  {#types}

[!DNL Target] umfasst mehrere Aktivitätstypen. In der folgenden Tabelle finden Sie einen Überblick über die einzelnen Aktivitätstypen mit Links, über die Sie mehr erfahren können. Damit Sie den Aktivitätstyp für Ihre Zwecke besser auswählen können, verwenden Sie das [Adobe Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md).

| Aktivitätstyp | Beschreibung |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | A/B-Tests vergleichen zwei oder mehr Versionen Ihres Website-Inhalts, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert. |
| [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Auto-Allocate], eine Art von A/B-Test, ermittelt aus zwei oder mehr Erlebnissen den Gewinner und weist dem Gewinner automatisch mehr Traffic zu, um die Konversionen während der Fortführung des Tests und des Lernens zu steigern. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | Automatisches Targeting, eine Art von A/B-Test, nutzt fortschrittliche Machine-Learning-Algorithmen zur Identifizierung eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen. Anhand des individuellen Kundenprofils und des Verhaltens früherer Besucher mit ähnlichen Profilen wird jedem Besucher das passendste Erlebnis bereitgestellt, um die Inhalte zu personalisieren und Konversionen zu fördern. |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) vergleicht Kombinationen von Angeboten in Elementen auf einer Seite, um festzustellen, welche Kombination für eine bestimmte Zielgruppe am besten funktioniert, und ermittelt, welches Element den größten Einfluss auf den Erfolg der Aktivität hat. |
| [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting] (XT) stellt Inhalte für eine bestimmte Zielgruppe basierend auf einem Satz aus Regeln und Kriterien bereit, die von den Werbungtreibenden definiert werden. |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besuchern basierend auf deren individuellem Kundenprofil durch erweitertes maschinelles Lernen verschiedene Varianten zu, um die Inhalte zu personalisieren und Konversionen zu fördern. |
| [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | Eine Empfehlung bestimmt, wie einem Website-Besucher ein Produkt vorgeschlagen wird, abhängig von den Aktivitäten dieses Besuchers auf der Website.<P>So können Sie zum Beispiel Personen, die einen Rucksack kaufen, dazu anregen, den Kauf von Wanderschuhen und -stöcken zu erwägen. Mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Algorithmus können Sie eine Empfehlung erstellen, die Artikel anzeigt, welche oft zusammen gekauft werden. Oder Sie möchten Besucher ermutigen, mehr Zeit auf Ihrer Medienseite zu verbringen, indem Sie dem Video, das sie gerade ansehen, ähnliche Videos empfehlen, indem Sie den Algorithmus „Personen, die sich dies angesehen haben“ verwenden.<P>**HINWEIS**: Sie können Empfehlungen auch in [!UICONTROL A/B Test]-, [!UICONTROL Auto-Allocate]-, [!UICONTROL Auto-Target]- und [!UICONTROL Experience Targeting] (XT)-Aktivitäten einfügen. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen. |

## Filter auf die Aktivitätenliste anwenden {#filters}

Greifen Sie auf Filter zu, indem Sie auf das Symbol **[!UICONTROL Show Filters]** ( ![Symbol Filter anzeigen](/help/main/assets/icons/Filter.svg) ) oben in der Liste klicken.

Im Menü können Sie Aktivitäten nach den folgenden Attributen filtern:

| Attribut | Details |
| --- | --- |
| [!UICONTROL Type] | Filtern nach [Aktivitätstyp](#types). |
| [!UICONTROL Status] | Nach Aktivitätsstatus filtern.<ul><li>**[!UICONTROL Live]**: Die Aktivität wird derzeit ausgeführt.</li><li>**[!UICONTROL Scheduled]**: Die Aktivität kann aktiviert werden, wenn das angegebene Startdatum und die angegebene Startzeit eintreffen.</li><li>**[!UICONTROL Inactive]**: Die Aktivität wurde angehalten oder deaktiviert.</li><li>**[!UICONTROL Ended]**: Das angegebene Enddatum und die angegebene Uhrzeit der Aktivität wurden erreicht, und die Aktivität wird nicht mehr bereitgestellt.</li><li>**[!UICONTROL Archived]**: Die Aktivität wurde archiviert. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.</li></ul>Weitere Informationen zu den veralteten [!UICONTROL Save as Draft] und [!UICONTROL Syncing] Status finden Sie in dem Hinweis unter dieser Tabelle. |
| [!UICONTROL Reporting Source] | Nach Berichtsquelle filtern.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): Zeigt Aktivitäten an, die [!UICONTROL Analytics for Target] (A4T) als Berichtsquelle verwenden.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): Zeigt Aktivitäten an, die [!DNL Target] als Berichtsquelle verwenden.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): Zeigt Aktivitäten an, die [!DNL Adobe Customer Analytics] als Berichtsquelle verwenden.</li></ul> |
| [!UICONTROL Experience Composer] | Filtern Sie, nach dem Experience Composer während der Aktivitätserstellung verwendet wurde:<ul><li>[Visual](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): Zeigt Aktivitäten an, die mithilfe des [!UICONTROL Visual Experience Composer] (VEC) erstellt wurden.</li><li>[Formularbasiert](/help/main/c-experiences/form-experience-composer.md): Zeigt Aktivitäten an, die mithilfe der [!UICONTROL Form-Based Experience Composer] erstellt wurden.</li></ul> |
| [!UICONTROL Metrics Type] | Filter, nach [ „Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md) bei der Erstellung der Aktivität ausgewählt wurde.<ul><li>[!UICONTROL Conversion]</li><li>[!UICONTROL Revenue]</li><li>[!UICONTROL Engagement]</li><li>[!UICONTROL Use an Analytics metric]</lI></ul> |
| [!UICONTROL Decisioning Method] | Filtern Sie nach der in den einzelnen Aktivitäten verwendeten Entscheidungsmethode.<ul><li>[Server-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=de): Zeigt Aktivitäten an, die Server-seitige Entscheidungsfindung verwenden.</li><li>[Client-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html?lang=de): Zeigt Aktivitäten an, die Client-seitige Entscheidungsfindung verwenden.</li></ul> |
| [!UICONTROL Activity Source] | Filtern Sie nach der Aktivitätsquelle, die zur Erstellung der einzelnen Aktivitäten verwendet wurde.<ul><li>[!DNL Adobe Target]</li><li>[[!DNL Adobe Target] API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=de)</li><li>[[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=de)</li><li>[[!DNL Adobe Experience Manager]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=de)</li><li>[[!DNL Adobe Mobile Services]](https://developer.adobe.com/client-sdks/home/)</li></ul> |
| [!UICONTROL Property] | Filtern Sie nach [Eigenschaft](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) in der die Aktivität erstellt wurde. |


>[!NOTE]
>
>**Aktualisierung der Aktivitätsstatus in der aktualisierten Benutzeroberfläche**: Mit den neuesten Aktualisierungen der Benutzeroberfläche sind die [!UICONTROL Save as Draft]- und [!UICONTROL Syncing] nicht mehr verfügbar. Dies liegt daran, dass die Erstellung und Bearbeitung von Aktivitäten jetzt direkt im Backend-[!DNL Target]-Bereitstellungssystem mithilfe der GraphQL-Ebene erfolgt, was einen optimierten und effizienteren Prozess gewährleistet.
>
>Zuvor wurden Aktivitäten zunächst im [!DNL Target] Frontend gespeichert und dann mit dem Backend-[!DNL Target]-Bereitstellungssystem synchronisiert, wofür diese Zwischenzustände erforderlich waren. Da dies nicht mehr der Fall ist, wurden diese Staaten entfernt.
>
>[!DNL Adobe] weiß, dass einige Kunden Interesse an der [!UICONTROL Save as Draft]-Funktion gezeigt haben. Obwohl wir dieses Feedback schätzen, wird diese Funktion derzeit nicht unterstützt.

## Ausführen von Schnellaktionen {#quick-actions}

Klicken Sie neben jedem Aktivitätsnamen auf das **[!UICONTROL More actions]**-Symbol ![Menü &quot;](/help/main/assets/icons/MoreVertical.svg) Aktionen„), um ein Menü zu öffnen, in dem Sie Schnellaktionen für eine Aktivität durchführen können.

Die folgenden Aktionen sind verfügbar (abhängig von Ihren Berechtigungen und dem Aktivitätsstatus):

| Aktion | Beschreibung |
| --- | --- |
| [!UICONTROL Edit] | Aktivität ändern. Es kann jede Aktivität bearbeitet werden.<P>Weitere Informationen zu den verschiedenen Bearbeitungsmöglichkeiten für Aktivitäten finden Sie unter [Bearbeiten einer Aktivität oder Speichern als Entwurf](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Deactivate] | Eine laufende oder geplante Änderung anhalten. Eine deaktivierte Aktivität kann reaktiviert oder archiviert werden.<P>Wenn Sie eine Aktivität deaktivieren oder archivieren und später erneut aktivieren, gehören die Besucher, die vor der Deaktivierung oder Archivierung Teil der Aktivität waren, nach der erneuten Aktivierung weiterhin zur Aktivität. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| [!UICONTROL Activate] | Startet eine inaktive oder eine zur Aktivierung bereite Aktivität. |
| [!UICONTROL Archive] | Die Aktivitätenliste an das Archiv senden. Standardmäßig werden archivierte Aktivitäten nicht mehr in der [!UICONTROL Activities] angezeigt. Ändern Sie den Filter für die [!UICONTROL Activities] so, dass er archivierte Aktivitäten enthält, um sie anzuzeigen. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.<P>Wenn Sie eine Aktivität deaktivieren oder archivieren und sie später erneut aktivieren, ist ein Besucher nach der Reaktivierung weiterhin Teil dieser Aktivität, sofern er sich in dieser Aktivität befand, bevor sie deaktiviert oder archiviert wurde. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| [!UICONTROL Copy] | Eine Aktivität kopieren. Jede Aktivität kann kopiert werden. Beim Kopieren einer Aktivität wird eine neue Aktivität mit dem gleichen Namen und dem Appendix „Copy“ erstellt. Beispielsweise wird ein Test mit der Bezeichnung „Browser Offers“ in „Browser Offers Copy“ umbenannt.<P>Visuelle Angebote werden mit der Aktivität kopiert. Sie können die Angebote in der Kopie sicher bearbeiten, ohne dass sich dies auf die ursprüngliche Aktivität auswirkt. Die einzige Ausnahme sind gespeicherte Angebote und Bilder im Inhalts-/Assets-Ordner. |
| [!UICONTROL Delete] | Einen Entwurf oder eine Aktivität löschen.<P>**HINWEIS**: Gelöschte Aktivitäten können nicht wiederhergestellt werden. Verwenden Sie die [!UICONTROL Archive] Aktion, es sei denn, Sie sind sicher, dass Sie diese Aktivität nie mehr benötigen. Anschließend können Sie die Aktivität bei Bedarf reaktivieren. |

## Zu beachten

Beachten Sie die folgenden Details zur [!UICONTROL Activity]:

* [!UICONTROL Archived] und [!UICONTROL Ended] Aktivitäten werden nicht in der [!UICONTROL Activities] angezeigt. Um diese Aktivitäten anzuzeigen, filtern Sie sie mithilfe des [Symbol „Filter](#filters) ( ![Symbol „Filter anzeigen](/help/main/assets/icons/Filter.svg) ) oben in der Liste.
* Wenn eine ursprünglich in [!DNL Target Classic] erstellte Aktivität deaktiviert oder gelöscht wird, wird sie aus [!DNL Target Standard/Premium] gelöscht. Gelöschte Aktivitäten, die ursprünglich in [!DNL Target Classic] erstellt wurden, werden nicht an den [!UICONTROL Archive] Ordner in [!DNL Target Standard/Premium] gesendet. Die Funktion für archivierte Ordner gilt nur für in [!DNL Target Standard/Premium] erstellte Aktivitäten.
* Mit allen Aktivitätstypen außer [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] können Sie entweder [!DNL Target] oder [!DNL Adobe Analytics] als Datenquelle verwenden. [!UICONTROL Automated Personalization], [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] *immer* verwenden [!DNL Target].
* Für mehrere Kanäle verfügbare Aktivitäten:

   * Web- und Mobilseiten
   * Mit dem Internet verbundene Bildschirme und Geräte, einschließlich Telefonzellen und Geldautomaten
   * E-Mail und andere Akquisekanäle oder Partnersites
   * Mobile Anwendungen
   * Weitere Möglichkeiten zur Bereitstellung getaggter Inhalte

## Einschränkungen   {#section_049D4684403A4E07B998067EB8E9BE56}

Für jede [!DNL Target]-Aktivität gelten die folgenden Inhaltsbeschränkungen:

| Element | Grenze |
|--- |--- |
| Eindeutige Selektoren | 300 Wenn ein Selektor in einem anderen Erlebnis wiederholt wird, wird er einmal gezählt. Wenn sie jedoch im selben Erlebnis wiederholt wird, wird sie erneut gezählt. |
| Angebote in jedem Erlebnis | 350 |
| Klick-Tracking-Selektoren in Metriken | 50 |
| Mboxes in Metriken | 50 |
| Zielgruppen und Orte | Kombinationen aus 50 Zielgruppen und Standorten (mbox) sollten nicht mehr als 50 sein. |

Die Aktivität kann nicht gespeichert werden, wenn Sie diese Beschränkungen überschreiten.

Wenn Sie die Anzahl dieser Elemente in Ihrer Aktivität erhöhen, wird auch die Zeit verlängert, die zum Synchronisieren der Aktivität in [!DNL Target] benötigt wird.

Weitere Informationen zu Einschränkungen des [!UICONTROL Visual Experience Composer] (VEC) finden Sie unter [Einschränkungen von Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## In [!DNL Target] importierte Attribute für Aktivitäten, die außerhalb von [!DNL Target] aktualisiert wurden {#section_802B0D174E6A44E1A96F404CA81AAE44}

Wenn in [!DNL Target] erstellte Aktivitäten von außerhalb von [!DNL Target] aktualisiert werden (z. B. über die API), werden die folgenden Aktivitätsattribute wieder in [!DNL Target] importiert: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority` und `marketingCloudMetadata(remoteModifiedBy)`.

Dieser Importvorgang wird beim Öffnen der [!UICONTROL Activities] mit einer maximalen Verzögerung von zehn Minuten ausgeführt.

