---
title: Kontextattribute erstellen
description: Erfahren Sie, wie Sie Kontextattribute und Kontextgruppen in Flags erstellen und organisieren, damit Sie sie in Zielgruppenkriterien verwenden können.
hide: true
source-git-commit: 9c6f2b72f964b06da51e1f3655545147d7240a93
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 5%

---

# Kontextattribute erstellen {#creating-your-context-attributes}

Kontextattribute sind benutzerdefinierte Datenfelder, die den Benutzer-, Sitzungs- oder Anwendungskontext beschreiben (z. B. Abonnementebene, App-Version oder Region). Verwenden Sie Kontextattribute, um Zielgruppenkriterien für Feature Flags zu definieren.

Kontextgruppen organisieren verwandte Kontextattribute in einer logischen Hierarchie. Verwenden Sie Kontextgruppen, um das Auffinden und Verwalten von Attributen während der Funktionskonfiguration zu erleichtern.

| Begriff | Beschreibung | Verwendet in |
| --- | --- | --- |
| **Kontextattribut** | Ein benanntes Feld mit einem Datentyp und optionalen vordefinierten Werten. | Zielgruppenkriterien, Funktionskonfiguration |
| **Kontextgruppe** | Eine Kategorie, die verwandte Kontextattribute organisiert. | Kontextauswahl beim Erstellen einer Funktion |
| **UI-Bezeichnung** | Der auf der Benutzeroberfläche angezeigte Anzeigename. | Zielgruppenkriterien und Verwaltungsseiten |
| **ID** | Eine eindeutige technische Kennung. | Anwendungsanfragen |
| **Vordefinierte Werte** | Eine optionale Liste mit zulässigen Werten mit Anzeigebezeichnungen. | Dropdown-Listen und Builder für Zielgruppenregeln |

## Voraussetzungen {#prerequisites}

Bevor Sie Kontextattribute und Kontextgruppen verwalten, führen Sie die folgenden Schritte aus:

* Sie haben Zugriff auf die **Flags-Konsole** in der richtigen Sandbox.
* Sie verfügen über die **Admin**-Rolle, die zum Erstellen und Verwalten von Kontextattributen und Kontextgruppen erforderlich ist.

## Navigieren zu Kontextattributen {#navigate}

1. Melden Sie sich bei der **Flags-Konsole** an.
1. Wählen Sie in der linken Navigation unter **Dashboards** die Option **Kontextattribute** aus.

Sie befinden sich jetzt auf der Seite **Kontextattribute**. Verwenden Sie diese Seite, um Kontextgruppen und Kontextattribute zu erstellen.

## Erstellen einer Kontextgruppe {#create-group}

Jedes Kontextattribut muss einer Gruppe angehören.

1. Wählen Sie in der linken Navigation unter **Dashboards** die Option **Kontextattribute** aus.
1. Wählen Sie auf **Registerkarte** Meine Kontextattribute“ die Option **Gruppe hinzufügen** aus.
1. Füllen Sie die Pflichtfelder aus.
1. Wählen Sie **Erstellen** aus.

### Felder gruppieren {#group-fields}

| Feld | Beschreibung |
| --- | --- |
| **Gruppenname** | Geben Sie einen eindeutigen Namen für die Gruppe ein. |
| **Eine Untergruppe bilden von** | Wählen Sie eine übergeordnete Gruppe aus, um die Hierarchie zu organisieren. Sie können beim Erstellen eines Attributs auch eine Gruppe erstellen. |

## Kontextattribut erstellen {#create-attribute}

1. Wählen Sie auf **Registerkarte** Meine Kontextattribute **die Option Neues** aus.
1. Füllen Sie die Pflichtfelder aus.
1. Wählen Sie **Senden** aus.

### Attributfelder {#attribute-fields}

| Feld | Beschreibung |
| --- | --- |
| **UI-Bezeichnung** | Geben Sie den Anzeigenamen ein, der in den Zielgruppenkriterien verwendet wird. |
| **ID** | Geben Sie eine eindeutige technische Kennung ein, die in den Anwendungsanfragen verwendet wird. |
| **Kontextgruppe** | Wählen Sie eine Gruppe aus oder erstellen Sie eine neue Gruppe inline. |
| **Datentyp** | Wählen Sie den Typ aus, der den von Ihrer Anwendung gesendeten Daten entspricht. |

| Datentyp | Beispiel |
| --- | --- |
| ZEICHENFOLGE | `gold` |
| GANZZAHL | `42` |
| BOOLESCH | `true` |
| DEZIMAL | `9.99` |
| DATUM | `2026-07-17` |
| VERSION | `1.2.0` |

### Vordefinierte Werte (optional) {#predefined-values}

Verwenden Sie vordefinierte Werte, um ein Attribut auf einen festen Satz von Werten zu beschränken. Wählen Sie **Vordefinierte Werte hinzufügen** aus.

| Feld | Beschreibung |
| --- | --- |
| **UI-Bezeichnung** | Geben Sie den Anzeigenamen ein. |
| **Wert** | Geben Sie den von der Anwendung gesendeten technischen Wert ein. |

Klicken Sie **Speichern**, um Ihre Änderungen anzuwenden.

## Fehlerbehebung {#troubleshooting}

| Fehler | Auflösung |
| --- | --- |
| **Erstellen** ist deaktiviert | Füllen Sie sowohl **Gruppenname** als auch **eine Untergruppe von)**. |
| Attribut kann nicht gesendet werden | Vollständige **ID** und **Kontextgruppe**. |
| Gruppe nicht im Dropdown-Menü sichtbar | Aktualisieren Sie die Seite oder erstellen Sie die Gruppe inline über das Attributformular. |
| Vordefinierte Werte werden nicht gespeichert | Wählen **im Modal &quot;**&quot; aus, bevor Sie das Attribut übermitteln. |

## Siehe auch {#see-also}

* [Erstellen und Verwenden von Regelsätzen](creating-and-using-rule-sets.md)
* [Verwenden des Kontexts in Zielgruppenregeln](using-context-in-audience-rules.md)
* [Zielgruppe in Feature Flags und Feature Groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
