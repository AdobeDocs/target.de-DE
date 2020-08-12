---
keywords: global mbox;implement mbox.js;implement at.js
description: Informationen zur globalen Mbox, einem Namen, der auf den Einzelserveraufruf verweist, der oben auf jeder Webseite in Ihrer Adobe Target-Implementierung erfolgt.
title: Erläuterung der globalen Mbox
feature: null
subtopic: Getting Started
topic: Standard
uuid: d8f48c94-6487-437b-828f-f9be7da58f48
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 73%

---


# Erläuterung der globalen Mbox{#understand-the-global-mbox}

Informationen zur globalen Mbox, einem Namen, der auf den Einzelserveraufruf verweist, der oben auf jeder Webseite in Ihrer Adobe Target-Implementierung erfolgt.

Standardmäßig erhält die globale Mbox den Namen [!DNL target-global-mbox]. Sie kann für Ihr Konto bei Bedarf aber auch umbenannt werden.

Es gibt einige Unterschiede zwischen einer normalen Mbox (nicht globale Mbox) und der globalen Mbox, darunter die folgenden:

| Normale Mbox | Globale Mbox |
|--- |--- |
| Eine normale Mbox bricht um Inhalte normalerweise mit dem Tag `<DIV>` um. | Die globale Mbox ist „leer“ und bricht nicht um Inhalt um. |
| In einer normalen Mbox kann nur Inhalt einer Aktivität bereitgestellt werden. | In einer Antwort an eine globale Mbox können Inhalte mehrerer Aktivitäten bereitgestellt werden. |

Wenn mehrere Aktivitäten über die globale Mbox oder über mehrere normale Mboxes bereitgestellt werden, [bestimmt [!DNL Target] die Priorität](../../../../c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F), mit der die Aktivität (oder die Aktivitäten) einer Webseite bereitgestellt werden.

Es lassen sich zusätzliche Daten auf Seitenniveau an [!DNL Target] sowie an die globale Mbox übermitteln, indem die Funktion `targetPageParams` genutzt wird. Dies entspricht in etwa der Funktion für Mbox-Parameter. Weitere Informationen finden Sie unter [Übergeben von Parametern an eine globale Mbox](../../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).
