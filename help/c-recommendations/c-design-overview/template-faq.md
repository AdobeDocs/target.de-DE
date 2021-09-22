---
keywords: Empfehlungen; häufig gestellte Fragen; FAQ
description: Überprüfen Sie eine Liste häufig gestellter Fragen (FAQs) und ihre Antworten auf Adobe [!DNL Target] Recommendations-Designs.
title: Wo kann ich auf Designfragen für [!DNL Target] Recommendations antworten?
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
source-git-commit: c7d5c8eb50b28ee3f7651e510d005e3f37912f62
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 70%

---

# ![PREMIUM](/help/assets/premium.png) Design-FAQ

Liste der häufig gestellten Fragen (FAQs) zu [!DNL Adobe Target] [!DNL Recommendations] Designs.

## Der Preis meines empfohlenen Artikels zeigt nicht beide Ziffern rechts vom Dezimalzeichen an. Wie kann ich sie anzeigen?

Standardmäßig werden bei numerischen Werten (z. B. `entity.value`), die in Designvorlagen zurückgegebenen werden, nach dem Dezimalzeichen keine Nullen angezeigt. Wenn ein Artikel beispielsweise 35,00 $ kostet, ist `entity.value` gleich 35, und nur „35“ wird auf der Seite angezeigt, und nicht „35,00“ $.

Zur Behebung dieses Problems stehen zwei Möglichkeiten zur Verfügung:

* Sie können Velocity-Skripts oder JavaScript verwenden, um die Formatierung auf den zurückgegebenen Wert anzuwenden.

* Sie können den Preis des Artikels zwei separaten Entitätsattributen übermitteln. Das erste, `entity.value`, kann für numerische Vergleiche verwendet werden (z. B. Preisvergleichsregeln). Das zweite sollte ein benutzerdefiniertes Attribut sein, z. B. `entity.displayValue`, das den Wert der Entität als Zeichenfolge speichert, um eine korrekte Darstellung zu ermöglichen.

   Beispiel:

   `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## Warum wird die Kategorie im Entwurf nicht angezeigt? Ich verwende `$entity1.categoryId`. {#section_073309B8051049C7953D396A93EA0713}

Die Kategorie-ID kann nicht in dem Entwurf angezeigt werden. Da mehrere Kategorien gespeichert werden können, kann das System nicht ermitteln, welche Kategorie angezeigt werden sollte.

## Wie kann ich einen Entwurf so ändern, dass ein sofortiges Update erfolgt?  {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

Wenn Sie den aktuell verwendeten Entwurf ändern, erfolgt das entsprechende Update erst nach einiger Zeit. Um den Entwurf sofort zu ändern, erstellen Sie einen neuen Entwurf, wählen Sie ihn in der Aktivität aus und speichern Sie die Empfehlung.

## Wie können wesentliche Informationen für eine Anzeige in dem Entwurf erfasst werden? Beispiel: Wenn die Kategorie des Schlüsselprodukts angezeigt werden soll, wie kann dieser Wert in dem Velocity-Entwurf codiert werden?  {#section_F08043B14BA24BC8815FEF25F4F84C39}

Der Parameter `$key. *`Wert`*` erfasst die meisten Informationen des Schlüsselprodukts, die innerhalb des Entwurfs angezeigt werden. Beispiel: Wenn Sie die Miniaturansicht des Schlüsselprodukts anzeigen möchten, sollten Sie `$key.thumbnailURL` verwenden.

## Welche Version von Velocity wird verwendet? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

Version 1.7 ohne zusätzliche Tools oder eingefügte Bibliotheken. Grundlegende Velocity-Funktionen sind verfügbar.

## Wie ersetze ich einen bestehenden Entitätswert durch einen leeren Wert? Beispielsweise muss entity.message eines Artikels zum Ende einer Promotion gelöscht werden. {#section_B88F2C2925DC4508974B2F8B13F961CB}

Das Senden in ein JavaScript-geschütztes Leerzeichen scheint dies zu tun. Lassen Sie die Entwickler `\u00A0` als Wert einschicken. Beispiel: `entity.message=\u00A0`. Sie können dies auch anstelle einer Null als Standardwert festlegen, wenn kein Wert vorhanden ist.

## Kann ich ein Profilskript in einem [!DNL Recommendations]-Design verwenden? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Ja. Um ein Profilskript in einem [!DNL Recommendations]-Design zu verwenden, schließen Sie den Namen in `\${...}` ein. Wenn Ihr Profilskript beispielsweise `user.basket` heißt, verweisen Sie es im Entwurf auf `\${user.basket}`. Beachten Sie, dass der umgekehrte Schrägstrich bedeutet, dass das Profilskript nicht von Velocity gerendert wird. Daher können Sie keine Vorgänge für das Profilskript in einer Velocity-Vorlage durchführen. Der Wert wird direkt auf der Seite gedruckt.
