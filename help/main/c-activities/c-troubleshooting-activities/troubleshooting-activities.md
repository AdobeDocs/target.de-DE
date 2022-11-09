---
keywords: Fehlerbehebung in Target;Problembehebung in Target;Standardinhalte;Test nicht verfügbar;Aktivität nicht verfügbar;Targeting funktioniert nicht;vorheriges Erlebnis erscheint;kann keine Aktivitäten erstellen;Aktivitäten erstellen;Seitenstruktur geändert;Seitenstruktur modifiziert;Fehlermeldung;Fehler beim Löschen von Profilskript;AJAX funktioniert nicht
description: Sollte Ihre Adobe  [!DNL Target] -Aktivität nicht auf Ihrer Site erscheinen, finden Sie hier Vorschläge zur Fehlerbehebung.
title: Wie kann ich Probleme in Verbindung mit Aktivitäten beheben?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
source-git-commit: 8890d29a71506095a166321e324a000b5ad862a6
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 50%

---

# Fehlerbehebung bei Aktivitäten

Wenn Ihre [!DNL Adobe Target]-Aktivität nicht auf Ihrer Site erscheint, helfen Ihnen die folgenden Empfehlungen vermutlich bei der Lösung.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen zur Fehlerbehebung finden Sie unter [Fehlerbehebung in Target](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) Links zu weiteren Fehlerbehebungsthemen, FAQs und weitere nützliche Informationen zur Fehlerbehebung bei Aktivitäten und anderen [!DNL Adobe Target]-Funktionen.

Die folgenden Abschnitte enthalten Probleme, auf die Sie möglicherweise mit vorgeschlagenen Lösungen stoßen.

## Es gelingt mir nicht, eine in der Benutzeroberfläche von [!DNL Target] erstellte Aktivität über die API zu aktualisieren.

Aktivitäten, die mithilfe der [!DNL Target] Die Benutzeroberfläche sollte über die [!DNL Target] Benutzeroberfläche. Dagegen sollten über die API erstellte Aktivitäten über die API aktualisiert werden. Wenn Sie ursprünglich eine Aktivität mit der API erstellt haben, bearbeiten Sie die Aktivität später über die [!DNL Target] -Benutzeroberfläche verwenden, werden nicht alle Änderungen aktualisiert. Alle Änderungen werden im Backend gespeichert und können durch einen weiteren API-Aufruf aktualisiert werden.

Machen Sie es sich zur Gewohnheit, eine Aktivität immer mit derselben Methode (UI oder API) zu aktualisieren, mit der sie ursprünglich erstellt wurde.

## Sie sehen Ihren Standardinhalt.

Vergewissern Sie sich, dass Ihre Aktivität abgeschlossen ist und aktiviert wurde.

## Aktivität ist nicht live.

**Validieren:** Navigieren Sie zu [!UICONTROL Übersicht] und überprüfen, ob der Test als inaktiv oder als Entwurf gekennzeichnet ist.

**Optionen:**

* Aktivieren Sie den Test.
* Verwenden Sie die Linkvorschau, um einen inaktiven Test anzuzeigen.

## Sie sind nicht für die Zielgruppen-Targeting-Bedingungen qualifiziert.

**Validierung:** Prüfen Sie die Targeting-Bedingungen auf der Übersichtsseite.

**Optionen:**

* Qualifizieren Sie sich und versuchen Sie es erneut.
* Verwenden Sie die Linkvorschau, um die Targeting-Bedingungen zu umgehen.

## Die Seite ist nicht für die Seiten-Targeting-Bedingungen qualifiziert.

**Validieren:** Im [!UICONTROL Übersicht] bestimmen, ob die Seite außerhalb der Targeting-Bedingungen liegt.

**Optionen:**

* Navigieren Sie zu [!UICONTROL Visual Experience Composer]klicken Sie auf URL > Erweitert > Aktuelle Seite.

## Anstelle eines neuen Erlebnisses wird ein früheres Erlebnis eingeblendet.

**Validierung:** Nutzen Sie eine der unten stehenden Optionen und versuchen Sie dann erneut, das Erlebnis anzuzeigen.

**Optionen:**

* Löschen Sie Cache und Cookies und versuchen Sie es erneut.
* Versuchen Sie es mit einem anderen Browser.
* Verwenden Sie den Privat-/Inkognito-Modus.

## Sie wurden kürzlich zu [!DNL Target] hinzugefügt, können jedoch keine Aktivitäten erstellen.

**Validierung:**[!UICONTROL  Klicken Sie auf Aktivität erstellen]. Wenn die Option nicht verfügbar ist, sind Sie wahrscheinlich nicht dazu berechtigt, eine Aktivität zu erstellen.

**Optionen:**

