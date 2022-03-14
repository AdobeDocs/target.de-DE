---
keywords: Cloud-Instanzen;öffentliche Suffix-Liste;öffentliches Suffix;Cookie;Erstanbieter-Cookie;Erstanbieter-Cookie;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Probleme (mit Lösungen) bei Kunden, die Cloud-basierte Instanzen zum Testen der Adobe verwenden [!DNL Target] oder zu Machbarkeitszwecken.
title: Kann ich [!DNL Target] mit Cloud-basierten Instanzen?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 70%

---

# Verwenden Cloud-basierter Instanzen mit Target

Informationen zu Problemen, die Kunden beim Verwenden Cloud-basierter Instanzen zum Testen von [!DNL Adobe Target] haben.

Target-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Instanzen umfassen möglicherweise die folgenden Domänen:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` oder `firebaseapp.com`.

Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

**Problem:** Moderne Browser speichern keine Cookies, wenn Sie diese Domänen verwenden.

Die [!DNL at.js] Die JavaScript-Bibliothek verwendet Cookies zur Benutzerverfolgung, um sicherzustellen, dass [!DNL Target] immer ein konsistentes Erlebnis darstellt. Wenn die Variable [!DNL Target] Cookies können nicht in der JavaScript-Bibliothek gespeichert werden. [!DNL Target] -Anfragen deaktiviert sind.

**Lösung:** Wenn Sie Cloud-basierte Instanzen mit in der öffentlichen Suffix-Liste enthaltenen Domänen verwenden möchten, hat es sich bewährt, die `cookieDomain`-Einstellung anzupassen. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).