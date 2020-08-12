---
description: Informationen zur sicheren Bereitstellung von „at.js“ in einer Nicht-Produktionsumgebung.
title: Bereitstellung von „at.js“ in einer Nicht-Produktionsumgebung
feature: null
uuid: 7f1adc43-35b4-442c-bb06-feab60604a87
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 92%

---


# Deploy at.js to a non-production environment{#deploy-at-js-to-a-non-production-environment}

Informationen zur sicheren Bereitstellung von „at.js“ in einer Nicht-Produktionsumgebung.

## DTM-Staging bereitstellen

Wenn Sie DTM verwenden, können Sie at.js ganz einfach in Ihrer Adobe Target-Toolkonfiguration speichern.

Speichern Sie die Bibliothek und verwenden Sie das DTM-Wechseltool, um sie mit Ihrem Produktionscode zu testen. Dadurch können Sie Ihre Adobe-Berater auch besser unterstützen.

Weitere Informationen finden Sie unter [Option 3: Manuelle Implementierung von Target mit in DTM gehosteter JavaScript-Target-Bibliothek](https://docs.adobe.com/content/help/en/dtm/implementing/target/add-target/t-implementing-target-manually-js-hosted-dtm.html) im Abschnitt *Best Practices zur Implementierung von Adobe Target mit Dynamic Tag Management*.

## Chrome-Erweiterung „Requestly“ zum Zuordnen einer anderen Datei verwenden

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie auch die [Adobe Target VEC Helper-Browsererweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) für Google Chrome verwenden.

Bei [Requestly](https://chrome.google.com/webstore/detail/requestly/mdnleldcmiljblolnjhpnblkcekpdkpa?hl=en) handelt es sich um eine kostenlose Chrome-Erweiterung, mit deren Hilfe Sie Anfragen an eine andere URL umleiten können.

Sie stellen at.js für eine URL bereit und verwenden anschließend Requestly, um Ihre aktuelle mbox.js-Datei-URL der neuen at.js-URL zuzuordnen. Wenn Ihre Website anschließend versucht, mbox.js zu laden, wird stattdessen at.js geladen. Mit diesem Ansatz kann sie Adobe auch besser unterstützen.

## In einer Entwicklungs-, Staging- oder QS-Umgebung bereitstellen

Wenn Sie mbox.js in Ihrer Codebasis hosten und einfach Aktualisierungen an Ihren Codeumgebungen vornehmen können, stellen Sie at.js in einer Ihrer niedrigeren Umgebungen bereit.

Damit Adobe Sie besser unterstützen kann, sollten Sie die Datei in einer Umgebung bereitstellen, auf die von Adobe zugegriffen werden kann.

## Charles oder Fiddler für die Zuordnung zu einer lokalen Datei verwenden

[Charles Web Debugging Proxy](https://www.charlesproxy.com/) ist eine Anwendung für Mac und Windows, deren Funktion „Map Local“ (Lokal zuordnen) genutzt werden kann, um das Laden der mbox.js-Produktionsdatei einer lokalen Kopie von at.js zuzuordnen. Eine Testversion für Mac und Windows kann kostenlos heruntergeladen werden.

[Fiddler](https://www.telerik.com/fiddler) ist ein ähnliches Tool, das ebenfalls kostenlos für Windows heruntergeladen werden kann.

## In einer anderen Tag-Manager-Umgebung bereitstellen

Wenn Sie einen anderen Tag-Manager verwenden, bietet dieser wahrscheinlich eine Funktion an, um at.js sicher und ohne Auswirkungen auf Ihren Produktionstraffic bereitzustellen.