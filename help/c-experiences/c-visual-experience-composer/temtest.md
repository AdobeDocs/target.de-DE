---
keywords: Vorlagentests;Vorlage;gleiches Erlebnis auf ähnlichen Seiten;Vorlagentest
description: Verwenden Sie eine Seitenvorlage in Adobe Target, um eine Struktur für Ihre Seiten bereitzustellen oder wenn Ihre Seiten ähnliche Elemente enthalten, um Variationen in ähnlich strukturierten Seitenelementen zu testen.
title: Gleiches Erlebnis auf ähnlichen Seiten
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 47%

---


# Gleiches Erlebnis auf ähnlichen Seiten

Verwenden Sie eine Seitenvorlage in [!DNL Adobe Target], um eine Struktur für Ihre Seiten bereitzustellen oder wenn Ihre Seiten ähnliche Elemente enthalten, um Variationen in ähnlich strukturierten Seitenelementen oder in Ihrer gesamten Domäne zu testen.

Damit diese Funktion korrekt ausgeführt werden kann, muss sie auf Seiten mit einer ähnlichen Struktur oder Vorlagenelementen verwendet werden, die auf allen Seiten gleich strukturiert sind.

>[!IMPORTANT]
>
>Diese Funktion verursacht wahrscheinlich unerwartete Ergebnisse, wenn Sie sie zum Ändern von Elementen auf Seiten verwenden, die sich nicht ähnlich sind.

Sie können diese Funktion zum Beispiel zum Durchführen einer der folgenden Aktivitäten verwenden:

* Testen einer globalen Navigationsleiste durch Neuanordnen oder Entfernen von Elementen
* Entfernen eines Elements aus allen Produktseiten, die eine bestimmte Seitenvorlage verwenden
* Hinzufügen eines Banners zu allen Produktseiten
* Ändern des Layouts der Artikelvorlage

Sie können Seiten angeben, die die Änderungselemente enthalten, oder die Änderung auf Ihre Website oder Domäne anwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität, wie unter [Aktivitäten](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) beschrieben.

1. Um die Seiten anzugeben, auf denen das Erlebnis angezeigt wird, klicken Sie im Ordner [!UICONTROL Visual Experience Composer] (VEC) auf das Zahnradsymbol und wählen Sie **[!UICONTROL Versand]**.

   ![Zahnradsymbol > Seiten-Versand](/help/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]** und geben Sie dann die Kriterien für die Seiten an, zu denen Sie das Erlebnis hinzufügen möchten.

1. Legen Sie den Seitenbereich fest. Der Seitenbereich kann einer der folgenden sein:

   * URL (Weitere Informationen zur Bewertung von URLs durch die Zielgruppe finden Sie unter [Häufig gestellte Fragen zu Zielgruppen und Audiencen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * Domäne
   * Pfad
   * Hashfragment (#) (Zielgruppe des Teils einer URL, der auf das #-Symbol folgt)
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

1. Geben Sie die Zeichenfolge ein, über die definiert wird, wo das Erlebnis hinzugefügt wird, wie die Domäne oder die im Seitennamen enthaltenen Zeichenfolgen.

   Wenn Sie beispielsweise **[!UICONTROL Domäne]** und **[!UICONTROL Ist (Groß- und Kleinschreibung berücksichtigen)]** auswählen, geben Sie die Domäne ein, in der das Erlebnis zu allen Seiten hinzugefügt werden soll.

   Sie können mehrere Elemente hinzufügen.

   >[!IMPORTANT]
   >
   >Mehrere Elemente verwenden die OR-Logik, d. h., ein einzelnes Element in der Liste macht die Bedingung wahr.

1. Geben Sie bei Bedarf zusätzliche Kriterien ein, indem Sie auf **[!UICONTROL Hinzufügen Vorlagenregel]** klicken und das Verfahren in den vorherigen Schritten wiederholen.

   Mehrere Kriterien werden mit der UND-Logik verbunden. [!DNL Target] fügt das Erlebnis zu allen Seiten hinzu, die den angegebenen Kriterien entsprechen.

>[!IMPORTANT]
>
> [!DNL Target] kann die Seiten nicht überprüfen, um sicherzustellen, dass sie wie erwartet angezeigt werden. Wenn Sie diese Funktion verwenden, sollten Sie daher die betroffenen Seiten immer testen, bevor Sie sie veröffentlichen.

## Anwendungsbeispiele

Sehen Sie sich die folgenden Anwendungsfälle an, um Möglichkeiten zur Verwendung von Vorlagenregeln auf Ihrer Site zu finden:

### Derselbe Aktivität über die gesamte Domäne rendern

In den folgenden Anwendungsfällen sollten Sie die gleiche Aktivität in Ihrer gesamten Domäne mit Vorlagenregeln wiedergeben:

* So fügen Sie eine globale Kopf- oder Fußzeile ein
* So fügen Sie ein globales Banner ein (z. B. COVID-19-Mitteilungen)
* So fügen Sie eine globale kostenlose Promo bei

1. Erstellen oder bearbeiten Sie eine Aktivität, wie unter [Aktivitäten](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) beschrieben.

1. Um die Domäne anzugeben, in der das Erlebnis angezeigt werden soll, klicken Sie im Visual Experience Composer auf das Zahnradsymbol und wählen Sie **[!UICONTROL Versand]**.

1. Klicken Sie auf **[!UICONTROL Hinzufügen Vorlagenregel]** > **[!UICONTROL Domäne]**.

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Auswerter auswählen]** die Option **[!UICONTROL Enthält]** und geben Sie dann die Domäne an.

   ![Domäne enthält](/help/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Schulungsvideo: Visual Experience Composer (2 von 2) (7:29) ![Tutorial badge](/help/assets/tutorial.png)

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)