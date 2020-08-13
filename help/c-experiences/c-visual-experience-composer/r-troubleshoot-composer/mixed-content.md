---
keywords: mixed content;secure;insecure;chrome;troubleshooting;vec;visual experience composer;unsecure;http;https;firefox;internet explorer
description: Einige Browser blockieren die Anzeige einer Seite, wenn sicherer Inhalt mit unsicherem Inhalt gemischt wird.
title: Enabling mixed content in your browser
feature: vec
topic: Advanced,Standard,Classic
uuid: 6944ce97-ff73-4b61-b006-35862ff83ef1
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 35%

---


# Enabling mixed content in your browser{#enabling-mixed-content-in-your-browser}

Gemischte Inhalte treten auf, wenn sowohl HTTPS- (sicherer) *als auch* HTTP- (unsicherer) Inhalte geladen werden, um dieselbe Webseite anzuzeigen, und die ursprüngliche Anforderung über HTTPS gesichert war.

Moderne Browser können die Anzeige einer Seite oder Warnmeldungen blockieren, wenn sicherer Inhalt mit unsicherem Inhalt gemischt wird.

If the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] tries to open a page containing mixed content, a message displays showing how to disable blocking in your browser so you can open an HTTP site or a site that has mixed calls (HTTPS and HTTP).

![Warnung zu gemischten Inhalten](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Zuvor konnten Sie, falls gemischte Inhalte unzulässig waren, in Schritt 1 des dreistufigen geführten Workflows beim Erstellen von Aktivitäten dennoch einige Aktionen ausführen. [!DNL Target]Von nun an blockiert Aktionen in Schritt 1. Wenn diese Meldung angezeigt wird, müssen Sie gemischte Inhalte aktivieren, bevor Sie mit der Erstellung der Aktivität fortfahren können.

Die Sicherheitseinstellungen Ihres Browsers verhindern möglicherweise, dass gemischter Inhalt oder unsicherer (HTTP-)Inhalt auf einer sicheren (HTTPS-)Seite oder in einem sicheren Frame (z. B. VEC) geladen wird. Wenn Sie die Sicherheitseinstellungen Ihres Browsers nicht deaktivieren möchten, benötigen Sie eine HTTPS-Website.

Wenn Ihre Website in einer unsicheren (HTTP-)Domäne betrieben wird, müssen Sie zulassen, dass VEC aktiven gemischten Inhalt lädt.

>[!NOTE]
>
>Die Zulassung von gemischten Inhalten wirkt sich nur auf VEC und nicht auf Ihre Live-Website aus.

Weitere Informationen finden Sie unter [Gemischte Inhalte](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) auf der *Mozilla-Entwicklernetzwerk* (MDN-)Website.

## Enabling mixed content in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Wenn Sie eine Site über eine sichere Verbindung besuchen, prüft Chrome, ob der Inhalt auf der Webseite sicher übertragen wurde.

Siehe [Diese Seite enthält unsichere Inhalte](https://support.google.com/chrome/answer/1342714?hl=en) in der Google Chrome-Hilfe.

Wenn Sie VEC mit der neuesten Version von Chrome (Version 79.0.3945.117 oder höher) verwenden, müssen Sie Ihre Site-Einstellungen aktualisieren. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. Klicken Sie auf das Sperren- oder Warnsymbol und dann auf **[!UICONTROL Site-Einstellungen]**.

   ![Site-Einstellungen](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Blättern Sie zu **[!UICONTROL Unsicheren Inhalten]** und verwenden Sie dann die Dropdown-Liste, um &quot;Blockieren (Standard)&quot;in &quot;Zulassen&quot;zu ändern.

   ![Insecure content](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laden Sie die VEC-Seite neu.

## Enabling mixed content in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Firefox blockiert standardmäßig Seiten, auf denen sicherer und unsicherer Inhalt gemischt ist. Es wird empfohlen, zur Verwendung von [!DNL Target] diese Einstellung dauerhaft zu ändern. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. Geben Sie in Firefox `about:config` in die Adressleiste ein.
1. Quittieren Sie die in Firefox angezeigte Warnmeldung.

   ![Firefox warning](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Geben Sie in die Suchleiste `block_active` ein.

   ![Firefox block active setting](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Doppelklicken Sie auf ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Der Wert ändert sich von „true“ zu „false“. Wenn der Wert „false“ anzeigt, sind Sie fertig.

   ![Firefox security](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

We recommended that you restart your computer after changing this setting.

## Enabling mixed content in Microsoft Edge

Wenn Sie eine Site über eine sichere Verbindung besuchen, prüft Edge, ob der Inhalt auf der Webseite sicher übertragen wurde.

If you are using the VEC with the latest version of Edge, you need to update your site settings. Visitors to your site do not need to complete these steps.

1. Click the lock or caution icon, then click **[!UICONTROL Site Permissions]**.

   ![Site-Berechtigungen in Microsoft Edge](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. Blättern Sie zu **[!UICONTROL Unsicheren Inhalten]** und verwenden Sie dann die Dropdown-Liste, um &quot;Blockieren (Standard)&quot;in &quot;Zulassen&quot;zu ändern.

   ![Insecure content](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. Reload the VEC page.