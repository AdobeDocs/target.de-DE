---
keywords: Versionshinweise;Versionen;Updates;Zukünftige Versionen;Verbesserungen;Neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: ' Versionshinweise '
translation-type: tm+mt
source-git-commit: 453106f7534f83c205722421bbf00044fde7da67
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 25%

---


# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 17. Februar 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Adobe empfiehlt, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

## Target Standard/Premium 21.2.1 (9. und 10. März 2021)

Dieses Maintenance Release umfasst die folgenden Erweiterungen, Fehlerbehebungen und Änderungen.

Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

* Zulässige Angebot-Größe erhöht:

   | Typ  | Vorherige Beschränkung | Neue Beschränkung |
   | --- | --- | --- |
   | HTML | 256 KB | 1024 KB |
   | Visuelle Angebot aus der Benutzeroberfläche der Zielgruppe | 64 KB | 1024 KB für jedes Erlebnis |
   | Über API | 512 KB | 1024 KB |

* Es wurde ein Fehler behoben, der dazu führte, dass die aktuelle Abhängigkeit nicht angezeigt wurde, wenn Kunden auf der Seite [!UICONTROL Ziele und Einstellungen] der Aktivität auf [!UICONTROL Abhängigkeit bearbeiten klicken. ] (TGT-39340)
* Es wurde ein Problem beim Aktualisieren der [!UICONTROL Audience-Bibliothek eines Arbeitsbereichs] behoben. Vor der Aktualisierung wurden die Audiencen für den aktuell ausgewählten Arbeitsbereich angezeigt. Nach der Aktualisierung wurden der [!UICONTROL Standardarbeitsbereich] und die zugehörigen Audiencen angezeigt. Die aktuelle Arbeitsfläche und ihre Audiencen bleiben nun nach der Aktualisierung erhalten. (TGT-38871)
* Es wurde ein Fehler behoben, der beim Kopieren einer [!UICONTROL Recommendations]-Aktivität und späteren Bearbeiten der ursprünglichen Aktivität durch Ändern der Kriteriensequenz auftrat. Die Änderung der Kriteriensequenz in der ursprünglichen Aktivität wurde auch auf die kopierte Aktivität falsch angewendet. (TGT-39155)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
