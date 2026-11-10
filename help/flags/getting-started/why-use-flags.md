---
title: Warum Flags verwenden?
description: Erfahren Sie mehr über die wichtigsten Anwendungsfälle für Flags in Adobe Target, von selektiven Funktionstests bis hin zu koordinierten Versionen mehrerer Anwendungen.
badge: label="Beta" type="Informative"
hide: true
exl-id: c39c6b34-2024-4c38-b2f2-a9b58f5eff63
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: c1fafcfcd7d5d22781abdd10e6eb3c2b84136c2d
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%
---
# Warum Flags verwenden? {#why-use}

Flags sind das richtige Tool, wenn Sie steuern müssen, wer eine Funktion zu welchem Zeitpunkt sieht - ob Sie in der Entwicklung testen, mit einer Untergruppe von Benutzern validieren oder eine große Version über mehrere Teams hinweg koordinieren.

## Häufige Anwendungsfälle {#use-cases}

**Selektive Tests während der Entwicklung**
Testen Sie eine Funktion mit Ihrer eigenen Sitzung, während andere Entwickler ihre Arbeit unbeeinflusst fortsetzen. Es ist keine komplexe Code-Verzweigung erforderlich.

**Gestaffelter Rollout mit Benutzer-Feedback**
Geben Sie eine Funktion zuerst für eine kleine Gruppe von Benutzern frei. Sammeln Sie Feedback, adressieren Sie Probleme und erweitern Sie die Zielgruppe schrittweise vor einer vollständigen Veröffentlichung.

**Schrittweiser Rollout zur Produktion**
Öffnen Sie eine neue Funktion schrittweise - 1 %, 10 %, 50 % und dann 100 % der Benutzer. Überwachen Sie die Leistung und die Benutzerantwort bei jedem Schritt. Wenn etwas schief geht, schalten Sie es sofort aus.

**Backend-Lastverwaltung**
Inkrementelles Durchführen eines Rollouts, um plötzliche Traffic-Spitzen bei Backend-Services zu vermeiden, anstatt alle Benutzer einer neuen Funktion gleichzeitig auszusetzen.

**Koordinierte Versionen mit mehreren Anwendungen**
Gleichzeitiges Aktivieren einer Funktion über mehrere Anwendungen hinweg für eine bestimmte Benutzergruppe. Flags sorgen für Konsistenz über die gesamte Release-Oberfläche.

**Zurückgestellte Versionen**
Stellen Sie Code vorab für die Produktion bereit und aktivieren Sie dann die Funktion zu einem bestimmten Zeitpunkt - z. B. zu Beginn eines Produkteinführungsereignisses - ohne Code-Änderung in letzter Minute.

**Kill-Schalter**
Wenn nach der Veröffentlichung ein Problem erkannt wird, deaktivieren Sie die Funktion ohne Hotfix oder erneute Bereitstellung. Die Änderungen werden bei der nächsten Aktualisierung des Flags wirksam (standardmäßig alle 5 Minuten).

<!-- -->
