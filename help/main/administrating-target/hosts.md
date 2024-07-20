---
keywords: Host; Hosts; Hostgruppe; Fehlerbehebung; Best Practices; Ubox; Umleitungen; Weiterleiten; Whitelist; Zulassungsliste; Blacklist; Blockierungsliste
description: Erfahren Sie, wie Sie Ihre Websites und Umgebungen vor der Produktion organisieren, um die Verwaltung und die separate Berichterstellung in Adobe Target zu erleichtern.
title: Was sind Hosts und wie verwende ich sie?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 17%

---

# Hosts

Organisieren Sie Ihre Sites und Umgebungen vor der Produktion für einfache Verwaltung und separate Berichterstellung in [!DNL Adobe Target].

Das Hauptziel bei der Hostverwaltung besteht darin, dafür zu sorgen, dass auf der Seite nicht versehentlich inaktive Inhalte erscheinen. Mit der Hostverwaltung können Sie Berichtsdaten auch nach [Umgebung](/help/main/administrating-target/environments.md) trennen.

Ein Host ist eine beliebige Domäne, von der aus eine [!DNL Target] -Anfrage ausgeführt wird. Auf einer Website ist es normalerweise die `location.hostname` -Eigenschaft der URL, die die [!DNL Target] -Anfrage ausführt.

Standardmäßig begrenzt [!DNL Target] einen Host nicht, der [!DNL Target] -Anfragen stellen und [!DNL Target] -Antworten empfangen kann. Wenn neue Hosts Anfragen stellen, funktionieren sie automatisch. Dieser Prozess ermöglicht auch Tests auf verschiedenen Domänen, die Sie nicht kennen oder nicht vorhersehen können. Wenn Sie dieses Standardverhalten überschreiben möchten, können Sie eine Zulassungsliste oder eine Blockierungsliste einrichten, um zu begrenzen, welche Hosts mit [!DNL Target] funktionieren.

Um Hosts zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![hosts_list image](assets/hosts_list.png)

## Erkennen von Hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Um einen Host zu erkennen und ihn der Liste [!UICONTROL Hosts] hinzuzufügen, müssen die folgenden Bedingungen erfüllt sein:

* Mindestens eine [!DNL Target] -Anfrage muss auf dem Host vorhanden sein
* Eine Seite auf dem Host muss Folgendes aufweisen:

   * einen genauen at.js-Verweis
   * Eine [!DNL Target] -Anfrage oder eine automatisch generierte globale [!DNL Target] -Anfrage

* Die Seite mit der [!DNL Target] -Anforderung muss in einem Browser angezeigt werden

Nachdem die Seite angezeigt wurde, wird der Host in der Liste [!UICONTROL Hosts] aufgelistet, sodass Sie ihn in einer Umgebung verwalten sowie Aktivitäten und Tests in der Vorschau anzeigen und starten können.

>[!NOTE]
>
>Dies umfasst sämtliche persönlichen Entwicklungsserver.

Nachdem ein Host zur Liste [!UICONTROL Host] hinzugefügt wurde, stellen Sie sicher, dass der Host erkannt wird.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Wird der Host nicht angezeigt, aktualisieren Sie den Browser.

   Standardmäßig wird ein neu erkannter Host in der Umgebung [!UICONTROL Production] platziert. Die Umgebung &quot;[!UICONTROL Production]&quot; ist die sicherste, da es nicht möglich ist, inaktive Aktivitäten von diesen Hosts aus anzuzeigen.

1. (Bedingt) Klicken Sie auf das Symbol **[!UICONTROL Move]** ( ![Verschiebungssymbol](/help/main/administrating-target/assets/icon-move.png) ), um den Host in die Umgebung [!UICONTROL Development], [!UICONTROL Staging] oder eine andere zu verschieben.

