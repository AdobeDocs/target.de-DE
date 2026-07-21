---
title: Erstellen und Verwenden von Regelsätzen
description: Erfahren Sie, wie Sie in Flags einen wiederverwendbaren Regelsatz von Zielgruppen-Kontextkriterien erstellen und in Feature Flags und Feature Groups importieren.
hide: true
source-git-commit: 9c6f2b72f964b06da51e1f3655545147d7240a93
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 1%

---

# Erstellen und Verwenden von Regelsätzen {#creating-and-using-rule-sets}

Ein Regelsatz ist eine wiederverwendbare Sammlung von Zielgruppen-Kontextkriterien. Erstellen Sie einen Regelsatz, wenn mehrere Feature Flags oder Feature Groups dieselbe Audience benötigen. Anschließend können Sie den Regelsatz importieren, anstatt die Zielgruppenkriterien für jede Funktion neu zu erstellen.

## Anforderungen an Regelsätze {#requirements}

| UI-Kennzeichnung | Verwenden | Erforderlich |
| --- | --- | --- |
| **Regelsatz eingeben** | Geben Sie einen Namen für den Regelsatz ein. | Ja |
| **Regelsatzbeschreibung** | Beschreiben Sie den Zweck des Regelsatzes. | Nein |
| **Kontext** | Definieren Sie mindestens ein Zielgruppenkriterium. Kontextattribute sind benannte Felder wie Abonnementebene, Anwendungsversion oder Region. | Ja |

## Erstellen eines Regelsatzes {#create-rule-set}

### Schritt 1: Neuen Regelsatz starten {#step-1-start}

Wählen Sie in **im linken Navigationsbereich die Option** Regelsatz“ und dann **Neuer Regelsatz** aus.

Auf **Registerkarte „Mein Regelsatz** werden die von Ihnen erstellten Regelsätze angezeigt. Auf **Registerkarte** Team-Regelsatz“ werden die Ihrem Team zur Verfügung stehenden Regelsätze angezeigt.

![Regelsatzliste ohne noch erstellte Regelsätze](assets/rule-set-list-empty.png)

### Schritt 2: Regelsatzdetails und -kriterien hinzufügen {#step-2-details}

1. Geben Sie einen Namen für den Regelsatz ein.
1. Geben Sie optional eine Beschreibung ein.
1. Definieren **unter &quot;**&quot; die Zielgruppenkriterien, die Sie wiederverwenden möchten.
1. Verwenden Sie **Und** oder **Oder** um mehrere Kriterien zu kombinieren.
1. Um einen komplexeren Ausdruck zu erstellen, wählen Sie **Verschachtelte Logik aktivieren**.

![Formular zur Erstellung von Regelsätzen mit Beispiel-Kontextkriterien](assets/rule-set-create-context.png)

### Schritt 3: Regelsatz speichern {#step-3-save}

Wählen Sie **Einstellungen speichern**. Der gespeicherte Regelsatz wird unter &quot;**Regelsatz“**.

![Regelsatzliste mit einem neu gespeicherten Regelsatz](assets/rule-set-list-created.png)

## Verwenden eines Regelsatzes in einem Feature Flag oder einer Feature Group {#use-rule-set}

### Schritt 1: Audience-Einstellungen öffnen und aktivieren {#step-1-open}

Öffnen Sie die Feature Flag oder Feature Group, in der Sie den Regelsatz verwenden möchten, wählen Sie die Registerkarte **Audience** und aktivieren Sie dann **Audience Rule**, um Audience-Kriterien zu aktivieren.

### Schritt 2: Regelsatz auswählen {#step-2-select}

Öffnen Sie das **Regelsatz auswählen** Dropdown. Wählen Sie den Regelsatz aus **Mein Regelsatz** oder **Mein Team-Regelsatz**.

![Wählen Sie das Dropdown-Menü Regelsatz aus, das auf der Registerkarte Zielgruppe geöffnet ist](assets/rule-set-select-in-audience.png)

### Schritt 3: Importierte Kriterien überprüfen {#step-3-review}

Die Kontextkriterien des ausgewählten Regelsatzes werden in die Zielgruppe importiert. Überprüfen Sie die Kriterien und speichern Sie dann das Feature Flag oder die Feature Group.

![Registerkarte „Feature Flag Zielgruppe“ mit importierten Regelsatzkriterien](assets/rule-set-imported-audience.png)

Sie können denselben Regelsatz in mehreren Funktions-Flags und Funktionsgruppen verwenden, die dieselbe Zielgruppe benötigen.

### Schritt 4: Feature Flag oder Feature Group speichern {#step-4-save}

Wählen Sie nach Überprüfung der importierten Zielgruppenkriterien **Einstellungen speichern**.

>[!NOTE]
>
>Beim Importieren eines Regelsatzes werden die Zielgruppenkriterien in das Feature Flag oder die Feature Group kopiert. Wenn die Zielgruppenkriterien später aktualisiert werden müssen, aktualisieren Sie sie separat in jeder Funktions-Flag und Funktionsgruppe, in die der Regelsatz importiert wurde. Beim Aktualisieren des ursprünglichen Regelsatzes werden zuvor importierte Zielgruppen nicht automatisch aktualisiert.

## Erstellen eines Regelsatzes aus einem Feature Flag oder einer Feature Group {#create-from-feature}

Sie können einen Regelsatz auch direkt über den Bildschirm „Zielgruppe“ einer Feature Flag oder Feature Group erstellen:

1. Öffnen Sie das Feature Flag oder die Feature Group und wählen Sie dann die Registerkarte **Audience** aus.
1. „Zielgruppenregel **aktivieren**.
1. Definieren Sie die Kontextkriterien, die Sie wiederverwenden möchten.
1. Klicken Sie auf die Schaltfläche **+** oben rechts neben dem Dropdown-Menü **Regelsatz auswählen**.
1. Geben **im Dialogfeld „Regelsatz speichern** einen Namen für den Regelsatz ein.
1. Wählen **Regelsatz speichern**.

## Siehe auch {#see-also}

* [Kontextattribute erstellen](creating-your-context-attributes.md)
* [Verwenden des Kontexts in Zielgruppenregeln](using-context-in-audience-rules.md)
* [Zielgruppe in Feature Flags und Feature Groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
