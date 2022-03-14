---
keywords: Vorlagentests;Vorlage;gleiches Erlebnis auf ähnlichen Seiten;Vorlagentest
description: Erfahren Sie, wie Sie die Adobe verwenden [!DNL Target] Visual Experience Composer (VEC) verwenden, um dasselbe Erlebnis auf mehreren Seiten einzubeziehen, die ähnlich strukturiert sind oder dieselben Vorlagenelemente enthalten.
title: Kann ich dasselbe Erlebnis auf ähnlichen Seiten einbeziehen?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 45%

---

# Gleiches Erlebnis auf ähnlichen Seiten

Verwenden Sie eine Seitenvorlage in [!DNL Adobe Target] , um eine Struktur für Ihre Seiten bereitzustellen oder wenn Ihre Seiten ähnliche Elemente enthalten, Variationen in ähnlich strukturierten Seitenelementen oder in der gesamten Domäne zu testen.

Damit diese Funktion ordnungsgemäß funktioniert, muss sie auf Seiten mit einer ähnlichen Struktur verwendet werden oder Vorlagenelemente enthalten, die auf allen Seiten gleich strukturiert sind.

>[!IMPORTANT]
>
>Diese Funktion verursacht wahrscheinlich unerwartete Ergebnisse, wenn Sie sie zum Ändern von Elementen auf Seiten verwenden, die sich nicht ähnlich sind.

Sie können diese Funktion zum Beispiel zum Durchführen einer der folgenden Aktivitäten verwenden:

* Testen einer globalen Navigationsleiste durch Neuanordnen oder Entfernen von Elementen
* Entfernen eines Elements aus allen Produktseiten, die eine bestimmte Seitenvorlage verwenden
* Hinzufügen eines Banners zu allen Produktseiten
* Ändern des Layouts der Artikelvorlage

Sie können Seiten angeben, die die Änderungselemente enthalten, oder die Änderung auf Ihre Site oder Domäne anwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Tätigkeiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. So legen Sie die Seiten fest, auf denen das Erlebnis angezeigt wird, im [!UICONTROL Visual Experience Composer] (VEC) Klicken Sie auf das Zahnradsymbol und wählen Sie **[!UICONTROL Seitenbereitstellung]**.

   ![Zahnradsymbol > Seitenbereitstellung](/help/main/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]** und geben Sie dann die Kriterien für die Seiten an, zu denen Sie das Erlebnis hinzufügen möchten.

1. Legen Sie den Seitenbereich fest. Der Seitenbereich kann einer der folgenden sein:

   * URL (Weitere Informationen zur Bewertung von URLs durch Target finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).
   * Domain
   * Pfad
   * Hash-Fragment (#) (Targeting des Teils einer URL, der auf das #-Symbol folgt)
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

   Wenn Sie beispielsweise **[!UICONTROL Domain]** und **[!UICONTROL Ist (Groß- und Kleinschreibung berücksichtigen)]** auswählen, geben Sie die Domain ein, in der das Erlebnis zu allen Seiten hinzugefügt werden soll.

   Sie können mehrere Elemente hinzufügen.

   >[!IMPORTANT]
   >
   >Mehrere Elemente verwenden die OR-Logik, d. h., dass jedes einzelne Element in der Liste die Bedingung wahr macht.

1. Geben Sie bei Bedarf zusätzliche Kriterien ein, indem Sie auf **[!UICONTROL Vorlagenregel hinzufügen]** und wiederholen Sie den Vorgang in den vorherigen Schritten.

   Mehrere Kriterien werden mit der UND-Logik verbunden. [!DNL Target] fügt das Erlebnis zu allen Seiten hinzu, die den angegebenen Kriterien entsprechen.

>[!IMPORTANT]
>
> [!DNL Target] kann die Seiten nicht überprüfen, um sicherzustellen, dass sie wie erwartet angezeigt werden. Wenn Sie diese Funktion verwenden, sollten Sie daher die betroffenen Seiten immer testen, bevor Sie sie veröffentlichen.

## Anwendungsbeispiele

In den folgenden Anwendungsfällen finden Sie Möglichkeiten zur Verwendung von Vorlagenregeln auf Ihrer Site:

### dieselbe Aktivität über die gesamte Domäne hinweg wiedergeben

In den folgenden Anwendungsfällen können Sie die Verwendung von Vorlagenregeln in Erwägung ziehen, um dieselbe Aktivität in Ihrer gesamten Domäne wiederzugeben:

* So fügen Sie eine globale Kopf- oder Fußzeile hinzu
* So fügen Sie ein globales Banner hinzu (z. B. COVID-19-Ankündigungen)
* So fügen Sie ein weltweites Angebot für kostenlosen Versand hinzu

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Tätigkeiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Um die Domäne anzugeben, in der das Erlebnis angezeigt wird, klicken Sie im Visual Experience Composer auf das Zahnradsymbol und wählen Sie **[!UICONTROL Seitenbereitstellung]**.

1. Klicken **[!UICONTROL Vorlagenregel hinzufügen]** > **[!UICONTROL Domäne]**.

1. Aus dem **[!UICONTROL Auswerter wählen]** Dropdown-Liste auswählen **[!UICONTROL Enthält]**, und geben Sie dann die Domäne an.

   ![Domäne enthält](/help/main/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Schulungsvideo: Visual Experience Composer (2 von 2) (7:29) ![Tutorial-Badge](/help/main/assets/tutorial.png)

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)
