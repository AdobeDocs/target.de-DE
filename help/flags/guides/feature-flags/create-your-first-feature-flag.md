---
title: Erstellen des ersten Feature Flags
description: Erfahren Sie, wie Sie ein Feature Flag in Flags erstellen, eine Zielgruppe festlegen und testen, bevor Sie es für Benutzer einführen.
hide: true
exl-id: ae115120-8da9-465e-a556-c17591ea7054
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 2%

---

# Erstellen des ersten Feature Flags {#create-feature-flag}

## Voraussetzungen {#prerequisites}

Bevor Sie ein Feature Flag erstellen, führen Sie Folgendes aus:

* Sie haben Zugriff auf die Konsole „Flags“ — siehe [Bei Konsole anmelden](../console/log-in-to-the-console.md)
* Ihr Programm wurde integriert - siehe [Onboarding Ihres Programms](../applications/onboard-your-application.md)
* Sie haben die Rolle **Produktversionsinhaber**.

## Schritt 1: Feature Flag erstellen {#create}

Gehen Sie wie folgt vor, um ein neues Feature Flag in der Konsole zu erstellen:

1. Melden Sie sich bei der **Flags-Konsole** an, wechseln Sie zum linken Bedienfeld und wählen Sie **Feature Flags** aus.
1. Wählen Sie Ihr Programm aus der Dropdown **Liste** Programm“ aus.
1. Wählen Sie **Neue Feature Flags** aus.
1. Füllen Sie die Formularfelder aus:

   | Feld | Beschreibung |
   | --- | --- |
   | **Name** | Eine Anzeigebeschriftung für das Feature Flag. Wird nicht im Code verwendet. |
   | **Schlüssel** * | Die Kennung, die im Code zum Auswerten des Flags verwendet wird. Kann nach der Erstellung nicht mehr geändert werden. |
   | **Beschreibung** | Optionale Beschreibung für Dokumentationszwecke. |
   | **Metadaten** | Optional. Bis zu 1.024 Zeichen. Verwenden Sie dieses Feld für alle zusätzlichen Metadaten, die mit dem Flag verknüpft werden sollen. |
   | **Tags** | Optionale Tags für Dokumentationszwecke. |
   | **Identität** * | Die Identität, mit der das Flag ausgewertet wird (z. B. ECID). Dies ist die in der Funktionsanfrage übergebene Identität. |
   | **Rollout in Prozent** | Der Prozentsatz Ihrer definierten Zielgruppe, der für diese Funktion bereitgestellt wird. Die Standardeinstellung ist 100 %. Siehe [Festlegen einer Funktion für den schrittweisen Rollout](set-feature-gradual-rollout.md). |

   Mit * markierte Felder sind Pflichtfelder.

>[!IMPORTANT]
>
>Der **Schlüssel** ist die in Ihrem Code verwendete Kennung und kann nach der Erstellung nicht geändert werden. Bei Schlüsseln **dürfen keine Leerzeichen enthalten** und wird zwischen **Groß- und Kleinschreibung**. Der **Name** ist nur eine Anzeigenbeschriftung und wird im Code nicht verwendet; die beiden sind unabhängig (der Name wird nicht in den Schlüssel konvertiert). Wenn Sie im Feld Schlüssel ein Leerzeichen eingeben, wird der Fehler ausgegeben: _„Ungültiger Wert für Funktionsschlüssel“_

1. Fügen Sie optional Zielgruppenkriterien hinzu (siehe Schritt 2).
1. Speichern Sie Ihre Feature Flag-Einstellungen.

## Schritt 2: Audience-Kriterien hinzufügen {#audience}

Zielgruppenkriterien steuern, welche Benutzer die Funktion sehen. Sie können Benutzende mit **Kontextattributen** - Werten ansprechen, die Ihre Website oder App in der Funktionsanfrage sendet (z. B. `locale` oder `platform`). Kombinieren Sie sie mit **AND**, **OR** und **NOT**. Siehe [Verwenden des Kontexts in Zielgruppenregeln](../audience/using-context-in-audience-rules.md).

Um Zielgruppenkriterien hinzuzufügen, wechseln Sie zur Registerkarte **Zielgruppe** , wenn Sie ein Feature Flag erstellen oder bearbeiten.

## Siehe auch {#see-also}

* [Festlegen einer Funktion für das schrittweise Rollout](set-feature-gradual-rollout.md)
* [Erstellen einer Funktionsgruppe](create-a-feature-group.md)

<!-- -->
