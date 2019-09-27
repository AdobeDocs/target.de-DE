---
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder kommenden Adobe Target-Versionen enthalten.
keywords: Versionshinweise;Versionen;Aktualisierungen;Zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen
seo-description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
seo-title: Adobe Target-Versionshinweise (Vorabversion)
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 1d91c46c78c0bcb58607def4cacaff0b761162fa

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Letzte Aktualisierung: 24. September 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Mitteilungen

**31. Juli 2019**

Mit [!UICONTROL Unternehmensberechtigungen] können [!DNL Target]-Kunden eine Organisation in Arbeitsbereiche für verschiedene Teams oder Arbeitsabläufe unterteilen. Die Funktion [!UICONTROL Unternehmensberechtigungen] ermöglicht die Aufteilung von Optimierungsprogrammen auf Teams. Die Funktion war zwar in der [!DNL Target] -Benutzeroberfläche verfügbar, die Admin-APIs werden aber erst seit der [!DNL Target]-Verson vom Februar 2019 unterstützt. Adobe aktualisierte die Admin-APIs, sodass Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. Zuvor waren Admin-APIs auf den Standardarbeitsbereich beschränkt. Das Update vom Februar 2019 ermöglichte dann den Zugriff auf alle Arbeitsbereiche mit der Rolle [!UICONTROL Genehmiger].

Ab der neuen [!DNL Target]Version vom September 2019 bieten [!UICONTROL Unternehmensberechtigungen] die folgenden Zugriffskontrollen:

* Sie können die Arbeitsbereiche auswählen, auf die die Integration angewendet wird.
* Sie können der Adobe I/O-Integration eine Rolle zuweisen: [!UICONTROL Genehmiger], [!UICONTROL Bearbeiter] oder [!UICONTROL Beobachter].

**Erforderliche Aktion**: Kunden, die derzeit APIs für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) in allen Arbeitsbereichen verwenden, müssen ihrer vorhandenen Adobe I/O-Integration Zugriff auf alle Arbeitsbereiche erteilen und die entsprechende Rolle zuweisen. Vor der September-Version wurden alle Integrationen mit der Rolle [!UICONTROL Genehmiger] ausgeführt, unabhängig davon, welche Rolle in der Dropdownliste [!UICONTROL Produktrolle] ausgewählt wurde. In der kommenden Version können Sie die gewünschte Rolle auswählen.

Diese Aktion sollten Sie im **August 2019** ausführen. Die Zugriffskontrolle wird ab der [!DNL Target]-Version vom September 2019 aktiviert und Sie werden dann nur auf den Standard-Arbeitsbereich zugreifen können, sofern dies Ihre aktuelle Einstellung ist. Das vorzeitige Einrichten von Integrationen hat keine Nachteile.

Schrittweise Anleitungen und weitere Informationen finden Sie unter [Gewähren von Zugriff von Adobe I/O Integrationen auf Arbeitsbereiche und Zuweisen von Rollen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.9.2 (30. September 2019)

Dieser Maintenance Release enthält die folgende Verbesserung:

* Verschiedene Korrekturen von Sicherheitsfehlern, einschließlich eines Sicherheits-Updates für den Rich-Text-Editor (RTE) im Visual Experience Composer (VEC). (TGT-35383)

## Target Standard/Premium 19.9.1 (10. September 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium-Zeichen](/help/assets/premium.png) für Unternehmen | With the Target September 2019 release, Enterprise Permissions provides customers with the following access controls:<UL><li>You can choose the workspaces to which the integration can be applied.</li><li>Sie können der Adobe I/O-Integration eine Rolle zuweisen: Genehmiger, Bearbeiter oder Beobachter.</li></ul>Schrittweise Anleitungen und weitere Informationen finden Sie unter [Gewähren von Zugriff von Adobe I/O Integrationen auf Arbeitsbereiche und Zuweisen von Rollen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
