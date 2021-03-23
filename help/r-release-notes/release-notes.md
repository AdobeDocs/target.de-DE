---
keywords: Versionshinweise;Neue Funktionen;Releases;Updates;Update;Release;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerbehebungen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: ' Versionshinweise '
translation-type: tm+mt
source-git-commit: 695e997ecb0a0acc6d9c20eb2cab3f4647602615
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 37%

---


# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Migrieren Sie vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

(Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## at.js 2.4.1 (23. März 2021)

Diese Version von at.js ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:

* Es wurde ein Problem behoben, bei dem `targetPageParams` in Mbox-Anforderungen enthalten war. `targetPageParams` sollte nur in  `pageLoad` Anforderungen enthalten sein. (TNT-40247)
* Optimierte Fenster- und Dokument-Globalen, die auf die Erweiterung [!DNL Adobe Experience Platform Launch] verweisen. (TNT-37124)

## Änderungen der IP-Adresse für Recommendations-Feed-Verarbeitungsserver (16. März 2021)

Die IP-Adressen der Feed-Verarbeitungsserver wurden am 16. März 2021 aktualisiert. [!DNL Target Recommendations] Weitere Informationen finden Sie unter [IP-Adressen, die von Recommendations-Feed-Processing-Servern verwendet werden](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md).

## Target Standard/Premium 21.2.1 (9. März 2021) 

Dieses Maintenance Release umfasst die folgenden Erweiterungen, Fehlerbehebungen und Änderungen.

Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

* Zulässige Größe des Angebots erhöht (TGT-38304):

   | Typ  | Vorherige Beschränkung | Neue Beschränkung |
   | --- | --- | --- |
   | HTML | 256 KB | 1024 KB |
   | Visuelle Angebot aus der Benutzeroberfläche der Zielgruppe | 64 KB | 1024 KB für jedes Erlebnis |
   | Über API | 512 KB | 1024 KB |

* [!UICONTROL Personalization Insight ] Reports für  [!UICONTROL Auto-Zielgruppe] -(AT) und  [!UICONTROL Automated Personalization] (AP)-Aktivitäten werden jetzt täglich erstellt. Sie können einen Bericht auswählen, der für die letzten 15, 30 und 60 Tage [!UICONTROL Automatisierte Segmente] oder [!UICONTROL Wichtige Attribute] bereitstellt. Die 45-Tage- und 90-Tage-Optionen wurden entfernt, damit die anderen Einstellungen des Lookback-Fensters täglich ausgeführt werden können. (TGT-39472)
* Es wurde ein Fehler behoben, der dazu führte, dass die aktuelle Abhängigkeit nicht angezeigt wurde, wenn Kunden auf der Seite [!UICONTROL Ziele und Einstellungen] der Aktivität auf [!UICONTROL Abhängigkeit bearbeiten klicken. ] (TGT-39340)
* Es wurde ein Problem beim Aktualisieren der [!UICONTROL Audience-Bibliothek eines Arbeitsbereichs] behoben. Vor der Aktualisierung wurden die Audiencen für den aktuell ausgewählten Arbeitsbereich angezeigt. Nach der Aktualisierung wurden der [!UICONTROL Standardarbeitsbereich] und die zugehörigen Audiencen angezeigt. Die aktuelle Arbeitsfläche und ihre Audiencen bleiben nun nach der Aktualisierung erhalten. (TGT-38871)
* Es wurde ein Fehler behoben, der beim Kopieren einer [!UICONTROL Recommendations]-Aktivität und späteren Bearbeiten der ursprünglichen Aktivität durch Ändern der Kriteriensequenz auftrat. Die Änderung der Kriteriensequenz in der ursprünglichen Aktivität wurde auch auf die kopierte Aktivität falsch angewendet. (TGT-39155)
* Es wurde ein Fehler behoben, der dazu führte, dass die falsche Produktanzahl für [!UICONTROL Recommendations]-Ausschlüsse angezeigt wurde. (TGT-39599)

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Detaillierte Informationen zur Ansicht zu Aktualisierungen in diesem Handbuch, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu  [Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Produktaktualisierung mit Priorität für Adoben | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
