---
keywords: QS; serverseitig, Server-seitig, Vorschau, Vorschaulinks
description: Erfahren Sie, wie Sie Adobe- [!DNL Target] QA-URLs mit serverseitiger Bereitstellung verwenden, um eine einfache End-to-End-Aktivitäts-QA mit Vorschau-Links, die sich nie ändern, optionalem Audience-Targeting und QA-Reporting durchzuführen, die von Live-Aktivitätsdaten segmentiert bleiben.
title: Kann ich Aktivitäts-QA mit serverseitiger Bereitstellung durchführen?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
TQID: 'https://experienceleague.adobe.com/zZJmFqpXtAigTiEWMZhRqXBJqvG3ANLussSPE3-NoDA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0a683f6e68bb7481b9e45c91a275a46b84a1ffd8
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 18%
---
# Verwenden von Aktivitäts-QA mit serverseitiger Bereitstellung {#qa-server-side}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Aktivitäts-QA-Parameter in einem Server-seitigen [!DNL Adobe Target] übergeben können, damit Sie Aktivitäten testen können, wenn `pageUrl` nicht verfügbar ist.

>[!ENDSHADEBOX]

Die Standardimplementierung der Aktivitäts-QA unterstützt die Übergabe von `qa_mode` über `pageUrl`. Dieser Ansatz ist für Standard-/Ajax-[!DNL Target]-Aufrufe praktisch. Sie ist jedoch nicht für Server-zu-Server-Aufrufe geeignet, z. B. eine Mobile SDK-Implementierung, bei der keine `pageUrl` verfügbar ist. Übergeben Sie in diesen Fällen die QA-Parameter in der Anfrage selbst. In der Anfrage werden dieselben Vorschau-Links, optionalen Zielgruppen-Targeting- und QA-Berichte gespeichert, die aus den Live-Aktivitätsdaten segmentiert sind.

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

In der folgenden Tabelle werden die Parameter einer Server-seitigen Anfrage beschrieben:

| Parameter | Typ | Standardwert | Beschreibung |
|--- |--- |--- |--- |
| token | Verschlüsseltes Token | Keine. Darf nicht leer sein. | Eine verschlüsselte Entität, die die Liste der Aktivitäts-IDs enthält, die in Aktivitäts-QA ausgeführt werden dürfen.<br>Validierungsregeln: Das Token muss ein verschlüsseltes Token sein, das zu dem in der [!DNL Target]-Anfrage angegebenen Client gehört. Alle im Token angegebenen Aktivitäten müssen zum Client gehören. |
| bypassEntryAudience | Boolesch | False | Gibt an, ob Zielgruppen für Einstiegsschritte für QA-Aktivitäten ausgewertet werden oder als übereinstimmend betrachtet werden. |
| listedActivitiesOnly | Boolesch | False | Gibt an, ob QS-Aktivitäten isoliert ausgeführt oder als aktive Aktivitäten für die aktuelle Umgebung ausgewertet werden. |
| evaluateAsTrueAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Gültigkeitsbereich der [!DNL Target] immer als „true“ ausgewertet werden. |
| evaluateAsFalseAudienceIds | ID-Liste | Leere Liste | Liste der Zielgruppen-IDs, die im Gültigkeitsbereich der [!DNL Target]-Anfrage immer als falsch ausgewertet werden. |
| activityIndex | Ganzzahl | Null. Darf nicht leer sein. | Aktivitätsindex im verschlüsselten Token. Wenn `activityIndex` null ist oder außerhalb der Grenzen der Aktivitäten im Token liegt, wird es ignoriert. Der Index beginnt mit 1<br>Validierungsregeln: Mindestens ein Aktivitätsindex ist erforderlich und muss auf eine im Token angegebene Aktivität verweisen. |
| experienceIndex | Ganzzahl | Null | Sofern angegeben, wird ein Erlebnis nach dem Index in der Aktivitätsdefinition ausgewählt. Wenn sie nicht angegeben ist oder außerhalb der Grenzen liegt, wird auf die Erlebnisauswahlstrategie der Aktivität zurückgegriffen. Der Index beginnt mit 1<br>Validierungsregeln: Der Wert kann null sein oder auf ein Erlebnis in der Aktivität verweisen. |
