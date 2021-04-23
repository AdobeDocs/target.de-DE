---
keywords: at.js-Plug-ins; unterstützte Plugins; nicht unterstützte Plugins; ttMeta; ttmeta; mboxTrack
description: Erfahren Sie mehr über die ältere Implementierung von "mbox.js"in Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Welche älteren Plugins werden in  [!DNL Target] at.js nicht unterstützt?
feature: 'at.js '
role: Developer
exl-id: 1d858f5b-58dc-4181-9cb5-aa6b22011abc
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 82%

---

# „at.js“-Plug-ins

Informationen zu unterstützten und nicht unterstützten at.js-Plug-ins in Adobe Target.

Viele Benutzer haben angepasste und Antwort-Plug-ins für [!DNL mbox.js] entwickelt. Solche benutzerdefinierten Plug-ins werden von [!DNL at.js] möglicherweise nicht unterstützt und benötigen eine Aktualisierung.

Sollten Sie ein Plug-in verwenden, das hier nicht aufgeführt ist, und seinen Status erfahren wollen, wenden Sie sich an Ihren Kundenbetreuer.

Hier finden Sie den aktuellen Status einiger der Plug-ins, die von vielen Kunden mit [!DNL at.js] genutzt werden:

| Plug-in | Details |
|--- |--- |
| mboxTrack | Wird nicht unterstützt.<br>Dies wird durch die Funktion [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) ersetzt. Aktualisieren Sie Ihre Plug-ins, um die neue Funktion anzuwenden.<br>Weitere Informationen finden Sie auf der Seite [Integrationen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md). |
| Plug-in zur beständigen Profilsicherung | Wird nicht unterstützt.<br>Die Unterstützung für dieses Plug-in wurde eingestellt, nachdem die Profillebensdauer in Target von zwei Wochen auf 90 Tage erweitert wurde. Prüfen Sie das Ablaufdatum Ihres Mbox-Cookies, um die Einstellung zur Profillebensdauer in Ihrem Konto herauszufinden.<br>Wenden Sie sich an den Kundendienst, wenn Sie die Profillebensdauer auf 90 Tage erweitern möchten. |
| ttMeta | Alte SiteCatalyst-Plug-ins sollten deaktiviert und durch [Adobe Analytics als Berichtsquelle für Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) ersetzt werden. Das ttMeta-Plugin sollte deaktiviert und durch [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) ersetzt werden. |
