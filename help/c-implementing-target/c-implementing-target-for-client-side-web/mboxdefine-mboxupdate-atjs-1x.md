---
description: 'Informationen über die Funktionen mboxdefine () und mboxupdate () für at. js. '
keywords: adobe.target.notification;Element;Selektor;Benachrichtigung;Erweiterung
seo-description: Informationen über die Funktionen mboxdefine () und mboxupdate () für die javascript-Bibliothek "at. js" von Adobe Target.
seo-title: Informationen über die Funktionen mboxdefine () und mboxupdate () für die javascript-Bibliothek "at. js" von Adobe Target.
solution: Target
subtopic: Erste Schritte
title: mboxDefine() und mboxUpdate() - at.js 1.x
topic: Standard
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mboxDefine() und mboxUpdate() - at.js 1.x

Definieren und aktualisieren Sie eine mbox in Adobe Target.

>[!NOTE]
>
>Diese Funktionen stehen nur für at.js, Version 1.*x*, zur Verfügung. Diese Funktionen wurden mit der Veröffentlichung von at. js 2. x veraltet. Diese Funktionen geben Standardinhalte zurück, wenn sie mit at. js 2. x verwendet werden.

`mboxDefine()` und `mboxCreate()` sind an „DIV“-HTML-Elemente gebunden, in denen das Angebot angezeigt werden soll. Diese Elemente sollten die Klasse `mboxDefault` aufweisen. Wenn diese Klasse nicht an die HTML-Elemente angefügt wird, tritt möglicherweise ein deutliches Flackern auf.

## mboxDefine   {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Erstellt eine interne Zuordnung zwischen einer „nodeid“ und einem Mbox-Namen, führt die Anforderung jedoch nicht aus Die Funktion kommt in der Regel zusammen mit `mboxUpdate()` zum Einsatz. Sie wurde vor allem deswegen in [!DNL at.js] integriert, um die Umstellung von [!DNL mbox.js] auf [!DNL at.js] zu erleichtern.

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Führt die Anforderung aus und wendet das Angebot auf das von `nodeId` in `mboxDefine()` () identifizierte Element an. Die Funktion kann auch dazu genutzt werden, eine Mbox zu aktualisieren, die durch `mboxCreate` initiiert wurde. Sie wurde vor allem deswegen in [!DNL at.js] integriert, um die Umstellung von [!DNL mbox.js] auf [!DNL at.js] zu erleichtern. `mboxDefine()`/ `mboxUpdate()` kann durch [adobe. target. getoffer ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) und [adobe. target. applyoffer ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) ersetzt werden.

## Beispiel {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```
