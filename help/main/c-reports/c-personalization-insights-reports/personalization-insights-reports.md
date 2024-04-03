---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; auto-target; auto target; Auto-Target-Bericht; Auto Target-Bericht; Personalisierung; Insights; automatisierte Segmente; FAQ; häufig gestellte Fragen; wichtige Attribute
description: Erfahren Sie, wie Sie die spezialisierten Berichte für Automated Personalization- (AP-) und AT-(Automatisches Targeting-)Aktivitäten - "Automatisierte Segmente"und "Wichtige Attribute"verwenden.
title: Wie verwende ich die Personalization Insights-Berichte?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
source-git-commit: 6c8f042acb257fc908349c679bf745e477f94af4
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 28%

---

# [!UICONTROL Personalization Insights] Berichte

Benutzer von [!UICONTROL Automated Personalization] AP und [!UICONTROL Auto-Target] (AT) Tätigkeiten: die [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes] Berichte.

## Zu beachten

Beachten Sie Folgendes bei der Verwendung von [!UICONTROL Personalization Insights] Berichte:

* AP- und AT-Aktivitäten sind als Teil der [[!DNL Target Premium] Lösung](/help/main/c-intro/intro.md#premium). Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.

* [!UICONTROL Personalization Insights] -Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die wie folgt konfiguriert sind:

   * [!DNL Target] reporting > [!UICONTROL Conversion]

     Beispiel:

     ![Zielberichte > Konversion](/help/main/c-reports/assets/conversion.png)

   * [!DNL Analytics] reporting > [!DNL Conversion]

     Beispiel:

     ![Analytics-Berichterstellung > Konversion](/help/main/c-reports/assets/analytics-reporting-conversion.png)

   * [!DNL Analytics] reporting > [!UICONTROL Use an Analytics metric] > [!UICONTROL Maximize Visit Conversion Rate]

     Beispiel:

     ![Verwenden einer Analytics-Metrik > Besuchskonversionsrate maximieren](/help/main/c-reports/assets/maximize-visit-conversion-rate.png)

* Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.

* [!UICONTROL Personalization Insights] Berichte sind nur verfügbar, wenn die Variable [!UICONTROL Primary Goal] wird aus dem [!UICONTROL Report Metric] Dropdown-Liste.

* [!UICONTROL Personalization Insights] Berichte werden in der [Standardumgebung](/help/main/administrating-target/hosts.md) nur.

* [!UICONTROL Personalization Insights] -Berichte werden nur für Aktivitäten generiert, die sich im [!UICONTROL Live] und wurden mindestens 15 Tage lang aktiviert und erhalten Traffic.

## Übersicht über die Berichte zu Personalization Insights {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Das Ziel der [!UICONTROL Personalization Insights] Berichte enthalten weitere Informationen darüber, wie die [!UICONTROL Target] Personalisierungsmodelle hinter Ihren AP- und AT-Aktivitäten personalisieren den Besuchertraffic. Die [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) bildet die Grundlage für die [!DNL Target] Personalisierungsmodelle.

Da das Ziel der [!UICONTROL Personalization Insights] Berichte sollen verstehen, wie die [!DNL Target] Personalisierungsmodelle entschieden, welchen Besucher zu welchen Inhaltselementen, der [!UICONTROL Personalization Insights] Berichte enthalten nur ein Untersegment des gesamten Traffics, der von Ihrer AP- oder AT-Aktivität bereitgestellt wird. Genauer gesagt enthalten die beiden Berichte sämtlichen Traffic, der das Personalisierungsmodell genutzt hat. Mit anderen Worten: [!UICONTROL Personalization Insights] -Berichte berücksichtigen keinen Kontroll-Traffic oder Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird.

Zwei [!UICONTROL Personalization Insights] Berichte sind verfügbar:

| Bericht | Details |
|--- |--- |
| [!UICONTROL Automated Segments] | Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente durch die [!DNL Target] Personalisierungsmodelle reagierten auf die Angebote/Erlebnisse in der Aktivität. |
| [!UICONTROL Important Attributes] | In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar. |

## Interpretieren von Attributen in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Es gibt zwei Arten von Attributen, die in [!UICONTROL Personalization Insights] Berichte, die in Ihren AP- oder AT-Modellen verwendet werden:

* **Automatisch von Target erfasste Attribute:** [!DNL Target] verwendet einen Basisdatensatz, um seine Personalisierungsalgorithmen in AP- und AT-Aktivitäten zu erstellen, die in Personalization Insights angezeigt werden. Siehe [Datenerfassung für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md) für Datentypen, Beispielattribute und deren [!UICONTROL Personalization Insights] Namenskonvention. Beachten Sie, dass die Modelle einer einzelnen Aktivität zwar berücksichtigt werden, jedoch möglicherweise nicht alle diese Attribute im endgültigen Modell verwenden.
* **An Target übergebene Attribute:** Siehe [Hochladen von Daten für die Target-Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] bietet viele Möglichkeiten, zusätzliche Daten an [!DNL Target] Anreicherung des Basisdatensatzes, der zum Erstellen der Personalisierungsalgorithmen in AP- und AT-Aktivitäten verwendet wird:

| Datentyp | Beschreibung | Datentyp-Namenskonvention |
|--- |--- |--- |
| Profilattribute, einschließlich Profilskripten, Profilupdate-API und Seitenprofilattributen | Die Informationen, die Sie dem Benutzerprofil in Target hinzugefügt haben.<br>Diese Informationen können aus Profilskripten, aus mit der Profilaktualisierungs-API hochgeladenen Informationen oder aus In-Mbox-Profilparametern stammen, denen „profile“ vorangestellt ist. | `Custom - Profile - [parameter name]` |
| Seitenparameter (auch &quot;Mbox-Parameter&quot;genannt) | Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden. | `Custom - Mbox Parameter - [parameter name]` |
| Kundenattribute | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gemeinsam genutzte Zielgruppen (Adobe Audience Manager oder Adobe Analytics) | Mittels Adobe Audience Manager oder Adobe Analytics erstellte und für Target freigegebene Zielgruppen. | `Custom - Experience Cloud Segment - [segment name]` |
| Freigegebene Zielgruppen (Adobe Experience Platform/Echtzeit-Kundendatenplattform) | Zielgruppen, die über die Adobe Experience Platform/Echtzeit-Kundendatenplattform erstellt und über Ziele für Target freigegeben wurden. | `Custom - Adobe Experience Platform Segment - [segment name]` |
| Freigegebene Attribute (Adobe Experience Platform/Echtzeit-Kundendatenplattform) | Attribute, die über die Adobe Experience Platform/Echtzeit-Kundendatenplattform erstellt und über Ziele für Target freigegeben wurden. Diese Funktion ist derzeit als Betaversion verfügbar. | `Custom - Adobe Experience Platform Attribute - [attribute name]]` |
| Aktivitätsinterne(s) Reporting-Zielgruppen/-Segment | Zielgruppen, die während der Einrichtung in &quot;Ziele und Metriken&quot;in Ihrer AP- oder AT-Aktivität definiert wurden. | `Custom - Reporting Segment - [segment name]` |

## Häufig gestellte Fragen  

Liste der häufig gestellten Fragen zu [!UICONTROL Automated Personalization] AP und [!UICONTROL Auto-Target] [!UICONTROL Insights] Berichte.

### Wie lange Daten benötigen [!UICONTROL Automated Personalization] AP und [!UICONTROL Auto-Target] Modelle bestehen fort?

[!UICONTROL Automated Personalization] AP und [!UICONTROL Auto-Target] -Modelle werden an den letzten 45 Tagen des Benutzerverhaltens (Benutzerprofile, Impressionsereignisse und Konversionsereignisse) für die Aktivität trainiert.

[!UICONTROL Automated Personalization] AP und [!UICONTROL Auto-Target] -Modelle speichern das Benutzerverhalten, Schulungsdatensätze und Modellentscheidungen 90 Tage lang, um [!UICONTROL Insights] Berichte. Nach 90 Tagen werden Trainings-Datensätze und Modellentscheidungen verworfen. [!UICONTROL Automated Personalization] AP und [!UICONTROL Auto-Target] -Modelle behalten außerdem aggregierte Erlebnis-/Angebotseindruck- und Konversionsdaten für Berichterstellungszwecke für zwei Jahre bei. Diese Daten sind nur aggregierte Daten und enthalten keine Profildaten auf individueller Ebene.

## Schulungsvideo: Verwenden der Personalization Insights-Berichte ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Weitere Informationen finden Sie unter [Verwenden der Personalization Insights-Berichte in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe Blogs

* Teil 1: [Das Mysterium aus dem Zauber der KI-gestützten Personalisierung holen](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Teil 2: [Einen Blick hinter den Vorhang der KI für die Personalisierung in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Teil 3: [MAGIX - die Lösung für das Black Box-Problem der KI-gestützten Personalisierung](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
