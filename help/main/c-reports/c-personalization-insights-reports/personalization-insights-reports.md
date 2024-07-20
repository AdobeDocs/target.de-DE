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

Für Benutzer der Aktivitäten [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] (AT) stehen zwei spezielle Berichte zur Verfügung: die Berichte [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes].

## Zu beachten

Beachten Sie bei Verwendung von [!UICONTROL Personalization Insights] -Berichten Folgendes:

* AP- und AT-Aktivitäten sind als Teil der [[!DNL Target Premium] Lösung](/help/main/c-intro/intro.md#premium) verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.

* [!UICONTROL Personalization Insights] -Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die wie folgt konfiguriert sind:

   * [!DNL Target] Berichterstellung > [!UICONTROL Conversion]

     Beispiel:

     ![Target-Berichterstellung > Konversion](/help/main/c-reports/assets/conversion.png)

   * [!DNL Analytics] Berichterstellung > [!DNL Conversion]

     Beispiel:

     ![Analytische Berichterstellung > Konversion](/help/main/c-reports/assets/analytics-reporting-conversion.png)

   * [!DNL Analytics] Berichterstellung > [!UICONTROL Use an Analytics metric] > [!UICONTROL Maximize Visit Conversion Rate]

     Beispiel:

     ![Verwenden Sie eine Analytics-Metrik > Besuchskonversionsrate maximieren](/help/main/c-reports/assets/maximize-visit-conversion-rate.png)

* Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.

* [!UICONTROL Personalization Insights] -Berichte sind nur verfügbar, wenn die [!UICONTROL Primary Goal] aus der Dropdownliste [!UICONTROL Report Metric] ausgewählt ist.

* [!UICONTROL Personalization Insights] -Berichte werden nur in der [Standardumgebung](/help/main/administrating-target/hosts.md) unterstützt.

* [!UICONTROL Personalization Insights] -Berichte werden nur für Aktivitäten generiert, die sich im Status [!UICONTROL Live] befinden und die mindestens 15 Tage lang aktiviert wurden und Traffic erhalten.

## Übersicht über Personalization Insights-Berichte {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Ziel der [!UICONTROL Personalization Insights] -Berichte ist es, weitere Informationen dazu bereitzustellen, wie die [!UICONTROL Target] -Personalisierungsmodelle hinter Ihren AP- und AT-Aktivitäten den Besucher-Traffic personalisieren. Der [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) bildet die Grundlage für die [!DNL Target] -Personalisierungsmodelle.

Da der Zweck der [!UICONTROL Personalization Insights] -Berichte darin besteht, zu verstehen, wie die [!DNL Target]-Personalisierungsmodelle entschieden haben, welchen Besucher an welche Inhaltselemente zu senden, spiegeln die [!UICONTROL Personalization Insights] -Berichte nur ein Untersegment des gesamten durch Ihre AP- oder AT-Aktivität bereitgestellten Traffics wider. Genauer gesagt enthalten die beiden Berichte sämtlichen Traffic, der das Personalisierungsmodell genutzt hat. Mit anderen Worten: [!UICONTROL Personalization Insights] -Berichte berücksichtigen keinen Kontroll-Traffic oder Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird.

Zwei [!UICONTROL Personalization Insights] -Berichte sind verfügbar:

| Bericht | Details |
|--- |--- |
| [!UICONTROL Automated Segments] | Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den [!DNL Target] -Personalisierungsmodellen definiert wurden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben. |
| [!UICONTROL Important Attributes] | In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar. |

## Interpretieren von Attributen in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Es gibt zwei Arten von Attributen, die in [!UICONTROL Personalization Insights] -Berichten dargestellt werden und in Ihren AP- oder AT-Modellen verwendet werden:

* **Automatisch von Target erfasste Attribute:** [!DNL Target] verwendet einen Basisdatensatz, um seine Personalisierungsalgorithmen in AP- und AT-Aktivitäten zu erstellen, die in Personalization Insights angezeigt werden. Siehe [Datenerfassung für die Personalization-Algorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md) für Datentypen, Beispielattribute und ihre [!UICONTROL Personalization Insights] -Namenskonvention. Beachten Sie, dass die Modelle einer einzelnen Aktivität zwar berücksichtigt werden, jedoch möglicherweise nicht alle diese Attribute im endgültigen Modell verwenden.
* **An Target übergebene Attribute:** Siehe [Hochladen von Daten für die Target Personalization-Algorithmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] bietet viele Möglichkeiten, zusätzliche Daten an [!DNL Target] zu übergeben, um den Basisdatensatz anzureichern, der zum Erstellen seiner Personalisierungsalgorithmen in AP- und AT-Aktivitäten verwendet wird:

| Datentyp | Beschreibung | Datentyp-Namenskonvention |
|--- |--- |--- |
| Profilattribute, einschließlich Profilskripten, Profilupdate-API und Seitenprofilattributen | Die Informationen, die Sie dem Benutzerprofil in Target hinzugefügt haben.<br>Diese Informationen können aus Profilskripten, aus mit der Profilaktualisierungs-API hochgeladenen Informationen oder aus In-Mbox-Profilparametern stammen, denen „profile“ vorangestellt ist. | `Custom - Profile - [parameter name]` |
| Seitenparameter (auch &quot;Mbox-Parameter&quot;genannt) | Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden. | `Custom - Mbox Parameter - [parameter name]` |
| Kundenattribute | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gemeinsam genutzte Zielgruppen (Adobe Audience Manager oder Adobe Analytics) | Mittels Adobe Audience Manager oder Adobe Analytics erstellte und für Target freigegebene Zielgruppen. | `Custom - Experience Cloud Segment - [segment name]` |
| Freigegebene Zielgruppen (Adobe Experience Platform/Echtzeit-Kundendatenplattform) | Zielgruppen, die über die Adobe Experience Platform/Echtzeit-Kundendatenplattform erstellt und über Ziele für Target freigegeben wurden. | `Custom - Adobe Experience Platform Segment - [segment name]` |
| Freigegebene Attribute (Adobe Experience Platform/Echtzeit-Kundendatenplattform) | Attribute, die über die Adobe Experience Platform/Echtzeit-Kundendatenplattform erstellt und über Ziele für Target freigegeben wurden. Diese Funktion befindet sich derzeit in Beta. | `Custom - Adobe Experience Platform Attribute - [attribute name]]` |
| Aktivitätsinterne(s) Reporting-Zielgruppen/-Segment | Zielgruppen, die während der Einrichtung in &quot;Ziele und Metriken&quot;in Ihrer AP- oder AT-Aktivität definiert wurden. | `Custom - Reporting Segment - [segment name]` |

## Häufig gestellte Fragen  

Liste der häufig gestellten Fragen zu Berichten vom Typ [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] [!UICONTROL Insights].

### Wie lange bleiben Daten für die Modelle [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] erhalten?

Die Modelle [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] werden an den letzten 45 Tagen des Benutzerverhaltens (Benutzerprofile, Impressionsereignisse und Konversionsereignisse) für die Aktivität trainiert.

Die Modelle [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] behalten das Benutzerverhalten, Trainings-Datensätze und Modellentscheidungen 90 Tage lang bei, um [!UICONTROL Insights] -Berichte zu erstellen. Nach 90 Tagen werden Trainings-Datensätze und Modellentscheidungen verworfen. Die Modelle [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] behalten außerdem aggregierte Impressions- und Konversionsdaten auf Erlebnis-/Angebotsebene für Berichtszwecke für zwei Jahre bei. Diese Daten sind nur aggregierte Daten und enthalten keine Profildaten auf individueller Ebene.

## Schulungsvideo: Verwenden der Personalization Insights-Berichte ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Weitere Informationen finden Sie unter [Verwenden der Personalization Insights-Berichte in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe Blogs

* Teil 1: [Das Mysterium aus dem Zauber der KI-gesteuerten Personalization holen](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Teil 2: [Eine Aussicht hinter dem Vorhang der KI für Personalization in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Teil 3: [MAGIX — The Solution to the Black Box issue of AI-Driven Personalization](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
