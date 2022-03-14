---
keywords: globale Mbox; Implementierung von at.js
description: Erfahren Sie mehr über die globale Mbox in Adobe Target, eine Bezeichnung für einen einzelnen Server-Aufruf, der oben auf jeder Webseite in Ihrer [!DNL Target] Implementierung.
title: Was ist eine globale Mbox?
feature: at.js
role: Developer
exl-id: 84d15feb-f5df-4879-ae35-a7f455c1b20f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 82%

---

# Erläuterung der globalen Mbox

Informationen über die globale mbox, eine Bezeichnung für einen einzelnen Server-Aufruf, der oben auf jeder Webseite der [!DNL Adobe Target]-Implementierung durchgeführt wird.

Standardmäßig erhält die globale Mbox den Namen `target-global-mbox`. Sie kann für Ihr Konto bei Bedarf aber auch umbenannt werden.

Es gibt einige Unterschiede zwischen einer normalen Mbox (nicht globale Mbox) und der globalen Mbox, darunter die folgenden:

| Normale Mbox | Globale Mbox |
|--- |--- |
| Eine normale Mbox bricht um Inhalte normalerweise mit dem Tag `<DIV>` um. | Die globale Mbox ist „leer“ und bricht nicht um Inhalt um. |
| In einer normalen Mbox kann nur Inhalt einer Aktivität bereitgestellt werden. | In einer Antwort an eine globale Mbox können Inhalte mehrerer Aktivitäten bereitgestellt werden. |

Wenn mehrere Aktivitäten über die globale Mbox oder über mehrere normale Mboxes bereitgestellt werden, [bestimmt [!DNL Target] die Priorität](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F), mit der die Aktivität (oder die Aktivitäten) einer Webseite bereitgestellt werden.

Es lassen sich zusätzliche Daten auf Seitenniveau an [!DNL Target] sowie an die globale Mbox übermitteln, indem die Funktion `targetPageParams` genutzt wird. Dies entspricht in etwa der Funktion für Mbox-Parameter. Weitere Informationen finden Sie unter [Übergeben von Parametern an eine globale Mbox](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).
