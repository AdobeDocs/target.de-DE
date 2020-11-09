---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.
title: Hosts
feature: hosts and environments
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 27%

---


# Hosts{#hosts}

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

Das Hauptziel bei der Hostverwaltung besteht darin, dafür zu sorgen, dass auf der Seite nicht versehentlich inaktive Inhalte erscheinen. Host management also lets you separate report data by [environment](/help/administrating-target/environments.md).

Ein Host ist eine Domäne, von der aus eine [!DNL Target] Anforderung ausgeführt wird. Auf einer Website ist es normalerweise die `location.hostname` Eigenschaft der URL, die die [!DNL Target] Anforderung ausführt.

Standardmäßig beschränkt [!DNL Target] dies keinen Host, der [!DNL Target] [!DNL Target] Anforderungen stellen und Antworten empfangen kann. Wenn neue Hosts Anforderungen stellen, funktionieren diese automatisch. Dies ermöglicht auch Tests auf verschiedenen Domänen, die Sie nicht kennen oder nicht vorhersehen können. Wenn Sie dieses Standardverhalten außer Kraft setzen möchten, können Sie eine Zulassungsliste oder Blockierungsliste einrichten, um zu begrenzen, mit welchen Hosts gearbeitet wird [!DNL Target].

Um Hosts zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Recognizing hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Um einen Host zu erkennen und ihn der [!UICONTROL Hosts] -Liste hinzuzufügen, müssen die folgenden Bedingungen erfüllt sein:

* At least one [!DNL Target] request must exist on the host
* Eine Seite auf dem Host muss  Folgendes aufweisen:

   * Ein genauer &quot;at.js&quot;- oder &quot;mbox.js&quot;-Verweis
   * Eine [!DNL Target] Anforderung oder eine automatisch generierte globale [!DNL Target] Anforderung

* The page with the [!DNL Target] request must be viewed in a browser

After the page is viewed, the host is listed in the [!UICONTROL Hosts] list, allowing you to manage it in an environment, as well as preview and launch activities and tests.

>[!NOTE]
>
>Dies umfasst sämtliche persönlichen Entwicklungsserver.

Stellen Sie nach dem Hinzufügen eines Hosts zur [!UICONTROL Hostgruppenliste] sicher, dass der Host erkannt wird.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Wird der Host nicht angezeigt, aktualisieren Sie den Browser. 


   By default, a newly recognized host is placed in the [!UICONTROL Production] environment. Diese Umgebung ist am sichersten, da es in ihr nicht zulässig ist, inaktive Aktivitäten über diese Hosts anzuzeigen.

1. (Bedingt) Klicken Sie auf das Symbol **[!UICONTROL Verschieben]** ( ![Verschieben-Symbol](/help/administrating-target/assets/icon-move.png) ), um den Host in die Umgebung [!UICONTROL Entwicklung], [!UICONTROL Staging]oder eine andere  zu verschieben.

>[!NOTE]
>
>The [!UICONTROL Production] environment cannot be deleted, even if you rename it. Es wird angenommen, dass in dieser Gruppe fertiggestellte, aktive Aktivitäten und Tests bereitgestellt werden. In der Standardumgebung ist es nicht zulässig, inaktive Kampagnen anzuzeigen.

## Sort or search the Hosts list {#section_068B23C9D8224EB78BC3B7C8580251B0}

To sort the [!UICONTROL Hosts] list, click any column header ([!UICONTROL Name], [!UICONTROL Environment], or [!UICONTROL Last Requested]) to sort the list in ascending or descending order.

To search the [!UICONTROL Hosts] list, type a search term in the [!UICONTROL Search Hosts] box.

## Create allowlists that specify hosts that are authorized to send Target requests to Target. {#allowlist}

You can create an allowlist that specifies hosts (domains) that are authorized to send [!DNL Target] requests to [!DNL Target]. Alle anderen Hosts, die Anforderungen generieren, erhalten eine kommentierte Fehlermeldung zur Autorisierung. By default, any host that contains a [!DNL Target] request registers with [!DNL Target] in the [!UICONTROL Production] environment and has access to all active and approved activities. If this is not the desired approach, you can instead use the allowlist to record specific hosts that are eligible to make [!DNL Target] requests and receive [!DNL Target] content. All hosts will continue to display in the [!UICONTROL Hosts] list, and environments can still be used to group these hosts and assign different levels to each, such as whether the host can see active and/or inactive activities.

So erstellen Sie eine Zulassungsliste:

