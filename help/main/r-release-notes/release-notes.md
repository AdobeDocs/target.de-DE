---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 3d8da94a52046e70a89dc24d7923f743bee5c458
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 83%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 22.9.1 (gestaffelte Veröffentlichung vom 13. bis 15. September 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **13. September**: Region Europa, Naher Osten und Afrika (EMEA)
* **14. September**: Amerikanische Region
* **15. September**: Region Asien-Pazifik (APAC)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Beim Herunterladen von at.js 2.10.0 (und höher) wurde eine Option [!UICONTROL Domain-übergreifend] hinzugefügt, um das Setzen von Drittanbieter-Cookies zu erlauben oder zu deaktivieren. (TGT-43674)
* Aktualisierte Benachrichtigungen im [!DNL Target] Benutzeroberfläche, die Kunden über den Import von [!DNL Recommendations] Feeds schlagen fehl. (TGT-35811)
* Es wurde ein Problem behoben, das dazu führte, dass [!UICONTROL Entscheidungsangebote] innerhalb des [!UICONTROL Visual Experience Composer] (VEC) nicht richtig funktionierten. (TGT-43866)
* Es wurde ein Problem behoben, durch das eine Fehlermeldung angezeigt wurde, wenn bei der Erstellung einer [!UICONTROL multivariaten Testaktivität] (MVT) das Konversionsziel [!UICONTROL Auf ein Element geklickt] ausgewählt wurde. (TGT-43842)
* Es wurde ein Problem behoben, das die Anzeige der Spalte [!UICONTROL Impressions] in der heruntergeladenen CSV-Berichtsdatei für Aktivitäten der [!UICONTROL Automated Personalization] (AP) verhinderte. (TGT-43780)
* Es wurde ein Problem behoben, das Kunden daran hinderte, HTML/JSON-Angebote nach dem Duplizieren von Erlebnissen zu bearbeiten, wenn sie die [!UICONTROL Form-Based Experience Composer] verwendeten. (TGT-43633)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine [!UICONTROL A/B-Test]-Aktivität von einem nicht standardmäßigen Arbeitsbereich in einen anderen nicht standardmäßigen Arbeitsbereich zu kopieren. (TGT-41910)
* Es wurde ein Problem behoben, das sicherstellte, dass Kunden die Verwendung von [!DNL Recommendations] Objekte (Designs, Kriterien, Sammlungen usw.) in [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT)-Aktivitäten, die Empfehlungen enthalten, sowie Kriterienobjekte löschen, die nicht mehr in verwendet werden [!DNL Target] Benutzeroberfläche und [!DNL Recommendations] Backend. (TGT-42331)
* Es wurde ein Fehler behoben, der dazu führte, dass eine Warnung zur Netzwerk-Zeitüberschreitung im [!DNL Target] Benutzeroberfläche beim Abrufen von Parametern. (TGT-43737)
* Die Benutzeroberfläche wurde aktualisiert, um sicherzustellen, dass bestimmte Drag &amp; Drop-Aktionen über die Tastatur zugänglich sind. (TGT-42969)
* Die Benutzeroberfläche wurde aktualisiert, um sicherzustellen, dass Textzeichenfolgen ordnungsgemäß lokalisiert sind.

## at.js-Version 2.10.0 (13. September 2022)

* Beim Herunterladen von at.js 2.10.0 (und höher) wurde eine Option [!UICONTROL Domain-übergreifend] hinzugefügt, um das Setzen von Drittanbieter-Cookies zu erlauben oder zu deaktivieren. (TGT-43674)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority Product Update | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md). |
