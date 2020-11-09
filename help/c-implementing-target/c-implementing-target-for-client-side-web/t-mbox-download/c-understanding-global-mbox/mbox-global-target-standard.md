---
keywords: global mbox;target classic;use global mbox from target classic
description: Target Standard erstellt standardmäßig eine globale Mbox mit der Bezeichnung „target-global-mbox“, die zum Ausführen von Aktivitäten verwendet wird, die in Target Standard erstellt wurden. Wenn Sie auf Ihren Seiten jedoch bereits eine globale MBox für Ihre bestehende Implementierung erstellt haben, können Sie diese MBox für Ihre Target Standard-Aktivitäten verwenden.
title: Verwenden einer globalen Mbox aus einer Legacy-Implementierung
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 57%

---


# Verwenden einer globalen Mbox aus einer Legacy-Implementierung{#use-a-global-mbox-from-a-legacy-implementation}

By default, [!DNL Target] creates a global mbox called target-global-mbox, which is used to run activities created in [!DNL Target]. Wenn Sie auf Ihren Seiten jedoch bereits eine globale MBox für Ihre bestehende Implementierung erstellt haben, können Sie diese MBox für Ihre [!DNL Target]-Aktivitäten verwenden.

>[!NOTE]
>
>Es ist nur eine globale Mbox pro Konto zulässig.

Sie müssen einige Parameter festlegen, um Ihre vorhandene globale MBox für [!DNL Target] und Ihre bestehende Implementierung verwenden zu können.

1. Go to [!DNL Target], then click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

   By default, **[!UICONTROL Page load enabled (Auto-create global mbox]** is enabled, and the custom global mbox is named `target-global-mbox`.

1. If you want to use an existing mbox, disable **[!UICONTROL Page load enabled (Auto-create global mbox]**, and specify the name of a previously created global mbox in the **[!UICONTROL Global Mbox]** field.

   The [!UICONTROL Global Mbox] drop-down lists all mboxes in your account. Wenn Sie eine Mbox verwenden möchten, die noch nicht vorhanden ist, erstellen Sie diese.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Die mbox.js-Einstellungen für Ihr Konto wurden aktualisiert.

1. Laden Sie die neue Datei &quot;at.js&quot;herunter und verweisen Sie darauf auf Ihrer Site.

   Alle bestehenden Aktivitäten werden aktualisiert, sodass diese die angegebene globale Mbox verwenden, einschließlich zuvor erstellter und implementierter Aktivitäten.

## Fehlerbehebung bei der Implementierung der globalen Mbox

Die folgenden häufig gestellten Fragen können zur Fehlerbehebung bei der Implementierung der globalen Mbox verwendet werden:

### Wieso wird die globale Mbox nicht geladen oder wieso gibt es eine Wartezeit beim Laden der globalen Mbox beim Laden der Seite?

Stellen Sie sicher, dass der &quot;at.js&quot;-Verweis der erste JavaScript-Aufruf auf der Seite ist. Weitere Lösungen zu diesem Problem finden Sie unter Häufig gestellte Fragen zur [globalen Mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md).
