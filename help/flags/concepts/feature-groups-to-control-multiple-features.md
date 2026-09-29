---
title: Funktionsgruppen zur Steuerung mehrerer Funktionen
description: Erfahren Sie, wie Sie mit Funktionsgruppen in Flags verwandte Funktionsflags programmübergreifend als eine Einheit bündeln und verwalten können.
badge: label="Beta" type="Informative"
hide: true
exl-id: dfeb7eff-34f1-4cb5-9c3e-a40d1eda3016
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%
---
# Funktionsgruppen zur Steuerung mehrerer Funktionen {#feature-groups}

Eine [Feature Flag](what-is-a-feature-flag.md) steuert ein einzelnes Feature. Wenn Sie mehrere zugehörige Feature Flags zusammen verwalten müssen - und sicherstellen, dass diese dieselbe Zielgruppe erreichen -, verwenden Sie eine **Feature Group**.

## Funktionen einer Funktionsgruppe {#what-it-does}

Eine Funktionsgruppe bündelt mehrere Funktions-Flags und ermöglicht es Ihnen, eine einzige Zielgruppenregel auf alle gleichzeitig anzuwenden. Dies ist nützlich, wenn eine einzelne benutzerseitige Funktion mehrere Anwendungen oder Dienste umfasst.

Nehmen wir zum Beispiel eine Funktion für die Zusammenarbeit, die Änderungen an einer Desktop-Anwendung, einer Mobile App und einem Backend-Service umfasst. Durch die Erstellung einer Funktionsgruppe mit Flags aus allen drei Anwendungen können Sie die Funktion für 1 % der Benutzer öffnen und sicherstellen, dass diese Benutzer ein konsistentes Erlebnis auf allen drei Oberflächen gleichzeitig sehen.

## Programmübergreifende Gruppierung {#cross-application}

Funktionsgruppen unterstützen programmübergreifendes Feature Management. Verwandte Flags über mehrere Anwendungen hinweg können gruppiert werden.


<!-- -->
