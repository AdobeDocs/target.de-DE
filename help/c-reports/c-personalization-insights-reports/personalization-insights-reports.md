---
keywords: Targeting;AP reports;automated personalization reports;auto-target;auto target;auto target report;auto-target report;personalization;insights;automated segments;faq;frequently asked questions;important attributes
description: Für Benutzer von Automatisierte Personalisierung (AP) und von Automatisches Targeting (AT) sind zwei spezialisierte Berichte verfügbar, die die Berichte für automatisierte Segmente und wichtige Attribute enthalten.
title: Berichte zu Personalization Insights
feature: reports
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 68%

---


# ![PREMIUM](/help/assets/premium.png) Personalization Insights-Berichte{#personalization-insights-reports}

Für Benutzer von AP ([!UICONTROL Automated Personalization])- und AT (Automatisches Targeting)-Aktivitäten sind zwei spezielle Berichte verfügbar: [!UICONTROL Automatisierte Segmente] und „Wichtige Attribute“.

>[!NOTE]
>
>Beachten Sie Folgendes, wenn Sie Personalization Insight-Berichte verwenden:
>
>* AP- und AT-Aktivitäten sind im Rahmen von [!DNL Target Premium] verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.
   >
   >
* [!UICONTROL Personalization Insights-Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die ein Konversionsoptimierungsziel verwenden. ] Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.
   >
   >
* [!UICONTROL Personalization Insight-] Berichte stehen nur zur Verfügung, wenn die  [!UICONTROL Primär-] Zielvorgabe aus der Dropdown-Liste  [!UICONTROL Report ] Metriken ausgewählt wurde.
   >
   >
* Personalization Insights-Berichte werden nur in der [Standardumgebung](/help/administrating-target/hosts.md) unterstützt.
   >
   >
* [!UICONTROL Personalization Insight-] Berichte werden nur für Aktivitäten generiert, die sich im   Livestatus befinden und die mindestens 15 Tage lang aktiviert wurden und Traffic erhalten haben.


## Übersicht über die Personalization Insights-Berichte {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Ziel der [!UICONTROL Personalization Insights]-Berichte ist es, mehr Informationen dazu bereitzustellen, wie die Target-Personalisierungsmodelle hinter Ihren AP- und AT-Aktivitäten den Besuchertraffic personalisieren.  Der [Random Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md) ist die Grundlage für die [!DNL Target]-Personalisierungsmodelle.

Da das Ziel der [!UICONTROL Personalization Insights]-Berichte darin besteht, zu verstehen, wie die [!DNL Target]-Personalisierungsmodelle entschieden haben, welchen Besucher zu welchem Inhaltselement zu senden, spiegeln die [!UICONTROL Personalization Insights]-Berichte nur ein Teilsegment des gesamten Traffics wider, der von Ihrer AP- oder AT-Aktivität bereitgestellt wird. Genauer gesagt enthalten die beiden Berichte sämtlichen Traffic, der das Personalisierungsmodell genutzt hat. [!UICONTROL Personalization Insights]-Berichte berücksichtigen also nicht den Kontrolltraffic oder den Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird.

Es stehen zwei [!UICONTROL Personalization Insights]-Berichte zur Verfügung:

| Bericht | Details |
|--- |--- |
| [!UICONTROL Automatisierte Segmente] | Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie verschiedene automatisierte Segmente, die von den [!DNL Target]-Personalisierungsmodellen definiert wurden, auf die Angebot/Erlebnisse in der Aktivität reagiert haben. |
| [!UICONTROL Wichtige Attribute] | In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar. |

## Interpretieren von Attributen in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Es gibt zwei Arten von Attributen in [!UICONTROL Personalization Insights]-Berichten, die in Ihren AP- oder AT-Modellen verwendet werden:

* **Automatisch von erfasste Attribute:**[!DNL Target] Target verwendet einen Basis-Datensatz, um die Personalisierungsalgorithmen in AP- und AT-Aktivitäten zu erstellen, die in Personalization Insights angezeigt werden. Siehe [Datenerfassung für die Personalisierungsalgorithmen](/help/c-activities/t-automated-personalization/ap-data.md) von Target für Datentypen, Beispielattribute und ihre Benennungskonvention für [!UICONTROL Personalization Insights]. Beachten Sie, dass, obwohl diese Attribute berücksichtigt werden, die individuellen Modelle einer Aktivität nicht unbedingt all diese Attribute im endgültigen Modell verwenden.
* **An Target übergebene Attribute:** Siehe  [Hochladen von Daten für die Target-Personalisierungs-Algorithmen](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] bietet viele Möglichkeiten, um zusätzliche Daten  [!DNL Target] zur Erweiterung des Basisdatensatzes, der zum Aufbau der Personalisierungsalgorithmen in AP- und AT-Aktivitäten verwendet wird, bereitzustellen:

| Datentyp | Beschreibung | Datentyp-Namenskonvention |
|--- |--- |--- |
| Profilattribute, einschließlich Profilskripten, Profilupdate-API und Seitenprofilattributen | Die Informationen, die Sie dem Benutzerprofil in Target hinzugefügt haben.<br>Diese Informationen können aus Profilskripten, aus mit der Profilaktualisierungs-API hochgeladenen Informationen oder aus In-Mbox-Profilparametern stammen, denen „profile“ vorangestellt ist. | `Custom - Profile - [parameter name]` |
| Seitenparameter (auch „Mbox-Parameter“ genannt) | Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden. | `Custom - Mbox Parameter - [parameter name]` |
| Kundenattribute | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gemeinsam genutzte Zielgruppen (Adobe Audience Manager oder Adobe Analytics) | Mittels Adobe Audience Manager oder Adobe Analytics erstellte und für Target freigegebene Zielgruppen. | `Custom - Experience Cloud Segment - [segment name]` |
| Aktivitätsinterne(s) Reporting-Zielgruppen/-Segment | Während der Einrichtung in „Ziele und Metriken“ definierte Zielgruppen in Ihrer AP- oder AT-Aktivität. | `Custom - Reporting Segment - [segment name]` |

## Schulungsvideo: Verwenden der Personalization Insights-Berichte  ![Tutorialzeichen](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Weitere Informationen finden Sie unter Verwenden der Personalisierungseinblicke-Berichte in Adobe Target[.](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html)

## Adoben-Blogs

* Teil 1: [Das Mysterium aus der Magie der AI-getriebenen Personalisierung entfernen](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Teil 2: [Einen Blick hinter den Vorhang der AI für Personalisierung in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Teil 3: [MAGIX — Lösung zum Black Box-Problem der AI-getriebenen Personalisierung](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
