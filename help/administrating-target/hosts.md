---
description: Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.
keywords: Host;Hosts;Hostgruppe;Umgebung;Fehlerbehebung;Best Practices
seo-description: Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.
seo-title: Hosts
solution: Target
title: Hosts
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Hosts{#hosts}

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

## Hosts {#concept_516BB01EBFBD4449AB03940D31AEB66E}

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

In [!DNL Target Classic] gab es ähnliche Funktionen. Hostgruppen aus [!DNL Target Classic] werden in [!DNL Target Standard/Premium] als „Umgebungen“ bezeichnet.

Das Hauptziel bei der Hostverwaltung besteht darin, dafür zu sorgen, dass auf der Seite nicht versehentlich inaktive Inhalte erscheinen. Hostverwaltung ermöglicht es Ihnen zudem, Berichtsdaten nach Umgebung aufzuteilen.

Ein Host ist ein Webserver (oder eine Webdomäne), von dem aus Inhalte während der verschiedenen Phasen eines Projekts bereitgestellt werden. Alle Hosts, die eine Mbox beliefern, werden erkannt.

Zwecks einfacher Verwaltung werden Hosts in Umgebungen zusammengefasst. Es können beispielsweise mehrere Dutzend Hosts in zwei oder drei Umgebungen aufgeteilt werden. Zu den aktuellen Umgebungen gehören Produktion, Staging und Entwicklung. Sie können nach Wunsch neue Umgebungen hinzufügen oder alte umbenennen.

Die Standardumgebung ist bereits fest mit „Produktion“ benannt. Die Standardumgebung kann nicht gelöscht werden, auch nicht, wenn sie umbenannt wird. In [!DNL Target] wird angenommen, dass in dieser Gruppe fertiggestellte, genehmigte Aktivitäten und Tests bereitgestellt werden.

Wenn eine Mbox-Anfrage von neuen Websites oder Domänen empfangen wird, werden diese neuen Domänen stets in der Produktionsumgebung angezeigt. Die Einstellungen der Umgebung „Produktion“ können nicht geändert werden, sodass für unbekannte oder neue Sites definitiv nur die Inhalte angezeigt werden, die aktiv und fertig sind. Über die Hostverwaltung kann außerdem problemlos für die Qualität neuer Aktivitäten und Inhalte in der Testumgebung, Staging-Umgebung und Entwicklungsumgebung vor der Aktivierung der Aktivitäten gesorgt werden.

Target beschränkt einen Host nicht, der Mboxes senden und empfangen kann. Wenn also neue Server oder Domänen erkannt werden, funktionieren sie automatisch (außer es wurde eine Whitelist oder eine Blacklist eingerichtet). Auf diese Weise wird auch das Testen von Werbeanzeigen auf verschiedenen Domänen ermöglicht, die unbekannt sind oder nicht antizipiert werden können.

Um Hosts und Umgebungen zu verwalten, klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Erkennen von Hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Informationen über die Bedingungen, die erfüllt sein müssen, damit [!DNL Target] einen Host erkennt und ihn der Hostgruppenliste hinzufügt

Damit ein Host erkannt werden kann, müssen folgende Bedingungen erfüllt werden:

* Auf dem Host muss mindestens eine Mbox vorhanden sein.
* Eine Seite auf dem Host muss Folgendes aufweisen:

   * einen genauen [!DNL mbox.js]-Verweis
   * einen Mbox- oder automatisch generierten globalen Mbox-Aufruf

* Die Seite mit der Mbox muss in einem Browser angezeigt werden.

Nach Aufruf der Seite erscheint der Host in der [!UICONTROL Hostgruppenliste], sodass Sie ihn in einer Umgebung verwalten, eine Vorschau anzeigen und Aktivitäten und Tests starten können.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Dies umfasst sämtliche persönlichen Entwicklungsserver.

Stellen Sie nach dem Hinzufügen eines Hosts zur [!UICONTROL Hostgruppenliste] sicher, dass der Host erkannt wird.

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Hosts]**.
1. Wird der Host nicht angezeigt, aktualisieren Sie den Browser. 
Standardmäßig wird ein neu erkannter Host zur Umgebung „Produktion“ hinzugefügt. Diese Umgebung ist am sichersten, da es in ihr nicht zulässig ist, inaktive Aktivitäten über diese Hosts anzuzeigen.
1. (Bedingt) Verschieben Sie den Host in die Entwicklungs- oder Staging-Umgebung.

