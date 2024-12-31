---
keywords: Profilskript;Profilskriptattribute;sich gegenseitig ausschließende Aktivitäten
description: Erfahren Sie, wie Sie mit Profilattributen Tests in Adobe einrichten können [!DNL Target]  bei denen mehrere Aktivitäten verglichen werden, aber nicht dieselben Besucher an jeder Aktivität teilnehmen können.
title: Kann ich Profilskripte verwenden, um sich gegenseitig ausschließende Aktivitäten zu testen?
feature: Audiences
exl-id: b0b23887-3339-411e-9f5c-64f9d1ba778c
source-git-commit: 34db233e0790f8ef04309c3f4b5acd12b7cdd5ad
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 72%

---

# Verwenden von Profilskripten zum Testen sich gegenseitig ausschließender Aktivitäten

Sie können in [!DNL Adobe Target] Profilattribute verwenden, um Tests einzurichten, mit denen zwei oder mehr Aktivitäten verglichen werden, aber nicht dieselben Besucher an jeder Aktivität teilnehmen lassen.

Hierdurch wird verhindert, dass ein Besucher einer Aktivität die Testergebnisse der anderen Aktivitäten beeinflusst. Wenn ein Besucher an mehreren Aktivitäten teilnimmt, ist es oft schwierig festzustellen, ob die positiven oder negativen Änderungen auf das Erlebnis des Besuchers in einer Aktivität zurückzuführen sind oder ob die Ergebnisse einer oder mehrerer Aktivitäten durch die Interaktionen zwischen den Aktivitäten beeinflusst wurden.

So können Sie zum Beispiel zwei Bereiche Ihres E-Commerce-Systems testen. Sie können testen, ob Sie die Schaltfläche „Zum Warenkorb hinzufügen“ rot statt blau machen. Vielleicht möchten Sie einen neuen Checkout-Prozess testen, der anstelle von fünf nur noch aus zwei Schritten besteht. Wenn beide Aktivitäten dasselbe Erfolgsereignis aufweisen (ein abgeschlossener Kauf), kann es schwierig sein festzustellen, ob die rote Schaltfläche die Konversionen verbessert oder ob dieselben Konversionen aufgrund des verbesserten Checkout-Prozesses ebenfalls erhöht wurden. Durch Trennung der Tests in zwei sich gegenseitig ausschließende Aktivitäten können Sie jede Veränderung einzeln prüfen.

Beachten Sie die folgenden Informationen, wenn Sie eines der folgenden Profilskripte verwenden:

* Das Profilskript muss ausgeführt werden, bevor die Aktivität gestartet wird, und das Skript muss unverändert bleiben, während die Aktivität ausgeführt wird.
* Durch diese Technik wird der Traffic in der Aktivität reduziert, wodurch die Aktivität möglicherweise länger ausgeführt werden muss. Sie müssen diesen Umstand berücksichtigen, wenn Sie die Dauer der Aktivität schätzen.

## Einrichten von zwei Aktivitäten

Zur Einteilung von Besuchern in Gruppen, denen unterschiedliche Aktivitäten angezeigt werden, müssen Sie ein Profilattribut erstellen. Mit einem Profilattribut lassen sich Besucher auf mehrere Gruppen verteilen. Zur Einrichtung des Profilattributs „twogroups“ erstellen Sie folgendes Skript:

```javascript
if (!user.get('twogroups')) { 
    var ran_number = Math.floor(Math.random() * 100); 
    if (ran_number <= 49) { 
        return 'GroupA'; 
    } else { 
        return 'GroupB'; 
    } 
}
```

* `if (!user.get('twogroups'))` bestimmt, ob das Profilattribut *twogroups* für den aktuellen Besucher eingerichtet ist. Falls ja, sind keine weiteren Aktionen erforderlich.

* `var ran_number=Math.floor(Math.random() *100)` bezeichnet eine neue Variable namens „ran_number“, legt ihren Wert auf eine Zufallsdezimalzahl zwischen 0 und 1 fest, multipliziert diese mit 100 und rundet sie ab, um einen Bereich von 100 (0-100) zu erstellen. Dies ist nützlich zur Angabe des Prozentsatzes von Besuchern, welche die Aktivität sehen.

* `if (ran_number <= 49)` beginnt mit einer Routine, die bestimmt, zu welcher Gruppe der Besucher gehört. Wird eine Zahl zwischen 0 und 49 ausgegeben, wird der Besucher Gruppe A zugewiesen. Wenn die Zahl 50-100 ist, wird der Besucher der Gruppe B zugewiesen. Welche Aktivität der Besucher angezeigt bekommt, wird durch seine Gruppenzugehörigkeit bestimmt.

Richten Sie nach der Erstellung des Profilattributs die erste Aktivität ein, um die gewünschte Population anzusprechen. Dazu muss der Benutzerprofilparameter `user.twogroups` mit dem für Gruppe A angegebenen Wert übereinstimmen.

>[!NOTE]
>
>Wählen Sie am Seitenanfang eine Mbox aus. Dieser Code bestimmt, ob ein Besucher die Aktivität wahrnimmt. Solange zuerst beim Browser eine Mbox auftritt, kann sie zum Festlegen dieses Werts verwendet werden.

Richten Sie die zweite Kampagne so ein, dass der Benutzerprofilparameter `user.twogroups` dem für Gruppe B festgelegten Wert entspricht.

## Einrichten von drei oder mehr Aktivitäten

Die Einrichtung von drei oder mehr Aktivitäten unterscheidet sich nicht wesentlich von der Einrichtung zweier Aktivitäten. Sie müssen jedoch das Profilattribut „JavaScript“ ändern, um eine separate Gruppe für jede Aktivität einzurichten und festzulegen, wem eine Aktivität angezeigt wird. Die Erzeugung von Zufallszahlen ist unterschiedlich. Sie hängt davon ab, ob Sie eine gerade oder ungerade Zahl an Gruppen erstellen.

Zum Erstellen von vier Gruppen verwenden Sie z. B. folgendes JavaScript:

```javascript
if (!user.get('fourgroups')) { 
    var ran_number = Math.floor​(Math.random() * 100); 
    if (ran_number <= 24) { 
        return 'GroupA'; 
    } else if (ran_number <= 49) { 
        return 'GroupB'; 
    } else if (ran_number <= 74) { 
        return 'GroupC'; 
    } else { 
        return 'GroupD'; 
    } 
}
```

In diesen Beispiel wird die Zufallszahl, nach der ein Besucher einer Gruppe zugewiesen wird, nach dem gleichen Prinzip berechnet wie bei zwei Gruppen: Es wird eine Zufallszahl erzeugt, die dann auf eine Ganzzahl abgerundet wird.

Wenn Sie eine ungerade Anzahl an Gruppen erstellen, oder wenn 100 geteilt durch die Anzahl keine Ganzzahl ergibt, sollten Sie die Dezimalstellen nicht auf eine Ganzzahl runden. Durch das Nichtrunden der Dezimalstellen können Sie auch nicht ganzzahlige Bereiche festlegen. Sie können dies durch Änderung folgender Zeile erreichen:

`var ran_number=Math.floor(Math.random()*100);`

an:

`var ran_number=Math.random()*100;`

Zur Aufteilung der Besucher in drei gleiche Gruppen verwenden Sie beispielsweise folgenden Code:

```javascript
if (!user.get('threegroups')) { 
    var ran_number = Math.random() * 100; 
    if (ran_number <= 32.33) { 
        return 'GroupA'; 
    } else if (ran_number <= 65.66) { 
        return 'GroupB'; 
    } else { 
        return 'GroupC'; 
    } 
}
```
