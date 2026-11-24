---
keywords: Empfehlungen;häufig gestellte Fragen;FAQ
description: Häufig gestellte Fragen (FAQs) und Antworten zu [!DNL Target Recommendations].
title: 'Häufig gestellte Fragen: Entwürfe'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
TQID: 'https://experienceleague.adobe.com/xRu0XEnc8wX8PZngba7CO67mFdja7HALL-1OSnhAmuY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: d5030abcda38bbc6d33b88ce3bb5d64f69e4e492
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 19%
---
# Häufig gestellte Fragen: Entwürfe {#design-faq}

>[!BEGINSHADEBOX]

**Auf dieser Seite** finden Sie Antworten auf häufig gestellte Fragen zu [!DNL Adobe Target] [!DNL Recommendations].

>[!ENDSHADEBOX]

+++ Wie kann der Preis eines empfohlenen Artikels beide Ziffern rechts vom Dezimalpunkt anzeigen?

Standardmäßig zeigen in Designs zurückgegebene numerische Werte (z. B. `entity.value`) nach dem Dezimalpunkt keine nachfolgenden Nullen an. Beispiel: Wenn ein Artikel 35,00 $ kostet, `entity.value` gleich 35 ist und nur 35 $ auf der Seite angezeigt werden, nicht 35,00 $.

Zur Behebung dieses Problems stehen zwei Möglichkeiten zur Verfügung:

* Velocity-Skripterstellung oder JavaScript können Formatierungen auf den zurückgegebenen Wert anwenden.

* Der Preis des Artikels kann in zwei separate Entitätsattribute übergeben werden. Das erste, `entity.value`, kann für numerische Vergleiche verwendet werden (z. B. Preisvergleichsregeln). Das zweite sollte ein benutzerdefiniertes Attribut sein, z. B. `entity.displayValue`, das den Wert der Entität als Zeichenfolge speichert, um eine ordnungsgemäße Wiedergabe zu ermöglichen.

  Beispiel:

  `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

+++

+++ Warum wird die Kategorie nicht im Design angezeigt, wenn $entity1.categoryId verwendet wird?

Die Kategorie-ID kann in einem Design nicht angezeigt werden. Es können mehrere Kategorien gespeichert werden, sodass das System nicht weiß, welche Kategorie angezeigt werden soll.

+++

+++ Wie kann ein Design geändert werden, um eine sofortige Aktualisierung zu erhalten?

Wenn Sie den aktuell verwendeten Entwurf ändern, erfolgt das entsprechende Update erst nach einiger Zeit. Wenn Sie den Entwurf sofort ändern möchten, erstellen Sie einen neuen Entwurf, wählen Sie diesen in der Aktivität aus und speichern Sie die Empfehlung.

+++

+++ Wie können Schlüsselinformationen, wie z. B. die Kategorie des Schlüsselprodukts, in einem Design angezeigt werden?

Die `$key`-Parameter erfassen die meisten Informationen des Schlüsselprodukts zur Anzeige innerhalb des Designs. Um beispielsweise die Miniaturansicht des wichtigsten Produkts anzuzeigen, verwenden Sie `$key.thumbnailURL`.

+++

+++ Welche Version von Velocity wird verwendet?

Version 1.7 ohne zusätzliche Tools oder Bibliotheken. Grundlegende Velocity-Funktionen sind verfügbar.

+++

+++ Wie kann ein vorhandener Entitätswert durch ein leeres ersetzt werden, z. B. wenn entity.message eines Elements am Ende einer Promotion gelöscht werden muss?

Dazu wird scheinbar ein unterbrechungsfreies Leerzeichen in JavaScript gesendet. Die Entwickler senden `\u00A0` als Wert, z. B. `entity.message=\u00A0`. Die Verwendung dieses Werts als Standard, wenn kein Wert anstelle eines Nullwerts vorhanden ist, kann ebenfalls in Betracht gezogen werden.

+++

+++ Kann ein Profilskript in einem [!DNL Recommendations]-Design verwendet werden?

Ja. Um ein Profilskript in einem [!DNL Recommendations]-Design zu verwenden, schließen Sie den Namen in `\${...}` ein. Wenn das Profilskript beispielsweise `user.basket` heißt, verweisen Sie im Entwurf darauf als `\${user.basket}`. Der umgekehrte Schrägstrich bedeutet, dass das Profilskript nicht von Velocity gerendert wird, sodass keine Vorgänge für das Profilskript in einer Velocity-Vorlage ausgeführt werden können. Der Wert wird direkt auf der Seite gedruckt.

+++
