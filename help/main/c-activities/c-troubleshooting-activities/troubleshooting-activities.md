---
keywords: Fehlerbehebung in Target;Problembehebung in Target;Standardinhalte;Test nicht verfügbar;Aktivität nicht verfügbar;Targeting funktioniert nicht;vorheriges Erlebnis erscheint;kann keine Aktivitäten erstellen;Aktivitäten erstellen;Seitenstruktur geändert;Seitenstruktur modifiziert;Fehlermeldung;Fehler beim Löschen von Profilskript;AJAX funktioniert nicht
description: Sollte Ihre Adobe-[!DNL Target]-Aktivität nicht auf Ihrer Site erscheinen, finden Sie hier Vorschläge zur Fehlerbehebung.
title: Wie kann ich Probleme in Verbindung mit Aktivitäten beheben?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
TQID: 'https://experienceleague.adobe.com/L-011t7q6c3aICs0ZrM01m9pZByH86FKGiLG1A7Rl2s'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9621044454d3e1b47c06cac2ad5d08cba8e482c0
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 7%
---
# Erste Schritte mit Aktivitäten zur Fehlerbehebung {#troubleshooting-activities}

>[!BEGINSHADEBOX]

**Auf dieser Seite** finden Sie Lösungen für häufige Probleme, wenn eine [!DNL Adobe Target] Aktivität nicht auf Ihrer Site erscheint oder sich nicht wie erwartet verhält.

>[!ENDSHADEBOX]

Verschiedene Ursachen können verhindern, dass eine [!DNL Adobe Target] Aktivität auf Ihrer Site angezeigt wird. Verwenden Sie die folgenden Probleme und Lösungsvorschläge, um die Ursache zu identifizieren und die Lösung anzuwenden.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen zur Fehlerbehebung finden Sie unter [Fehlerbehebung in Target](/help/main/r-troubleshooting-target/troubleshooting-target.md) Links zu weiteren Themen zur Fehlerbehebung, FAQs und andere nützliche Informationen zu Fehlerbehebungsaktivitäten und anderen Funktionen in [!DNL Adobe Target].

## Die Aktivität wird nicht wie erwartet angezeigt {#not-displayed}

+++ Standardinhalt wird angezeigt

Vergewissern Sie sich, dass Ihre Aktivität abgeschlossen ist und aktiviert wurde.

+++

</br>

+++ Aktivität ist nicht live

**Validieren** Überprüfen Sie auf der Registerkarte **[!UICONTROL Übersicht]**, ob die Aktivität als inaktiv oder als Entwurf markiert ist.

**Optionen:**

* die Aktivität aktivieren.
* Verwenden Sie Vorschau-Links, um die inaktive Aktivität anzuzeigen.

+++

</br>

+++ Sie sind nicht für die Zielgruppen-Targeting-Bedingungen qualifiziert

**Validieren** Überprüfen Sie die Zielgruppenbestimmungsbedingungen auf der Seite **[!UICONTROL Übersicht]**.

**Optionen:**

* Für die Zielgruppe qualifizieren und dann erneut versuchen.
* Verwenden Sie Vorschau-Links, um die Targeting-Bedingungen zu umgehen.

+++

</br>

+++ Die Seite ist nicht für die Bedingungen zum Seiten-Targeting qualifiziert

**Validieren:** Stellen Sie auf der Seite **[!UICONTROL Übersicht]** fest, ob die Seite außerhalb der Zielgruppenbestimmungsbedingungen liegt.

**Optionen:**

* Wechseln Sie zu **[!UICONTROL Visual Experience Composer]** und klicken Sie auf URL > Erweitert > Aktuelle Seite.

+++

</br>

+++ Ein vorheriges Erlebnis wird anstelle des neuen angezeigt

**Validieren:** Versuchen Sie eine der folgenden Optionen und versuchen Sie dann erneut, das Erlebnis anzuzeigen.

**Optionen:**

* Cache und Cookies löschen und erneut versuchen.
* Versuchen Sie es mit einem anderen Browser.
* Privaten oder Inkognito-Modus verwenden.

+++

</br>

+++ Die Struktur der Seite hat sich seit der Einrichtung der Aktivität geändert

**Validieren** Wechseln Sie zum **[!UICONTROL Visual Experience Composer]** für die vorhandene Aktivität und suchen Sie nach einer Warnmeldung, die anzeigt, dass sich die Selektoren (oder die Struktur) geändert haben.

**Optionen:**

* Erstellen Sie die Aktivität erneut.

Weitere Informationen darüber, wie Seitenänderungen die Anzeige von Inhalten durch [!DNL Target] beeinflussen, finden Sie unter [Szenarien für Seitenänderungen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md).

+++

</br>

+++ Die Struktur der Seite wird beim Laden der Seite (zur Laufzeit) geändert

**Validieren** Fragen Sie Ihren Entwickler.

**Hinweis:** Damit [!DNL Target] erkennen können, wo Aktivitätsänderungen angewendet werden müssen, sollten Sie kein Element mit derselben Klasse dynamisch einfügen oder die Klasse von gleichrangigen Elementen dynamisch ändern.

**Optionen:**

* Aktualisieren Sie den Seiten-Code mithilfe einer ID, um jedes getestete Element eindeutig zu identifizieren.
* Beenden Sie die dynamische Änderung der Klasse oder der gleichrangigen Elemente wie oben beschrieben.

