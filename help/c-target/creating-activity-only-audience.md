---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; nur Aktivität; nur Activity; adhoc
description: Erfahren Sie, wie Sie in Adobe [!DNL Target] Zielgruppen "Nur Aktivität"erstellen, die nur einmal verwendet werden können.
title: Kann ich eine Zielgruppe erstellen, die nur einmal verwendet werden soll?
feature: Zielgruppen
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 20a5201b5c05b1f083252ac73b3b4bbc91e97aaa
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 64%

---

# Erstellen einer Zielgruppe „Nur Aktivität“

Erstellen Sie Zielgruppen &quot;Nur Aktivität&quot;innerhalb des geleiteten Arbeitsablaufs mit drei Schritten [!DNL Adobe Target], während Sie eine Aktivität erstellen. Diese Ad-hoc-Zielgruppen können an anderen Orten innerhalb derselben Aktivität verwendet werden, werden aber nicht in der [!UICONTROL Zielgruppenbibliothek] gespeichert und können nicht in anderen Aktivitäten verwendet werden.

Zielgruppen „Nur Aktivität“ bieten die folgenden Vorteile:

* Sie können Zielgruppen vom Typ „Nur Aktivität“ verwenden, um eine Zielgruppe zu erstellen, die Sie nur einmal verwenden und nicht in der [!UICONTROL Zielgruppenbibliothek] speichern möchten. Zielgruppen &quot;Nur Aktivität&quot;verhindern, dass die [!UICONTROL Zielgruppenbibliothek] mit Zielgruppen überladen wird, die Sie nie wieder verwenden möchten.
* Zielgruppen „Nur Aktivität“ werden in der [!UICONTROL Zielgruppenbibliothek] nicht angezeigt. Da diese Zielgruppen nicht in der Bibliothek angezeigt werden, sind sie vor unerwünschten Änderungen durch andere in Ihrer Organisation geschützt.

1. Klicken Sie beim Erstellen einer [Aktivität](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Targeting]** auf die drei vertikalen Ellipsen und dann auf **[!UICONTROL Zielgruppe ersetzen]**.

   ![Schrittergebnis](assets/edit_audience.png)

1. Klicken Sie auf **[!UICONTROL Zielgruppe erstellen]**.

1. Klicken Sie auf **[!UICONTROL Diese Aktivität ist nur]**.

   ![](assets/activity-only-aud.png)

1. Geben Sie einen beschreibenden Namen für die Zielgruppe ein.
1. Ziehen Sie die gewünschten Attribute per Drag-and-Drop in den Audience Builder.

   Regeln ermöglichen es, Ihre Zielgruppe auf eine Untergruppe Ihrer Site-Besucher zu beschränken. Jeder Regeltyp hat eigene Parameter. Weitere Informationen zum Konfigurieren der einzelnen Typen von Zielgruppenregeln finden Sie unter [Kategorien für Zielgruppen](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Zu beachten

Berücksichtigen Sie beim Arbeiten mit Zielgruppen „Nur Aktivität“ folgende Informationen:

* Sie können Zielgruppen &quot;Nur Aktivität&quot;im [!UICONTROL Visual Experience Composer] (VEC) oder im [!UICONTROL formularbasierten Experience Composer] erstellen. Diese Funktionalität ersetzt Verfeinerungsregeln in früheren Versionen von [!DNL Target].
* Sie können eine Aktivität erstellen und für die spätere Verwendung in anderen Aktivitäten in der [!UICONTROL Zielgruppenbibliothek] speichern oder eine Zielgruppe „Nur Aktivität“ erstellen. Wenn Sie die Zielgruppe gespeichert haben, können Sie den Zielgruppentyp nicht mehr ändern.
* Verfeinerungen für vorhandene Aktivitäten werden in Zielgruppen „Nur Aktivität“ migriert.
* Der Status von Zielgruppen vom Typ „Nur Aktivität“ kann [!UICONTROL Verwendet] oder [!UICONTROL Nicht verwendet] sein. Nicht verwendete Zielgruppen „Nur Aktivität“ werden angezeigt, bis die Aktivität gespeichert wird. Wenn Sie sie nicht verwenden und versuchen, die Aktivität zu speichern, wird Ihnen ein Warnhinweis angezeigt, der Sie darauf hinweist, dass die nicht verwendete Zielgruppe „Nur Aktivität“ gelöscht wird.
* Sie können die Details zur Zielgruppendefinition über Pop-up-Karten in der Zielgruppenauswahl anzeigen, ohne die Zielgruppe zu öffnen.
* Sie können [mehrere Zielgruppen kombinieren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), um „Nur Aktivität“-Zielgruppen zu erstellen.
