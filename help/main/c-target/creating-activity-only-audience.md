---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; nur Aktivität; nur Activity; adhoc
description: Erfahren Sie, wie Sie in Adobe Zielgruppen "Nur Aktivität"erstellen [!DNL Target] die nur einmal verwendet werden.
title: Kann ich eine Zielgruppe erstellen, die nur einmal verwendet werden soll?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 55%

---

# Erstellen einer Zielgruppe „Nur Aktivität“

Erstellen von Zielgruppen &quot;Nur Aktivität&quot;aus dem [!DNL Adobe Target] geleiteter Arbeitsablauf mit drei Schritten während der Erstellung einer Aktivität. Diese Ad-hoc-Zielgruppen können an anderen Orten innerhalb derselben Aktivität verwendet werden, werden aber nicht in der [!UICONTROL Zielgruppenbibliothek] gespeichert und können nicht in anderen Aktivitäten verwendet werden.

Zielgruppen „Nur Aktivität“ bieten die folgenden Vorteile:

* Sie können Zielgruppen vom Typ „Nur Aktivität“ verwenden, um eine Zielgruppe zu erstellen, die Sie nur einmal verwenden und nicht in der [!UICONTROL Zielgruppenbibliothek] speichern möchten. Zielgruppen &quot;Nur Aktivität&quot;helfen dabei, die [!UICONTROL Zielgruppenbibliothek] nicht mit Zielgruppen überladen werden, die Sie nie wieder verwenden möchten.
* Zielgruppen „Nur Aktivität“ werden in der [!UICONTROL Zielgruppenbibliothek] nicht angezeigt. Da diese Zielgruppen nicht in der Bibliothek angezeigt werden, sind sie vor unerwünschten Änderungen durch andere in Ihrer Organisation geschützt.

1. Beim Erstellen einer [activity](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)auf **[!UICONTROL Targeting]** Seite, klicken Sie auf die drei vertikalen Ellipsen und dann auf **[!UICONTROL Zielgruppe ersetzen]**.

   ![Schrittergebnis](assets/edit_audience.png)

1. Klicken Sie auf **[!UICONTROL Zielgruppe erstellen]**.

1. Klicken **[!UICONTROL Diese Aktivität]**.

   ![](assets/activity-only-aud.png)

1. Geben Sie einen beschreibenden Namen für die Zielgruppe ein.
1. Ziehen Sie die gewünschten Attribute per Drag-and-Drop in den Audience Builder.

   Regeln ermöglichen es, Ihre Zielgruppe auf eine Untergruppe Ihrer Site-Besucher zu beschränken. Jeder Regeltyp hat eigene Parameter. Weitere Informationen zum Konfigurieren der einzelnen Typen von Zielgruppenregeln finden Sie unter [Kategorien für Zielgruppen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D).

1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Zu beachten

Berücksichtigen Sie beim Arbeiten mit Zielgruppen „Nur Aktivität“ folgende Informationen:

* Sie können Zielgruppen &quot;Nur Aktivität&quot;im [!UICONTROL Visual Experience Composer] (VEC) oder im [!UICONTROL Form-Based Experience Composer]. Diese Funktionalität ersetzt Verfeinerungsregeln in früheren Versionen von [!DNL Target].
* Sie können eine Aktivität erstellen und für die spätere Verwendung in anderen Aktivitäten in der [!UICONTROL Zielgruppenbibliothek] speichern oder eine Zielgruppe „Nur Aktivität“ erstellen. Wenn Sie die Zielgruppe gespeichert haben, können Sie den Zielgruppentyp nicht mehr ändern.
* Verfeinerungen für vorhandene Aktivitäten werden in Zielgruppen „Nur Aktivität“ migriert.
* Der Status von Zielgruppen vom Typ „Nur Aktivität“ kann [!UICONTROL Verwendet] oder [!UICONTROL Nicht verwendet] sein. Nicht verwendete Zielgruppen „Nur Aktivität“ werden angezeigt, bis die Aktivität gespeichert wird. Wenn Sie sie nicht verwenden und versuchen, die Aktivität zu speichern, wird Ihnen ein Warnhinweis angezeigt, der Sie darauf hinweist, dass die nicht verwendete Zielgruppe „Nur Aktivität“ gelöscht wird.
* Sie können die Details zur Zielgruppendefinition über Pop-up-Karten in der Zielgruppenauswahl anzeigen, ohne die Zielgruppe zu öffnen.
* Sie können [mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), um „Nur Aktivität“-Zielgruppen zu erstellen.
* Zielgruppen &quot;Nur Aktivität&quot;unterstützen keine Ausschlussregeln.

   Sie können die folgenden Alternativen verwenden, um Ausschlussregeln zu verwenden:

   * [Erstellen und Verwenden einer Bibliothekszielgruppe](/help/main/c-target/c-audiences/create-audience.md) anstelle einer Zielgruppe &quot;Nur Aktivität&quot;.
   * [Kombinieren mehrerer](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) (bis zu 20) Bibliothekszielgruppen in eine Zielgruppe &quot;Nur Aktivität&quot;. Beim Kombinieren von Zielgruppen können Regeln in einzelnen Bibliothekszielgruppen verwendet und ausgeschlossen werden, selbst wenn die kombinierte Zielgruppe als Zielgruppe &quot;Nur Aktivität&quot;gespeichert wird.
