---
keywords: Klick-Tracking;Klicks verfolgen;Klicks;AppMeasurement
description: Erfahren Sie, wie Sie mit [!DNL Adobe Target] Klicks auf beliebige Elemente als Erfolgsmetrik verfolgen können.
title: Was ist Klick-Tracking?
feature: Success Metrics
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 60%

---

# Klick-Tracking

[!DNL Adobe Target] ermöglicht Ihnen, Klicks auf beliebige Elemente als Erfolgsmetrik zu verfolgen.

>[!NOTE]
>
>Das Tracking von Klicks wird von der globalen [!DNL Target]-Anfrage nicht unterstützt, wenn sie als Ort in einer formularbasierten Aktivität verwendet wird.

## Klick-Tracking einrichten {#section_5540C5A533114E57BAE022A600B02E72}

1. Wenn Sie die Ziele für Ihre Aktivität auf der Seite [!UICONTROL Ziele und Einstellungen] festlegen, wählen Sie die Erfolgsmetrik **[!UICONTROL Konversion]** aus.
1. Wählen Sie als Aktion **[!UICONTROL Klicks auf ein Element]** aus und klicken Sie anschließend auf **[!UICONTROL Elemente auswählen]**.

   Ihre Seite wird im [!UICONTROL Visual Experience Composer] (VEC) geöffnet.

1. Wählen Sie die Elemente aus, die Sie verfolgen möchten.

   Tipps zur Auswahl von Elementen finden Sie unten im Abschnitt *Zu beachten*.

1. Klicken Sie oben im Bildschirm auf **[!UICONTROL Speichern]** , um Ihre Auswahl zu speichern.

Wenn ein Aktivitätsteilnehmer auf ein ausgewähltes Element klickt, wird dieser Klick als Konversion gezählt.

## Bedienfeld „Ausgewählte Elemente“ {#selected-elements}

Für die Aktivitäten [!UICONTROL A/B-Test], [!UICONTROL Erlebnis-Targeting] (XT), [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Multivarianz-Test] (MVT) werden im Bedienfeld [!UICONTROL Ausgewählte Elemente] die für Klick-Tracking auf der rechten Seite ausgewählten Elemente aufgelistet.

![Bedienfeld „Ausgewählte Elemente“](/help/c-activities/r-success-metrics/assets/selected-elements.png)

Es gibt mehrere Aktionen, die angewendet werden können, wenn Sie den Mauszeiger über ein Element im Bedienfeld [!UICONTROL Ausgewählte Elemente] bewegen. In der folgenden Tabelle werden die einzelnen Aktionen beschrieben, die für ein Element durchgeführt werden können:

| Aktion | Beschreibung |
| --- | --- |
| Informationen | Zeigt den Elementtyp und den vollständigen DOM-Pfad zum Selektor an. |
| Bearbeiten | Ermöglicht die Bearbeitung des CSS-Selektors. |
| Löschen | Löscht das Element. |

### Element hinzufügen

Wenn Sie den DOM-Pfad zum Selektor bereits kennen, können Sie ihn manuell hinzufügen, indem Sie auf das Pluszeichen oben im Bedienfeld klicken.

![Symbol „Element hinzufügen“](/help/c-activities/r-success-metrics/assets/add-element.png)

### Popup für ausgewählte Elemente

Nachdem Sie mehrere Elemente für das Klick-Tracking ausgewählt haben, können Sie den Link [!UICONTROL Ausgewählte Elemente] im Aktivitätsschritt [!UICONTROL Ziele und Einstellungen] anklicken, um die vollständige Liste der für das Klick-Tracking ausgewählten Elemente anzuzeigen. Die Liste enthält den vollständigen DOM-Pfad eines jeden Elements, damit Sie überprüfen können, ob das ausgewählte Element für das Klick-Tracking verwendet werden soll.

![Link „Ausgewählte Elemente“](/help/c-activities/r-success-metrics/assets/elements-selected-link.png)

## Zu beachten {#considerations}

Beachten Sie Folgendes, wenn Sie Elemente auswählen:

