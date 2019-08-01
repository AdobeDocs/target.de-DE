---
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [! DNL Adobe Target] veröffentlicht.
keywords: Versionshinweise
seo-description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [! DNL Adobe Target] veröffentlicht.
seo-title: Versionshinweise zu Adobe Target (Vorabversion)
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: e1174aacc5610878c8671e88fbd20d51fedffe6c

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert am 31. Juli 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungsdaten, Funktionen und andere Informationen können ohne vorherige Benachrichtigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Mitteilungen

**31. Juli 2019**

[!UICONTROL Mit Unternehmensberechtigungen] können [!DNL Target] Kunden eine einzige Organisation verwenden, sie jedoch in Arbeitsflächen für verschiedene Teams oder Arbeitsabläufe unterteilen. The [!UICONTROL Enterprise Permissions] feature facilitates effective scaling of optimization programs across teams. Although this feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until the [!DNL Target] February 2019 release. Adobe hat die Admin-apis aktualisiert, damit Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. So, while earlier, Admin APIs were restricted to the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

**Erforderliche Aktion**: Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihre vorhandene Adobe I/O-Integration für alle Arbeitsbereiche mit der gewünschten Rolle bereitstellen. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of the role selected from the [!UICONTROL Product Role] drop-down list. In der kommenden Version können Sie jetzt die gewünschte Rolle auswählen.

This action should be performed during the month of **August 2019**. After the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. Es gibt keine negativen Auswirkungen auf die Einrichtung von Integrationsrollen im Voraus.

For step-by-step instructions and more information, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.8.1 (20. August 2019) {#tgt-19-8-1}

Dieses Maintenance Release umfasst die folgende Verbesserung:

* Verschiedene Sicherheitsfehlerbehebungen, einschließlich Sicherheits-Updates für Rich-Text-Editor (RTE) im Visual Experience Composer (VEC). (TGT-35383)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
