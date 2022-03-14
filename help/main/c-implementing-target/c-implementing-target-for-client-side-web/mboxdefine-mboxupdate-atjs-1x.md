---
keywords: Mboxdefine; mboxdefine; mbox definie; Mboxupdate; mboxupdate; mbox-Update; at.js; Funktionen; funktion
description: Verwenden Sie die Funktionen mboxDefine() und mboxUpdate() für die Adobe. [!DNL Target] JavaScript-Bibliothek at.js , um eine Mbox zu definieren oder zu aktualisieren. (at.js 1.x)
title: Wie verwende ich die Funktionen mboxDefine() und mboxUpdate()?
feature: at.js
role: Developer
exl-id: 48261be0-c4d0-4961-9712-ef7e0d2cb1c0
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 75%

---

# mboxDefine() und mboxUpdate() - at.js 1.x

Definieren und aktualisieren Sie eine Mbox in Adobe Target.

>[!NOTE]
>
>Diese Funktionen stehen nur für at.js, Version 1.*x*, zur Verfügung. Diese Funktionen sind mit der Veröffentlichung von at.js 2.x überholt. Diese Funktionen geben Standardinhalte zurück, wenn sie mit at.js 2.x verwendet werden.

`mboxDefine()` und `mboxCreate()` sind an „DIV“-HTML-Elemente gebunden, in denen das Angebot angezeigt werden soll. Diese Elemente sollten die Klasse `mboxDefault` aufweisen. Wenn diese Klasse nicht an die HTML-Elemente angefügt wird, tritt möglicherweise ein deutliches Flackern auf.

## mboxDefine  {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Erstellt eine interne Zuordnung zwischen einer „nodeid“ und einem Mbox-Namen, führt die Anforderung jedoch nicht aus Die Funktion kommt in der Regel zusammen mit `mboxUpdate()` zum Einsatz. Integriert in [!DNL at.js] hauptsächlich um die Umstellung von [!DNL mbox.js] (jetzt nicht mehr unterstützt) auf [!DNL at.js].

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Führt die Anforderung aus und wendet das Angebot auf das von `nodeId` in `mboxDefine()` () identifizierte Element an. Die Funktion kann auch dazu genutzt werden, eine Mbox zu aktualisieren, die durch `mboxCreate` initiiert wurde. Integriert in [!DNL at.js] hauptsächlich um die Umstellung von [!DNL mbox.js] (jetzt nicht mehr unterstützt) auf [!DNL at.js]. `mboxDefine()`/ `mboxUpdate()` kann mithilfe der Selektor-Option durch [adobe.target.getOffer()](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) und [adobe.target.applyOffer()](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) ersetzt werden.

## Beispiel {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```javascript
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```