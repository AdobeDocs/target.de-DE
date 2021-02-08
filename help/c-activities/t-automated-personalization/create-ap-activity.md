---
keywords: automatisierte Personalisierung;ap;Audiencen;ensemble;Random. Wald;Restschwankung;Fehlerschwankung;Lebenszeitwert
description: Erfahren Sie, wie Sie mit dem Visual Experience Composer (VEC) eine Automated Personalization (AP)-Aktivität in Adobe Target erstellen.
title: Wie erstelle ich eine Automated Personalization-Aktivität?
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '2057'
ht-degree: 91%

---


# ![PREMIUM](/help/assets/premium.png) Erstellen einer Aktivität mit automatisierter Personalisierung

Der Arbeitsablauf für die Aktivität [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target] unterscheidet sich vom Arbeitsablauf der anderen Aktivitäten.

1. Klicken Sie in der Liste [!DNL Target] [!UICONTROL Aktivitäten] auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Automated Personalization]**.

   ![Aktivität erstellen: Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/assets/ap_create-new.png)

1. Um den [!UICONTROL Visual Experience Composer] (VEC) zu verwenden, klicken Sie auf **[!UICONTROL Visuell (Standard)]**.

   ![Dialogfeld zum Erstellen einer automatisierten Personalisierung](/help/c-activities/t-automated-personalization/assets/ap_url-new.png)

   Wenn Sie den [!UICONTROL Form-Based Experience Composer] verwenden möchten, wählen Sie [!UICONTROL Formular]. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zu VEC und [!UICONTROL Form-Based Experience Composer] werden [!DNL Target] die Angebot [!UICONTROL Einzelseitenanwendung VEC] und VEC für Mobilanwendungen erstellt. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >Die Option [!UICONTROL „Arbeitsplatz auswählen“] in der obigen Abbildung ist eine Funktion von [Target Premium](/help/c-intro/intro.md). Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.

1. (Bedingt) Wenn Sie ein Premium-Kunde sind, [wählen Sie einen Arbeitsbereich](/help/administrating-target/c-user-management/property-channel/property-channel.md).[!DNL Target]

1. Überprüfen Sie die Aktivitäts-URL bzw. geben Sie sie ein und klicken Sie dann auf **[!UICONTROL Weiter]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://wwww.adobe.com`] überein.

   Die Seite mit der angegebenen URL wird im Visual Experience Composer geöffnet.

1. Um der Aktivität einen Namen zu geben, klicken Sie auf das Feld **[!UICONTROL Name]** und geben Sie Ihren Aktivitäten-Namen ein.

   ![Namensfeld](/help/c-activities/t-automated-personalization/assets/ab_newname-new.png)

   Folgende Zeichen sind im Aktivitätsnamen nicht zulässig:

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

1. Die Seitenelemente können Sie wie im Abschnitt zu den [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) beschrieben ändern.

   Sie können aus dem Asset-Manager mehrere Bilder auf einmal auswählen. Dies ermöglicht Ihnen, sich die Seite mit jedem der für die Aktivität konfigurierten Bilder schnell anzusehen. Sie können auch einfach Textelemente in Ihren Angeboten bearbeiten. Wenn Sie ein Element bearbeiten, werden Balken darauf eingeblendet, um darauf hinzuweisen, dass Sie Änderungen vorgenommen haben.

