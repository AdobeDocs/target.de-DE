---
keywords: QS;Vorschau;Bookmarklet;Vorschaulinks
description: Erfahren Sie, wie Sie die Adobe [!DNL Target] QA-Lesezeichenliste verwenden, um die  [!DNL Target]  von QA-Modus zu erzwingen.
title: Wie verwende ich die Lesezeichenliste für Aktivitäts-QA?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 13%

---

# Lesezeichenliste für Aktivitäts-QA

Informationen, die Sie bei der Verwendung der [!DNL Target]-QA-Lesezeichenliste unterstützen, um zu erzwingen, dass [!DNL Target] Sie aus dem QA-Modus entlassen.

>[!NOTE]
>
>Der Prozess zum Erstellen eines Bookmarklets variiert je nach Browsertyp und -version. Schauen Sie in den Hilfe-Seiten Ihres Browsers nach oder suchen Sie im Internet nach genauen Anweisungen.

## Lesezeichenliste für Aktivitäts-QA für at.js 1.*x*  

Da [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) beibehalten wird, muss Ihre [!DNL Target]-Sitzung nach dem Durchsuchen einer Website im QA-Modus ablaufen, oder Sie müssen [!DNL Target] aus dem QA-Modus entlassen, bevor Sie Ihre Website wie einen typischen Besucher anzeigen können. Verwenden Sie die Lesezeichenliste für QA-[!DNL Target], um den QA-Modus zu deaktivieren.

Um die Lesezeichenliste für [!DNL Target]-QA zu verwenden, erstellen Sie eine Lesezeichenliste mit dem folgenden JavaScript-Code und fügen Sie sie zur Lesezeichen-Symbolleiste Ihres Browsers hinzu:

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

Sie können den QA-Modus auch manuell deaktivieren, indem Sie eine Seite Ihrer Site mit einem leeren Wert im `at_preview_token`-Parameter laden.

Beispiel:

`https://www.mysite.com/?at_preview_token=`

## Lesezeichenliste für Aktivitäts-QA für at.js 2.*x*  

Im Gegensatz zu at.js 1.*x*, at.js 2.*x* unterstützt keine Third-Party-Cookies, und der QA-Modus bleibt nur für die First-Party-Domain bestehen (mithilfe eines First-Party-Cookies, das von at.js gesetzt wird). Daher in at.js 2.*x* wird die QA-Modus-Sitzung nur Client-seitig verwaltet und es werden keine QA-Modus-Cookies an Target gesendet.

Um die Lesezeichenliste für [!DNL Target]-QA zu verwenden, erstellen Sie eine Lesezeichenliste mit dem folgenden JavaScript-Code und fügen Sie sie zur Lesezeichen-Symbolleiste Ihres Browsers hinzu:

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

## Lesezeichenliste für Aktivitäts-QA verwenden

Klicken Sie in der Symbolleiste Ihres Browsers auf das Lesezeichen.
