---
keywords: partielle Daten; Teildaten; A4T; Diskrepanzen; Analytics für Target; verwaist; virtuelle Report Suite; Phantom; Fehlerbehebung; gelöst; überhöht; unspezifisch
description: Erfahren Sie, wie Sie die Auswirkungen überhöhter Besuchs- und Besucherzahlen bei der Verwendung von Analytics for [!DNL Target] (A4t) minimieren können. Erfahren Sie, was "partielle Daten"sind und wie Sie sie reduzieren können.
title: Wie kann ich überhöhte Besuchs- und Besucherzahlen in A4T minimieren?
feature: 'Analytics for Target (A4T) '
exl-id: 308711f7-e630-4f6b-8a6d-a1f36ed7902d
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 47%

---

# Minimieren überhöhter Besuchs- und Besucherzahlen in A4T

Informationen, die Sie dabei unterstützen, die Auswirkungen überhöhter Besuchs- und Besucherzahlen bei der Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) zu minimieren.

>[!IMPORTANT]
>Am 14. November 2016 hat sich in Adobe Analytics die Art und Weise geändert, in der manche Daten für Kunden per Analytics-Berichterstellung für Target (A4T) verarbeitet werden. Diese Änderungen bewirkten, dass Adobe Target-Daten besser auf das Datenmodell für Adobe Analytics ausgerichtet sind. Diese Änderungen wurden für alle Kunden eingeführt, die A4T verwenden. Diese Änderungen sollen insbesondere das Problem lösen, dass manche Kunden bei Ausführung von Target-Aktivitäten eine überhöhte Anzahl von Besuchern verzeichnet haben.
>
>Diese Änderung ist nicht rückwirkend. Wenn in Ihren historischen Berichten überhöhte Zählerwerte stehen, die Sie gerne von Ihren Berichten ausschließen möchten, können Sie dazu eine virtuelle Report Suite erstellen (wie weiter unten erklärt).
>
>Außerdem wurden mehrere JavaScript-Bibliotheken aktualisiert, um überhöhte Werte zu minimieren. Adobe empfiehlt ein Upgrade auf die folgenden Bibliotheksversionen (oder neuer):
>
>* Experience Cloud-Besucher-ID-Service: visitorAPI.js, Version 2.3.0 oder neuer.
>* Adobe Analytics: appMeasurement.js, Version 2.1.
>* Adobe Target: at.js-Version 0.9.6 oder höher (ausgenommen Version 1.1.0 bei der Verwendung von Umleitungsangeboten mit A4T).


## Was hat sich geändert? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

Wenn [!DNL Adobe Analytics] zum Messen von [!DNL Target] Aktivitäten verwendet wird (was als A4T bezeichnet wird), erfasst [!DNL Analytics] zusätzliche Daten, die nicht verfügbar sind, wenn keine [!DNL Target] -Aktivität auf der Seite vorhanden ist. Die [!DNL Target] -Aktivität löst einen -Aufruf am Anfang der Seite aus, [!DNL Analytics] löst jedoch seine Datenerfassungsaufrufe normalerweise am Ende der Seite aus. In der bisherigen Implementierung von A4T enthält Adobe diese zusätzlichen Daten immer dann, wenn eine [!DNL Target] -Aktivität aktiv war. In Zukunft werden diese zusätzlichen Daten in Adobe nur noch dann erfasst, wenn die Tags [!DNL Target] und [!DNL Analytics] ausgelöst wurden.

## Warum hat Adobe diese Änderung vorgenommen? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe ist stolz auf die Genauigkeit und Qualität seiner bereitgestellten Daten. Wenn das Tag [!DNL Target] ausgelöst wird, das Tag [!DNL Analytics] jedoch nicht, zeichnet Analytics &quot;partielle Daten&quot;auf (manchmal auch als &quot;nicht zuordenbare Treffer&quot;bezeichnet). Diese nicht zugewiesenen Treffer werden nicht von [!DNL Analytics] erfasst, wenn keine [!DNL Target] -Aktivität vorhanden ist. Auch wenn die Aufnahme dieser partiellen Daten in die [!DNL Analytics] -Berichterstellung zusätzliche Informationen bietet, stellt es doch die Konsistenz mit historischen Daten aus früheren Zeiträumen sicher, in denen keine [!DNL Target] -Aktivitäten ausgeführt wurden. Diese Situation kann für [!DNL Analytics] -Benutzer, die Trends im Zeitverlauf analysieren, zu Problemen führen. Um die Datenkonsistenz in [!DNL Analytics] zu gewährleisten, schließt die Adobe alle partiellen Daten aus.

