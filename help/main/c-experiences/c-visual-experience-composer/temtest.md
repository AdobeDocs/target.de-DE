---
keywords: Vorlagentests;Vorlage;gleiches Erlebnis auf ähnlichen Seiten;Vorlagentest
description: Erfahren Sie, wie Sie mit Adobe [!DNL Target] Visual Experience Composer (VEC) dasselbe Erlebnis auf mehreren Seiten einschließen können, die ähnlich strukturiert sind oder dieselben Vorlagenelemente enthalten.
title: Kann ich dasselbe Erlebnis auf ähnlichen Seiten verwenden?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
TQID: 'https://experienceleague.adobe.com/zk7U6g7gk7XkpWsEFQbwuCm7xbpIb1lCaZefxjn-39g'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: ef98a6e0-f26c-4870-9bd4-e6b72e9cc699
    internal-label: Experiences and offers
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 17%
---
# Gleiches Erlebnis auf ähnlichen Seiten {#similar-pages}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit Seitenbereitstellungsregeln im [!UICONTROL Visual Experience Composer] (VEC) dasselbe Erlebnis auf Seiten mit ähnlicher Struktur einbeziehen.

>[!ENDSHADEBOX]

Eine Seitenvorlage in [!DNL Adobe Target] bietet eine Struktur für Seiten. Wenn Seiten ähnliche Elemente enthalten, können Varianten dieser ähnlich strukturierten Seitenelemente über mehrere Seiten oder über eine gesamte Domain hinweg getestet werden.

Damit sie ordnungsgemäß funktionieren, muss diese Funktion auf Seiten mit ähnlicher Struktur verwendet werden oder Vorlagenelemente enthalten, die auf allen Seiten gleich strukturiert sind.

>[!IMPORTANT]
>
>Die Verwendung dieser Funktion zum Ändern von Elementen auf unterschiedlichen Seiten führt wahrscheinlich zu unerwarteten Ergebnissen.

Mit dieser Funktion können Sie beispielsweise eine der folgenden Aktionen durchführen:

* Testen einer globalen Navigationsleiste durch Neuanordnen oder Entfernen von Elementen
* Entfernen eines Elements aus allen Produktseiten, die eine bestimmte Seitenvorlage verwenden
* Hinzufügen eines Banners zu allen Produktseiten
* Layout der Artikelvorlage ändern

## Angeben der Seiten für ein Erlebnis {#specify-pages}

Die Seiten, auf denen ein Erlebnis angezeigt wird, werden mit Seitenbereitstellungsregeln angegeben. Die Regeln können bestimmte Seiten enthalten oder die Änderung auf die Site oder Domain anwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Aktivitäten](/help/main/c-activities/activities.md) beschrieben.

1. Klicken Sie [!UICONTROL &#x200B; Visual Experience &#x200B;] auf das Symbol **[!UICONTROL Konfigurieren]** ( ![Symbol Konfigurieren](/help/main/assets/icons/Setting.svg) ) und wählen Sie dann **[!UICONTROL Seitenbereitstellung]**.

   ![Aktivitäten](assets/vec_edit_1.png)

1. Klicken Sie **[!UICONTROL Regel hinzufügen]** und geben Sie dann die Kriterien für die Seiten an, denen das Erlebnis hinzugefügt werden soll.

1. Geben Sie den Seitenbereich an: **[!UICONTROL URL]**, **[!UICONTROL Domain]**, **[!UICONTROL Path]**, **[!UICONTROL Hash (#) Fragment]** (der Teil einer URL, der dem #-Symbol folgt), **[!UICONTROL Query]** oder **[!UICONTROL Custom]**.

   Weitere Informationen dazu, wie [!DNL Target] URLs auswertet, finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).

   ![Aktivitäten](assets/vec_edit_2.png)

1. Wählen Sie einen Operator aus. Der Operator gibt an, in welcher Beziehung die Elemente nach dem Operator zum Seitenbereich stehen.

1. Geben Sie die Zeichenfolge ein, über die definiert wird, wo das Erlebnis hinzugefügt wird, wie die Domain oder die im Seitennamen enthaltenen Zeichenfolgen.

   Wenn beispielsweise **[!UICONTROL Domain]** und **[!UICONTROL Ist (Groß- und Kleinschreibung]**) ausgewählt sind, geben Sie die Domain ein, zu der das Erlebnis zu allen Seiten hinzugefügt wird.

   Es können mehrere Elemente einbezogen werden. Mehrere Elemente verwenden die OR-Logik, d. h. jedes einzelne Element in der Liste macht die Bedingung wahr.

1. (Optional) Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und wiederholen Sie die Schritte 3 bis 6, um weitere Kriterien einzugeben.

   Mehrere Kriterien werden mit der UND-Logik verbunden. [!DNL Target] fügt das Erlebnis allen Seiten hinzu, die den angegebenen Kriterien entsprechen.

>[!IMPORTANT]
>
>[!DNL Target] können die Seiten nicht überprüfen, um sicherzustellen, dass sie wie erwartet angezeigt werden. Daher ist es immer eine wichtige Praxis, wenn Sie diese Funktion verwenden, um die betroffenen Seiten zu testen, bevor Sie sie veröffentlichen.

## Anwendungsszenarien {#use-cases}

Vorlagenregeln können auf einer Site auf unterschiedliche Weise verwendet werden, wie der folgende Anwendungsfall zeigt.

### Dieselbe Aktivität für die gesamte Domain rendern {#entire-domain}

Vorlagenregeln können dieselbe Aktivität für die gesamte Domain rendern, z. B.:

* Einschließen einer globalen Kopf- oder Fußzeile
* So fügen Sie ein globales Banner hinzu (z. B. COVID-19-Ankündigungen)
* Um eine globale Versandkostenabo aufzunehmen

1. Erstellen oder bearbeiten Sie eine Aktivität wie in [Aktivitäten](/help/main/c-activities/activities.md) beschrieben.

1. Um die Domain anzugeben, in der das Erlebnis angezeigt wird, klicken [!UICONTROL Visual Experience Composer] auf das **[!UICONTROL Konfigurieren]**-Symbol ( ![Konfigurieren-Symbol](/help/main/assets/icons/Setting.svg) ) und wählen Sie dann **[!UICONTROL Seitenbereitstellung]** aus.

1. Klicken Sie **[!UICONTROL Regel hinzufügen]** > **[!UICONTROL Domain]**.

1. Wählen Sie in **[!UICONTROL Dropdown-]** „Evaluator auswählen“ die Option **[!UICONTROL Enthält]** und geben Sie dann die Domain an.

   ![Aktivitäten](assets/vec_edit_3.png)
