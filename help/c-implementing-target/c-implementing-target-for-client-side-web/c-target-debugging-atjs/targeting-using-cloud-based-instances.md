---
keywords: Cloud-Instanzen;öffentliche Suffix-Liste;öffentliches Suffix;Cookie;Erstanbieter-Cookie;Erstanbieter-Cookie;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Informationen zu Problemen, die Kunden beim Verwenden Cloud-basierter Instanzen zum Testen von Adobe Target haben.
title: Cloud-basierte Instanzen verwenden
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 94%

---


# Verwenden Cloud-basierter Instanzen mit Target{#use-cloud-based-instances-with-target}

Informationen zu Problemen, die Kunden beim Verwenden Cloud-basierter Instanzen zum Testen von [!DNL Adobe Target] haben.

Target-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Instanzen umfassen möglicherweise die folgenden Domänen:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` oder `firebaseapp.com`.

Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

**Problem:** Moderne Browser speichern keine Cookies, wenn Sie diese Domänen verwenden.

Die [!DNL at.js]- und [!DNL mbox.js]-JavaScript-Bibliotheken verwenden Cookies zum Verfolgen von Benutzern. Dies dient dazu, sicherzustellen, dass [!DNL Target] immer ein konsistentes Erlebnis präsentiert. Wenn in den JavaScript-Bibliotheken von [!DNL Target] keine Cookies gespeichert werden können, werden [!DNL Target]-Anforderungen deaktiviert.

**Lösung:** Wenn Sie Cloud-basierte Instanzen mit in der öffentlichen Suffix-Liste enthaltenen Domänen verwenden möchten, hat es sich bewährt, die `cookieDomain`-Einstellung anzupassen. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).