## Welche Ursachen gibt es für partielle Daten? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

Bei Adobe sind einige Kunden mit einer hohen Anzahl partieller Daten in [!DNL Analytics] konfrontiert. Hohe Mengen partieller Daten können aus einer fehlerhaften Implementierung resultieren, aber es gibt auch legitime Ursachen.

Als Ursachen für partielle Daten haben wir die folgenden Punkte festgestellt:

* **Abweichende Report Suite-IDs (Implementierung):** Die während der Aktivitätseinrichtung festgelegte Report Suite stimmt nicht mit der Report Suite für die Seite überein, auf der der Test erfolgt. Die Daten können nicht auf [!DNL Analytics]-Servern abgeglichen werden. Daher sieht sie wie partielle Daten aus.
* **Langsame Seiten:** [!DNL Target] -Aufrufe befinden sich oben auf der Seite und  [!DNL Analytics] Aufrufe befinden sich normalerweise am Ende der Seite. Wenn die Seite langsam geladen wird, erhöht dies die Wahrscheinlichkeit, dass ein Besucher die Seite verlässt, nachdem der Aufruf [!DNL Target], jedoch vor dem Aufruf [!DNL Analytics] ausgelöst wurde. Langsame Seiten können besonders bei mobilen Websites problematisch sein, da dort die Verbindungsgeschwindigkeiten häufig geringer sind.
* **Seitenfehler:** Wenn JavaScript-Fehler auftreten oder andere Szenarien vorliegen, in denen nicht alle Touchpoints ausgelöst werden (Experience Cloud-ID-Dienst, Target und Analytics), sind partielle Datenergebnisse.
* **Umleitungsangebote in  [!DNL Target] Aktivitäten:** Für Umleitungsangebote in Aktivitäten, die A4T verwenden, muss Ihre Implementierung bestimmte Mindestanforderungen erfüllen. Darüber hinaus gibt es wichtige Informationen, die Sie kennen müssen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58).
* **Alte Bibliotheksversionen:** Im vergangenen Jahr hat die Adobe verschiedene Verbesserungen an den JavaScript-Bibliotheken (  [!DNL appMeasurement.js],  `at.js` und  `visitorAPI.js`) vorgenommen, um sicherzustellen, dass Daten so effizient wie möglich gesendet werden. Weitere Informationen zu Implementierungsanforderungen finden Sie unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543).

## Welches sind die Best Practices zum Reduzieren partieller Daten? {#section_065C38501527451C8058278054A1818D}

Überprüfen Sie die folgenden Schritte, um die partielle Datenerfassung zu reduzieren:

