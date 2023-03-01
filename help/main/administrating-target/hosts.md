---
keywords: Host; Hosts; Hostgruppe; Fehlerbehebung; Best Practices; Ubox; Umleitungen; Weiterleiten; Whitelist; Zulassungsliste; Blacklist; Blockierungsliste
description: Erfahren Sie, wie Sie Ihre Websites und Umgebungen vor der Produktion organisieren, um die Verwaltung und die separate Berichterstellung in Adobe Target zu erleichtern.
title: Was sind Hosts und wie verwende ich sie?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 22%

---

# Hosts

Organisieren Sie Ihre Sites und Umgebungen vor der Produktion für einfache Verwaltung und separate Berichterstattung in [!DNL Adobe Target].

Das Hauptziel bei der Hostverwaltung besteht darin, dafür zu sorgen, dass auf der Seite nicht versehentlich inaktive Inhalte erscheinen. Mit der Hostverwaltung können Berichtsdaten auch nach [Umgebung](/help/main/administrating-target/environments.md).

Ein Host ist eine beliebige Domäne, von der aus ein [!DNL Target] -Anfrage ausgeführt wird. Auf einer Website ist es normalerweise der `location.hostname` -Eigenschaft der URL, die die [!DNL Target] -Anfrage.

Standardmäßig [!DNL Target] beschränkt keine Hosts, die [!DNL Target] Anfragen und empfangen [!DNL Target] Antworten. Wenn neue Hosts Anfragen stellen, funktionieren sie automatisch. Dieser Prozess ermöglicht auch Tests auf verschiedenen Domänen, die Sie nicht kennen oder nicht vorhersehen können. Wenn Sie dieses Standardverhalten überschreiben möchten, können Sie eine Zulassungsliste oder eine Blockierungsliste einrichten, um zu begrenzen, mit welchen Hosts gearbeitet wird [!DNL Target].

Um Hosts zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![hosts_list-Bild](assets/hosts_list.png)

## Erkennen von Hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

So erkennen Sie einen Host und fügen ihn zum [!UICONTROL Hosts] auflisten, müssen folgende Bedingungen erfüllt sein:

* Mindestens ein [!DNL Target] -Anfrage muss auf dem Host vorhanden sein
* Eine Seite auf dem Host muss  Folgendes aufweisen:

   * einen genauen at.js-Verweis
   * A [!DNL Target] -Anfrage oder einer automatisch generierten globalen [!DNL Target] Anfrage

* Die Seite mit der [!DNL Target] -Anfrage muss in einem Browser angezeigt werden

Nachdem die Seite angezeigt wurde, wird der Host im [!UICONTROL Hosts] -Liste, mit der Sie sie in einer Umgebung verwalten und eine Vorschau der Aktivitäten und Tests anzeigen und starten können.

>[!NOTE]
>
>Dies umfasst sämtliche persönlichen Entwicklungsserver.

Stellen Sie nach dem Hinzufügen eines Hosts zur [!UICONTROL Hostgruppenliste] sicher, dass der Host erkannt wird.

1. Klicken **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Wird der Host nicht angezeigt, aktualisieren Sie den Browser. 


   Standardmäßig wird ein neu erkannter Host im [!UICONTROL Produktion] Umgebung. Die [!UICONTROL Produktion] ist die sicherste Umgebung, da es nicht möglich ist, inaktive Aktivitäten von diesen Hosts aus anzuzeigen.

1. (Bedingt) Klicken Sie auf die **[!UICONTROL Verschieben]** Symbol ( ![Verschiebe-Symbol](/help/main/administrating-target/assets/icon-move.png) ), um den Host in die [!UICONTROL Entwicklung], [!UICONTROL Staging]oder einer anderen Umgebung.

>[!NOTE]
>
>Die [!UICONTROL Produktion] -Umgebung kann nicht gelöscht werden, selbst wenn sie umbenannt wird. Es wird davon ausgegangen, dass in dieser Umgebung fertig gestellte, aktive Aktivitäten und Tests bereitgestellt werden. In der Standardumgebung ist es nicht zulässig, inaktive Kampagnen anzuzeigen.

## Sortieren oder Durchsuchen der Hostgruppenliste {#section_068B23C9D8224EB78BC3B7C8580251B0}

So sortieren Sie die [!UICONTROL Hosts] auf eine beliebige Spaltenüberschrift ([!UICONTROL Name], [!UICONTROL Umgebung]oder [!UICONTROL Zuletzt angefordert]), um die Liste in auf- oder absteigender Reihenfolge zu sortieren.

So durchsuchen Sie die [!UICONTROL Hosts] Liste, geben Sie einen Suchbegriff in die [!UICONTROL Hosts suchen] ankreuzen.

## Erstellen von Zulassungslisten, die Hosts spezifizieren, die zum Senden berechtigt sind [!DNL Target] Anforderungen an [!DNL Target]. {#allowlist}

Sie können eine Zulassungsliste erstellen, die Hosts (Domänen) angibt, die zum Senden berechtigt sind [!DNL Target] Anforderungen an [!DNL Target]. Alle anderen Hosts, die Anforderungen generieren, erhalten eine kommentierte Fehlerantwort mit einem Autorisierungsfehler. Standardmäßig ist jeder Host, der eine [!DNL Target] Anforderungsregister mit [!DNL Target] im [!UICONTROL Produktion] und hat Zugriff auf alle aktiven und genehmigten Aktivitäten. Wenn dieser Ansatz nicht gewünscht wird, können Sie stattdessen die Zulassungsliste verwenden, um bestimmte Hosts aufzuzeichnen, die zum Erstellen von [!DNL Target] Anfragen und empfangen [!DNL Target] Inhalt. Alle Hosts werden weiterhin im [!UICONTROL Hosts] -Liste und -Umgebungen können weiterhin verwendet werden, um diese Hosts zu gruppieren und ihnen unterschiedliche Ebenen zuzuweisen, z. B. ob der Host aktive und/oder inaktive Aktivitäten sehen kann.

