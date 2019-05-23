---
description: Mithilfe von QA-URLs mit serverseitiger Bereitstellung können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.
keywords: QS; serverseitig, Server-seitig, Vorschau, Vorschaulinks
seo-description: Mithilfe von QA-URLs mit serverseitiger Bereitstellung können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.
seo-title: Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung
solution: Target
title: Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung
topic: Advanced,Standard,Classic
uuid: c1875243-e37f-4205-9e6b-6e96cadf4a7f
translation-type: tm+mt
source-git-commit: 32eb575df3129e7452a1c794cb7ac03e641e829c

---


# Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung{#use-activity-qa-with-server-side-delivery}

Mithilfe von QA-URLs mit serverseitiger Bereitstellung können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.

Die Standardimplementierung der Aktivitäts-QS unterstützt die Übergabe von `qa_mode`-Parametern über `pageUrl`-Mbox-Parameter. Dieser Ansatz eignet sich für Standard-/Ajax-Mbox-Aufrufe. Bei serverseitigen Aufrufen ist dies jedoch nicht der beste Ansatz für das Mobile SDK, wenn `pageUrl` nicht verfügbar ist.

Folgendes Codebeispiel zeigt die Aktivitäts-QA in einem serverseitigen Aufruf:

```
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
| token | Verschlüsseltes Token | Keine.<br>Darf nicht leer sein. | Ein verschlüsseltes Element, das die Liste der Aktivitäts-IDs enthält, die in der Aktivitäts-QA ausgeführt werden dürfen.<br>Validierungsregeln: Sollte ein verschlüsseltes Token sein, das zum Client gehört, der in der Mbox-Anfrage angegeben ist. Alle im Token angegebenen Aktivitäten müssen zu dem Client gehören. |
| bypassEntryAudience | Boolesch | False | Gibt an, ob Ziele der Einstiegsstufe für QA-Aktivitäten überprüft werden sollen oder als übereinstimmend gelten. |
| listedActivitiesOnly | Boolesch | False | Gibt an, ob QA-Aktivitäten isoliert ausgeführt oder für die aktuelle Umgebung als aktive Aktivitäten bewertet werden sollen. |
| evaluateAsTrueAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Rahmen der Mbox-Anfrage immer mit „true“ bewertet werden sollen. |
| evaluateAsFalseAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Rahmen der Mbox-Anfrage immer mit „false“ bewertet werden sollen. |
| activityIndex | Ganzzahl | Null.<br>Darf nicht leer sein. | Aktivitätsindex im verschlüsselten Token. Wenn activityIndex außerhalb der Grenzwerte der Aktivität im Token liegt oder null ist, wird er ignoriert. Der Index beginnt bei 1.<br>Validierungsregeln: Sollte mindestens ein Aktivitätsindex sein und auf eine im Token angegebene Aktivität verweisen. |
| experienceIndex | Ganzzahl | Null. | Sofern angegeben, wird ein Erlebnis nach dem Index in der Aktivitätsdefinition ausgewählt. Wenn nicht angegeben oder außerhalb der Grenzwerte, wird stattdessen die Erlebnisselektor-Strategie der Aktivität verwendet. Der Index beginnt bei 1.  Validierungsregeln: Kann null sein oder auf ein Erlebnis in einer Aktivität verweisen. |