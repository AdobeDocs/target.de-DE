---
keywords: globale Mbox;Target Classic;globale Mbox mit Target Classic verwenden
description: Erfahren Sie, wie Sie eine veraltete globale Mbox für Ihre Adobe Target-Aktivitäten verwenden können, wenn Sie bereits eine globale Mbox auf Ihren Seiten für Ihre älteren Implementierungen erstellt haben.
title: Kann ich eine globale Mbox aus einer älteren Implementierung verwenden?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 41%

---


# Globale Mbox aus einer älteren Implementierung verwenden

Standardmäßig erstellt [!DNL Target] eine globale Mbox mit dem Namen Zielgruppe-global-mbox, die zum Ausführen von Aktivitäten verwendet wird, die in [!DNL Target] erstellt wurden. Wenn Sie auf Ihren Seiten jedoch bereits eine globale MBox für Ihre bestehende Implementierung erstellt haben, können Sie diese MBox für Ihre [!DNL Target]-Aktivitäten verwenden.

>[!NOTE]
>
>Es ist nur eine globale Mbox pro Konto zulässig.

Sie müssen einige Parameter festlegen, um Ihre vorhandene globale MBox für [!DNL Target] und Ihre bestehende Implementierung verwenden zu können.

1. Gehen Sie zu [!DNL Target] und klicken Sie dann auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.

   Standardmäßig ist **[!UICONTROL Seitenladung aktiviert (Globale Mbox automatisch erstellen]** ist aktiviert und die benutzerdefinierte globale Mbox heißt `target-global-mbox`.

1. Wenn Sie eine vorhandene Mbox verwenden möchten, deaktivieren Sie **[!UICONTROL Seitenladeaktivierung (Globale Mbox automatisch erstellen]**) und geben Sie den Namen einer zuvor erstellten globalen Mbox im Feld **[!UICONTROL Globale Mbox]** an.

   Mit der Dropdownliste [!UICONTROL Globale Mbox] werden alle mboxes in Ihrem Konto Liste. Wenn Sie eine Mbox verwenden möchten, die noch nicht vorhanden ist, erstellen Sie diese.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Die mbox.js-Einstellungen für Ihr Konto wurden aktualisiert.

1. Laden Sie die neue Datei &quot;at.js&quot;herunter und verweisen Sie darauf auf Ihrer Site.

   Alle bestehenden Aktivitäten werden aktualisiert, sodass diese die angegebene globale Mbox verwenden, einschließlich zuvor erstellter und implementierter Aktivitäten.

## Fehlerbehebung bei der Implementierung der globalen Mbox

Die folgenden häufig gestellten Fragen können zur Fehlerbehebung bei der Implementierung der globalen Mbox verwendet werden:

### Wieso wird die globale Mbox nicht geladen oder wieso gibt es eine Wartezeit beim Laden der globalen Mbox beim Laden der Seite?

Stellen Sie sicher, dass der &quot;at.js&quot;-Verweis der erste JavaScript-Aufruf auf der Seite ist. Weitere Lösungen für dieses Problem finden Sie unter [Häufig gestellte Fragen zur globalen Mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md).