Nachdem Sie als Benutzer in [!DNL Target], müssen Sie über die [!UICONTROL Genehmiger] Rolle, um Aktivitäten zu erstellen.

* Bitten Sie den Administrator Ihres Kontos, Sie zu einem Genehmiger zu machen.
* Wenn Sie der Administrator sind, geben Sie sich die [!UICONTROL Genehmiger] Rolle von **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]** in [!DNL Target].

   Weitere Informationen finden Sie unter [Zuweisen der Rolle „Genehmiger“](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## Die Struktur der Seite hat sich seit der Einrichtung der Aktivität geändert.

**Validierung:**[!UICONTROL  Rufen Sie im Visual Experience Composer die vorhandene Aktivität auf. ] Suchen Sie nach einem Hinweis, der davor warnt, dass die Selektoren (oder die Struktur) verändert wurde(n).

**Optionen:**

* Erstellen Sie die Aktivität erneut.

Weitere Informationen dazu, wie sich Seitenänderungen auf [!DNL Target]Die Fähigkeit zur Anzeige, siehe [Szenarien für die Seitenmodifizierung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Struktur der Seite wird während des Seitenladevorgangs (während der Laufzeit) verändert.

**Validierung:** Fragen Sie den Entwickler.

**Hinweis:** Zur [!DNL Target] Um zu erkennen, wo Aktivitätsänderungen angewendet werden sollen, vermeiden Sie das dynamische Einfügen eines Elements mit derselben Klasse oder das dynamische Ändern der Klasse von Geschwisterelementen.

**Optionen:**

* Aktualisieren Sie den Seiten-Code, um jedes getestete Element eindeutig zu identifizieren (mithilfe einer ID).
* Unterbrechen Sie die dynamische Modifizierung der Klasse oder Geschwister wie oben beschrieben.

Weitere Informationen dazu, wie sich Seitenänderungen auf [!DNL Target]Die Fähigkeit zur Anzeige, siehe [Szenarien für die Seitenmodifizierung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Andere Aktivitäten werden auf derselben Seite ausgeführt.

**Validieren:** Verwenden Sie die [!UICONTROL Kollisionen] , um zu sehen, ob andere Aktivitäten ausgeführt werden.

**Hinweis:**[!UICONTROL  Die Registerkarte Kollisionen funktioniert nicht mit dem Vorlagentestmodul.]

**Optionen:**

* Erhöhen Sie die Priorität dieser Aktivität.
* Senken Sie die Priorität dieser Aktivität.
* Deaktivieren Sie andere Aktivitäten.

## Wenn Sie ein Profilskript löschen, wird eine Fehlermeldung angezeigt.

**Validierung:**[!DNL Target] Beim Löschen eines Profilskripts aus wird die Fehlermeldung „Profilskript konnte nicht gelöscht werden“ angezeigt.

**Optionen:**

Führen Sie einen der folgenden Schritte aus:

* Löschen Sie das Profilskript erneut. Die Erfolgsmeldung wird angezeigt.
* Warten Sie etwa 10 Minuten auf die [!DNL Target] Importer zur Ausführung. Der Importer aktualisiert die Profilskriptliste.

## Einige ajax-Aufrufe von [!DNL Target] funktionieren nicht.

**Hinweis:** Mehrere Ajax [!DNL Target] -Aufrufe mit demselben Namen, aber unterschiedlichen Parametern funktionieren nicht auf derselben Seite. Nur der erste Aufruf erfolgt.

## Sie haben über die API von [!DNL Target] eine Aktivität aktiviert, aber die Aktivität hat in der Benutzeroberfläche von [!DNL Target] den Status [!UICONTROL Inaktiv].

Wenn Sie bestimmte Aktionen ausführen, z. B. eine Aktivität außerhalb der Benutzeroberfläche mit der [!DNL Target] API verwenden, kann es bis zu zehn Minuten dauern, bis die Aktualisierung auf die Benutzeroberfläche übertragen wird.

## Nach der Aktivitätskonvertierung befindet sich der Besucher in keinem Erlebnis.

Wenn die Konversionsmetrik der Aktivität, um sich für ein Erlebnis zu qualifizieren, im selben Versand gesendet wird [!DNL Target] als Aktivitätsqualifikation anzufordern, befindet sich der Besucher möglicherweise nicht mehr in einem Erlebnis, nachdem die Anfrage gesendet wurde. In dieser Situation sieht der Besucher Standardinhalte. [!DNL Adobe] empfiehlt, keine Aktivitätskonvertierung und -qualifikation in derselben Anforderung zu senden.

Wenn Sie beide Einstellungen in derselben Anforderung senden möchten, können Sie [!UICONTROL Erweiterte Einstellungen] , um anzugeben, dass der Besucher nach der Konvertierung im selben Erlebnis verbleibt.
