---
description: Standardmäßig werden Besucherprofile 14 Tage lang gespeichert. Diese Profillebensdauer kann verlängert werden.
keywords: Übersicht und Referenz
seo-description: Standardmäßig werden Besucherprofile 14 Tage lang gespeichert. Diese Profillebensdauer kann verlängert werden.
seo-title: Lebensdauer des Besucherprofils
solution: Target
subtopic: Erste Schritte
title: Lebensdauer des Besucherprofils
topic: Standard
uuid: 01ccda60-7e28-4d26-8d5d-1c0a022bbef0
translation-type: tm+mt
source-git-commit: 745eb38b18ce7b29d87abb588ecdbb3fffc8cfc1

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

Wenn Sie zwei Sites unter einem Kundencode haben und ein Besucher beide Seiten besucht, wird für das Profil die Profillebensdauer der Site festgelegt, die zuletzt besucht wurde. Wenn beispielsweise Site 1 eine Profillebensdauer von 84 Tagen aufweist und Site 2 eine 14-Tage-Lebensdauer hat und der Besucher Site 1 und dann Site 2 besucht, läuft das Profil des Besuchers in 14 Tagen nach Inaktivität ab. Wenn der Besucher Site 1 nach Besuch von Site 2 besucht, läuft das Profil in 84 Tagen nach Inaktivität ab.
