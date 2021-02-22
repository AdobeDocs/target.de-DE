---
keywords: gemischte Inhalte;sicher;unsicher;Chrom;Fehlerbehebung;vec;Visual Experience Composer;unsecure;http;https;firefox;Internet Explorer
description: Einige Browser blockieren die Anzeige einer Seite, wenn sicherer Inhalt mit unsicherem Inhalt gemischt wird. Erfahren Sie, wie Sie gemischte Inhalte in Chrome, Firefox und Edge aktivieren.
title: Wie aktiviere ich gemischte Inhalte in meinem Browser?
feature: 'Visual Experience Composer (VEC) '
translation-type: tm+mt
source-git-commit: 453106f7534f83c205722421bbf00044fde7da67
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 26%

---


# Zulassen von gemischtem Inhalt in Ihrem Browser

Gemischte Inhalte treten auf, wenn die ursprüngliche Anforderung über HTTPS sicher ist, aber HTTPS *und* HTTP-Inhalt geladen wird, um die Webseite anzuzeigen. HTTPS-Inhalte sind sicher. HTTP-Inhalte sind unsicher.

Moderne Browser können die Anzeige einer Seite oder Warnmeldungen blockieren, wenn sicherer Inhalt mit unsicherem Inhalt gemischt wird.

Eine Warnmeldung wird angezeigt, wenn der [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] versucht, eine Seite mit gemischtem Inhalt zu öffnen. Diese Meldung informiert Sie darüber, wie Sie die Blockierung in Ihrem Browser deaktivieren können. Durch Deaktivieren der Blockierung können Sie eine HTTP-Site oder eine Site mit gemischten Aufrufen (HTTPS und HTTP) öffnen.

![Warnung zu gemischten Inhalten](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Zuvor konnten Sie, falls gemischte Inhalte unzulässig waren, in Schritt 1 des dreistufigen geführten Workflows beim Erstellen von Aktivitäten dennoch einige Aktionen ausführen. [!DNL Target]Von nun an blockiert Aktionen in Schritt 1. Wenn diese Meldung angezeigt wird, müssen Sie gemischte Inhalte aktivieren, bevor Sie mit der Erstellung der Aktivität fortfahren können.

Die Sicherheitseinstellungen Ihres Browsers verhindern möglicherweise, dass gemischter Inhalt oder unsicherer (HTTP-)Inhalt auf einer sicheren (HTTPS-)Seite oder in einem sicheren Frame (z. B. VEC) geladen wird. Wenn Sie die Sicherheitseinstellungen Ihres Browsers nicht deaktivieren möchten, benötigen Sie eine HTTPS-Website.

Wenn Ihre Website auf einer unsicheren (HTTP) Domäne ausgeführt wird, müssen Sie zulassen, dass VEC aktive gemischte Inhalte lädt.

>[!NOTE]
>
>Die Zulassung von gemischten Inhalten wirkt sich nur auf VEC und nicht auf Ihre Live-Website aus.

Weitere Informationen finden Sie unter [Gemischte Inhalte](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) auf der *Mozilla-Entwicklernetzwerk* (MDN-)Website.

## Aktivieren von gemischten Inhalten in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Wenn Sie eine Site über eine sichere Verbindung besuchen, prüft Chrome, ob der Inhalt auf der Webseite sicher übertragen wurde.

Siehe &quot;[Diese Seite enthält unsicheren Inhalt](https://support.google.com/chrome/answer/1342714?hl=en)&quot;in der Google Chrome-Hilfe.

Wenn Sie VEC mit der neuesten Version von Chrome (Version 79.0.3945.117 oder höher) verwenden, müssen Sie Ihre Site-Einstellungen aktualisieren. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. Klicken Sie auf das Symbol Sperren (Vorsicht) und dann auf **[!UICONTROL Site-Einstellungen]**.

   ![Site-Einstellungen](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Blättern Sie zu **[!UICONTROL Unsicherer Inhalt]** und verwenden Sie dann die Dropdown-Liste, um &quot;Block (Standard)&quot;in &quot;Allow&quot;zu ändern.

   ![Unsicherer Inhalt](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laden Sie die VEC-Seite neu.

## Zulassen von gemischtem Inhalt in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Firefox blockiert standardmäßig Seiten, auf denen sicherer und unsicherer Inhalt gemischt ist. Es wird empfohlen, zur Verwendung von [!DNL Target] diese Einstellung dauerhaft zu ändern. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. Geben Sie in Firefox `about:config` in die Adressleiste ein.
1. Quittieren Sie die in Firefox angezeigte Warnmeldung.

   ![Firefox-Warnung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Geben Sie in die Suchleiste `block_active` ein.

   ![Einstellung &quot;Firefox block_active&quot;](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Doppelklicken Sie auf ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Der Wert ändert sich von „true“ zu „false“. Wenn der Wert „false“ anzeigt, sind Sie fertig.

   ![Firefox-Sicherheit](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

Starten Sie den Computer nach dem Ändern dieser Einstellung neu.

## Zulassen von gemischten Inhalten in Microsoft Edge

Wenn Sie eine Site über eine sichere Verbindung besuchen, prüft Edge, ob der Inhalt auf der Webseite sicher übertragen wurde.

Wenn Sie den VEC mit der neuesten Version von Edge verwenden, müssen Sie Ihre Site-Einstellungen aktualisieren. Besucher Ihrer Site müssen diese Schritte nicht ausführen.

1. Klicken Sie auf das Symbol Sperren (Vorsicht) und dann auf **[!UICONTROL Site-Berechtigungen]**.

   ![Site-Berechtigungen in Microsoft Edge](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. Blättern Sie zu **[!UICONTROL Unsicherer Inhalt]** und verwenden Sie dann die Dropdown-Liste, um &quot;Block (Standard)&quot;in &quot;Allow&quot;zu ändern.

   ![Unsicherer Inhalt](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. Laden Sie die VEC-Seite neu.