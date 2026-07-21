---
title: Komplexe Zielgruppenregeln
description: Erfahren Sie, wie Sie mit Regelsätzen für große oder komplexe Zielgruppen in Flags arbeiten, einschließlich der Begrenzung von Massenwerten und wie Sie Regeln über mehrere Bedingungen hinweg aufteilen.
hide: true
exl-id: 37e037b6-45eb-4261-b580-30d94d8e55da
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# Komplexe Zielgruppenregeln {#complex-rules}

## Verwenden verschachtelter Logik für komplexe Regeln {#nested-logic}

Verschachtelte Logik ermöglicht die Kombination mehrerer Zielgruppenbedingungen mit präziser UND/ODER-Steuerung. So aktivieren Sie es:

1. Fügen Sie die gewünschten Zielgruppenbedingungen hinzu.
2. Aktivieren Sie **Verschachtelte Logik** im Abschnitt Zielgruppenregeln .
3. Jeder Bedingung wird eine Nummer zugewiesen. Geben Sie einen logischen Ausdruck ein, der auf diese Zahlen verweist. Beispiel:
   * `1 and (2 or 3)`
   * `(1 and 2) or 3`
   * `(1 and 2) or (3 and 4)`

## Siehe auch {#see-also}

* [Zielgruppe in Feature Flags und Feature Groups](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
