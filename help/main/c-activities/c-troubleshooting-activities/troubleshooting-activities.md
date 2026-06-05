---
keywords: Fehlerbehebung in Target;Problembehebung in Target;Standardinhalte;Test nicht verfügbar;Aktivität nicht verfügbar;Targeting funktioniert nicht;vorheriges Erlebnis erscheint;kann keine Aktivitäten erstellen;Aktivitäten erstellen;Seitenstruktur geändert;Seitenstruktur modifiziert;Fehlermeldung;Fehler beim Löschen von Profilskript;AJAX funktioniert nicht
description: Sollte Ihre Adobe  [!DNL Target] -Aktivität nicht auf Ihrer Site erscheinen, finden Sie hier Vorschläge zur Fehlerbehebung.
title: Wie kann ich Probleme in Verbindung mit Aktivitäten beheben?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
TQID: https://experienceleague.adobe.com/L-011t7q6c3aICs0ZrM01m9pZByH86FKGiLG1A7Rl2s
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 866
ht-degree: 43%

---

# Fehlerbehebung bei Aktivitäten

Wenn Ihre [!DNL Adobe Target]-Aktivität nicht auf Ihrer Site erscheint, helfen Ihnen die folgenden Empfehlungen vermutlich bei der Lösung.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen zur Fehlerbehebung finden Sie unter [Fehlerbehebung in Target](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) Links zu weiteren Fehlerbehebungsthemen, FAQs und weitere nützliche Informationen zur Fehlerbehebung bei Aktivitäten und anderen [!DNL Adobe Target]-Funktionen.

Die folgenden Abschnitte enthalten Probleme, auf die Sie bei vorgeschlagenen Lösungen stoßen können.

## Es gelingt mir nicht, eine in der Benutzeroberfläche von [!DNL Target] erstellte Aktivität über die API zu aktualisieren.

Aktivitäten, die mit der [!DNL Target]-Benutzeroberfläche erstellt wurden, sollten über die [!DNL Target]-Benutzeroberfläche aktualisiert werden. Dagegen sollten über die API erstellte Aktivitäten über die API aktualisiert werden. Wenn Sie beispielsweise eine ursprünglich über die API erstellte Aktivität später über die [!DNL Target]-Benutzeroberfläche bearbeiten, werden nicht alle Änderungen aktualisiert. Alle Änderungen werden im Backend gespeichert und können durch einen weiteren API-Aufruf aktualisiert werden.

Machen Sie es sich zur Gewohnheit, eine Aktivität immer mit derselben Methode (UI oder API) zu aktualisieren, mit der sie ursprünglich erstellt wurde.

## Sie sehen Ihren Standardinhalt.

Vergewissern Sie sich, dass Ihre Aktivität abgeschlossen ist und aktiviert wurde.

## Aktivität ist nicht live.

**Validieren:** Wechseln Sie zur Registerkarte [!UICONTROL Übersicht] und überprüfen Sie, ob der Test als inaktiv oder als Entwurf markiert ist.

**Optionen:**

* Aktivieren Sie den Test.
* Verwenden Sie die Linkvorschau, um einen inaktiven Test anzuzeigen.

## Sie qualifizieren sich nicht für die Bedingungen für die Zielgruppen-Zielgruppenbestimmung.

**Validierung:** Prüfen Sie die Targeting-Bedingungen auf der Übersichtsseite.

**Optionen:**

* Qualifizieren Sie sich und versuchen Sie es erneut.
* Verwenden Sie die Linkvorschau, um die Targeting-Bedingungen zu umgehen.

## Die Seite ist nicht für die Bedingungen zum Seiten-Targeting qualifiziert.

**Validieren:** Stellen Sie auf der Seite [!UICONTROL Übersicht] fest, ob die Seite außerhalb der Zielgruppenbestimmungsbedingungen liegt.

**Optionen:**

* Navigieren Sie zu [!UICONTROL Visual Experience Composer] und klicken Sie auf URL > Erweitert > Aktuelle Seite.

## Anstelle eines neuen Erlebnisses wird ein früheres Erlebnis eingeblendet.

**Validierung:** Nutzen Sie eine der unten stehenden Optionen und versuchen Sie dann erneut, das Erlebnis anzuzeigen.

**Optionen:**

* Löschen Sie Cache und Cookies und versuchen Sie es erneut.
* Versuchen Sie es mit einem anderen Browser.
* Verwenden Sie den Privat-/Inkognito-Modus.

## Sie wurden kürzlich zu [!DNL Target] hinzugefügt, können jedoch keine Aktivitäten erstellen.

**Validieren:** Klicken Sie auf [!UICONTROL Aktivität erstellen]. Wenn die Option nicht verfügbar ist, sind Sie wahrscheinlich nicht dazu berechtigt, eine Aktivität zu erstellen.

**Optionen:**

