---
keywords: QS;Vorschau;Bookmarklet;Vorschaulinks
description: Erfahren Sie, wie Sie mit dem Adobe [!DNL Target] QA-Bookmarklet erzwingen können, dass [!DNL Target] Sie aus dem QA-Modus freigeben.
title: Wie verwende ich das Lesezeichen für Aktivitäts-QA?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 13%

---

# Lesezeichenliste für Aktivitäts-QA

Informationen, die Sie bei der Verwendung des [!DNL Target] QA-Bookmarklets unterstützen, um [!DNL Target] zu zwingen, Sie aus dem QA-Modus freizugeben.

>[!NOTE]
>
>Der Prozess zum Erstellen eines Bookmarklets variiert je nach Browsertyp und -version. Schauen Sie in den Hilfe-Seiten Ihres Browsers nach oder suchen Sie im Internet nach genauen Anweisungen.

## Lesezeichenliste für Aktivitäts-QA für at.js 1.*x*  

Da der [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) hängt, muss nach dem Durchsuchen einer Website im QA-Modus Ihre [!DNL Target] Sitzung ablaufen oder Sie müssen [!DNL Target] aus dem QA-Modus freigeben, bevor Sie Ihre Site wie ein normaler Besucher anzeigen können. Verwenden Sie das QS [!DNL Target]-Lesezeichen, um das Beenden des QS-Modus zu erzwingen.

Um das QS-Bookmarklet [!DNL Target] zu verwenden, erstellen Sie ein Lesezeichen mit dem folgenden JavaScript-Code und fügen Sie es der Lesezeichensymbolleiste Ihres Browsers hinzu:

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

Sie können sich auch manuell selbst aus dem QA-Modus lösen, indem Sie eine Seite auf Ihrer Site mit dem Parameter `at_preview_token` mit einem leeren Wert laden.

Beispiel:

`https://www.mysite.com/?at_preview_token=`

## Lesezeichenliste für Aktivitäts-QA für at.js 2.*x*  

Im Gegensatz zu at.js 1.*x*, at.js 2.*x* unterstützt keine Drittanbieter-Cookies, und der QA-Modus hängt nur für die Erstanbieter-Domäne an (mithilfe eines Erstanbieter-Cookies, das von at.js gesetzt wird). Daher in at.js 2.*x*: Die Sitzung im QS-Modus wird nur clientseitig verwaltet und es werden keine Cookies im QS-Modus an Target gesendet.

Um das QS-Bookmarklet [!DNL Target] zu verwenden, erstellen Sie ein Lesezeichen mit dem folgenden JavaScript-Code und fügen Sie es der Lesezeichensymbolleiste Ihres Browsers hinzu:

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

## Verwenden des Lesezeichens für Aktivitäts-QA

Klicken Sie in der Symbolleiste Ihres Browsers auf das Lesezeichen.
