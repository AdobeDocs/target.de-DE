---
description: Mit Aktivitäten können Sie Seitenentwürfe testen und Inhalt auf bestimmte Zielgruppen ausrichten.
keywords: Aktivitätenliste;Aktivitäten;Aktivität;Aktivitätstypen;Aktivität bearbeiten;Aktivitätsaktionen;Aktivitätsattribut;Aktivitätslistenfilter;Aktivitätsbeschränkungen
seo-description: Mit den Aktivitäten in Adobe Target können Sie Seitenentwürfe testen und Inhalte auf bestimmte Zielgruppen ausrichten.
seo-title: Aktivitäten in Adobe Target
solution: Target
title: Aktivitäten
topic: Standard
uuid: 89dca5b4-c23d-4dfa-8f13-f1b05c7ab22c
translation-type: tm+mt
source-git-commit: b45a1a141e9e1d229ed3f92b8124d3edf3bc3042

---


# Aktivitäten{#activities}

Mit Aktivitäten können Sie Seitenentwürfe testen und Inhalt auf bestimmte Zielgruppen ausrichten. Eine Aktivität legt die Erlebnisse fest, auf die ein Site-Besucher stoßen kann.

Sie können z. B. eine Aktivität entwerfen, die zwei verschiedene Einstiegsseiten testet, eine, die Informationen zu Sommerschuhen für Damen hervorhebt und eine weitere Landingpage, die allgemeinere Sommerbekleidung hervorhebt. Durch die Aktivität werden die Bedingungen festgelegt, die steuern, wann diese beiden Landingpages angezeigt werden, sowie die Metriken, die bestimmen, welche Seite erfolgreicher ist. Die Aktivität wird so konfiguriert, dass sie bei Zutreffen bestimmter Bedingungen beginnt und endet (z. B. zwischen bestimmten Terminen) oder dass sie beginnt, wenn die Aktivität genehmigt wird, und endet, wenn sie deaktiviert wird.

Sie sollten den Entwurf einer Aktivität sorgfältig planen. Legen Sie fest, wann die Aktivität starten und wie lange sie dauern soll. Führen Sie dann Ihre Angebote auf, und weisen Sie jedem dieser Angebote eine Zielgruppe zu.

## Aktivitätstypen

Target enthält mehrere Aktivitätstypen. In der folgenden Tabelle finden Sie einen Überblick über die einzelnen Aktivitätstypen mit Links, mit denen Sie mehr erfahren können. Damit Sie besser den Aktivitätstyp für Ihre Zwecke auswählen können, haben wir auch das [Adobe Target-Aktivitätshandbuch erstellt](/help/c-activities/target-activities-guide.md).

