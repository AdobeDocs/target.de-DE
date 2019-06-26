---
description: Mit Target können Sie Klicks auf beliebige Elemente, etwa Erfolgsmetriken, erfassen.
keywords: Klick-Tracking;Klicks verfolgen;Klicks;AppMeasurement
seo-description: Mit Target können Sie Klicks auf beliebige Elemente, etwa Erfolgsmetriken, erfassen.
seo-title: Klick-Tracking
solution: Target
subtopic: Erste Schritte
title: Klick-Tracking
topic: Standard
uuid: 4a8fbb23-93d8-49f3-aca3-dbbdd6da0178
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Klick-Tracking{#click-tracking}

Mit Target können Sie Klicks auf beliebige Elemente, etwa Erfolgsmetriken, erfassen.

>[!NOTE]
>
>Das Tracking von Klicks wird in globalen Target-Mboxes nicht unterstützt, wenn sie als Standort in formularbasierten Aktivitäten verwendet werden.

## Setting Up click tracking {#section_5540C5A533114E57BAE022A600B02E72}

1. Wenn Sie die Ziele für Ihre Aktivität auf der Seite [!UICONTROL Ziele und Einstellungen] festlegen, wählen Sie die Erfolgsmetrik **[!UICONTROL Konversion]aus.**
1. Wählen Sie als Aktion **[!UICONTROL Klicks auf ein Element]** aus und klicken Sie anschließend auf **[!UICONTROL Elemente auswählen]**.

   Ihre Seite wird im [!UICONTROL Visual Experience Composer] (VEC) geöffnet.

1. Wählen Sie die Elemente aus, die Sie verfolgen möchten.

   Tipps zur Auswahl von Elementen finden Sie unten im Abschnitt „Zu beachten“.

1. Klicken Sie auf das Häkchen oben auf dem Bildschirm, um Ihre Auswahl zu speichern.

Wenn ein Aktivitätsteilnehmer auf ein ausgewähltes Element klickt, wird dieser Klick als Konversion gezählt.

## Selected Elements panel {#selected-elements}

For A/B Test, Experience Targeting (XT), Automated Personalization (AP), and Multivariate Test (MVT) activities, a [!UICONTROL Selected Elements] panel lists all of the selected elements for click tracking on the right side.

![Bedienfeld &quot;Ausgewählte Elemente «](/help/c-activities/r-success-metrics/assets/selected-elements.png)

There are a several actions that can be applied when you hover over an element in the [!UICONTROL Selected Elements] panel. Die folgende Tabelle beschreibt die einzelnen Aktionen, die für ein Element durchgeführt werden können:

| Aktion | Beschreibung |
| --- | --- |
| Informationen | Zeigt den Elementtyp und den vollständigen DOM-Pfad zum Selektor an. |
| Bearbeiten | Ermöglicht die Bearbeitung des CSS-Selektors. |
| Löschen | Löscht das Element. |

### Element hinzufügen

Wenn Sie den DOM-Pfad zum Selektor bereits kennen, können Sie ihn manuell hinzufügen, indem Sie auf das Pluszeichen oben im Bedienfeld klicken.

![Symbol &quot;Element hinzufügen «](/help/c-activities/r-success-metrics/assets/add-element.png)

### Popup zum Hover ausgewählt

After selecting multiple elements for click tracking, you can click the [!UICONTROL Elements Selected] link on the activity&#39;s [!UICONTROL Goals &amp; Settings] step to see the full list of elements selected for click tracking. Die Liste enthält den vollständigen DOM-Pfad für das Element, damit Sie überprüfen können, ob das ausgewählte Element für die Klick-Tracking verwendet werden soll.

![Link &quot;Elemente ausgewählt «](/help/c-activities/r-success-metrics/assets/elements-selected-link.png)

## Zu beachten {#considerations}

Beachten Sie Folgendes, wenn Sie Elemente auswählen:

* Die DOM-Pfad-Funktion steht beim Einrichten des Klick-Tracking zur Verfügung. Wenn Sie auf ein Element auf der Seite klicken, wird das VEC-Optionsmenü angezeigt. Darüber hinaus wird der entsprechende DOM-Pfad unten auf der Seite angezeigt. Sie können den DOM-Pfad verwenden, um Informationen über das ausgewählte Element (Typ, ID und Klasse) schnell anzuzeigen und den DOM-Pfad nach oben oder unten verschieben, um das gewünschte Element auszuwählen.

   ![DOM-Pfad-Illustration](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   Wie beim Erstellen von Erlebnissen in Schritt 1 im Arbeitsablauf für die Aktivitätserstellung können Sie mit der DOM-Pfadauswahl am unteren Seitenrand ein Element auswählen. Wenn Sie ein Element aus dem DOM-Pfad auswählen, wird das entsprechende Element in VEC als „Ausgewählt“ angezeigt. Um die Auswahl eines ausgewählten Elements aufzuheben, können Sie erneut auf das Element in der DOM-Pfadauswahl klicken oder im VEC auf das Feld „Ausgewählt“ klicken.

   Weitere Informationen finden Sie unter [Navigate elements using the DOM path (In Elementen über den DOM-Pfad navigieren)](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Visual Experience Composer–Optionen*.

* Sie können eine andere Seite aufrufen, um Klicks auf einer Seite zu verfolgen, auf der Sie möglicherweise keine Inhalte ändern. Diese andere Seite muss mithilfe der [Mehrseiten-Funktion](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) in die Aktivität aufgenommen werden, und [!DNL at.js] oder [!DNL mbox.js] muss darin implementiert werden.
* Wenn Sie mehr als ein Element auswählen und ein Teilnehmer auf eines der ausgewählten Elemente klickt, wird der Klick gezählt. Sie können die Elemente getrennt zählen, indem Sie jeweils einzeln Erfolgsmetriken für sie festlegen.
* Achten Sie darauf, die Ebene des Elements auszuwählen, die Sie verfolgen möchten. Wenn Sie zum Beispiel eine Schaltfläche angeben möchten, achten Sie darauf, den Link und nicht den Schaltflächentext auszuwählen.
* Klickereignisse werden auf derselben Seite des Klicks an [!DNL Target] gesendet.
* Wenn es sich bei der Klick-Verfolgungsmetrik um die Zielmetrik einer A4T-Aktivität handelt, muss der Besucher innerhalb von 60 Sekunden nach dem Laden der Seite auf dieses Element klicken, damit die Metrikverfolgung erfolgt.
* Klick-Tracking funktioniert nicht bei Elementen, in deren Selektoren Escapezeichen enthalten sind, unter anderem die folgenden:

   | Zeichen | Beschreibung |
   |---|---|
   | # | Raute oder Hash |
   | : | Doppelpunkt |
   | . | Zeitraum |
   | $ | Dollarzeichen |
   | `[ ]` | Eckige Klammern |

* Wenn Sie [!DNL at.js]-Klick-Tracking und Analytics AppMeasurement verwenden, hebt [!DNL at.js]-Klick-Tracking alle anderen Klick-Ereignishandler auf. Aus diesem Grund wird der AppMeasurement-Klick-Handler niemals ausgeführt.

   [!DNL at.js] behandelt Klick-Tracking auf besondere Art und Weise, wenn das zugrundeliegende Element ein `A`-Tag (Link) oder ein `FORM`-Tag ist.

   Es werden die folgenden Schritte von [!DNL at.js] ausgeführt, wenn das Klick-Tracking-Ereignis zu einem `A`-Tag (Link) oder einem `FORM`-Tag hinzugefügt wird:

   1. `event.preventDefault()` aufrufen

   1. Target-Anfrage absenden

   1. Nach erfolgreicher Target-Anfrage oder nach „error“-Rückruf wird ein Standard-Verhalten ausgeführt:

      * `A`-Tag (Link): Das Standard-Verhalten ist es, zu der URL zu navigieren, die durch das HREF-Attribut definiert wird.
      * `FORM`-Tag: Das Standard-Verhalten ist es, das Formular zu übermitteln.
   Bei diesem Standardverhalten kommt es möglicherweise zu Konflikten mit Analytics-Klick-Tracking. Wenn Sie Analytics verwenden, sollten Sie das Klick-Tracking über Analytics ausführen, und nicht über Target.

* Klick-Tracking wird nicht auf Seiten aufgezeichnet, wo die Seite und die Aktivitäts-URL zu unterschiedlichen Präsenzen gehören. Berechtigungen für Unternehmensbenutzer sind eine Target Premium-Funktion. Weitere Informationen finden Sie unter [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md).

## Schulungsvideo {#section_36607204DAE146E3B8E2C609D244EDB1}

In diesem Video sind Informationen zur Erstellung von Klick-Tracking-Erfolgsmetriken enthalten.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktion
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380?captions=ger)