* Die DOM-Pfad-Funktion steht beim Einrichten des Klick-Tracking zur Verfügung. Wenn Sie auf ein Element auf der Seite klicken, wird das VEC-Optionsmenü angezeigt. Darüber hinaus wird der entsprechende DOM-Pfad unten auf der Seite angezeigt. Sie können den DOM-Pfad verwenden, um Informationen über das ausgewählte Element (Typ, ID und Klasse) schnell anzuzeigen und den DOM-Pfad nach oben oder unten verschieben, um das gewünschte Element auszuwählen.

   ![DOM-Pfad-Illustration](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   Wie beim Erstellen von Erlebnissen in Schritt 1 im Arbeitsablauf für die Aktivitätserstellung können Sie mit der DOM-Pfadauswahl am unteren Seitenrand ein Element auswählen. Wenn Sie ein Element aus dem DOM-Pfad auswählen, wird das entsprechende Element in VEC als „Ausgewählt“ angezeigt. Um die Auswahl eines ausgewählten Elements aufzuheben, können Sie erneut in der DOM-Pfadauswahl auf das Element klicken oder im VEC auf das Feld &quot;Ausgewählt&quot;klicken.

   Weitere Informationen finden Sie unter [Navigate elements using the DOM path (In Elementen über den DOM-Pfad navigieren)](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Visual Experience Composer–Optionen*.

* Sie können eine andere Seite aufrufen, um Klicks auf einer Seite zu verfolgen, auf der Sie möglicherweise keine Inhalte ändern. Diese andere Seite muss mithilfe der   [mehrseitige Funktionen ](/help/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) verwenden und darin implementiert werden  [!DNL at.js] müssen.
* Wenn Sie mehr als ein Element auswählen und ein Teilnehmer auf eines der ausgewählten Elemente klickt, wird der Klick gezählt. Sie können die Elemente getrennt zählen, indem Sie jeweils einzelne Erfolgsmetriken für sie festlegen. Um ein Element durch Klicken auf mehrere Elemente auf einer Seite zu zählen, bearbeiten Sie den CSS-Element-Selektor, um mehrere Elemente abzugleichen.
* Achten Sie darauf, die Ebene des Elements auszuwählen, die Sie verfolgen möchten. Wenn Sie zum Beispiel eine Schaltfläche angeben möchten, achten Sie darauf, den Link und nicht den Schaltflächentext auszuwählen.
* Klickereignisse werden auf derselben Seite des Klicks an [!DNL Target] gesendet.
* Wenn die Klick-Tracking-Metrik die Zielmetrik einer [!UICONTROL Analytics for Target] (A4T)-Aktivität ist, muss der Besucher innerhalb von 60 Sekunden nach dem Laden der Seite auf dieses Element klicken, damit die Metrik verfolgt wird.
* Klick-Tracking funktioniert nicht bei Elementen, in deren Selektoren Escapezeichen enthalten sind, unter anderem die folgenden:

   | Zeichen | Beschreibung |
   |---|---|
   | # | Raute  oder Hash |
   | : | Doppelpunkt |
   | . | Punkt |
   | $ | Dollarzeichen |
   | `[ ]` | Eckige Klammern |

* Wenn Sie [!DNL at.js][!DNL Analytics]-Klick-Tracking und  AppMeasurement verwenden, hebt [!DNL at.js]-Klick-Tracking alle anderen Klick-Ereignishandler auf. Aus diesem Grund wird der AppMeasurement-Klick-Handler niemals ausgeführt.

   [!DNL at.js] behandelt Klick-Tracking auf besondere Art und Weise, wenn das zugrundeliegende Element ein `A`-Tag (Link) oder ein `FORM`-Tag ist.

   Es werden die folgenden Schritte von [!DNL at.js] ausgeführt, wenn das Klick-Tracking-Ereignis zu einem `A`-Tag (Link) oder einem `FORM`-Tag hinzugefügt wird:

   1. `event.preventDefault()` aufrufen

   1. Lösen Sie die [!DNL Target] -Anfrage.

   1. Führen Sie bei [!DNL Target] Anfrage-Erfolgs- oder Fehler-Rückruf das Standardverhalten aus:

      * `A`-Tag (Link): Das Standard-Verhalten ist es, zu der URL zu navigieren, die durch das HREF-Attribut definiert wird.
      * `FORM`-Tag: Das Standard-Verhalten ist es, das Formular zu übermitteln.

   Dieses Standardverhalten kann das Klick-Tracking mit [!DNL Analytics] beeinträchtigen. Wenn Sie [!DNL Analytics] verwenden, sollten Sie sich für das Klick-Tracking auf [!DNL Analytics] und nicht auf [!DNL Target] verlassen.

* Klick-Tracking wird nicht auf Seiten aufgezeichnet, wo die Seite und die Aktivitäts-URL zu unterschiedlichen Präsenzen gehören. Berechtigungen für Unternehmensbenutzer sind eine [!DNL Target Premium]-Funktion. Weitere Informationen finden Sie unter [Enterprise-Benutzerberechtigungen](/help/administrating-target/c-user-management/property-channel/property-channel.md).

* Klick-Tracking-Metriken sind mit keinem bestimmten Erlebnis in einer Aktivität verknüpft.

* Verwenden Sie Zielgruppen, wenn Sie den Umfang der Klick-Tracking-Metriken einschränken müssen.

* Mehrere Aktivitäten können eine Click-Track-Metrik für denselben Selektor definieren. Wenn dies der Fall ist und ein Besucher sich für eine dieser Aktivitäten qualifiziert und auf diesen Selektor klickt, erhöht sich die Klickverfolgungsmetrik für alle zugehörigen Aktivitäten, für die sich der Besucher qualifiziert hat.

## Schulungsvideo {#section_36607204DAE146E3B8E2C609D244EDB1}

In diesem Video sind Informationen zur Erstellung von Klick-Tracking-Erfolgsmetriken enthalten.

* Erläuterung von „Zielmetriken“
* Metriken für [!UICONTROL Konversion], [!UICONTROL Umsatz] und [!UICONTROL Interaktion]
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
