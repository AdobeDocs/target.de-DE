---
keywords: mbox.js faq;mbox.js frequently asked questions;document.write;tt.omtrdc.net;parser blocking
description: Antworten auf häufig zu „mbox.js“ gestellte Fragen
title: Häufig gestellte Fragen zu „mbox.js“
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 98%

---


# Häufig gestellte Fragen zu „mbox.js“{#mbox-js-frequently-asked-questions}

Antworten auf häufig zu „mbox.js“ gestellte Fragen

## Wie wirkt sich mbox.js auf Seitenladezeiten aus? {#section_90B3B94FE0BF4B369577FCB97B67F089}

Weitere Informationen finden Sie unter [Die Vorteile von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits).

## Warum erhalte ich Warnhinweise zur Parser-Blockade in Google Chrome, wenn ich „mbox.js“ und „document.write“ verwende? {#section_355A3A5BF02F42EEB8271C96EF41590A}

Diese Konsolenmeldung wird angezeigt, wenn Chrome für unterschiedliche Szenarien mit Verwendung der Funktion `document.write` in der Datei mbox.js eingesetzt wird. Es handelt sich hierbei um einen Warnhinweis, der jedoch keine Auswirkung auf die Aktivitätserstellung hat.

Am einfachsten lässt sich diese Meldung vermeiden, indem Sie  [die Target-Implementierung in die JavaScript-Bibliothek at.js migrieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA), in der `document.write` nicht verwendet wird. Die Verwendung von at.js bietet gegenüber mbox.js zahlreiche weitere Vorteile. Weitere Informationen finden Sie in den [häufig gestellten Fragen zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769).

## Warum werden meine Mboxes nicht auf meinen Webseiten ausgelöst? {#section_4BA5DA424B734324AAB51E4588FA50F5}

Target-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

Modere Browser speichern keine Cookies, wenn Sie diese Domänen verwenden - es sei denn, Sie passen die Einstellung `cookieDomain` mit targetGlobalSettings() an. Weitere Informationen finden Sie unter [Verwenden Cloud-basierter Instanzen mit Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566).

## Was ist die Domain tt.omtrdc.net, zu der die Aufrufe des Target-Servers gehen? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] ist der Domainname für das EDGE-Netzwerk von Adobe, mit dem alle Server-Aufrufe für Target empfangen werden.

## Warum verwenden at.js und mbox.js nicht die Cookie-Flags „HttpOnly“ und „Secure“?{#section_74527E3B41B54B0A83F217C3E664ED1F}

„HttpOnly“ kann nur über Server-seitigen Code festgelegt werden. Target-Cookies, wie z. B. Mbox, werden über JavaScript-Code erstellt und gespeichert. Target kann das Cookie-Flag „HttpOnly“ also nicht verwenden.

„Secure“ kann nur über JavaScript festgelegt werden, wenn die Seite mit HTTPS geladen wurde. Wenn die Seite nur mit HTTP geladen wird, kann JavaScript dieses Flag nicht festlegen. Darüber hinaus ist das Cookie bei der Verwendung des Flags „Secure“ nur auf HTTPS-Seiten verfügbar.

Damit Target Benutzer richtig verfolgen kann – und weil Cookies Client-seitig generiert werden –, verwendet Target keines der Flags.
