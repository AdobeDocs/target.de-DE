---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; auto-target; auto target; Auto-Target-Bericht; Auto Target-Bericht; Personalisierung; Insights; automatisierte Segmente; FAQ; häufig gestellte Fragen; wichtige Attribute
description: Erfahren Sie, wie Sie die spezialisierten Berichte für Automated Personalization- (AP-) und AT-(Automatisches Targeting-)Aktivitäten - "Automatisierte Segmente"und "Wichtige Attribute"verwenden.
title: Wie verwende ich die Personalization Insights-Berichte?
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 57%

---

# ![PREMIUM](/help/main/assets/premium.png) Personalization Insights-Berichte

Für Benutzer von AP ([!UICONTROL Automated Personalization])- und AT (Automatisches Targeting)-Aktivitäten sind zwei spezielle Berichte verfügbar: [!UICONTROL Automatisierte Segmente] und „Wichtige Attribute“.

>[!NOTE]
>
>Beachten Sie bei Verwendung von Personalization Insights-Berichten Folgendes:
>
>* AP- und AT-Aktivitäten sind im Rahmen von [!DNL Target Premium] verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.
>
>* [!UICONTROL Personalization Insights-Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die ein Konversionsoptimierungsziel verwenden. ] Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.
>
>* [!UICONTROL Personalization Insights] Berichte sind nur verfügbar, wenn die Variable [!UICONTROL Primäres Ziel] wird aus dem [!UICONTROL Berichtsmetrik] Dropdown-Liste.
>
>* Personalization Insights-Berichte werden nur in der [Standardumgebung](/help/main/administrating-target/hosts.md) unterstützt.
>
>* [!UICONTROL Personalization Insights] -Berichte werden nur für Aktivitäten generiert, die sich im [!UICONTROL Live] und wurden mindestens 15 Tage lang aktiviert und erhalten Traffic.


## Übersicht über die Personalization Insights-Berichte {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Ziel der [!UICONTROL Personalization Insights]-Berichte ist es, mehr Informationen dazu bereitzustellen, wie die Target-Personalisierungsmodelle hinter Ihren AP- und AT-Aktivitäten den Besuchertraffic personalisieren.  Die [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) bildet die Grundlage für die [!DNL Target] Personalisierungsmodelle.

Da das Ziel der [!UICONTROL Personalization Insights] Berichte sollen verstehen, wie die [!DNL Target] Personalisierungsmodelle entschieden, welchen Besucher zu welchen Inhaltselementen, der [!UICONTROL Personalization Insights] Berichte enthalten nur ein Untersegment des gesamten Traffics, der von Ihrer AP- oder AT-Aktivität bereitgestellt wird. Genauer gesagt enthalten die beiden Berichte sämtlichen Traffic, der das Personalisierungsmodell genutzt hat. [!UICONTROL Personalization Insights]-Berichte berücksichtigen also nicht den Kontrolltraffic oder den Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird.

Zwei [!UICONTROL Personalization Insights] Berichte sind verfügbar:

| Bericht | Details |
|--- |--- |
| [!UICONTROL Automatisierte Segmente] | Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente durch die [!DNL Target] Personalisierungsmodelle reagierten auf die Angebote/Erlebnisse in der Aktivität. |
| [!UICONTROL Wichtige Attribute] | In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar. |

## Interpretieren von Attributen in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Es gibt zwei Arten von Attributen in [!UICONTROL Personalization Insights]-Berichten, die in Ihren AP- oder AT-Modellen verwendet werden:

* **Automatisch von erfasste Attribute:**[!DNL Target] Target verwendet einen Basis-Datensatz, um die Personalisierungsalgorithmen in AP- und AT-Aktivitäten zu erstellen, die in Personalization Insights angezeigt werden. Siehe [Datenerfassung für die Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/ap-data.md) von Target für Datentypen, Beispielattribute und ihre Benennungskonvention für [!UICONTROL Personalization Insights]. Beachten Sie, dass, obwohl diese Attribute berücksichtigt werden, die individuellen Modelle einer Aktivität nicht unbedingt all diese Attribute im endgültigen Modell verwenden.
* **An Target übergebene Attribute:** Siehe  [Hochladen von Daten für die Target-Personalisierungs-Algorithmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] bietet viele Möglichkeiten, zusätzliche Daten an [!DNL Target] Anreicherung des Basisdatensatzes, der zum Erstellen der Personalisierungsalgorithmen in AP- und AT-Aktivitäten verwendet wird:

| Datentyp | Beschreibung | Datentyp-Namenskonvention |
|--- |--- |--- |
| Profilattribute, einschließlich Profilskripten, Profilupdate-API und Seitenprofilattributen | Die Informationen, die Sie dem Benutzerprofil in Target hinzugefügt haben.<br>Diese Informationen können aus Profilskripten, aus mit der Profilaktualisierungs-API hochgeladenen Informationen oder aus In-Mbox-Profilparametern stammen, denen „profile“ vorangestellt ist. | `Custom - Profile - [parameter name]` |
| Seitenparameter (auch „Mbox-Parameter“ genannt) | Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden. | `Custom - Mbox Parameter - [parameter name]` |
| Kundenattribute | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gemeinsam genutzte Zielgruppen (Adobe Audience Manager oder Adobe Analytics) | Mittels Adobe Audience Manager oder Adobe Analytics erstellte und für Target freigegebene Zielgruppen. | `Custom - Experience Cloud Segment - [segment name]` |
| Aktivitätsinterne(s) Reporting-Zielgruppen/-Segment | Während der Einrichtung in „Ziele und Metriken“ definierte Zielgruppen in Ihrer AP- oder AT-Aktivität. | `Custom - Reporting Segment - [segment name]` |

## Häufig gestellte Fragen  

Liste der häufig gestellten Fragen zu [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] [!UICONTROL Insights] Berichte.

### Wie lange bleiben Daten für die Modelle [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] erhalten?

[!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] -Modelle werden an den letzten 45 Tagen des Benutzerverhaltens (Benutzerprofile, Impressionsereignisse und Konversionsereignisse) für die Aktivität trainiert.

[!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] -Modelle speichern das Benutzerverhalten, Schulungsdatensätze und Modellentscheidungen 90 Tage lang, um [!UICONTROL Insights] Berichte. Nach 90 Tagen werden Trainings-Datensätze und Modellentscheidungen verworfen. [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] -Modelle behalten außerdem aggregierte Erlebnis-/Angebotseindruck- und Konversionsdaten für Berichterstellungszwecke für zwei Jahre bei. Diese Daten sind nur aggregierte Daten und enthalten keine Profildaten auf individueller Ebene.

## Schulungsvideo: Verwenden der Personalization Insights-Berichte ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Weitere Informationen finden Sie unter [Verwenden der Personalization Insights-Berichte in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe Blogs

* Teil 1: [Das Mysterium aus dem Zauber der KI-gestützten Personalisierung holen](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Teil 2: [Einen Blick hinter den Vorhang der KI für die Personalisierung in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Teil 3: [MAGIX - die Lösung für das Black Box-Problem der KI-gesteuerten Personalisierung](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)