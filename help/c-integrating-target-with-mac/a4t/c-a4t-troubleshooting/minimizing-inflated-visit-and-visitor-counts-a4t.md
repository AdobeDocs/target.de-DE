---
keywords: partielle Daten; Teildaten; A4T; Diskrepanzen; Analytics für Target; verwaist; virtuelle Report Suite; Phantom; Fehlerbehebung; gelöst; überhöht; unspezifisch
description: Erfahren Sie, wie Sie bei der Verwendung von Analytics for [!DNL Target] (A4t) die Auswirkungen überhöhter Besuchs- und Besucher-Zählungen minimieren können. Erfahren Sie, was "partielle Daten"sind und wie Sie diese reduzieren können.
title: Wie kann ich überhöhte Besuchs- und Besucher-Zählungen in A4T minimieren?
feature: Analytics for Target (A4T)
exl-id: 308711f7-e630-4f6b-8a6d-a1f36ed7902d
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 48%

---

# Minimieren überhöhter Besuchs- und Besucherzahlen in A4T

Informationen, die Sie bei der Minimierung der Auswirkungen überhöhter Besuchs- und Besucher-Zahlen unterstützen, wenn Sie [!DNL Adobe Analytics] als Berichte-Quelle für [!DNL Adobe Target] (A4T) verwenden.

>[!IMPORTANT]
>Am 14. November 2016 hat sich in Adobe Analytics die Art und Weise geändert, in der manche Daten für Kunden per Analytics-Berichterstellung für Target (A4T) verarbeitet werden. Diese Änderungen bewirkten, dass Adobe Target-Daten besser auf das Datenmodell für Adobe Analytics ausgerichtet sind. Diese Änderungen wurden für alle Kunden eingeführt, die A4T verwenden. Diese Änderungen sollen insbesondere das Problem lösen, dass manche Kunden bei Ausführung von Target-Aktivitäten eine überhöhte Anzahl von Besuchern verzeichnet haben.
>
>Diese Änderung ist nicht rückwirkend. Wenn in Ihren historischen Berichten überhöhte Zählerwerte stehen, die Sie gerne von Ihren Berichten ausschließen möchten, können Sie dazu eine virtuelle Report Suite erstellen (wie weiter unten erklärt).
>
>Außerdem wurden mehrere JavaScript-Bibliotheken aktualisiert, um überhöhte Zählerwerte zu minimieren. Adobe empfiehlt die Aktualisierung auf die folgenden Bibliotheksversionen (oder höher):
>
>* Experience Cloud-Besucher-ID-Service: visitorAPI.js, Version 2.3.0 oder neuer.
>* Adobe Analytics: appMeasurement.js, Version 2.1.
>* Adobe Target: at.js-Version 0.9.6 oder höher (ausgenommen Version 1.1.0 bei der Verwendung von Umleitungsangeboten mit A4T).

>
>  
Die mbox.js Bibliothek unterstützt keine Umleitungsangebote in A4T. Ihre Implementierung muss at.js verwenden.

## Was hat sich geändert? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

Wenn [!DNL Adobe Analytics] zur Messung von [!DNL Target]-Aktivitäten (als A4T bezeichnet) verwendet wird, erfasst [!DNL Analytics] zusätzliche Daten, die nicht verfügbar sind, wenn keine [!DNL Target]-Aktivität auf der Seite vorhanden ist. Die [!DNL Target]-Aktivität löst einen Aufruf am Seitenanfang aus, [!DNL Analytics] löst jedoch in der Regel die Datenerfassungsaufrufe am Seitenende aus. Bei der bisherigen Implementierung von A4T enthält die Adobe diese zusätzlichen Daten, sobald eine [!DNL Target]-Aktivität aktiv war. In Zukunft werden diese zusätzlichen Daten in der Adobe nur dann berücksichtigt, wenn die Tags [!DNL Target] und [!DNL Analytics] ausgelöst wurden.

## Warum hat Adobe diese Änderung vorgenommen? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe ist stolz auf die Genauigkeit und Qualität seiner bereitgestellten Daten. Wenn das [!DNL Target]-Tag ausgelöst wird, das [!DNL Analytics]-Tag jedoch nicht, zeichnet Analytics &quot;partielle Daten&quot;auf (manchmal auch als &quot;nicht zugewiesene Treffer&quot;bezeichnet). Diese nicht zugewiesenen Treffer werden nicht von [!DNL Analytics] erfasst, wenn keine [!DNL Target]-Aktivität vorhanden ist. Obwohl die Einbeziehung dieser partiellen Daten in den Berichte [!DNL Analytics] zusätzliche Informationen bietet, führt sie auch zu Inkonsistenzen mit historischen Daten aus Zeiträumen, in denen keine [!DNL Target]-Aktivitäten ausgeführt wurden. Diese Situation kann Probleme für [!DNL Analytics]-Benutzer verursachen, die Trends im Laufe der Zeit analysieren. Zur Gewährleistung der Datenkonsistenz in [!DNL Analytics] schließt die Adobe alle Teildaten aus.

