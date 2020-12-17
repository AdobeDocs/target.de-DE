---
keywords: qa;server side;server-side;preview;preview links
description: Verwenden Sie Adobe Target QA-URLs mit serverseitigem Versand, um eine durchgängige Qualitätssicherung mit Vorschauen-Links durchzuführen, die sich nicht ändern, optionales Audiencen-Targeting und QS-Berichte, der aus Live-Aktivitäten segmentiert bleibt.
title: Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung
feature: Activities
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 73%

---


# Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung{#use-activity-qa-with-server-side-delivery}

Mithilfe von QA-URLs mit serverseitiger Bereitstellung können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.

Die Standardimplementierung der Aktivität QA unterstützt die Übergabe von `qa_mode`-Parametern über `pageUrl`-Parameter. Dieser Ansatz eignet sich für Standard/AJAX [!DNL Target]-Aufrufe. Bei serverseitigen Aufrufen ist dies jedoch nicht der beste Ansatz für das Mobile SDK, wenn `pageUrl` nicht verfügbar ist.

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
| token | Verschlüsseltes Token | Keine.<br>Darf nicht leer sein. | Ein verschlüsseltes Element, das die Liste der Aktivitäts-IDs enthält, die in der Aktivitäts-QA ausgeführt werden dürfen.<br>Validierungsregeln: Sollte ein verschlüsseltes Token sein, das zu dem in der  [!DNL Target] Anforderung angegebenen Client gehört. Alle im Token angegebenen Aktivitäten müssen zu dem Client gehören. |
| bypassEntryAudience | Boolesch | False | Gibt an, ob Ziele der Einstiegsstufe für QA-Aktivitäten überprüft werden sollen oder als übereinstimmend gelten. |
| listedActivitiesOnly | Boolesch | False | Gibt an, ob QA-Aktivitäten isoliert ausgeführt oder für die aktuelle Umgebung als aktive Aktivitäten bewertet werden sollen. |
| evaluateAsTrueAudienceIds | ID-Liste | Leere Liste | Liste von Audiencen-IDs, die im Rahmen der [!DNL Target]-Anforderung immer als &quot;true&quot;bewertet werden sollten. |
| evaluateAsFalseAudienceIds | ID-Liste | Leere Liste | Liste von Audiencen-IDs, die im Gültigkeitsbereich der [!DNL Target]-Anforderung immer als &quot;false&quot;bewertet werden sollten. |
| activityIndex | Ganzzahl | Null.<br>Darf nicht leer sein. | Aktivitätsindex im verschlüsselten Token. Wenn activityIndex außerhalb der Grenzwerte der Aktivität im Token liegt oder null ist, wird er ignoriert. Der Index beginnt bei 1.<br>Validierungsregeln: Sollte mindestens ein Aktivitätsindex sein und auf eine im Token angegebene Aktivität verweisen. |
| experienceIndex | Ganzzahl | Null. | Sofern angegeben, wird ein Erlebnis nach dem Index in der Aktivitätsdefinition ausgewählt. Wenn nicht angegeben oder außerhalb der Grenzwerte, wird stattdessen die Erlebnisselektor-Strategie der Aktivität verwendet. Der Index beginnt bei 1.  Validierungsregeln: Kann null sein oder auf ein Erlebnis in einer Aktivität verweisen. |