Weitere Informationen darüber, wie Seitenänderungen die Anzeige von Inhalten durch [!DNL Target] beeinflussen, finden Sie unter [Szenarien für Seitenänderungen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md).

+++

</br>

+++ Andere Aktivitäten werden auf derselben Seite ausgeführt

**Validieren:** Verwenden Sie die Registerkarte **[!UICONTROL Kollisionen]** um zu sehen, ob andere Aktivitäten ausgeführt werden.

**Hinweis:** Die Registerkarte **[!UICONTROL Kollisionen]** funktioniert nicht mit dem Vorlagentestmodul.

**Optionen:**

* Erhöhen Sie die Priorität dieser Aktivität.
* Die Priorität der anderen Aktivitäten herabsetzen
* Deaktivieren Sie die anderen Aktivitäten.

+++

## Benutzer, API und die Benutzeroberfläche {#users-api-ui}

+++ Ich habe eine Aktivität in der [!DNL Target]-Benutzeroberfläche erstellt und kann sie nicht über die API aktualisieren

Aktivitäten, die mit der [!DNL Target]-Benutzeroberfläche erstellt wurden, sollten über die [!DNL Target]-Benutzeroberfläche aktualisiert werden. Dagegen sollten über die API erstellte Aktivitäten über die API aktualisiert werden. Wenn Sie beispielsweise eine Aktivität über die API erstellen, diese aber später über die [!DNL Target]-Benutzeroberfläche bearbeiten, werden nicht alle Änderungen aktualisiert. Alle Änderungen werden im Backend gespeichert und können durch einen weiteren API-Aufruf aktualisiert werden.

Aktualisieren Sie die Aktivität am besten mithilfe derselben Methode (Benutzeroberfläche oder API), mit der sie erstellt wurde.

+++

</br>

+++ Sie wurden kürzlich zu [!DNL Target] hinzugefügt, können jedoch keine Aktivitäten erstellen

**Validieren:** Klicken Sie auf **[!UICONTROL Aktivität erstellen]**. Wenn die Option nicht verfügbar ist, sind Sie wahrscheinlich nicht dazu berechtigt, eine Aktivität zu erstellen.

**Optionen:**

Nachdem Sie in [!DNL Target] als Benutzer hinzugefügt wurden, benötigen Sie die Rolle **[!UICONTROL Genehmiger]** , um Aktivitäten zu erstellen.

* Bitten Sie den Administrator Ihres Kontos, Sie zu einer genehmigenden Person zu machen.
* Falls Sie selbst der Administrator sind, erteilen Sie sich **[!UICONTROL [!DNL Target] unter**&#x200B;[!UICONTROL &#x200B; Administration &#x200B;]&#x200B;**>**&#x200B;[!UICONTROL &#x200B; Benutzer &#x200B;]&#x200B;**die Rolle „Genehmiger]**. Siehe [Weisen Sie sich selbst die Rolle der genehmigenden Person zu](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

+++

</br>

+++ Sie haben über die [!DNL Target]-API eine Aktivität aktiviert, aber die Aktivität hat in der [!DNL Target]-Benutzeroberfläche  Status Inaktiv“

Wenn Sie bestimmte Aktionen ausführen, wie zum Beispiel eine Aktivität außerhalb der Benutzeroberfläche über die [!DNL Target]-API zu aktivieren, kann es bis zu 10 Minuten dauern, bis die Aktualisierung bis zur Benutzeroberfläche propagiert wird.

+++

</br>

+++ Beim Löschen eines Profilskripts wird eine Fehlermeldung angezeigt

**Validieren** Beim Löschen eines Profilskripts aus [!DNL Target] wird die Fehlermeldung „Fehler beim Löschen des Profilskripts“ angezeigt.

**Optionen:**

Führen Sie einen der folgenden Schritte aus:

* Löschen Sie das Profilskript erneut. Die Erfolgsmeldung wird angezeigt.
* Warten Sie etwa 10 Minuten, bis das [!DNL Target]-Import-Tool ausgeführt wird. Der Importer aktualisiert die Profilskriptliste.

+++

## Aufrufe und Konversion {#calls-and-conversion}

+++ Einige ajax-[!DNL Target] funktionieren nicht.

**Hinweis:** Mehrere ajax-[!DNL Target] mit demselben Namen, aber unterschiedlichen Parametern funktionieren auf derselben Seite nicht. Nur der erste Aufruf erfolgt.

+++

</br>

+++ Nach der Aktivitätskonvertierung ist für den Besucher kein Erlebnis mehr vorhanden

In seltenen Fällen kann es vorkommen, dass, wenn die Konversionsmetrik der Aktivität, die einen Besucher für ein Erlebnis qualifiziert, in derselben Anfrage wie die Aktivitätsqualifikation gesendet wird, der Besucher nach dem Senden der Anfrage kein Erlebnis hat. In diesem Fall sieht der Besucher den Standardinhalt und die über Token erfasste Erlebnis-ID lautet -1. [!DNL Adobe] empfiehlt nicht, Aktivitätsqualifizierung und -konvertierung in derselben [!DNL Target]-Anfrage zu senden.

Wenn Sie beide Metriken in derselben Anfrage senden möchten, können Sie mit **[!UICONTROL Erweiterte Einstellungen]** angeben, dass der Besucher nach der Konvertierung im selben Erlebnis bleibt.

+++
