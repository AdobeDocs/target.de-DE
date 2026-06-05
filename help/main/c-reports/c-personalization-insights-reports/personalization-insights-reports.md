---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; auto-target; auto target; Auto-Target-Bericht; Auto Target-Bericht; Personalisierung; Insights; automatisierte Segmente; FAQ; häufig gestellte Fragen; wichtige Attribute
description: Erfahren Sie, wie Sie die spezialisierten Berichte für Aktivitäten von Automated Personalization (AP) und Automatisches Targeting (AT) verwenden - automatisierte Segmente und wichtige Attribute.
title: Wie verwende ich die Personalization Insights-Berichte?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
TQID: https://experienceleague.adobe.com/qDaIhyfV-m3oHJArqg8TKMAe-k5QwjEUjGzhZrPSTEI
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
subfeature_v2: id: fff07a91-d479-45f4-ae95-9762e79b1b7c
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1023
ht-degree: 29%

---

# [!UICONTROL Personalization Insights] Berichte

Für Benutzer von [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Automatisches Targeting] (AT)-Aktivitäten stehen zwei spezialisierte Berichte zur Verfügung: die Berichte [!UICONTROL Automatisierte ] und [!UICONTROL Wichtige Attribute].

## Zu beachten

Beachten Sie bei der Verwendung von [!UICONTROL Personalization Insights]-Berichten Folgendes:

