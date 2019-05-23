---
description: Target Standard erstellt standardmäßig eine globale Mbox mit der Bezeichnung „target-global-mbox“, die zum Ausführen von Aktivitäten verwendet wird, die in Target Standard erstellt wurden. Wenn Sie auf Ihren Seiten jedoch bereits eine globale MBox für Ihre bestehende Implementierung erstellt haben, können Sie diese MBox für Ihre Target Standard-Aktivitäten verwenden.
keywords: globale Mbox;Target Classic;globale Mbox mit Target Classic verwenden
seo-description: Target Standard erstellt standardmäßig eine globale Mbox mit der Bezeichnung „target-global-mbox“, die zum Ausführen von Aktivitäten verwendet wird, die in Target Standard erstellt wurden. Wenn Sie auf Ihren Seiten jedoch bereits eine globale MBox für Ihre bestehende Implementierung erstellt haben, können Sie diese MBox für Ihre Target Standard-Aktivitäten verwenden.
seo-title: Verwenden einer globalen Mbox aus einer Legacy-Implementierung
solution: Target
subtopic: Erste Schritte
title: Verwenden einer globalen Mbox aus einer Legacy-Implementierung
topic: Standard
uuid: 31b03dab-99da-4040-bab6-4f5cb452ffdc
translation-type: tm+mt
source-git-commit: 78c756d3606c4080675f76f49c926f9882593ca2

---


# Verwenden einer globalen Mbox aus einer Legacy-Implementierung{#use-a-global-mbox-from-a-legacy-implementation}

Target Standard erstellt standardmäßig eine globale Mbox mit der Bezeichnung „target-global-mbox“, die zum Ausführen von Aktivitäten verwendet wird, die in Target Standard erstellt wurden. Wenn Sie auf Ihren Seiten jedoch bereits eine globale MBox für Ihre bestehende Implementierung erstellt haben, können Sie diese MBox für Ihre Target Standard-Aktivitäten verwenden.

>[!NOTE]
>
>Es ist nur eine globale Mbox pro Konto zulässig.

Sie müssen einige Parameter festlegen, um Ihre vorhandene globale MBox für [!DNL Target Standard] und Ihre bestehende Implementierung verwenden zu können.

1. Gehen Sie zu [!DNL Target Standard] und klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]**.

   [!UICONTROL Globale Mbox automatisch erstellen] ist standardmäßig aktiviert und die benutzerdefinierte globale Mbox trägt die Bezeichnung `target-global-mbox`.
1. Wenn Sie eine vorhandene Mbox verwenden möchten, deaktivieren Sie [!UICONTROL Globale Mbox automatisch erstellen] und geben Sie den Namen einer zuvor erstellten globalen Mbox im Feld [!UICONTROL Benutzerdefinierte globale mbox] an.

   In der Dropdownliste [!UICONTROL „Benutzerdefinierte globale Mbox“] werden alle Mboxes Ihres Kontos angezeigt. Wenn Sie eine Mbox verwenden möchten, die noch nicht vorhanden ist, erstellen Sie diese in Target Classic.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Die mbox.js-Einstellungen für Ihr Konto wurden aktualisiert.
1. Laden Sie die neue mbox.js-Datei herunter und referenzieren Sie sie auf Ihrer Site.

   Sobald Sie Ihre Produktions-Site mit der neuen mbox.js-Datei aktualisiert haben, können Sie Ihre Voreinstellungen festlegen.
1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Voreinstellungen]**.
1. Geben Sie im Feld [!UICONTROL „Benutzerdefinierte globale Mbox“] den Namen der globalen Mbox an, die Sie auf der Implementierungsseite ausgewählt haben.
1. Klicken Sie auf **[!UICONTROL Senden]**.

   Alle bestehenden Aktivitäten werden aktualisiert, sodass diese die angegebene globale Mbox verwenden, einschließlich zuvor erstellter und implementierter Aktivitäten.
   **Fehlerbehebung bei der Implementierung der globalen mbox**   *Wieso wird die globale Mbox nicht geladen oder wieso gibt es eine Wartezeit beim Laden der globalen Mbox beim Laden der Seite?*

Vergewissern Sie sich, dass der mbox.js-Verweis der erste JavaScript-Aufruf auf der Seite ist. Weitere Lösungsmöglichkeiten für dieses Problem finden Sie unter   [„mbox.js“-Implementierung](../../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420).
