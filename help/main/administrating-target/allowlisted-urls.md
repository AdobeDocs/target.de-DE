---
keywords: Zulassungsliste;Remote-Angebot;Administration;URL-Muster;Validierung;Aktivitäten;Angebote;Platzhalter;Regex
description: Erfahren Sie im Abschnitt Adobe Target-Administration , wie Sie auf die Zulassungsliste gesetzt URLs für Remote-Angebote anzeigen, suchen, hinzufügen und löschen können, einschließlich des Validierungsverhaltens und des Kontobereichs.
title: Verwalten von Remote-Angebots-URLs
feature: Administration & Configuration
topic: Implementation
role: Admin
level: Intermediate
solution: Target
product: Target
source-git-commit: 882c91244e5dae0977c8a6a1e5878525f497a720
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Geteilte URLs

Auf die Zulassungsliste gesetzt URLs definieren vertrauenswürdige URL-Muster, in denen Ihr Unternehmen [!DNL Adobe Target] Erlebnisse erstellen und ausführen kann, einschließlich der Verwendung von Remote- oder Umleitungsangeboten. Die Liste funktioniert neben [Host-Management](/help/main/administrating-target/hosts.md) und [Umgebungen](/help/main/administrating-target/environments.md), gilt jedoch speziell für zulässige Remote-Angebots-URL-Muster und zugehörige Validierungen.

Um URLs zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Allowlisted URLs]**.

![Seite mit URL-Liste, Suchfeld und URL-Steuerung hinzufügen](../administrating-target/assets/allowlist-1.png)

## Verwalten von URLs {#add-url}

In der Haupttabelle werden die einzelnen Muster in einer Spalte aufgelistet. Unterstützte Einträge können exakte URLs, Platzhalterpfade oder Musterformate enthalten, die Ihr Unternehmen für Remote-Erlebnisse akzeptiert.

1. Klicken Sie auf **[!UICONTROL Add URL]**.

   ![](../administrating-target/assets/allowlist-2.png)

1. Geben Sie im Dialogfeld die URL oder das Muster ein, die bzw. das Ihr Unternehmen zulassen muss.

   ![](../administrating-target/assets/allowlist-3.png)

1. Speichern Sie Ihre Änderungen.

   Nachdem das Muster auf die Zulassungsliste gesetzt wurde, können Benutzende vorbehaltlich Ihrer anderen [!DNL Target] Aktivitäten und Angebote erstellen oder ausführen, die auf dieser URL basieren.

1. Verwenden Sie das Feld **[!UICONTROL Search URLs]** , um die Tabelle zu filtern.

1. Um eine URL zu löschen, suchen Sie die Zeile für das Muster, das Sie nicht mehr benötigen, und klicken Sie auf das Symbol ![Löschen](../administrating-target/assets/do-not-localize/Smock_Delete_18_N.svg).

   ![](../administrating-target/assets/allowlist-4.png)


