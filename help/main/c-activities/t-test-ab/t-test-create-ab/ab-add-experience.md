---
keywords: Targeting;Erlebnis;Erlebnis hinzufügen;Erlebnisse hinzufügen
description: Verwenden Sie den [!UICONTROL Visual Experience Composer], um Aktivitäten Erlebnisse hinzuzufügen.
title: Wie kann ich Erlebnisse in einer A/B-Aktivität hinzufügen?
feature: A/B Tests
exl-id: c0f1b5a7-07b0-46c2-97f3-95dcc0fcbe3d
TQID: 'https://experienceleague.adobe.com/7qEiUXkfMbPmtB2eMio0LztOYM3naHxG-WRQZOyMmlU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 9f1aaf5c0b172b4bbe89266800708881306e4592
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 25%
---
# Hinzufügen von Erlebnissen {#ab-add-experience}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie ein Erlebnis in einer A/B-Aktivität hinzufügen und gestalten und es umbenennen, umleiten, duplizieren oder löschen.

>[!ENDSHADEBOX]

Der [!DNL Adobe Target] **[!UICONTROL Visual Experience Composer]** (VEC) bietet eine visuelle Benutzeroberfläche zum Hinzufügen und Bearbeiten von Erlebnissen auf Ihrer Seite. Weitere Informationen zu Erlebnissen finden Sie unter [Erlebnisse](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D).

## Hinzufügen und Entwerfen eines Erlebnisses {#add-experience}

So fügen Sie ein Erlebnis hinzu und ändern die Seite für dieses Erlebnis:

1. Klicken Sie auf **[!UICONTROL Seite]** Erlebnisse“ in Visual Experience Composer auf das Symbol **[!UICONTROL Hinzufügen]** ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ) oben im Bereich **[!UICONTROL Erlebnisse]**.

   Nachdem Sie eine neue Aktivität erstellt haben, zeigt VEC auf der linken Seite zwei Registerkarten an: Erlebnis A und Erlebnis B. Erlebnis A ist das Kontrollerlebnis. Sie können dem Test mehrere Erlebnisse hinzufügen.

1. Wählen Sie die zu ändernden Elemente aus und nehmen Sie die gewünschten Änderungen vor.

   Wenn Sie den Mauszeiger über die Elemente auf der Seite bewegen, werden die Elemente hervorgehoben. Alle hervorgehobenen Elemente können mit dem VEC geändert werden. Wenn Sie eine [!DNL Target] Anfrage auf der Seite mit [!DNL Target Classic] (früher [!DNL Test&Target]) erstellt haben, wird diese [!DNL Target] Anfrage als ein Element angezeigt, das den Namen der Anfrage anzeigt, und kann wie jedes andere Element geändert werden.

   Eine Liste der Aktionen, die für ein Element auf der angezeigten Seite durchgeführt werden können, um das Erlebnis zu ändern, finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

1. Klicken Sie **[!UICONTROL Weiter]** wenn Sie mit dem Entwerfen des Erlebnisses fertig sind.

>[!NOTE]
>
>Wenn Sie ein Bild aus einer anderen Quelle als der Hauptseite bereitstellen (z. B. ein Bild, das auf `akamai.net` gehostet und auf `example.com` bereitgestellt wird), wird das Bild nicht in der Miniaturansicht der Seite, die auf dem Flussdiagramm zu sehen ist, angezeigt.

## Umbenennen eines Erlebnisses {#rename-experience}

So geben Sie einem Erlebnis einen neuen Namen:

1. Klicken Sie auf **[!UICONTROL Symbol „Erlebnis]**&quot; ( ![Symbol „Umbenennen](/help/main/assets/icons/Rename.svg) ) neben dem Erlebnis.

1. Geben Sie einen neuen Namen ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

Beim Benennen oder Umbenennen eines Erlebnisses sind die folgenden Zeichen nicht zulässig:

| Zeichen | Beschreibung |
|--- |--- |
| `/` | Vorwärtsschrägstrich |
| `?` | Fragezeichen |
| `#` | Raute |
| `:` | Doppelpunkt |
| `=` | Gleich |
| `+` | Plus |
| `-` | Minus |
| `@` | At-Zeichen |

## Erlebnis zu einer URL umleiten {#redirect-to-url}

Informationen zum Senden von Besuchern eines Erlebnisses an eine andere URL finden Sie unter [Umleiten zu URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md):

1. Klicken Sie **[!UICONTROL Bereich]** Erlebnisse“ auf das Symbol **[!UICONTROL Mehr]** ( ![Mehr-](/help/main/assets/icons/MoreSmall.svg) ) neben dem Erlebnis und dann auf **[!UICONTROL Zu URL umleiten]**.

1. Geben Sie die URL an, zu der Sie das Erlebnis umleiten möchten.

1. (Bedingt) Aktivieren Sie das **[!UICONTROL Aktuelle Abfrageparameter einschließen]**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Duplizieren eines Erlebnisses {#duplicate-experience}

Sie können ein Erlebnis in einen A/B-Test kopieren, um kleinere Änderungen daran vorzunehmen, ohne das Erlebnis neu erstellen zu müssen. Klicken Sie **[!UICONTROL Bereich]** Erlebnisse“ auf das Symbol **[!UICONTROL Mehr]** ( ![Mehr-](/help/main/assets/icons/MoreSmall.svg) ) neben dem Erlebnis und dann auf **[!UICONTROL Duplizieren]**.

## Löschen eines Erlebnisses {#delete-experience}

Klicken Sie **[!UICONTROL Bereich]** Erlebnisse“ auf das Symbol **[!UICONTROL Mehr]** ( ![Mehr-](/help/main/assets/icons/MoreSmall.svg) ) neben dem Erlebnis, klicken Sie auf **[!UICONTROL Löschen]** und dann auf **[!UICONTROL Löschen]**, um die Aktion zu bestätigen.
