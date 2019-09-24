---
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.
keywords: Versionshinweise
seo-description: Versionshinweise mit Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder kommenden [!DNL Adobe Target]-Versionen.
seo-title: Adobe Target-Versionshinweise (Vorabversion)
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: d675c6875c8474ba490956ea395076eef5b9e58f

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

**31. Juli 2019**

[!UICONTROL Enterprise Permissions] ermöglicht es [!DNL Target] Kunden, ein Unternehmen zu verwenden, unterteilt es jedoch in Arbeitsbereiche für verschiedene Teams oder Arbeitsabläufe. Die [!UICONTROL Funktion "Berechtigungen] für Unternehmen"erleichtert die effektive Skalierung von Optimierungsprogrammen in allen Teams. Obwohl diese Funktion in der [!DNL Target] Benutzeroberfläche verfügbar war, fehlte den Admin-APIs bis zur Version [!DNL Target] vom Februar 2019 die entsprechende Unterstützung. Adobe hat die Admin-APIs aktualisiert, damit Sie mit dem Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsflächen zugreifen können. Während sich die Admin-APIs früher auf den Standardarbeitsbereich beschränkten, gewährte das Update vom Februar 2019 Zugriff auf alle Arbeitsbereiche mit Zugriff auf [!UICONTROL Genehmigende Benutzer] .

Ab der kommenden Version [!DNL Target] September 2019 bieten [!UICONTROL Enterprise Permissions] den Kunden die folgenden Zugriffskontrollen:

* Sie können die Arbeitsbereiche auswählen, auf die die Integration angewendet werden kann
* Sie können eine Rolle auf die Adobe I/O-Integration anwenden: [!UICONTROL Genehmigende Person], [!UICONTROL Editor]oder [!UICONTROL Beobachter].

**Aktion erforderlich**: Kunden, die derzeit APIs für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) in allen Arbeitsbereichen nutzen, müssen ihren bestehenden Adobe-I/O-Integrationszugriff auf alle Arbeitsbereiche mit der gewünschten Rolle gewähren. Vor der Version vom September wurden alle Integrationen mit [!UICONTROL genehmigenden] Zugriff ausgeführt, unabhängig von der Rolle, die in der Dropdownliste [!UICONTROL Produktrolle] ausgewählt wurde. Mit der kommenden Version können Sie jetzt die gewünschte Rolle auswählen.

Diese Aktion sollte im Monat **August 2019** durchgeführt werden. Nach der Version [!DNL Target] vom September 2019 werden die Zugriffskontrollen aktiviert und Sie werden den Zugriff auf den Standardarbeitsbereich beobachten, wenn Sie so eingerichtet sind. Die vorzeitige Einrichtung von Integrationsrollen hat keine nachteiligen Folgen.

For step-by-step instructions and more information, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.9.2 (30. September 2019)

Dieses Maintenance Release umfasst die folgende Verbesserung:

* Several security fixes, including a security update to the Rich Text Editor (RTE) in the Visual Experience Composer (VEC). (TGT-35383)

## Target Standard/Premium 19.9.1 (10. September 2019)

| Funktion / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) Enterprise Permissions | With the Target September 2019 release, Enterprise Permissions provides customers with the following access controls:<UL><li>You can choose the workspaces to which the integration can be applied.</li><li>You can apply a role to the Adobe I/O integration: Approver, Editor, or Observer.</li></ul>For step-by-step instructions and more information, see Grant Adobe I/O integrations access to workspaces and assign roles.[](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md) |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
