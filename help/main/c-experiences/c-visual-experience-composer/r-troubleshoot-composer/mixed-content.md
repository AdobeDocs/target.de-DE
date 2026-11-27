---
keywords: gemischte Inhalte;sicher;unsicher;Chrome;Fehlerbehebung;VEC;Visual Experience Composer;unsecure;http;https;Firefox;Internet Explorer
description: Erfahren Sie, wie Sie gemischte Inhalte in [!DNL Chrome], [!DNL Firefox] und [!DNL Edge] aktivieren.
title: Wie aktiviere ich gemischte Inhalte in meinem Browser
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
TQID: 'https://experienceleague.adobe.com/6Q1UvNmU-vSr9sp3pe2JN-wkjFUMWFxtPkgQegArrVw'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 11%
---
# Zulassen von gemischtem Inhalt im Browser {#mixed-content}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie gemischte Inhalte in [!DNL Google Chrome], [!DNL Mozilla Firefox] und [!DNL Microsoft Edge] aktivieren, damit der **[!UICONTROL Visual Experience Composer]** (VEC) HTTP-Websites und Websites öffnen kann, die gemischte Inhalte enthalten.

>[!ENDSHADEBOX]

Eine Seite enthält gemischte Inhalte, wenn sie sicher über HTTPS angefordert wird, aber sowohl HTTPS- als auch HTTP-Inhalte lädt. HTTPS-Inhalte sind sicher, HTTP-Inhalte dagegen nicht, sodass moderne Browser eine solche Seite blockieren oder eine Warnmeldung anzeigen.

Wenn der **[!UICONTROL Visual Experience Composer]** (VEC) in [!DNL Adobe Target] versucht, eine Seite zu öffnen, die gemischte Inhalte enthält, wird eine Warnmeldung mit Anweisungen zum Deaktivieren der Blockierung im Browser angezeigt. Durch Deaktivieren der Blockierung kann eine HTTP-Site oder eine Site mit gemischtem Inhalt (HTTPS und HTTP) geöffnet werden.

![Seite zur Aktivitätserstellung mit der Meldung, dass Browser-Skripte geladen werden dürfen, um Aktivitäten zu erstellen, neben einer Illustration der Aufforderung zum erneuten Laden des Browsers](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Zuvor blieben einige Aktionen in Schritt 1 des dreistufigen geleiteten Workflows verfügbar, wenn gemischte Inhalte nicht zulässig waren. [!DNL Target] blockiert jetzt alle Aktionen in Schritt 1, sodass gemischte Inhalte aktiviert werden müssen, bevor die Erstellung der Aktivität fortgesetzt werden kann.

Die Sicherheitseinstellungen des Browsers blockieren möglicherweise nicht sichere (HTTP-)Inhalte, die auf einer sicheren (HTTPS-)Seite oder in einem sicheren Frame wie dem VEC geladen werden. Die Alternative zum Ändern dieser Einstellungen ist eine HTTPS-Website. Wenn die Website in einer unsicheren (HTTP-)Domain ausgeführt wird, muss der VEC aktive gemischte Inhalte laden dürfen.

>[!IMPORTANT]
>
>Das Zulassen von gemischtem Inhalt wirkt sich nur auf VEC und nicht auf die Live-Website aus.

Weitere Informationen finden Sie unter [Gemischte Inhalte](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) auf der *Mozilla Developer Network* (MDN-)Website.

## Zulassen von gemischtem Inhalt in [!DNL Google Chrome]

[!DNL Chrome] überprüft, ob der Inhalt einer über eine sichere Verbindung angeforderten Seite sicher übertragen wurde. Siehe [Warnungen zu unsicheren Sites verwalten](https://support.google.com/chrome/answer/99020?hl=de) in der Hilfe von Google Chrome.

Um VEC mit der neuesten Version von [!DNL Chrome] (Version 79.0.3945.117 oder höher) zu verwenden, aktualisieren Sie die Site-Einstellungen wie folgt. Besucherinnen und Besucher der Website müssen diese Schritte nicht ausführen.

1. Klicken Sie auf das Schlosssymbol (Achtung) und dann auf **[!UICONTROL Site-Einstellungen]**.

   ![Chrome-Adressleiste mit hervorgehobenem Verbindungsmenü „Öffnen“ und hervorgehobenen Site-Einstellungen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Ändern **[!UICONTROL unter „Nicht sicherer]**&quot; in der Dropdown-Liste „Sperren (Standard)“ in „Zulassen“.

   ![Einstellungen der Chrome-Site, in denen die Dropdown-Liste „Nicht sicherer Inhalt“ geöffnet ist und die Option „Zulassen“ ausgewählt wurde](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laden Sie die VEC-Seite neu.

## Zulassen von gemischtem Inhalt in [!DNL Mozilla Firefox]

Standardmäßig blockiert [!DNL Firefox] Seiten, die sicheren und nicht sicheren Inhalt mischen. Daher muss diese Einstellung dauerhaft geändert werden, um [!DNL Target] verwenden zu können. Besucherinnen und Besucher der Website müssen diese Schritte nicht ausführen.

1. Geben Sie in [!DNL Firefox] in der Adressleiste `about:config` ein.
1. Bestätigen Sie die von [!DNL Firefox] angezeigte Warnmeldung.

   ![Firefox Fahren Sie mit der Warnseite Vorsicht für :config mit der Schaltfläche Risiko akzeptieren und fortfahren fort](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Geben Sie in der Suchleiste `block_active` ein.

   ![Firefox über:config Suchen Sie nach block_active, wobei security.Mixed_content.block_active_content auf „true“ gesetzt ist](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Doppelklicken Sie auf `security.mixed_content.block_active_content`.

   Der Wert ändert sich von „True“ in „False“. Wenn der Wert „False“ anzeigt, ist die Änderung abgeschlossen.

   ![Firefox über:config Anzeigen von security.Mixed_content.block_active_content auf „false“ festgelegt](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. Starten Sie den Computer neu, nachdem Sie diese Einstellung geändert haben.

## Zulassen von gemischtem Inhalt in [!DNL Microsoft Edge]

[!DNL Edge] überprüft, ob der Inhalt einer über eine sichere Verbindung angeforderten Seite sicher übertragen wurde. Um VEC mit der neuesten Version von [!DNL Edge] zu verwenden, aktualisieren Sie die Site-Einstellungen wie folgt. Besucherinnen und Besucher der Website müssen diese Schritte nicht ausführen.

1. Klicken Sie [!DNL Edge] in der Menüleiste auf **[!DNL Microsoft Edge]**, klicken Sie auf **[!UICONTROL Einstellungen]** und dann auf **Cookies und Site-Berechtigungen**.
1. Scrollen Sie zu **[!UICONTROL Nicht sicherer Inhalt]** und klicken Sie darauf.
1. Klicken Sie neben **[!UICONTROL Zulassen]** auf **[!UICONTROL Hinzufügen]**, geben Sie die Site ein, auf der unsichere Inhalte zugelassen werden sollen, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.
1. Laden Sie die VEC-Seite neu.
