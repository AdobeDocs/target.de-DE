---
keywords: Traffic-Schätzung;Automated Personalization;App;Traffic schätzen
description: Verwenden Sie die [!UICONTROL Traffic-Schätzung] um zu beurteilen, ob genügend Traffic für eine [!UICONTROL Automated Personalization]-Aktivität vorhanden ist.
title: Wie viel Traffic wird für eine erfolgreiche Aktivität vom Typ [!UICONTROL Automated Personalization] benötigt?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
TQID: 'https://experienceleague.adobe.com/rLjNgDlAWK-r9Zv7083vo-PdWTPy3aHGS4fXEGeTdnY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: ddd4fa83540294ee229b87f041bc2245ba9a3464
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 8%
---
# Schätzen des für einen erfolgreichen Test erforderlichen Traffics {#traffic-estimator}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie mit der **[!UICONTROL Traffic-Schätzung]** überprüfen können, ob Ihre **[!UICONTROL Automated Personalization]**-Aktivität über ausreichend Traffic verfügt, um erfolgreich zu sein.

>[!ENDSHADEBOX]

Die [!DNL Adobe Target]Traffic **[!UICONTROL Schätzung]** liefert Feedback, mit dem Sie wissen, ob Sie über ausreichend Traffic für eine erfolgreiche **[!UICONTROL Automated Personalization]** (AP)-Aktivität verfügen. AP-Aktivitäten verwenden mehrere Angebotskombinationen, daher ist es wichtig zu wissen, wie viel Traffic erforderlich ist, um aussagekräftige Ergebnisse zu liefern. Die **[!UICONTROL Traffic-Schätzung]** nutzt Statistiken zu Ihrer Seite und der Anzahl der getesteten Erlebnisse, um die Menge an Traffic und die Testdauer zu schätzen, die für den Erfolg der Aktivität erforderlich sind.

Die **[!UICONTROL Traffic-Schätzung]** bestimmt, ob ausreichend Traffic vorhanden ist, um personalisierte Modelle zu generieren, indem die geschätzten Seitenimpressionen und die typische Konversionsrate für die Seiten verglichen werden. Idealerweise gewährleistet die korrekte Stichprobengröße bei einer erfolgreichen Aktivität, dass personalisierter Inhalt innerhalb von 50 % der Dauer der Aktivität oder innerhalb von 14 Tagen bereit ist (je nachdem, welcher Fall zuerst eintritt). Dieser Prozess lässt ausreichend Zeit für den Erhalt personalisierter Inhalte und das Erlernen der bereitzustellenden Inhalte.

[!DNL Target] stellt Erlebnisse nach dem Zufallsprinzip bereit, bis die Personalisierungsalgorithmen erstellt wurden. Das Häkchensymbol neben jedem Angebot zeigt an, wenn das Modell für dieses Angebot bereit ist und [!DNL Target] mit der Bereitstellung personalisierter Inhalte beginnen kann. Die Steigerung wird erst erwartet, wenn die Modelle bereit sind. Daher können Sie mit der visuellen Anzeige die richtigen Erwartungen festlegen. Verwenden Sie die **[!UICONTROL Traffic-Schätzung]** im **[!UICONTROL Visual Experience Composer]** (VEC), um eine Richtlinie zu erhalten, wann die Modelle bereit sind.

>[!NOTE]
>
>Ein personalisiertes Modell wird nicht immer bereitgestellt, selbst wenn der Traffic ausreicht. [!DNL Target] erstellt und testet das Modell, stellt es jedoch nur bereit, wenn es eine bessere Leistung als eine zufällige Auswahl von Erlebnissen erzielt. Wenn das Modell nicht besser als zufällig ist, unterscheiden sich die Angebote wahrscheinlich nicht genug voneinander. Machen Sie in diesem Fall die Angebote visuell unterschiedlicher, wenn die Nachricht ähnlich ist, oder ändern Sie die Nachricht selbst.

## Traffic-Schätzung verwenden {#use-traffic-estimator}

