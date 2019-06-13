---
description: Wenn Ihre Aktivität nicht auf Ihrer Site erscheint, helfen Ihnen diese Empfehlungen zur Fehlerbehebung vielleicht bei der Suche nach Ihrer Lösung.
keywords: Fehlerbehebung in Target;Problembehebung in Target;Standardinhalte;Test nicht verfügbar;Aktivität nicht verfügbar;Targeting funktioniert nicht;vorheriges Erlebnis erscheint;kann keine Aktivitäten erstellen;Aktivitäten erstellen;Seitenstruktur geändert;Seitenstruktur modifiziert;Fehlermeldung;Fehler beim Löschen von Profilskript;AJAX funktioniert nicht
seo-description: Wenn Ihre Aktivität nicht auf Ihrer Site erscheint, helfen Ihnen diese Empfehlungen zur Fehlerbehebung vielleicht bei der Suche nach Ihrer Lösung.
seo-title: Fehlerbehebung bei Aktivitäten
solution: Target
title: Fehlerbehebung bei Aktivitäten
topic: Advanced,Standard,Classic
uuid: 5b22c369-0efc-48c0-a0dc-0179b18536fe
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Fehlerbehebung bei Aktivitäten{#troubleshoot-activities}

Wenn Ihre Aktivität nicht auf Ihrer Site erscheint, helfen Ihnen diese Empfehlungen zur Fehlerbehebung vielleicht bei der Suche nach Ihrer Lösung.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen zur Fehlerbehebung finden Sie unter [Fehlerbehebung in Target](../../r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) Links zu weiteren Fehlerbehebungsthemen, FAQs und weitere nützliche Informationen zur Fehlerbehebung bei Aktivitäten und anderen [!DNL Adobe Target]-Funktionen.

Die folgenden Abschnitte enthalten möglicherweise auftretende Probleme sowie Lösungsvorschläge.

## Sie sehen Ihren Standardinhalt.

Vergewissern Sie sich, dass Ihre Aktivität abgeschlossen ist und aktiviert wurde.

## Aktivität ist nicht live.

**Validierung:** Gehen Sie zur Registerkarte Übersicht und prüfen Sie, ob der Test als inaktiv oder als Entwurf gekennzeichnet ist.

**Optionen:**

* Aktivieren Sie den Test.
* Verwenden Sie die Linkvorschau, um einen inaktiven Test anzuzeigen.

## Sie haben keine Berechtigung für die Targeting-Bedingungen der Zielgruppe.

**Validierung:** Prüfen Sie die Targeting-Bedingungen auf der Übersichtsseite.

**Optionen:**

* Qualifizieren Sie sich und versuchen Sie es erneut.
* Verwenden Sie die Linkvorschau, um die Targeting-Bedingungen zu umgehen.

## Die Seite hat keine Berechtigung für die Seiten-Targeting-Bedingungen.

**Validierung:** Ermitteln Sie auf der Übersichtsseite, ob die Seite nicht unter die Targeting-Bedingungen fällt.

**Optionen:**

* Gehen Sie zum Visual Experience Composer und klicken Sie auf URL\&gt; Erweitert\&gt;Aktuelle Seite.

## Anstelle eines neuen Erlebnisses wird ein früheres Erlebnis eingeblendet.

**Validierung:** Nutzen Sie eine der unten stehenden Optionen und versuchen Sie dann erneut, das Erlebnis anzuzeigen.

**Optionen:**

* Löschen Sie Cache und Cookies und versuchen Sie es erneut.

* Versuchen Sie es mit einem anderen Browser.
* Verwenden Sie den Privat-/Inkognito-Modus.

## Sie wurden kürzlich zu Target hinzugefügt, können jedoch keine Aktivitäten erstellen.

**Validierung:** Klicken Sie auf Aktivität erstellen. Wenn die Option nicht verfügbar ist, sind Sie wahrscheinlich nicht dazu berechtigt, eine Aktivität zu erstellen.

**Optionen:**

Nachdem Sie in Target als Benutzer hinzugefügt wurden, müssen Sie die Rolle „Genehmiger“ haben, damit Sie Aktivitäten erstellen können.

* Bitten Sie den Administrator Ihres Konto darum, Ihnen die Genehmigerrolle zu geben.
* Sollten Sie der Administrator sein, können Sie sich in Target Standard unter Einrichten &gt; Benutzer selbst die Rolle „Genehmiger“ geben.

   Weitere Informationen finden Sie unter [Zuweisen der Rolle „Genehmiger“](../../administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## Die Struktur der Seite hat sich seit der Einrichtung der Aktivität geändert.

**Validierung:** Rufen Sie im Visual Experience Composer die vorhandene Aktivität auf. Suchen Sie nach einem Hinweis, der davor warnt, dass die Selektoren (oder die Struktur) verändert wurde(n).

**Optionen:**

* Erstellen Sie die Aktivität erneut.

Weitere Informationen darüber, wie Seitenmodifizierungen sich auf die Anzeige von Target auswirken, finden Sie unter [Szenarien für die Seitenmodifizierung](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Struktur der Seite wird während des Seitenladevorgangs (während der Laufzeit) verändert.

**Validierung:** Fragen Sie den Entwickler.

**Hinweis:** Damit Target erkennen kann, wo Änderungen der Aktivität vorgenommen werden sollten, sollten Sie das dynamische Einfügen von Elementen bei derselben Klasse bzw. die dynamische Modifizierung der Klasse von Geschwisterelementen vermeiden.

**Optionen:**

* Aktualisieren Sie den Seiten-Code, um jedes zu testende Element eindeutig zu identifizieren (mithilfe einer id).
* Unterbrechen Sie die dynamische Modifizierung der Klasse oder Geschwister wie oben beschrieben.

Weitere Informationen darüber, wie Seitenmodifizierungen sich auf die Anzeige von Target auswirken, finden Sie unter [Szenarien für die Seitenmodifizierung](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## mbox.js verschiebt sämtlichen folgenden Code aus dem Kopf in den Textkörper.

**Validierung:** Betrachten Sie die Quelle, um zu ermitteln, ob der mbox.js-Datei vor dem schließenden </body> Tag Deklarationen folgen.

**Optionen:**

* Positionieren Sie mbox.js als letztes Element im `<head>`-Abschnitt Ihrer Seite.
* Verwenden Sie eindeutige div-IDs für die auf höchster Ebene innerhalb des Textteils gelegenen Elemente.

## Andere Aktivitäten werden auf derselben Seite ausgeführt.

**Validierung:** Verwenden Sie die Registerkarte Kollisionen, um zu sehen, ob andere Aktivitäten ausgeführt werden.

**Hinweis:** Die Registerkarte Kollisionen funktioniert nicht mit dem Vorlagentestmodul.

**Optionen:**

* Erhöhen Sie die Priorität dieser Aktivität.
* Senken Sie die Priorität dieser Aktivität.
* Deaktivieren Sie andere Aktivitäten.

## Wenn Sie ein Profilskript löschen, wird eine Fehlermeldung angezeigt.

**Validierung:** Beim Löschen eines Profilskripts aus Target Standard/Premium wird die Fehlermeldung „Profilskript konnte nicht gelöscht werden“ angezeigt.

**Optionen:**

Führen Sie einen der folgenden Schritte aus:

* Erneut löschen. Die Erfolgsmeldung wird angezeigt.
* Warten Sie ungefähr 10 Minuten, bis der Target Standard-/Premium-Importer ausgeführt werden kann. Der Importer aktualisiert die Profilskriptliste.

## Einige AJAX-Mbox-Aufrufe funktionieren nicht.

**Hinweis:** Mehrere AJAX-Mbox-Aufrufe mit demselben Mbox-Namen, jedoch verschiedenen Parametern auf derselben Seite funktionieren nicht. Nur der erste Aufruf erfolgt.

## Sie haben eine Aktivität über die Target API aktiviert, aber die Aktivität zeigt in der Target-Benutzeroberfläche den Status „Inaktiv“.

Hinweis: Wenn Sie bestimmte Aktionen ausführen, wie zum Beispiel eine Aktivität außerhalb der Benutzeroberfläche über die Target-API zu aktivieren, kann es bis zu 10 Minuten dauern, bis die Aktualisierung bis zur Benutzeroberfläche propagiert wird.