>[!NOTE]
>
>Die Umgebung „Produktion“ kann nicht gelöscht werden, auch nicht, wenn sie umbenannt wird. Es wird angenommen, dass in dieser Gruppe fertiggestellte, aktive Aktivitäten und Tests bereitgestellt werden. In der Standardumgebung ist es nicht zulässig, inaktive Kampagnen anzuzeigen.

## Verwalten von Hosts und Umgebungen {#concept_90573F5A52E04600A8C3C5897880C10F}

Informationen, die Sie dabei unterstützen, Hosts und Umgebungen (Hostgruppen) zu verwalten, darunter Einrichten der Standardberichterstattung, Erstellen von Whitelists, Ändern des Namens einer Umgebung, Verschieben eines Hosts in eine andere Umgebung und Löschen eines Hosts oder einer Umgebung


Um auf die [!UICONTROL Hostliste] zuzugreifen, klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Filtern, Sortieren und Durchsuchen der Hostgruppenliste {#section_068B23C9D8224EB78BC3B7C8580251B0}

Möchten Sie die [!UICONTROL Hostgruppenliste] nach Umgebung filtern, klicken Sie auf die Dropdownliste **[!UICONTROL Alle]und wählen Sie die gewünschte Umgebung aus (Produktion, Staging, Entwicklung oder eine von Ihnen erstellte, benutzerdefinierte Umgebung).**

Möchten Sie die [!UICONTROL Hostgruppenliste] sortieren, klicken Sie auf eine Spaltenüberschrift („Name“, „Umgebung“ oder „Zuletzt angefordert“), um die Liste auf- oder absteigend zu sortieren.

Möchten Sie die [!UICONTROL Hostgruppenliste] durchsuchen, geben Sie einen Suchbegriff in das Suchfeld ein.

## Auswählen mehrerer Hosts {#section_EF3B458475184B7EA997C3559714397C}

Möchten Sie mehrere Hosts auswählen, aktivieren Sie die Kontrollkästchen neben der Spalte [!UICONTROL Name] der gewünschten Hosts. Sie können alle ausgewählten Hosts verschieben oder löschen.

## Erstellen einer Umgebung {#section_32097D0993724DF3A202D164D3F18674}

1. Klicken Sie in der [!UICONTROL Hostgruppenliste] auf die Registerkarte **[!UICONTROL Umgebungen].**
1. Klicken Sie auf **[!UICONTROL Umgebung erstellen]**.
1. Geben Sie einen beschreibenden Namen für die Umgebung an.
1. Legen Sie den aktiven Modus für die Umgebung fest: [!UICONTROL Aktive Aktivitäten] oder [!UICONTROL aktive und inaktive Aktivitäten].
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Festlegen des Standardhosts für die Berichterstellung {#section_4F8539B07C0C45E886E8525C344D5FB0}

Sie können die Umgebung auswählen, die Sie als Standard für alle Aktivitätsberichte festlegen möchten.

Sollten Sie die Produktionsumgebung als Standardeinstellung festlegen, werden ihr automatisch alle unbekannten Hosts hinzugefügt und Datenberichte aus dieser Umgebung werden in die Standardberichtsansicht übernommen. Die Erstellung einer „reinen“ Umgebung gewährleistet hingegen, dass ausschließlich Coresites/Domänen eingeschlossen werden.

So legen Sie die Standardumgebung für die Berichterstellung fest:

1. Klicken Sie in der [!UICONTROL Hostgruppenliste] auf die Registerkarte **[!UICONTROL Einstellungen].**
1. Wählen Sie den Standardhost aus der Dropdownliste **[!UICONTROL Umgebungseinstellungen]aus.**
1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>[!DNL Recommendations]-Benutzer müssen ihre Verhaltens- und Produktdatenbank neu erstellen, wenn Hosts die Hostgruppen wechseln.

## Erstellen von Whitelists, die Hosts identifizieren, die Mbox-Anrufe an Target senden können{#section_0AF7F56C386A42C381AF704DEF08D5CC}

Sie können eine Whitelist erstellen, in der Hosts (Domänen) aufgeführt sind, die Mbox-Aufrufe an [!DNL Target] senden können. Alle anderen Hosts, die Anrufe generieren, erhalten eine kommentierte Fehlermeldung, dass sie nicht autorisiert sind. Hosts, die einen Mbox-Anruf enthalten, werden standardmäßig bei [!DNL Target] in der Hostgruppe „Produktion“ registriert und erhalten Zugriff auf alle aktiven und genehmigten Aktivitäten. Wenn dies nicht gewünscht wird, können Sie mithilfe der Whitelist bestimmte Hosts festlegen, die zu Mbox-Aufrufen berechtigt sind und [!DNL Target]-Kampagneninhalte empfangen dürfen. Alle Hosts werden weiterhin in der [!UICONTROL Hostgruppenliste] angezeigt und sie können nach wie vor in den Umgebungen gruppiert und mit verschiedenen Ebenen versehen werden, beispielsweise, ob ein Host aktive und/oder inaktive Kampagnen sehen kann.

So erstellen Sie eine Whitelist:

1. Klicken Sie in der [!UICONTROL Hostgruppenliste] auf die Registerkarte **[!UICONTROL Einstellungen].**
1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Aktivierte Hosts für Inhaltsbereitstellung aktivieren].**
1. Fügen Sie nach Wunsch Hosts im Feld **[!UICONTROL Im Host enthalten]hinzu.**

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn auf einem nicht autorisierten Host ein Mbox-Aufruf erfolgt, antwortet der Aufruf mit `/* no display - unauthorized mbox host */`.

Die Whitelist hat gegenüber Umgebungen Vorrang. Wir empfehlen, alle Hosts zu löschen, bevor Sie die Whitelist-Funktionen nutzen. Dann werden nur die in der Whitelist zugelassenen Hosts in der Hostliste angezeigt. Anschließend können Sie die Hosts in die gewünschten Umgebungen verschieben.

Manchmal erscheinen Hosts anderer Sites in Ihren Umgebungen. Eine Domäne wird in der Liste angezeigt, wenn die Domäne Ihre mbox.js aufruft. Wenn beispielsweise eine Ihrer Webseiten auf den Server eines anderen kopiert wird, wird diese Domäne in Ihrer Umgebung angezeigt. Es können auch Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt werden.

In Fällen, in denen `mboxHost` an einen API-Aufruf weitergegeben wird, wird die Konversion für die weitergegebene Umgebung aufgezeichnet. Wenn keine Umgebung weitergegeben wird, ist der Host beim Aufruf standardmäßig „Produktion“.

Des Weiteren können Sie eine Blacklist erstellen, in der Hosts (Domänen) aufgeführt werden, die keine Mbox-Aufrufe an [!DNL Target] senden können, indem Sie die entsprechenden Hosts in das Feld [!UICONTROL Nicht im Host enthalten] einfügen.

## Ändern des Namens einer Umgebung {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klicken Sie in der [!UICONTROL Hostgruppenliste] auf die Registerkarte **[!UICONTROL Umgebungen].**
1. Halten Sie den Mauszeiger über die gewünschte Umgebung und klicken Sie auf das **[!UICONTROL Bearbeitungssymbol.]**
1. Ändern Sie den Namen der Umgebung.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Verschieben eines Hosts in eine andere Umgebung {#section_9F52549958BD485EB74FE78C32773D2A}

1. Halten Sie in der [!UICONTROL Hostgruppenliste] den Mauszeiger über denjenigen Host, den Sie verschieben möchten.
1. Klicken Sie auf das Symbol für das **[!UICONTROL Verschieben.]**
1. Wählen Sie aus der Dropdownliste die gewünschte Umgebung aus und klicken Sie auf das Häkchen.

## Löschen eines Hosts {#section_F56355BA4BC54B078A1A8179BC954632}

Sie können einen Host, der nicht mehr gebraucht wird, löschen.

1. Halten Sie in der [!UICONTROL Hostgruppenliste] den Mauszeiger über denjenigen Host, den Sie löschen möchten.
1. Klicken Sie auf das **[!UICONTROL Löschsymbol.]**
1. Klicken Sie auf **[!UICONTROL Löschen], um den Löschvorgang zu bestätigen.**

>[!NOTE]
>
>Der Host wird erneut aufgeführt, wenn jemand auf dem Host eine Seite mit Mbox aufruft.

## Löschen einer Umgebung {#section_737F8869612047868D03FC755B1223D3}

Sie können eine Umgebung, die nicht mehr benötigt wird, löschen.

1. Klicken Sie in der [!UICONTROL Hostgruppenliste] auf die Registerkarte **[!UICONTROL Umgebungen].**
1. Halten Sie den Mauszeiger über die Umgebung, die Sie löschen möchten.
1. Klicken Sie auf das **[!UICONTROL Löschsymbol.]**
1. Klicken Sie auf **[!UICONTROL Löschen], um den Löschvorgang zu bestätigen.**

>[!NOTE]
>
>Die Umgebung „Produktion“ kann nicht gelöscht werden, sie kann jedoch umbenannt werden.

## Fehlerbehebung für Hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Best Practices für die Verwaltung von und Fehlerbehebung in [!DNL Adobe Target].

Probieren Sie folgende Methoden zur Fehlerbehebung aus, falls Probleme mit Ihren Hosts auftreten:

**Der Host wird in der Mbox-Liste des Kontos nicht angezeigt.**

* Aktualisieren Sie die Seite [!UICONTROL Hosts] Ihres Browsers.
* Überprüfen Sie den Mbox-Code einschließlich des [!DNL mbox.js]-Verweises auf seine Richtigkeit.
* Versuchen Sie es damit, zu einer der Mboxes auf dem Host zu surfen. Es besteht die Möglichkeit, dass keine Mbox auf dem Host bislang in einem Browser wiedergegeben wurde.

**In der[!UICONTROL Hostgruppenliste]werden zufällige oder unbekannte Domänen angezeigt.**

Eine Domäne wird in der Liste angezeigt, wenn von der Domäne [!DNL Target] aufgerufen wurde. Häufig werden Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt. Wenn eine aufgeführte Domäne von Ihrem Team nicht verwendet wird, können Sie auf [!UICONTROL Löschen] klicken, um sie zu entfernen.

**Meine Mbox gibt die Meldung /* Keine Anzeige - nicht autorisierter Mbox-Host */ zurück.**

Wenn ein Mbox-Aufruf auf einem nicht autorisierten Host erfolgt, antwortet der Aufruf mit /* Keine Anzeige - nicht autorisierter Mbox-Host */.

## Recommendations: Sammlungen und Ausschlüsse nach Umgebung (Hostgruppe) filtern

![Premium-Zeichen](/help/assets/premium.png)

Sie können eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>Recommendations-Aktivitäten sind als Bestandteil der Target Premium-Lösung verfügbar. Ohne Target Premium-Lizenz sind sie nicht für Target Standard verfügbar.

Die Hostgruppe kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Verwendungen zu trennen. Sie können beispielsweise Hostgruppen für Entwicklungs- und Produktionsumgebungen, unterschiedliche Marken oder unterschiedliche Länder verwenden. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Mit dem Umgebungsfilter können Sie auch eine andere Hostgruppe auswählen, um die Ergebnisse in der Vorschau anzuzeigen.) Neu hinzugefügte Elemente sind standardmäßig in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wurde eine Umgebungs-ID angegeben. Bereitgestellte Empfehlungen hängen von der in der Anfrage angegebenen Hostgruppe ab.

Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.

Der Umgebungsfilter ist an den folgenden Orten in der Target-Benutzeroberfläche verfügbar:

* Katalogsuche ([!UICONTROL Recommendations &gt; Katalogsuche])
* Dialogfeld „Sammlung erstellen“ ([!UICONTROL Recommendations &gt; Sammlungen &gt; Neu erstellen])
* Dialogfeld „Sammlung aktualisieren“ ([!UICONTROL Recommendations &gt; Sammlungen &gt; Bearbeiten])
* Dialogfeld „Ausschluss erstellen“ ([!UICONTROL Recommendations &gt; Ausschlüsse &gt; Neu erstellen])
* Dialogfeld „Ausschluss aktualisieren“ ([!UICONTROL Recommendations &gt; Ausschlüsse &gt; Bearbeiten])
