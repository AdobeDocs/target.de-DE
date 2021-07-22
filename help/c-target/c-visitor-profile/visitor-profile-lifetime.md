---
keywords: Übersicht und Referenz
description: Erfahren Sie mehr darüber, wann ein Besucherprofil in [!DNL Adobe Target] abläuft.
title: Was ist die Lebensdauer des Besucherprofils und kann ich sie erweitern?
feature: Zielgruppen
exl-id: 70cb5e3b-ed6d-450d-8c6e-f1bfe8d26e54
source-git-commit: c19163020cdcb41a17ea6b65b5b500fadc9c7512
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 45%

---

# Lebensdauer des Besucherprofils

Standardmäßig läuft ein Besucherprofil in [!DNL Adobe Target] nach 14 Tagen Inaktivität für diesen Besucher ab. Diese Profillebensdauer kann verlängert werden.

[Wenden Sie sich an ClientCare oder Ihren Adobe-Berater](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Profillebensdauer ohne Zusatzkosten zu verlängern. Die Lebensdauer kann auf bis zu 90 Tage festgelegt werden.

Wenn Ihr Profil über den Standardwert hinaus erweitert wird, müssen Sie keine neue [!DNL Platform Web SDK]-Datei oder at.js-Datei herunterladen.

Das Ablaufdatum wird für vorhandene Profile nicht zurückgesetzt. Wenn ein früherer Besucher nicht innerhalb von 15 Tagen zurückkehrt, läuft das Profil ab. Wenn ein früherer Besucher vor Ablauf des ursprünglichen zweiwöchigen Profils zurückkehrt, wird das Profil auf die verlängerte Lebensdauer zurückgesetzt. Für alle neuen Besucherprofile wird die verlängerte Profillebensdauer festgelegt.

Im folgenden Szenario nehmen Sie an, dass eine oder beide Sites mit dem [!DNL Platform Web SDK] implementiert sind. Wenn sich beide Sites unter einem Clientcode befinden und ein Besucher beide Sites besucht, wird für das Profil die Lebensdauer der Profile festgelegt, die zuletzt besucht wurden. Angenommen, Site 1 verfügt über eine Profillebensdauer von 84 Tagen. Site 2 hat eine Lebensdauer von 14 Tagen. Wenn der Besucher Site 1 und dann Site 2 besucht, läuft das Profil des Besuchers nach 14 Tagen Inaktivität ab. Wenn der Besucher Site 1 nach dem Besuch von Site 2 besucht, läuft das Profil nach 84 Tagen Inaktivität ab.