Nachdem Sie in [!DNL Target] als Benutzer hinzugefügt wurden, müssen Sie über die Rolle [!UICONTROL Genehmiger] verfügen, um Aktivitäten zu erstellen.

* Bitten Sie den Administrator Ihres Kontos, Sie zu einer genehmigenden Person zu machen.
* Falls Sie selbst der Administrator sind, erteilen Sie sich in [!DNL Target] unter **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]** die Rolle [!UICONTROL Genehmiger].

  Weitere Informationen finden Sie unter [Zuweisen der Rolle „Genehmiger“](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## Die Struktur der Seite hat sich seit der Einrichtung der Aktivität geändert.

**Validieren** Wechseln Sie zum [!UICONTROL Visual Experience Composer] für die vorhandene Aktivität. Suchen Sie nach einem Hinweis, der davor warnt, dass die Selektoren (oder die Struktur) verändert wurde(n).

**Optionen:**

* Erstellen Sie die Aktivität erneut.

Weitere Informationen darüber, wie Seitenänderungen die Anzeige von [!DNL Target] beeinträchtigen, finden Sie unter [Szenarien für Seitenänderungen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Struktur der Seite wird während des Seitenladevorgangs (während der Laufzeit) verändert.

**Validierung:** Fragen Sie den Entwickler.

**Hinweis** Damit [!DNL Target] erkennen können, wo Aktivitätsänderungen angewendet werden sollen, sollten Sie kein Element mit derselben Klasse dynamisch einfügen oder die Klasse von gleichrangigen Elementen dynamisch ändern.

**Optionen:**

* Aktualisieren Sie den Seiten-Code, um jedes getestete Element eindeutig zu identifizieren (mithilfe einer ID).
* Stoppen Sie die dynamische Modifizierung der Klasse oder Geschwister wie oben beschrieben.

Weitere Informationen darüber, wie Seitenänderungen die Anzeige von [!DNL Target] beeinträchtigen, finden Sie unter [Szenarien für Seitenänderungen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Andere Aktivitäten werden auf derselben Seite ausgeführt.

**Validieren:** Verwenden Sie die Registerkarte [!UICONTROL Kollisionen] um zu sehen, ob andere Aktivitäten ausgeführt werden.

**Hinweis:** Die Registerkarte [!UICONTROL Kollisionen] funktioniert nicht mit dem Vorlagentestmodul.

**Optionen:**

* Erhöhen Sie die Priorität dieser Aktivität.
* Senken Sie die Priorität dieser Aktivität.
* Deaktivieren Sie andere Aktivitäten.

## Wenn Sie ein Profilskript löschen, wird eine Fehlermeldung angezeigt.

**Validieren** Beim Löschen eines Profilskripts aus [!DNL Target] wird die Fehlermeldung „Fehler beim Löschen des Profilskripts“ angezeigt.

**Optionen:**

Führen Sie einen der folgenden Schritte aus:

* Löschen Sie das Profilskript erneut. Die Erfolgsmeldung wird angezeigt.
* Warten Sie etwa 10 Minuten, bis das [!DNL Target]-Import-Tool ausgeführt wird. Der Importer aktualisiert die Profilskriptliste.

## Einige ajax-Aufrufe von [!DNL Target] funktionieren nicht.

**Hinweis:** Mehrere ajax-[!DNL Target] mit demselben Namen, aber unterschiedlichen Parametern funktionieren auf derselben Seite nicht. Nur der erste Aufruf erfolgt.

## Sie haben über die [!DNL Target]-API eine Aktivität aktiviert, aber die Aktivität hat in der [!DNL Target]-Benutzeroberfläche  Status Inaktiv“.

Wenn Sie bestimmte Aktionen ausführen, wie zum Beispiel das Aktivieren einer Aktivität außerhalb der Benutzeroberfläche mithilfe der [!DNL Target]-API, kann es bis zu 10 Minuten dauern, bis die Aktualisierung bis zur Benutzeroberfläche propagiert wird.

## Nach der Aktivitätskonvertierung ist für den Besucher kein Erlebnis mehr vorhanden.

In seltenen Fällen kann es vorkommen, dass, wenn die Konversionsmetrik der Aktivität, die für ein Erlebnis qualifiziert ist, in derselben Anfrage wie die Aktivitätsqualifizierung gesendet wird, der Besucher nach dem Senden der Anfrage kein Erlebnis hat. In diesem Fall sieht der Besucher den Standardinhalt und die Erlebnis-ID, die über Token erfasst wird, wäre -1. [!DNL Adobe] empfiehlt nicht, Aktivitätsqualifizierung und -konvertierung in derselben [!DNL Target]-Anfrage zu senden.

Wenn Sie beide Metriken in derselben Anfrage senden möchten, können Sie mit [!UICONTROL Erweiterte Einstellungen] angeben, dass der Besucher nach der Konvertierung im selben Erlebnis bleibt.