* AP- und AT-Aktivitäten sind als Teil der [[!DNL Target Premium] Lösung](/help/main/c-intro/intro.md#premium) verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.

* [!UICONTROL Personalization Insights]-Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die wie folgt konfiguriert sind:

   * [!DNL Target] > [!UICONTROL Konversion]

     Beispiel:

     ![Target-Reporting > Konversion](/help/main/c-reports/assets/conversion.png)

   * [!DNL Analytics] > [!DNL Conversion]

     Beispiel:

     ![Analytics-Reporting > Konversion](/help/main/c-reports/assets/analytics-reporting-conversion.png)

   * [!DNL Analytics] > [!UICONTROL Analytics-Metrik verwenden] > [!UICONTROL Konversionsrate für Besuche maximieren]

     Beispiel:

     ![Analytics-Metrik verwenden > Konversionsrate für Besuche maximieren](/help/main/c-reports/assets/maximize-visit-conversion-rate.png)

* Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.

* [!UICONTROL Personalization Insights]-Berichte sind nur verfügbar, wenn das [!UICONTROL Primäre Ziel] aus der Dropdown-Liste [!UICONTROL Berichtsmetrik] ausgewählt wurde.

* [!UICONTROL Personalization Insights]-Berichte werden nur in der [Standardumgebung](/help/main/administrating-target/hosts.md) unterstützt.

* [!UICONTROL Personalization Insights]-Berichte werden nur für Aktivitäten generiert, die sich im Status [!UICONTROL Live] befinden und seit mindestens 15 Tagen aktiviert sind und Traffic empfangen.

## Übersicht über das Reporting zu Personalization Insights {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Die [!UICONTROL Personalization Insights]-Berichte enthalten weitere Informationen darüber, wie die [!UICONTROL Target]-Personalisierungsmodelle hinter Ihren AP- und AT-Aktivitäten den Besucher-Traffic personalisieren. Der [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) ist die Grundlage für die [!DNL Target] Personalisierungsmodelle.

Da es das Ziel der [!UICONTROL Personalization Insights]-Berichte ist zu verstehen, wie die [!DNL Target] Personalisierungsmodelle entschieden haben, welche Besucherin oder welchen Besucher an welche Inhaltselemente zu senden, spiegeln die [!UICONTROL Personalization Insights]-Berichte nur ein Untersegment des gesamten Traffics wider, der von Ihrer AP- oder AT-Aktivität bereitgestellt wird. Genauer gesagt enthalten die beiden Berichte sämtlichen Traffic, der das Personalisierungsmodell genutzt hat. [!UICONTROL Personalization Insights]-Berichte berücksichtigen also nicht den Kontrolltraffic oder den Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird.

Zwei [!UICONTROL Personalization Insights]-Berichte sind verfügbar:

| Bericht | Details |
|--- |--- |
| [!UICONTROL Automatisierte Segmente] | Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie verschiedene durch die [!DNL Target] Personalisierungsmodelle definierte automatisierte Segmente auf die Angebote/Erlebnisse in der Aktivität reagierten. |
| [!UICONTROL Wichtige Attribute] | In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar. |

## Interpretieren von Attributen in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Es gibt zwei Arten von Attributen in [!UICONTROL Personalization Insights]-Berichten, die in Ihren AP- oder AT-Modellen verwendet werden:

* **Automatisch von Target erfasste Attribute:** [!DNL Target] verwendet einen Basisdatensatz, um seine Personalisierungsalgorithmen in AP- und AT-Aktivitäten zu erstellen, die in Personalization Insights umgesetzt werden. Unter [Datenerfassung für Personalization-Algorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md) finden Sie Datentypen, Beispielattribute und ihre [!UICONTROL Personalization Insights]-Namenskonvention. Beachten Sie, dass, obwohl diese Attribute berücksichtigt werden, die Modelle einer einzelnen Aktivität möglicherweise nicht alle diese Attribute im endgültigen Modell verwenden.
* **An Target übergebene Attribute:** Siehe [Hochladen von Daten für die Target Personalization-Algorithmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] bietet viele Möglichkeiten, zusätzliche Daten an [!DNL Target] zu übergeben, um den Basisdatensatz anzureichern, der zum Erstellen der Personalisierungsalgorithmen in AP- und AT-Aktivitäten verwendet wird:

| Datentyp | Beschreibung | Datentyp-Namenskonvention |
|--- |--- |--- |
| Profilattribute, einschließlich Profilskripten, Profilupdate-API und Seitenprofilattributen | Die Informationen, die Sie dem Benutzerprofil in Target hinzugefügt haben.<br>Diese Informationen können aus Profilskripten, aus mit der Profilaktualisierungs-API hochgeladenen Informationen oder aus In-Mbox-Profilparametern stammen, denen „profile“ vorangestellt ist. | `Custom - Profile - [parameter name]` |
| Seitenparameter (auch „mbox-Parameter“ genannt) | Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden. | `Custom - Mbox Parameter - [parameter name]` |
| Kundenattribute | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gemeinsam genutzte Zielgruppen (Adobe Audience Manager oder Adobe Analytics) | Mittels Adobe Audience Manager oder Adobe Analytics erstellte und für Target freigegebene Zielgruppen. | `Custom - Experience Cloud Segment - [segment name]` |
| Freigegebene Zielgruppen (Adobe Experience Platform/Real-Time CDP) | Zielgruppen, die über Adobe Experience Platform/Real-Time CDP erstellt und über Ziele für Target freigegeben wurden. | `Custom - Adobe Experience Platform Segment - [segment name]` |
| Freigegebene Attribute (Adobe Experience Platform/Real-Time CDP) | Attribute, die über Adobe Experience Platform/Real-Time CDP erstellt und über Ziele für Target freigegeben wurden. Diese Funktion befindet sich derzeit in Beta. | `Custom - Adobe Experience Platform Attribute - [attribute name]]` |
| Aktivitätsinterne(s) Reporting-Zielgruppen/-Segment | Zielgruppen, die während der Einrichtung in „Ziele und Metriken“ in Ihrer AP- oder automatischen Targeting-Aktivität definiert wurden. | `Custom - Reporting Segment - [segment name]` |

## Häufig gestellte Fragen

Liste der häufig gestellten Fragen zu [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Auto-][!UICONTROL Insights]-Berichten.

### Wie lange bleiben Daten für die Modelle [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] erhalten?

Die [!UICONTROL Automated Personalization] (AP)- [!UICONTROL Automatisches Targeting]-Modelle werden für die letzten 45 Tage des Benutzerverhaltens (Benutzerprofile, Impressionsereignisse und Konversionsereignisse) für die Aktivität trainiert.

Die [!UICONTROL Automated Personalization] (AP)- [!UICONTROL Automatisches Targeting]-Modelle behalten das Benutzerverhalten, Trainings-Aufzeichnungen und Modellentscheidungsdaten 90 Tage lang bei, um [!UICONTROL Insights]-Berichte zu erstellen. Nach 90 Tagen werden Trainingsdatensätze und Modellentscheidungen verworfen. Die [!UICONTROL Automated Personalization] (AP)- [!UICONTROL Automatisches Targeting]-Modelle behalten außerdem aggregierte Impressions- und Konversionsdaten auf Erlebnis-/Angebotsebene für Berichtszwecke für zwei Jahre bei. Diese Daten sind nur Daten auf Aggregatebene und enthalten keine Profildaten auf individueller Ebene.

## Schulungsvideo: Verwenden von Personalization Insights-Berichten ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Weitere Informationen finden Sie unter [Verwenden der Personalization Insights-Berichte in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe Blogs

* Teil 1: [Die Magie des KI-getriebenen Personalization aus dem Rätsel holen](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Teil 2: [Ein Blick hinter den Vorhang der KI für Personalization in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Teil 3: [MAGIX - die Lösung für das Black Box-Problem von AI-Driven Personalization](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
