---
title: Verwenden des Kontexts in Zielgruppenregeln
description: Erfahren Sie, wie Sie Kontextattribute in Zielgruppenregeln für Feature Flags und Feature Groups in Flags verwenden.
badge: label="Beta" type="Informative"
hide: true
exl-id: 0367f475-9209-4d53-86b4-a739a73a23a7
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# Verwenden des Kontexts in Zielgruppenregeln {#context-in-audience-rules}

Kontextattribute sind Werte, die von der Client-Anwendung zur Laufzeit bereitgestellt werden. Sie ermöglichen es Ihnen, Benutzende auf der Grundlage dynamischer Informationen auf Sitzungsebene anzusprechen, wie z. B. die aktive Sprache des Benutzers, der Gerätetyp oder der Anwendungsstatus.

Kontextattribute sind für Web- und Mobile-Clients relevant.

## So funktionieren Kontextattribute {#how-context-attributes-work}

Ihre Anwendung übergibt beim Bewerten eines Feature Flags Kontextattribute an Flags. Sie definieren in der Konsole Regeln, die diese Werte überprüfen, und die Plattform verwendet sie zum Zeitpunkt der Auswertung, um festzustellen, ob der Benutzer qualifiziert ist.

## Kontextattribut hinzufügen {#adding-context-attribute}

So fügen Sie einer Zielgruppenregel ein Kontextattribut hinzu:

1. Öffnen Sie das Feature Flag oder die Feature Group in der Konsole.
2. Navigieren Sie zur Registerkarte **Zielgruppe** .
3. Fügen **unter &quot;**&quot; eine neue Bedingung hinzu.
4. Wählen Sie das Kontextattribut, den Operator und den Wert aus.

Wenn das benötigte Kontextattribut nicht in der Liste angezeigt wird, können Sie ein neues erstellen - siehe &quot;[ von Kontextattributen](creating-your-context-attributes.md).

## Siehe auch {#see-also}

* [Zielgruppe in Feature Flags und Feature Groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
