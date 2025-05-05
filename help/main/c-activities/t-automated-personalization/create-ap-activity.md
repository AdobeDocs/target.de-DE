---
keywords: Automated Personalization;App
description: Erfahren Sie, wie Sie eine [!UICONTROL Automated Personalization] (AP)-Aktivität mit dem [!UICONTROL Visual Experience Composer] erstellen.
title: Wie erstelle ich eine [!UICONTROL Automated Personalization] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '1844'
ht-degree: 24%

---

# [!UICONTROL Automated Personalization] erstellen

Erstellen Sie eine [!UICONTROL Automated Personalization] (AP)-Aktivität in [!DNL Adobe Target] mithilfe des [!UICONTROL Visual Experience Composer] (VEC).

Der Workflow für die [!UICONTROL Automated Personalization] (AP)-Aktivität in [!DNL Target] unterscheidet sich vom Workflow der anderen Aktivitätstypen.

1. Klicken Sie in der Liste [!DNL Target] [!UICONTROL Activities] auf **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

1. Um den [!UICONTROL Visual Experience Composer] (VEC) zu verwenden, klicken Sie auf **[!UICONTROL Visual]**.

   Um die [!UICONTROL Form-Based Experience Composer] zu verwenden, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] die [!UICONTROL Single Page Application VEC]. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung bei VEC finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) [Wählen Sie einen Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standardeinstellung zu einer anderen URL wechseln.

   [!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://wwww.adobe.com`] überein.

1. Klicken Sie auf **[!UICONTROL Create]**.

   Die Seite mit der angegebenen URL wird in VEC geöffnet.

1. Klicken Sie auf das **[!UICONTROL Rename]** ( ![Umbenennungssymbol](/help/main/assets/icons/MoreSmallListVert.svg) ), klicken Sie auf **[!UICONTROL Rename]**, geben Sie einen Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Save]**.

   Der Aktivitätsname darf nicht mit einem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

   Der Aktivitätsname darf keine der folgenden Zeichenfolgen enthalten:

   | Zeichenfolge | Beschreibung |
   |--- |--- |
   | ;= | Semikolon, Gleich |
   | ;+ | Semikolon plus |
   | ;- | Semikolon, Minus |
   | ;@ | Semikolon, at-Zeichen |
   | ,= | Komma, gleich |
   | ,+ | Komma, plus |
   | ,- | Komma, Minus |
   | ,@ | Komma, at-Zeichen |
   | `[`&quot; | Offene eckige Klammer, doppelte Anführungszeichen |
   | &quot;`]` | Doppelte Anführungszeichen, eckige Klammer schließen |

1. Die Seitenelemente können Sie wie im Abschnitt zu den [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) beschrieben ändern.

   Sie können aus dem Asset-Manager mehrere Bilder auf einmal auswählen. Auf diese Weise können Sie die Seite mit jedem für die Aktivität konfigurierten Bild schnell anzeigen. Sie können auch einfach Textelemente in Ihren Angeboten bearbeiten. Wenn Sie ein Element bearbeiten, werden Balken darauf eingeblendet, um darauf hinzuweisen, dass Sie Änderungen vorgenommen haben.

1. Klicken Sie auf das **[!UICONTROL Manage Content]** ( ![Symbol „Inhalt verwalten](/help/main/assets/icons/Experience.svg) ), um die verfügbaren Kombinationen zu konfigurieren.

   Oben im Bildschirm wird ein Dialogfeld mit zwei Optionen angezeigt: [!UICONTROL Experiences] und [!UICONTROL Offers].

   >[!NOTE]
   >
   >Sie können in einer AP-Aktivität zwar bis zu 30.000 Erlebnisse erstellen, die Aktivität funktioniert jedoch am besten, wenn weniger als 5.000 Erlebnisse verwendet werden. Diese Beschränkung gilt selbst dann, wenn bei der Aktivität die Option [!UICONTROL Disalow Duplicates] aktiviert ist.

   In der [!UICONTROL Experiences] Liste werden alle für die Aktivität ausgewählten Inhaltselemente und der ihnen zugewiesene Speicherort angezeigt.

   Sie können bestimmte Erlebnisse ausschließen, indem Sie das Kontrollkästchen neben dem gewünschten Erlebnis aktivieren und dann auf das Symbol [!UICONTROL Exclude] klicken.

   Sie können Erlebnisse im Batch aus- oder einschließen , indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann auf das Symbol [!UICONTROL Exclude] klicken.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Offers]** , um Inhaltselemente auszuwählen und sie Berichtsgruppen zuzuweisen oder nur bestimmten Besuchern zu ermöglichen, bestimmte Angebote beim Targeting zu sehen.

   Weitere Informationen zu Berichtsgruppen finden Sie unter [Berichtsgruppen in Automated Personalization ](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

<!--
1. (Conditional) Click **[!UICONTROL Exclusion Groups]** to choose any combination of elements that you want to exclude from the activity.

   ![Exclusion Groups tab of Manage Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the [!UICONTROL Disalow Duplicates] option.

   If you do not currently have any exclusion groups included in your activity, click **Create Exclusion Group**. You can filter to create a list that shows only the combinations you want to exclude. Name your exclusion group, then click **Save**.

   To edit an existing exclusion group, hover over the group you want to edit, then click the pencil icon.-->

1. Klicken Sie auf **[!UICONTROL Done]** , wenn Sie die Einrichtung des Inhalts Ihrer Aktivität abgeschlossen haben.

1. Klicken Sie oben in der [!UICONTROL Visual Experience Composer] auf **[!UICONTROL Targeting]** , um mit dem nächsten Schritt im Drei-Schritte-Workflow fortzufahren.

   Der **Targeting**-Schritt kommt Ihnen bekannt vor, wenn Sie andere [!DNL Target] Aktivitätstypen verwendet haben. Hier können Sie eine Zielgruppe auswählen und den Prozentsatz der Besucher angeben, die die einzelnen Erlebnisse sehen.

   Das Flussdiagramm wird geöffnet.

   ![AP-Test-Targeting-Schritt](/help/main/c-activities/t-automated-personalization/assets/ap-traffic-flow.png)

   Das Flussdiagramm führt Sie durch die Schritte Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, Auswählen der Traffic-Zuordnungsmethode und Festlegen der Traffic-Zuordnung für jedes Erlebnis in der Aktivität.

1. (Bedingt) Klicken Sie auf das **[!UICONTROL All Visitors]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die [!UICONTROL All Visitors] Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Daraufhin wird der rechte Rahmen angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Prozentsatz der Besuchenden für die Aktivität zuweisen können.

   1. Um die Audience zu ändern, klicken Sie auf das **[!UICONTROL Replace]-** ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) im rechten Rahmen.
   1. Wählen Sie im Dialogfeld [!UICONTROL Add Audience] die [ Audience aus ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) klicken Sie dann auf **[!UICONTROL Assign Audience]**.

      Sie können auf **Kombinieren von Zielgruppen** klicken, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

      Wenn Sie eine neue Zielgruppe erstellen müssen, die sich noch nicht in der [!UICONTROL Audience Library] befindet, klicken Sie auf **Zielgruppe erstellen**. Während des [Zielgruppen-Workflows erstellen](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

      * **[!UICONTROL Audience Library]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der [!UICONTROL Audience Library] gespeichert wird und in anderen Aktivitäten wiederverwendet werden kann.
      * **[!UICONTROL This activity only]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht im [!UICONTROL Audience Library] gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann.

   1. Klicken Sie im rechten Rahmen auf **[!UICONTROL Visitor Percentage]** und wählen Sie dann den Prozentsatz der qualifizierten Besucher aus, die Sie in die Aktivität eingeben möchten.

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Klicken Sie auf das **[!UICONTROL Traffic Allocation]**, um eine der folgenden Optionen auszuwählen:

   ![Optionen für das Traffic-Zuordnungsziel](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap-new.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** Wenn Sie den Algorithmus testen möchten, verwenden Sie eine 50/50-prozentige Aufteilung der Besucher zwischen dem Steuerelement und dem Zielalgorithmus. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Wird zur Verwendung mit „zufälligen Erlebnissen“ als Kontrolle vorgeschlagen.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** Wenn Sie eine „Always on“-Aktivität erstellen möchten, geben Sie 10 % der Besucher das Steuerelement. Diese Option stellt sicher, dass genügend Daten für die Algorithmen vorhanden sind, um das Lernen im Laufe der Zeit fortzusetzen. Der Nachteil hier ist, dass Sie im Gegenzug für die Personalisierung eines größeren Teils Ihres Traffics weniger Präzision in der genauen Steigerung haben. Unabhängig von Ihrem Ziel ist diese Option die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird.
   * **[!UICONTROL Custom Allocation]:** Teilen Sie den Prozentsatz wie gewünscht manuell auf.

1. (Bedingt) Wählen Sie aus der Dropdown-Liste [!UICONTROL Control] ([ ein bestimmtes Erlebnis aus, das als Kontrolle verwendet werden soll](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oder wählen Sie [!UICONTROL Random Experience.]

   Das Kontrollerlebnis liefert einen Vergleich, um zu ermitteln, welche Steigerung der automatisierte Test ermöglicht.

   [!UICONTROL Automated Personalization] misst die Leistung immer an einer Kontrollgruppe. Es empfiehlt sich, mindestens 10 % der Teilnehmer in der Kontrollgruppe zu platzieren. Wenn Sie testen möchten, ob der Personalisierungsalgorithmus für die angegebenen Daten besser funktioniert als keine Personalisierung (z. B. die zufällig bereitgestellte Kontrolle), stellt eine Traffic-Aufteilung von 50/50 % zwischen dem Steuerelement und dem Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit dar, dieses Ziel zu erreichen. Wenn Sie den personalisierten Traffic maximieren möchten und weniger Wert auf das Verständnis des genauen Anstiegs legen, den Ihre Aktivität erzeugt, ist eine Traffic-Aufteilung von 10/90 % zwischen dem Steuerelement und dem Personalisierungsalgorithmus der schnellste und genaueste Weg, um dieses Ziel zu erreichen.

   >[!NOTE]
   >
   >In [!UICONTROL Automated Personalization]-Aktivitäten werden Eingabekriterien (URL-Targeting, Vorlagenregeln und Zielgruppenziele) für jede Anfrage ausgewertet. In älteren Versionen wurden Eingabekriterien nur einmal pro Sitzung bewertet.

1. Klicken Sie auf **[!UICONTROL Next]** , um die Seite **[!UICONTROL Goals & Settings]** anzuzeigen.
1. Konfigurieren Sie die Aktivität mit den folgenden Einstellungen und klicken Sie dann auf **[!UICONTROL Save & Close]**.

   | Einstellung | Beschreibung |
   |--- |--- |
   | [!UICONTROL Name] | Benennen Sie die Aktivität. Geben Sie der Aktivität einen Namen, der aussagekräftig genug ist, damit die Team-Mitglieder sie in der [!UICONTROL Activities] erkennen können. In der oben stehenden Tabelle sehen Sie, welche Zeichen in einem Aktivitätsnamen nicht zulässig sind. |
   | [!UICONTROL Objective] | (Optional) Geben Sie das Ziel des Tests ein. Das Ziel hilft Ihnen, den Zweck der Aktivität zu verinnerlichen. |
   | [!UICONTROL Priority] | Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die Legacy-Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option in [!UICONTROL Administration] > [!UICONTROL Reporting] (Standard) nicht aktiviert ist, geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High].<P>Um die feinabgestimmten Prioritäten zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und schalten Sie die Option [!UICONTROL Enable Fine-Grained Priorities] auf „Ein“.<P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:<ul><li>0 = Niedrig</li><li>999 = Hoch</li></ul>Für Aktivitäten, die in früheren Versionen von [!DNL Target Standard/Premium] erstellt wurden, wird [!UICONTROL Low] Priorität in 0, [!UICONTROL Medium] Priorität in 5 und [!UICONTROL High] Priorität in 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.<P>**Hinweis**: Bevor Sie diese Option nach der Verwendung von feinkörnigen Prioritäten deaktivieren können, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden. |
   | [!UICONTROL Duration] | Legen Sie das Start- und Enddatum für die Aktivität fest. Sie können [!UICONTROL When Activated] auswählen oder ein bestimmtes Datum und eine bestimmte Uhrzeit angeben. |
   | [!UICONTROL Optimization Goal] | Geben Sie das Optimierungsziel an, das aus zwei Parametern besteht:<ul><li>dem, was Sie mit der Aktivität messen möchten,</li><li>der von einem Aktivitätsteilnehmer durchgeführten Aktion, die zeigt, dass das Ziel erreicht wurde</li></ul>Sie können das Optimierungsziel benennen, indem Sie die drei Punkte rechts von [!UICONTROL My Primary Goal] auswählen. [!UICONTROL Automated Personalization] Aktivitäten können [!UICONTROL Conversion] oder [!UICONTROL Revenue] messen. Die Konvertierung kann durch Anzeigen einer Seite oder einer Mbox erreicht werden. Es können auch Klicks verfolgt werden.<P>Das primäre Ziel wird auch die Modellierungsmetrik, die vom Modellierungssystem zur Berechnung des Erfolgs des Erlebnisses verwendet wird.<P>Besucher können zu Tracking-Zwecken in der Aktivität beibehalten werden, nachdem Sie das Modellierungsziel erreicht haben. Beispielsweise wird oft eine [!UICONTROL Automated Personalization]-Aktivität verwendet, um die Klickraten zu verbessern, und dies wird als Modellierungsziel festgelegt. Es ist jedoch wichtig zu sehen, wie erhöhte Klickraten zur finalen Konversion führen; daher ist ein Tracking durch die finale Konversion entscheidend.<P>Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.<P>Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.<P>Mit der Option [!UICONTROL Add Dependency] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.<P>So fügen Sie eine Abhängigkeit hinzu:<ol><li>Nachdem Sie zusätzliche Metriken hinzugefügt haben, klicken Sie unter dem Dreipunkt-Menü rechts von [!UICONTROL Additional Goal] auf **[!UICONTROL Advanced Settings]** .</li><li>Klicken Sie auf die Option **[!UICONTROL Add Dependency]** unten im Abschnitt [!UICONTROL Reporting Settings] .</li><li>Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf [!UICONTROL Reached] , um zwischen [!UICONTROL Reached] und [!UICONTROL Not Reached] umzuschalten.</li></ol>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben. |
   | [!UICONTROL Conversion Metric] | Standardmäßig ist die Konversionsmetrik mit der Optimierungszielmetrik identisch. Sie können jedoch eine separate Konversionsmetrik definieren, indem Sie die Option [!UICONTROL Same as Optimization Goal] deaktivieren. |
   | [!UICONTROL Additional Metrics] | Fügen Sie alle zusätzlichen Berichtsmetriken hinzu, die Sie verwenden möchten. Sie können Konversions- oder Umsatzmetriken hinzufügen.<P>**Hinweis**: Die [!UICONTROL Engagement] wird nicht als zusätzliche Metrik unterstützt. Mit der [!DNL Target] Benutzeroberfläche können Sie möglicherweise die [!UICONTROL Engagement] Metrik auswählen, aber die Daten werden in Berichten nicht genau angezeigt. |
   | [!UICONTROL Audiences for Reporting] | Fügen Sie Zielgruppen hinzu, um die Filterung nach Zielgruppen in Berichten zu ermöglichen. Standardmäßig zeigen die Berichte Ergebnisse für alle berechtigten Besucher. Fügen Sie Zielgruppen hinzu, um Ergebnisse nach spezifischeren Besucheruntergruppen zu filtern.<P>**Hinweis**: Im Gegensatz zu anderen Aktivitätstypen können [!UICONTROL Automated Personalization] [!UICONTROL Adobe Analytics] nicht als Berichtsquelle (A4T) verwenden. |
   | [!UICONTROL Notes] | Geben Sie alle Informationen zu Ihrer Aktivität ein, die für Sie oder andere Team-Mitglieder nützlich sind. Die Größe des [!UICONTROL Notes] Fensterbereichs kann geändert werden. |

   Wenn Sie eine Metrik benennen oder umbenennen, sind die folgenden Zeichen nicht zulässig:

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

Nachdem Sie auf **[!UICONTROL Save & Close]** geklickt haben, wird die [!UICONTROL Overview] der Aktivität angezeigt. Klicken Sie auf **Erlebnisse in der Vorschau**, um eine Vorschau des Aussehens Ihrer Erlebnisse nach der Bereitstellung anzuzeigen. Es wird ein Popup angezeigt, mit dem Sie Links zu Ihren AP-Erlebnissen auf Ihrer Site anzeigen und freigeben können, um eine „echte Vorschau“ der Erlebnisse außerhalb des [!UICONTROL Target] [!UICONTROL Visual Experience Composer] (VEC) zu erhalten. Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Klicken auf einen Link und das anschließende Kopieren der URL direkt aus dem Browser funktioniert nicht. Durch Kopieren des Links enthält die URL einen Parameter, der die Seite nur dann korrekt anzeigt, wenn Sie über den Link in der Nachricht auf die Seite zugreifen.

Weitere Informationen zur Berichterstellung finden Sie unter [Automatisierte Personalisierungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).
