---
keywords: qa;preview;bookmarklet;preview links
description: Informationen, die Sie bei der Verwendung des Adobe Target QA-Bookmarklets unterstützen, um die Zielgruppe zu erzwingen, Sie aus dem QA-Modus zu entfernen.
title: Aktivität QA Bookmarklet für Adobe Target
feature: qa
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 11%

---


# Lesezeichenliste für Aktivitäts-QA{#activity-qa-bookmarklet}

Informationen, die Sie bei der Verwendung des [!DNL Target] QA-Bookmarklets unterstützen, damit [!DNL Target] erzwungen wird, Sie aus dem QA-Modus zu entfernen.

>[!NOTE]
>
>Der Prozess zum Erstellen eines Bookmarklets variiert je nach Browsertyp und -version. Schauen Sie in den Hilfe-Seiten Ihres Browsers nach oder suchen Sie im Internet nach genauen Anweisungen.

## Aktivität QA Bookmarklet for at.js 1.*x* 

Da [QS-Modus](/help/c-activities/c-activity-qa/activity-qa.md) fixierbar ist, muss nach dem Durchsuchen einer Website im QA-Modus Ihre [!DNL Target] Sitzung ablaufen oder Sie müssen [!DNL Target] aus dem QS-Modus freigeben, bevor Sie Ihre Site wie ein typischer Besucher Ansicht haben können. Verwenden Sie das QA [!DNL Target]-Lesezeichen, um sich aus dem QA-Modus zu drängen.

Um das [!DNL Target] QA-Lesezeichen zu verwenden, erstellen Sie ein Lesezeichen mit dem folgenden JavaScript-Code und fügen Sie es der Lesezeichenleiste Ihres Browsers hinzu:

```javascript
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

Sie können sich auch manuell aus dem QS-Modus verdrängen, indem Sie eine Seite mit dem Parameter `at_preview_token` mit einem leeren Wert auf Ihrer Site laden.

Beispiel:

`https://www.mysite.com/?at_preview_token=`

## Aktivität QA Bookmarklet for at.js 2.*x* 

Im Gegensatz zu at.js 1.*x*, at.js 2.*Drittanbieter-Cookies werden von* xdoes nicht unterstützt, und der QS-Modus ist nur für die Erstanbieterdomäne fixierbar (durch ein Erstanbieter-Cookie, das von at.js gesetzt wird). Daher in at.js 2.*x*, die QS-Modus-Sitzung wird nur clientseitig verwaltet und keine Cookies im QS-Modus werden an die Zielgruppe gesendet.

Um das [!DNL Target] QA-Lesezeichen zu verwenden, erstellen Sie ein Lesezeichen mit dem folgenden JavaScript-Code und fügen Sie es der Lesezeichenleiste Ihres Browsers hinzu:

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {
            document.cookie = AT_QA_MODE + '; Path=/; Max-Age=-0;';
            var url = window.location.href.split('at_preview_token',2)[0];
            window.open(url.substring(0, url.length - 1), '_self', 'noreferrer');
        }
    })();
```

## Verwenden des Aktivität QA-Bookmarklets

Klicken Sie in der Symbolleiste Ihres Browsers auf das Lesezeichen.