1. Klicken Sie auf **[!UICONTROL Inhalt verwalten]**, um die verfügbaren Kombinationen zu konfigurieren.

   ![Option „Inhalt verwalten“](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Oben auf dem Bildschirm wird ein Dialogfeld mit drei Optionen angezeigt: „Erlebnisse“, „Angebote“ und „Ausschlussgruppen“.

   ![Dialogfeld „Inhalt verwalten“](/help/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Obwohl Sie bis zu 30.000 Erlebnisse in einer AP-Aktivität erstellen können, funktionieren die Aktivitäten am besten, wenn weniger als 5.000 Erlebnisse verwendet werden.

   Die Liste [!UICONTROL Erlebnisse] zeigt jedes für die Aktivität ausgewählte Inhaltselement und den Ort, dem diese Aktivität zugeordnet ist.

   Sie können spezifische Erlebnisse ausschließen, indem Sie den Mauszeiger über das gewünschte Erlebnis bewegen und dann auf das Ausschlusssymbol klicken.

   ![Symbol zum Ausschließen](/help/c-activities/t-automated-personalization/assets/icon-exclude.png)

   Sie können Erlebnisse in einem Batch-Vorgang ausschließen/einschließen, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann in der oberen rechten Ecke des Dialogfelds auf das Ausschließen-Symbol klicken.

   ![Optionen für den Batch-Vorgang zum Ausschließen](/help/c-activities/t-automated-personalization/assets/batch-exclude.png)

   Sie können diese Listenansicht so filtern, dass nur ausgeschlossene oder nur eingeschlossene Aktivitäten angezeigt werden. Klicken Sie dazu auf die Dropdownliste **Status**.

1. (Optional) Klicken Sie auf **[!UICONTROL Angebote]**, um Inhalte auszuwählen und sie den richtigen Berichtsgruppen zuzuweisen oder per Targeting nur bestimmten Besuchern die Anzeige bestimmter Angebote zu ermöglichen.

   Weitere Informationen finden Sie unter [Berichtsgruppen für Angebote in Automated Personalization](/help/c-reports/offer-reporting-groups-in-automated-personalization.md#concept_194128C0B56B4B26AAB57DB49892960C).

   Mit der Liste [!UICONTROL Standort] können Sie Angebote nach Standort filtern. Mit der Liste [!UICONTROL Berichtsgruppe] können Sie Angebote nach Berichtsgruppe filtern. Sie können die Liste [!UICONTROL Berichtsgruppe] auch verwenden, um [!UICONTROL nicht zugewiesenen Angeboten] zu filtern und so ein Angebot, dem bisher noch keine Berichtsgruppe zugewiesen wurde, einer beliebigen Gruppe zuzuweisen.

   Sie können bestimmte Erlebnisse zu einer Berichtsgruppe hinzufügen, indem Sie den Mauszeiger über das gewünschte Angebot bewegen und auf das Ordnersymbol klicken.

   ![Ordnersymbol](/help/c-activities/t-automated-personalization/assets/icon-folder.png)

   Sie können Erlebnisse in einem Batch-Vorgang zu einer Berichtsgruppe hinzufügen, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann oben rechts im Dialogfeld auf das Berichtsgruppen-Ordnersymbol klicken.

   ![Optionen für Berichtsgruppen](/help/c-activities/t-automated-personalization/assets/report-group-options.png)

   Es ist wichtig zu verstehen, dass sich Berichtsgruppen darauf auswirken, wie Target seine Modelle erstellt. Daher wird empfohlen, dass Sie Berichtsgruppen nur dann verwenden, wenn Sie planen, Angebote zu ersetzen oder neue Angebote hinzuzufügen, während die Aktivität aktiv ist. Wenn ein neues Angebot in eine aktive Aktivität eingeführt wird, kann die Maschine durch das Verschieben des neuen Angebots in eine Gruppe mit vorhandenen ähnlichen Angeboten die für die anderen Angebote in der zugehörigen Gruppe bereits gesammelten Daten verwenden, um Informationen über das neue Angebot zu erhalten. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben.

   Weitere Informationen zum Targeting eines Angebots für bestimmte Zielgruppen erhalten Sie unter [Target-AP-Angebote](/help/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

1. (Abhängig von Ihrer Lizenz) Klicken Sie auf **[!UICONTROL Ausschlussgruppen]**, um beliebige Kombinationen der Elemente auszuwählen, die Sie aus der Aktivität ausschließen möchten.

   ![Registerkarte mit Ausschlussgruppen im Dialogfeld „Inhalt verwalten“](/help/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Obwohl Sie bis zu 30.000 Erlebnisse in einem AP-Test erstellen können, funktionieren die Algorithmen am besten, wenn weniger als 10.000 eindeutige Erlebnisse verwendet werden.

   Klicken Sie auf **Ausschlussgruppe erstellen**, sofern in Ihrer Aktivität nicht bereits Ausschlussgruppen vorhanden sind. Sie können filtern, um eine Liste zu erstellen, die nur die Kombinationen anzeigt, die Sie ausschließen möchten. Benennen Sie Ihre Ausschlussgruppe und klicken Sie auf **Speichern**.

   Bewegen Sie zum Bearbeiten einer vorhandenen Ausschlussgruppe den Mauszeiger über die Gruppe, die Sie bearbeiten möchten, und klicken Sie dann auf das Stiftsymbol.

1. Klicken Sie auf **[!UICONTROL Fertig]**, wenn Sie die Einrichtung des Inhalts Ihrer Aktivität abgeschlossen haben.

1. Der **Targeting**-Schritt wird Ihnen vertraut vorkommen, wenn Sie andere Target-Aktivitätstypen verwendet haben. Hier können Sie eine Zielgruppe auswählen und den Prozentsatz der Besucher angeben, denen das Kontrollerlebnis angezeigt wird. Klicken Sie dazu auf die Dropdownliste **[!UICONTROL Zuordnung anpassen]** und klicken Sie dann auf **Weiter**.

   In der Dropdownliste [!UICONTROL Zuordnung anpassen] können Sie aus den folgenden Optionen auswählen:

   ![Dropdown-Liste für die Traffic-Zuordnung](/help/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **Personalisierungsalgorithmus auswerten (50/50):** Wenn Sie den Algorithmus testen möchten, sollten Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus verwenden. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit „zufällige Erlebnisse“ als Kontrolle empfohlen.
   * **Personalisierungs-Traffic maximieren (90/10):** Wenn Sie eine „Always on“-Aktivität erstellen möchten, sollten Sie 10 % der Besucher in den Kontrollbereich versetzen, um sicherzustellen, dass ausreichend Daten vorhanden sind, damit die Algorithmen mit der Zeit weiterhin lernen können. Beachten Sie, dass das Personalisieren einer größeren Traffic-Menge zur Folge hat, dass die Bestimmung der exakten Steigerung weniger präzise ist. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird.
   * **Zuordnung anpassen:** Teilen Sie den Prozentsatz nach Bedarf manuell auf.

1. (Abhängig von Ihrer Lizenz) Wählen Sie aus der Dropdownliste [!UICONTROL Kontrolle] ein [spezifisches Erlebnis aus, das als Kontrolle verwendet werden soll, ](/help/c-activities/t-automated-personalization/experience-as-control.md)oder wählen Sie [!UICONTROL Zufälliges Erlebnis] aus.

   Das Kontrollerlebnis liefert einen Vergleich, um zu ermitteln, welche Steigerung der automatisierte Test ermöglicht.

   Die automatisierte Personalisierung misst immer die Leistung im Vergleich zu einer Kontrollgruppe. Es empfiehlt sich, mindestens 10 % der Teilnehmer in der Kontrollgruppe zu platzieren. Wenn Sie testen möchten, ob der Personalisierungsalgorithmus für die angegebenen Daten besser funktioniert als ohne Personalisierung (d. h. die zufallsgestützte Kontrolle), stellt eine 50/50-Prozentaufteilung des Traffics zwischen dem Kontroll- und Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit dar, um dieses Ziel zu erreichen. Wenn Sie die Menge des personalisierten Traffics maximieren möchten und Sie sich weniger Gedanken dahingehend machen, ob Sie die genaue Steigerung nachvollziehen können, die durch Ihre Aktivität generiert wird, stellt eine 10/90-Prozentaufteilung des Traffics zwischen dem Kontroll- und Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit dar, um dieses Ziel zu erreichen.

   >[!NOTE]
   >
   >In automatisierten Personalisierungsaktivitäten werden nun Eingabekriterien (URL-Targeting, Vorlagenregeln und Zielgruppen-Targeting) für jede Abfrage ausgewertet. In älteren Versionen wurden Eingabekriterien nur einmal pro Sitzung bewertet.

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Seite **[!UICONTROL Ziele und Einstellungen]** anzuzeigen.
1. Konfigurieren Sie die Aktivität mit den folgenden Einstellungen und klicken Sie dann auf **[!UICONTROL Speichern und schließen]**.

   | Einstellung | Beschreibung |
   |--- |--- |
   | Name | Benennen Sie die Aktivität. Geben Sie der Aktivität einen beschreibenden Namen, sodass Teammitglieder diese in der Aktivitätenliste erkennen können.  In der oben stehenden Tabelle sehen Sie, welche Zeichen in einem Aktivitätsnamen nicht zulässig sind. |
   | Ziel | (Optional) Geben Sie das Ziel des Tests ein. Das Ziel hilft Ihnen, den Zweck der Aktivität zu verinnerlichen. |
   | Priorität | Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren.<br>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<br>Wenn diese Option in  [!UICONTROL Administration] >  [!UICONTROL Berichte]  (Standard) nicht aktiviert ist, geben Sie eine Priorität an: Niedrig, mittel oder hoch.<br>Klicken Sie zum Aktivieren der Feinabstufungen auf  [!UICONTROL Administration]  >  [!UICONTROL Berichte] und aktivieren Sie dann die Option Feinkörnige  [!UICONTROL Prioritäten ] aktivieren auf die Position &quot;Ein&quot;.<br>Ist diese Option aktiviert, legen Sie einen Wert zwischen 0 und 999 fest:<ul><li>0 = Niedrig</li><li>999 = Hoch</li></ul>Bei Aktivitäten, die in älteren Versionen von Target Standard/Premium erstellt wurden, wird eine niedrige Priorität in den Wert 0, eine mittlere in den Wert 5 und eine hohe in den Wert 10 umgewandelt. Diese Werte können nach Wunsch angepasst werden.<br>**Hinweis:** Haben Sie genauere Prioritäten verwendet und möchten Sie die Option deaktivieren, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden. |
   | Dauer | Legen Sie Start- und Enddatum für die Aktivität fest. |
   | Optimierungsziel | Geben Sie das Optimierungsziel an, das aus zwei Parametern besteht:<ul><li>dem, was Sie mit der Aktivität messen möchten,</li><li>der von einem Aktivitätsteilnehmer durchgeführten Aktion, die zeigt, dass das Ziel erreicht wurde</li></ul>Sie können das Optimierungsziel benennen. Wählen Sie dazu die drei Punkte rechts neben „Mein Primärziel“ aus. Automatisierte Personalisierungsaktivitäten können die Konversion, RPV und AOV messen. Konversion kann durch Betrachten einer Seite oder einer Mbox erreicht werden. Es können auch Klicks verfolgt werden.<br>Das primäre Ziel wird außerdem zur Modellierungsmetrik, die vom Modellierungssystem verwendet wird, um den Erfolg des Erlebnisses zu berechnen.<br>Besucher können zu Tracking-Zwecken in der Aktivität beibehalten werden, nachdem Sie das Modellierungsziel erreicht haben. Beispiel: Eine Aktivität „Automatisierte Personalisierung“ wird oft verwendet, um die Klickraten zu verbessern; dies wird als Modellierungsziel festgelegt. Es ist jedoch wichtig zu sehen, wie erhöhte Klickraten zur finalen Konversion führen; daher ist ein Tracking durch die finale Konversion entscheidend.<br>Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.<br>Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.<br>Mithilfe der Option Abhängigkeit hinzufügen kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.<br>So fügen Sie eine Abhängigkeit hinzu:<ol><li>Klicken Sie nach dem Hinzufügen von zusätzlichen Metriken unter dem Menü mit den drei Punkten rechts neben „Zusätzliches Ziel“ auf [!UICONTROL Erweiterte Einstellungen].</li><li>Klicken Sie unten im Abschnitt zu [!UICONTROL Berichtseinstellungen] auf die Option [!UICONTROL Abhängigkeit hinzufügen].</li><li>Verschieben Sie die gewünschte Metrik per Drag-and-drop vom linken Bereich in den rechten Bereich. Klicken Sie dann auf [!UICONTROL Erreicht], um die Einstellung zwischen [!UICONTROL Erreicht] und [!UICONTROL Nicht erreicht] zu wechseln</li></ol>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben. |
   | Konversionsmetrik | Standardmäßig entspricht die Konversionsmetrik der Optimierungszielmetrik. Sie können jedoch eine separate Konversionsmetrik definieren, indem Sie die Option [!UICONTROL Wie Optimierungsziel] deaktivieren. |
   | Zusätzliche Metriken | Geben Sie beliebige weitere Berichterstellungsmetriken an, die Sie verwenden möchten. Sie können Konversions- oder Umsatzmetriken hinzufügen.<br>**Hinweis:** Die Interaktionskennzahl wird nicht als zusätzliche Metrik unterstützt. Sie können die Interaktionsmetrik in der Benutzeroberfläche zwar auswählen, aber in Berichten werden keine korrekten Daten angezeigt. |
   | Zielgruppen für die Berichterstellung | Fügen Sie Zielgruppen hinzu, um die Filterung nach Zielgruppen in Berichten zu ermöglichen. Standardmäßig zeigen die Berichte Ergebnisse für alle berechtigten Besucher. Fügen Sie Zielgruppen hinzu, um Ergebnisse nach spezifischeren Besucheruntergruppen zu filtern.<br>**Hinweis:** Im Gegensatz zu anderen Aktivitätstypen kann Automated Personalization Adobe Analytics nicht als Berichtsquelle verwenden. |
   | Hinweise | Geben Sie sämtliche Informationen ein, die für Sie und Ihre Team-Mitglieder von Nutzen sind. Die Größe des Notizbereichs kann angepasst werden. |

   Beachten Sie, dass bei der (Um-)Benennung von Metriken folgende Zeichen nicht zulässig sind:

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

Nachdem Sie auf **[!UICONTROL Erstellen]** geklickt haben, wird die Aktivitätsübersicht angezeigt. Klicken Sie auf **Vorschau für Erlebnisse**, um das Erscheinungsbild Ihrer Erlebnisse bei Bereitstellung in der Vorschau anzuzeigen. Ein Pop-up erscheint, das Sie zum Aufrufen und Freigeben der Links zu Ihren AP-Erlebnissen auf Ihrer Seite verwenden können, um eine Vorschau der Erlebnisse außerhalb des Visual Experience Composer von Target zu erhalten. Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Anklicken des Links und Kopieren der URL direkt auf der Seite funktionieren nicht, weil die URL einen Parameter enthält, der die Seite nur dann korrekt anzeigt, wenn Sie vom Link in der Nachricht aus auf die Seite zugreifen.

Weitere Informationen zur Berichterstellung finden Sie unter [Automatisierte Personalisierungsberichte](/help/c-reports/reports-ap.md#concept_C02BAFC922114A44846998FD956E345A).
