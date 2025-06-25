---
keywords: Klick-Tracking;Klicks verfolgen;Klicks;AppMeasurement
description: Erfahren Sie, wie Sie mit  [!DNL Adobe Target]  Klicks auf beliebige Elemente als Erfolgsmetrik verfolgen können.
title: Was ist Klick-Tracking?
feature: Success Metrics
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: 43d2484e57b1e2d292cf65c041fb9f5f49b2084c
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 75%

---

# Klick-Tracking

[!DNL Adobe Target] können Sie Klicks auf beliebige Elemente als Erfolgsmetrik verfolgen. Klick-Tracking bezieht sich auf den Prozess der Überwachung und Aufzeichnung von Benutzerinteraktionen, insbesondere Klicks auf Elemente innerhalb einer Web-Seite oder eines Erlebnisses. Dies ist ein wichtiger Bestandteil zur Messung der Interaktion und Leistung bei A/B-Tests, multivariaten Tests und Personalisierungsaktivitäten.

>[!NOTE]
>
>Das Tracking von Klicks wird bei der globalen [!DNL Target]-Anfrage bei Verwendung als Standort in einer formularbasierten Aktivität nicht unterstützt.

## Klick-Tracking einrichten {#section_5540C5A533114E57BAE022A600B02E72}

1. Wenn Sie die Ziele für Ihre Aktivität auf der Seite [!UICONTROL Goals & Settings] festlegen, wählen Sie die Erfolgsmetrik **[!UICONTROL Conversion]** aus.
1. Wählen Sie als Aktion **[!UICONTROL Clicked an element]** aus und klicken Sie dann auf **[!UICONTROL Select elements]**.

   Ihre Seite wird im [!UICONTROL Visual Experience Composer] (VEC) geöffnet.

1. Wählen Sie die Elemente aus, die Sie verfolgen möchten.

   Tipps zur Auswahl von Elementen finden Sie unten im Abschnitt *Zu beachten*.

1. Klicken Sie oben auf dem Bildschirm auf **[!UICONTROL Done]** , um Ihre Auswahl zu speichern.

Wenn ein Aktivitätsteilnehmer auf ein ausgewähltes Element klickt, wird dieser Klick als Konversion gezählt.

## Bedienfeld „Ausgewählte Elemente“ {#selected-elements}

Bei [!UICONTROL A/B Test]-, [!UICONTROL Experience Targeting]- (XT), [!UICONTROL Automated Personalization]- (AP) und [!UICONTROL Multivariate Test]-(MVT)-Aktivitäten werden im [!UICONTROL Selected Elements] die für das Klick-Tracking ausgewählten Elemente auf der linken Seite aufgelistet.

![Bedienfeld „Ausgewählte Elemente“](/help/main/c-activities/r-success-metrics/assets/selected-elements.png)

Es gibt mehrere Aktionen, die ausgeführt werden können, wenn Sie auf ein Element im [!UICONTROL Tracked Components] klicken. In der folgenden Tabelle werden die einzelnen Aktionen beschrieben, die für ein Element durchgeführt werden können:

| Aktion | Beschreibung |
| --- | --- |
| [!UICONTROL Tracked actions] | Zeigt die Elementaktion an. |
| [!UICONTROL CSS selector] | Ermöglicht die Bearbeitung des CSS-Selektors. |
| [!DNL Delete] | Löscht das Element. |

### Element hinzufügen

Wenn Sie den DOM-Pfad zum Selektor bereits kennen, können Sie ihn manuell hinzufügen, indem Sie auf das [!UICONTROL Add Component] oben im Bedienfeld klicken.

## Zu beachten {#considerations}

Beachten Sie Folgendes, wenn Sie Elemente auswählen:

