---
keywords: Cloud-Instanzen;öffentliche Suffix-Liste;öffentliches Suffix;Cookie;Erstanbieter-Cookie;Erstanbieter-Cookie;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Erfahren Sie mehr über Probleme (mit Lösungen), mit denen Kunden konfrontiert sind, wenn sie Cloud-basierte Instanzen zum Testen der Adobe [!DNL Target] oder zum Testen des Machbarkeitsnachweises verwenden.
title: Kann ich [!DNL Target] mit Cloud-basierten Instanzen verwenden?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 67%

---

# Verwenden Cloud-basierter Instanzen mit Target

Informationen zu Problemen, die Kunden beim Verwenden Cloud-basierter Instanzen zum Testen von [!DNL Adobe Target] haben.

Target-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Instanzen umfassen möglicherweise die folgenden Domänen:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` oder `firebaseapp.com`.

Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

**Problem:** Moderne Browser speichern keine Cookies, wenn Sie diese Domänen verwenden.

Die JavaScript-Bibliothek [!DNL at.js] verwendet Cookies zum Verfolgen von Benutzern, um sicherzustellen, dass [!DNL Target] immer ein konsistentes Erlebnis darstellt. Wenn die JavaScript-Bibliothek [!DNL Target] keine Cookies speichern kann, werden [!DNL Target]-Anforderungen deaktiviert.

**Lösung:** Wenn Sie Cloud-basierte Instanzen mit in der öffentlichen Suffix-Liste enthaltenen Domänen verwenden möchten, hat es sich bewährt, die `cookieDomain`-Einstellung anzupassen. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).
