---
description: 'Informationen zur registerExtension()-Funktion für at.js. '
keywords: Registerextension; Registererweiterung; Registrierung registrieren; at. js; Funktionen; function; Clientcode; Serverdomain; Globalmboxname; Globalmboxautocreate; timeout
seo-description: Informationen zur registerExtension()-Funktion für die Adobe Target-JavaScript-Bibliothek at.js.
seo-title: Informationen zur registerExtension()-Funktion für die Adobe Target-JavaScript-Bibliothek at.js.
solution: Target
subtopic: Erste Schritte
title: registerExtension()
topic: Standard
translation-type: tm+mt
source-git-commit: ef2c4ac78fef5889d5a6e9e053dfd36b77919dd4

---


# registerExtension() - at.js 1.x

Stellt eine Standardart zur Registrierung bestimmter Erweiterungen dar.

>[!NOTE]
>
>Diese Funktion steht nur für at.js, Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird.

Der Optionsparameter ist obligatorisch und hat die folgende Struktur:

| Schlüssel | Typ | Erforderlich | Beschreibung |
|--- |--- |--- |--- |
| name | Zeichenfolge | Ja | Name der Erweiterung |
| Module | Array[Zeichenfolge] | Ja | Ein Zeichenfolgen-Array, das die angefragten Modulnamen beschreibt |
| registrieren | Funktion | Ja | Eine Funktion zur Initialisierung und Erstellung der Erweiterung. Diese Funktion erhält, basierend auf dem Modul-Array, Argumente. |

Hinweise:

* Wird einer dieser Parameter nicht bereitgestellt, wird eine Ausnahme generiert.
* Ist das Modul-Array leer, wird eine Ausnahme generiert.

Weitere Informationen und Beispiele zur Verwendung von `registerExtension` finden Sie auf der Seite [Adobe Experience Cloud at.js-Erweiterungen](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions) auf GitHub.

## Methoden für Einstellungsmodule {#section_8501CDD4B0624FA2B10532C98C5F4328}

| Schlüssel | Typ | Beschreibung |
|--- |--- |--- |
| clientCode | Zeichenfolge | Clientcode |
| serverDomain | Zeichenfolge | Edgeserverdomäne |
| globalMboxName | Zeichenfolge | Name der globalen Mbox in Target |
| globalMboxAutoCreate | Boolesch | Zeigt an, ob die automatische Erstellung aktiviert oder deaktiviert ist. |
| Zeitüberschreitung | Nummer | Zeitüberschreitung der Abfrage |

## Methoden für Logger-Module {#section_10AF62B49AEF48F981E950D26E176138}

| Schlüssel | Typ | Beschreibung |
|--- |--- |--- |
| log | Funktion | Protokolliert die Variablenliste der Argumente in der Browser-Konsole, falls vorhanden. Wird nur aktiviert, wenn `mboxDebug=true` an die URL übermittelt wird. |
| error | Funktion | Protokolliert die Variablenliste der Argumente in der Browser-Konsole. Wird nur aktiviert, wenn schwerwiegende Fehler auftreten, beispielsweise Zeitüberschreitungen des Netzwerks, nicht gefundene HTML-Knoten usw. |
