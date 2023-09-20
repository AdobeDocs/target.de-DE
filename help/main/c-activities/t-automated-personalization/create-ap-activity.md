---
keywords: automatisierte Personalisierung;App
description: Erfahren Sie, wie Sie eine [!UICONTROL Automated Personalization] Aktivität (AP) in [!DNL Adobe Target] mithilfe der [!UICONTROL Visual Experience Composer].
title: Wie erstelle ich eine [!UICONTROL Automated Personalization] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1884'
ht-degree: 42%

---

# Erstellen einer [!UICONTROL Automated Personalization]-Aktivität

Erstellen Sie eine [!UICONTROL Automated Personalization] Aktivität (AP) in [!DNL Adobe Target] mithilfe der [!UICONTROL Visual Experience Composer] (VEC).

Die [!UICONTROL Automated Personalization] Aktivitäts-Workflow in [!DNL Target] unterscheidet sich vom Workflow der anderen Aktivitätstypen.

1. Aus dem [!DNL Target] [!UICONTROL Tätigkeiten] Liste, klicken Sie **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Automated Personalization]**.

   ![Aktivität erstellen: Automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/assets/ap-create-new.png)

1. So verwenden Sie die [!UICONTROL Visual Experience Composer] (VEC), klicken Sie auf **[!UICONTROL Visuell]**.

   So verwenden Sie die [!UICONTROL Form-Based Experience Composer]auswählen [!UICONTROL Formular]. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer], [!DNL Target] bietet die [!UICONTROL VEC für Einzelseiten-Apps]. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung für VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) [Arbeitsbereich auswählen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Überprüfen oder geben Sie die Aktivitäts-URL ein und klicken Sie auf **[!UICONTROL Erstellen]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://wwww.adobe.com`] überein.

   Die Seite mit der angegebenen URL wird im VEC geöffnet.

1. Klicken Sie auf **[!UICONTROL Name]** und geben Sie Ihren Aktivitätsnamen ein.

   ![Namensfeld](/help/main/c-activities/t-automated-personalization/assets/ap-new-name.png)

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

1. Klicken Sie auf **[!UICONTROL Inhalt verwalten]**, um die verfügbaren Kombinationen zu konfigurieren.

   ![Option „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Oben im Bildschirm wird ein Dialogfeld mit drei Optionen angezeigt: [!UICONTROL Erlebnisse], [!UICONTROL Angebote], und [!UICONTROL Ausschlussgruppen].

   ![Dialogfeld „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Obwohl Sie bis zu 30.000 Erlebnisse in einer AP-Aktivität erstellen können, funktionieren die Aktivitäten am besten, wenn weniger als 5.000 Erlebnisse verwendet werden. Diese Beschränkung gilt auch dann, wenn die Aktivität die Variable [!UICONTROL Duplikate anzeigen] -Option.

   Die [!UICONTROL Erlebnisse] zeigt jedes für die Aktivität ausgewählte Inhaltselement und den Ort an, dem es zugewiesen ist.

   Sie können bestimmte Erlebnisse ausschließen, indem Sie den Mauszeiger über das gewünschte Erlebnis bewegen und dann auf [!UICONTROL Ausschließen] Symbol.

   ![Symbol zum Ausschließen](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   Sie können Erlebnisse in einem Batch-Vorgang ausschließen oder einschließen, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann auf [!UICONTROL Ausschließen] in der oberen rechten Ecke des Dialogfelds.

   ![Optionen für den Batch-Vorgang zum Ausschließen](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   Sie können diese Listenansicht so filtern, dass nur ausgeschlossene oder nur eingeschlossene Aktivitäten angezeigt werden. Klicken Sie dazu auf die Dropdownliste [!UICONTROL Status].

1. (Optional) Klicken Sie auf **[!UICONTROL Angebote]**, um Inhalte auszuwählen und sie den richtigen Berichtsgruppen zuzuweisen oder per Targeting nur bestimmten Besuchern die Anzeige bestimmter Angebote zu ermöglichen.

   Weitere Informationen zu Berichtsgruppen finden Sie unter [Berichtsgruppen für Angebote in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

1. (Bedingt) Klicken Sie auf **[!UICONTROL Ausschlussgruppen]** , um eine beliebige Elementkombination auszuwählen, die Sie von der Aktivität ausschließen möchten.

   ![Registerkarte mit Ausschlussgruppen im Dialogfeld „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Obwohl Sie bis zu 30.000 Erlebnisse in einem AP-Test erstellen können, funktionieren die Algorithmen am besten, wenn weniger als 10.000 eindeutige Erlebnisse verwendet werden. Diese Beschränkung gilt auch dann, wenn die Aktivität die Variable [!UICONTROL Duplikate anzeigen] -Option.

   Klicken Sie auf **Ausschlussgruppe erstellen**, sofern in Ihrer Aktivität nicht bereits Ausschlussgruppen vorhanden sind. Sie können filtern, um eine Liste zu erstellen, die nur die Kombinationen anzeigt, die Sie ausschließen möchten. Benennen Sie Ihre Ausschlussgruppe und klicken Sie auf **Speichern**.

   Bewegen Sie zum Bearbeiten einer vorhandenen Ausschlussgruppe den Mauszeiger über die Gruppe, die Sie bearbeiten möchten, und klicken Sie dann auf das Stiftsymbol.

1. Klicken Sie auf **[!UICONTROL Fertig]**, wenn Sie die Einrichtung des Inhalts Ihrer Aktivität abgeschlossen haben.

1. Die **Targeting** Schritt vertraut aussieht, wenn Sie andere [!DNL Target] Aktivitätstypen. Hier können Sie eine Zielgruppe auswählen und den Prozentsatz der Besucher angeben, denen das Kontrollerlebnis angezeigt wird, indem Sie auf die **[!UICONTROL Zuordnung anpassen]** Dropdown-Liste und klicken Sie auf **Nächste**.

   In der Dropdownliste [!UICONTROL Zuordnung anpassen] können Sie aus den folgenden Optionen auswählen:

   ![Dropdown-Liste für die Traffic-Zuordnung](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **[!UICONTROL Personalisierungsalgorithmus auswerten (50/50)]:** Wenn Sie den Algorithmus testen möchten, sollten Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus verwenden. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit &quot;zufälligen Erlebnissen&quot;als Kontrolle empfohlen.
   * **[!UICONTROL Personalisierungs-Traffic maximieren (90/10)]:** Wenn Sie eine &quot;Always on&quot;-Aktivität erstellen möchten, sollten Sie 10 % der Besucher in den Kontrollbereich versetzen. Diese Option stellt sicher, dass genügend Daten vorhanden sind, damit die Algorithmen mit der Zeit weiterhin lernen können. Der Nachteil besteht darin, dass Sie im Austausch für die Personalisierung eines größeren Teils Ihres Traffics weniger präzise wissen, was genau die Steigerung ist. Unabhängig von Ihrem Ziel ist diese Option die empfohlene Traffic-Aufteilung bei der Verwendung eines bestimmten Erlebnisses als Kontrolle.
   * **[!UICONTROL Zuordnung anpassen]:** Teilen Sie den Prozentsatz nach Bedarf manuell auf.

1. (Abhängig von Ihrer Lizenz) Wählen Sie aus der Dropdownliste [!UICONTROL Kontrolle] ein [spezifisches Erlebnis aus, das als Kontrolle verwendet werden soll, ](/help/main/c-activities/t-automated-personalization/experience-as-control.md)oder wählen Sie [!UICONTROL Zufälliges Erlebnis] aus.

   Das Kontrollerlebnis liefert einen Vergleich, um zu ermitteln, welche Steigerung der automatisierte Test ermöglicht.

   [!UICONTROL Die automatisierte Personalisierung misst immer die Leistung im Vergleich zu einer Kontrollgruppe. ] Es empfiehlt sich, mindestens 10 % der Teilnehmer in der Kontrollgruppe zu platzieren. Wenn Sie testen möchten, ob der Personalisierungsalgorithmus für die angegebenen Daten besser abschneidet als keine Personalisierung (z. B. die zufällig bereitgestellte Kontrolle), ist eine 50/50-Prozentaufteilung des Traffics zwischen Kontrolle und Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit, dieses Ziel zu erreichen. Wenn Sie die Menge des personalisierten Traffics maximieren möchten und weniger daran interessiert sind, die genaue Steigerung zu verstehen, die Ihre Aktivität generiert, ist eine Traffic-Aufspaltung von 10/90 Prozent zwischen dem Kontroll- und dem Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit, dieses Ziel zu erreichen.

   >[!NOTE]
   >
   >In [!UICONTROL Automated Personalization] Aktivitäten, Einstiegskriterien (URL-Targeting, Vorlagenregeln und Zielgruppen-Targeting) werden für jede Anforderung ausgewertet. In älteren Versionen wurden Eingabekriterien nur einmal pro Sitzung bewertet.

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Seite **[!UICONTROL Ziele und Einstellungen]** anzuzeigen.
1. Konfigurieren Sie die Aktivität mit den folgenden Einstellungen und klicken Sie dann auf **[!UICONTROL Speichern und schließen]**.

   | Einstellung | Beschreibung |
   |--- |--- |
   | [!UICONTROL Name] | Benennen Sie die Aktivität. Geben Sie der Aktivität einen beschreibenden Namen, damit die Teammitglieder sie im [!UICONTROL Tätigkeiten] Liste. In der oben stehenden Tabelle sehen Sie, welche Zeichen in einem Aktivitätsnamen nicht zulässig sind. |
   | [!UICONTROL Ziel] | (Optional) Geben Sie das Ziel des Tests ein. Das Ziel hilft Ihnen, den Zweck der Aktivität zu verinnerlichen. |
   | [!UICONTROL Priorität] | Abhängig von Ihren Einstellungen wird die [!DNL Target] Benutzeroberfläche und Optionen für [!UICONTROL Priorität] variieren. Sie können die veralteten Einstellungen von [!UICONTROL Niedrig], [!UICONTROL Mittel]oder [!UICONTROL Hoch]oder Sie können genauer unterteilte Prioritäten von 0 bis 999 festlegen.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option nicht aktiviert ist in [!UICONTROL Administration] > [!UICONTROL Berichterstellung] (Standardeinstellung), geben Sie eine Priorität an: [!UICONTROL Niedrig], [!UICONTROL Mittel]oder [!UICONTROL Hoch].<P>Um genauer unterteilte Prioritäten festzulegen, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Berichterstellung], und schalten Sie dann die [!UICONTROL Aktivieren genauer Prioritätensetzung] auf die Position &quot;Ein&quot;.<P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:<ul><li>0 = Niedrig</li><li>999 = Hoch</li></ul>Für Aktivitäten, die in früheren Versionen von [!DNL Target Standard/Premium], [!UICONTROL Niedrig] die Priorität in 0 umgewandelt wird, [!UICONTROL Mittel] die Priorität in 5 umgewandelt wird und [!UICONTROL Hoch] -Priorität in 10 umgewandelt wird. Diese Werte können nach Wunsch angepasst werden.<P>**Hinweis:** Haben Sie genauere Prioritäten verwendet und möchten Sie die Option deaktivieren, müssen zunächst alle Prioritätswerte auf 0, 5 und 10 zurückgesetzt werden. |
   | [!UICONTROL Dauer] | Legen Sie Start- und Enddatum für die Aktivität fest. Sie können [!UICONTROL Bei Aktivierung] oder Sie können ein bestimmtes Datum und eine bestimmte Uhrzeit angeben. |
   | [!UICONTROL Optimierungsziel] | Geben Sie das Optimierungsziel an, das aus zwei Parametern besteht:<ul><li>dem, was Sie mit der Aktivität messen möchten,</li><li>der von einem Aktivitätsteilnehmer durchgeführten Aktion, die zeigt, dass das Ziel erreicht wurde</li></ul>Sie können das Optimierungsziel benennen, indem Sie die drei Punkte rechts von [!UICONTROL Mein Primäres Ziel]. [!UICONTROL Automated Personalization] Aktivitäten können [!UICONTROL Konversion] oder [!UICONTROL Umsatz]. Die Konversion kann durch Anzeigen einer Seite oder einer Mbox erreicht werden. Es können auch Klicks verfolgt werden.<P>Das primäre Ziel wird außerdem zur Modellierungsmetrik, die vom Modellierungssystem verwendet wird, um den Erfolg des Erlebnisses zu berechnen.<P>Besucher können zu Tracking-Zwecken in der Aktivität beibehalten werden, nachdem Sie das Modellierungsziel erreicht haben. Beispiel: Häufig wird eine [!UICONTROL Automated Personalization] -Aktivität dient zur Verbesserung der Klickraten, die als Modellierungsziel festgelegt wird. Es ist jedoch wichtig zu sehen, wie erhöhte Klickraten zur finalen Konversion führen; daher ist ein Tracking durch die finale Konversion entscheidend.<P>Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht.<P>Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können.<P>Mithilfe der Option [!UICONTROL Abhängigkeit hinzufügen] kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.<P>So fügen Sie eine Abhängigkeit hinzu:<ol><li>Klicken Sie nach dem Hinzufügen zusätzlicher Metriken auf **[!UICONTROL Erweiterte Einstellungen]** unter dem Menü mit drei Punkten rechts von [!UICONTROL Zusätzliches Ziel].</li><li>Klicken Sie unten im Abschnitt zu [!UICONTROL Berichtseinstellungen] auf die Option **[!UICONTROL Abhängigkeit hinzufügen]**.</li><li>Verschieben Sie die gewünschte Metrik per Drag-and-drop vom linken Bereich in den rechten Bereich. Klicken Sie dann auf [!UICONTROL Erreicht], um die Einstellung zwischen [!UICONTROL Erreicht] und [!UICONTROL Nicht erreicht] zu wechseln </li></ol>Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben. |
   | [!UICONTROL Konversionsmetrik] | Standardmäßig entspricht die Konversionsmetrik der Optimierungszielmetrik. Sie können jedoch eine separate Konversionsmetrik definieren, indem Sie die Option [!UICONTROL Wie Optimierungsziel] deaktivieren. |
   | [!UICONTROL Zusätzliche Metriken] | Fügen Sie zusätzliche Berichtsmetriken hinzu, die Sie verwenden möchten. Sie können Konversions- oder Umsatzmetriken hinzufügen.<P>**Hinweis**: Die [!UICONTROL Interaktion] -Metrik wird nicht als zusätzliche Metrik unterstützt. Die [!DNL Target] In der Benutzeroberfläche können Sie die [!UICONTROL Interaktion] Metrik, aber die Daten werden in Berichten nicht korrekt angezeigt. |
   | [!UICONTROL Zielgruppen für die Berichterstellung] | Fügen Sie Zielgruppen hinzu, um die Filterung nach Zielgruppen in Berichten zu ermöglichen. Standardmäßig zeigen die Berichte Ergebnisse für alle berechtigten Besucher. Fügen Sie Zielgruppen hinzu, um Ergebnisse nach spezifischeren Besucheruntergruppen zu filtern.<P>**Hinweis**: Im Gegensatz zu anderen Aktivitätstypen, [!UICONTROL Automated Personalization] kann nicht verwendet werden [!UICONTROL Adobe Analytics] als Berichtsquelle (A4T). |
   | [!UICONTROL Hinweise] | Geben Sie alle Informationen über Ihre Aktivität ein, die für Sie oder andere Teammitglieder nützlich sind. Die [!UICONTROL Hinweise] -Bereich kann angepasst werden. |

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

Nachdem Sie auf **[!UICONTROL Speichern und schließen]**, der [!UICONTROL Übersicht] angezeigt. Klicks **Erlebnisvorschau** , um zu sehen, wie Ihre Erlebnisse bei der Bereitstellung aussehen. Es wird ein Popup angezeigt, mit dem Sie Links zu Ihren AP-Erlebnissen auf Ihrer Site anzeigen und freigeben können, um eine &quot;echte Vorschau&quot;der Erlebnisse außerhalb der [!UICONTROL Target] [!UICONTROL Visual Experience Composer] (VEC). Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Klicken auf einen Link und das anschließende Kopieren der URL direkt aus dem Browser funktionieren nicht. Durch das Kopieren des Links enthält die URL einen Parameter, der die Seite nur dann richtig anzeigt, wenn Sie über den Link in der Nachricht auf die Seite zugreifen.

Weitere Informationen zur Berichterstellung finden Sie unter [Automatisierte Personalisierungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).
