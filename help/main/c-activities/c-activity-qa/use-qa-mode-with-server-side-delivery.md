---
keywords: QS; serverseitig, Server-seitig, Vorschau, Vorschaulinks
description: Erfahren Sie, wie Sie Adobe [!DNL Target] QA-URLs mit serverseitiger Bereitstellung verwenden, um eine einfache End-to-End-Aktivitäts-QA mit Vorschau-Links, die sich nie ändern, optionalem Audience-Targeting und QA-Reporting durchzuführen, die weiterhin von Live-Aktivitätsdaten segmentiert sind.
title: Kann ich Aktivitäts-QA mit serverseitiger Bereitstellung durchführen?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 59%

---

# Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung

Verwenden Sie QA-URLs mit serverseitiger Bereitstellung in [!DNL Adobe Target], um eine einfache End-to-End-Aktivitäts-QA mit Vorschaulinks durchzuführen, die sich nie ändern, optionales Audience-Targeting und QA-Berichte, die aus Live-Aktivitätsdaten segmentiert bleiben.

Die Standardimplementierung der Aktivitäts-QA unterstützt die Übergabe von `qa_mode` über `pageUrl`. Dieser Ansatz ist für Standard-/Ajax-[!DNL Target]-Aufrufe praktisch. Bei serverseitigen Aufrufen ist dies jedoch nicht der beste Ansatz für das Mobile SDK, wenn `pageUrl` nicht verfügbar ist.

Folgendes Codebeispiel zeigt die Aktivitäts-QA in einem serverseitigen Aufruf:

```json
{
  "mbox" : "orderConfirmPage",
  "clientSideAnalyticsLogging": true,
  "clicked" : true,
  "tntId" : "12121212.17_01",
  "order" : {
    ...
  },
  "profileParameters" : {
    ...
  },
  "mboxParameters" : {
    ...
  },
  "requestLocation" : {
    ...
  },
  "qaMode" : {
    "token" : "<encrypted token string>",
    "bypassEntryAudience" : true,
    "listedActivitiesOnly" : true,
    "evaluateAsTrueAudienceIds" : [audienceId1, audienceId2...],
    "evaluateAsFalseAudienceIds" : [audienceId3, audienceId4...],
    "previewIndexes" : [
       {
         "activityIndex" : 1,
         "experienceIndex" : 1
       }
     ],
  },
  "mboxTrace" : true
}
```

Die folgende Tabelle enthält Informationen zu serverseitigen Anfragen:

| Parameter | Typ | Standardwert | Beschreibung |
|--- |--- |--- |--- |
| token | Verschlüsseltes Token | Keine.<br>Darf nicht leer sein. | Ein verschlüsseltes Element, das die Liste der Aktivitäts-IDs enthält, die in der Aktivitäts-QA ausgeführt werden dürfen.<br>Validierungsregeln: Sollte ein verschlüsseltes Token sein, das zu dem in der [!DNL Target]-Anfrage angegebenen Client gehört. Alle im Token angegebenen Aktivitäten müssen zu dem Client gehören. |
| bypassEntryAudience | Boolesch | False | Gibt an, ob Ziele der Einstiegsstufe für QA-Aktivitäten überprüft werden sollen oder als übereinstimmend gelten. |
| listedActivitiesOnly | Boolesch | False | Gibt an, ob QA-Aktivitäten isoliert ausgeführt oder für die aktuelle Umgebung als aktive Aktivitäten bewertet werden sollen. |
| evaluateAsTrueAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Gültigkeitsbereich der [!DNL Target]-Anfrage immer als „true“ ausgewertet werden sollen. |
| evaluateAsFalseAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Gültigkeitsbereich der [!DNL Target]-Anfrage immer als „false“ ausgewertet werden sollen. |
| activityIndex | Ganzzahl | Null.<br>Darf nicht leer sein. | Aktivitätsindex im verschlüsselten Token. Wenn activityIndex außerhalb der Grenzwerte der Aktivität im Token liegt oder null ist, wird er ignoriert. Der Index beginnt bei 1.<br>Validierungsregeln: Sollte mindestens ein Aktivitätsindex sein und auf eine im Token angegebene Aktivität verweisen. |
| experienceIndex | Ganzzahl | Null. | Sofern angegeben, wird ein Erlebnis nach dem Index in der Aktivitätsdefinition ausgewählt. Wenn nicht angegeben oder außerhalb der Grenzwerte, wird stattdessen die Erlebnisselektor-Strategie der Aktivität verwendet. Der Index beginnt mit 1 Validierungsregeln: Kann null sein oder sollte auf ein Erlebnis in der Aktivität verweisen. |
