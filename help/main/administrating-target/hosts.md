---
keywords: Host;Hosts;Hostgruppe;Fehlerbehebung;Best Practices;ubox;Umleitungen;Umleitung;Whitelist;Zulassungsliste;Blacklist;Blockierungsliste
description: Erfahren Sie, wie Sie Ihre Websites und Vorproduktionsumgebungen organisieren, um die Verwaltung und das separate Reporting in Adobe Target zu erleichtern.
title: Was sind Hosts und wie verwende ich sie?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: 12831d6584acc482db415629d7e70a18e39c47c2
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 17%

---

# Hosts

Organisieren Sie Ihre Sites und Vorproduktionsumgebungen für einfaches Management und separates Reporting in [!DNL Adobe Target].

Das Hauptziel bei der Hostverwaltung besteht darin, dafür zu sorgen, dass auf der Seite nicht versehentlich inaktive Inhalte erscheinen. Die Hostverwaltung ermöglicht auch die Trennung von Berichtsdaten nach [Umgebung](/help/main/administrating-target/environments.md).

Ein Host ist jede Domain, von der eine [!DNL Target]-Anfrage gesendet wird. Auf einer Website ist dies normalerweise die `location.hostname` Eigenschaft der URL, die die [!DNL Target] anfordert.

Standardmäßig beschränkt [!DNL Target] keinen Host, der [!DNL Target] Anfragen stellen und [!DNL Target] Antworten empfangen kann. Wenn neue Hosts Anfragen stellen, funktionieren sie automatisch. Dieser Prozess ermöglicht auch Tests in verschiedenen Domains, die Sie nicht kennen oder nicht vorhersehen können. Wenn Sie dieses Standardverhalten überschreiben möchten, können Sie eine oder eine -Zulassungsliste auf die Blockierungsliste setzte einrichten, um zu begrenzen, welche Hosts mit [!DNL Target] funktionieren.

{{permissions-update}}

Um Hosts zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

## Erkennen von Hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Um einen Host zu erkennen und ihn der [!UICONTROL Hosts] Liste hinzuzufügen, müssen die folgenden Bedingungen erfüllt sein:

* Auf dem Host muss mindestens eine [!DNL Target] vorhanden sein
* Eine Seite auf dem Host muss Folgendes enthalten:

   * Eine genaue at.js-Referenz
   * Eine [!DNL Target] Anfrage oder eine automatisch generierte globale [!DNL Target]

* Die Seite mit der [!DNL Target] muss in einem Browser angezeigt werden

Nachdem die Seite angezeigt wurde, wird der Host in der Liste [!UICONTROL Hosts] aufgeführt, sodass Sie ihn in einer Umgebung verwalten und Aktivitäten und Tests in der Vorschau anzeigen und starten können.

>[!NOTE]
>
>Dies umfasst sämtliche persönlichen Entwicklungsserver.

Nachdem ein Host zur [!UICONTROL Host] hinzugefügt wurde, stellen Sie sicher, dass der Host erkannt wird.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Wird der Host nicht angezeigt, aktualisieren Sie den Browser.

   Standardmäßig wird ein neu erkannter Host in der [!UICONTROL Production] platziert. Die [!UICONTROL Production] Umgebung ist die sicherste Umgebung, da sie das Anzeigen inaktiver Aktivitäten von diesen Hosts nicht zulässt.

1. (Bedingt) Klicken Sie auf das **[!UICONTROL Move]** ( ![move icon](/help/main/administrating-target/assets/icon-move.png) ), um den Host in die [!UICONTROL Development], [!UICONTROL Staging] oder eine andere Umgebung zu verschieben.

>[!NOTE]
>
>Die [!UICONTROL Production] Umgebung kann nicht gelöscht werden, selbst wenn Sie sie umbenennen. Es wird davon ausgegangen, dass in dieser Umgebung die endgültigen, aktiven Aktivitäten und Tests durchgeführt werden. In der Standardumgebung ist es nicht zulässig, inaktive Kampagnen anzuzeigen.

## Sortieren oder Durchsuchen der Hosts-Liste {#section_068B23C9D8224EB78BC3B7C8580251B0}

Um die [!UICONTROL Hosts] Liste zu sortieren, klicken Sie auf eine beliebige Spaltenüberschrift ([!UICONTROL Name], [!UICONTROL Environment] oder [!UICONTROL Last Requested]), um die Liste in auf- oder absteigender Reihenfolge zu sortieren.

Um die [!UICONTROL Hosts] zu durchsuchen, geben Sie einen Suchbegriff in das [!UICONTROL Search Hosts] ein.

## Erstellen Sie Zulassungslisten, die Hosts angeben, die autorisiert sind, [!DNL Target] Anfragen an [!DNL Target] zu senden. {#allowlist}

Sie können eine -Zulassungsliste erstellen, die Hosts (Domains) angibt, die autorisiert sind, [!DNL Target]-Anfragen an [!DNL Target] zu senden. Alle anderen Hosts, die Anfragen generieren, erhalten eine auskommentierte Autorisierungsfehlerantwort. Standardmäßig registriert sich jeder Host mit einer [!DNL Target]-Anfrage bei [!DNL Target] in der [!UICONTROL Production]-Umgebung und hat Zugriff auf alle aktiven und genehmigten Aktivitäten. Wenn dieser Ansatz nicht erwünscht ist, können Sie stattdessen die Zulassungsliste verwenden, um bestimmte Hosts aufzuzeichnen, die für [!DNL Target]-Anfragen und den Empfang [!DNL Target] Inhalte geeignet sind. Alle Hosts werden weiterhin in der [!UICONTROL Hosts] angezeigt, und Umgebungen können weiterhin verwendet werden, um diese Hosts zu gruppieren und jedem verschiedene Ebenen zuzuweisen, z. B. ob der Host aktive und/oder inaktive Aktivitäten sehen kann.