## Welche Ursachen gibt es für partielle Daten? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

Bei einigen Kunden, die in [!DNL Analytics] eine hohe Rate von partiellen Daten haben, ist die Adobe auf einige Kunden gestoßen. Hohe Raten von partiellen Daten können aus einer fehlerhaften Implementierung resultieren, aber es gibt auch legitime Ursachen.

Als Ursachen für partielle Daten haben wir die folgenden Punkte festgestellt:

* **Abweichende Report Suite-IDs (Implementierung):** Die während der Aktivitätseinrichtung festgelegte Report Suite stimmt nicht mit der Report Suite für die Seite überein, auf der der Test erfolgt. Die Daten können auf [!DNL Analytics]-Servern nicht abgeglichen werden, daher sieht es wie Teildaten aus.
* **Langsame Seiten:** [!DNL Target] Aufrufe befinden sich oben auf der Seite und  [!DNL Analytics] Aufrufe befinden sich normalerweise am unteren Rand der Seite. Wenn die Seite langsam geladen wird, erhöht dies die Wahrscheinlichkeit, dass ein Besucher die Seite verlässt, nachdem der Aufruf [!DNL Target] ausgelöst wurde, jedoch vor dem Aufruf [!DNL Analytics]. Langsame Seiten können besonders auf mobilen Websites problematisch sein, auf denen die Verbindungen häufig langsamer sind.
* **Seitenfehler:** Wenn JavaScript-Fehler oder andere Szenarien vorliegen, in denen kein Touchpoint ausgelöst wird (Experience Cloud-ID-Dienst, Zielgruppe und Analytics), werden partielle Datenergebnisse angezeigt.
* **Angebot in  [!DNL Target] Aktivität umleiten:** Für Umleitungs-Angebot in Aktivitäten, die A4T verwenden, muss Ihre Implementierung bestimmte Mindestanforderungen erfüllen. Darüber hinaus gibt es wichtige Informationen, die Sie wissen müssen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58).
* **Alte Bibliotheksversionen: Im** vergangenen Jahr wurden die JavaScript-Bibliotheken (  [!DNL appMeasurement.js],  `at.js/mbox.js`und  `visitorAPI.js`) durch die Adobe verbessert, um sicherzustellen, dass Daten so effizient wie möglich gesendet werden. Weitere Informationen zu Implementierungsanforderungen finden Sie unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543).

## Welches sind die Best Practices zum Reduzieren partieller Daten? {#section_065C38501527451C8058278054A1818D}

Überprüfen Sie die folgenden Schritte, um die teilweise Datenerfassung zu reduzieren:

