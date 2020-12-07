---
keywords: qa;server side;server-side;preview;preview links
description: Mithilfe von QA-URLs mit serverseitiger Bereitstellung können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.
title: Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung
feature: qa
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 82%

---


# Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung{#use-activity-qa-with-server-side-delivery}

Mithilfe von QA-URLs mit serverseitiger Bereitstellung können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.

The standard implementation of Activity QA supports passing `qa_mode` parameters via `pageUrl` parameters. This approach is convenient for standard/ajax [!DNL Target] calls. Bei serverseitigen Aufrufen ist dies jedoch nicht der beste Ansatz für das Mobile SDK, wenn `pageUrl` nicht verfügbar ist.

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
| token | Verschlüsseltes Token | Keine.<br>Darf nicht leer sein. | Ein verschlüsseltes Element, das die Liste der Aktivitäts-IDs enthält, die in der Aktivitäts-QA ausgeführt werden dürfen.<br>Validierungsregeln: Sollte ein verschlüsseltes Token sein, das zu dem in der [!DNL Target] Anforderung angegebenen Client gehört. Alle im Token angegebenen Aktivitäten müssen zu dem Client gehören. |
| bypassEntryAudience | Boolesch | False | Gibt an, ob Ziele der Einstiegsstufe für QA-Aktivitäten überprüft werden sollen oder als übereinstimmend gelten. |
| listedActivitiesOnly | Boolesch | False | Gibt an, ob QA-Aktivitäten isoliert ausgeführt oder für die aktuelle Umgebung als aktive Aktivitäten bewertet werden sollen. |
| evaluateAsTrueAudienceIds | ID-Liste | Leere Liste | List of audience IDs that should always be evaluated as true in the scope of the [!DNL Target] request. |
| evaluateAsFalseAudienceIds | ID-Liste | Leere Liste | List of audience IDs that should always be evaluated as false in the scope of the [!DNL Target] request. |
| activityIndex | Ganzzahl | Null.<br>Darf nicht leer sein. | Aktivitätsindex im verschlüsselten Token. Wenn activityIndex außerhalb der Grenzwerte der Aktivität im Token liegt oder null ist, wird er ignoriert. Der Index beginnt bei 1.<br>Validierungsregeln: Sollte mindestens ein Aktivitätsindex sein und auf eine im Token angegebene Aktivität verweisen. |
| experienceIndex | Ganzzahl | Null. | Sofern angegeben, wird ein Erlebnis nach dem Index in der Aktivitätsdefinition ausgewählt. Wenn nicht angegeben oder außerhalb der Grenzwerte, wird stattdessen die Erlebnisselektor-Strategie der Aktivität verwendet. Der Index beginnt bei 1.  Validierungsregeln: Kann null sein oder auf ein Erlebnis in einer Aktivität verweisen. |