---
keywords: QS;Vorschau;Bookmarklet;Vorschaulinks
description: Erfahren Sie, wie Sie mit der Adobe [!DNL Target] QA-Lesezeichenliste erzwingen können, dass [!DNL Target] Sie aus dem QA-Modus entlassen.
title: Wie verwende ich die Lesezeichenliste für Aktivitäts-QA?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
TQID: 'https://experienceleague.adobe.com/kOQcdF2WgiAGkOS3rrLWfDSFTvRJX8jb-IeaahWnM0c'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0a683f6e68bb7481b9e45c91a275a46b84a1ffd8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 6%
---
# Lesezeichenliste für Aktivitäts-QA {#activity-qa-bookmarklet}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie mit der [!DNL Target]-QA-Lesezeichenliste den **[!UICONTROL Aktivitäts-QA]**-Modus beenden und Ihre Site wie einen typischen Besucher anzeigen können.

>[!ENDSHADEBOX]

Nachdem Sie eine Website im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) durchsucht haben, bleibt der QA-Modus seitenübergreifend erhalten, bis Ihre [!DNL Target] abläuft. Eine Lesezeichenliste ist ein Browser-Lesezeichen, das JavaScript ausführt. Die Lesezeichenliste für [!DNL Target]-QA erzwingt, dass [!DNL Target] Sie aus dem QA-Modus entlassen, sodass Sie nicht warten müssen, bis die Sitzung abläuft. Verwenden Sie die Version, die der auf Ihrer Site bereitgestellten at.js-Version entspricht.

>[!NOTE]
>
>Der Prozess zum Erstellen eines Bookmarklets variiert je nach Browsertyp und -version. Ziehen Sie die Hilfe Ihres Browsers in Anspruch oder suchen Sie im Internet nach bestimmten Richtungen.

## Lesezeichenliste für Aktivitäts-QA für at.js 1.*x*

Um die Lesezeichenliste für [!DNL Target]-QA zu verwenden, erstellen Sie eine Lesezeichenliste mit dem folgenden JavaScript-Code und fügen Sie sie der Lesezeichen-Symbolleiste Ihres Browsers hinzu:

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

Sie können den QA-Modus auch manuell verlassen, indem Sie eine Seite auf Ihrer Site laden, deren `at_preview_token` auf einen leeren Wert gesetzt ist. Beispiel:

`https://www.mysite.com/?at_preview_token=`

## Lesezeichenliste für Aktivitäts-QA für at.js 2.*x*

Im Gegensatz zu at.js 1.*x* unterstützt at.js 2.*x* keine Cookies von Drittanbietern. Der QA-Modus wird nur für die Erstanbieter-Domain mithilfe eines von at.js gesetzten Erstanbieter-Cookies beibehalten. Infolgedessen wird die QA-Modus-Sitzung nur auf der Client-Seite verwaltet und es werden keine QA-Modus-Cookies an [!DNL Target] gesendet.

Um die Lesezeichenliste für [!DNL Target]-QA zu verwenden, erstellen Sie eine Lesezeichenliste mit dem folgenden JavaScript-Code und fügen Sie sie der Lesezeichen-Symbolleiste Ihres Browsers hinzu:

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

Nachdem Sie die Lesezeichenliste, die Ihrer at.js-Version entspricht, zu Ihrem Browser hinzugefügt haben, verwenden Sie sie, wenn Sie den QA-Modus verlassen möchten:

1. Öffnen Sie eine beliebige Seite Ihrer Site, während Sie sich im QA-Modus befinden.
1. Klicken Sie in der Symbolleiste „Lesezeichen“ Ihres Browsers auf die Lesezeichenliste.
1. Laden Sie eine Seite Ihrer Site. [!DNL Target] wird die Sitzung aus dem QA-Modus freigegeben, und die Site wird so angezeigt wie für einen typischen Besucher.
