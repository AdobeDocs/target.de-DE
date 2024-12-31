---
keywords: Übersicht und Referenz
description: Erfahren Sie mehr darüber, wann ein Besucherprofil in  [!DNL Adobe Target] abläuft.
title: Was ist die Lebensdauer des Besucherprofils und kann ich sie verlängern?
feature: Audiences
exl-id: 70cb5e3b-ed6d-450d-8c6e-f1bfe8d26e54
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 62%

---

# Lebensdauer des Besucherprofils

Standardmäßig läuft ein Besucherprofil in [!DNL Adobe Target] nach 14 Tagen Inaktivität für diesen Besucher ab. Diese Profillebensdauer kann verlängert werden.

[Wenden Sie sich an ClientCare oder Ihren Adobe-Berater](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um die Profillebensdauer ohne Zusatzkosten zu verlängern. Die Lebensdauer kann auf bis zu 90 Tage festgelegt werden.

Sie müssen keine neue [!DNL Platform Web SDK]- oder at.js-Datei herunterladen, wenn Ihr Profil über das Standardprofil hinaus erweitert wird.

Das Ablaufdatum wird für vorhandene Profile nicht zurückgesetzt. Wenn ein früherer Besucher nicht innerhalb von 15 Tagen zurückkehrt, läuft das Profil ab. Wenn ein früherer Besucher vor Ablauf des ursprünglichen zweiwöchigen Profils zurückkehrt, wird das Profil auf die verlängerte Lebensdauer zurückgesetzt. Für alle neuen Besucherprofile wird die verlängerte Profillebensdauer festgelegt.
