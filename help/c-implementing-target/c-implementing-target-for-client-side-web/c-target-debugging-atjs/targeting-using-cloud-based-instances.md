---
keywords: Cloud-Instanzen;öffentliche Suffix-Liste;öffentliches Suffix;Cookie;Erstanbieter-Cookie;Erstanbieter-Cookie;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Informieren Sie sich über Probleme (mit Lösungen), mit denen Kunden konfrontiert sind, wenn sie Adobe Target mithilfe von Cloud-basierten Instanzen testen oder zu Testversand-of-Concept-Zwecken arbeiten.
title: Kann ich Zielgruppe mit Cloud-basierten Instanzen verwenden?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Verwenden Cloud-basierter Instanzen mit Target{#use-cloud-based-instances-with-target}

Informationen zu Problemen, die Kunden beim Verwenden Cloud-basierter Instanzen zum Testen von [!DNL Adobe Target] haben.

Target-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Instanzen umfassen möglicherweise die folgenden Domänen:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` oder `firebaseapp.com`.

Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

**Problem:** Moderne Browser speichern keine Cookies, wenn Sie diese Domänen verwenden.

Die [!DNL at.js]- und [!DNL mbox.js]-JavaScript-Bibliotheken verwenden Cookies zum Verfolgen von Benutzern. Dies dient dazu, sicherzustellen, dass [!DNL Target] immer ein konsistentes Erlebnis präsentiert. Wenn in den JavaScript-Bibliotheken von [!DNL Target] keine Cookies gespeichert werden können, werden [!DNL Target]-Anforderungen deaktiviert.

**Lösung:** Wenn Sie Cloud-basierte Instanzen mit in der öffentlichen Suffix-Liste enthaltenen Domänen verwenden möchten, hat es sich bewährt, die `cookieDomain`-Einstellung anzupassen. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).
