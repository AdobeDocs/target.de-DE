---
keywords: automatisierte Personalisierung;App
description: Erfahren Sie, wie Sie mit der Aktivität [!UICONTROL Visual Experience Composer] eine Aktivität vom Typ [!UICONTROL Automated Personalization] (AP) erstellen.
title: Wie erstelle ich eine [!UICONTROL Automated Personalization] -Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
hide: true
hidefromtoc: true
exl-id: fe6e5130-53a0-4254-8299-b52086c20004
source-git-commit: 8bfad2fe6804c241deec6c8ea70e2f8e7d79d8c6
workflow-type: tm+mt
source-wordcount: '1767'
ht-degree: 28%

---

# Erstellen einer [!UICONTROL Automated Personalization] -Aktivität

Erstellen Sie mit dem VEC (2) eine Aktivität vom Typ [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target].[!UICONTROL Visual Experience Composer]

Der Aktivitäts-Workflow [!UICONTROL Automated Personalization] (AP) in [!DNL Target] unterscheidet sich vom Workflow der anderen Aktivitätstypen.

1. Klicken Sie in der Liste [!DNL Target] [!UICONTROL Activities] auf **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

1. Um den VEC (0) zu verwenden, klicken Sie auf **[!UICONTROL Visual]**.[!UICONTROL Visual Experience Composer]

   Um den [!UICONTROL Form-Based Experience Composer] zu verwenden, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] die [!UICONTROL Single Page Application VEC]. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung für VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) [Wählen Sie einen Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standard-URL zu einer anderen URL wechseln.

   [!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen sowohl [!DNL `http://www.adobe.com`] als auch [!DNL `https://wwww.adobe.com`] überein.

1. Klicken Sie auf **[!UICONTROL Create]**.

   Die Seite mit der angegebenen URL wird im VEC geöffnet.

1. Klicken Sie auf das Symbol **[!UICONTROL Rename]** ( ![Symbol &quot;Umbenennen&quot;](/help/main/assets/icons/MoreSmallListVert.svg) ), klicken Sie auf **[!UICONTROL Rename]**, geben Sie einen Namen für die Aktivität an und klicken Sie auf **[!UICONTROL Save]**.

   Der Aktivitätsname darf mit keinem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

   Der Aktivitätsname darf keine der folgenden Zeichensequenzen enthalten:

   | Zeichensequenz | Beschreibung |
   |--- |--- |
   | ;= | Semikolon, Gleich |
   | ;+ | Semikolon, Plus |
   | ;- | Semikolon, Minus |
   | ;@ | Semikolon, At-Zeichen |
   | ,= | Komma, gleich |
   | ,+ | Komma, Plus |
   | ,- | Komma, Minus |
   | ,@ | Komma, At-Zeichen |
   | `[`&quot; | Offene eckige Klammer, doppelte Anführungszeichen |
   | &quot;`]` | Doppelte Anführungszeichen, eckige Klammer schließen |

1. Die Seitenelemente können Sie wie im Abschnitt zu den [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) beschrieben ändern.

   Sie können aus dem Asset-Manager mehrere Bilder auf einmal auswählen. Auf diese Weise können Sie die Seite mit jedem der für die Aktivität konfigurierten Bilder schnell anzeigen. Sie können auch einfach Textelemente in Ihren Angeboten bearbeiten. Wenn Sie ein Element bearbeiten, werden Balken darauf eingeblendet, um darauf hinzuweisen, dass Sie Änderungen vorgenommen haben.

1. Klicken Sie auf **[!UICONTROL Manage Content]** , um die verfügbaren Kombinationen zu konfigurieren.

   ![Option „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Oben im Bildschirm wird ein Dialogfeld mit drei Optionen angezeigt: [!UICONTROL Experiences], [!UICONTROL Offers] und [!UICONTROL Exclusion Groups].

   ![Dialogfeld „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Obwohl Sie bis zu 30.000 Erlebnisse in einer AP-Aktivität erstellen können, funktionieren die Aktivitäten am besten, wenn weniger als 5.000 Erlebnisse verwendet werden. Dieselbe Beschränkung wird auch angewendet, wenn die Aktivität die [!UICONTROL Disalow Duplicates] -Option aktiviert hat.

   Die Liste [!UICONTROL Experiences] zeigt jedes für die Aktivität ausgewählte Inhaltselement und den Ort, dem sie zugewiesen ist.

   Sie können bestimmte Erlebnisse ausschließen, indem Sie den Mauszeiger über das gewünschte Erlebnis bewegen und dann auf das Symbol [!UICONTROL Exclude] klicken.

   ![Symbol zum Ausschließen](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   Sie können Erlebnisse in einem Batch-Vorgang ausschließen oder einschließen, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann oben rechts im Dialogfeld auf das Symbol [!UICONTROL Exclude] klicken.

   ![Optionen für den Batch-Vorgang zum Ausschließen](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   Sie können diese Listenansicht so filtern, dass nur ausgeschlossene oder nur eingeschlossene Aktivitäten angezeigt werden. Klicken Sie dazu auf die Dropdownliste [!UICONTROL Status] .

1. (Bedingt) Klicken Sie auf **[!UICONTROL Offers]** , um Inhaltselemente auszuwählen und sie Berichtsgruppen zuzuweisen oder nur bestimmten Besuchern zu erlauben, bestimmte Angebote mit Targeting anzuzeigen.

   Weitere Informationen zu Berichtsgruppen finden Sie unter [Berichtsgruppen für Angebote in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

1. (Bedingt) Klicken Sie auf **[!UICONTROL Exclusion Groups]** , um eine beliebige Kombination von Elementen auszuwählen, die Sie aus der Aktivität ausschließen möchten.

   ![Registerkarte mit Ausschlussgruppen im Dialogfeld „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Sie können zwar bis zu 30.000 Erlebnisse in einem AP-Test erstellen, der Algorithmus erzielt jedoch die beste Leistung, wenn weniger als 10.000 verschiedene Erlebnisse verwendet werden. Dieselbe Beschränkung wird auch angewendet, wenn die Aktivität die [!UICONTROL Disalow Duplicates] -Option aktiviert hat.

   Klicken Sie auf **Ausschlussgruppe erstellen**, sofern in Ihrer Aktivität nicht bereits Ausschlussgruppen vorhanden sind. Sie können filtern, um eine Liste zu erstellen, die nur die Kombinationen anzeigt, die Sie ausschließen möchten. Benennen Sie Ihre Ausschlussgruppe und klicken Sie dann auf **Speichern**.

   Bewegen Sie zum Bearbeiten einer vorhandenen Ausschlussgruppe den Mauszeiger über die Gruppe, die Sie bearbeiten möchten, und klicken Sie dann auf das Stiftsymbol.

1. Klicken Sie auf **[!UICONTROL Done]** , wenn Sie die Einrichtung des Inhalts Ihrer Aktivität abgeschlossen haben.

1. Der Schritt **Targeting** sieht vertraut aus, wenn Sie andere [!DNL Target] Aktivitätstypen verwendet haben. Hier können Sie eine Zielgruppe auswählen und den Prozentsatz der Besucher angeben, die das Kontrollerlebnis sehen, indem Sie auf die Dropdownliste **[!UICONTROL Custom Allocation]** klicken und dann auf **Weiter** klicken.

   In der Dropdownliste [!UICONTROL Custom Allocation] können Sie aus den folgenden Optionen auswählen:

   ![Dropdown-Liste für die Traffic-Zuordnung](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** Wenn Sie den Algorithmus testen möchten, verwenden Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit &quot;zufälligen Erlebnissen&quot;als Kontrolle empfohlen.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** Wenn Ihr Ziel darin besteht, eine &quot;Always on&quot;-Aktivität zu erstellen, sollten Sie 10 % der Besucher in den Kontrollbereich versetzen. Diese Option stellt sicher, dass genügend Daten vorhanden sind, damit die Algorithmen mit der Zeit weiterhin lernen können. Der Nachteil besteht darin, dass Sie im Austausch für die Personalisierung eines größeren Teils Ihres Traffics weniger präzise wissen, was genau die Steigerung ist. Unabhängig von Ihrem Ziel ist diese Option die empfohlene Traffic-Aufteilung bei der Verwendung eines bestimmten Erlebnisses als Kontrolle.
   * **[!UICONTROL Custom Allocation]:** Teilen Sie den Prozentsatz nach Wunsch manuell auf.

1. (Bedingt) Wählen Sie aus der Dropdownliste [!UICONTROL Control] ein spezifisches Erlebnis aus, das als Kontrolle verwendet werden soll ](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oder wählen Sie [!UICONTROL Random Experience.][

   Das Kontrollerlebnis liefert einen Vergleich, um zu ermitteln, welche Steigerung der automatisierte Test ermöglicht.

   [!UICONTROL Automated Personalization] misst die Leistung immer im Vergleich zu einer Kontrollgruppe. Es empfiehlt sich, mindestens 10 % der Teilnehmer in der Kontrollgruppe zu platzieren. Wenn Sie testen möchten, ob der Personalisierungsalgorithmus für die angegebenen Daten besser abschneidet als keine Personalisierung (z. B. die zufällig bereitgestellte Kontrolle), ist eine 50/50-Prozentaufteilung des Traffics zwischen Kontrolle und Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit, dieses Ziel zu erreichen. Wenn Sie die Menge des personalisierten Traffics maximieren möchten und weniger daran interessiert sind, die genaue Steigerung zu verstehen, die Ihre Aktivität generiert, ist eine Traffic-Aufspaltung von 10/90 Prozent zwischen dem Kontroll- und dem Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit, dieses Ziel zu erreichen.

   >[!NOTE]
   >
   >In [!UICONTROL Automated Personalization] -Aktivitäten werden Eingabekriterien (URL-Targeting, Vorlagenregeln und Zielgruppen-Targeting) für jede Anfrage ausgewertet. In älteren Versionen wurden Eingabekriterien nur einmal pro Sitzung bewertet.

1. Klicken Sie auf **[!UICONTROL Next]** , um die Seite **[!UICONTROL Goals & Settings]** anzuzeigen.
1. Konfigurieren Sie die Aktivität mit den folgenden Einstellungen und klicken Sie auf **[!UICONTROL Save & Close]**.

   | Einstellung | Beschreibung |
   |--- |--- |
   | [!UICONTROL Name] | Benennen Sie die Aktivität. Geben Sie der Aktivität einen beschreibenden Namen, damit Teammitglieder sie in der Liste [!UICONTROL Activities] erkennen können. In der oben stehenden Tabelle sehen Sie, welche Zeichen in einem Aktivitätsnamen nicht zulässig sind. |
   | [!UICONTROL Objective] | (Optional) Geben Sie das Ziel des Tests ein. Das Ziel hilft Ihnen, den Zweck der Aktivität zu verinnerlichen. |
   | [!UICONTROL Priority] | Abhängig von Ihren Einstellungen variieren die [!DNL Target]-Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die veralteten Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder genauer unterteilte Prioritäten von 0 bis 999 aktivieren.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option unter [!UICONTROL Administration] > [!UICONTROL Reporting] (Standardeinstellung) nicht aktiviert ist, geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High].<P>Um genauer unterteilte Prioritäten zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und stellen Sie dann die Option [!UICONTROL Enable Fine-Grained Priorities] auf die Position &quot;Ein&quot;.<P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:<ul><li>0 = Niedrig</li><li>999 = Hoch</li></ul>Bei Aktivitäten, die in früheren Versionen von [!DNL Target Standard/Premium] erstellt wurden, wird die Priorität [!UICONTROL Low] in 0, die Priorität [!UICONTROL Medium] in 5 und die Priorität [!UICONTROL High] in 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.<P>**Hinweis**: Bevor Sie diese Option deaktivieren können, nachdem Sie genauere Prioritäten verwendet haben, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden. |
   | [!UICONTROL Duration] | Legen Sie das Start- und Enddatum für die Aktivität fest. Sie können &quot;[!UICONTROL When Activated]&quot;auswählen oder ein bestimmtes Datum und eine bestimmte Uhrzeit angeben. |
   | [!UICONTROL Optimization Goal] | Geben Sie das Optimierungsziel an, das aus zwei Parametern besteht:<ul><li>dem, was Sie mit der Aktivität messen möchten,</li><li>der von einem Aktivitätsteilnehmer durchgeführten Aktion, die zeigt, dass das Ziel erreicht wurde</li></ul>Sie können das Optimierungsziel benennen, indem Sie die drei Punkte rechts von [!UICONTROL My Primary Goal] auswählen. [!UICONTROL Automated Personalization] -Aktivitäten können [!UICONTROL Conversion] oder [!UICONTROL Revenue] messen. Die Konversion kann durch Anzeigen einer Seite oder einer Mbox erreicht werden. Es können auch Klicks verfolgt werden.<P>Das primäre Ziel wird außerdem zur Modellierungsmetrik, die vom Modellierungssystem verwendet wird, um den Erfolg des Erlebnisses zu berechnen.<P>Besucher können zu Tracking-Zwecken in der Aktivität beibehalten werden, nachdem Sie das Modellierungsziel erreicht haben. Beispielsweise wird häufig eine [!UICONTROL Automated Personalization] -Aktivität verwendet, um die Klickraten zu verbessern, und dies wird als Modellierungsziel festgelegt. Es ist jedoch wichtig zu sehen, wie erhöhte Klickraten zur finalen Konversion führen; daher ist ein Tracking durch die finale Konversion entscheidend.<P>Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.<P>Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.<P>Mit der Option [!UICONTROL Add Dependency] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.<P>So fügen Sie eine Abhängigkeit hinzu:<ol><li>Klicken Sie nach dem Hinzufügen zusätzlicher Metriken unter dem Menü mit den drei Punkten rechts von [!UICONTROL Additional Goal] auf **[!UICONTROL Advanced Settings]** .</li><li>Klicken Sie unten im Abschnitt [!UICONTROL Reporting Settings] auf die Option **[!UICONTROL Add Dependency]** .</li><li>Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf [!UICONTROL Reached] , um die Einstellung zwischen [!UICONTROL Reached] und [!UICONTROL Not Reached] umzuschalten.</li></ol>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben. |
   | [!UICONTROL Conversion Metric] | Standardmäßig entspricht die Konversionsmetrik der Optimierungszielmetrik. Sie können jedoch eine separate Konversionsmetrik definieren, indem Sie die Option [!UICONTROL Same as Optimization Goal] deaktivieren. |
   | [!UICONTROL Additional Metrics] | Fügen Sie zusätzliche Berichtsmetriken hinzu, die Sie verwenden möchten. Sie können Konversions- oder Umsatzmetriken hinzufügen.<P>**Hinweis**: Die Metrik [!UICONTROL Engagement] wird nicht als zusätzliche Metrik unterstützt. In der Benutzeroberfläche von [!DNL Target] können Sie zwar die Metrik [!UICONTROL Engagement] auswählen, die Daten werden jedoch nicht korrekt in Berichten angezeigt. |
   | [!UICONTROL Audiences for Reporting] | Fügen Sie Zielgruppen hinzu, um die Filterung nach Zielgruppen in Berichten zu ermöglichen. Standardmäßig zeigen die Berichte Ergebnisse für alle berechtigten Besucher. Fügen Sie Zielgruppen hinzu, um Ergebnisse nach spezifischeren Besucheruntergruppen zu filtern.<P>**Hinweis**: Im Gegensatz zu anderen Aktivitätstypen kann [!UICONTROL Automated Personalization] [!UICONTROL Adobe Analytics] nicht als Berichtsquelle (A4T) verwenden. |
   | [!UICONTROL Notes] | Geben Sie alle Informationen über Ihre Aktivität ein, die für Sie oder andere Teammitglieder nützlich sind. Die Größe des Bereichs [!UICONTROL Notes] kann geändert werden. |

   Wenn Sie eine Metrik benennen oder umbenennen, sind folgende Zeichen nicht zulässig:

   | Zeichen | Beschreibung |
   |--- |--- |
   | / | Vorwärtsschrägstrich |
   | ? | Fragezeichen |
   | # | Raute |
   | : | Doppelpunkt |
   | = | Gleich |
   | + | Plus |
   | - | Minus |
   | @ | At-Zeichen |

Nachdem Sie auf **[!UICONTROL Save & Close]** geklickt haben, wird die Seite [!UICONTROL Overview] der Aktivität angezeigt. Klicken Sie auf **Erlebnisvorschau anzeigen** , um eine Vorschau des Erscheinungsbilds Ihrer Erlebnisse bei Bereitstellung anzuzeigen. Es wird ein Popup angezeigt, über das Sie Links zu Ihren AP-Erlebnissen auf Ihrer Site anzeigen und freigeben können, um eine &quot;echte Vorschau&quot;der Erlebnisse außerhalb von [!UICONTROL Target] [!UICONTROL Visual Experience Composer] (VEC) zu erhalten. Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Klicken auf einen Link und das anschließende Kopieren der URL direkt aus dem Browser funktionieren nicht. Durch das Kopieren des Links enthält die URL einen Parameter, der die Seite nur dann richtig anzeigt, wenn Sie über den Link in der Nachricht auf die Seite zugreifen.

Weitere Informationen zur Berichterstellung finden Sie unter [Automatisierte Personalisierungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).
