---
keywords: mbox.js FAQ;häufig gestellte Fragen zu mbox.js;document.write;tt.omtrdc.net;Parser-Blockierung
description: Erfahren Sie mehr über die alte mbox.js-Implementierung von Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Was sind häufig gestellte Fragen zu [!DNL Target] mbox.js?
feature: at.js
role: Developer
exl-id: 0e207896-d45b-45f9-8556-6532fda72a45
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 75%

---

# Häufig gestellte Fragen zu „mbox.js“

Antworten auf häufig zu „mbox.js“ gestellte Fragen

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Wir empfehlen allen Kunden, vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek zu migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Warum werden meine Mboxes nicht auf meinen Webseiten ausgelöst? {#section_4BA5DA424B734324AAB51E4588FA50F5}

Target-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

Modere Browser speichern keine Cookies, wenn Sie diese Domänen verwenden - es sei denn, Sie passen die Einstellung `cookieDomain` mit targetGlobalSettings() an. Weitere Informationen finden Sie unter [Verwenden Cloud-basierter Instanzen mit Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566).

## Was ist die Domain tt.omtrdc.net, zu der die [!DNL Target]-Server-Aufrufe gehen? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] ist der Domainname für das EDGE-Netzwerk von Adobe, mit dem alle Server-Aufrufe für Target empfangen werden.

## Warum verwenden at.js und mbox.js nicht die Cookie-Flags „HttpOnly“ und „Secure“? {#section_74527E3B41B54B0A83F217C3E664ED1F}

„HttpOnly“ kann nur über Server-seitigen Code festgelegt werden. Target-Cookies, wie z. B. Mbox, werden über JavaScript-Code erstellt und gespeichert. Target kann das Cookie-Flag „HttpOnly“ also nicht verwenden.

„Secure“ kann nur über JavaScript festgelegt werden, wenn die Seite mit HTTPS geladen wurde. Wenn die Seite nur mit HTTP geladen wird, kann JavaScript dieses Flag nicht festlegen. Darüber hinaus ist das Cookie bei der Verwendung des Flags „Secure“ nur auf HTTPS-Seiten verfügbar.

Damit Target Benutzer richtig verfolgen kann – und weil Cookies Client-seitig generiert werden –, verwendet Target keines der Flags.
