---
keywords: Overview and Reference
description: Standardmäßig werden Besucherprofile 14 Tage lang gespeichert. Diese Profillebensdauer kann verlängert werden.
title: Lebensdauer des Besucherprofils
feature: visitor profiles
subtopic: Getting Started
topic: Standard
uuid: 01ccda60-7e28-4d26-8d5d-1c0a022bbef0
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%

---


# Lebensdauer des Besucherprofils{#visitor-profile-lifetime}

Standardmäßig läuft ein Besucherprofil nach 14 Tagen Inaktivität für diesen Besucher ab. Diese Profillebensdauer kann verlängert werden.

[Wenden Sie sich an ClientCare oder Ihren Adobe-Berater](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Profillebensdauer ohne Zusatzkosten zu verlängern. Die Lebensdauer kann auf bis zu 90 Tage festgelegt werden.

Anhand der verwendeten [!DNL Target] JavaScript-Bibliothek ([!DNL at.js] oder [!DNL mbox.js]) wird bestimmt, ob Sie eine neue Datei herunterladen müssen oder nicht:

| Ziel-Bibliothek | Details |
|--- |--- |
| at.js | Wenn Ihr Profil über den Standardwert hinaus verlängert wird, müssen Sie keine neue at.js-Datei herunterladen. |
| mbox.js | Wenn Ihr Profil über den Standardwert von 14 Tagen hinaus verlängert wird, müssen Sie eine neue mbox.js-Datei herunterladen, nachdem Ihr Berater oder ClientCare Ihre Einstellungen geändert hat. Die Cookie-Verlängerung zur Unterstützung der geänderten Profillebensdauer ist in der aktualisierten mbox.js-Datei enthalten. Nachdem Sie mit der Verwendung der neuen Bibliothek begonnen haben, werden die Profillebensdauerdaten der Besucher aktualisiert. |

Das Ablaufdatum wird für vorhandene Profile nicht zurückgesetzt. Wenn ein früherer Besucher nicht innerhalb von 15 Tagen zurückkehrt, läuft das Profil ab. Wenn ein früherer Besucher vor Ablauf des ursprünglichen zweiwöchigen Profils zurückkehrt, wird das Profil auf die verlängerte Lebensdauer zurückgesetzt. Für alle neuen Besucherprofile wird die verlängerte Profillebensdauer festgelegt.

Wenn Sie zwei Sites unter einem Kundencode haben und ein Besucher beide Seiten besucht, wird für das Profil die Profillebensdauer der Site festgelegt, die zuletzt besucht wurde. Wenn z. B. Site 1 eine Profillebensdauer von 84 Tagen und Site 2 eine Profillebensdauer von 14 Tagen hat und der Besucher zuerst Site 1 und dann Site 2 besucht, läuft das Profil des Besuchers nach 14 Tagen Inaktivität ab. Wenn der Besucher Site 1 nach dem Besuch von Site 2 besucht, läuft das Profil nach 84 Tagen Inaktivität ab.
