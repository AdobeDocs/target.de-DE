---
keywords: gemischte Inhalte;sicher;unsicher;Chrome;Fehlerbehebung;VEC;Visual Experience Composer;unsecure;http;https;Firefox;Internet Explorer
description: Erfahren Sie, wie Sie gemischte Inhalte in [!DNL Chrome], [!DNL Firefox], und [!DNL Edge].
title: So aktivieren Sie gemischten Inhalt in meinem Browser
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
source-git-commit: c5b43faa2fc55c2c8737e586cfdfaa1444a05880
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 64%

---

# Zulassen von gemischtem Inhalt in Ihrem Browser

Gemischte Inhalte treten auf, wenn die ursprüngliche Anfrage über HTTPS sicher ist, aber HTTPS- *und* HTTP-Inhalte geladen werden, um die Webseite anzuzeigen. HTTPS-Inhalt ist sicher. HTTP-Inhalte sind nicht sicher.

Moderne Browser blockieren möglicherweise die Anzeige einer Seite oder zeigen einen Warnhinweis an, wenn sicherer gemeinsam mit nicht sicherem Inhalt aufgerufen wird.

Ein Warnhinweis wird angezeigt, wenn [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] versucht, eine Seite mit gemischtem Inhalt zu öffnen. Dieser Hinweis informiert Sie darüber, wie Sie die Blockierung in Ihrem Browser deaktivieren können. Durch Deaktivieren der Blockierung können Sie eine HTTP-Site oder eine Site mit gemischtem Inhalt (HTTPS und HTTP) öffnen.

![Warnung zu gemischtem Inhalt](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Zuvor konnten Sie, wenn gemischte Inhalte nicht zulässig waren, in Schritt 1 des dreistufigen Workflows beim Erstellen von Aktivitäten dennoch einige Aktionen ausführen. Von nun an blockiert [!DNL Target] Aktionen in Schritt 1. Wenn dieser Hinweis angezeigt wird, müssen Sie gemischte Inhalte aktivieren, bevor Sie den Vorgang fortsetzen können.

Die Sicherheitseinstellungen Ihres Browsers verhindern möglicherweise, dass gemischter Inhalt oder nicht sicherer (HTTP-)Inhalt auf einer sicheren (HTTPS-)Seite oder in einem sicheren Frame (z. B. VEC) geladen wird. Wenn Sie die Sicherheitseinstellungen Ihres Browsers nicht deaktivieren möchten, benötigen Sie eine HTTPS-Website.

Wenn Ihre Website in einer unsicheren (HTTP-)Domain betrieben wird, müssen Sie zulassen, dass VEC aktiven gemischten Inhalt lädt.

>[!IMPORTANT]
>
>Die Zulassung von gemischten Inhalten wirkt sich nur auf VEC und nicht auf Ihre Live-Website aus.

Weitere Informationen finden Sie unter [Gemischte Inhalte](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) auf der *Mozilla Developer Network* (MDN-)Website.

## Zulassen von gemischtem Inhalt in [!DNL Google Chrome] {#task_FF297A08F66E47A588C14FD67C037B3A}

Wenn Sie eine Site über eine sichere Verbindung besuchen, [!DNL Chrome] überprüft, ob der Inhalt auf der Webseite sicher übertragen wurde.

Siehe &quot;[Warnungen zu unsicheren Sites verwalten](https://support.google.com/chrome/answer/99020?hl=de)&quot;in der Chrome-Hilfe von Google.

Wenn Sie VEC mit der neuesten Version von [!DNL Chrome] (Version 79.0.3945.117 oder höher), müssen Sie Ihre Site-Einstellungen aktualisieren. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. Klicken Sie auf das Schlosssymbol (Achtung) und dann auf **[!UICONTROL Site-Einstellungen]**.

   ![Site-Einstellungen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scrollen Sie zu **[!UICONTROL Nicht sicherer Inhalt]** und ändern Sie dann in der Dropdown-Liste „Sperren (Standard)“ in „Zulassen“.

   ![Nicht sicherer Inhalt](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laden Sie die VEC-Seite neu.

## Zulassen von gemischtem Inhalt in [!DNL Mozilla Firefox] {#task_5448763B8DC941FD80F84041AEF0A14D}

Standardmäßig ist [!DNL Firebox] blockiert Seiten, die sichere und unsichere Inhalte mischen. Sie sollten diese Einstellung dauerhaft ändern, um [!DNL Target]. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. Geben Sie in Firefox `about:config` in die Adressleiste ein.
1. Bestätigen Sie die von [!DNL Firefox].

   ![Firefox-Warnung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Geben Sie in die Suchleiste `block_active` ein.

   ![Firefox-Einstellung „block_active“](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Doppelklicken Sie auf ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Der Wert ändert sich von „true“ zu „false“. Wenn der Wert „false“ anzeigt, sind Sie fertig.

   ![Firefox-Sicherheit](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. Starten Sie den Computer nach Änderung dieser Einstellung neu.

## Zulassen von gemischtem Inhalt in [!DNL Microsoft Edge]

Wenn Sie eine Site über eine sichere Verbindung besuchen, [!DNL Edge] überprüft, ob der Inhalt auf der Webseite sicher übertragen wurde.

Wenn Sie VEC mit der neuesten Version von [!DNL Edge]müssen Sie Ihre Site-Einstellungen aktualisieren. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. In [!DNL Edge]klicken **[!DNL Microsoft Edge]** in der Menüleiste, **[!UICONTROL Einstellungen]** Klicken Sie auf **Cookies und Site-Berechtigungen**.

1. Scrollen Sie zu **[!UICONTROL Unsicherer Inhalt]**.

1. Klicks **[!UICONTROL Unsicherer Inhalt]** Klicken Sie auf **[!UICONTROL Hinzufügen]** neben **[!UICONTROL Zulassen]**, fügen Sie die Site hinzu, auf der unsichere Inhalte zugelassen werden sollen, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

1. Laden Sie die VEC-Seite neu.
