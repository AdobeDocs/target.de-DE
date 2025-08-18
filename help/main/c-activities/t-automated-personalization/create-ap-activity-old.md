---
keywords: Automated Personalization;App
description: Erfahren Sie, wie Sie eine [!UICONTROL Automated Personalization] (AP)-Aktivität in erstellen [!DNL Adobe Target]  indem Sie die [!UICONTROL Visual Experience Composer] verwenden.
title: Wie erstelle ich eine [!UICONTROL Automated Personalization] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '1743'
ht-degree: 28%

---

# [!UICONTROL Automated Personalization] erstellen

Erstellen Sie eine [!UICONTROL Automated Personalization] (AP)-Aktivität in [!DNL Adobe Target] mithilfe des [!UICONTROL Visual Experience Composer] (VEC).

Der Workflow für die [!UICONTROL Automated Personalization] (AP)-Aktivität in [!DNL Target] unterscheidet sich vom Workflow der anderen Aktivitätstypen.

1. Klicken Sie in der Liste [!DNL Target] [!UICONTROL Activities] auf **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

   ![Aktivität erstellen: Automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/assets/ap-create-new.png)

1. Um den [!UICONTROL Visual Experience Composer] (VEC) zu verwenden, klicken Sie auf **[!UICONTROL Visual]**.

   Um die [!UICONTROL Form-Based Experience Composer] zu verwenden, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] die [!UICONTROL Single Page Application VEC]. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung bei VEC finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) [Wählen Sie einen Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Überprüfen oder geben Sie die Aktivitäts-URL ein und klicken Sie dann auf **[!UICONTROL Create]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://wwww.adobe.com`] überein.

   Die Seite mit der angegebenen URL wird in VEC geöffnet.

1. Klicken Sie auf das Feld **[!UICONTROL Name]** und geben Sie Ihren Aktivitätsnamen ein.

   ![Namensfeld](/help/main/c-activities/t-automated-personalization/assets/ap-new-name.png)

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

1. Klicken Sie auf **[!UICONTROL Manage Content]** , um die verfügbaren Kombinationen zu konfigurieren.

   ![Option „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Oben im Bildschirm wird ein Dialogfeld mit drei Optionen angezeigt: [!UICONTROL Experiences], [!UICONTROL Offers] und [!UICONTROL Exclusion Groups].

   ![Dialogfeld „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Sie können in einer AP-Aktivität zwar bis zu 30.000 Erlebnisse erstellen, die Aktivität funktioniert jedoch am besten, wenn weniger als 5.000 Erlebnisse verwendet werden. Diese Beschränkung gilt selbst dann, wenn bei der Aktivität die Option [!UICONTROL Disalow Duplicates] aktiviert ist.

   In der [!UICONTROL Experiences] Liste werden alle für die Aktivität ausgewählten Inhaltselemente und der ihnen zugewiesene Speicherort angezeigt.

   Sie können bestimmte Erlebnisse ausschließen, indem Sie den Mauszeiger über das gewünschte Erlebnis bewegen und dann auf das Symbol [!UICONTROL Exclude] klicken.

   ![Symbol zum Ausschließen](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   Sie können Erlebnisse im Batch-Modus aus- oder einschließen, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann auf das [!UICONTROL Exclude] oben rechts im Dialogfeld klicken.

   ![Optionen für den Batch-Vorgang zum Ausschließen](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   Sie können diese Listenansicht so filtern, dass nur ausgeschlossene oder nur eingeschlossene Aktivitäten angezeigt werden, indem Sie auf die Dropdown-Liste [!UICONTROL Status] klicken.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Offers]** , um Inhaltselemente auszuwählen und sie Berichtsgruppen zuzuweisen oder nur bestimmten Besuchern zu ermöglichen, bestimmte Angebote beim Targeting zu sehen.

   Weitere Informationen zu Berichtsgruppen finden Sie unter [Berichtsgruppen in Automated Personalization ](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

1. (Bedingt) Klicken Sie auf **[!UICONTROL Exclusion Groups]** , um eine beliebige Kombination von Elementen auszuwählen, die Sie aus der Aktivität ausschließen möchten.

   ![Registerkarte mit Ausschlussgruppen im Dialogfeld „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Sie können zwar bis zu 30.000 Erlebnisse in einem AP-Test erstellen, der Algorithmus funktioniert jedoch am besten, wenn weniger als 10.000 unterschiedliche Erlebnisse verwendet werden. Diese Beschränkung gilt selbst dann, wenn bei der Aktivität die Option [!UICONTROL Disalow Duplicates] aktiviert ist.

   Klicken Sie auf **Ausschlussgruppe erstellen**, sofern in Ihrer Aktivität nicht bereits Ausschlussgruppen vorhanden sind. Sie können filtern, um eine Liste zu erstellen, die nur die Kombinationen anzeigt, die Sie ausschließen möchten. Benennen Sie Ihre Ausschlussgruppe und klicken Sie dann auf **Speichern**.

   Bewegen Sie zum Bearbeiten einer vorhandenen Ausschlussgruppe den Mauszeiger über die Gruppe, die Sie bearbeiten möchten, und klicken Sie dann auf das Stiftsymbol.

1. Klicken Sie auf **[!UICONTROL Done]** , wenn Sie die Einrichtung des Inhalts Ihrer Aktivität abgeschlossen haben.

1. Der **Targeting**-Schritt kommt Ihnen bekannt vor, wenn Sie andere [!DNL Target] Aktivitätstypen verwendet haben. Hier können Sie eine Zielgruppe auswählen und den Prozentsatz der Besucher angeben, die das Kontrollerlebnis sehen, indem Sie auf die Dropdown-Liste **[!UICONTROL Custom Allocation]** und dann auf **Weiter** klicken.

   In der Dropdown-Liste [!UICONTROL Custom Allocation] können Sie aus den folgenden Optionen auswählen:

   ![Dropdown-Liste für die Traffic-Zuordnung](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

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
   | [!UICONTROL Optimization Goal] | Geben Sie das Optimierungsziel an, das aus zwei Parametern besteht:<ul><li>dem, was Sie mit der Aktivität messen möchten,</li><li>der von einem Aktivitätsteilnehmer durchgeführten Aktion, die zeigt, dass das Ziel erreicht wurde</li></ul>Sie können das Optimierungsziel benennen, indem Sie die drei Punkte rechts von [!UICONTROL My Primary Goal] auswählen. [!UICONTROL Automated Personalization] Aktivitäten können [!UICONTROL Conversion] oder [!UICONTROL Revenue] messen. Die Konvertierung kann durch Anzeigen einer Seite oder einer Mbox erreicht werden. Es können auch Klicks verfolgt werden.<P>Das primäre Ziel wird auch die Modellierungsmetrik, die vom Modellierungssystem zur Berechnung des Erfolgs des Erlebnisses verwendet wird.<P>Besucher können zu Tracking-Zwecken in der Aktivität beibehalten werden, nachdem Sie das Modellierungsziel erreicht haben. Beispielsweise wird oft eine [!UICONTROL Automated Personalization]-Aktivität verwendet, um die Klickraten zu verbessern, und dies wird als Modellierungsziel festgelegt. Es ist jedoch wichtig zu sehen, wie erhöhte Klickraten zur finalen Konversion führen; daher ist ein Tracking durch die finale Konversion entscheidend.<P>Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.<P>Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.<P>Mit der Option [!UICONTROL Add Dependency] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.<P>So fügen Sie eine Abhängigkeit hinzu:<ol><li>Nachdem Sie zusätzliche Metriken hinzugefügt haben, klicken Sie unter dem Dreipunkt-Menü rechts von **[!UICONTROL Advanced Settings]** auf [!UICONTROL Additional Goal] .</li><li>Klicken Sie auf die Option **[!UICONTROL Add Dependency]** unten im Abschnitt [!UICONTROL Reporting Settings] .</li><li>Ziehen Sie die gewünschten Metriken aus dem linken Bereich in den rechten Bereich und klicken Sie dann auf [!UICONTROL Reached] , um zwischen [!UICONTROL Reached] und [!UICONTROL Not Reached] umzuschalten.</li></ol>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben. |
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
