---
keywords: qa;preview;bookmarklet;preview links
description: Informationen, die Sie bei der Verwendung des Adobe Target QA-Bookmarklets unterstützen, um die Zielgruppe zu erzwingen, Sie aus dem QA-Modus zu entfernen.
title: Aktivität QA Bookmarklet für Adobe Target
feature: qa
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: 620bb6dfbe160cf27ef5de9199c3d91fb806f316
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 11%

---


# Lesezeichenliste für Aktivitäts-QA{#activity-qa-bookmarklet}

Information to help you use the [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.

>[!NOTE]
>
>Der Prozess zum Erstellen eines Bookmarklets variiert je nach Browsertyp und -version. Schauen Sie in den Hilfe-Seiten Ihres Browsers nach oder suchen Sie im Internet nach genauen Anweisungen.

## Aktivität QA Bookmarklet for at.js 1.*x* 

Because [QA mode](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. Use the QA [!DNL Target] bookmarklet to force yourself out of QA mode.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser&#39;s Bookmarks Toolbar:

```
javascript:(
    function () {
        if (window.location.href.indexOf('?') != -1) {
            var parts = window.location.href.split('at_preview_token',2);
            if (parts.length > 1) {
                window.location.href = parts[0].concat('at_preview_token=');
            } else {
                window.location.href = window.location.href.concat("&at_preview_token=")
            }
        } else {
            window.location.href = window.location.href.concat("?at_preview_token=")
        }
    }
)();
```

## Aktivität QA Bookmarklet for at.js 2.*x* 

Im Gegensatz zu at.js 1.*x*, at.js 2.*x* unterstützt keine Drittanbieter-Cookies, und der QS-Modus ist nur für die Erstanbieterdomäne fixierbar (durch ein Erstanbieter-Cookie, das von at.js gesetzt wird). Daher in at.js 2.*x*, die QS-Modus-Sitzung wird nur clientseitig verwaltet und keine Cookies im QS-Modus werden an die Zielgruppe gesendet.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser&#39;s Bookmarks Toolbar:

```
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {
            document.cookie = AT_QA_MODE + '; Max-Age=-99999999;';
            var url = window.location.href.split('at_preview_token',2)[0];
            window.location.href = url.substring(0, url.length - 1);
        }
    })();
```

## Verwenden des Aktivität QA-Bookmarklets

Klicken Sie in der Symbolleiste Ihres Browsers auf das Lesezeichen.

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value.

Beispiel:

`https://www.mysite.com/?at_preview_token=`
