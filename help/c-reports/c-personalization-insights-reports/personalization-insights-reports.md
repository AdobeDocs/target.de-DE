---
description: Für Benutzer von Automatisierte Personalisierung (AP) und von Automatisches Targeting (AT) sind zwei spezialisierte Berichte verfügbar, die die Berichte für automatisierte Segmente und wichtige Attribute enthalten.
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; auto-target; auto target; Auto-Target-Bericht; Auto Target-Bericht; Personalisierung; Insights; automatisierte Segmente; FAQ; häufig gestellte Fragen; wichtige Attribute
seo-description: Für Benutzer von Automatisierte Personalisierung (AP) und von Automatisches Targeting (AT) sind zwei spezialisierte Berichte verfügbar, die die Berichte für automatisierte Segmente und wichtige Attribute enthalten.
seo-title: Berichte zu Personalization Insights
solution: Target
title: Berichte zu Personalization Insights
title-outputclass: premium
uuid: 2507a7a6-d229-412a-a992-5777b45c80e7
badge: premium
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# ![PREMIUM](/help/assets/premium.png) Personalization Insights-Berichte{#personalization-insights-reports}

Für Benutzer von AP (Automated Personalization)- und AT (Automatisches Targeting)-Aktivitäten sind zwei spezielle Berichte verfügbar: „Automatisierte Segmente“ und „Wichtige Attribute“.

>[!NOTE]
>
>AP- und AT-Aktivitäten sind im Rahmen von [!DNL Target Premium] verfügbar. Sie sind nicht mit [!DNL Target Standard]ohne[!DNL Target Premium] Lizenz enthalten.
>
>Personalization Insights-Berichte sind nur für AP- und AT-Aktivitäten verfügbar, die ein Konversionsoptimierungsziel verwenden. Auch Aktivitäten, deren Optimierungsziel von Konversion zu Umsatz geändert wurde, nachdem die Aktivität bereits live war, werden nicht unterstützt.
>
>Personalization Insights-Berichte werden nur in der [Standardumgebung](../../administrating-target/hosts.md) unterstützt.

## Übersicht über die Personalization Insights-Berichte {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Ziel der [!UICONTROL Personalization Insights]-Berichte ist es, mehr Informationen dazu bereitzustellen, wie die Target-Personalisierungsmodelle hinter Ihren AP- und AT-Aktivitäten den Besuchertraffic personalisieren. Der [Random Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md) stellt die Grundlage für die Personalisierungsmodelle von Target dar.

Da die Personalization Insights-Berichte vermitteln sollen, wie die Target-Personalisierungsmodelle entscheiden, welche Inhalte an welchen Besucher gesendet werden, spiegeln die Personalization Insights-Berichte nur ein Untersegment des gesamten durch Ihre AP- oder AT-Aktivitäten bereitgestellten Traffics wider. Genauer gesagt enthalten die beiden Berichte sämtlichen Traffic, der das Personalisierungsmodell genutzt hat. Personalization Insights-Berichte berücksichtigen also nicht den Kontrolltraffic oder den Traffic, der vom Gesamt-Gewinnermodell bereitgestellt wird.

Es stehen zwei Berichte zur Verfügung:

| Bericht | Details |
|--- |--- |
| Automatisierte Segmente | Verschiedene Besucher reagieren unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben. |
| Wichtige Attribute | In unterschiedlichen Aktivitäten sind Attribute mal mehr, mal weniger wichtig für die Personalisierungsentscheidung des Modells. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar. |

## Interpretieren von Attributen in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Es gibt zwei Arten von Attributen in [!UICONTROL Personalization Insights]-Berichten, die in Ihren AP- oder AT-Modellen verwendet werden:

* **Automatisch von Target erfasste Attribute:** Target verwendet einen Basis-Datensatz, um die Personalisierungsalgorithmen in AP- und AT-Aktivitäten zu erstellen, die in Personalization Insights angezeigt werden. Siehe [Datenerfassung für die Personalisierungsalgorithmen](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058) von Target für Datentypen, Beispielattribute und ihre Benennungskonvention für [!UICONTROL Personalization Insights]. Beachten Sie, dass, obwohl diese Attribute berücksichtigt werden, die individuellen Modelle einer Aktivität nicht unbedingt all diese Attribute im endgültigen Modell verwenden.
* **An Target übergebene Attribute:** Siehe [Hochladen von Daten für die Target-Personalisierungs-Algorithmen](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

Target bietet verschiedene Möglichkeiten, zusätzliche Daten zu übergeben, um den Basis-Datensatz zu erweitern, der für die Erstellung der Personalisierungsalgorithmen in AP- und AT-Aktivitäten eingesetzt wird:

| Datentyp | Beschreibung | Datentyp-Namenskonvention |
|--- |--- |--- |
| Profilattribute, einschließlich Profilskripten, Profilupdate-API und Seitenprofilattributen | Die Informationen, die Sie dem Benutzerprofil in Target hinzugefügt haben.<br>Diese Informationen können aus Profilskripten, aus mit der Profilaktualisierungs-API hochgeladenen Informationen oder aus In-Mbox-Profilparametern stammen, denen „profile“ vorangestellt ist. | `Custom - Profile - [parameter name]` |
| Seitenparameter (auch „Mbox-Parameter“ genannt) | Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden. | `Custom - Mbox Parameter - [parameter name]` |
| Kundenattribute | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verarbeiten Sie die Daten nach dem Hochladen mit Adobe Analytics und Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gemeinsam genutzte Zielgruppen (Adobe Audience Manager oder Adobe Analytics) | Mittels Adobe Audience Manager oder Adobe Analytics erstellte und für Target freigegebene Zielgruppen. | `Custom - Experience Cloud Segment - [segment name]` |
| Aktivitätsinterne(s) Reporting-Zielgruppen/-Segment | Während der Einrichtung in „Ziele und Metriken“ definierte Zielgruppen in Ihrer AP- oder AT-Aktivität. | `Custom - Reporting Segment - [segment name]` |

## Schulungsvideo: Verwenden der Personalization Insights-Berichte

>[!VIDEO](https://video.tv.adobe.com/v/25601/?captions=ger)

For more information, see [Using the Personalization Insights Reports in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).