| Schritt | Aufgabe |
| --- | --- |
| ![Schritt 1](assets/step1_icon.png) | Stellen Sie sicher, dass die in [!DNL Target] ausgewählte Report Suite mit der auf den Seiten, auf denen die Aktivität angezeigt wird, identisch ist. |
| ![Schritt 2](assets/step2_icon.png) | Stellen Sie sicher, dass die Bibliotheken visitorAPI.js, appMeasurement.js, at.js/mbox.js in A4T-kompatiblen Versionen verfügbar sind. Weitere Informationen zu Implementierungsanforderungen finden Sie unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md). |
| ![Schritt 3](assets/step3_icon.png) | Stellen Sie sicher, dass die SDID für alle [!DNL Target]- und [!DNL Analytics]-Aufrufe eingestellt wird, die die Seite verlassen, und dass sie übereinstimmen.<br/>Verwenden Sie einen Netzwerkanalysator oder ein Debugging-Tool, um sicherzustellen, dass der  `mboxMCSDID` Parameter bei  [!DNL Target] Aufrufen mit dem SDID-Parameter im  [!DNL Analytics] Aufruf übereinstimmt. |
| ![Schritt 4](assets/step4_icon.png) | Überzeugen Sie sich, dass die Bibliotheken für die Implementierung in der richtigen Reihenfolge in Ihren Websites geladen werden. Weitere Informationen finden Sie unter  [Analytics für die Target-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Wie lässt sich feststellen, wie viele partielle Daten man hat? {#section_89B663E2824A4805AB934153508A0F4B}

Auch wenn dies nicht direkt in [!DNL Analytics] angegeben ist, können Sie sich an die Adobe Kundenunterstützung wenden, um einen Bericht zu partiellen Daten zu erhalten. Dieser Bericht soll beim Debugging helfen.

## Wie kann man Verlaufstrends ohne partielle Daten anzeigen? {#section_4C9DED560FAD4428B362DDA2064897C3}

Diese Änderung der Verarbeitung betrifft Daten erst nach dem Veröffentlichungsdatum (14. November 2016). Wenn Sie Ihre historischen Metriken passend anpassen möchten, empfiehlt Adobe, ein Segment zum Ausschließen partieller Daten zu erstellen.

Die nachfolgenden Informationen bezüglich dieser Änderung enthalten auch Anweisungen darüber, wie Sie das Segment definieren und es auf eine virtuelle Report Suite anwenden, sodass dieses Segment immer auf Ihre [!DNL Analytics]-Ansichten angewendet wird.

Meistens ist ein Treffer in [!DNL Target] auf jeder einzelnen Website mit einem Treffer in [!DNL Analytics] verknüpft. Diese Verknüpfung wird vorgenommen, wenn eine konsistente SDID sowohl im Aufruf von [!DNL Target] als auch von [!DNL Analytics] verwendet wird und eine [!DNL Experience Cloud ID] (MCID) im Aufruf [!DNL Analytics] auf der gleichen Seite enthalten ist. [!DNL Target] hat normalerweise auch die MCID, aber wenn der Aufruf vor der Rückgabe der Besucher-ID  [!DNL Target] erfolgt, wird der Treffer aufgrund der SDID immer noch zugewiesen. Außerdem muss der Besucher lange genug auf der Seite bleiben, um einen [!DNL Analytics]-Anruf auslösen zu können, nachdem ein [!DNL Target]-Anruf ausgelöst wurde. Dieses Szenario ist ideal.

**Treffer mit partiellen Daten:** Manchmal bleiben Besucher nicht lange genug auf einer Seite, um einen Aufruf von [!DNL Analytics] auszulösen, während in [!DNL Target] jedoch eine entsprechende MCID vorliegt. Dieses Szenario führt zu Treffern mit partiellen Daten (Treffern ohne [!DNL Analytics]-Ansicht). Wenn diese Benutzer zu Ihrer Site zurückkehren und eine Ansicht mit [!DNL Analytics]-Code erstellen, werden sie ordnungsgemäß als wiederkehrende Besucher gezählt. Diese Treffer wären verloren gegangen, wenn Sie nur [!DNL Analytics]-Code auf der Seite hätten. Einige Kunden möchten für diese Treffer keine Daten aufzeichnen, da sie bestimmte Metriken (Besuche) sehr stark in die Höhe treiben, andere Metriken (Seitenansichten pro Besuch, Zeit pro Besuch und so weiter) jedoch stark reduzieren. Sie sehen auch Besuche ohne Ansichten der Seite. Es gibt jedoch einige gute Gründe, diese Daten trotzdem zu erfassen.

Um solche Treffer mit partiellen Daten zu minimieren, können Sie Ihre Seite so gestalten, dass sie schneller geladen wird, Bibliotheken auf die neueste Version aktualisieren oder eine [virtuelle Report Suite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) erstellen, in der solche Treffer ausgeschlossen sind. Eine schrittweise Anleitung finden Sie unter [Virtual Report Suites erstellen](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) im *Analytics-Komponentenleitfaden*.

Die folgende Abbildung zeigt die Segmentdefinition für die virtuelle Report Suite:

![](assets/ts_a4t.png)

Beim Erstellen der virtuellen Report Suite müssen Sie für die Segmentdefinition die folgende Konfiguration festlegen (wie in der Abbildung oben gezeigt):

* **Treffer anzeigen:**
* Analytics for Target: Vorhanden
* Und
* Seitenansichten: Nicht vorhanden
* Und
* Benutzerspezifische Linkinstanzen: Nicht vorhanden
* Und
* Downloadlinkinstanzen: Nicht vorhanden
* Und
* Exitlinkinstanzen: Nicht vorhanden

**Verwaiste Treffer:** In einigen wenigen Fällen bleiben Besucher nicht lange genug auf einer Seite, um einen Aufruf von Analytics auszulösen, und Target konnte keine passende MCID erfassen. Diese Treffer werden von der Adobe als &quot;verwaiste&quot;Treffer definiert. Diese Treffer stehen für Kunden, die nur selten zurückkehren, und treiben die Zählungen der Besuche und Besucher unverhältnismäßig stark in die Höhe.

Möchten Sie die Anzahl dieser „verwaisten“ Treffer minimieren, können Sie eine [virtuelle Report Suite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) erstellen, in der diese Treffer nicht erfasst werden.

## Was bedeutet dies für meine [!DNL Target]-Berichterstellung? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Sobald diese Änderung eintritt, werden möglicherweise weniger neue Besucher und Besuche bei Live-Tests angezeigt, da [!DNL Adobe] keine eingehenden partiellen Daten verarbeitet. Bei Konversionen und Treffern in anderen [!DNL Analytics]-Metriken ändert sich nichts.
