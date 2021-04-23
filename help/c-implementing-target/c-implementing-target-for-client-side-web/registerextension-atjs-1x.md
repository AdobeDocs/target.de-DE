---
keywords: Registerextension; Registererweiterung; Register erweitern; at.js; Funktionen; funktion; Clientcode; Serverdomain; Globalmboxname; Globalmbox autocreate; Zeitüberschreitung
description: Verwenden Sie die Funktion registerExtension() für die JavaScript-Adobe  [!DNL Target] at.js, um eine bestimmte Erweiterung zu registrieren. (at.js 1.x)
title: Wie verwende ich die Funktion registerExtension()?
feature: 'at.js '
role: Developer
exl-id: 7f0898b4-ddd5-425c-99dc-94f9b30f8ba7
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 90%

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

## Methoden für Logger-Module   {#section_10AF62B49AEF48F981E950D26E176138}

| Schlüssel | Typ | Beschreibung |
|--- |--- |--- |
| log | Funktion | Protokolliert die Variablenliste der Argumente in der Browser-Konsole, falls vorhanden. Wird nur aktiviert, wenn `mboxDebug=true` an die URL übermittelt wird. |
| error | Funktion | Protokolliert die Variablenliste der Argumente in der Browser-Konsole. Wird nur aktiviert, wenn schwerwiegende Fehler auftreten, beispielsweise Zeitüberschreitungen des Netzwerks, nicht gefundene HTML-Knoten usw. |