* Die DOM-Pfad-Funktion steht beim Einrichten des Klick-Tracking zur Verfügung. Wenn Sie auf ein Element auf der Seite klicken, wird das VEC-Optionsmenü angezeigt. Darüber hinaus wird der entsprechende DOM-Pfad unten auf der Seite angezeigt. Sie können den DOM-Pfad verwenden, um Informationen über das ausgewählte Element (Typ, ID und Klasse) schnell anzuzeigen und den DOM-Pfad nach oben oder unten verschieben, um das gewünschte Element auszuwählen.

  Wie beim Erstellen von Erlebnissen in Schritt 1 im Arbeitsablauf für die Aktivitätenerstellung können Sie mit der DOM-Pfadauswahl am unteren Seitenrand ein Element auswählen. Wenn Sie ein Element aus dem DOM-Pfad auswählen, wird das entsprechende Element in VEC als „Ausgewählt“ angezeigt. Um die Auswahl eines ausgewählten Elements aufzuheben, können Sie erneut auf das Element in der DOM-Pfadauswahl klicken oder im VEC auf das Feld „Ausgewählt“ klicken.

  Weitere Informationen finden Sie unter [Navigate elements using the DOM path (In Elementen über den DOM-Pfad navigieren)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Visual Experience Composer–Optionen*.

* Sie können eine andere Seite aufrufen, um Klicks auf einer Seite zu verfolgen, auf der Sie möglicherweise keine Inhalte ändern. Diese andere Seite muss mithilfe der [Mehrseiten-Funktion“ in die Aktivität aufgenommen ](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) und dafür [!DNL at.js] implementiert werden.
* Wenn Sie mehr als ein Element auswählen und ein Teilnehmer auf eines der ausgewählten Elemente klickt, wird der Klick gezählt. Sie können die Elemente getrennt zählen, indem Sie jeweils einzelne Erfolgsmetriken für sie festlegen. Wenn nur ein einzelnes Element gezählt werden soll, obwohl auf mehrere Elemente der Seite geklickt wird, müssen Sie dem CSS-Element-Selektor mehrere Elemente zuordnen.
* Achten Sie darauf, die Ebene des Elements auszuwählen, die Sie verfolgen möchten. Wenn Sie zum Beispiel eine Schaltfläche angeben möchten, achten Sie darauf, den Link und nicht den Schaltflächentext auszuwählen.
* Klickereignisse werden auf derselben Seite des Klicks an [!DNL Target] gesendet.
* Wenn es sich bei der Klick-Tracking-Metrik um die Zielmetrik einer [!UICONTROL Analytics for Target] (A4T)-Aktivität handelt, muss der Besucher innerhalb von 60 Sekunden nach dem Laden der Seite auf dieses Element klicken, damit das Metrik-Tracking erfolgt.
* Klick-Tracking funktioniert nicht bei Elementen, in deren Selektoren Escapezeichen enthalten sind, unter anderem die folgenden:

  | Zeichen | Beschreibung |
  |---|---|
  | # | Nummernzeichen oder Hash |
  | : | Doppelpunkt |
  | . | Punkt |
  | $ | Dollarzeichen |
  | `[ ]` | Eckige Klammern |

* Wenn Sie [!DNL at.js]-Klick-Tracking und [!DNL Analytics]-AppMeasurement verwenden, hebt [!DNL at.js]-Klick-Tracking alle anderen Klick-Ereignishandler auf. Aus diesem Grund wird der AppMeasurement-Klick-Handler niemals ausgeführt.

  [!DNL at.js] behandelt Klick-Tracking auf besondere Art und Weise, wenn das zugrundeliegende Element ein `A`-Tag (Link) oder ein `FORM`-Tag ist.

  Es werden die folgenden Schritte von [!DNL at.js] ausgeführt, wenn das Klick-Tracking-Ereignis zu einem `A`-Tag (Link) oder einem `FORM`-Tag hinzugefügt wird:

   1. `event.preventDefault()` aufrufen

   1. Lösen Sie die [!DNL Target]-Anfrage aus.

   1. Nach erfolgreicher [!DNL Target]-Anfrage oder nach „error“-Rückruf wird ein Standardverhalten ausgeführt:

      * `A`-Tag (Link): Das Standard-Verhalten ist es, zu der URL zu navigieren, die durch das HREF-Attribut definiert wird.
      * `FORM`-Tag: Das Standard-Verhalten ist es, das Formular zu übermitteln.

  Bei diesem Standardverhalten kommt es möglicherweise zu Konflikten mit [!DNL Analytics]-Klick-Tracking. Wenn Sie [!DNL Analytics] verwenden, sollten Sie das Klick-Tracking über [!DNL Analytics] ausführen statt über [!DNL Target].

* Klick-Tracking wird nicht auf Seiten aufgezeichnet, wo die Seite und die Aktivitäts-URL zu unterschiedlichen Präsenzen gehören. Berechtigungen für Unternehmensbenutzer sind eine [!DNL Target Premium]-Funktion. Weitere Informationen finden Sie unter [Enterprise-Benutzerberechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

* Klick-Tracking-Metriken sind mit keinem bestimmten Erlebnis in einer Aktivität verknüpft.

* Verwenden Sie Zielgruppen, wenn Sie den Umfang der Klick-Tracking-Metriken einschränken müssen.

* Mehrere Aktivitäten können eine Click-Tracking-Metrik für denselben Selektor definieren. Wenn dies der Fall ist und ein Besucher sich für eine dieser Aktivitäten qualifiziert und auf diesen Selektor klickt, erhöht sich die Klick-Tracking-Metrik für alle zugehörigen Aktivitäten, für die der Besucher qualifiziert ist.

## Schulungsvideo {#section_36607204DAE146E3B8E2C609D244EDB1}

In diesem Video sind Informationen zur Erstellung von Klick-Tracking-Erfolgsmetriken enthalten.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von [!UICONTROL Conversion], [!UICONTROL Revenue] und [!UICONTROL Engagement] Metriken
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