So erstellen Sie eine Zulassungsliste:

1. Aus dem [!UICONTROL Hosts] Liste, klicken Sie auf **[!UICONTROL Hosts zulassen]**.
1. Aktivieren Sie die **[!UICONTROL Zulässige Hosts für die Inhaltsbereitstellung aktivieren]** umschalten.
1. Fügen Sie die gewünschten Hosts im **[!UICONTROL Host enthält]** nach Bedarf.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Fügen Sie die gewünschten Hosts im **[!UICONTROL Host enthält nicht]** nach Bedarf.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn eine [!DNL Target] -Anfrage auf einem nicht autorisierten Host erfolgt, antwortet der -Aufruf mit `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best Practices für die Sicherheit**: Wenn Sie die Ubox-Funktion von [!DNL Target], steuert diese Zulassungsliste auch die Liste der Domänen, auf die Ihre [Weiterleitungen](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implement-email/working-with-redirectors.html){target=_blank} kann navigieren. Stellen Sie sicher, dass Sie alle Domänen hinzufügen, zu denen Sie umleiten möchten, wenn Sie &quot;ubox&quot;als Teil Ihrer Implementierung verwenden. Wenn die Zulassungsliste nicht angegeben wird, [!DNL Adobe] ist nicht in der Lage, die Umleitungs-URLs zu überprüfen und vor potenziellen schädlichen Umleitungen zu schützen.
>
>Die Zulassungsliste hat Vorrang vor Umgebungen. Löschen Sie alle Hosts, bevor Sie die Funktion &quot;Zulassungsliste&quot;verwenden, und dann werden nur die von der Zulassungsliste zugelassenen Hosts in Ihrer Hostliste angezeigt. Anschließend können Sie die Hosts in die gewünschten Umgebungen verschieben.

Manchmal erscheinen Hosts anderer Sites in Ihren Umgebungen. Eine Domäne wird in der Liste angezeigt, wenn die Domäne at.js aufruft. Wenn beispielsweise eine Ihrer Webseiten auf den Server eines anderen kopiert wird, wird diese Domain in Ihrer Umgebung angezeigt. Es können auch Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt werden.

In Fällen, in denen `mboxHost` an einen API-Aufruf weitergegeben wird, wird die Konversion für die weitergegebene Umgebung aufgezeichnet. Wenn keine Umgebung übergeben wird, wird der Host im -Aufruf standardmäßig auf [!UICONTROL Produktion].

Sie können auch eine Blockierungsliste erstellen, die Hosts (Domänen) angibt, die nicht gesendet werden können [!DNL Target] Anforderungen an [!DNL Target] durch Hinzufügen der gewünschten Hosts in der [!UICONTROL Host enthält nicht] ankreuzen.

>[!NOTE]
>
>Die [!UICONTROL Autorisierte Hosts] list wird für beide [!DNL Target] Hosts und standardmäßige Umleitungs-Hosts. Fügen Sie alle vorhandenen Domänen hinzu, die für die Verwendung der [!DNL Adobe Target] JavaScript-SDK (at.js) *UND* alle Domänen, die in Standard-Umleitungs-URLs der Posteingang verwendet werden. Fügen Sie der Zulassungsliste in Zukunft alle neuen ähnlichen Domänen hinzu.

## Löschen eines Hosts {#section_F56355BA4BC54B078A1A8179BC954632}

Sie können einen Host, der nicht mehr gebraucht wird, löschen.

1. Aus dem [!UICONTROL Hosts] Liste, klicken Sie auf die **[!UICONTROL Löschen]** Symbol.
1. Klicken Sie auf **[!UICONTROL Löschen]**, um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Der Host wird erneut aufgeführt, wenn jemand zu einer Seite navigiert, die eine [!DNL Target] Anfrage auf dem Host.

## Fehlerbehebung für Hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probieren Sie folgende Methoden zur Fehlerbehebung aus, falls Probleme mit Ihren Hosts auftreten:

**Der Host wird nicht in der Liste für Ihr Konto angezeigt.**

* Aktualisieren Sie die Seite [!UICONTROL Hosts] Ihres Browsers.
* Vergewissern Sie sich, dass die [!DNL Target] -Anfrage korrekt ist, einschließlich der at.js-Referenz.
* Versuchen Sie, zu einem der [!DNL Target] -Anfragen auf dem Host. Es ist möglich, dass [!DNL Target] -Anfrage auf dem Host wurde jemals in einem Browser gerendert.

**In der [!UICONTROL Hostgruppenliste] werden zufällige oder unbekannte Domänen angezeigt.**

Eine Domäne wird in dieser Liste angezeigt, wenn eine Anforderung an [!DNL Target] wird aus der Domäne erstellt. Häufig werden Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt. Wenn eine aufgeführte Domain von Ihrem Team nicht verwendet wird, können Sie auf [!UICONTROL Löschen] klicken, um sie zu entfernen.

**My [!DNL Target] Anfrage gibt zurück /&#42; Keine Anzeige - nicht autorisierter Mbox-Host &#42;/.**

Wenn eine [!DNL Target] Anfrage wird auf einem nicht autorisierten Host durchgeführt. Die Anfrage antwortet mit /&#42; Keine Anzeige - nicht autorisierter Mbox-Host &#42;/.
