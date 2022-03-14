---
keywords: API;Adobe I/O
description: Erfahren Sie, wie Sie aus der Adobe wechseln [!DNL Target] Klassische ältere APIs für die neuen APIs in Adobe I/O.
title: Wie kann ich von alten APIs zu Adobe I/O wechseln?
feature: Implement Server-side
role: Developer
exl-id: 4b4274a9-b91a-4a79-9b40-8b1909a2d1d1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 83%

---

# Übergang von [!DNL Target] Legacy-APIs für Adobe I/O

Informationen für einen leichteren Übergang von den Target-Vorgänger-APIs zu den neuen APIs in Adobe I/O.

Mit der Außerbetriebnahme von Adobe Target Classic stehen auch die mit Ihrem Target Classic-Konto verknüpften APIs nicht mehr zur Verfügung. Dieses Dokument enthält Informationen, die Ihnen beim Übergang von Ihren alten API-basierten Integrationen zu den Target-APIs von Adobe I/O helfen.

Weitere Informationen zur Target-API-Dokumentation finden Sie unter  [Target-APIs und NodeJS-SDK](/help/main/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md#concept_5718EC1FF2ED4436935D0BCCD7AA29A6).

## Terminologie   {#section_D8286EDAE3B24D208DA432AEF2E88FD9}

| Begriff | Beschreibung |
|--- |--- |
| Vorgänger-API | Mit Ihrem Target Classic-Konto verknüpfte APIs. Diese API-Aufrufe basieren auf einer Benutzername-und-Kennwort-basierten Authentifizierung und verwenden den Hostnamen `testandtarget.omniture.com`. Wenn Ihre API-Aufrufe einen Benutzernamen und ein Kennwort in der Anforderungs-URL enthalten, müssen Sie auf Adobe I/O-APIs umstellen. |
| Adobe I/O | Adobe I/O ist das neue Gateway für Target-APIs. Diese APIs sind mit Ihrem Target Standard/Premium-Konto verknüpft. Die Target-APIs in Adobe I/O nutzen eine JWT-basierte Authentifizierung, die dem Branchenstandard für sichere Unternehmens-APIs entspricht. |

## Timeline  {#section_A478EBF637554A2DB5A31661955121ED}

Die Vorgänger-APIs werden im Rahmen der Außerbetriebnahme von Target Classic eingestellt:

| Datum | Details |
|--- |--- |
| 17. Oktober 2017 | Alle API-Methoden, die einen Schreibvorgang (`saveCampaign`, `copyCampaign`, `saveHTMLOfferContent` und `setCampaignState`) durchführen, wurden beendet.<br>Dies ist dasselbe Datum, an dem alle Target Classic-Benutzerkonten auf schreibgeschützt gesetzt wurden. |
| 14. November 2017 | Die verbleibenden APIs wurden eingestellt. Dies ist das Datum, an dem die Target Classic-Benutzeroberfläche eingestellt wurde. |

Recommendations Classic-APIs sind von diesem Zeitplan nicht betroffen.

## Äquivalente Methoden  {#section_DDB42CCC172545B09CB728D794CC466B}

In der folgenden Tabelle werden die äquivalenten neuen Target API-Methoden für die alten API-Methoden aufgeführt. Die neuen APIs geben im Vergleich zur XML-Antwort von den Vorgänger-APIs JSON zurück.

Die neuen API-Methoden sind mit dem entsprechenden Abschnitt auf der API-Dokumentations-Website verknüpft. Für jede API-Methode wird ein Beispiel angegeben. Sie können auch die Admin Postman Collection verwenden, die API-Beispielaufrufe für alle neuen Adobe API-Methoden in Adobe I/O enthält.

| Gruppierung | Vorgänger-API-Methode | Neue API-Methode | Hinweise |
|--- |--- |--- |--- |
| Kampagne/Aktivität | Kampagnenerstellung | [AB-Aktivität erstellen](https://developers.adobetarget.com/api/#create-ab-activity)<br>[XT-Aktivität erstellen](https://developers.adobetarget.com/api/#create-xt-activity) | Die neuen APIs enthalten separate Erstellungsmethoden für AB und XT |
|  | Kampagnenaktualisierung | [AB-Aktivität aktualisieren](https://developers.adobetarget.com/api/#update-ab-activity)<br>[XT-Aktivität aktualisieren](https://developers.adobetarget.com/api/#update-xt-activity) |  |
|  | Kampagne kopieren | Nicht zutreffend | APIs zum Erstellen von Aktivitäten verwenden |
|  | Kampagnenliste | [Listenaktivitäten](https://developers.adobetarget.com/api/#list-activities) |  |
|  | Kampagnenstatus | [Aktivitätsstatus aktualisieren](https://developers.adobetarget.com/api/#update-activity-state) |  |
|  | Kampagnenansicht | [AB-Aktivität nach ID abrufen](https://developers.adobetarget.com/api/#get-ab-activity-by-id)<br>[XT-Aktivität nach ID abrufen](https://developers.adobetarget.com/api/#get-xt-activity-by-id) |  |
|  | Drittanbieter-Kampagnen-ID | Nicht zutreffend | Wenn Sie eine thirdpartyID verwenden, können die relevanten Aktivitätsmethoden verwendet werden |
| Angebote | Angebotserstellung | [Angebot erstellen](https://developers.adobetarget.com/api/#create-offer) |  |
|  | Angebotsabruf | [Angebot nach ID abrufen](https://developers.adobetarget.com/api/#get-offer-by-id) |  |
|  | Angebotsliste | [Angebote auflisten](https://developers.adobetarget.com/api/#list-offers) |  |
|  | Ordnerliste | Nicht zutreffend | Ordner werden in Target Standard/Premium nicht unterstützt |
| Berichterstellung | Kampagnenleistungsbericht | [AB-Leistungsbericht abrufen](https://developers.adobetarget.com/api/#get-ab-performance-report)<br>[XT-Leistungsbericht abrufen](https://developers.adobetarget.com/api/#get-xt-performance-report) |  |
|  | Audit-Bericht | [Audit-Bericht abrufen](https://developers.adobetarget.com/api/#get-audit-report) |  |
|  | 1-1-Inhaltsbericht | [AP-Leistungsbericht abrufen](https://developers.adobetarget.com/api/#get-ap-activity-performance-report) |  |
| Kontoeinstellungen | Hostgruppen abrufen | [Umgebungen auflisten](https://developers.adobetarget.com/api/#list-environments) |  |

## Ausnahmen {#section_09CF9A0E289149279783B4801D1B6D4C}

Wenn Sie eine Ausnahme benötigen, wenden Sie sich an den Kundenerfolgsmanager.

## Hilfe  {#section_591F850E2B7A4342B1C233693425415C}

Wenden Sie sich an den Adobe Target-Kundendienst (tt-support@adobe.com), wenn Sie Fragen haben oder beim Übergang zu den neuen Target-APIs in Adobe I/O Hilfe benötigen.