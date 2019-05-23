---
description: Informationen, die Ihnen bei der Verwendung der Target QA-Lesezeichenliste helfen, damit Target zum Freigeben aus dem QA-Modus gezwungen wird.
keywords: QS;Vorschau;Bookmarklet;Vorschaulinks
seo-description: Informationen, die Ihnen bei der Verwendung der Target QA-Lesezeichenliste helfen, damit Target zum Freigeben aus dem QA-Modus gezwungen wird.
seo-title: Lesezeichenliste für Aktivitäts-QA
solution: Target
title: Lesezeichenliste für Aktivitäts-QA
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: af3e1d9c6db4733b6eb37f8232b164be65c4dd2e

---


# Lesezeichenliste für Aktivitäts-QA{#activity-qa-bookmarklet}

Informationen, die Ihnen bei der Verwendung der Target QA-Lesezeichenliste helfen, damit Target zum Freigeben aus dem QA-Modus gezwungen wird.

Da der [QS-Modus](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) nach dem Website-Browsen im QS-Modus hängt, muss die Target-Sitzung ablaufen oder Target muss Sie aus dem QS-Modus freigeben, bevor Sie Ihre Website wie ein normaler Besucher anzeigen können. Verwenden Sie die QA Target-Lesezeichenliste, um Ihre Freigabe aus dem QA-Modus selbst zu erzwingen.

Um das QS-Bookmarklet von Target zu verwenden, erstellen Sie ein Bookmarklet mit folgendem JavaScript-Code und fügen Sie es der Lesezeichensymbolleiste Ihres Browsers hinzu:

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

Sie können sich auch manuell selbst aus dem QS-Modus lösen, indem Sie auf Ihrer Site eine Seite laden, wobei der Parameter `at_preview_token` einen leeren Wert hat (beispielsweise `https://www.mysite.com/?at_preview_token=`).
