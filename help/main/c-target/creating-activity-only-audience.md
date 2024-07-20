---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; nur Aktivität; nur Activity; adhoc
description: Erfahren Sie, wie Sie in Adobe [!DNL Target] Zielgruppen "Nur Aktivität"erstellen, die nur einmal verwendet werden können.
title: Kann ich eine Zielgruppe erstellen, die nur einmal verwendet werden soll?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 33%

---

# Erstellen einer Zielgruppe „Nur Aktivität“

Erstellen Sie Zielgruppen vom Typ &quot;Nur Aktivität&quot;innerhalb des geleiteten Arbeitsablaufs mit drei Schritten, während Sie eine Aktivität erstellen. [!DNL Adobe Target] Diese Ad-hoc-Zielgruppen können an anderen Orten innerhalb derselben Aktivität verwendet werden, werden jedoch nicht in [!UICONTROL Audiences Library] gespeichert und können nicht in anderen Aktivitäten verwendet werden.

Zielgruppen „Nur Aktivität“ bieten die folgenden Vorteile:

* Sie können Zielgruppen vom Typ &quot;Nur Aktivität&quot;verwenden, um eine Zielgruppe zu erstellen, die Sie nur einmal verwenden und nicht im [!UICONTROL Audiences Library] speichern möchten. Mit Zielgruppen vom Typ &quot;Nur Aktivität&quot;können Sie verhindern, dass die [!UICONTROL Audiences Library] mit Zielgruppen überladen wird, die Sie nie wieder verwenden möchten.
* Zielgruppen &quot;Nur Aktivität&quot;sind nicht in der [!UICONTROL Audiences Library] sichtbar. Da diese Zielgruppen nicht in der Bibliothek angezeigt werden, sind sie vor unerwünschten Änderungen durch andere in Ihrer Organisation geschützt.

1. Klicken Sie beim Erstellen einer [Aktivität](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Targeting]** auf die drei vertikalen Ellipsen und dann auf **[!UICONTROL Replace Audience]**.

   ![Schrittergebnis](assets/edit_audience.png)

1. Klicken Sie auf **[!UICONTROL Create Audience]**.

1. Klicken Sie auf **[!UICONTROL This activity only]**.

   ![Bild &quot;Nur Aktivität&quot;](assets/activity-only-aud.png)

1. Geben Sie einen beschreibenden Namen für die Zielgruppe ein.
1. Ziehen Sie die gewünschten Attribute per Drag-and-Drop in den Audience Builder.

   Regeln ermöglichen es, Ihre Zielgruppe auf eine Untergruppe Ihrer Site-Besucher zu beschränken. Jeder Regeltyp hat eigene Parameter. Weitere Informationen zum Konfigurieren der einzelnen Typen von Zielgruppenregeln finden Sie unter [Kategorien für Zielgruppen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D).

1. Klicken Sie auf **[!UICONTROL Done]**.

## Zu beachten

Berücksichtigen Sie beim Arbeiten mit Zielgruppen „Nur Aktivität“ folgende Informationen:

* Sie können Zielgruppen &quot;Nur Aktivität&quot;im [!UICONTROL Visual Experience Composer] (VEC) oder im [!UICONTROL Form-Based Experience Composer] erstellen. Diese Funktion ersetzt die Verfeinerungsregeln in früheren Versionen von [!DNL Target].
* Sie können eine Aktivität erstellen, die in [!UICONTROL Audience Library] zur Wiederverwendung in anderen Aktivitäten gespeichert wird, oder Sie erstellen eine Zielgruppe &quot;Nur Aktivität&quot;. Wenn Sie die Zielgruppe gespeichert haben, können Sie den Zielgruppentyp nicht mehr ändern.
* Verfeinerungen für vorhandene Aktivitäten werden in Zielgruppen „Nur Aktivität“ migriert.
* Zielgruppen &quot;Nur Aktivität&quot;haben den Status &quot;[!UICONTROL Used]&quot;oder &quot;[!UICONTROL Unused]&quot;. Nicht verwendete Zielgruppen „Nur Aktivität“ werden angezeigt, bis die Aktivität gespeichert wird. Wenn Sie sie nicht verwenden und versuchen, die Aktivität zu speichern, wird Ihnen ein Warnhinweis angezeigt, der Sie darauf hinweist, dass die nicht verwendete Zielgruppe „Nur Aktivität“ gelöscht wird.
* Sie können die Details zur Zielgruppendefinition über Pop-up-Karten in der Zielgruppenauswahl anzeigen, ohne die Zielgruppe zu öffnen.
* Sie können [mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), um „Nur Aktivität“-Zielgruppen zu erstellen.
* Zielgruppen &quot;Nur Aktivität&quot;unterstützen keine Ausschlussregeln.

  Sie können die folgenden Alternativen verwenden, um Ausschlussregeln zu verwenden:

   * [Erstellen und verwenden Sie eine Bibliothekszielgruppe](/help/main/c-target/c-audiences/create-audience.md) anstelle einer reinen Aktivitätszielgruppe.
   * [Kombinieren mehrerer](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) (bis zu 20) Bibliothekszielgruppen in einer Zielgruppe &quot;Nur Aktivität&quot;. Beim Kombinieren von Zielgruppen können Regeln in einzelnen Bibliothekszielgruppen verwendet und ausgeschlossen werden, selbst wenn die kombinierte Zielgruppe als Zielgruppe &quot;Nur Aktivität&quot;gespeichert wird.
