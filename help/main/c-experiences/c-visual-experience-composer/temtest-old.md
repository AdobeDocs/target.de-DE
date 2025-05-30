---
keywords: Vorlagentests;Vorlage;gleiches Erlebnis auf ähnlichen Seiten;Vorlagentest
description: Erfahren Sie, wie Sie mit dem Adobe [!DNL Target] Visual Experience Composer (VEC) dasselbe Erlebnis auf mehreren Seiten einbinden können, die ähnlich strukturiert sind oder dieselben Vorlagenelemente enthalten.
title: Kann ich dasselbe Erlebnis auf ähnlichen Seiten verwenden?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 34%

---

# Gleiches Erlebnis auf ähnlichen Seiten

Verwenden Sie eine Seitenvorlage in [!DNL Adobe Target], um Ihren Seiten eine Struktur zu verleihen, oder wenn Ihre Seiten ähnliche Elemente enthalten, um Varianzen in ähnlich strukturierten Seitenelementen oder in Ihrer gesamten Domain zu testen.

Damit sie ordnungsgemäß funktionieren, muss diese Funktion auf Seiten mit ähnlicher Struktur verwendet werden oder Vorlagenelemente enthalten, die auf allen Seiten gleich strukturiert sind.

>[!IMPORTANT]
>
>Diese Funktion verursacht wahrscheinlich unerwartete Ergebnisse, wenn Sie sie zum Ändern von Elementen auf Seiten verwenden, die sich nicht ähnlich sind.

Sie können diese Funktion zum Beispiel zum Durchführen einer der folgenden Aktivitäten verwenden:

* Testen einer globalen Navigationsleiste durch Neuanordnen oder Entfernen von Elementen
* Entfernen eines Elements aus allen Produktseiten, die eine bestimmte Seitenvorlage verwenden
* Hinzufügen eines Banners zu allen Produktseiten
* Ändern des Layouts der Artikelvorlage

Sie können Seiten angeben, die die Änderungselemente enthalten, oder die Änderung auf Ihre Site oder Domain anwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) beschrieben.

1. Um die Seiten anzugeben, auf denen das Erlebnis angezeigt werden soll, klicken Sie im [!UICONTROL Visual Experience Composer] (VEC) auf das Zahnradsymbol und wählen Sie dann **[!UICONTROL Page Delivery]** aus.

   ![Zahnradsymbol > Seitenbereitstellung](/help/main/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Klicken Sie auf **[!UICONTROL Add Template Rule]** und geben Sie dann die Kriterien für die Seiten an, denen Sie das Erlebnis hinzufügen möchten.

1. Legen Sie den Seitenbereich fest. Der Seitenbereich kann einer der folgenden sein:

   * URL (Weitere Informationen zum Auswerten von URLs durch Target finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)).
   * Domain
   * Pfad
   * Fragment mit Hash-Wert (#) (Zielgruppe ist der Teil einer URL, der dem #-Symbol folgt.)
   * Abfrage
   * Parameter

1. Wählen Sie einen Operator aus.

   Der Operator gibt an, in welcher Beziehung die Elemente nach dem Operator zum Seitenbereich stehen. Zu den verfügbaren Operatoren gehören:

   * Enthält
   * Enthält nicht
   * Ist (Groß- und Kleinschreibung berücksichtigen)
   * Ist nicht
   * Beginnt mit
   * Endet mit

1. Geben Sie die Zeichenfolge ein, über die definiert wird, wo das Erlebnis hinzugefügt wird, wie die Domain oder die im Seitennamen enthaltenen Zeichenfolgen.

   Wenn Sie beispielsweise **[!UICONTROL Domain]** und **[!UICONTROL Is (case sensitive)]** auswählen, geben Sie die Domain ein, zu der das Erlebnis zu allen Seiten hinzugefügt werden soll.

   Sie können mehrere Elemente hinzufügen.

   >[!IMPORTANT]
   >
   >Mehrere Elemente verwenden die OR-Logik, d. h. jedes einzelne Element in der Liste macht die Bedingung wahr.

1. Geben Sie bei Bedarf zusätzliche Kriterien ein, indem Sie auf **[!UICONTROL Add Template Rule]** klicken und den Vorgang in den vorherigen Schritten wiederholen.

   Mehrere Kriterien werden mit der UND-Logik verbunden. [!DNL Target] fügt das Erlebnis allen Seiten hinzu, die den angegebenen Kriterien entsprechen.

>[!IMPORTANT]
>
> [!DNL Target] können die Seiten nicht überprüfen, um sicherzustellen, dass sie wie erwartet angezeigt werden. Daher ist es immer eine wichtige Praxis, wenn Sie diese Funktion verwenden, um betroffene Seiten zu testen, bevor Sie sie veröffentlichen.

## Anwendungsbeispiele

Überprüfen Sie die folgenden Anwendungsfälle, um zu erfahren, wie Sie Vorlagenregeln auf Ihrer Site verwenden können:

### Dieselbe Aktivität für die gesamte Domain rendern

Sie können in Erwägung ziehen, Vorlagenregeln zu verwenden, um dieselbe Aktivität in Ihrer gesamten Domain für die folgenden Anwendungsfälle zu rendern:

* Einschließen einer globalen Kopf- oder Fußzeile
* So fügen Sie ein globales Banner hinzu (z. B. COVID-19-Ankündigungen)
* Um eine globale Versandkostenabo aufzunehmen

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) beschrieben.

1. Um die Domain anzugeben, in der das Erlebnis angezeigt werden soll, klicken Sie in Visual Experience Composer auf das Zahnradsymbol und wählen Sie dann **[!UICONTROL Page Delivery]** aus.

1. Klicken Sie auf **[!UICONTROL Add Template Rule]** > **[!UICONTROL Domain]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Choose evaluator]** die Option **[!UICONTROL Contains]** aus und geben Sie dann die Domain an.

   ![Domain enthält](/help/main/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Schulungsvideo: Visual Experience Composer (2 von 2) (7:29) ![Tutorial-Badge](/help/main/assets/tutorial.png)

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/30166?captions=ger)
