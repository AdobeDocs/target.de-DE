---
keywords: Host;Hosts;Hostgruppe;Fehlerbehebung;Best Practices;Ubox;Umleitungen;Umleitung;Whitelist;Zulassungsliste;Blacklist;Blockierungsliste
description: Erfahren Sie, wie Sie Ihre Websites und Umgebung vor der Produktion für eine einfache Verwaltung und getrennten Berichte in Adobe Target organisieren.
title: Was sind Hosts und wie verwende ich sie?
feature: Administration & Configuration
role: Administrator
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Hosts{#hosts}

Organisieren Sie Ihre Sites und Umgebung vor der Produktion für einfache Verwaltung und separaten Berichte in [!DNL Adobe Target].

Das Hauptziel bei der Hostverwaltung besteht darin, dafür zu sorgen, dass auf der Seite nicht versehentlich inaktive Inhalte erscheinen. Mit der Hostverwaltung können Sie Berichtsdaten auch nach [Umgebung](/help/administrating-target/environments.md) trennen.

Ein Host ist eine Domäne, von der aus eine [!DNL Target]-Anforderung ausgeführt wird. Auf einer Website ist es normalerweise die `location.hostname`-Eigenschaft der URL, die die [!DNL Target]-Anforderung ausführt.

Standardmäßig beschränkt [!DNL Target] keinen Host, der [!DNL Target]-Anforderungen stellen und [!DNL Target]-Antworten empfangen kann. Wenn neue Hosts Anforderungen stellen, funktionieren diese automatisch. Dies ermöglicht auch Tests auf verschiedenen Domänen, die Sie nicht kennen oder nicht vorhersehen können. Wenn Sie dieses Standardverhalten überschreiben möchten, können Sie eine Zulassungsliste oder Blockierungsliste einrichten, um zu begrenzen, welche Hosts mit [!DNL Target] funktionieren.

Um Hosts zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Erkennen von Hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Um einen Host zu erkennen und ihn der Liste [!UICONTROL Hosts] hinzuzufügen, müssen die folgenden Bedingungen erfüllt sein:

* Mindestens eine [!DNL Target]-Anforderung muss auf dem Host vorhanden sein
* Eine Seite auf dem Host muss  Folgendes aufweisen:

   * Ein genauer &quot;at.js&quot;- oder &quot;mbox.js&quot;-Verweis
   * Eine [!DNL Target]-Anforderung oder eine automatisch generierte globale [!DNL Target]-Anforderung

* Die Seite mit der [!DNL Target]-Anforderung muss in einem Browser angezeigt werden

Nach der Anzeige der Seite wird der Host in der Liste [!UICONTROL Hosts] aufgelistet, sodass Sie ihn in einer Umgebung verwalten sowie Aktivitäten und Tests für die Vorschau und den Start starten können.

>[!NOTE]
>
>Dies umfasst sämtliche persönlichen Entwicklungsserver.

Stellen Sie nach dem Hinzufügen eines Hosts zur [!UICONTROL Hostgruppenliste] sicher, dass der Host erkannt wird.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Wird der Host nicht angezeigt, aktualisieren Sie den Browser. 


   Standardmäßig wird ein neu erkannter Host in der Umgebung [!UICONTROL Produktion] platziert. Diese Umgebung ist am sichersten, da es in ihr nicht zulässig ist, inaktive Aktivitäten über diese Hosts anzuzeigen.

1. (Bedingt) Klicken Sie auf das Symbol **[!UICONTROL Verschieben]** ( ![Verschieben-Symbol](/help/administrating-target/assets/icon-move.png) ), um den Host in die Umgebung [!UICONTROL Entwicklung], [!UICONTROL Staging] oder eine andere zu verschieben.

>[!NOTE]
>
>Die Umgebung [!UICONTROL Produktion] kann nicht gelöscht werden, auch wenn Sie sie umbenennen. Es wird angenommen, dass in dieser Gruppe fertiggestellte, aktive Aktivitäten und Tests bereitgestellt werden. In der Standardumgebung ist es nicht zulässig, inaktive Kampagnen anzuzeigen.

## Sortieren oder suchen Sie nach der Hostgruppen-Liste {#section_068B23C9D8224EB78BC3B7C8580251B0}

Um die Liste [!UICONTROL Hosts] zu sortieren, klicken Sie auf eine Spaltenüberschrift ([!UICONTROL Name], [!UICONTROL Umgebung] oder [!UICONTROL Zuletzt angefordert]), um die Liste in auf- oder absteigender Reihenfolge zu sortieren.

Um die Liste [!UICONTROL Hosts] zu durchsuchen, geben Sie einen Suchbegriff in das Feld [!UICONTROL Search Hosts] ein.

## Erstellen Sie Zulassungslisten, die Hosts angeben, die berechtigt sind, Zielgruppen an die Zielgruppe zu senden. {#allowlist}

Sie können eine Zulassungsliste erstellen, die Hosts (Domänen) angibt, die berechtigt sind, [!DNL Target]-Anforderungen an [!DNL Target] zu senden. Alle anderen Hosts, die Anforderungen generieren, erhalten eine kommentierte Fehlermeldung zur Autorisierung. Standardmäßig werden alle Hosts, die eine [!DNL Target]-Anforderung enthalten, mit [!DNL Target] in der [!UICONTROL Production]-Umgebung registriert und haben Zugriff auf alle aktiven und genehmigten Aktivitäten. Wenn dies nicht gewünscht wird, können Sie stattdessen mithilfe der Zulassungsliste bestimmte Hosts aufzeichnen, die berechtigt sind, [!DNL Target]-Anforderungen zu stellen und [!DNL Target]-Inhalte zu empfangen. Alle Hosts werden weiterhin in der Liste [!UICONTROL Hosts] angezeigt, und Umgebung können weiterhin verwendet werden, um diese Hosts zu gruppieren und ihnen verschiedene Ebenen zuzuweisen, z. B. ob der Host aktive und/oder inaktive Aktivitäten sehen kann.

So erstellen Sie eine Zulassungsliste:

1. Klicken Sie in der Liste [!UICONTROL Hosts] auf **[!UICONTROL Hosts autorisieren]**.
1. Aktivieren Sie den Umschalter **[!UICONTROL Autorisierte Hosts für Content Versand]** aktivieren.
1. hinzufügen Sie die gewünschten Hosts im Feld **[!UICONTROL Host enthält]**.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. hinzufügen die gewünschten Hosts im Feld **[!UICONTROL Host enthält nicht]**, wie gewünscht.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn eine [!DNL Target]-Anforderung auf einem nicht autorisierten Host erfolgt, antwortet der Aufruf mit `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best Practices** für Sicherheit: Wenn Sie die Ubox-Funktion von verwenden,  [!DNL Target]beachten Sie, dass diese Zulassungsliste auch die Liste der Domänen steuert, zu denen die  [](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) Umleitung navigiert. Stellen Sie sicher, dass Sie alle Domänen hinzufügen, denen Sie umleiten möchten, wenn Sie Ubox als Teil Ihrer Implementierung verwenden. Wenn die Zulassungsliste nicht angegeben ist, kann [!DNL Adobe] die Umleitungs-URLs nicht überprüfen und vor möglichen bösartigen Umleitungen schützen.
>
>Die Zulassungsliste hat Vorrang vor Umgebung. Sie sollten alle Hosts löschen, bevor Sie die Funktion &quot;Zulassungsliste&quot;verwenden. Dann werden nur die Hosts angezeigt, die von der Zulassungsliste zugelassen sind. Anschließend können Sie die Hosts in die gewünschten Umgebungen verschieben.

Manchmal erscheinen Hosts anderer Sites in Ihren Umgebungen. Eine Domäne wird in der Liste angezeigt, wenn die Domäne Ihre &quot;at.js&quot;oder &quot;mbox.js&quot;aufruft. Wenn beispielsweise eine Ihrer Webseiten auf den Server eines anderen kopiert wird, wird diese Domäne in Ihrer Umgebung angezeigt. Es können auch Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt werden.

In Fällen, in denen `mboxHost` an einen API-Aufruf weitergegeben wird, wird die Konversion für die weitergegebene Umgebung aufgezeichnet. Wenn keine Umgebung übergeben wird, ist der Host im Aufruf standardmäßig [!UICONTROL Produktion].

Sie können auch eine Blockierungsliste erstellen, die Hosts (Domänen) angibt, die keine [!DNL Target]-Anforderungen an [!DNL Target] senden können, indem Sie die gewünschten Hosts im Feld [!UICONTROL Host enthält nicht] hinzufügen.

>[!NOTE]
>
>Da die Liste für autorisierte Hosts sowohl für [!DNL Target]-Hosts als auch für standardmäßige Umleitungs-Hosts verwendet wird, müssen Sie alle vorhandenen Domänen hinzufügen, die für die Verwendung des [!DNL Adobe Target]-JavaScript-SDK (at.js) *AND* für alle Domänen, die in den Standard-Umleitungs-URLs von ubox verwendet werden, zugelassen sind. Sie müssen der Zulassungsliste in Zukunft auch alle neuen ähnlichen Domänen hinzufügen.

## Einen Host {#section_F56355BA4BC54B078A1A8179BC954632} löschen

Sie können einen Host, der nicht mehr gebraucht wird, löschen.

1. Klicken Sie in der Liste [!UICONTROL Hosts] auf das Symbol **[!UICONTROL Löschen]**.
1. Klicken Sie auf **[!UICONTROL Löschen]**, um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Der Host wird erneut aufgelistet, wenn jemand zu einer Seite navigiert, die eine [!DNL Target]-Anforderung auf dem Host enthält.

## Fehlerbehebung für Hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probieren Sie folgende Methoden zur Fehlerbehebung aus, falls Probleme mit Ihren Hosts auftreten:

**Der Host wird nicht in der Liste für Ihr Konto angezeigt.**

* Aktualisieren Sie die Seite [!UICONTROL Hosts] Ihres Browsers.
* Vergewissern Sie sich, dass die [!DNL Target]-Anforderung korrekt ist, einschließlich des Verweises &quot;at.js&quot;oder &quot;mbox.js&quot;.
* Suchen Sie nach einer der [!DNL Target]-Anforderungen auf dem Host. Es ist möglich, dass keine [!DNL Target] Anforderung auf dem Host jemals in einem Browser gerendert wurde.

**In der [!UICONTROL Hostgruppenliste] werden zufällige oder unbekannte Domänen angezeigt.**

Eine Domäne wird in dieser Liste angezeigt, wenn eine Anforderung an [!DNL Target] aus der Domäne erfolgt. Häufig werden Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt. Wenn eine aufgeführte Domäne von Ihrem Team nicht verwendet wird, können Sie auf [!UICONTROL Löschen] klicken, um sie zu entfernen.

**Meine  [!DNL Target] Anfrage gibt /* keine Anzeige - nicht autorisierter Mbox-Host */ zurück.**

Wenn eine [!DNL Target]-Anforderung auf einem nicht autorisierten Host erfolgt, antwortet die Anfrage mit /* Keine Anzeige - nicht autorisierter Mbox-Host */.