| Aktivitätstyp | Beschreibung |
|--- |--- |
| [A/B-Test](/help/c-activities/t-test-ab/test-ab.md) | Beim A/B-Test werden zwei oder mehr Versionen Ihrer Website-Inhalte verglichen, um festzustellen, mit welcher Version Ihre Konversionen in einem vorab festgelegten Zeitraum verbessert werden.<br>**Hinweis:** Sie können [nun Empfehlungen in A/B-Test-Aktivitäten einfügen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/c-intro/intro.md#premium)verfügen. |
| [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Die Funktion „Automatisch zuweisen“ identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.<br>**Hinweis:** Sie können [jetzt Empfehlungen in Aktivitäten mit automatisierter Zuordnung einfügen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine Funktion für diese Funktion verfügen müssen, dass Sie über eine [Target Premium-Lizenz verfügen](/help/c-intro/intro.md#premium). |
| [Auto-targettarget](/help/c-activities/auto-target-to-optimize.md)<br>![Premium](/help/assets/premium.png) | Beim automatischen Targeting werden mehrere vermarkterdefinierte Erlebnisse mit hoher Leistung über das erweiterte maschinelle Lernen identifiziert. Zudem erhalten alle Besucher basierend auf ihrem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen ein optimal auf sie zugeschnittenes Erlebnis, um die Inhalte zu personalisieren und Konversionen zu fördern.<br>**Hinweis:** Sie können [nun Empfehlungen in Aktivitäten mit automatischem Targeting einfügen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine Funktion für diese Funktion verfügen müssen, dass Sie über eine [Target Premium-Lizenz verfügen](/help/c-intro/intro.md#premium). |
| [Verwenden von Analytics-Daten](/help/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) (A 4 T) | Sie können eine Aktivität so konfigurieren, dass [!DNL Adobe Analytics] als Berichtsquelle verwendet wird. Für diesen Aktivitätstyp ist es erforderlich, dass Sie Ihr [!DNL Adobe Experience Cloud]-Konto sowohl mit [!DNL Analytics] als auch mit [!DNL Target] verbinden. |
| [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Beim Multivarianz-Test (MVT) werden Kombinationen aus Angeboten in Elementen auf einer Seite verglichen, um zu bestimmen, welche Kombination die beste Leistung für eine bestimmte Zielgruppe erzielt. Zudem gibt er an, welches Element den größten Einfluss auf den Erfolg der Aktivität hat. |
| [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md) | Beim Erlebnis-Targeting (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus vermarkterdefinierten Regeln und Kriterien bereitgestellt.<br>**Hinweis:** Sie können [nun Empfehlungen in Erlebnis-Targeting-Aktivitäten einbeziehen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/c-intro/intro.md#premium)verfügen. |
| [Automatisierte personalisierungtarget](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>![Premium](/help/assets/premium.png) | Die automatisierte Personalisierung (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besuchern basierend auf deren individuellem Kundenprofil mithilfe des erweiterten maschinellen Lernens verschiedene Variationen zu, um die Inhalte zu personalisieren und Konversionen zu fördern. |
| [Recommendationstarget](/help/c-recommendations/recommendations.md)<br>![Premium](/help/assets/premium.png) | Eine Empfehlung bestimmt, wie ein Produkt dem Website-Benutzer je nach dessen Aktivitäten auf der Site vorgeschlagen werden soll.<br>So können Sie zum Beispiel Personen, die einen Rucksack kaufen, dazu anregen, den Kauf von Wanderschuhen und -stöcken zu erwägen. Mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Algorithmus können Sie eine Empfehlung erstellen, die Artikel anzeigt, welche oft zusammen gekauft werden. Oder Sie können Besucher dazu anregen, mehr Zeit auf Ihrer Medienwebsite zu verbringen, indem Sie mithilfe des „Personen, die dieses Video angesehen haben, sahen auch“-Algorithmus Videos empfehlen, die dem angezeigten Video ähneln.<br>**Hinweis:** Sie können jetzt Empfehlungen in A/B-Tests (einschließlich automatisierter Zuordnung und automatisches Targeting) und Erlebnis-Targeting (XT) einbeziehen. Siehe [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md). |

## Aktivitätenliste {#section_DE8E2DB30D534962A931EF8BB48240F5}

Die [!UICONTROL Aktivitätenliste] ist die Standardansicht beim Öffnen [!DNL Target]. Sie können auf dieser Seite neue Aktivitäten erstellen und vorhandene Aktivitäten verwalten.

Sie können die [!UICONTROL Aktivitätenliste] auch anzeigen, indem Sie oben in der Benutzeroberfläche auf die Registerkarte [!UICONTROL Aktivitäten] [!DNL Target] klicken.

![Aktivitätenliste](/help/c-activities/assets/activities-list.png)

Die Aktivitätenliste bietet eine Übersicht über alle Aktivitäten:

| Element | Beschreibung |
|--- |--- |
| Typ | Den Aktivitätstyp, etwa „A/B“ oder „MVT“ |
| Name | Der Name der Aktivität. |
| URL | Die URL erscheint in hellerem Text unter dem Namen.<br>Die URL für die Aktivität identifiziert, wo die Aktivität angezeigt wird. Auf diese Weise können Sie innerhalb kürzester Zeit eine Aktivität definieren und bestimmen, ob auf einer bestimmten Seite bereits ein Test ausgeführt wird.<br>Wird ein Test für mehrere URLs ausgeführt, zeigt ein Link, wie viele weitere URLs verwendet werden. Klicken Sie auf den Link, um die vollständige Liste an URLs für diese Aktivität anzuzeigen.<br>Sie können anhand der URL suchen. Verwenden Sie die Dropdownliste neben dem Suchfeld und wählen Sie [!UICONTROL URL suchen]. |
| Status | Der Status der Aktivität kann wie folgt lauten:<ul><li>**Live**: Die Aktivität wird derzeit ausgeführt.</li><li>**Entwurf:** Die Einrichtung der Aktivität hat begonnen, sie kann jedoch noch nicht ausgeführt werden.</li><li>**Geplant:** Die Aktivität wird zum festgelegten Startdatum und zur festgelegten Startzeit aktiviert.</li><li>**Inaktiv:** Die Aktivität wurde angehalten oder deaktiviert.</li><li>**Synchronisierung:** Die Aktivität wurde gespeichert und wird mit dem Target-Bereitstellungsnetzwerk synchronisiert.</li><li>**Beendet:** Das angegebene Enddatum und die angegebene Uhrzeit der Aktivität wurden erreicht und die Aktivität wird nicht mehr bedient.</li><li>**Archiviert:** Die Aktivität wurde archiviert. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.</li></ul>**Hinweis:** Wenn Sie bestimmte Aktionen ausführen (z. B. eine Aktivität außerhalb der Benutzeroberfläche über API-Methoden aktivieren), kann es bis zu 10 Minuten dauern, bis die Aktualisierung bis zur Benutzeroberfläche propagiert wird. |
| Quelle | Zeigt, wo die Aktivität erstellt wurde:<ul><li>Adobe Target</li><li>Adobe Target Classic</li><li>Adobe Experience Manager  (AEM)</li><li>Adobe Mobile Services (AMS)</li></ul> |
| Eigenschaft | Zeigt die [Eigenschaft](/help/administrating-target/c-user-management/property-channel/property-channel.md) für die Aktivität an. |
| Geschätzte Umsatzsteigerung | Zeigt die voraussichtliche Umsatzsteigerung an, wenn 100 % der Zielgruppe das erfolgreichste Erlebnis sehen.<br>Wird anhand der folgenden Formel berechnet:<br>`(<winning experience> - <control experience>)*<total number of visitors>`<br>Das Ergebnis wird auf maximal eine Dezimalstelle gerundet, wenn die gekürzte Form vor der Dezimalstelle nur eine Ziffer enthält. Beispiele: 1,6 Mio. $, 60 K $, 900 $, 8,5 K $, 205 K $<br>Diese Spalte zeigt „---“ für Aktivitäten, die nicht genügend Daten haben, um einen Gewinner festzustellen, oder keine Kostenschätzung haben.<br>Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md). |
| Zuletzt aktualisiert | Das Datum der letzten Aktualisierung und der Name der Person, die sie durchgeführt hat. |

Bewegen Sie den Mauszeiger über eine Aktivität, um die verfügbaren Aktionen anzuzeigen.

![Aktivitätenliste - Hover-Aktionen](/help/c-activities/assets/activities_list_hover.png)

Die folgenden Aktionen sind verfügbar (je nach Ihren Berechtigungen):

| Aktion | Beschreibung |
| --- | --- |
| Bearbeiten | Aktivität ändern. Es kann jede Aktivität bearbeitet werden.<br>Weitere Informationen zu den verschiedenen Möglichkeiten, Aktivitäten zu bearbeiten, finden Sie unter [Bearbeiten einer Aktivität oder Speichern als Entwurf](/help/c-activities/edit-activity.md). |
| Deaktivieren | Eine laufende oder geplante Änderung anhalten. Eine deaktivierte Kampagne kann reaktiviert oder archiviert werden.<br>Wenn Sie eine Aktivität deaktivieren oder archivieren und später erneut aktivieren, gehören die Besucher, die vor der Deaktivierung oder Archivierung Teil der Aktivität waren, nach der erneuten Aktivierung weiterhin zur Aktivität. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| Aktivieren | Eine inaktive oder bereite Aktion starten. |
| Archivieren | Die Aktivitätenliste an das Archiv senden. Archivierte Aktivitäten werden standardmäßig nicht mehr in der Aktivitätenliste aufgeführt. Ändern Sie den Filter für die Aktivitätenliste, damit auch archivierte Aktivitäten angezeigt werden. Sie können eine archivierte Aktivität wieder aktivieren, um sie erneut zu verwenden.<br>Wenn Sie eine Aktivität deaktivieren oder archivieren und später erneut aktivieren, gehören die Besucher, die vor der Deaktivierung oder Archivierung Teil der Aktivität waren, nach der erneuten Aktivierung weiterhin zur Aktivität. Alle zwischen den beiden Ereignissen aufgezeichneten Konversionsmetriken werden nicht auf die Aktivität angerechnet. |
| Kopieren   | Eine Aktivität kopieren. Jede Aktivität kann kopiert werden. Beim Kopieren einer Aktivität wird eine neue Aktivität mit dem gleichen Namen und dem Appendix „Copy“ erstellt. Beispielsweise wird ein Test mit der Bezeichnung „Browser Offers“ in „Browser Offers Copy“ umbenannt.<br>Visuelle Angebote werden mit der Aktivität kopiert. Sie können die Angebote in der Kopie sicher bearbeiten, ohne dass sich dies auf die ursprüngliche Aktivität auswirkt. Die einzige Ausnahme sind gespeicherte Angebote und Bilder im Inhalts-/Assets-Ordner. |
| Löschen | Einen Entwurf oder eine bereite Aktivität löschen. Gelöschte Aktivitäten können nicht wiederhergestellt werden. |

Beachten Sie folgende Details zur Aktivitätenliste:

* Archivierte und beendete Aktivitäten werden nicht in der [!UICONTROL Aktivitätenliste] aufgeführt. Um diese Aktivitäten anzuzeigen, filtern Sie sie mithilfe der erweiterten Filtereinstellungen in der linken Leiste.
* Sobald eine ursprünglich in [!DNL Target Classic] erstellte Aktivität deaktiviert oder gelöscht wird, wird sie aus [!DNL Target Standard/Premium] gelöscht. Gelöschte Aktivitäten, die ursprünglich in [!DNL Target Classic] erstellt wurden, werden nicht an den Ordner [!UICONTROL Archiv] in [!DNL Target Standard/Premium] gesendet. Die Funktion für archivierte Ordner gilt nur für in [!DNL Target Standard/Premium] erstellte Aktivitäten.
* Bei allen anderen Aktivitätstypen als [!UICONTROL Automated Personalization] (AP), [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] haben Sie die Wahl zwischen [!DNL Target] und [!DNL Adobe Analytics] als Datenquelle. [!UICONTROL AP], [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] verwenden *immer* [!DNL Target]-Daten.
* Für mehrere Kanäle verfügbare Aktivitäten:

   * Web- und Mobilseiten
   * Mit dem Internet verbundene Bildschirme und Geräte, einschließlich Telefonzellen und Geldautomaten
   * E-Mail und andere Akquisekanäle oder Partnersites
   * Mobile Anwendungen
   * Weitere Möglichkeiten zur Bereitstellung getaggter Inhalte

## Sortieren und Filtern der Aktivitätenliste {#section_41DAD479FFF740E2BB67BF4825955670}

Standardmäßig wird die Liste nach dem Datum der letzten Änderung der Aktivität sortiert, vom neuesten Datum absteigend. Es gibt jedoch mehrere Filteroptionen, mit deren Hilfe Sie die Liste anpassen können, sodass die von Ihnen gewünschten Aktivitäten angezeigt werden.

### Suche {#search-heading}

Verwenden Sie das Suchfeld, um nach Aktivitäten zu suchen, die auf Ihre Suchkriterien zutreffen.

![Aktivitätssuche](/help/c-activities/assets/activities_search_new.png)

Das Suchfeld enthält ein Dropdownmenü, mit dessen Hilfe Sie Ihre Suche durch Festlegen eines der folgenden Suchfilter eingrenzen können:   [!UICONTROL Aktivitätsname] und [!UICONTROL URL].

### Aktivitätslistenfilter

Sie können bestimmen, welche Aktivitäten in Ihrer Aktivitätenliste angezeigt werden, indem Sie Listenfilter auswählen.

![Aktivitäten nach Typ filtern](/help/c-activities/assets/activities_filters_new.png)

Sie können nach den folgenden Optionen filtern. Wenn in einzelnen Kategorien nichts ausgewählt wird, wird standardmäßig die Einstellung „Alle“ verwendet.

| Filterkategorie | Filter |
|--- |--- |
| Typ | A/B-Test: [Manuelle](/help/c-activities/t-test-ab/test-ab.md)Zuordnung, [automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)und [automatisches Targeting](/help/c-activities/auto-target-to-optimize.md).<br>[Automated personalizationexperience](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>[targetingmultivariate](/help/c-activities/t-experience-target/experience-target.md)<br>[testrecommendations](/help/c-activities/c-multivariate-testing/multivariate-testing.md)<br>[](/help/c-recommendations/recommendations.md) |
| Status | Live<br>Entwurf<br>Geplant<br>Inaktiv<br>Synchronisierung<br>Beendet<br>Archiviert |
| Berichtsquelle | Targetanalytics<br> |
| Experience Composer | Visuell<br>Formularbasiert |
| Metriktyp | Konversion<br>Umsatz<br>Interaktion |
| Aktivitätsquelle | Adobe Target<br>Adobe Target Classic<br>Adobe Experience Manager<br>Adobe Mobile Services |

### Nach Aktivitätsattribut sortieren

Klicken Sie auf eine der folgenden Überschriften, um auszuwählen, ob die Aktivitäten für die ausgewählte Überschrift in auf- oder absteigender Reihenfolge angezeigt werden sollen.

* Aktivitätsname
* Aktivitätstyp

![Aktivitätenliste aufsteigend](/help/c-activities/assets/activities_list_ascending.png)

## Tipps und Tricks {#section_F77F30A246A14B538D9363B7F3639F97}

Nutzen Sie Adobe Target optimal, indem Sie mehr über verschiedene Funktionen und darüber, warum Sie sie ausprobieren sollten, erfahren. In den Tipps und Tricks finden Sie Links zu Videos, Anwendungsbeispielen, Blogs, Dokumentation und vieles mehr.

Die Funktion „Tipps und Tricks“ wird regelmäßig auf der Seite der Aktivitätenliste angezeigt. Nachdem Sie einen Tipp gelesen oder geschlossen haben, wird die Funktion nicht mehr angezeigt, bis der nächste Tipp verfügbar ist. Sie können optional die Anzeige aller Tipps deaktivieren, indem Sie auf das Hilfesymbol und anschließend auf [!UICONTROL „Tipp des Tages deaktivieren“] klicken.

![Tipp des Tages deaktivieren](/help/c-activities/assets/tip-disable-new.png)

## Einschränkungen {#section_049D4684403A4E07B998067EB8E9BE56}

Für jede Target-Aktivität gelten die folgenden Inhaltsbeschränkungen:

| Element | Grenze |
|--- |--- |
| Eindeutige Selektoren | 300 – Wenn ein Selektor in einem anderen Erlebnis wiederholt wird, wird er nur einmal gezählt. Wenn sie jedoch im selben Erlebnis wiederholt wird, wird sie erneut gezählt. |
| Angebote in jedem Erlebnis | 350 |
| Klick-Tracking-Selektoren in Metriken | 50 |
| Mboxes in Metriken | 50 |
| Zielgruppen und Orte | 50 – Die Kombination von Zielgruppen und Standorten (Mbox) sollte nicht über 50 liegen. |

Die Aktivität kann nicht gespeichert werden, wenn Sie diese Beschränkungen überschreiten.

Die Erhöhung der Anzahl dieser Elemente in Ihrer Aktivität verlängert auch die Zeit, die für das Synchronisieren der Aktivität in Target benötigt wird.

Weitere Beschränkungen des Visual Experience Composer finden Sie unter [Beschränkungen des Visual Experience Composer](../c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## In Target importierte Attribute für Aktivitäten, die außerhalb von Target aktualisiert wurden {#section_802B0D174E6A44E1A96F404CA81AAE44}

Wenn in [!DNL Target] erstellte Aktivitäten außerhalb von [!DNL Target] aktualisiert werden (z. B. via Adobe I/O), werden die folgenden Aktivitätsattribute nach [!DNL Target] zurückimportiert:

`thirdpartyId`

`startDate`

`endDate`

`status`

`priority`

`marketingCloudMetadata(remoteModifiedBy)`

Dieser Import wird ausgeführt, wenn die Aktivitätenseite geöffnet wird. Die maximale Verzögerung beträgt dabei zehn Minuten. (KB-1526)

## Schulungsvideos {#section_BE80D13A2E81460C885F902010E1AD87}

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätstypen (9:03)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Verwalten von Aktivitäten (5:55)

In diesem Video wird erläutert, wie die Aktivitätenliste zur Verwaltung von Aktivitäten eingesetzt werden kann.

* Definieren des Begriffs *Aktivität*
* Auffinden von Aktivitäten in der Aktivitätenliste
* Bearbeiten, Deaktivieren und Löschen von Aktivitäten

>[!VIDEO](https://video.tv.adobe.com/v/18550)