So erstellen Sie eine Zulassungsliste:

1. Klicken Sie in der [!UICONTROL Hosts] auf **[!UICONTROL Authorize Hosts]**.
1. Aktivieren Sie den Umschalter **[!UICONTROL Enable Authorized Hosts for content delivery]** .
1. Fügen Sie die gewünschten Hosts nach Bedarf in das **[!UICONTROL Host contains]** ein.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Fügen Sie die gewünschten Hosts nach Bedarf in das **[!UICONTROL Host does not contains]** ein.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Klicken Sie auf **[!UICONTROL Save]**.

Wenn eine [!DNL Target]-Anfrage auf einem nicht autorisierten Host erfolgt, antwortet der Aufruf mit `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best Practices für die Sicherheit**: Wenn Sie die ubox-Funktion von [!DNL Target] verwenden, steuert diese Zulassungsliste auch die Liste der Domains, zu denen Ihre [Weiterleitungen](https://experienceleague.adobe.com/docs/target-dev/developer/implement-email/working-with-redirectors.html?lang=de){target=_blank} navigieren können. Stellen Sie sicher, dass Sie alle Domains hinzufügen, zu denen Sie umleiten möchten, wenn Sie ubox als Teil Ihrer Implementierung verwenden. Wenn die Zulassungsliste nicht angegeben ist, können [!DNL Adobe] die Umleitungs-URLs nicht überprüfen und vor potenziellen bösartigen Umleitungen schützen.
>
>Die Zulassungsliste hat Vorrang vor Umgebungen. Löschen Sie alle Hosts, bevor Sie die Funktion Zulassungsliste verwenden, dann werden nur die von der Zulassungsliste zugelassenen Hosts in Ihrer Hosts-Liste angezeigt. Anschließend können Sie die Hosts in die gewünschten Umgebungen verschieben.

Manchmal erscheinen Hosts anderer Sites in Ihren Umgebungen. Eine Domain wird in der Liste angezeigt, wenn die Domain at.js aufruft. Wenn beispielsweise eine Ihrer Webseiten auf den Server eines anderen kopiert wird, wird diese Domain in Ihrer Umgebung angezeigt. Es können auch Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt werden.

In Fällen, in denen `mboxHost` an einen API-Aufruf weitergegeben wird, wird die Konversion für die weitergegebene Umgebung aufgezeichnet. Wenn keine Umgebung übergeben wird, wird der Host im Aufruf standardmäßig auf [!UICONTROL Production] gesetzt.

Sie können auch eine -Blockierungsliste erstellen, die Hosts (Domains) angibt, die keine [!DNL Target]-Anfragen an [!DNL Target] senden können, indem Sie die gewünschten Hosts in das [!UICONTROL Host Does Not Contain] Feld einfügen.

>[!NOTE]
>
>Die [!UICONTROL Authorized Hosts] Liste wird sowohl für [!DNL Target] Hosts als auch für Standard-Umleitungs-Hosts verwendet. Fügen Sie alle vorhandenen Domains hinzu, die für die Verwendung der [!DNL Adobe Target] JavaScript SDK (at.js) genehmigt wurden *UND* alle Domains, die in den standardmäßigen Weiterleitungs-URLs des Posteingangs verwendet werden. Fügen Sie der Zulassungsliste in Zukunft alle neuen ähnlichen Domains hinzu.

## Löschen eines Hosts {#section_F56355BA4BC54B078A1A8179BC954632}

Sie können einen Host, der nicht mehr gebraucht wird, löschen.

1. Klicken Sie in der [!UICONTROL Hosts] auf das Symbol **[!UICONTROL Delete]** .
1. Klicken Sie auf **[!UICONTROL Delete]** , um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Der Host wird erneut aufgeführt, wenn jemand zu einer Seite navigiert, die eine [!DNL Target] auf dem Host enthält.

## Fehlerbehebung für Hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probieren Sie folgende Methoden zur Fehlerbehebung aus, falls Probleme mit Ihren Hosts auftreten:

**Host wird für Ihr Konto nicht in der Liste angezeigt.**

* Aktualisieren Sie die [!UICONTROL Hosts] Seite in Ihrem Browser.
* Vergewissern Sie sich, dass die [!DNL Target]-Anfrage korrekt ist, einschließlich der at.js-Referenz.
* Versuchen Sie, zu einer der [!DNL Target] Anfragen auf dem Host zu navigieren. Es ist möglich, dass nie eine [!DNL Target] auf dem Host in einem Browser gerendert wurde.

**Zufällige oder unbekannte Domains werden in der [!UICONTROL Host] angezeigt.**

Eine Domain wird in der Liste angezeigt, wenn von der Domain eine Anfrage an [!DNL Target] gestellt wurde. Häufig werden Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt. Wenn die aufgelistete Domain nicht von Ihrem Team verwendet wird, können Sie auf [!UICONTROL Delete] klicken, um sie zu entfernen.

**Meine [!DNL Target]-Anfrage gibt &quot;/&#42;&quot; ohne Anzeige zurück - Nicht autorisierter Mbox-Host &#42;/.**

Wenn eine [!DNL Target]-Anfrage auf einem nicht autorisierten Host durchgeführt wird, antwortet die Anfrage mit /&#42; Keine Anzeige - Nicht autorisierter mbox-Host &#42;/.
