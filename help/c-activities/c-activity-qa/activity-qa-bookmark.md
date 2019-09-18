---
description: Informationen, die Sie bei der Verwendung des Adobe Target-QA-Bookmarklets unterstützen, um Target zu zwingen, Sie aus dem Qualitätssicherungs-Modus zu entfernen.
keywords: QS;Vorschau;Bookmarklet;Vorschaulinks
seo-description: Informationen, die Sie bei der Verwendung des Adobe Target-QA-Bookmarklets unterstützen, um Target zu zwingen, Sie aus dem Qualitätssicherungs-Modus zu entfernen.
seo-title: Activity QA-Bookmarklet für Adobe Target
solution: Target
title: Lesezeichenliste für Aktivitäts-QA
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: 1df7fbf78f9e20d8a907809b228ed591036c1a24

---


# Lesezeichenliste für Aktivitäts-QA{#activity-qa-bookmarklet}

Information to help you use the [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.

Because [QA mode](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. Use the QA [!DNL Target] bookmarklet to force yourself out of QA mode.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser's Bookmarks Toolbar:

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

Anschließend sollte die Lesezeichenliste für die erneute Verwendung in der Symbolleiste angezeigt werden.

>[!NOTE]
>
>Der Prozess zum Erstellen eines Bookmarklets variiert je nach Browsertyp und -version. Schauen Sie in den Hilfe-Seiten Ihres Browsers nach oder suchen Sie im Internet nach genauen Anweisungen.

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value.

Beispiel:

`https://www.mysite.com/?at_preview_token=`