1. Klicken Sie in der Liste [!UICONTROL Hosts] auf Hosts **[!UICONTROL autorisieren]**.
1. Aktivieren Sie den Umschalter Autorisierte Hosts für Content Versand **[!UICONTROL aktivieren]** .
1. Add the desired hosts in the **[!UICONTROL Host contains]** box, as desired.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Add the desired hosts in the **[!UICONTROL Host does not contains]** box, as desired.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

If a [!DNL Target] request is made on an unauthorized host, the call will respond with `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best Practices** für Sicherheit: Wenn Sie die Ubox-Funktion von verwenden, [!DNL Target]beachten Sie, dass diese Zulassungsliste auch die Liste der Domänen steuert, zu denen Ihre [Weiterleitungen](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) navigieren können. Stellen Sie sicher, dass Sie alle Domänen hinzufügen, denen Sie umleiten möchten, wenn Sie Ubox als Teil Ihrer Implementierung verwenden. Wenn die Zulassungsliste nicht angegeben ist, [!DNL Adobe] können die Umleitungs-URLs nicht überprüft und vor möglichen böswilligen Umleitungen geschützt werden.
>
>Die Zulassungsliste hat Vorrang vor Umgebung. Sie sollten alle Hosts löschen, bevor Sie die Funktion &quot;Zulassungsliste&quot;verwenden. Dann werden nur die Hosts angezeigt, die von der Zulassungsliste zugelassen sind. Anschließend können Sie die Hosts in die gewünschten Umgebungen verschieben.

Manchmal erscheinen Hosts anderer Sites in Ihren Umgebungen. Eine Domäne wird in der Liste angezeigt, wenn die Domäne Ihre &quot;at.js&quot;oder &quot;mbox.js&quot;aufruft. Wenn beispielsweise eine Ihrer Webseiten auf den Server eines anderen kopiert wird, wird diese Domäne in Ihrer Umgebung angezeigt. Es können auch Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt werden.

In Fällen, in denen `mboxHost` an einen API-Aufruf weitergegeben wird, wird die Konversion für die weitergegebene Umgebung aufgezeichnet. If no environment is passed, the host in the call defaults to [!UICONTROL Production].

You can also create a denylist that specifies hosts (domains) than cannot send [!DNL Target] requests to [!DNL Target] by adding the desired hosts in the [!UICONTROL Host Does Not Contain] box.

>[!NOTE]
>
>Da die Liste &quot;Autorisierte Hosts&quot;sowohl für [!DNL Target] Hosts als auch für Standard-Umleitungshosts verwendet wird, müssen Sie alle vorhandenen Domänen hinzufügen, die für die Verwendung des [!DNL Adobe Target] JavaScript-SDK (at.js) zugelassen sind, *UND* alle Domänen, die in den Ubox-Standard-Umleitungs-URLs verwendet werden. Sie müssen der Zulassungsliste in Zukunft auch alle neuen ähnlichen Domänen hinzufügen.

## Delete a host {#section_F56355BA4BC54B078A1A8179BC954632}

Sie können einen Host, der nicht mehr gebraucht wird, löschen.

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Delete]** icon.
1. Klicken Sie auf **[!UICONTROL Löschen]**, um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Der Host wird erneut aufgeführt, wenn jemand zu einer Seite navigiert, die eine [!DNL Target] Anforderung auf dem Host enthält.

## Fehlerbehebung für Hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probieren Sie folgende Methoden zur Fehlerbehebung aus, falls Probleme mit Ihren Hosts auftreten:

**Der Host wird nicht in der Liste für Ihr Konto angezeigt.**

* Aktualisieren Sie die Seite [!UICONTROL Hosts] Ihres Browsers.
* Überprüfen Sie, ob die [!DNL Target] Anforderung korrekt ist, einschließlich des Verweises auf at.js oder mbox.js.
* Try browsing to one of the [!DNL Target] requests on the host. It&#39;s possible that no [!DNL Target] request on the host was ever rendered in a browser.

**In der [!UICONTROL Hostgruppenliste] werden zufällige oder unbekannte Domänen angezeigt.**

A domain appears in this list if a request to [!DNL Target] is made from the domain. Häufig werden Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt. Wenn eine aufgeführte Domäne von Ihrem Team nicht verwendet wird, können Sie auf [!UICONTROL Löschen] klicken, um sie zu entfernen.

**Meine [!DNL Target] Anfrage gibt /* keine Anzeige - nicht autorisierter Mbox-Host */ zurück.**

If a [!DNL Target] request is made on an unauthorized host, the request will respond with /* no display - unauthorized mbox host */.
