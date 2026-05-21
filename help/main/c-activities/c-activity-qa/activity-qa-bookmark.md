---
keywords: QS;Vorschau;Bookmarklet;Vorschaulinks
description: Erfahren Sie, wie Sie die Lesezeichenliste für Adobe [!DNL Target] QA verwenden, um  [!DNL Target]  Veröffentlichung aus dem QA-Modus zu erzwingen.
title: Wie verwende ich die Lesezeichenliste für Aktivitäts-QA?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
TQID: https://experienceleague.adobe.com/kOQcdF2WgiAGkOS3rrLWfDSFTvRJX8jb-IeaahWnM0c
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 12%

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

Im Gegensatz zu at.js 1.*x* unterstützt at.js 2.*x* keine Drittanbieter-Cookies, und der QA-Modus bleibt nur für die Erstanbieter-Domain erhalten (mithilfe eines von at.js gesetzten Erstanbieter-Cookies). Daher wird in at.js 2.*x* die QA-Modus-Sitzung nur auf der Client-Seite verwaltet und es werden keine QA-Modus-Cookies an Target gesendet.

Um die Lesezeichenliste für [!DNL Target]-QA zu verwenden, erstellen Sie eine Lesezeichenliste mit dem folgenden JavaScript-Code und fügen Sie sie zur Lesezeichen-Symbolleiste Ihres Browsers hinzu:

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {            
            document.cookie = AT_QA_MODE + ';domain='+window.location.hostname+";Path=/; Max-Age=-0;";
            var token = window.location.href.indexOf("?at_preview_token")<0? "&at_preview_token" : "?at_preview_token";
            var url = window.location.href.split(token,2)[0];
            window.open(url, '_self', 'noreferrer');
        }
    })(); 
```

## Lesezeichenliste für Aktivitäts-QA verwenden

Klicken Sie in der Symbolleiste Ihres Browsers auf das Lesezeichen.