>[!NOTE]
>
>Die Umgebung [!UICONTROL Production] kann nicht gelöscht werden, selbst wenn sie umbenannt wird. Es wird davon ausgegangen, dass in dieser Umgebung fertig gestellte, aktive Aktivitäten und Tests bereitgestellt werden. In der Standardumgebung ist es nicht zulässig, inaktive Kampagnen anzuzeigen.

## Sortieren oder Durchsuchen der Hostgruppenliste {#section_068B23C9D8224EB78BC3B7C8580251B0}

Um die Liste [!UICONTROL Hosts] zu sortieren, klicken Sie auf eine beliebige Spaltenüberschrift ([!UICONTROL Name], [!UICONTROL Environment] oder [!UICONTROL Last Requested]), um die Liste in auf- oder absteigender Reihenfolge zu sortieren.

Um die Liste [!UICONTROL Hosts] zu durchsuchen, geben Sie einen Suchbegriff in das Feld [!UICONTROL Search Hosts] ein.

## Erstellen Sie Zulassungslisten, die Hosts angeben, die berechtigt sind, [!DNL Target] -Anfragen an [!DNL Target] {#allowlist} zu senden.

Sie können eine Zulassungsliste erstellen, die Hosts (Domänen) angibt, die berechtigt sind, [!DNL Target] -Anfragen an [!DNL Target] zu senden. Alle anderen Hosts, die Anforderungen generieren, erhalten eine kommentierte Fehlerantwort mit einem Autorisierungsfehler. Hosts, die eine [!DNL Target] -Anfrage enthalten, werden standardmäßig bei [!DNL Target] in der [!UICONTROL Production] -Umgebung registriert und erhalten Zugriff auf alle aktiven und genehmigten Aktivitäten. Wenn dieser Ansatz nicht gewünscht wird, können Sie stattdessen die Zulassungsliste verwenden, um bestimmte Hosts aufzuzeichnen, die berechtigt sind, [!DNL Target] -Anforderungen zu stellen und [!DNL Target] -Inhalte zu empfangen. Alle Hosts werden weiterhin in der Liste [!UICONTROL Hosts] angezeigt und Umgebungen können weiterhin verwendet werden, um diese Hosts zu gruppieren und ihnen verschiedene Ebenen zuzuweisen, z. B. ob der Host aktive und/oder inaktive Aktivitäten sehen kann.

So erstellen Sie eine Zulassungsliste:

1. Klicken Sie in der Liste [!UICONTROL Hosts] auf **[!UICONTROL Authorize Hosts]**.
1. Aktivieren Sie den Umschalter **[!UICONTROL Enable Authorized Hosts for content delivery]** .
1. Fügen Sie die gewünschten Hosts nach Bedarf im Feld **[!UICONTROL Host contains]** hinzu.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Fügen Sie die gewünschten Hosts nach Bedarf im Feld **[!UICONTROL Host does not contains]** hinzu.

   Es können mehrere Hosts, einer pro Zeile, aufgeführt sein.

1. Klicken Sie auf **[!UICONTROL Save]**.

