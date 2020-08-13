---
keywords: template testing;template;same experience on similar pages;template test
description: Wenn Sie die Struktur Ihrer Seite mithilfe einer Seitenvorlage erstellen oder wenn Ihre Seite ähnliche Elemente enthält, können Sie mithilfe dieser Funktion Variationen in ähnlich strukturierten Seitenelementen testen.
title: Gleiches Erlebnis auf ähnlichen Seiten
feature: experiences
uuid: 055b276e-2492-40d8-b48e-849dffa93f35
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 96%

---


# Gleiches Erlebnis auf ähnlichen Seiten{#include-the-same-experience-on-similar-pages}

Wenn Sie die Struktur Ihrer Seite mithilfe einer Seitenvorlage erstellen oder wenn Ihre Seite ähnliche Elemente enthält, können Sie mithilfe dieser Funktion Variationen in ähnlich strukturierten Seitenelementen testen.

Damit diese Funktion korrekt ausgeführt wird, muss sie auf Seiten mit einer sehr ähnlichen Struktur verwendet werden oder Vorlagenelemente, die auf allen Seiten gleich strukturiert sind, enthalten.

>[!IMPORTANT]
>
>Diese Funktion verursacht wahrscheinlich unerwartete Ergebnisse, wenn Sie sie zum Ändern von Elementen auf Seiten verwenden, die sich nicht ähnlich sind.

Sie können diese Funktion zum Beispiel zum Durchführen einer der folgenden Aktivitäten verwenden:

* Testen einer globalen Navigationsleiste durch Neuanordnen oder Entfernen von Elementen
* Entfernen eines Elements aus allen Produktseiten, die eine bestimmte Seitenvorlage verwenden
* Hinzufügen eines Banners zu allen Produktseiten
* Ändern des Layouts der Artikelvorlage

Im folgenden Informationsvideo erfahren Sie mehr dazu, wie Sie Vorlagen nutzen:

Sie können Seiten angeben, die die Änderungselemente enthalten, oder die Änderung auf Ihre gesamte Site anwenden.

1. Erstellen Sie eine Aktivität wie in [Aktivitäten](../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) beschrieben.
1. Um die Seiten anzugeben, auf denen das Erlebnis angezeigt werden soll, klicken Sie im Visual Experience Composer auf das Zahnradsymbol und wählen Sie **[!UICONTROL Bereitstellung der Seite]** aus.
1. Klicken Sie auf **[!UICONTROL Vorlagenregel hinzufügen]** und geben Sie dann die Kriterien für die Seiten an, zu denen Sie das Erlebnis hinzufügen möchten.

1. Legen Sie den Seitenbereich fest. Der Seitenbereich kann einer der folgenden sein:

   * URL (For more information about how Target evaluates URLs, see [Targets and audiences FAQ](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * Domäne
   * Pfad
   * Hashfragment (#) (Nehmen Sie ein Targeting auf den Teil der URL vor, der auf das #-Symbol folgt.)
   * Abfrage
   * Parameter

1. Wählen Sie einen Operator aus.

   Der Operator gibt an, in welcher Beziehung die Elemente nach dem Operator zum Seitenbereich stehen. Die verfügbaren Operatoren sind:

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
   >Mehrere Elemente verwenden die `OR`-Logik, was bedeutet, dass jedes einzelne Element in der Liste die Bedingung wahr macht.

1. Geben Sie bei Bedarf zusätzliche Kriterien ein, indem Sie auf **[!UICONTROL Vorlagenregel hinzufügen]** klicken und die Vorgehensweise aus dem vorherigen Schritt wiederholen.

   Mehrere Kriterien werden mit der UND-Logik verbunden. Adobe Target fügt das Erlebnis zu allen Seiten hinzu, die den angegebenen Kriterien entsprechen.

>[!IMPORTANT]
>
> Target kann die Seiten nicht überprüfen, um sicherzustellen, dass sie wie erwartet angezeigt werden. Wenn Sie diese Funktion verwenden, sollten Sie daher die betroffenen Seiten immer testen, bevor Sie sie veröffentlichen.

## Schulungsvideo: Visual Experience Composer (2 von 2) (7:29) ![Tutorialzeichen](/help/assets/tutorial.png)

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)