---
keywords: Mboxcreate; mboxcreate; mbox create; at.js; Funktionen; funktion
description: Verwenden Sie die Funktion mboxCreate() für die Adobe Target at.js JavaScript-Bibliothek, um Angebot auf das nächste DIV mit dem Klassennamen mboxDefault anzuwenden. (at.js 1.x)
title: Wie verwende ich die Funktion mboxCreate()?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 85%

---


# mboxCreate(mbox,params) - at.js 1.x {#reference_E68805FE86C64792B2066DB17B253D74}

Führt eine Anforderung aus und wendet das Angebot auf den nächsten DIV-Bereich mit dem Klassennamen „mboxDefault“ an.

>[!NOTE]
>
>Diese Funktion steht nur für at.js, Version 1.*x*, zur Verfügung. Diese Funktion ist mit der Veröffentlichung von at.js 2.x überholt. Diese Funktion gibt Standardinhalte zurück, wenn sie mit at.js 2.x verwendet wird.

Diese Funktion wurde vor allem deswegen in [!DNL at.js] integriert, um die Umstellung von [!DNL mbox.js] auf [!DNL at.js] zu erleichtern. Eine aktuellere Alternative zu `mboxCreate()` ist `adobe.target.applyOffer()`/ `adobe.target.getOffer()` oder die Angular-Richtlinie.

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