Wenn eine [!DNL Target] -Anfrage auf einem nicht autorisierten Host erfolgt, antwortet der Aufruf mit `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best Practices für die Sicherheit**: Wenn Sie die Ubox-Funktion von [!DNL Target] verwenden, steuert diese Zulassungsliste auch die Liste der Domänen, zu denen Ihre [Weiterleitungen](https://experienceleague.adobe.com/docs/target-dev/developer/implement-email/working-with-redirectors.html){target=_blank} navigieren können. Stellen Sie sicher, dass Sie alle Domänen hinzufügen, zu denen Sie umleiten möchten, wenn Sie &quot;ubox&quot;als Teil Ihrer Implementierung verwenden. Wenn die Zulassungsliste nicht angegeben wird, kann [!DNL Adobe] die Umleitungs-URLs nicht überprüfen und vor potenziellen böswilligen Umleitungen schützen.
>
>Die Zulassungsliste hat Vorrang vor Umgebungen. Löschen Sie alle Hosts, bevor Sie die Funktion &quot;Zulassungsliste&quot;verwenden, und dann werden nur die von der Zulassungsliste zugelassenen Hosts in Ihrer Hostliste angezeigt. Anschließend können Sie die Hosts in die gewünschten Umgebungen verschieben.

Manchmal erscheinen Hosts anderer Sites in Ihren Umgebungen. Eine Domäne wird in der Liste angezeigt, wenn die Domäne at.js aufruft. Wenn beispielsweise eine Ihrer Webseiten auf den Server eines anderen kopiert wird, wird diese Domain in Ihrer Umgebung angezeigt. Es können auch Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt werden.

In Fällen, in denen `mboxHost` an einen API-Aufruf weitergegeben wird, wird die Konversion für die weitergegebene Umgebung aufgezeichnet. Wenn keine Umgebung übergeben wird, ist der Host im Aufruf standardmäßig [!UICONTROL Production].

Sie können auch eine Blockierungsliste erstellen, die Hosts (Domänen) angibt, die keine [!DNL Target] Anforderungen an [!DNL Target] senden können, indem Sie die gewünschten Hosts in das Feld [!UICONTROL Host Does Not Contain] einfügen.

>[!NOTE]
>
>Die Liste [!UICONTROL Authorized Hosts] wird sowohl für [!DNL Target] -Hosts als auch für standardmäßige Weiterleitungs-Hosts verwendet. Fügen Sie alle vorhandenen Domänen hinzu, die für die Verwendung des [!DNL Adobe Target] JavaScript SDK (at.js) *UND* genehmigt wurden, und zwar alle Domänen, die in den Standard-Umleitungs-URLs der Ubox verwendet werden. Fügen Sie der Zulassungsliste in Zukunft alle neuen ähnlichen Domänen hinzu.

## Löschen eines Hosts {#section_F56355BA4BC54B078A1A8179BC954632}

Sie können einen Host, der nicht mehr gebraucht wird, löschen.

1. Klicken Sie in der Liste [!UICONTROL Hosts] auf das Symbol **[!UICONTROL Delete]** .
1. Klicken Sie auf **[!UICONTROL Delete]** , um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Der Host wird erneut aufgeführt, wenn ein Besucher zu einer Seite navigiert, die eine [!DNL Target] -Anfrage auf dem Host enthält.

## Fehlerbehebung für Hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probieren Sie folgende Methoden zur Fehlerbehebung aus, falls Probleme mit Ihren Hosts auftreten:

**Der Host wird nicht in der Liste für Ihr Konto angezeigt.**

* Aktualisieren Sie die Seite [!UICONTROL Hosts] in Ihrem Browser.
* Vergewissern Sie sich, dass die [!DNL Target] -Anfrage einschließlich der at.js-Referenz korrekt ist.
* Versuchen Sie, zu einer der [!DNL Target] -Anforderungen auf dem Host zu navigieren. Es ist möglich, dass keine [!DNL Target] -Anfrage auf dem Host jemals in einem Browser gerendert wurde.

**Zufällige oder unbekannte Domänen werden in der Liste [!UICONTROL Host] angezeigt.**

Eine Domäne wird in dieser Liste angezeigt, wenn eine Anforderung an [!DNL Target] von der Domäne stammt. Häufig werden Domänen von Spider-Engines, Übersetzungssites oder lokalen Festplatten angezeigt. Wenn die aufgelistete Domäne nicht von Ihrem Team verwendet wird, können Sie auf [!UICONTROL Delete] klicken, um sie zu entfernen.

**Meine [!DNL Target] -Anfrage gibt /&#42; keine Anzeige zurück - nicht autorisierter Mbox-Host &#42;/.**

Wenn eine [!DNL Target] -Anfrage auf einem nicht autorisierten Host erfolgt, antwortet die Anfrage mit /&#42; no display - unauthorized mbox host &#42;/.
