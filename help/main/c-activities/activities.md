---
keywords: Aktivitätenliste;Aktivitäten;Aktivität;Aktivitätstypen;Aktivität bearbeiten;Aktivitätsaktionen;Aktivitätsattribut;Aktivitätslistenfilter;Aktivitätsbeschränkungen;Personalisierung;Personalisierung
description: Erfahren Sie, wie Sie mit Aktivitäten in [!DNL Target] Inhalte für bestimmte Zielgruppen personalisieren und Seitenentwürfe testen können.
title: Wie kann ich Inhalte personalisieren und Seitendesigns mit [!DNL Target] testen?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: be63fa4c89f229e3f4566cb400e1268d2cdf08d2
workflow-type: tm+mt
source-wordcount: '2290'
ht-degree: 36%

---

# Aktivitäten

Mit Aktivitäten in [!DNL Adobe Target] können Sie Inhalte für bestimmte Zielgruppen personalisieren und Seitenentwürfe testen.

Sie können z. B. eine Aktivität entwerfen, die zwei verschiedene Landingpages testet: eine, die Informationen zu Sommerschuhen für Damen hervorhebt, und eine andere Landingpage, die allgemein Sommerbekleidung bewirbt. Durch die Aktivität werden die Bedingungen festgelegt, die steuern, wann diese beiden Landingpages angezeigt werden, sowie die Metriken, die bestimmen, welche Seite erfolgreicher ist. Die Aktivität wird so konfiguriert, dass sie bei Zutreffen bestimmter Bedingungen beginnt und endet (z. B. zwischen bestimmten Terminen) oder dass sie beginnt, wenn die Aktivität genehmigt wird, und endet, wenn sie deaktiviert wird.

Sie sollten den Entwurf einer Aktivität sorgfältig planen. Bestimmen Sie, wann die Aktivität beginnen soll und wie lange sie dauern soll. Führen Sie dann Ihre Angebote auf, und weisen Sie jedem dieser Angebote eine Zielgruppe zu.

## Aktivitätenliste {#section_DE8E2DB30D534962A931EF8BB48240F5}

Die Liste [!UICONTROL Activities] ist die Standardansicht beim Öffnen von [!DNL Target]. Sie können auf dieser Seite Aktivitäten erstellen und vorhandene Aktivitäten verwalten.

Sie können die Liste [!UICONTROL Activities] auch anzeigen, indem Sie auf die Registerkarte [!UICONTROL Activities] oben in der Benutzeroberfläche von [!DNL Target] klicken.

![Aktivitätenliste](/help/main/c-activities/assets/activities-list-new.png)

Die Liste [!UICONTROL Activities] bietet eine Übersicht über alle Aktivitäten und ermöglicht Ihnen die Durchführung verschiedener Aktionen:

