---
title: Verwenden des Kontexts in Zielgruppenregeln
description: Erfahren Sie, wie Sie Kontextattribute in Zielgruppenregeln für Feature Flags und Feature Groups in Flags verwenden.
badge: label="Beta" type="Informative"
hide: true
exl-id: 0367f475-9209-4d53-86b4-a739a73a23a7
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
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

Wenn das benötigte Kontextattribut nicht in der Liste angezeigt wird, können Sie ein neues erstellen - siehe &quot;[&#x200B; von Kontextattributen](creating-your-context-attributes.md).

## Siehe auch {#see-also}

* [Zielgruppe in Feature Flags und Feature Groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
