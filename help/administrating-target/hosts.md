---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist
description: Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.
title: Hosts
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: 34c4c48602df8550287e86c535ebc350fe2185f7
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 68%

---


# Hosts{#hosts}

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

Das Hauptziel bei der Hostverwaltung besteht darin, dafür zu sorgen, dass auf der Seite nicht versehentlich inaktive Inhalte erscheinen. Host management also lets you separate report data by [environment](/help/administrating-target/environments.md).

Ein Host ist ein Webserver (oder eine Webdomäne), von dem aus Inhalte während der verschiedenen Phasen eines Projekts bereitgestellt werden. Alle Hosts, die eine Mbox beliefern, werden erkannt.

Zwecks einfacher Verwaltung werden Hosts in Umgebungen zusammengefasst. Es können beispielsweise mehrere Dutzend Hosts in zwei oder drei Umgebungen aufgeteilt werden. The preset environments include [!UICONTROL Production], [!UICONTROL Staging], and [!UICONTROL Development]. Sie können nach Wunsch neue Umgebungen hinzufügen oder alte umbenennen.

One environment, the default environment, is pre-named [!UICONTROL Production]. Die Standardumgebung kann nicht gelöscht werden, auch nicht, wenn sie umbenannt wird. In [!DNL Target] wird angenommen, dass in dieser Gruppe fertiggestellte, genehmigte Aktivitäten und Tests bereitgestellt werden.

When an mbox request is received from new websites or domains, these new domains always appear in the [!UICONTROL Production] environment. The [!UICONTROL Production] environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. Über die Hostverwaltung kann außerdem problemlos für die Qualität neuer Aktivitäten und Inhalte in der Testumgebung, Staging-Umgebung und Entwicklungsumgebung vor der Aktivierung der Aktivitäten gesorgt werden.

[!DNL Target] beschränkt einen Host nicht, der Mboxes senden und empfangen kann. Wenn also neue Server oder Domänen erkannt werden, funktionieren sie automatisch (außer es wurde eine Whitelist oder eine Blacklist eingerichtet). Auf diese Weise wird auch das Testen von Werbeanzeigen auf verschiedenen Domänen ermöglicht, die unbekannt sind oder nicht antizipiert werden können.

Um Hosts zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Recognizing hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Um einen Host zu erkennen und ihn der [!UICONTROL Hosts] -Liste hinzuzufügen, müssen die folgenden Bedingungen erfüllt sein:

* Auf dem Host muss mindestens eine Mbox vorhanden sein.
* Eine Seite auf dem Host muss  Folgendes aufweisen:

   * Ein genauer &quot;at.js&quot;- oder &quot;mbox.js&quot;-Verweis
   * einen Mbox- oder automatisch generierten globalen Mbox-Aufruf

* Die Seite mit der Mbox muss in einem Browser angezeigt werden.

Nach Aufruf der Seite erscheint der Host in der [!UICONTROL Hostgruppenliste], sodass Sie ihn in einer Umgebung verwalten, eine Vorschau anzeigen und Aktivitäten und Tests starten können.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Dies umfasst sämtliche persönlichen Entwicklungsserver.

Stellen Sie nach dem Hinzufügen eines Hosts zur [!UICONTROL Hostgruppenliste] sicher, dass der Host erkannt wird.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Wird der Host nicht angezeigt, aktualisieren Sie den Browser. 


   By default, a newly recognized host is placed in the [!UICONTROL Production] environment. Diese Umgebung ist am sichersten, da es in ihr nicht zulässig ist, inaktive Aktivitäten über diese Hosts anzuzeigen.

1. (Bedingt) Klicken Sie auf das Symbol Verschieben ( ![Verschieben-Symbol](/help/administrating-target/assets/icon-move.png) ), um den Host in die [!UICONTROL Entwicklungs]-, [!UICONTROL Staging]- oder andere Umgebung zu verschieben.

>[!NOTE]
>
>The [!UICONTROL Production] environment cannot be deleted, even if you rename it. Es wird angenommen, dass in dieser Gruppe fertiggestellte, aktive Aktivitäten und Tests bereitgestellt werden. In der Standardumgebung ist es nicht zulässig, inaktive Kampagnen anzuzeigen.

## Sort or search the Hosts list {#section_068B23C9D8224EB78BC3B7C8580251B0}

To sort the [!UICONTROL Hosts] list, click any column header ([!UICONTROL Name], [!UICONTROL Environment], or [!UICONTROL Last Requested]) to sort the list in ascending or descending order.

To search the [!UICONTROL Hosts] list, type a search term in the [!UICONTROL Search Hosts] box.

## Create whitelists that specify hosts that are authorized to send mbox calls to Target. {#whitelist}

