---
keywords: Cloud-Instanzen;öffentliche Suffix-Liste;öffentliches Suffix;Cookie;Erstanbieter-Cookie;Erstanbieter-Cookie;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Informieren Sie sich über Probleme (mit Lösungen), mit denen Kunden konfrontiert sind, wenn sie Cloud-basierte Instanzen zum Testen der Adobe [!DNL Target] oder zu Testversand-of-Concept-Zwecken verwenden.
title: Kann ich  [!DNL Target] mit Cloud-basierten Instanzen verwenden?
feature: 'at.js '
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 82%

---

# Verwenden Cloud-basierter Instanzen mit Target

Informationen zu Problemen, die Kunden beim Verwenden Cloud-basierter Instanzen zum Testen von [!DNL Adobe Target] haben.

Target-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Instanzen umfassen möglicherweise die folgenden Domänen:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` oder `firebaseapp.com`.

Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

**Problem:** Moderne Browser speichern keine Cookies, wenn Sie diese Domänen verwenden.

Die [!DNL at.js]- und [!DNL mbox.js]-JavaScript-Bibliotheken verwenden Cookies zum Verfolgen von Benutzern. Dies dient dazu, sicherzustellen, dass [!DNL Target] immer ein konsistentes Erlebnis präsentiert. Wenn in den JavaScript-Bibliotheken von [!DNL Target] keine Cookies gespeichert werden können, werden [!DNL Target]-Anforderungen deaktiviert.

**Lösung:** Wenn Sie Cloud-basierte Instanzen mit in der öffentlichen Suffix-Liste enthaltenen Domänen verwenden möchten, hat es sich bewährt, die `cookieDomain`-Einstellung anzupassen. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).
