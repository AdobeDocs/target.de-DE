---
keywords: Adobe Experience Platform Web SDK;aep Web SDK;Web SDK;SDK;Adobe Experience Cloud;Platform Edge Network;Adobe Experience Platform Platform Edge Network;Edge Network;Edge Network;AEP Edge Network
description: Erfahren Sie, wie Sie mit dem Adobe Experience Platform Web SDK über das AEP Edge Network mit den verschiedenen Diensten in Adobe Experience Cloud interagieren können.
title: Wie implementiere ich das Experience Platform Web SDK?
feature: AEP Web SDK
role: Developer
exl-id: afcd741f-bb7e-4bc2-b96c-ec10d5d6f4c5
source-git-commit: 36d9f041315c215c8a2e56b4c208f2f8c9e6dd7d
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 6%

---

# Adobe Experience Platform Web SDK

[!DNL Adobe Experience Platform Web SDK] (AEP Web SDK) ist eine Client-seitige JavaScript-Bibliothek, mit der Kunden von  [!DNL Adobe Experience Cloud] mit den verschiedenen Diensten im Experience Cloud interagieren können (einschließlich  [!DNL Target]), und zwar über das  [!UICONTROL Adobe Experience Platform Edge Network]. Zusätzlich zur JavaScript-Bibliothek gibt es eine [!DNL Experience Platform Launch]-Erweiterung, die Sie bei Ihren Web SDK-Konfigurationen unterstützen kann.

Weitere Informationen finden Sie unter den folgenden Links in der *Adobe Experience Platform Web SDK*-Hilfe:

* Umfassende Informationen: [Was ist das Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)
* Spezifische Informationen zu [!DNL Target]: [Target Overview](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html)

## Empfohlene Dokumentation in diesem Handbuch

Neben der oben erwähnten [!DNL Platform Web SDK]-Dokumentation enthalten Themen in diesem Handbuch auch Informationen, die speziell für [!DNL Platform Web SDK] gelten, da sie sich auf [!DNL Target]-Funktionen beziehen.

| Funktion | Beschreibung/Link |
| --- | --- |
| [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Verwenden Sie QA-URLs in [!DNL Adobe Target], um einfache End-to-End-Aktivitäts-QAs mit unveränderbaren Vorschaulinks, optionalem Zielgruppen-Targeting und QA-Berichten durchzuführen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben. [!UICONTROL Mit Aktivitäts-] QA können Sie Ihre  [!DNL Target] Aktivitäten vollständig testen, bevor Sie sie live schalten.<br>Siehe  [Kompatibilität des QS-Modus der JavaScript-Bibliothek in Target ](/help/c-activities/c-activity-qa/activity-qa.md#compatibility) und  [Vorschau-URLs](/help/c-activities/c-activity-qa/activity-qa.md#preview). |
| [Analytics for Target (A4T) ](/help/c-integrating-target-with-mac/a4t/a4t.md) | [!DNL Adobe Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, mit der Sie Aktivitäten erstellen können, die auf  [!DNL Analytics] Konversionsmetriken und Zielgruppensegmenten basieren. Mit der A4T-Integration können Sie [!DNL Analytics]-Berichte verwenden, um Ihre Ergebnisse zu untersuchen.<br>Siehe  [Unterstützte Aktivitätstypen ](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) und  [Implementierungsschritte für eine Adobe Experience Platform Web SDK-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#platform). |
| [Zielgruppen](/help/c-target/target.md) | Zielgruppen in [!DNL Adobe Target] bestimmen, wer Inhalte und Erlebnisse in einer zielgerichteten Aktivität sieht.<br>Siehe  [Verwenden der ](/help/c-target/c-audiences/audiences.md#use-list) Bibliothek Zielgruppen  [Kombinieren mehrerer Zielgruppen](/help/c-target/combining-multiple-audiences.md). |
| [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Umleitungsangebote führen dazu, dass die Browser der Besucher zu einer neuen Seite umleiten.<br>Siehe  [Unterstützt  [!DNL Adobe Experience Platform Web SDK] das Umleitungsangebot für A4T?](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) |
| [Antwort-Token](/help/administrating-target/response-tokens.md) | Mit Antwort-Token können Sie Target-Daten an Google Analytics und andere Drittanbieter-Integrationen senden.<br>Unter  [Senden von Daten an Google Analytics über Platform Web ](/help/administrating-target/response-tokens.md#platform-web-sdk) SDK finden Sie ein Codebeispiel zur Durchführung dieser Aufgabe. |
| [Implementierung von Einzelseiten-Apps](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/spa-implementation.html?lang=en) | [!UICONTROL Adobe Experience Platform Web ] SDK bietet umfassende Funktionen, mit denen Ihr Unternehmen mithilfe von Client-seitigen Technologien der neuesten Generation, wie Single Page Applications (SPA), Personalisierungen ausführen kann.<br>Dieses Thema finden Sie im  *Platform Web SDK-* Übersichtshandbuch. |
| [Änderungen der TLS-Verschlüsselung (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Mit TLS (Transport Layer Security) können Sie die höchsten Sicherheitsstandards einhalten und die Sicherheit von Kundendaten fördern. |
