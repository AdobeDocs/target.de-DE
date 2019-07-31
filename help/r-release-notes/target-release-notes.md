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
source-git-commit: 48cb808283c9b2858e1bd041feb3fe8228253d6a

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

Enterprise Permissions allows [!DNL Target] customers to use a single organization, but divide it into workspaces for their different teams or workflows. Dies ermöglicht eine effektive Skalierung ihres Optimierungsprogramms für Teams. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier this year. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, Target Enterprise Permissions will provide customers with the following access controls:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

Dieses Update unterstützt die folgenden Anwendungsfälle:

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Gewähren Sie der Adobe I/O-Integration Zugriff auf ausgewählte Arbeitsbereiche mit der entsprechenden Rolle, damit ein zentrales Team API-basierte Änderungen in nur wenigen Arbeitsbereichen vornehmen kann.
* Jedes Team, das seinen Arbeitsbereich besitzt, beschließt, seine eigene Integration zu haben, sobald das Team bereit ist, apis zu entdecken und die Rolle entsprechend auszuwählen.
* Kombinieren Sie die obigen Szenarien und stimmen Sie überein.

**Erforderliche Aktion**: Diejenigen Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihren vorhandenen Adobe I/O-Integrationszugriff auf alle Arbeitsbereiche mit der gewünschten Rolle gemäß ihrem Verwendungsfall erteilen. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, irrespective of choice made in the [!UICONTROL Product Role] drop-down list. Sie können jetzt die gewünschte Rolle auswählen.

This action *must* be performed before September 4, 2019 to not face any disruption on your end. Wenn diese Aktion nicht durchgeführt wird, nach [! DNL Target September werden die Zugriffssteuerungselemente aktiviert, und Sie werden den Zugriff auf nur den Standardarbeitsbereich beobachten, wenn Sie aktuell eingerichtet sind. Es gibt keine negative Reaktion auf die Einrichtung von Integrationen im Voraus gemäß den oben genannten Richtlinien. Je früher Sie diese Änderung vornehmen, desto besser. Es ist nur wenig Zeit erforderlich, um diese Einstellung einzurichten, je nach Anzahl der Arbeitsbereiche in Ihrer Organisation. Dieser Vorgang erfordert nur einige Klicks, um eine vorhandene Integration in Arbeitsflächen mit der gewünschten Rolle zu integrieren.

## Target Standard/Premium 19.8.1 (20. August 2019) {#tgt-19-8-1}

Dieses Maintenance Release umfasst die folgende Verbesserung:

* Verschiedene Sicherheitsfehlerbehebungen, einschließlich Sicherheits-Updates für Rich-Text-Editor (RTE) im Visual Experience Composer (VEC). (TGT-35383)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
