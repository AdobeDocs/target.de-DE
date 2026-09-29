---
title: Festlegen einer Funktionsgruppe für das schrittweise Rollout
description: Erfahren Sie, wie Sie in Flags einen prozentualen schrittweisen Rollout für eine Funktionsgruppe konfigurieren.
badge: label="Beta" type="Informative"
hide: true
exl-id: fcf187f1-2f33-4e3a-b740-985d5bc0bcdc
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%
---
# Festlegen einer Funktionsgruppe für das schrittweise Rollout {#gradual-rollout-feature-group}

Der prozentuale Rollout für eine Funktionsgruppe wird auf der Registerkarte &quot;**&quot;**. Sie können diesen Wert jederzeit während des Rollouts nach oben oder unten anpassen.

## Funktionsweise {#how-it-works}

Wenn Sie einen prozentualen Rollout festlegen, z. B. 60 %, wird dieser Prozentsatz Ihrer definierten Zielgruppe der Funktionsgruppe angezeigt. Der Prozentsatz des Rollouts **erforderlich** und beträgt standardmäßig **100%** (die Funktionsgruppe wird für die gesamte passende Zielgruppe bereitgestellt). Sie können sie in Schritten von **1 %**. Der verbleibende Prozentsatz wird in die **Kontrollgruppe** aufgenommen, die das Standardverhalten erhält.

Wenn Sie mehrere Varianten (für A/B-Tests) konfiguriert haben, wird der Belichtungsprozentsatz gleichmäßig auf die Varianten verteilt. Beispielsweise ergibt eine Exposition von 60 % bei drei Varianten 20 % pro Variante, während es in der Kontrollgruppe 40 % sind.

Sie können den Prozentsatz jederzeit erhöhen oder verringern, um den Rollout zu erweitern, zu reduzieren oder auszusetzen.

## Siehe auch {#see-also}

* [Erstellen einer Funktionsgruppe](create-a-feature-group.md)
* [A/B-Tests mit Feature Flags](a-b-testing.md)
* [Schrittweiser Rollout](../../concepts/gradual-rollout.md)

<!-- -->
