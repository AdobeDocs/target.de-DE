---
description: Liste der häufig gestellten Fragen (FAQs) zu Recommendations-Entwürfen.
keywords: Empfehlungen; häufig gestellte Fragen; FAQ
seo-description: Liste der häufig gestellten Fragen (FAQs) zu Recommendations-Entwürfen.
seo-title: 'Häufig gestellte Fragen: Entwürfe'
solution: Target
title: 'Häufig gestellte Fragen: Entwürfe'
title-outputclass: premium
topic: Premium
uuid: ac222ade-ddd9-4b32-a16f-4d83b8766384
badge: premium
translation-type: tm+mt
source-git-commit: 279b6bef59e0b486a9aad7f3b6117edbbe377688

---


# ![PREMIUM](/help/assets/premium.png) Design-FAQ {#design-faq}

Liste der häufig gestellten Fragen (FAQs) zu Recommendations-Entwürfen.

## Der Preis meines empfohlenen Artikels zeigt nicht beide Werte rechts vom Dezimalpunkt an. Wie kann ich sie anzeigen?

Standardmäßig werden in den in den Designvorlagen zurückgegebenen numerischen Werten (z. `entity.value`B.) nach dem Dezimalpunkt keine nachfolgenden Nullen angezeigt. Wenn ein Element beispielsweise 35,00 US-Dollar hat, `entity.value` gleich 35 und nur 35 auf der Seite angezeigt wird, nicht 35,00 $.

Für dieses Problem stehen zwei Optionen zur Verfügung.

* Sie können die Velocity-Skripterstellung oder Javascript verwenden, um die Formatierung auf den zurückgegebenen Wert anzuwenden.

* Sie können den Preis des Elements in zwei separate Entitätsattribute übergeben. Die erste kann `entity.value`für numerische Vergleiche verwendet werden (z. B. Preisvergleichsregeln). Die zweite sollte ein benutzerdefiniertes Attribut sein, z. B. `entity.displayValue` der Wert der Entität als Zeichenfolge speichert, um eine ordnungsgemäße Wiedergabe zu ermöglichen.

   Beispiel:

   `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## Warum wird die Kategorie im Entwurf nicht angezeigt? Ich verwende $entity1.categoryId. {#section_073309B8051049C7953D396A93EA0713}

Die Kategorie-ID kann nicht in dem Entwurf angezeigt werden. Da mehrere Kategorien gespeichert werden können, kann das System nicht ermitteln, welche Kategorie angezeigt werden sollte.

## Wie kann ich einen Entwurf so ändern, dass ein sofortiges Update erfolgt? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

Wenn Sie den aktuell verwendeten Entwurf ändern, erfolgt das entsprechende Update erst nach einiger Zeit. Wenn Sie den Entwurf sofort ändern möchten, erstellen Sie einen neuen Entwurf, wählen Sie diesen in der Kampagne aus und speichern Sie die Empfehlung.

## Wie können wesentliche Informationen für eine Anzeige in dem Entwurf erfasst werden? Beispiel: Wenn die Kategorie des Schlüsselprodukts angezeigt werden soll, wie kann dieser Wert in dem Velocity-Entwurf codiert werden? {#section_F08043B14BA24BC8815FEF25F4F84C39}

Der Parameter `$key. *`Wert`*` erfasst die meisten Informationen des Schlüsselprodukts, die innerhalb des Entwurfs angezeigt werden. Beispiel: Wenn Sie die Miniaturansicht des Schlüsselprodukts anzeigen möchten, sollten Sie `$key.thumbnailURL` verwenden.

## Welche Version von Velocity wird verwendet? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

Version 1.7 ohne zusätzliche Tools oder eingefügte Bibliotheken. Grundlegende Velocity-Funktionen sind verfügbar.

## Wie ersetze ich einen bestehenden Entitätswert durch einen leeren Wert? Beispielsweise muss entity.message eines Artikels zum Ende einer Promotion gelöscht werden. {#section_B88F2C2925DC4508974B2F8B13F961CB}

Dies scheint mit der Übermittlung eines geschützten Leerzeichens in JavaScript zu funktionieren. Lassen Sie die Entwickler `\u00A0` als Wert einschicken. Beispiel: `entity.message=\u00A0`. Sie können dies auch anstelle einer Null als Standardwert festlegen, wenn kein Wert vorhanden ist.

## Kann ich in einem Recommendations-Entwurf ein Profilskript verwenden? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Ja. Sie müssen jedoch vor dem $ im Profilskriptnamen einen linksseitigen Schrägstrich (\) hinzufügen.
