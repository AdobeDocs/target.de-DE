---
keywords: Einschränkungen von Visual Experience Composer;Browserunterstützung;Integrationen;Plug-ins;asynchrone Überlegungen
description: Erfahren Sie mehr über die ältere Implementierung von "mbox.js"in Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Was sind die Unterschiede zwischen "at.js"und "mbox.js"?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 92%

---


# Einschränkungen von „at.js“

Zwischen „at.js“ und mbox.js bestehen einige Unterschiede. In diesem Abschnitt werden einige Unterschiede und Einschränkungen behandelt, damit Sie erfolgreich mit „at.js“ arbeiten können.

## Bekannte Einschränkungen von Visual Experience Composer {#section_4B63C97169DE4C93B22944E880FD3DF1}

* Die Optionen „Element einfügen“ und „Neu anordnen“ in Visual Experience Composer sollten in Einzelseiten-Apps vermieden werden.

   Da das DOM bei Seitenladeereignissen für Einzelseiten-Apps nicht gelöscht wird, wie das bei normalen Websites der Fall ist, werden die Aktionen „Element einfügen“ und „Neu anordnen“ möglicherweise mehrere Male angewendet, abhängig davon, wie sich der Besucher in der Einzelseiten-App bewegt.

## Integrationen und Plug-ins   {#section_D92E31170176406AAC7B5005F03D3425}

Einige Funktionen von [!DNL mbox.js] stehen in [!DNL at.js] nicht zur Verfügung. Interne [„mbox.js“-Objekte und -Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (z. B. `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` und andere) werden in [!DNL at.js] nicht mehr unterstützt (Beispiel: `mboxFactoryDefault`). Dies ist beabsichtigt und soll verhindern, dass [!DNL at.js] für nicht unterstützte Funktionen manipuliert wird, was langfristig dazu führen kann, dass eine Implementierung beschädigt wird und eine Aktualisierung nicht mehr möglich ist. Die zulässigen Methoden werden im Abschnitt zu den APIs in dieser Dokumentation behandelt. Konsequenzen:

* Alte seitenbasierte [Integrationen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) mit anderen Adobe-Lösungen funktionieren möglicherweise nicht und sollten auf aktuelle, Server-seitige Integrationen aktualisiert werden.
* [Benutzerdefinierte, für „mbox.js“ entwickelte Plug-ins](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) funktionieren möglicherweise nicht, bis sie für [!DNL at.js] aktualisiert wurden.

   Stellen Sie sicher, dass Sie sämtliche [Plug-ins](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) in Ihre Tests einschließen.

## Erwägungen für asynchrones Laden {#section_B586360A3DD34E2995AE25A18E3FB953}

Da nun alle Mboxes asynchron arbeiten, blockieren sie nicht das Rendern von Seiten und werden nicht in der Reihenfolge zurückgegeben, in der sie ausgelöst wurden.

* Wenn Sie eine globale Mbox im [Form-Based Experience Composer](/help/c-experiences/experiences.md#section_3643394BD424463C8768F2907DEBCC22) verwenden, dürfen HTML-Angebote nur die Tags `<script>`, `<style>` und `<link>` enthalten.

   Bei der Bereitstellung filtert [!DNL at.js] alle anderen HTML-Tags heraus, wenn die globalen Mbox-Angebote angewendet werden. Globale Mbox-Angebote werden auch auf den HTML-HEAD angewendet, sodass DIV, SPAN usw. nicht möglich sind. `<div>test</div>` kann beispielsweise nicht angewendet werden, da das `<div>`-Tag nur in HTML-BODY verwendet werden kann.

* Die ältere, seitenbasierte Integration von [!DNL Target] in [!DNL Analytics] funktioniert nicht mehr.

   Diese Integration setzt voraus, dass der [!DNL Target]-Aufruf vor dem [!DNL Analytics]-Aufruf erfolgt.

* Vermeiden Sie JavaScript-Abhängigkeiten zwischen Ihrem Angebot und der Seite.

   Sie sollten nicht davon ausgehen, dass das JavaScript in Ihrem Angebot vor dem hartcodierten JavaScript unter der Mbox ausgeführt wird.

* Vermeiden Sie JavaScript-Abhängigkeiten zwischen mehreren Angeboten auf der Seite.

   Sie können nicht mehr davon ausgehen, dass das von der ersten Mbox bereitgestellte Angebot vor dem von Ihrer zweiten Mbox bereitgestellten Angebot ausgeführt wird.

* DOM-Manipulations- und Umleitungsangebote sollten über die automatisch erstellte globale Mbox in [!DNL at.js] und im Abschnitt `<head>` > bereitgestellt werden.

   Eine `mboxCreate()`-Funktion ganz oben im Abschnitt `<body>` führt mit hoher Wahrscheinlichkeit zu einem Flackern der Standardinhalte.

