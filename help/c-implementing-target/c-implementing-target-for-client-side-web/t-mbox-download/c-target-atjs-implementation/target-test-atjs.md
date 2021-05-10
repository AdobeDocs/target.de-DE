---
keywords: at.js;Nicht-Produktion;Nicht-Produktion;Bereitstellung
description: Erfahren Sie mehr über die ältere Implementierung von "mbox.js"in Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Wie stelle ich at.js in einer Nicht-Produktions-Umgebung bereit?
feature: 'at.js '
role: Developer
exl-id: 607b2b5b-bb2a-4443-abc0-452b421fc009
translation-type: tm+mt
source-git-commit: 824743300725bbd39077882a0971a9ccb4f753ab
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 80%

---

# &quot;at.js&quot;in einer Nicht-Produktions-Umgebung bereitstellen

Informationen zur sicheren Bereitstellung von „at.js“ in einer Nicht-Produktionsumgebung.

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
