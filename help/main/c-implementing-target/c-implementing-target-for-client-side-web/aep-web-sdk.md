---
keywords: Adobe Experience Platform Web SDK;aep Web SDK;Web SDK;SDK;Adobe Experience Cloud;Platform Edge Network;Adobe Experience Platform Platform Edge Network;Edge Network;Edge Network;AEP Edge Network
description: Erfahren Sie, wie Sie mit dem Adobe Experience Platform Web SDK über das AEP Edge Network mit den verschiedenen Diensten in Adobe Experience Cloud interagieren können.
title: Wie implementiere ich das Experience Platform Web SDK?
feature: AEP Web SDK
role: Developer
exl-id: afcd741f-bb7e-4bc2-b96c-ec10d5d6f4c5
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 16%

---

# Adobe Experience Platform Web SDK

[!DNL Adobe Experience Platform Web SDK] (AEP Web SDK) ist eine clientseitige JavaScript-Bibliothek, die Kunden von [!DNL Adobe Experience Cloud] Interaktion mit den verschiedenen Dienststellen des Experience Cloud (einschließlich [!DNL Target]) durch die [!UICONTROL Adobe Experience Platform Edge Network]. Zusätzlich zur JavaScript-Bibliothek gibt es eine [!DNL Adobe Experience Platform] -Erweiterung, um Sie bei Ihren Web SDK-Konfigurationen zu unterstützen.

Weitere Informationen finden Sie unter den folgenden Links in der *Adobe Experience Platform Web SDK* help:

* Umfassende Informationen: [Was ist das Adobe Experience Platform Web SDK?](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de)
* Spezifische Informationen für [!DNL Target]: [Target-Übersicht](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html?lang=de)

## Tutorial: Implementieren von Adobe Experience Cloud mit dem Platform Web SDK

Erfahren Sie, wie Sie [Implementieren von Experience Cloud-Anwendungen mit dem Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=_blank}. Informationen speziell für Target finden Sie unter [Target mit dem Platform Web SDK einrichten](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/applications-setup/setup-target.html){target=_blank} innerhalb des Tutorials.

## Empfohlene Dokumentation

Zusätzlich zu den [!DNL Platform Web SDK] Die oben genannten Dokumentationen enthalten auch Themen in diesem Handbuch Informationen zu [!DNL Platform Web SDK] in Bezug auf [!DNL Target] Funktionen.

| Funktion | Beschreibung/Link |
| --- | --- |
| [Aktivitäts-QA](/help/main/c-activities/c-activity-qa/activity-qa.md) | Verwenden von QA-URLs in [!DNL Adobe Target] zur einfachen End-to-End-Aktivitäts-QA mit unveränderbaren Vorschaulinks, optionalem Zielgruppen-Targeting und QA-Berichten, die basierend auf Live-Aktivitätsdaten segmentiert bleiben. [!UICONTROL Aktivitäts-QA] Sie können Ihre [!DNL Target] -Aktivitäten, bevor sie live geschaltet werden.<br>Siehe [Kompatibilität des JavaScript-Bibliotheks-QA-Modus in Target](/help/main/c-activities/c-activity-qa/activity-qa.md#compatibility) und [Vorschau-URLs](/help/main/c-activities/c-activity-qa/activity-qa.md#preview). |
| [Analytics for Target (A4T) ](/help/main/c-integrating-target-with-mac/a4t/a4t.md) | [!DNL Adobe Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, die Ihnen das Erstellen von Aktivitäten ermöglicht, die auf Konversionsmetriken und Zielgruppensegmenten aus [!DNL Analytics] basieren. Mit der A4T-Integration können Sie Ihre Ergebnisse anhand von [!DNL Analytics]-Berichten überprüfen.<br>Siehe [Unterstützte Aktivitätstypen](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) und [Implementierungsschritte für eine Adobe Experience Platform Web SDK-Implementierung](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#platform). |
| [Zielgruppen](/help/main/c-target/target.md) | Zielgruppen in [!DNL Adobe Target] bestimmen, wer Inhalte und Erlebnisse in einer zielgerichteten Aktivität sieht.<br>Siehe [Verwenden der Zielgruppenliste](/help/main/c-target/c-audiences/audiences.md#use-list) und [Kombinieren mehrerer Zielgruppen](/help/main/c-target/combining-multiple-audiences.md). |
| [Erstellen von Zielgruppen](/help/main/c-target/c-audiences/audiences.md) | Die Verwendung der in [!DNL Adobe Experience Platform] erstellten Zielgruppen liefert umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen.<ul>Siehe [Verwenden von Zielgruppen aus [!DNL Adobe Experience Platform]](/help/main/c-target/c-audiences/audiences.md#aep). |
| [Angebotsentscheidungen](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md) | Fügen Sie in Adobe Journey Optimizer erstellte Angebotsentscheidungen zu Target-Aktivitäten hinzu (manueller A/B-Test oder Erlebnis-Targeting), um das nächste beste Angebot für Ihre Besucher im Web und auf Mobilgeräten zu ermitteln und bereitzustellen. |
| [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Umleitungsangebote führen dazu, dass die Browser der Besucher zu einer neuen Seite umleiten.<br>Siehe [Stellt die [!DNL Adobe Experience Platform Web SDK] Unterstützung von Umleitungsangeboten für A4T?](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) |
| [Antwort-Token](/help/main/administrating-target/response-tokens.md) | Mit Antwort-Token können Sie Target-Daten an Google Analytics und andere Drittanbieter-Integrationen senden.<br>Siehe [Senden von Daten an Google Analytics über das Platform Web SDK](/help/main/administrating-target/response-tokens.md#platform-web-sdk) um ein Codebeispiel für die Ausführung dieser Aufgabe anzuzeigen. |
| [Implementierung von Einzelseiten-Apps](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/spa-implementation.html?lang=en) im *Übersicht über das Platform Web SDK* Handbuch. | [!UICONTROL Adobe Experience Platform Web SDK] bietet umfassende Funktionen, mit denen Ihr Unternehmen mithilfe von Client-seitigen Technologien der nächsten Generation Personalisierungen ausführen kann, wie z. B. Einzelseitenanwendungen (SPA). |
| [Änderungen der TLS-Verschlüsselung (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/) | Mit TLS (Transport Layer Security){target=_blank} können Sie die höchsten Sicherheitsstandards einhalten und die Sicherheit von Kundendaten fördern. |