| Element | Beschreibung |
|--- |--- |
| Linke Navigationsleiste | Wechseln Sie zwischen Ihren gespeicherten oder Live-Aktivitäten und fehlgeschlagenen oder [Entwurfsaktivitäten](/help/main/c-activities/edit-activity.md). |
| Symbol [!UICONTROL Show filters]<P>![Symbol &quot;Filter anzeigen&quot;](/help/main/c-activities/assets/show-filters-icon.png) | Greifen Sie auf Filter zu, indem Sie oben in der Liste auf das Symbol **[!UICONTROL Show Filters]** klicken.<P>Weitere Informationen finden Sie unten unter [Anwenden von Filtern auf die Aktivitätenliste](#filters). |
| Suchfeld | Suchen Sie schnell eine Aktivität oder reduzieren Sie die Anzahl der in der Liste [!UICONTROL Activity] angezeigten Aktivitäten. Sie können nach [!UICONTROL Name], [!UICONTROL URL] oder [!UICONTROL ID] suchen. |
| [!UICONTROL Create Activity] | Erstellen Sie eine Aktivität. Weitere Informationen zur Erstellung der verschiedenen Aktivitätstypen finden Sie unter: <ul><li>[Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Erstellen einer automatischen Zuordnungsaktivität](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Erstellen einer automatischen Targeting-Aktivität](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Erstellen einer Automated Personalization-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Erstellen eines Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/recommendations.md)</li></ul>Weitere Informationen zu den einzelnen Typen finden Sie unten unter [Aktivitätstypen](#types). |
| [!UICONTROL Create mobile preview link]<P>![Menü &quot;Mehr Aktionen&quot;](/help/main/c-activities/assets/icon-create-mobile-link.png) | Verwenden Sie [mobile Vorschaulinks](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html?lang=de), um eine einfache durchgängige Qualitätssicherung für Aktivitäten mobiler Apps durchzuführen.<P>Klicken Sie auf das Symbol &quot;**Mehr Optionen**&quot;(die vertikale Ellipse), wählen Sie &quot;**Mobile Vorschaulink erstellen**&quot;und wählen Sie dann die Aktivitäten aus, die Sie auf einem Mobilgerät testen möchten. |
| Tabelle anpassen<P>![Symbol &quot;Tabelle anpassen&quot;](/help/main/c-activities/assets/icon-customize-table.png) | Ändern Sie, welche Spalten in der Liste [!UICONTROL Activity] angezeigt werden, indem Sie auf das Symbol **[!UICONTROL Customize Table]** oben rechts in der Tabelle klicken und dann die gewünschten Spalten auswählen oder deaktivieren.<P>Die Änderungen werden auf Ihr Konto angewendet und bleiben auch dann aktiv, wenn Sie sich von [!DNL Target] abmelden. |
| Kontrollkästchen für Massenvorgänge | Führen Sie Massenvorgänge für alle Aktivitäten oder für ausgewählte Aktivitäten durch.<P>Eine Liste der verfügbaren Aktionen (abhängig von Ihren Berechtigungen und dem Aktivitätsstatus) finden Sie unten unter [Durchführen von Schnellaktionen](#quick-actions) . |
| [!UICONTROL Type] | Der Aktivitätstyp. In der Spalte [!UICONTROL Type] können Sie jede Aktivität schnell nach Typ identifizieren. <ul><li>AB-M: manual [!UICONTROL A/B Test]</li><li>AB-AA: [!UICONTROL Auto-Allocate]</li><li>AB-AT: [!UICONTROL Auto-Target]</li><li>AP: [!UICONTROL Automated Personalization]</li><li>XT: [!UICONTROL Experience Targeting]</li><li>MVT: [!UICONTROL Multivariate Test]</li><li>REC: [!UICONTROL Recommendations]</li></ul>Weitere Informationen zu den einzelnen Typen finden Sie unten unter [Aktivitätstypen](#types). |
| [!UICONTROL Name] | Der Name der Aktivität. Klicken Sie auf einen Aktivitätsnamen, um die Seite [!UICONTROL Overview] dieser Aktivität anzuzeigen. <P>Klicken Sie auf das Symbol **[!UICONTROL Quick Info]** neben dem jeweiligen Aktivitätsnamen, um weitere Informationen zu dieser Aktivität in einer Pop-up-Karte anzuzeigen.<p>Klicken Sie auf das Symbol &quot;**[!UICONTROL More actions]**&quot;(die horizontalen Auslassungspunkte) neben dem jeweiligen Aktivitätsnamen, um ein Menü zu öffnen, über das Sie für eine Aktivität Schnellaktionen durchführen können. Die folgenden Aktionen sind verfügbar (je nach Ihren Berechtigungen und dem Aktivitätsstatus): [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete] und [!UICONTROL Archive]. Weitere Informationen zu den einzelnen Aktionen finden Sie unten unter [Schnellaktionen durchführen](#quick-actions) .<P>Klicken Sie auf die Tabellenüberschrift, um die Liste alphabetisch in auf- oder absteigender Reihenfolge nach Namen zu sortieren. |
| [!UICONTROL Status] | Der Status der Aktivität kann wie folgt lauten:<ul><li>**Live**: Die Aktivität wird derzeit ausgeführt.</li><li>**Entwurf**: Die Aktivitätseinrichtung wurde gestartet, die Aktivität befindet sich jedoch im [Entwurfsmodus](/help/main/c-activities/edit-activity.md) und kann noch nicht ausgeführt werden.</li><li>**Geplant:** Die Aktivität wird zum festgelegten Startdatum und zur festgelegten Startzeit aktiviert.</li><li>**Inaktiv:** Die Aktivität wurde angehalten oder deaktiviert.</li><li>**Synchronisierung**: Die Aktivität wurde gespeichert und wird mit dem [!DNL Target]-Bereitstellungsnetzwerk synchronisiert.</li><li>**Beendet**: Das angegebene Enddatum und die angegebene Endzeit der Aktivität wurden erreicht und die Aktivität wird nicht mehr bedient.</li><li>**Archiviert:** Die Aktivität wurde archiviert. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.</li></ul>**Hinweis**: Wenn Sie bestimmte Aktionen ausführen, z. B. eine Aktivität außerhalb der [!DNL Target] -Benutzeroberfläche mit API-Methoden aktivieren, kann es bis zu zehn Minuten dauern, bis die Aktualisierung auf die [!DNL Target] -Benutzeroberfläche propagiert wird. |
| [!UICONTROL Last Updated] | Datum und Uhrzeit der letzten Aktualisierung der Aktivität und nach wem.<P>Klicken Sie auf die Tabellenüberschrift, um die Liste in auf- oder absteigender Reihenfolge nach Datum zu sortieren. |
| [!UICONTROL Priority] | Die Priorität der Aktivität.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Je nach Ihren [Einstellungen](/help/main/administrating-target/reporting.md) variieren die [!DNL Target] Benutzeroberfläche und Optionen für [!UICONTROL Priority]. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren. |
| [!UICONTROL Property] | Zeigt die [Eigenschaft](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) für die Aktivität an.<P>Berechtigungen für Unternehmensbenutzer sind eine Funktion von [Target Premium](/help/main/c-intro/intro.md#premium) . |
| [!UICONTROL Estimated Lift in Revenue] | Zeigt die voraussichtliche Umsatzsteigerung an, wenn 100 % der Zielgruppe das erfolgreichste Erlebnis sehen.<P>Zur Berechnung wird folgende Formel verwendet:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Diese Zahl wird auf maximal eine Dezimalstelle gerundet, wenn die gekürzte Form vor der Dezimalstelle nur eine Ziffer enthält. Beispiele: 1,6 Mio. $, 60 K $, 900 $, 8,5 K $, 205 K $<P>Diese Zeile zeigt „---“ für Aktivitäten, die nicht genügend Daten haben, um eine Gewinnershow anzuberaumen, oder keine Kostenschätzung haben.<P>Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md). |
| [!UICONTROL Source] | Zeigt an, wo die Aktivität erstellt wurde: [!DNL Adobe Target], [Adobe Target API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=de), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=de), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=de) oder [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Location] | Die URL für die Aktivität identifiziert, wo die Aktivität angezeigt wird. Diese Spalte hilft Ihnen dabei, eine Aktivität schnell zu identifizieren und festzustellen, ob auf einer bestimmten Seite bereits eine Aktivität ausgeführt wird.<P>Wenn eine Aktivität auf mehreren URLs ausgeführt wird, zeigt ein Link, wie viele weitere URLs verwendet werden. Klicken Sie auf den Link, um die vollständige Liste an URLs für diese Aktivität anzuzeigen.<P>Sie können anhand der URL suchen. Verwenden Sie die Dropdownliste neben dem Suchfeld und wählen Sie [!UICONTROL URL] aus. |
| Autor | Der Name der Person, die die Aktivität erstellt hat. |
| [!UICONTROL Decisioning Method] | Die in jeder Aktivität verwendete Entscheidungsmethode: [Server-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=de) oder [Client-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

## Aktivitätstypen  {#types}

[!DNL Target] umfasst mehrere Aktivitätstypen. In der folgenden Tabelle finden Sie einen Überblick über die einzelnen Aktivitätstypen mit Links, über die Sie mehr erfahren können. Damit Sie besser den Aktivitätstyp für Ihre Zwecke auswählen können, haben wir auch das [Adobe Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md) erstellt.

| Aktivitätstyp | Beschreibung |
|--- |--- |
| [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) | Beim A/B-Test werden zwei oder mehr Versionen Ihres Website-Inhalts verglichen, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert. |
| [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Auto-Allocate], ein A/B-Test, identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird. |
| [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | Beim automatischen Targeting, einer Art von A/B-Test, werden mehrere von Marketingexperten definierte Erlebnisse mit hoher Leistung über das erweiterte maschinelle Lernen identifiziert. Zudem erhalten alle Besucher basierend auf dem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen ein optimal auf sie zugeschnittenes Erlebnis, um Inhalte zu personalisieren und Konversionen zu fördern. |
| [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) vergleicht Kombinationen aus Angeboten in Elementen auf einer Seite, um zu bestimmen, welche Kombination für eine bestimmte Zielgruppe die beste Leistung erzielt, und identifiziert, welches Element den größten Einfluss auf den Erfolg der Aktivität hat. |
| [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting] (XT) stellt Inhalte für eine bestimmte Zielgruppe basierend auf einem Satz von durch Marketingexperten definierten Regeln und Kriterien bereit. |
| [Automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besuchern basierend auf ihrem individuellen Kundenprofil mithilfe des erweiterten maschinellen Lernens verschiedene Varianten zu, um die Inhalte zu personalisieren und Konversionen zu fördern. |
| [Recommendations](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | Eine Empfehlung bestimmt, wie ein Produkt einem Website-Besucher je nach den Aktivitäten dieses Besuchers auf der Site vorgeschlagen wird.<P>So können Sie zum Beispiel Personen, die einen Rucksack kaufen, dazu anregen, den Kauf von Wanderschuhen und -stöcken zu erwägen. Mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Algorithmus können Sie eine Empfehlung erstellen, die Artikel anzeigt, welche oft zusammen gekauft werden. Oder Sie möchten Besucher dazu anregen, mehr Zeit auf Ihrer Medienwebsite zu verbringen, indem Sie mit dem Algorithmus &quot;Personen, die das Video angesehen haben, haben auch dieses Video angesehen&quot;Videos empfehlen, die dem angesehenen Video ähneln.<P>**HINWEIS**: Sie können auch Empfehlungen in die Aktivitäten [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] und [!UICONTROL Experience Targeting] (XT) einbeziehen. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen. |

## Filter auf die Aktivitätenliste anwenden {#filters}

Greifen Sie auf Filter zu, indem Sie oben in der Liste auf das Symbol **[!UICONTROL Show Filters]** klicken.

![Filteroptionen](/help/main/c-activities/assets/show-filters-options.png)

Im Menü können Sie Aktivitäten nach folgenden Attributen filtern:
|Attribut|Details|
| — | — |
|[!UICONTROL Type]|Filtern nach [Aktivitätstyp](#types).|
|[!UICONTROL Status]|Filtern nach Aktivitätsstatus.|
|[!UICONTROL Reporting Source]|Filtern nach Berichtsquelle.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): Zeigt Aktivitäten an, die [!UICONTROL Analytics for Target] (A4T) als Berichtsquelle verwenden.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): Zeigt Aktivitäten an, die [!DNL Target] als Berichtsquelle verwenden.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): Zeigt Aktivitäten an, die [!DNL Adobe Customer Analytics] als Berichtsquelle verwenden.</li></ul>|
|[!UICONTROL Experience Composer]|Filtern, nach welchem Experience Composer bei der Aktivitätserstellung verwendet wurde:<ul><li>[Visual](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): Zeigt Aktivitäten an, die mit dem VEC (2}) erstellt wurden.[!UICONTROL Visual Experience Composer]</li><li>[Formularbasiert](/help/main/c-experiences/form-experience-composer.md): Zeigt Aktivitäten an, die mit dem [!UICONTROL Form-Based Experience Composer] erstellt wurden.</li></ul>|
|[!UICONTROL Metrics Type]|Filtern Sie, nach welchem [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md) bei der Erstellung einer Aktivität ausgewählt wurde.<ul><li>Konversion</li><li>Umsatz</li><li>Interaktion</li></ul>|
|[!UICONTROL Decisioning Method]|Filtern nach der in den einzelnen Aktivitäten verwendeten Entscheidungsmethode<ul><li>[Serverseitig](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=de): Zeigt Aktivitäten an, die serverseitige Entscheidungen verwenden.</li><li>[Client-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): Zeigt Aktivitäten an, die clientseitige Entscheidungen verwenden.</li></ul>|
|[!UICONTROL Activity Source]|Filtern Sie nach der Aktivitätsquelle, mit der die einzelnen Aktivitäten erstellt werden.<ul><li>[!DNL Adobe Target]</li><li>[Adobe Target-API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=de)</li><li>[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=de)</li><li>[Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=de)</li><li>[Adobe Mobile-Dienste](https://developer.adobe.com/client-sdks/documentation/)</li></ul>|
|[!UICONTROL Property]|Filtern Sie nach der [Eigenschaft](/help/main/administrating-target/c-user-management/property-channel/property-channel.md), in der die Aktivität erstellt wurde.|

## Schnellaktionen durchführen {#quick-actions}

Klicken Sie auf das Symbol &quot;**[!UICONTROL More actions]**&quot;(die horizontalen Auslassungspunkte) neben dem jeweiligen Aktivitätsnamen, um ein Menü zu öffnen, über das Sie für eine Aktivität Schnellaktionen durchführen können.

![Optionen für Schnellaktionen](/help/main/c-activities/assets/quick-actions.png)

Die folgenden Aktionen sind verfügbar (je nach Berechtigungen und Aktivitätsstatus):

| Aktion | Beschreibung |
| --- | --- |
| [!UICONTROL Edit] | Aktivität ändern. Es kann jede Aktivität bearbeitet werden.<P>Weitere Informationen zu den verschiedenen Methoden zum Bearbeiten von Aktivitäten finden Sie unter [Bearbeiten einer Aktivität oder Speichern als Entwurf](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Deactivate] | Eine laufende oder geplante Änderung anhalten. Eine deaktivierte Aktivität kann reaktiviert oder archiviert werden.<P>Wenn Sie eine Aktivität deaktivieren oder archivieren und später erneut aktivieren, gehören die Besucher, die vor der Deaktivierung oder Archivierung Teil der Aktivität waren, nach der erneuten Aktivierung weiterhin zur Aktivität. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| [!UICONTROL Activate] | Starten Sie eine inaktive Aktivität oder eine Aktivität, die zur Aktivierung bereit ist. |
| [!UICONTROL Archive] | Die Aktivitätenliste an das Archiv senden. Archivierte Aktivitäten werden standardmäßig nicht mehr in der Liste [!UICONTROL Activities] angezeigt. Ändern Sie den Filter für die Aktivitätenliste, damit auch archivierte Aktivitäten angezeigt werden. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.<P>Wenn Sie eine Aktivität deaktivieren oder archivieren und später erneut aktivieren, gehören die Besucher, die vor der Deaktivierung oder Archivierung Teil der Aktivität waren, nach der erneuten Aktivierung weiterhin zur Aktivität. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| [!UICONTROL Copy] | Eine Aktivität kopieren. Jede Aktivität kann kopiert werden. Beim Kopieren einer Aktivität wird eine neue Aktivität mit dem gleichen Namen und dem Appendix „Copy“ erstellt. Beispielsweise wird ein Test mit der Bezeichnung „Browser Offers“ in „Browser Offers Copy“ umbenannt.<P>Visuelle Angebote werden mit der Aktivität kopiert. Sie können die Angebote in der Kopie sicher bearbeiten, ohne dass sich dies auf die ursprüngliche Aktivität auswirkt. Die einzige Ausnahme sind gespeicherte Angebote und Bilder im Inhalts-/Assets-Ordner. |
| [!UICONTROL Delete] | Einen Entwurf oder eine Aktivität löschen.<P>**HINWEIS**: Gelöschte Aktivitäten können nicht wiederhergestellt werden. Verwenden Sie die Aktion [!UICONTROL Archive] , es sei denn, Sie sind sicher, dass Sie diese Aktivität nie mehr benötigen werden. Danach können Sie die Aktivität bei Bedarf reaktivieren. |

## Zu beachten

Beachten Sie die folgenden Details zur Liste [!UICONTROL Activity] :

* Archivierte und beendete Aktivitäten werden nicht in der Liste [!UICONTROL Activities] angezeigt. Um diese Aktivitäten anzuzeigen, filtern Sie sie mit dem [Filtersymbol](#filters) oben in der Liste.
* Wenn eine ursprünglich in [!DNL Target Classic] erstellte Aktivität deaktiviert oder gelöscht wird, wird sie aus [!DNL Target Standard/Premium] gelöscht. Gelöschte Aktivitäten, die ursprünglich in [!DNL Target Classic] erstellt wurden, werden nicht an den Ordner [!UICONTROL Archive] in [!DNL Target Standard/Premium] gesendet. Die Funktion für archivierte Ordner gilt nur für in [!DNL Target Standard/Premium] erstellte Aktivitäten.
* Bei allen anderen Aktivitätstypen als [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] haben Sie die Wahl zwischen [!DNL Target] und [!DNL Adobe Analytics] als Datenquelle. [!UICONTROL AP], [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] *immer* verwenden [!DNL Target] Daten.
* Für mehrere Kanäle verfügbare Aktivitäten:

   * Web- und Mobilseiten
   * Mit dem Internet verbundene Bildschirme und Geräte, einschließlich Telefonzellen und Geldautomaten
   * E-Mail und andere Akquisekanäle oder Partnersites
   * Mobile Anwendungen
   * Weitere Möglichkeiten zur Bereitstellung getaggter Inhalte

## Einschränkungen   {#section_049D4684403A4E07B998067EB8E9BE56}

Für jede Target-Aktivität gelten die folgenden Inhaltsbeschränkungen:

| Element | Grenze |
|--- |--- |
| Eindeutige Selektoren | 300, wenn ein Selektor in einem anderen Erlebnis wiederholt wird, wird er einmal gezählt. Wenn sie jedoch im selben Erlebnis wiederholt wird, wird sie erneut gezählt. |
| Angebote in jedem Erlebnis | 350 |
| Klick-Tracking-Selektoren in Metriken | 50 |
| Mboxes in Metriken | 50 |
| Zielgruppen und Orte | 50 Zielgruppen- und Standortkombinationen (Mbox) dürfen nicht mehr als 50 betragen. |

Die Aktivität kann nicht gespeichert werden, wenn Sie diese Beschränkungen überschreiten.

Wenn Sie die Anzahl dieser Elemente in Ihrer Aktivität erhöhen, verlängert sich auch die Zeit, die zum Synchronisieren der Aktivität über [!DNL Target] benötigt wird.

Weitere Einschränkungen von V[!UICONTROL isual Experience Composer] VEC finden Sie unter [Einschränkungen von Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## In [!DNL Target] importierte Attribute für Aktivitäten, die außerhalb von [!DNL Target] aktualisiert wurden {#section_802B0D174E6A44E1A96F404CA81AAE44}

Wenn in [!DNL Target] erstellte Aktivitäten außerhalb von [!DNL Target] aktualisiert werden (z. B. über die API), werden die folgenden Aktivitätsattribute wieder in [!DNL Target] importiert: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority` und `marketingCloudMetadata(remoteModifiedBy)`.

Dieser Importauftrag wird ausgeführt, wenn die Aktivitätsseite geöffnet wird, mit einer maximalen Verzögerung von zehn Minuten.

## Schulungsvideos {#section_BE80D13A2E81460C885F902010E1AD87}

Das folgende Video enthält weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätstypen (9:03)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

