---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; nur Aktivität; nur Activity; adhoc
description: Erfahren Sie, wie Sie in Adobe Target Audiencen erstellen, die nur für die Aktivität bestimmt sind und in der aktuellen Aktivität nur einmal verwendet werden können und nicht in der Bibliothek "Audiencen"gespeichert sind.
title: Kann ich eine Audience erstellen, die nur einmal verwendet werden kann?
feature: Audiences
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 91%

---


# Erstellen einer Zielgruppe „Nur Aktivität“{#create-an-activity-only-audience}

Erstellen Sie Zielgruppen „Nur Aktivität“ innerhalb des geleiteten Arbeitsablaufs mit drei Schritten, während Sie eine Aktivität erstellen. Diese Ad-hoc-Zielgruppen können an anderen Orten innerhalb derselben Aktivität verwendet werden, werden aber nicht in der [!UICONTROL Zielgruppenbibliothek] gespeichert und können nicht in anderen Aktivitäten verwendet werden.

Zielgruppen „Nur Aktivität“ bieten die folgenden Vorteile:

* Sie können Zielgruppen vom Typ „Nur Aktivität“ verwenden, um eine Zielgruppe zu erstellen, die Sie nur einmal verwenden und nicht in der [!UICONTROL Zielgruppenbibliothek] speichern möchten. Somit sammeln sich keine Zielgruppen in der [!UICONTROL Zielgruppenbibliothek], die Sie nie wieder verwenden möchten.
* Zielgruppen „Nur Aktivität“ werden in der [!UICONTROL Zielgruppenbibliothek] nicht angezeigt. Gleichzeitig sind sie so auch vor Änderungen durch andere Personen in Ihrer Organisation geschützt.

1. Klicken Sie beim Erstellen einer [Aktivität](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der **[!UICONTROL Target]**-Seite auf das Symbol mit den drei vertikalen Strichen und dann auf **[!UICONTROL Zielgruppe ändern]**.

   ![Schrittergebnis](assets/edit_audience.png)

1. Klicken Sie auf der Seite [!UICONTROL Zielgruppe auswählen] auf **[!UICONTROL Zielgruppe „Nur Aktivität“]**.

   ![](assets/activity-only-aud.png)

1. Klicken Sie auf **[!UICONTROL Zielgruppe erstellen]**.
1. Geben Sie einen beschreibenden Namen für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL + Regel hinzufügen]**.

   Regeln ermöglichen es, die Zielgruppe auf eine Untergruppe der Site-Besucher einzuschränken.

1. Wählen Sie einen Regeltyp aus.

   Jeder Regeltyp hat eigene Parameter. Weitere Informationen zum Konfigurieren der einzelnen Typen von Zielgruppenregeln finden Sie unter [Kategorien für Zielgruppen](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D).

1. Definieren Sie die Regelparameter.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Zu beachten

Berücksichtigen Sie beim Arbeiten mit Zielgruppen „Nur Aktivität“ folgende Informationen:

* Sie können Zielgruppen „Nur Aktivität“ im Visual Experience Composer (VEC) oder im Form-Based Experience Composer erstellen. Diese Funktionalität ersetzt Verfeinerungsregeln in früheren Versionen von Target.
* Sie können eine Aktivität erstellen und für die spätere Verwendung in anderen Aktivitäten in der [!UICONTROL Zielgruppenbibliothek] speichern oder eine Zielgruppe „Nur Aktivität“ erstellen. Wenn Sie die Zielgruppe gespeichert haben, können Sie den Zielgruppentyp nicht mehr ändern.
* Verfeinerungen für vorhandene Aktivitäten werden in Zielgruppen „Nur Aktivität“ migriert.
* Der Status von Zielgruppen vom Typ „Nur Aktivität“ kann [!UICONTROL Verwendet] oder [!UICONTROL Nicht verwendet] sein. Nicht verwendete Zielgruppen „Nur Aktivität“ werden angezeigt, bis die Aktivität gespeichert wird. Wenn Sie sie nicht verwenden und versuchen, die Aktivität zu speichern, wird Ihnen ein Warnhinweis angezeigt, der Sie darauf hinweist, dass die nicht verwendete Zielgruppe „Nur Aktivität“ gelöscht wird.
* Sie können die Details zur Zielgruppendefinition über Pop-up-Karten in der Zielgruppenauswahl anzeigen, ohne die Zielgruppe zu öffnen.
* Sie können [mehrere Zielgruppen kombinieren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), um „Nur Aktivität“-Zielgruppen zu erstellen.

