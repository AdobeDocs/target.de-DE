---
keywords: Vorlagentests;Vorlage;gleiches Erlebnis auf ähnlichen Seiten;Vorlagentest
description: Erfahren Sie, wie Sie mit  [!DNL Target]  Visual Experience Composer (VEC) dasselbe Erlebnis auf mehreren Seiten einbinden können, die ähnlich strukturiert sind oder dieselben Vorlagenelemente enthalten.
title: Kann ich dasselbe Erlebnis auf ähnlichen Seiten verwenden?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
TQID: https://experienceleague.adobe.com/zk7U6g7gk7XkpWsEFQbwuCm7xbpIb1lCaZefxjn-39g
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 564
ht-degree: 23%

---

# Gleiches Erlebnis auf ähnlichen Seiten

Verwenden Sie eine Seitenvorlage in [!DNL Adobe Target], um Ihren Seiten eine Struktur zu verleihen, oder wenn Ihre Seiten ähnliche Elemente enthalten, um Varianzen in ähnlich strukturierten Seitenelementen oder in Ihrer gesamten Domain zu testen.

Damit sie ordnungsgemäß funktionieren, muss diese Funktion auf Seiten mit ähnlicher Struktur verwendet werden oder Vorlagenelemente enthalten, die auf allen Seiten gleich strukturiert sind.

>[!IMPORTANT]
>
>Die Verwendung dieser Funktion zum Ändern von Elementen auf unterschiedlichen Seiten führt wahrscheinlich zu unerwarteten Ergebnissen.

Sie können diese Funktion zum Beispiel zum Durchführen einer der folgenden Aktivitäten verwenden:

* Testen einer globalen Navigationsleiste durch Neuanordnen oder Entfernen von Elementen
* Entfernen eines Elements aus allen Produktseiten, die eine bestimmte Seitenvorlage verwenden
* Hinzufügen eines Banners zu allen Produktseiten
* Layout der Artikelvorlage ändern

Sie können Seiten angeben, die die Änderungselemente enthalten, oder die Änderung auf Ihre Site oder Domain anwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) beschrieben.

1. Um die Seiten anzugeben, auf denen das Erlebnis angezeigt wird, klicken Sie [!UICONTROL Visual Experience Composer] (VEC) auf das Symbol [!UICONTROL Konfigurieren] ( ![Symbol Konfigurieren](/help/main/assets/icons/Setting.svg) ) und wählen Sie dann **[!UICONTROL Seitenbereitstellung]** aus.

1. Klicken Sie **[!UICONTROL Regel hinzufügen]** und geben Sie dann die Kriterien für die Seiten an, denen Sie das Erlebnis hinzufügen möchten.

1. Legen Sie den Seitenbereich fest. Der Seitenbereich kann einer der folgenden sein:

   * [!UICONTROL URL] (Weitere Informationen dazu, wie [!DNL Target] URLs auswertet, finden Sie unter [Häufig gestellte Fragen zu Zielen und ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md))
   * [!UICONTROL Domain]
   * [!UICONTROL path]
   * [!UICONTROL Hash (#)-Fragment] (zielen Sie auf den Teil einer URL, der dem #-Symbol folgt.)
   * [!UICONTROL Abfrage]
   * [!UICONTROL Benutzerspezifisch]

1. Wählen Sie einen Operator aus.

   Der Operator gibt an, in welcher Beziehung die Elemente nach dem Operator zum Seitenbereich stehen. Zu den verfügbaren Operatoren gehören:

   * [!UICONTROL Enthält]
   * [!UICONTROL Enthält nicht]
   * [!UICONTROL Ist (von Schreibweise abhängig)]
   * [!UICONTROL Ist nicht]
   * [!UICONTROL Beginnt mit]
   * [!UICONTROL Endet mit]

1. Geben Sie die Zeichenfolge ein, über die definiert wird, wo das Erlebnis hinzugefügt wird, wie die Domain oder die im Seitennamen enthaltenen Zeichenfolgen.

   Wenn Sie beispielsweise **[!UICONTROL Domain]** und **[!UICONTROL Ist (Groß- und Kleinschreibung berücksichtigen)]**, geben Sie die Domain ein, zu der das Erlebnis zu allen Seiten hinzugefügt werden soll.

   Sie können mehrere Elemente hinzufügen.

   >[!IMPORTANT]
   >
   >Mehrere Elemente verwenden die OR-Logik, d. h. jedes einzelne Element in der Liste macht die Bedingung wahr.

1. Geben Sie bei Bedarf zusätzliche Kriterien ein, indem Sie auf **[!UICONTROL Regel hinzufügen]** klicken und den Vorgang in den vorherigen Schritten wiederholen.

   Mehrere Kriterien werden mit der UND-Logik verbunden. [!DNL Target] fügt das Erlebnis allen Seiten hinzu, die den angegebenen Kriterien entsprechen.

>[!IMPORTANT]
>
> [!DNL Target] können die Seiten nicht überprüfen, um sicherzustellen, dass sie wie erwartet angezeigt werden. Daher ist es immer eine wichtige Praxis, wenn Sie diese Funktion verwenden, um betroffene Seiten zu testen, bevor Sie sie veröffentlichen.

## Anwendungsszenarien

Überprüfen Sie die folgenden Anwendungsfälle, um zu erfahren, wie Sie Vorlagenregeln auf Ihrer Site verwenden können:

### Dieselbe Aktivität für die gesamte Domain rendern

Sie können in Erwägung ziehen, Vorlagenregeln zu verwenden, um dieselbe Aktivität in Ihrer gesamten Domain für die folgenden Anwendungsfälle zu rendern:

* Einschließen einer globalen Kopf- oder Fußzeile
* So fügen Sie ein globales Banner hinzu (z. B. COVID-19-Ankündigungen)
* Um eine globale Versandkostenabo aufzunehmen

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) beschrieben.

1. Um die Domain anzugeben, in der das Erlebnis angezeigt wird, klicken [!UICONTROL Visual Experience Composer] auf das [!UICONTROL Konfigurieren]-Symbol ( ![Konfigurieren-Symbol](/help/main/assets/icons/Setting.svg) ) und wählen Sie dann **[!UICONTROL Seitenbereitstellung]** aus.

1. Klicken Sie **[!UICONTROL Regel hinzufügen]** > **[!UICONTROL Domain]**.

1. Wählen Sie in **[!UICONTROL Dropdown-]** „Evaluator auswählen“ die Option **[!UICONTROL Enthält]** und geben Sie dann die Domain an.
