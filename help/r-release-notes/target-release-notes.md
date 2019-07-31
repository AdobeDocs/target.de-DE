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
source-git-commit: b88460fbd90168ddc19cbae1939b47ac69a854a8

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

**31. Juli 2019**: [!UICONTROL Mit der Enterprise-Berechtigung] können [!DNL Target] Kunden eine einzige Organisation verwenden, sie jedoch in Arbeitsflächen für verschiedene Teams oder Arbeitsabläufe unterteilen.

The [!UICONTROL Enterprise Permissions] feature facilitates effective scaling of optimization programs across teams. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier in 2019. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!DNL Target] [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

**Erforderliche Aktion**: Diejenigen Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihren vorhandenen Adobe I/O-Integrationszugriff auf alle Arbeitsbereiche mit der gewünschten Rolle gemäß ihrem Verwendungsfall erteilen. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of choice made from the [!UICONTROL Product Role] drop-down list. Sie können jetzt die gewünschte Rolle auswählen.

This action should be performed before **September 4, 2019** to not face any disruption on your end. If this action is not performed, after the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. Es gibt keine negative Reaktion auf die Einrichtung von Integrationen im Voraus. Je früher Sie diese Änderung vornehmen, desto besser. Es ist nur wenig Zeit erforderlich, um diese Einstellung einzurichten, je nach Anzahl der Arbeitsbereiche in Ihrer Organisation. Dieser Vorgang erfordert nur einige Klicks, um eine vorhandene Integration in Arbeitsflächen mit der gewünschten Rolle zu integrieren.

For step-by-step instructions, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.8.1 (20. August 2019) {#tgt-19-8-1}

Dieses Maintenance Release umfasst die folgende Verbesserung:

* Verschiedene Sicherheitsfehlerbehebungen, einschließlich Sicherheits-Updates für Rich-Text-Editor (RTE) im Visual Experience Composer (VEC). (TGT-35383)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
