---
keywords: at.js plugins;supported plugins;unsupported plugins;ttMeta;ttmeta;mboxTrack
description: Informationen zu unterstützten und nicht unterstützten Plug-ins für „at.js“ in Adobe Target
title: at.js-Plug-ins für Adobe Target
feature: at.js
translation-type: tm+mt
source-git-commit: 88f6e4c6ad168e4f9ce69aa6618d8641b466e28a
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 97%

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