| Schritt | Aufgabe |
| --- | --- |
| ![Schritt 1](assets/step1_icon.png) | Stellen Sie sicher, dass die in [!DNL Target] ausgewählte Report Suite mit der auf den Seiten übereinstimmt, auf denen die Aktivität angezeigt wird. |
| ![Schritt 2](assets/step2_icon.png) | Stellen Sie sicher, dass sich die Bibliotheken visitorAPI.js, appMeasurement.js und at.js in A4T-kompatiblen Versionen befinden. Weitere Informationen zu Implementierungsanforderungen finden Sie unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md). |
| ![Schritt 3](assets/step3_icon.png) | Stellen Sie sicher, dass die SDID für alle [!DNL Target] - und [!DNL Analytics] -Aufrufe festgelegt wird, die die Seite verlassen, und dass sie übereinstimmen.<br/>Verwenden Sie einen Netzwerk-Analyzer oder ein Debugging-Tool, um sicherzustellen, dass der  `mboxMCSDID` Parameter bei  [!DNL Target] Aufrufen mit dem SDID-Parameter im  [!DNL Analytics] Aufruf übereinstimmt. |
| ![Schritt 4](assets/step4_icon.png) | Überzeugen Sie sich, dass die Bibliotheken für die Implementierung in der richtigen Reihenfolge in Ihren Websites geladen werden. Weitere Informationen finden Sie unter  [Analytics für die Target-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Wie lässt sich feststellen, wie viele partielle Daten man hat? {#section_89B663E2824A4805AB934153508A0F4B}

Auch wenn dies nicht direkt in [!DNL Analytics] angegeben ist, können Sie sich an die Adobe Kundenunterstützung wenden, um einen Bericht zu partiellen Daten zu erhalten. Dieser Bericht soll beim Debugging helfen.

## Wie kann man Verlaufstrends ohne partielle Daten anzeigen? {#section_4C9DED560FAD4428B362DDA2064897C3}

Diese Änderung der Verarbeitung betrifft Daten erst nach dem Veröffentlichungsdatum (14. November 2016). Wenn Sie Ihre historischen Metriken an eine Übereinstimmung anpassen möchten, empfiehlt Adobe, ein Segment zum Ausschließen partieller Daten zu erstellen.

Die nachfolgenden Informationen bezüglich dieser Änderung enthalten auch Anweisungen darüber, wie Sie das Segment definieren und es auf eine virtuelle Report Suite anwenden, sodass dieses Segment immer auf Ihre [!DNL Analytics]-Ansichten angewendet wird.

Meistens ist ein Treffer in [!DNL Target] auf jeder einzelnen Website mit einem Treffer in [!DNL Analytics] verknüpft. Diese Verknüpfung wird vorgenommen, wenn eine konsistente SDID sowohl im Aufruf von [!DNL Target] als auch von [!DNL Analytics] verwendet wird und eine [!DNL Experience Cloud ID] (MCID) im Aufruf [!DNL Analytics] auf der gleichen Seite enthalten ist. [!DNL Target] weist normalerweise auch die MCID auf. Wenn jedoch der -Aufruf vor der Rückgabe der Besucher-ID  [!DNL Target] erfolgt, wird der Treffer aufgrund der SDID trotzdem zugeordnet. Außerdem muss der Besucher lange genug auf der Seite bleiben, um einen [!DNL Analytics]-Anruf auslösen zu können, nachdem ein [!DNL Target]-Anruf ausgelöst wurde. Dieses Szenario ist ideal.

**Treffer mit partiellen Daten:** Manchmal bleiben Besucher nicht lange genug auf einer Seite, um einen Aufruf von [!DNL Analytics] auszulösen, während in [!DNL Target] jedoch eine entsprechende MCID vorliegt. Dieses Szenario führt zu Treffern mit partiellen Daten (Treffer ohne [!DNL Analytics] Seitenansicht). Wenn diese Benutzer zu Ihrer Site zurückkehren und eine Seite anzeigen, die [!DNL Analytics]-Code enthält, werden sie ordnungsgemäß als wiederkehrende Besucher gezählt. Diese Treffer wären verloren gegangen, wenn sich auf der Seite nur [!DNL Analytics] -Code befände. Einige Kunden möchten für diese Treffer keine Daten aufzeichnen, da sie bestimmte Metriken (Besuche) sehr stark in die Höhe treiben, andere Metriken (Seitenansichten pro Besuch, Zeit pro Besuch und so weiter) jedoch stark reduzieren. Sie sehen auch Besuche ohne Seitenansichten. Es gibt jedoch einige gute Gründe, diese Daten trotzdem zu erfassen.

Um solche Treffer mit partiellen Daten zu minimieren, können Sie Ihre Seite so gestalten, dass sie schneller geladen wird, Bibliotheken auf die neueste Version aktualisieren oder eine [virtuelle Report Suite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) erstellen, in der solche Treffer ausgeschlossen sind. Eine schrittweise Anleitung finden Sie unter [Virtual Report Suites erstellen](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) im *Leitfaden zu Analytics-Komponenten*.

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

**Verwaiste Treffer:** In einigen wenigen Fällen bleiben Besucher nicht lange genug auf einer Seite, um einen Aufruf von Analytics auszulösen, und Target konnte keine passende MCID erfassen. Diese Treffer werden von Adobe als &quot;verwaiste&quot;Treffer definiert. Diese Treffer stehen für Kunden, die nur selten zurückkehren, und treiben die Zählungen der Besuche und Besucher unverhältnismäßig stark in die Höhe.

Möchten Sie die Anzahl dieser „verwaisten“ Treffer minimieren, können Sie eine [virtuelle Report Suite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) erstellen, in der diese Treffer nicht erfasst werden.

## Was bedeutet dies für meine [!DNL Target]-Berichterstellung? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Sobald diese Änderung vorgenommen wurde, wird möglicherweise ein Rückgang an neuen Besuchern und Besuchen bei Live-Tests angezeigt, da [!DNL Adobe] eingehende partielle Daten nicht mehr verarbeitet. Bei Konversionen und Treffern in anderen [!DNL Analytics]-Metriken ändert sich nichts.
