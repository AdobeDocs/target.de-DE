---
keywords: Umsatzsteigerung;Umsatz;Schätzung der Umsatzsteigerung;Steigerung berechnen;geschätzter Wert
description: Target kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden.
title: Geschätzte Umsatzsteigerung
topic: Advanced,Standard,Classic
uuid: e3ccb440-ce54-4a5a-be93-69a6162a160f
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Geschätzte Umsatzsteigerung{#estimate-lift-in-revenue}

Target kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden.

>[!NOTE]
>
>Die geschätzte Steigerung ist derzeit nicht für Erlebnis-Targeting-Aktivitäten (XT) verfügbar.

Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert. Sie kann über die Kontovoreinstellungen aktiviert werden. Experience Cloud-Administratoren können diese Funktion aktivieren bzw. deaktivieren. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.

>[!IMPORTANT]
>
>Die geschätzte Steigerung stellt nur eine Schätzung dar. Die Genauigkeit hängt von verschiedenen Faktoren ab, einschließlich prognostizierter Zahlen, wenn sich aktuelle Trends fortsetzen. Bei diesen Werten handelt es sich um Schätzungen, die auf Leistungsdaten aus der Vergangenheit beruhen, weshalb sie nicht als finanzielle Richtlinien angesehen werden sollten. Zukünftige Ergebnisse können abweichend ausfallen.

Für diese Schätzung werden das Ausmaß der Steigerung durch das erfolgreichste Erlebnis und die Gesamtanzahl Ihrer Besucher über den Testzeitraum der Aktivität berücksichtigt. Sie zeigt die Steigerung an, die möglicherweise erzielt werden könnte, wenn alle Besucher das erfolgreichste Erlebnis zu Gesicht bekämen, sofern sich die Trends fortsetzen, die während des Tests herrschten.

Die geschätzte Umsatzsteigerung wird auf Basis von „Umsatz pro Besuch (RPV)“ berechnet, was wiederum von der Metrik für das primäre Ziel abgerufen wird.

Die geschätzte Steigerung wird mit folgender Formel berechnet: (&lt;RPV des erfolgreichsten Erlebnisses&gt; - &lt;RPV des Kontrollerlebnises&gt;)*&lt;Gesamtanzahl Besucher in der Aktivität&gt;

Das Ergebnis wird auf maximal eine Dezimalstelle gerundet, wenn die gekürzte Form vor der Dezimalstelle nur eine Ziffer enthält. Beispiele: 1,6 Mio. $, 60 K $, 900 $, 8,5 K $, 205 K $

Wenn Ihr erfolgreichstes Erlebnis beispielsweise eine Steigerung von 0,59 $ und die Kontrollerfahrung eine Steigerung von 0,15 $ aufweist, wird eine Steigerung von 0,44 $ pro Besucher berechnet. Wenn Sie 75.000 Besucher hatten, beträgt die die Umsatzsteigerung 33.000 $, wenn alle Besucher das erfolgreichste Erlebnis sehen und sich die aktuellen Trends fortsetzen.

Ebenso verhält es sich, wenn Ihr erfolgreichstes Erlebnis eine Steigerung von 0,17 $ gegenüber der Kontrollerfahrung zeigt und Sie während des Testzeitraums 192.000 Besucher hatten. Wenn sich die aktuellen Trends fortsetzen, können Sie mit einer Umsatzsteigerung von 32.640 $ rechnen.

Das Feld für die geschätzte Umsatzsteigerung wird unter folgenden Bedingungen als „---“ angezeigt:

* Wenn es nicht genügend Besucher gab, um eine vernünftige Schätzung abzugeben
* Wenn der geschätzte Wert der Metrik nicht auf der Setup-Seite der Metriken bereitgestellt wurde
* Wenn das leistungsstärkste Erlebnis die Kontrolle ist

Beim Festlegen eines Ziels für die Aktivität zeigt das Feld „Geschätzter Wert“ einen Wert für Ihr Ziel. Mit diesem Wert kann Target die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Der Datentyp ist eine Währung. Dieses Feld wird progressiv angezeigt, nachdem der Benutzer die Maßnahme, die zur Erfüllung des Ziels ergriffen wurde, angibt.

Der Umsatz, der geschätzt wird, wenn 100 % der Besucher das erfolgreichste Erlebnis anzeigen, wird oben in Ihren Target-Berichten angezeigt.
