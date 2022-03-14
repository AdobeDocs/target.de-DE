---
keywords: QS; serverseitig, Server-seitig, Vorschau, Vorschaulinks
description: Erfahren Sie, wie Sie Adobe verwenden [!DNL Target] QA-URLs mit serverseitiger Bereitstellung zur einfachen End-to-End-Aktivitäts-QAs mit unveränderbaren Vorschaulinks, optionalem Zielgruppen-Targeting und QA-Berichten, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.
title: Kann ich Aktivitäts-QA mit serverseitiger Bereitstellung durchführen?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 63%

---

# Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung

Verwenden von QA-URLs mit serverseitiger Bereitstellung in [!DNL Adobe Target] zur einfachen End-to-End-Aktivitäts-QA mit unveränderbaren Vorschaulinks, optionalem Zielgruppen-Targeting und QA-Berichten, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.

Die Standardimplementierung der Aktivitäts-QA unterstützt die Übergabe von `qa_mode` Parameter über `pageUrl` Parameter. Dieser Ansatz eignet sich für Standard/Ajax. [!DNL Target] -Aufrufe. Bei serverseitigen Aufrufen ist dies jedoch nicht der beste Ansatz für das Mobile SDK, wenn `pageUrl` nicht verfügbar ist.

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
| token | Verschlüsseltes Token | Keine.<br>Darf nicht leer sein. | Ein verschlüsseltes Element, das die Liste der Aktivitäts-IDs enthält, die in der Aktivitäts-QA ausgeführt werden dürfen.<br>Validierungsregeln: Sollte ein verschlüsseltes Token sein, das zum Client gehört, der in der Datei [!DNL Target] -Anfrage. Alle im Token angegebenen Aktivitäten müssen zu dem Client gehören. |
| bypassEntryAudience | Boolesch | False | Gibt an, ob Ziele der Einstiegsstufe für QA-Aktivitäten überprüft werden sollen oder als übereinstimmend gelten. |
| listedActivitiesOnly | Boolesch | False | Gibt an, ob QA-Aktivitäten isoliert ausgeführt oder für die aktuelle Umgebung als aktive Aktivitäten bewertet werden sollen. |
| evaluateAsTrueAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Bereich der [!DNL Target] -Anfrage. |
| evaluateAsFalseAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Bereich der [!DNL Target] -Anfrage. |
| activityIndex | Ganzzahl | Null.<br>Darf nicht leer sein. | Aktivitätsindex im verschlüsselten Token. Wenn activityIndex außerhalb der Grenzwerte der Aktivität im Token liegt oder null ist, wird er ignoriert. Der Index beginnt bei 1.<br>Validierungsregeln: Sollte mindestens ein Aktivitätsindex sein und auf eine im Token angegebene Aktivität verweisen. |
| experienceIndex | Ganzzahl | Null. | Sofern angegeben, wird ein Erlebnis nach dem Index in der Aktivitätsdefinition ausgewählt. Wenn nicht angegeben oder außerhalb der Grenzwerte, wird stattdessen die Erlebnisselektor-Strategie der Aktivität verwendet. Der Index beginnt bei 1.  Validierungsregeln: Kann null sein oder auf ein Erlebnis in einer Aktivität verweisen. |
