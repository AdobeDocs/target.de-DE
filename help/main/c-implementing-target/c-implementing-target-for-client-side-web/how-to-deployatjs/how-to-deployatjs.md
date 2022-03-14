---
keywords: implementieren;at.js;JavaScript-Bibliothek
description: Erfahren Sie, wie Sie die Adobe bereitstellen [!DNL Target] JavaScript-Bibliothek "at.js"mit Tags in Adobe Experience Platform oder ohne Tag-Manager verwenden.
title: Wie stelle ich at.js bereit?
feature: Implement Server-side
role: Developer
exl-id: a11b916a-923e-43d2-af0f-8efde7cd547e
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 35%

---

# Implementieren von „at.js“

Informationen zur Bereitstellung der [!DNL Adobe Target] JavaScript-Bibliothek, at.js, mithilfe von Tags in [!DNL Adobe Experience Platform] oder ohne Tag-Manager.

Sie können at.js mithilfe der folgenden Methoden bereitstellen:

* **[Implementierung [!DNL Target] Verwenden von Tags in [!DNL Adobe Experience Platform]](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)**: Tags in [!DNL Adobe Experience Platform] sind die nächste Generation von Tag-Management-Funktionen von [!DNL Adobe]. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerlebnisse erforderlich sind.

   >[!NOTE]
   >
   >[!DNL Adobe Experience Platform Launch] wurde als Suite von Datenerfassungstechnologien in [!DNL Adobe Experience Platform] umbenannt. Dies spiegelt sich in der Produktdokumentation in verschiedenen Änderungen hinsichtlich der verwendeten Begriffe wider. Eine konsolidierte Übersicht der terminologischen Änderungen finden Sie im folgenden [Dokument](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de).

* **[Implementieren von Target ohne einen Tag-Manager](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)**: Sie können Target ohne Verwendung eines Tag-Managers implementieren (z. B. Tags in [!DNL Adobe Experience Platform]).
* **Implementieren von Target mit einem Drittanbieter-Tag-Manager**: [Tags in [!DNL Adobe Experience Platform]](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) is the preferred method to implement Target; however, you can also implement Target using a third-party tag manager, including Tealium, Ensighten, and Google Tag. For a list of benefits of using Launch, see [Advantages of implementing at.js using the [!DNL Adobe Target] Erweiterung](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#section_48B3F938B6F8491DAF798E0DB54EF304).

   Wenn Sie jedoch wissen, wie Sie [!DNL Target] ohne Tag-Manager können Sie mühelos mit einem Drittanbieter-Tag-Manager implementieren, anstatt at.js im Site-Code fest zu codieren.

   Im Folgenden finden Sie zwei wichtige Themen, die Sie bei der Implementierung unterstützen [!DNL Target] mit einem Drittanbieter-Tag-Manager:

   * [Vor der Implementierung](/help/main/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md)
   * [Implementierung [!DNL Target] ohne Tag-Manager](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)

   Weitere Informationen finden Sie in der Dokumentation für Ihren Drittanbieter-Tag-Manager.

Zu implementieren [!DNL Target] bei Verwendung von Einzelseiten-Apps (SPA) siehe [Implementieren von Einzelseiten-Apps](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).
