---
keywords: Aktivitätenliste;Aktivitäten;Aktivität;Aktivitätstypen;Aktivität bearbeiten;Aktivitätsaktionen;Aktivitätsattribut;Aktivitätslistenfilter;Aktivitätsbeschränkungen;Personalisierung;Personalisierung
description: Erfahren Sie, wie Aktivitäten auf Adobe ausgeführt werden [!DNL Target] Sie können Inhalte für bestimmte Zielgruppen personalisieren und Seitenentwürfe testen.
title: Wie kann ich Inhalte personalisieren und Seitendesigns testen mit [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: 4b62017fe4dca61b5b05c7778f3a02cf446c17f7
workflow-type: tm+mt
source-wordcount: '2487'
ht-degree: 44%

---

# Aktivitäten

Mit den Aktivitäten in [!DNL Adobe Target] können Sie Inhalte an bestimmte Zielgruppen anpassen und Ihre Seitendesigns testen.

Sie können z. B. eine Aktivität entwerfen, die zwei verschiedene Landingpages testet: eine, die Informationen zu Sommerschuhen für Damen hervorhebt, und eine andere Landingpage, die allgemein Sommerbekleidung bewirbt. Durch die Aktivität werden die Bedingungen festgelegt, die steuern, wann diese beiden Landingpages angezeigt werden, sowie die Metriken, die bestimmen, welche Seite erfolgreicher ist. Die Aktivität wird so konfiguriert, dass sie bei Zutreffen bestimmter Bedingungen beginnt und endet (z. B. zwischen bestimmten Terminen) oder dass sie beginnt, wenn die Aktivität genehmigt wird, und endet, wenn sie deaktiviert wird.

Sie sollten den Entwurf einer Aktivität sorgfältig planen. Bestimmen Sie, wann die Aktivität beginnen soll und wie lange sie dauern soll. Führen Sie dann Ihre Angebote auf, und weisen Sie jedem dieser Angebote eine Zielgruppe zu.

## Aktivitätenliste {#section_DE8E2DB30D534962A931EF8BB48240F5}

Die Liste [!UICONTROL Aktivitäten] ist die Standardansicht beim Öffnen [!DNL Target]. Sie können auf dieser Seite Aktivitäten erstellen und vorhandene Aktivitäten verwalten.

Sie können die Liste [!UICONTROL Aktivitäten] auch anzeigen, indem Sie oben in der [!DNL Target]-Benutzeroberfläche auf die Registerkarte [!UICONTROL Aktivitäten] klicken.

>[!NOTE]
>
>Die folgende Abbildung und Tabelle zeigt die Funktionalität der aktualisierten Aktivitätenlisten-Benutzeroberfläche, die sich derzeit in der Beta-Phase befindet und demnächst veröffentlicht wird.


![Aktivitätenliste](/help/main/c-activities/assets/activities-list-new.png)

Die [!UICONTROL Tätigkeiten] Die Liste bietet eine Übersicht über alle Aktivitäten und ermöglicht die Durchführung verschiedener Aktionen:

| Element | Beschreibung |
|--- |--- |
| Linke Navigationsleiste | Zwischen gespeicherten oder Live-Aktivitäten und fehlgeschlagenen Aktivitäten wechseln oder [Entwürfe von Aktivitäten](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Filter anzeigen] icon<P>![Symbol Filter anzeigen](/help/main/c-activities/assets/show-filters-icon.png) | Zugriff auf Filter durch Klicken auf **[!UICONTROL Filter anzeigen]** -Symbol am oberen Rand der Liste.<P>Weitere Informationen finden Sie unter [Filter auf die Aktivitätenliste anwenden](#filters) unten. |
| Suchfeld | Suchen Sie schnell eine Aktivität oder reduzieren Sie die Anzahl der in der [!UICONTROL Aktivität] Liste. Sie können nach [!UICONTROL Name], [!UICONTROL URL]oder [!UICONTROL ID]. |
| [!UICONTROL Aktivität erstellen] | Erstellen Sie eine Aktivität. Weitere Informationen zur Erstellung der verschiedenen Aktivitätstypen finden Sie unter: <ul><li>[Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Erstellen einer automatischen Zuordnungsaktivität](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Erstellen einer automatischen Targeting-Aktivität](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Erstellen einer Automated Personalization-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Erstellen eines Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/recommendations.md)</li></ul>Weitere Informationen zu den einzelnen Typen finden Sie unter [Aktivitätstypen](#types) unten. |
| [!UICONTROL Link zur mobilen Vorschau erstellen]<P>![Menü &quot;Mehr Aktionen&quot;](/help/main/c-activities/assets/icon-create-mobile-link.png) | Verwendung [mobile Vorschaulinks](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html?lang=de) zur einfachen durchgängigen Qualitätssicherung von App-Aktivitäten.<P>Klicken Sie auf **Weitere Optionen** -Symbol (die vertikale Ellipse), wählen Sie die **Link zur mobilen Vorschau erstellen** und wählen Sie dann die Aktivitäten aus, die Sie auf einem Mobilgerät testen möchten. |
| Tabelle anpassen<P>![Symbol &quot;Tabelle anpassen&quot;](/help/main/c-activities/assets/icon-customize-table.png) | Ändern der Spaltenanzeige in [!UICONTROL Aktivität] Liste durch Klicken auf **[!UICONTROL Tabelle anpassen]** rechts oben in der Tabelle ein und wählen die gewünschten Spalten aus oder heben die Auswahl auf.<P>Die Änderungen werden auf Ihr Konto angewendet und bleiben auch dann aktiv, wenn Sie sich von [!DNL Target]. |
| Kontrollkästchen für Massenvorgänge | Führen Sie Massenvorgänge für alle Aktivitäten oder für ausgewählte Aktivitäten durch.<P>Eine Liste der verfügbaren Aktionen (abhängig von Ihren Berechtigungen und dem Aktivitätsstatus) finden Sie unter [Schnellaktionen durchführen](#quick-actions) unten. |
| [!UICONTROL Typ] | Der Aktivitätstyp. Die [!UICONTROL Typ] ermöglicht es Ihnen, jede Aktivität schnell nach Typ zu identifizieren. <ul><li>AB-M: Handbuch [!UICONTROL A/B-Test]</li><li>AB-AA: [!UICONTROL Automatische Zuordnung]</li><li>AB-AT: [!UICONTROL Automatisches Targeting]</li><li>AP: [!UICONTROL Automated Personalization]</li><li>XT: [!UICONTROL Erlebnis-Targeting]</li><li>MVT: [!UICONTROL Multivarianz-Test]</li><li>REC: [!UICONTROL Recommendations]</li></ul>Weitere Informationen zu den einzelnen Typen finden Sie unter [Aktivitätstypen](#types) unten. |
| [!UICONTROL Name] | Der Name der Aktivität. Klicken Sie auf einen Aktivitätsnamen, um die [!UICONTROL Übersicht] Seite. <P>Klicken Sie auf **[!UICONTROL Schnellinformationen]** neben dem jeweiligen Aktivitätsnamen, um weitere Informationen zu dieser Aktivität in einer Pop-up-Karte anzuzeigen.<p>Klicken Sie auf **[!UICONTROL Mehr Aktionen]** neben dem jeweiligen Aktivitätsnamen (die horizontalen Auslassungspunkte), um ein Menü zu öffnen, über das Sie Schnellaktionen für eine Aktivität durchführen können. Die folgenden Aktionen sind verfügbar (je nach Berechtigungen und Aktivitätsstatus): [!UICONTROL Bearbeiten], [!UICONTROL Aktivieren], [!UICONTROL Deaktivieren], [!UICONTROL Kopieren], [!UICONTROL Löschen], und [!UICONTROL Archivieren]. Weitere Informationen zu den einzelnen Aktionen finden Sie unter [Schnellaktionen durchführen](#quick-actions) unten.<P>Klicken Sie auf die Tabellenüberschrift, um die Liste alphabetisch in auf- oder absteigender Reihenfolge nach Namen zu sortieren. |
| [!UICONTROL Status] | Der Status der Aktivität kann wie folgt lauten:<ul><li>**Live**: Die Aktivität wird derzeit ausgeführt.</li><li>**Entwurf**: Die Aktivitätseinrichtung wurde gestartet, die Aktivität befindet sich jedoch in der [Entwurfsmodus](/help/main/c-activities/edit-activity.md) und noch nicht bereit zur Ausführung ist.</li><li>**Geplant:** Die Aktivität wird zum festgelegten Startdatum und zur festgelegten Startzeit aktiviert.</li><li>**Inaktiv:** Die Aktivität wurde angehalten oder deaktiviert.</li><li>**Synchronisierung**: Die Aktivität wurde gespeichert und wird mit der [!DNL Target] Versandnetzwerk.</li><li>**Beendet**: Das angegebene Enddatum und die angegebene Uhrzeit der Aktivität wurden erreicht und die Aktivität wird nicht mehr bedient.</li><li>**Archiviert:** Die Aktivität wurde archiviert. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.</li></ul>**Hinweis:**[!DNL Target] Wenn Sie bestimmte Aktionen ausführen (z. B. eine Aktivität außerhalb der Benutzeroberfläche über API-Methoden aktivieren), kann es bis zu 10 Minuten dauern, bis die Aktualisierung bis zur Benutzeroberfläche propagiert wird.[!DNL Target] |
| [!UICONTROL Zuletzt aktualisiert] | Datum und Uhrzeit der letzten Aktualisierung der Aktivität und nach wem.<P>Klicken Sie auf die Tabellenüberschrift, um die Liste in auf- oder absteigender Reihenfolge nach Datum zu sortieren. |
| [!UICONTROL Priorität] | Die Priorität der Aktivität.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Je nach [settings](/help/main/administrating-target/reporting.md), die [!DNL Target] Benutzeroberfläche und Optionen für [!UICONTROL Priorität] variieren. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren. |
| [!UICONTROL Eigenschaft] | Zeigt die [Eigenschaft](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) für die Aktivität an.<P>Berechtigungen für Unternehmensbenutzer sind [Target Premium](/help/main/c-intro/intro.md#premium) Funktion. |
| [!UICONTROL Geschätzte Umsatzsteigerung] | Zeigt die voraussichtliche Umsatzsteigerung an, wenn 100 % der Zielgruppe das erfolgreichste Erlebnis sehen.<P>Zur Berechnung wird folgende Formel verwendet:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Diese Zahl wird auf maximal eine Dezimalstelle gerundet, wenn die gekürzte Form vor der Dezimalstelle nur eine Ziffer enthält. Beispiele: 1,6 Mio. $, 60 K $, 900 $, 8,5 K $, 205 K $<P>Diese Zeile zeigt „---“ für Aktivitäten, die nicht genügend Daten haben, um eine Gewinnershow anzuberaumen, oder keine Kostenschätzung haben.<P>Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md). |
| [!UICONTROL Quelle] | Zeigt an, wo die Aktivität erstellt wurde: [!DNL Adobe Target], [Adobe Target-API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=de), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=de), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html)oder [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Standort] | Die URL für die Aktivität identifiziert, wo die Aktivität angezeigt wird. Diese Spalte hilft Ihnen dabei, eine Aktivität schnell zu identifizieren und festzustellen, ob auf einer bestimmten Seite bereits eine Aktivität ausgeführt wird.<P>Wenn eine Aktivität auf mehreren URLs ausgeführt wird, zeigt ein Link, wie viele weitere URLs verwendet werden. Klicken Sie auf den Link, um die vollständige Liste an URLs für diese Aktivität anzuzeigen.<P>Sie können anhand der URL suchen. Verwenden Sie die Dropdownliste neben dem Suchfeld und wählen Sie [!UICONTROL URL]. |
| Autor | Der Name der Person, die die Aktivität erstellt hat. |
| [!UICONTROL Entscheidungsmethode] | Die in den einzelnen Aktivitäten verwendete Entscheidungsmethode: [Serverseitig](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=de) oder [Client-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

## Aktivitätstypen  {#types}

[!DNL Target] umfasst mehrere Aktivitätstypen. In der folgenden Tabelle finden Sie einen Überblick über die einzelnen Aktivitätstypen mit Links, über die Sie mehr erfahren können. Damit Sie besser den Aktivitätstyp für Ihre Zwecke auswählen können, haben wir auch das [Adobe Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md) erstellt.

| Aktivitätstyp | Beschreibung |
|--- |--- |
| [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) | Beim A/B-Test werden zwei oder mehr Versionen Ihres Website-Inhalts verglichen, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert. |
| [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Automatische Zuordnung], ein Typ von A/B-Test, identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird. |
| [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | Beim automatischen Targeting, einer Art von A/B-Test, werden mehrere von Marketingexperten definierte Erlebnisse mit hoher Leistung über das erweiterte maschinelle Lernen identifiziert. Zudem erhalten alle Besucher basierend auf dem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen ein optimal auf sie zugeschnittenes Erlebnis, um Inhalte zu personalisieren und Konversionen zu fördern. |
| [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) vergleicht Kombinationen aus Angeboten in Elementen auf einer Seite, um festzustellen, welche Kombination die beste Leistung für eine bestimmte Zielgruppe erzielt, und identifiziert, welches Element den größten Einfluss auf den Erfolg der Aktivität hat. |
| [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) | Beim [!UICONTROL Experience Targeting] (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus Regeln und Kriterien, die von den Werbungtreibenden definiert werden, bereitgestellt. |
| [Automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besuchern basierend auf ihrem individuellen Kundenprofil mithilfe des erweiterten maschinellen Lernens verschiedene Varianten zu, um Inhalte zu personalisieren und Konversionen zu fördern. |
| [Recommendations](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | Eine Empfehlung bestimmt, wie ein Produkt einem Website-Besucher je nach den Aktivitäten dieses Besuchers auf der Site vorgeschlagen wird.<P>So können Sie zum Beispiel Personen, die einen Rucksack kaufen, dazu anregen, den Kauf von Wanderschuhen und -stöcken zu erwägen. Mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Algorithmus können Sie eine Empfehlung erstellen, die Artikel anzeigt, welche oft zusammen gekauft werden. Oder Sie möchten Besucher dazu anregen, mehr Zeit auf Ihrer Medienwebsite zu verbringen, indem Sie mit dem Algorithmus &quot;Personen, die das Video angesehen haben, haben auch dieses Video angesehen&quot;Videos empfehlen, die dem angesehenen Video ähneln.<P>**NOTE**: Sie können auch Empfehlungen in [!UICONTROL A/B-Test], [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting], und [!UICONTROL Erlebnis-Targeting] (XT). Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen. |

## Filter auf die Aktivitätenliste anwenden {#filters}

Zugriff auf Filter durch Klicken auf **[!UICONTROL Filter anzeigen]** -Symbol am oberen Rand der Liste.

![Filteroptionen](/help/main/c-activities/assets/show-filters-options.png)

Im Menü können Sie Aktivitäten nach folgenden Attributen filtern: |Attribut|Details| | — | — | |[!UICONTROL Typ]|Filtern nach [Aktivitätstyp](#types).| |[!UICONTROL Status]|Filtern nach Aktivitätsstatus.| |[!UICONTROL Berichtsquelle]|Filtern nach Berichtsquelle.<ul><li>[Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md): Zeigt Aktivitäten an, die [!UICONTROL Analytics for Target] (A4T) als Berichtsquelle verwenden.</li><li>[Target](/help/main/c-reports/reports.md): Zeigt Aktivitäten an, die [!DNL Target] als Berichtsquelle.</li></ul>| |[!UICONTROL Experience Composer]|Filtern, nach welchem Experience Composer bei der Aktivitätserstellung verwendet wurde:<ul><li>[Visuell](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): Zeigt Aktivitäten an, die mit der Variablen [!UICONTROL Visual Experience Composer] (VEC).</li><li>[Formularbasiert](/help/main/c-experiences/form-experience-composer.md): Zeigt Aktivitäten an, die mit der [!UICONTROL Form-Based Experience Composer].</li></ul>| |[!UICONTROL Metriktyp]|Filtern nach [Erfolgsmetrik](/help/main/c-activities/r-success-metrics/success-metrics.md) während der Erstellung der Aktivität ausgewählt wurde.<ul><li>Konversion</li><li>Umsatz</li><li>Interaktion</li></ul>| |[!UICONTROL Entscheidungsmethode]|Filtern nach der in den einzelnen Aktivitäten verwendeten Entscheidungsmethode<ul><li>[Serverseitig](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=de): Zeigt Aktivitäten an, die serverseitige Entscheidungen verwenden.</li><li>[Client-seitig](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): Zeigt Aktivitäten an, die clientseitige Entscheidungsfindung verwenden.</li></ul>| |[!UICONTROL Aktivitätsquelle]|Filtern Sie nach der Aktivitätsquelle, mit der die einzelnen Aktivitäten erstellt werden.<ul><li>[!DNL Adobe Target]</li><li>[Adobe Target-API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=de)</li><li>[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=de)</li><li>[Adobe Experience Manager ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html)</li><li>[Adobe Mobile-Dienste](https://developer.adobe.com/client-sdks/documentation/)</li></ul>| |[!UICONTROL Eigenschaft]|Filtern nach der [property](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) in dem die Aktivität erstellt wurde.|

## Schnellaktionen durchführen {#quick-actions}

Klicken Sie auf **[!UICONTROL Mehr Aktionen]** neben dem jeweiligen Aktivitätsnamen (die horizontalen Auslassungspunkte), um ein Menü zu öffnen, über das Sie Schnellaktionen für eine Aktivität durchführen können.

![Optionen für Schnellaktionen](/help/main/c-activities/assets/quick-actions.png)

Die folgenden Aktionen sind verfügbar (je nach Berechtigungen und Aktivitätsstatus):

| Aktion | Beschreibung |
| --- | --- |
| [!UICONTROL Bearbeiten ] | Aktivität ändern. Es kann jede Aktivität bearbeitet werden.<P>Weitere Informationen zu den verschiedenen Möglichkeiten, Aktivitäten zu bearbeiten, finden Sie unter [Bearbeiten einer Aktivität oder Speichern als Entwurf](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Deaktivieren] | Eine laufende oder geplante Änderung anhalten. Eine deaktivierte Aktivität kann reaktiviert oder archiviert werden.<P>Wenn Sie eine Aktivität deaktivieren oder archivieren und später erneut aktivieren, gehören die Besucher, die vor der Deaktivierung oder Archivierung Teil der Aktivität waren, nach der erneuten Aktivierung weiterhin zur Aktivität. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| [!UICONTROL Aktivieren] | Starten Sie eine inaktive Aktivität oder eine Aktivität, die zur Aktivierung bereit ist. |
| [!UICONTROL Archivieren] | Die Aktivitätenliste an das Archiv senden. Archivierte Aktivitäten werden standardmäßig nicht mehr im [!UICONTROL Tätigkeiten] Liste. Ändern Sie den Filter für die Aktivitätenliste, damit auch archivierte Aktivitäten angezeigt werden. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.<P>Wenn Sie eine Aktivität deaktivieren oder archivieren und später erneut aktivieren, gehören die Besucher, die vor der Deaktivierung oder Archivierung Teil der Aktivität waren, nach der erneuten Aktivierung weiterhin zur Aktivität. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| [!UICONTROL Kopieren] | Eine Aktivität kopieren. Jede Aktivität kann kopiert werden. Beim Kopieren einer Aktivität wird eine neue Aktivität mit dem gleichen Namen und dem Appendix „Copy“ erstellt. Beispielsweise wird ein Test mit der Bezeichnung „Browser Offers“ in „Browser Offers Copy“ umbenannt.<P>Visuelle Angebote werden mit der Aktivität kopiert. Sie können die Angebote in der Kopie sicher bearbeiten, ohne dass sich dies auf die ursprüngliche Aktivität auswirkt. Die einzige Ausnahme sind gespeicherte Angebote und Bilder im Inhalts-/Assets-Ordner. |
| [!UICONTROL Löschen] | Einen Entwurf oder eine Aktivität löschen.<P>**HINWEIS**: Gelöschte Aktivitäten können nicht wiederhergestellt werden. Wenn Sie sich nicht sicher sind, dass Sie diese Aktivität nicht erneut benötigen, verwenden Sie die [!UICONTROL Archivieren] Aktion. Danach können Sie die Aktivität bei Bedarf reaktivieren. |

## Zu beachten

Beachten Sie die folgenden Details zu den [!UICONTROL Aktivität] list:

* Archivierte und beendete Aktivitäten werden nicht in der [!UICONTROL Aktivitätenliste] aufgeführt. Um diese Aktivitäten anzuzeigen, filtern Sie sie mithilfe der [Filtersymbol](#filters) oben in der Liste.
* Wenn eine Aktivität ursprünglich in [!DNL Target Classic] deaktiviert oder gelöscht wird, wird sie aus [!DNL Target Standard/Premium]. Gelöschte Aktivitäten, die ursprünglich in [!DNL Target Classic] erstellt wurden, werden nicht an den Ordner [!UICONTROL Archiv] in [!DNL Target Standard/Premium] gesendet. Die Funktion für archivierte Ordner gilt nur für in [!DNL Target Standard/Premium] erstellte Aktivitäten.
* Bei allen anderen Aktivitätstypen als [!UICONTROL Automated Personalization] (AP), [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] haben Sie die Wahl zwischen [!DNL Target] und [!DNL Adobe Analytics] als Datenquelle. [!UICONTROL AP], [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] verwenden *immer* [!DNL Target]-Daten.
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
| Eindeutige Selektoren | 300 – Wenn ein Selektor in einem anderen Erlebnis wiederholt wird, wird er nur einmal gezählt. Wenn sie jedoch im selben Erlebnis wiederholt wird, wird sie erneut gezählt. |
| Angebote in jedem Erlebnis | 350 |
| Klick-Tracking-Selektoren in Metriken | 50 |
| Mboxes in Metriken | 50 |
| Zielgruppen und Orte | 50 Zielgruppen- und Standortkombinationen (Mbox) dürfen nicht mehr als 50 betragen. |

Die Aktivität kann nicht gespeichert werden, wenn Sie diese Beschränkungen überschreiten.

Durch die Erhöhung der Anzahl dieser Elemente in Ihrer Aktivität verlängert sich auch die Zeit, die zum Synchronisieren der Aktivität über [!DNL Target].

Für zusätzliche Grenzwerte des V[!UICONTROL Visual Experience Composer] VEC, siehe [Einschränkungen von Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## In importierte Attribute [!DNL Target] für Aktivitäten, die außerhalb von [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

Wenn Aktivitäten in [!DNL Target] werden von außerhalb von [!DNL Target] (z. B. über API) werden die folgenden Aktivitätsattribute nach [!DNL Target]: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority`, und `marketingCloudMetadata(remoteModifiedBy)`.

Dieser Importauftrag wird ausgeführt, wenn die Aktivitätsseite geöffnet wird, mit einer maximalen Verzögerung von zehn Minuten.

## Schulungsvideos {#section_BE80D13A2E81460C885F902010E1AD87}

Das folgende Video enthält weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätstypen (9:03)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

