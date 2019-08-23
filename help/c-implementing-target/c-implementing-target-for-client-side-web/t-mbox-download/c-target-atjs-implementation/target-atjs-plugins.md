---
description: Informationen zu unterstützten und nicht unterstützten at. js-Plugins in Target.
keywords: at. js-Plugins; unterstützte Plugins; nicht unterstützte Plugins; Ttmeta; ttmeta; Mboxtrack
seo-description: Informationen zu unterstützten und nicht unterstützten at. js-Plugins für Adobe Target
seo-title: '" at. js" -Plugins für Adobe Target'
solution: Target
title: „at.js“-Plug-ins
topic: Standard
uuid: ef36b2b2-bf6d-497e-b3f5-2b572a1b8a8d
translation-type: tm+mt
source-git-commit: c3afa420f33f98d7c4bb332acdef7a248fe4670a

---


# at.js plug-ins{#at-js-plug-ins}

Informationen zu unterstützten und nicht unterstützten at. js-Plugins in Adobe Target.

Viele Benutzer haben angepasste und Antwort-Plug-ins für [!DNL mbox.js] entwickelt. Solche benutzerdefinierten Plug-ins werden von [!DNL at.js] möglicherweise nicht unterstützt und benötigen eine Aktualisierung.

Sollten Sie ein Plug-in verwenden, das hier nicht aufgeführt ist, und seinen Status erfahren wollen, wenden Sie sich an Ihren Kundenbetreuer.

Hier finden Sie den aktuellen Status einiger der Plug-ins, die von vielen Kunden mit [!DNL at.js] genutzt werden:

| Plug-in | Details |
|--- |--- |
| mboxTrack | Wird nicht unterstützt.<br>Dies wird durch die Funktion [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) ersetzt. Aktualisieren Sie Ihre Plug-ins, um die neue Funktion anzuwenden.<br>Weitere Informationen finden Sie auf der Seite [Integrationen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md). |
| Plug-in zur beständigen Profilsicherung | Wird nicht unterstützt.<br>Die Unterstützung für dieses Plug-in wurde eingestellt, nachdem die Profillebensdauer in Target von zwei Wochen auf 90 Tage erweitert wurde. Prüfen Sie das Ablaufdatum Ihres Mbox-Cookies, um die Einstellung zur Profillebensdauer in Ihrem Konto herauszufinden.<br>Wenden Sie sich an den Kundendienst, wenn Sie die Profillebensdauer auf 90 Tage erweitern möchten. |
| ttMeta | Old SiteCatalyst plugins should be disabled and replaced with [Adobe Analytics as the reporting source for Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Das ttMeta-Plugin sollte deaktiviert und durch [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj) ersetzt werden. |