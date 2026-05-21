---
keywords: Automated Personalization;App
description: Erfahren Sie, wie Sie eine [!UICONTROL Automated Personalization] (AP)-Aktivität mit dem [!UICONTROL Visual Experience Composer] erstellen.
title: Wie erstelle ich eine [!UICONTROL Automated Personalization] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
TQID: https://experienceleague.adobe.com/5eUFwob4BekIJP4SM2lrSDQam4h1AXIByJjM7-1RNL8
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 8d0c691fdbeee92b36105db9175475507e5fcfce
workflow-type: tm+mt
source-wordcount: 1856
ht-degree: 23%

---

# [!UICONTROL Automated Personalization] erstellen

Erstellen Sie eine [!UICONTROL Automated Personalization] (AP)-Aktivität in [!DNL Adobe Target] mithilfe des [!UICONTROL Visual Experience Composer] (VEC).

Der Workflow für die [!UICONTROL Automated Personalization] (AP)-Aktivität in [!DNL Target] unterscheidet sich vom Workflow der anderen Aktivitätstypen.

Dieses Verfahren folgt dem dreistufigen Workflow in der [!UICONTROL Visual Experience Composer]:

1. [Schritt 1: Erstellen Sie Erlebnisse](#build-experiences)
1. [Schritt 2: Zielgruppenbestimmung festlegen](#set-targeting)
1. [Schritt 3: Ziele und Einstellungen konfigurieren](#configure-goals-and-settings)

## Schritt 1: Erstellen Sie Erlebnisse {#build-experiences}

Definieren Sie den Pool von Inhaltsvarianten, mit denen [!UICONTROL Automated Personalization] personalisieren können. Je umfassender und differenzierter Ihre Erlebnisse und Angebote sind, desto besser kann der Algorithmus den richtigen Inhalt für jeden Besucher abgleichen.

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

1. Um die Aktivität zu benennen, klicken Sie auf das Symbol **[!UICONTROL Edit]** ( ![Bearbeiten](/help/main/assets/icons/Edit.svg) ) neben &quot;[!UICONTROL Untitled Activity]&quot;, geben Sie einen beschreibenden Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Save]**.

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

   Ein Dialogfeld wird mit zwei Registerkarten angezeigt: [!UICONTROL Experiences] und [!UICONTROL Offers]. Auf der Registerkarte [!UICONTROL Experiences] werden alle Inhaltselemente und deren Speicherort aufgelistet. Um ein oder mehrere Erlebnisse auszuschließen, aktivieren Sie die entsprechenden Kontrollkästchen und klicken Sie auf das Symbol [!UICONTROL Exclude] . Weitere Optionen finden Sie unter [Verwalten von Ausschlüssen](/help/main/c-activities/t-automated-personalization/managing-exclusions.md).

   >[!IMPORTANT]
   >
   >**Best Practice:** Um eine optimale Leistung zu erzielen, beschränken Sie [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target] auf 4-6 Standorte mit 4-6 Angeboten pro Standort. Die Gesamtzahl der Erlebnisse wächst aus der kartesischen Kombination von Standorten und Angeboten. Größere Konfigurationen können zu langsamem Laden oder Bearbeiten im [!UICONTROL Visual Experience Composer] führen. Halten Sie die Gesamtzahl unter 5.000 Erlebnisse für optimale Ergebnisse; die feste Grenze ist 30.000 (dieselbe Grenze gilt, wenn die [!UICONTROL Disallow Duplicates] aktiviert ist).

1. (Bedingt) Klicken Sie auf **[!UICONTROL Offers]** , um Inhaltselemente auszuwählen und sie Berichtsgruppen zuzuweisen oder nur bestimmten Besuchern zu ermöglichen, bestimmte Angebote beim Targeting zu sehen.

   Weitere Informationen zu Berichtsgruppen finden Sie unter [Berichtsgruppen in Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

<!--
1. (Conditional) Click **[!UICONTROL Exclusion Groups]** to choose any combination of elements that you want to exclude from the activity.

   ![Exclusion Groups tab of Manage Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the [!UICONTROL Disalow Duplicates] option.

   If you do not currently have any exclusion groups included in your activity, click **Create Exclusion Group**. You can filter to create a list that shows only the combinations you want to exclude. Name your exclusion group, then click **Save**.

   To edit an existing exclusion group, hover over the group you want to edit, then click the pencil icon.
-->

1. Klicken Sie auf **[!UICONTROL Done]** , wenn Sie die Einrichtung des Inhalts Ihrer Aktivität abgeschlossen haben.

## Schritt 2: Zielgruppenbestimmung festlegen {#set-targeting}

Entscheiden Sie, welche Besucher in die Aktivität eintreten und wie viel Traffic offen gelegt wird. Kombinieren Sie sie mit einer Kontrollgruppe, damit [!DNL Target] die Ergebnisse der Aufstiegspersonalisierung messen können.

1. Klicken Sie oben in der [!UICONTROL Visual Experience Composer] auf **[!UICONTROL Targeting]** , um mit dem nächsten Schritt im Drei-Schritte-Workflow fortzufahren.

   Der **Targeting**-Schritt kommt Ihnen bekannt vor, wenn Sie andere [!DNL Target] Aktivitätstypen verwendet haben. Hier können Sie eine Zielgruppe auswählen und den Prozentsatz der Besucher angeben, die die einzelnen Erlebnisse sehen.

1. Das Flussdiagramm führt Sie durch die Schritte Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, Auswählen der Traffic-Zuordnungsmethode und Festlegen der Traffic-Zuordnung für jedes Erlebnis in der Aktivität.

   ![AP-Test-Targeting-Schritt](/help/main/c-activities/t-automated-personalization/assets/ap-traffic-flow.png)

1. (Bedingt) Klicken Sie auf das Steuerelement **[!UICONTROL All Visitors]** , um [eine andere Zielgruppe auswählen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) für die Aktivität festzulegen und ihren Besucherprozentsatz festzulegen.

   Die [!UICONTROL All Visitors] Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt, z. B. können Sie Einträge auf 50 % aller Besucher oder 45 % Ihrer „Californians“-Zielgruppe beschränken.

1. Klicken Sie auf das **[!UICONTROL Traffic Allocation]**, um eine der folgenden Optionen auszuwählen:

   ![Optionen für das Traffic-Zuordnungsziel](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap-new.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** Wenn Sie den Algorithmus testen möchten, verwenden Sie eine 50/50-prozentige Aufteilung der Besucher zwischen dem Steuerelement und dem Zielalgorithmus. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Wird zur Verwendung mit „zufälligen Erlebnissen“ als Kontrolle vorgeschlagen.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** Wenn Sie eine „Always on“-Aktivität erstellen möchten, geben Sie 10 % der Besucher das Steuerelement. Diese Option stellt sicher, dass genügend Daten für die Algorithmen vorhanden sind, um das Lernen im Laufe der Zeit fortzusetzen. Der Nachteil hier ist, dass Sie im Gegenzug für die Personalisierung eines größeren Teils Ihres Traffics weniger Präzision in der genauen Steigerung haben. Unabhängig von Ihrem Ziel ist diese Option die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird.
   * **[!UICONTROL Custom Allocation]:** Teilen Sie den Prozentsatz wie gewünscht manuell auf.

1. (Bedingt) Wählen Sie aus der Dropdown-Liste [!UICONTROL Control] ([&#x200B; ein bestimmtes Erlebnis aus, das als Kontrolle verwendet werden soll](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oder wählen Sie [!UICONTROL Random Experience.]

   Das Kontrollerlebnis liefert einen Vergleich, um zu ermitteln, welche Steigerung der automatisierte Test ermöglicht.

   [!UICONTROL Automated Personalization] misst die Leistung immer an einer Kontrollgruppe. Es empfiehlt sich, mindestens 10 % der Teilnehmer in der Kontrollgruppe zu platzieren. Wenn Sie testen möchten, ob der Personalisierungsalgorithmus für die angegebenen Daten besser funktioniert als keine Personalisierung (z. B. die zufällig bereitgestellte Kontrolle), stellt eine Traffic-Aufteilung von 50/50 % zwischen dem Steuerelement und dem Personalisierungsalgorithmus die schnellste und genaueste Möglichkeit dar, dieses Ziel zu erreichen. Wenn Sie den personalisierten Traffic maximieren möchten und weniger Wert auf das Verständnis des genauen Anstiegs legen, den Ihre Aktivität erzeugt, ist eine Traffic-Aufteilung von 10/90 % zwischen dem Steuerelement und dem Personalisierungsalgorithmus der schnellste und genaueste Weg, um dieses Ziel zu erreichen.

   >[!NOTE]
   >
   >In [!UICONTROL Automated Personalization]-Aktivitäten werden Eingabekriterien (URL-Targeting, Vorlagenregeln und Zielgruppenziele) für jede Anfrage ausgewertet. In älteren Versionen wurden Eingabekriterien nur einmal pro Sitzung bewertet.

## Schritt 3: Ziele und Einstellungen konfigurieren {#configure-goals-and-settings}

Teilen Sie [!DNL Target] mit, wie der Erfolg aussieht. Das von Ihnen gewählte Optimierungsziel ist die Metrik, mit der der Personalisierungsalgorithmus trainiert, also wählen Sie das Ergebnis aus, das für diese Aktivität am wichtigsten ist.

1. Klicken Sie auf **[!UICONTROL Next]** , um die Seite **[!UICONTROL Goals & Settings]** anzuzeigen.
1. Konfigurieren Sie die Aktivität mit den folgenden Einstellungen und klicken Sie dann auf **[!UICONTROL Save & Close]**.

   | Einstellung | Beschreibung |
   |--- |--- |
   | [!UICONTROL Name] | Benennen Sie die Aktivität. Geben Sie der Aktivität einen Namen, der aussagekräftig genug ist, damit die Team-Mitglieder sie in der [!UICONTROL Activities] erkennen können. In der oben stehenden Tabelle sehen Sie, welche Zeichen in einem Aktivitätsnamen nicht zulässig sind. |
   | [!UICONTROL Objective] | (Optional) Geben Sie das Ziel des Tests ein. Das Ziel hilft Ihnen, den Zweck der Aktivität zu verinnerlichen. |
   | [!UICONTROL Priority] | Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für [!UICONTROL Priority]. Sie können die Legacy-Einstellungen von [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High] verwenden oder feinabgestimmte Prioritäten von 0 bis 999 aktivieren.<P>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.<P>Wenn diese Option in [!UICONTROL Administration] > [!UICONTROL Reporting] (Standard) nicht aktiviert ist, geben Sie eine Priorität an: [!UICONTROL Low], [!UICONTROL Medium] oder [!UICONTROL High].<P>Um die feinabgestimmten Prioritäten zu aktivieren, klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Reporting] und schalten Sie die Option [!UICONTROL Enable Fine-Grained Priorities] auf „Ein“.<P>Wenn diese Option aktiviert ist, geben Sie einen Wert zwischen 0 und 999 an:<ul><li>0 = Niedrig</li><li>999 = Hoch</li></ul>Für Aktivitäten, die in früheren Versionen von [!DNL Target Standard/Premium] erstellt wurden, wird [!UICONTROL Low] Priorität in 0, [!UICONTROL Medium] Priorität in 5 und [!UICONTROL High] Priorität in 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.<P>**Hinweis**: Bevor Sie diese Option nach der Verwendung von feinkörnigen Prioritäten deaktivieren können, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden. |
   | [!UICONTROL Duration] | Legen Sie Start- und Enddatum für die Aktivität fest. Sie können [!UICONTROL When Activated] auswählen oder ein bestimmtes Datum und eine bestimmte Uhrzeit angeben. |
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
