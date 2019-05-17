---
description: Liste der häufig gestellten Fragen zu Erlebnis-Targeting und Zielgruppen
keywords: Fehlerbehebung; häufig gestellte Fragen; FAQ; FAQs; Targets; Zielgruppen
seo-description: Liste der häufig gestellten Fragen zu Erlebnis-Targeting und Zielgruppen
seo-title: Häufig gestellte Fragen zu Zielen und Zielgruppen
solution: Target
title: Häufig gestellte Fragen zu Zielen und Zielgruppen
topic: Standard
uuid: 4a8d977a-aa98-4aff-843e-ace32b8eed53
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Häufig gestellte Fragen zu Zielen und Zielgruppen{#targets-and-audiences-faq}

Liste der häufig gestellten Fragen zu Erlebnis-Targeting und Zielgruppen

## Warum sind voreingestellte Zielgruppen in der Target-Bibliothek beim Erstellen von Zielgruppen unter anderen Kategorien aufgeführt? {#section_9EBF5B0F9DF94168A15B92B905CCF7E0}

Vorab eingestellte Zielgruppen in der Target-Bibliothekskategorie sind veraltete Zielgruppen und bestehen auch in anderen Kategorien. Beispiel: Die veraltete Target-Bibliothek &gt; Zielgruppe „Neue Besucher“ verfügt über ein aktuelleres Gegenstück: Besucherprofil &gt; Neuer Besucher.

Best Practice ist, die neuen Zielgruppen einzusetzen, da diese eine bessere Leistung erzielen. Einigen Kunden verwenden möglicherweise ältere, voreingestellte Zielgruppen, die aus diesem Grund nicht aus der Target-Oberfläche gelöscht wurden.

## Wie erkenne ich, wie Traffic zwischen Zielgruppen aufgeteilt wird?   {#section_067EEFB956E7465CBF77EC86834470AB}

Standardmäßig wird Traffic gleichmäßig zwischen Erlebnissen aufgeteilt. Sie können jedoch  Prozentsatzziele für jedes Erlebnis angeben. In diesem Fall wird eine zufällige Nummer generiert und diese Nummer wird verwendet, um das anzuzeigende Erlebnis auszuwählen. Die sich ergebenden Prozentzahlen entsprechen möglicherweise nicht genau den festgelegten Zielen, allerdings bedeutet mehr Traffic, dass die Erlebnisse enger auf die beabsichtigen Ziele aufgeteilt werden sollten.

## Welches Erlebnis wird angezeigt, wenn sich ein Benutzer für eine Aktivität qualifiziert, in der mehrere Erlebnisse mit verschiedenen qualifizierten Zielgruppen enthalten sind?   {#section_94A60B11212D48FD8AB0803C6C7E7253}

Der Benutzer qualifiziert sich für das erste Erlebnis/die erste Zielgruppe, das/die auf der [!UICONTROL Target]-Seite der Aktivität angezeigt wird.

In der folgenden Darstellung qualifiziert sich ein Benutzer aus Kalifornien mit einem Windows-Gerät sowohl für Erlebnis A (Zielgruppe Windows) als auch für Erlebnis C (Zielgruppe Kalifornien). Dem Benutzer wird in diesem Fall Erlebnis A angezeigt, da es in der Liste auf der Target-Seite vor Erlebnis C aufgeführt wird.

![](assets/audiences_order.png)

## Warum unterscheiden sich die Namen der gleichen Zielgruppe in Target, Adobe Audience Manager (AAM) und der Zielgruppenbibliothek in den Core Services voneinander? {#section_F67E61A607B6444C8DAA4F99C3E95AED}

Zielgruppennamen sind [!DNL Target] eindeutig; in [!DNL AAM] und in [!DNL Audience Library]können Sie jedoch denselben Namen für mehrere Zielgruppen haben (wenn sie sich in verschiedenen Ordnern befinden). Wenn [!DNL Target] Sie einen Zielgruppennamen treffen, der einer [!DNL AAM] oder [!DNL Audience Library] einer Zielgruppe entspricht, [!DNL Target] hängt der Name &quot; # &lt; number &gt;&quot; an.

So könnten Ihnen beispielsweise folgende Zielgruppen angezeigt werden: „PC-Nutzer“ (in [!DNL AAM]) und „PC-Nutzer #1“ (in [!DNL Target]).

## Warum kann ich eine Zielgruppe nicht umbenennen? {#section_54E420556F534D20836E261E253D8B97}

Einige Zielgruppen wurden vorab eingerichtet, darunter „Neue Besucher“ und „Wiederkehrende Besucher“. Diese voreingestellten Zielgruppen können von Benutzern nicht umbenannt werden.

## Warum werden meine gesamten Profilparameter auf der Benutzeroberfläche von Target nicht angezeigt?   {#section_3CD947D15C984EE9AD19550220E0E8BD}

[!DNL Target] erlaubt pro Mbox-Aufruf maximal 50 eindeutige Profilattribute. Wenn Sie mehr als 50 Profilattribute an [!DNL Target] übergeben müssen, können Sie hierzu die API-Methode [!UICONTROL Profilupdate] nutzen. Weitere Informationen finden Sie unter [Profilupdate](https://developers.adobetarget.com/api/#authentication-tokens) in der Dokumentation zur Adobe Target-API.

## Warum werden Besuchern Erlebnisse für eine AP-Aktivität angezeigt, die sie nicht sehen sollten? {#section_41CECEAE0881446A8D9F3B016857914B}

Aktivitäten vom Typ „Automatisierte Personalisierung“ werden einmal pro Sitzung ausgewertet. Wenn für ein bestimmtes Erlebnis qualifizierte aktive Sitzungen vorhanden waren und diesen nun neue Angebote hinzugefügt werden, wird Benutzern der neue Inhalt zusammen mit den zuvor angezeigten Angeboten angezeigt. Da sie zuvor für diese Erlebnisse qualifiziert wurden, werden sie ihnen weiterhin für die Dauer der Sitzung angezeigt. Wenn dies bei jedem einzelnen Seitenbesuch ausgewertet werden soll, sollten Sie den Erlebnis-Targeting-Aktivitätstyp (XT) ändern.

## Warum werden Änderungen an Zielgruppen, die per API erstellt wurden, nicht in der Target-UI angezeigt?   {#section_6BEB237CAC004A06A290F9644E5BF0FB}

Im Gegensatz zu Angeboten und Profilskripten werden Änderungen, die per API an mit Target Standard erstellten Zielgruppen vorgenommen werden, derzeit nicht mit der Target-UI synchronisiert.

## Zeichenfolgen, die Zahlen darstellen (Fließkommazahlen werden ebenfalls unterstützt), werden als Zahlen verglichen.{#strings-that-represent-numbers}

Wenn der linke und rechte Teil der Gleichheitsausdrücke als eine Zahl analysiert werden kann, werden die beiden Teile als Zahlen und nicht als Zeichenfolgen verglichen.

Beispiel:

| Wert | Targeting-Kriterien | Ergebnis |
| --- | --- | --- |
| 1.0 | gleich 1 | wahr |
| 1 | equalsIgnoreCase 1.0 | wahr |
| 1.230 | gleich 1 | wahr |
| 1.500 | gleich 1,5 | wahr |
| 1.200 | ist kleiner als 2 | wahr |
| 2 | ist größer als 3.0 | false |
| 045 | gleich 45 | wahr |

Zahlen in wissenschaftlicher Schreibweise werden immer als Zeichenfolgen verglichen.

Beispiel:

„4e-2“ entspricht nur „4e-2“. Es wird *nicht* „0,04“ entsprechen.