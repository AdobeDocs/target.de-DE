---
description: Erstellen Sie Zielgruppen „Nur Aktivität“ innerhalb des geleiteten Arbeitsablaufs mit drei Schritten, während Sie eine Aktivität erstellen. Diese Ad-hoc-Zielgruppen können an anderen Orten innerhalb derselben Aktivität verwendet werden, werden aber nicht in der Zielgruppenbibliothek gespeichert und können nicht in anderen Aktivitäten verwendet werden.
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; nur Aktivität; nur Activity; adhoc
seo-description: Erstellen Sie ausschließlich Zielgruppen aus dem mit drei Schritten geleiteten Arbeitsablauf für Adobe Target, wenn Sie eine Aktivität erstellen. Diese Ad-hoc-Zielgruppen können an anderen Orten innerhalb derselben Aktivität verwendet werden, werden aber nicht in der Zielgruppenbibliothek gespeichert und können nicht in anderen Aktivitäten verwendet werden.
seo-title: Erstellen einer Zielgruppe „Nur Aktivität“ in Adobe Target
solution: Target
title: Erstellen einer Zielgruppe „Nur Aktivität“
topic: Advanced,Standard,Classic
uuid: 3d0898d0-96e8-4bc9-86bd-3ae39db0e74d
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Erstellen einer Zielgruppe „Nur Aktivität“{#create-an-activity-only-audience}

Erstellen Sie Zielgruppen „Nur Aktivität“ innerhalb des geleiteten Arbeitsablaufs mit drei Schritten, während Sie eine Aktivität erstellen. These ad hoc audiences can be used in other places within the same activity, but are not stored in the [!UICONTROL Audiences Library] for use in other activities.

Zielgruppen „Nur Aktivität“ bieten die folgenden Vorteile:

* You can use activity-only audiences to create an audience that you want to use only once and you do not want to store it in the [!UICONTROL Audiences Library]. This prevents the [!UICONTROL Audiences Library] from being cluttered with audiences that you never want to use again.
* Activity-only audiences are not visible in the [!UICONTROL Audiences Library]. Gleichzeitig sind sie so auch vor Änderungen durch andere Personen in Ihrer Organisation geschützt.

1. While creating an [activity](../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), on the **[!UICONTROL Target]** page, click the three vertical ellipses, then click **[!UICONTROL Replace Audience]**.

   ![Schrittergebnis](assets/edit_audience.png)

1. On the [!UICONTROL Choose Audience] page, click **[!UICONTROL Activity Only Audience]**.

   ![](assets/activity-only-aud.png)

1. Klicken Sie auf **[!UICONTROL Zielgruppe erstellen]**.
1. Geben Sie einen beschreibenden Namen für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL + Regel hinzufügen]**.

   Regeln ermöglichen es, die Zielgruppe auf eine Untergruppe der Site-Besucher einzuschränken.

1. Wählen Sie einen Regeltyp aus.

   Jeder Regeltyp hat eigene Parameter. Weitere Informationen zum Konfigurieren der einzelnen Typen von Zielgruppenregeln finden Sie unter [Kategorien für Zielgruppen](../c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D).

1. Definieren Sie die Regelparameter.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Zu beachten

Berücksichtigen Sie beim Arbeiten mit Zielgruppen „Nur Aktivität“ folgende Informationen:

* Sie können Zielgruppen „Nur Aktivität“ im Visual Experience Composer (VEC) oder im Form-Based Experience Composer erstellen. Diese Funktionalität ersetzt Verfeinerungsregeln in früheren Versionen von Target.
* You can create an activity to store in the [!UICONTROL Audience Library] for reuse in other activities or you create an activity-only audience. Wenn Sie die Zielgruppe gespeichert haben, können Sie den Zielgruppentyp nicht mehr ändern.
* Verfeinerungen für vorhandene Aktivitäten werden in Zielgruppen „Nur Aktivität“ migriert.
* Activity-only audiences have a status of [!UICONTROL Used] or [!UICONTROL Unused]. Nicht verwendete Zielgruppen „Nur Aktivität“ werden angezeigt, bis die Aktivität gespeichert wird. Wenn Sie sie nicht verwenden und versuchen, die Aktivität zu speichern, wird Ihnen ein Warnhinweis angezeigt, der Sie darauf hinweist, dass die nicht verwendete Zielgruppe „Nur Aktivität“ gelöscht wird.
* Sie können die Details zur Zielgruppendefinition über Pop-up-Karten in der Zielgruppenauswahl anzeigen, ohne die Zielgruppe zu öffnen.
* Sie können [mehrere Zielgruppen kombinieren](../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), um „Nur Aktivität“-Zielgruppen zu erstellen.

