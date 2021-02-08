---
keywords: Fehlerbehebung in Target;Problembehebung in Target;Standardinhalte;Test nicht verfügbar;Aktivität nicht verfügbar;Targeting funktioniert nicht;vorheriges Erlebnis erscheint;kann keine Aktivitäten erstellen;Aktivitäten erstellen;Seitenstruktur geändert;Seitenstruktur modifiziert;Fehlermeldung;Fehler beim Löschen von Profilskript;AJAX funktioniert nicht
description: Suchen Sie nach Empfehlungen zur Fehlerbehebung, falls Ihre Adobe Target-Aktivität nicht auf Ihrer Site erscheint.
title: Wie kann ich Aktivitäten beheben?
feature: Activities
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 76%

---


# Fehlerbehebung bei Aktivitäten

Wenn Ihre [!DNL Adobe Target]-Aktivität nicht auf Ihrer Site angezeigt wird, sollten diese Vorschläge zur Fehlerbehebung Sie bei der Suche nach Ihrer Lösung unterstützen.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen zur Fehlerbehebung finden Sie unter [Fehlerbehebung in Target](/help/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) Links zu weiteren Fehlerbehebungsthemen, FAQs und weitere nützliche Informationen zur Fehlerbehebung bei Aktivitäten und anderen [!DNL Adobe Target]-Funktionen.

Die folgenden Abschnitte enthalten möglicherweise auftretende Probleme sowie Lösungsvorschläge.

## Ich habe eine Aktivität mit der Benutzeroberfläche der Zielgruppe erstellt und kann sie nicht über die API aktualisieren.

Aktivitäten, die mit der Benutzeroberfläche der Zielgruppe erstellt wurden, sollten über die Benutzeroberfläche der Zielgruppe aktualisiert werden. Über API erstellte Aktivitäten sollten über API aktualisiert werden. Wenn Sie beispielsweise eine Aktivität ursprünglich mit der API erstellen, die Aktivität dann später jedoch über die Benutzeroberfläche der Zielgruppe bearbeiten, werden nicht alle Änderungen aktualisiert. Alle Änderungen werden im Backend gespeichert und können durch einen weiteren API-Aufruf aktualisiert werden.

Am besten sollten Sie die Aktivität mit derselben Methode (UI oder API) aktualisieren, mit der die Aktivität ursprünglich erstellt wurde.

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

* Gehen Sie zum Visual Experience Composer und klicken Sie auf URL\> Erweitert\>Aktuelle Seite.

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
* Wenn Sie der Administrator sind, geben Sie sich die Rolle &quot;Genehmigende Person&quot;von **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]** in der Zielgruppe ein.

   Weitere Informationen finden Sie unter [Zuweisen der Rolle „Genehmiger“](/help/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## Die Struktur der Seite hat sich seit der Einrichtung der Aktivität geändert.

**Validierung:** Rufen Sie im Visual Experience Composer die vorhandene Aktivität auf. Suchen Sie nach einem Hinweis, der davor warnt, dass die Selektoren (oder die Struktur) verändert wurde(n).

**Optionen:**

* Erstellen Sie die Aktivität erneut.

Weitere Informationen darüber, wie Seitenmodifizierungen sich auf die Anzeige von Target auswirken, finden Sie unter  [Szenarien für die Seitenmodifizierung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Struktur der Seite wird während des Seitenladevorgangs (während der Laufzeit) verändert.

**Validierung:** Fragen Sie den Entwickler.

**Hinweis:** Damit Target erkennen kann, wo Änderungen der Aktivität vorgenommen werden sollten, sollten Sie das dynamische Einfügen von Elementen bei derselben Klasse bzw. die dynamische Modifizierung der Klasse von Geschwisterelementen vermeiden.

**Optionen:**

* Aktualisieren Sie den Seiten-Code, um jedes zu testende Element eindeutig zu identifizieren (mithilfe einer id).
* Unterbrechen Sie die dynamische Modifizierung der Klasse oder Geschwister wie oben beschrieben.

Weitere Informationen darüber, wie Seitenmodifizierungen sich auf die Anzeige von Target auswirken, finden Sie unter  [Szenarien für die Seitenmodifizierung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## mbox.js verschiebt sämtlichen folgenden Code aus dem Kopf in den Textkörper.

**Validierung:** Betrachten Sie die Quelle, um zu ermitteln, ob der mbox.js-Datei vor dem schließenden `</body>` Tag Deklarationen folgen.

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

## Einige AJAX [!DNL Target]-Aufrufe funktionieren nicht.

**Hinweis:** Mehrere AJAX- [!DNL Target] Aufrufe mit demselben Namen, aber unterschiedlichen Parametern funktionieren nicht auf derselben Seite. Nur der erste Aufruf erfolgt.

## Sie haben eine Aktivität mit der Zielgruppen-API aktiviert, aber die Aktivität zeigt in der Benutzeroberfläche der Zielgruppe den Status [!UICONTROL Inaktiv] an.

Hinweis: Wenn Sie bestimmte Aktionen ausführen, wie zum Beispiel eine Aktivität außerhalb der Benutzeroberfläche über die Target-API zu aktivieren, kann es bis zu 10 Minuten dauern, bis die Aktualisierung bis zur Benutzeroberfläche propagiert wird.