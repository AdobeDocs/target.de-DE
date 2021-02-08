---
keywords: Übersicht und Referenz
description: Erfahren Sie mehr darüber, wann ein Besucher-Profil in Adobe Target abläuft (standardmäßig 14 Tage). Die Lebensdauer des Profils kann verlängert werden, indem Sie sich an den Kundendienst von Adobe wenden.
title: Was ist das Besucher Profil Lifetime und kann ich es erweitern?
feature: Audiences
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 73%

---


# Lebensdauer des Besucherprofils{#visitor-profile-lifetime}

Standardmäßig läuft ein Besucherprofil nach 14 Tagen Inaktivität für diesen Besucher ab. Diese Profillebensdauer kann verlängert werden.

[Wenden Sie sich an ClientCare oder Ihren Adobe-Berater](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Profillebensdauer ohne Zusatzkosten zu verlängern. Die Lebensdauer kann auf bis zu 90 Tage festgelegt werden.

Anhand der verwendeten [!DNL Target] JavaScript-Bibliothek ([!DNL at.js] oder [!DNL mbox.js]) wird bestimmt, ob Sie eine neue Datei herunterladen müssen oder nicht:

| Ziel-Bibliothek | Details |
|--- |--- |
| at.js | Wenn Ihr Profil über den Standardwert hinaus verlängert wird, müssen Sie keine neue at.js-Datei herunterladen. |
| mbox.js | Wenn Ihr Profil über den Standardwert von 14 Tagen hinaus verlängert wird, müssen Sie eine neue mbox.js-Datei herunterladen, nachdem Ihr Berater oder ClientCare Ihre Einstellungen geändert hat. Die Cookie-Verlängerung zur Unterstützung der geänderten Profillebensdauer ist in der aktualisierten mbox.js-Datei enthalten. Nachdem Sie mit der Verwendung der neuen Bibliothek begonnen haben, werden die Profillebensdauerdaten der Besucher aktualisiert. |

Das Ablaufdatum wird für vorhandene Profile nicht zurückgesetzt. Wenn ein früherer Besucher nicht innerhalb von 15 Tagen zurückkehrt, läuft das Profil ab. Wenn ein früherer Besucher vor Ablauf des ursprünglichen zweiwöchigen Profils zurückkehrt, wird das Profil auf die verlängerte Lebensdauer zurückgesetzt. Für alle neuen Besucherprofile wird die verlängerte Profillebensdauer festgelegt.

Gehen Sie im folgenden Szenario davon aus, dass eine oder beide Sites mit &quot;mbox.js&quot;implementiert sind. Dies erfordert eine Codeaktualisierung, nachdem das Profil aktualisiert wurde. Wenn sich beide Sites unter einem Clientcode befinden und ein Besucher beide Sites besucht, wird das Profil auf die Lebensdauer der Profil auf der jeweiligen Site eingestellt, die zuletzt besucht wurde. Wenn z. B. Site 1 eine Profillebensdauer von 84 Tagen und Site 2 eine Profillebensdauer von 14 Tagen hat und der Besucher zuerst Site 1 und dann Site 2 besucht, läuft das Profil des Besuchers nach 14 Tagen Inaktivität ab. Wenn der Besucher Site 1 nach dem Besuch von Site 2 besucht, läuft das Profil nach 84 Tagen Inaktivität ab.