Sie können eine Whitelist erstellen, in der Hosts (Domänen) aufgeführt sind, die Mbox-Aufrufe an [!DNL Target] senden können. Alle anderen Hosts, die Anrufe generieren, erhalten eine kommentierte Fehlermeldung, dass sie nicht autorisiert sind. Hosts, die einen Mbox-Anruf enthalten, werden standardmäßig bei [!DNL Target] in der Hostgruppe „Produktion“ registriert und erhalten Zugriff auf alle aktiven und genehmigten Aktivitäten. Wenn dies nicht gewünscht wird, können Sie mithilfe der Whitelist bestimmte Hosts festlegen, die zu Mbox-Aufrufen berechtigt sind und [!DNL Target]-Kampagneninhalte empfangen dürfen. Alle Hosts werden weiterhin in der [!UICONTROL Hostgruppenliste] angezeigt und sie können nach wie vor in den Umgebungen gruppiert und mit verschiedenen Ebenen versehen werden, beispielsweise, ob ein Host aktive und/oder inaktive Kampagnen sehen kann.

So erstellen Sie eine Whitelist:

1. Klicken Sie in der Liste [!UICONTROL Hosts] auf Hosts **[!UICONTROL autorisieren]**.
1. Aktivieren Sie den Umschalter Autorisierte Hosts für Content Versand **[!UICONTROL aktivieren]** .
1. Add the desired hosts in the **[!UICONTROL Host contains]** box, as desired.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Add the desired hosts in the **[!UICONTROL Host does not contains]** box, as desired.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn auf einem nicht autorisierten Host ein Mbox-Aufruf erfolgt, antwortet der Aufruf mit `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best Practices** für Sicherheit: Wenn Sie Ubox-Funktionen von verwenden, [!DNL Target]beachten Sie, dass diese Whitelist auch die Liste der Domänen steuert, zu denen Ihre [Weiterleitungen](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) navigieren können. Stellen Sie sicher, dass Sie alle Domänen hinzufügen, denen Sie umleiten möchten, wenn Sie Ubox als Teil Ihrer Implementierung verwenden. Wenn die Whitelist nicht angegeben ist, kann Adobe die Umleitungs-URLs nicht überprüfen und vor möglichen bösartigen Umleitungen schützen.
>
>Die Whitelist hat gegenüber Umgebungen Vorrang. Wir empfehlen, alle Hosts zu löschen, bevor Sie die Whitelist-Funktionen nutzen. Dann werden nur die in der Whitelist zugelassenen Hosts in der Hostliste angezeigt. Anschließend können Sie die Hosts in die gewünschten Umgebungen verschieben.

Manchmal erscheinen Hosts anderer Sites in Ihren Umgebungen. Eine Domäne wird in der Liste angezeigt, wenn die Domäne Ihre &quot;at.js&quot;oder &quot;mbox.js&quot;aufruft. Wenn beispielsweise eine Ihrer Webseiten auf den Server eines anderen kopiert wird, wird diese Domäne in Ihrer Umgebung angezeigt. Es können auch Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt werden.

In Fällen, in denen `mboxHost` an einen API-Aufruf weitergegeben wird, wird die Konversion für die weitergegebene Umgebung aufgezeichnet. If no environment is passed, the host in the call defaults to [!UICONTROL Production].

Des Weiteren können Sie eine Blacklist erstellen, in der Hosts (Domänen) aufgeführt werden, die keine Mbox-Aufrufe an [!DNL Target] senden können, indem Sie die entsprechenden Hosts in das Feld [!UICONTROL Nicht im Host enthalten] einfügen.

## Delete a host {#section_F56355BA4BC54B078A1A8179BC954632}

Sie können einen Host, der nicht mehr gebraucht wird, löschen.

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Delete]** icon.
1. Klicken Sie auf **[!UICONTROL Löschen]**, um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Der Host wird erneut aufgeführt, wenn jemand auf dem Host eine Seite mit Mbox aufruft.

## Fehlerbehebung für Hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Best Practices für die Verwaltung von und Fehlerbehebung in [!DNL Adobe Target].

Probieren Sie folgende Methoden zur Fehlerbehebung aus, falls Probleme mit Ihren Hosts auftreten:

**Der Host wird in der Mbox-Liste des Kontos nicht angezeigt.**

* Aktualisieren Sie die Seite [!UICONTROL Hosts] Ihres Browsers.
* Vergewissern Sie sich, dass der mbox-Code einschließlich des Verweises auf at.js oder mbox.js korrekt ist.
* Versuchen Sie es damit, zu einer der Mboxes auf dem Host zu surfen. Es besteht die Möglichkeit, dass keine Mbox auf dem Host bislang in einem Browser wiedergegeben wurde.

**In der[!UICONTROL Hostgruppenliste]werden zufällige oder unbekannte Domänen angezeigt.**

Eine Domäne wird in der Liste angezeigt, wenn von der Domäne [!DNL Target] aufgerufen wurde. Häufig werden Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt. Wenn eine aufgeführte Domäne von Ihrem Team nicht verwendet wird, können Sie auf [!UICONTROL Löschen] klicken, um sie zu entfernen.

**Meine Mbox gibt die Meldung /* Keine Anzeige - nicht autorisierter Mbox-Host */ zurück.**

Wenn ein Mbox-Aufruf auf einem nicht autorisierten Host erfolgt, antwortet der Aufruf mit /* Keine Anzeige - nicht autorisierter Mbox-Host */.
