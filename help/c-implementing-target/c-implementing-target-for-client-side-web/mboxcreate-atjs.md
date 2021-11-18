---
keywords: Mboxcreate; mboxcreate; mbox create; at.js; Funktionen; funktion
description: Verwenden der Funktion mboxCreate() für die Adobe [!DNL Target] JavaScript-Bibliothek at.js , um Angebote auf das nächstgelegene DIV mit dem Klassennamen mboxDefault anzuwenden. (at.js 1.x)
title: Wie verwende ich die Funktion mboxCreate()?
feature: at.js
role: Developer
exl-id: 821ad97a-345a-4e56-9be6-ab1c7d3a651d
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 79%

---

# mboxCreate(mbox,params) - at.js 1.x

Führt eine Anforderung aus und wendet das Angebot auf den nächsten DIV-Bereich mit dem Klassennamen „mboxDefault“ an.

>[!NOTE]
>
>Diese Funktion steht nur für at.js, Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird.

Diese Funktion ist in [!DNL at.js] hauptsächlich um die Umstellung von [!DNL mbox.js] (jetzt nicht mehr unterstützt) auf [!DNL at.js]. Eine aktuellere Alternative zu `mboxCreate()` ist `adobe.target.applyOffer()`/ `adobe.target.getOffer()` oder die Angular-Richtlinie.

## Beispiel

```javascript
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  mboxCreate('mboxName','param1=value1','param2=value2'); 
</script>
```

## Hinweise

`mboxCreate()` verwendet nun den „json“- statt des „standard“-Endpunkts und wird asynchron ausgelöst. Konsequenzen:

* [Debuggen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) verhält sich ein wenig anders.
* Vermeiden Sie Angebotscode, der synchrone, blockierende Aufrufe voraussetzt.

   Ein Beispiel hierfür wären Angebote mit JavaScript-Variablen, die vom Websitecode oder anderen Mboxes verwendet werden, die später auf der Seite auftauchen.

* Achten Sie darauf, einen `<div class="mboxDefault"></div>`-Bereich zu definieren, bevor Sie `mboxCreate()` aufrufen, da [!DNL at.js] diesen Bereich nicht selbstständig erstellt.

* Von leeren `mboxCreate()`-Funktionen als globale Mbox ganz oben auf der Seite wird abgeraten.

   Die automatisch erstellte globale Mbox in [!DNL at.js] ist die bessere Option, da sie im `<head>`-Bereich ausgelöst wird und Inhalte früher zurückgeben kann.