Beim Erstellen einer **[!UICONTROL Automated Personalization]**-Aktivität können Sie mit der **[!UICONTROL Traffic-Schätzung]** überprüfen, ob der Traffic auf Ihrer Seite ausreicht, damit die personalisierten Modelle rechtzeitig bereit sind. Wenn Sie diese Prüfung vor dem Start der Aktivität ausführen, wird ein Test vermieden, mit dem nicht genügend Besucher erreicht werden können, um personalisierte Inhalte bereitzustellen. Außerdem erfahren Sie, wie Sie die Anzahl der Angebotskombinationen oder die Dauer der Aktivität anpassen können, wenn der Traffic nicht ausreicht.

1. Rufen Sie über die ]**-Aktivität von**[!UICONTROL  die Seite **[!UICONTROL Erlebnisse]** des **[!UICONTROL Visual Experience Composer] auf.

1. Klicken Sie auf **[!UICONTROL Traffic]**-Symbol (![Traffic-Schätzsymbol](/help/main/assets/icons/Gauge2.svg)).

   Die **[!UICONTROL Traffic-Schätzung]** wird geöffnet. Um das Fenster zu verlassen, klicken Sie erneut auf das Symbol.

   ![Benutzeroberfläche der Traffic-Schätzung](assets/ap-est.png)

1. Geben Sie die typische Konversionsrate (oder die von dieser Aktivität erwartete Konversionsrate), die geschätzten Aktivitätsimpressionen pro Tag und die Testdauer an.

   Die **[!UICONTROL Traffic-Schätzung]** verwendet diese Metriken, um zu bestimmen, welche Anpassungen erforderlich sind, um einen erfolgreichen Test auszuführen.

   | Metrik | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Anzahl der Angebote]** | Diese Metrik wird automatisch anhand der Anzahl der Erlebnisse berechnet, die im Rahmen Ihrer Aktivität nach allen Ausschlüssen erstellt werden. |
   | **[!UICONTROL Typische Konversionsrate]** | Diese Metrik wird als Prozentsatz ausgedrückt, basierend auf Ihrer Schätzung oder früheren Daten aus Ihrem Analysesystem. |
   | **[!UICONTROL Geschätzte Besuche pro Tag]** | Diese Metrik stellt die Anzahl der Besuche pro Tag dar, die Besucherinnen und Besucher, die die Aktivität anzeigen können, auf der Grundlage der Targeting-Kriterien verzeichnen. Diese Metrik könnte auf Ihren Analysedaten basieren. Bei dieser Zahl muss es sich um Besuche und nicht um Unique Visitors handeln. |
   | **[!UICONTROL Testdauer]** | Die Anzahl der Tage, binnen derer Sie die Aktivität ausführen möchten. |



1. Überprüfen Sie die Ergebnisse. Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte.

   Wenn Sie beispielsweise viele Kombinationen testen und Ihre Konversionsrate und Impressions zu niedrig sind, zeigt die **[!UICONTROL Traffic-Schätzung]** an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic gering ist, kann die **[!UICONTROL Traffic-Schätzung]** eine niedrigere Anzahl von Angebotskombinationen vorschlagen, sodass Sie den Test über die gewünschte Anzahl von Tagen ausführen können.

   ![Traffic-Schätzung mit angezeigten Werten und Ergebnissen](assets/ap-est-no.png)

1. Wenn Sie nicht über ausreichend Traffic verfügen, ziehen Sie die folgenden Optionen in Betracht:

   * Verwenden Sie eine [**[!UICONTROL Automatisches Targeting]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md)-Aktivität anstelle von **[!UICONTROL Automated Personalization]** um Erlebnisse mit mehreren Angebotsänderungen in einer Erlebnisvariante zu erstellen.
   * Verringern Sie die Anzahl der Angebotskombinationen innerhalb Ihrer **[!UICONTROL Automated Personalization]**-Aktivität.
   * Erhöhen Sie die Dauer der Aktivität.

1. Passen Sie die Zahlen an, bis **[!UICONTROL Traffic-Schätzung]** anzeigt, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.

   Wenn der Traffic ausreichend ist, wird **[!UICONTROL Symbol „Traffic]** ein grünes Häkchen angezeigt. Wenn der Traffic nicht ausreicht, wird als Symbol ein roter Warnhinweis angezeigt.

   ![Traffic-Schätzung zeigt eine ausreichende Traffic-Meldung an](assets/ap-est-yes.png)
