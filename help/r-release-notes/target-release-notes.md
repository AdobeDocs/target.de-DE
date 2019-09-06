---
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [! DNL Adobe Target] veröffentlicht.
keywords: Versionshinweise
seo-description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [! DNL Adobe Target] veröffentlicht.
seo-title: Adobe Target-Versionshinweise (Vorabversion)
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 27963738d0935427bd9c96df6922911394df31c3

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Letzte Aktualisierung: 6. September 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Mitteilungen

**31. Juli 2019**

[!UICONTROL Mit Unternehmensberechtigungen] können [!DNL Target] Kunden eine einzige Organisation verwenden, sie jedoch in Arbeitsflächen für verschiedene Teams oder Arbeitsabläufe unterteilen. Mit der [!UICONTROL Funktion für Unternehmensberechtigungen] können optimierte Optimierungsprogramme für Teams optimiert werden. Obwohl diese Funktion in der [!DNL Target] Benutzeroberfläche verfügbar war, konnten die Admin-apis bis zum Release [!DNL Target] von Februar 2019 die entsprechende Unterstützung ablesen. Adobe hat die Admin-apis aktualisiert, damit Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. Zuvor waren Admin-apis also auf den Standardarbeitsbereich beschränkt. Das Update vom Februar 2019 ermöglichte den Zugriff auf alle Arbeitsbereiche mit [!UICONTROL dem Genehmigerzugriff.]

Ab der neuen [!DNL Target] Version September 2019 [!UICONTROL stehen Kunden die folgenden] Zugriffssteuerungsmöglichkeiten zur Verfügung:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* Sie können eine Rolle auf die Integration von Adobe I/O anwenden: [!UICONTROL Genehmigende Person], [!UICONTROL Editor]oder [!UICONTROL Beobachter].

**Erforderliche Aktion**: Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihre vorhandene Adobe I/O-Integration für alle Arbeitsbereiche mit der gewünschten Rolle bereitstellen. Vor der September-Version wurden alle Integrationen, die mit [!UICONTROL dem Genehmiger ausgeführt wurden,] unabhängig von der Rolle, die in der Dropdownliste [!UICONTROL "Produktrolle] " ausgewählt wurde, verwendet. In der kommenden Version können Sie jetzt die gewünschte Rolle auswählen.

Diese Aktion sollte im **August 2019** durchgeführt werden. Nach der Version [!DNL Target] vom September 2019 werden die Zugriffssteuerungselemente aktiviert und Sie werden nur auf den Standardarbeitsbereich zugreifen, wenn Sie aktuell eingerichtet sind. Es gibt keine negativen Auswirkungen auf die Einrichtung von Integrationsrollen im Voraus.

Schrittweise Anweisungen und weitere Informationen finden Sie unter [Gewähren von Adobe I/O-Integrationen auf Arbeitsflächen und Zuweisen von Rollen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.9.1 (10. September 2019)

| Funktion / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium-Badge](/help/assets/premium.png) Enterprise-Berechtigungen | Ab der kommenden Version von Target September 2019 stehen Kunden die folgenden Zugriffssteuerungsmöglichkeiten zur Verfügung:<UL><li>Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.</li><li>Sie können eine Rolle auf die Integration von Adobe I/O anwenden: Genehmigende Person, Editor oder Beobachter.</li></ul>Schrittweise Anweisungen und weitere Informationen finden Sie unter [Gewähren von Adobe I/O-Integrationen auf Arbeitsflächen und Zuweisen von Rollen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

## Target Standard/Premium 19.9.2 (24. September 2019)

Dieses Maintenance Release umfasst die folgende Verbesserung:

* Verschiedene Sicherheitsfehlerbehebungen, einschließlich Sicherheits-Updates für Rich-Text-Editor (RTE) im Visual Experience Composer (VEC). (TGT-35383)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
