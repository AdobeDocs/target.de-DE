---
keywords: partielle Daten; Teildaten; A4T; Diskrepanzen; Analytics für Target; verwaist; virtuelle Report Suite; Phantom; Fehlerbehebung; gelöst; überhöht; unspezifisch
description: Hilfreiche Informationen dazu, wie Sie bei der Verwendung von Analytics als Berichtsquelle die Auswirkungen überhöhter Besuchs- und Besucherzahlen minimieren können.
title: Minimieren überhöhter Besuchs- und Besucherzahlen in A4T
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 97%

---


# Minimieren überhöhter Besuchs- und Besucherzahlen in A4T{#minimizing-inflated-visit-and-visitor-counts-in-a-t}

Hilfreiche Informationen dazu, wie Sie bei der Verwendung von Analytics als Berichtsquelle die Auswirkungen überhöhter Besuchs- und Besucherzahlen minimieren können.

>[!IMPORTANT]
>Am 14. November 2016 hat sich in Adobe Analytics die Art und Weise geändert, in der manche Daten für Kunden per Analytics-Berichterstellung für Target (A4T) verarbeitet werden. Diese Änderungen bewirkten, dass Adobe Target-Daten besser auf das Datenmodell für Adobe Analytics ausgerichtet sind. Diese Änderungen wurden für alle Kunden eingeführt, die A4T verwenden. Diese Änderungen sollen insbesondere das Problem lösen, dass manche Kunden bei Ausführung von Target-Aktivitäten eine überhöhte Anzahl von Besuchern verzeichnet haben.
>
>Diese Änderung ist nicht rückwirkend. Wenn in Ihren historischen Berichten überhöhte Zählerwerte stehen, die Sie gerne von Ihren Berichten ausschließen möchten, können Sie dazu eine virtuelle Report Suite erstellen (wie weiter unten erklärt).
>
>Außerdem wurden verschiedene JavaScript-Bibliotheken aktualisiert, um überhöhten Zählerwerten vorzubeugen. Es wird empfohlen, dass Sie eine Aktualisierung auf die folgenden Bibliotheksversionen (oder neuer) vornehmen:
>
>* Experience Cloud-Besucher-ID-Service: visitorAPI.js, Version 2.3.0 oder neuer.
>* Adobe Analytics: appMeasurement.js, Version 2.1.
>* Adobe Target: at.js-Version 0.9.6 oder höher (ausgenommen Version 1.1.0 bei der Verwendung von Umleitungsangeboten mit A4T).

>
>  
Die mbox.js Bibliothek unterstützt keine Umleitungsangebote in A4T. Ihre Implementierung muss at.js verwenden.

## Was hat sich geändert? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

Wenn [!DNL Adobe Analytics] zum Messen von [!DNL Target]-Aktivitäten verwendet wird (was als A4T bezeichnet wird), erfasst [!DNL Analytics] zusätzliche Daten, die nur dann verfügbar sind, wenn auf der Seite eine [!DNL Target]-Aktivität vorhanden ist. Der Grund dafür ist, dass [!DNL Target]-Aktivitäten ihre Aufrufe zu Beginn der Seite vornehmen, während [!DNL Analytics] seine Datenerfassungsaufrufe für gewöhnlich am Ende der Seite auslöst. In der bisherigen Implementierung von A4T haben wir diese zusätzlichen Daten immer mit eingefügt, wenn eine [!DNL Target]-Aktivität aktiv war. Ab nun werden wir diese zusätzlichen Daten nur noch dann einfügen, wenn sowohl die [!DNL Target]- als auch die [!DNL Analytics]-Tags ausgelöst wurden.

## Warum hat Adobe diese Änderung vorgenommen? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe ist stolz auf die Genauigkeit und Qualität seiner bereitgestellten Daten. Wenn nur das [!DNL Target]-Tag, jedoch nicht das [!DNL Analytics]-Tag ausgelöst wird, verzeichnen wir „partielle Daten“ (manchmal auch als „nicht zuordenbare Treffer“ bezeichnet), die [!DNL Analytics] nicht erfassen würde, wenn keine [!DNL Target]-Aktivität vorhanden wäre. Auch wenn die Aufnahme solcher partiellen Daten in [!DNL Analytics]-Berichten keinen zusätzlichen Informationswert bietet, stellt es doch die Konsistenz mit historischen Daten aus früheren Zeiträumen sicher, in denen Daten ohne laufende [!DNL Target]-Aktivitäten erfasst wurden. Dies könnte für [!DNL Analytics]-Benutzer, die Trends über größere Zeiträume analysieren, zu einem Problem werden. Um die Datenkonsistenz in [!DNL Analytics] sicherzustellen, werden wir alle partiellen Daten ausschließen.

## Welche Ursachen gibt es für partielle Daten? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

Wir haben bei einigen Kunden ein sehr hohes Aufkommen an partiellen Daten in [!DNL Analytics] bemerkt. Das kann aus einer fehlerhaften Implementierung resultieren, aber auch ganz normale Ursachen sind möglich.

Als Ursachen für partielle Daten haben wir die folgenden Punkte festgestellt:

* **Abweichende Report Suite-IDs (Implementierung):** Die während der Aktivitätseinrichtung festgelegte Report Suite stimmt nicht mit der Report Suite für die Seite überein, auf der der Test erfolgt. Das sieht dann so aus, als ob Daten fehlen würden, da die Daten nicht auf [!DNL Analytics]-Servern abgeglichen werden können.
* **Langsame Seite:** [!DNL Target]-Aufrufe erfolgen am Beginn der Seite, [!DNL Analytics]-Aufrufe dagegen meist am Ende der Seite. Bei einer Seite mit einer langsamen Ladegeschwindigkeit besteht daher eine höhere Wahrscheinlichkeit, dass Besucher die Seite verlassen, nachdem zwar der [!DNL Target]-Aufruf, nicht jedoch der [!DNL Analytics]-Aufruf ausgelöst wurde. Dies kann besonders bei mobilen Websites zu einem Problem werden, da dort die Verbindungsgeschwindigkeiten meist niedriger sind.
* **Seitenfehler:** Wenn JavaScript-Fehler auftreten oder andere Szenarien vorliegen, in denen die einzelnen Endpunkte nicht ausgelöst werden (Experience Cloud ID-Service, Target und Analytics), führt dies zu partiellen Daten.
* **Umleitungsangebot(e) in [!DNL Target]Aktivitäten:** Für Umleitungsangebote in Aktivitäten mit A4T muss Ihre Implementation bestimmten Mindestanforderungen entsprechen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58).
* **Alte Versionen der Bibliotheken:** Im Verlauf des letzten Jahres hat Adobe verschiedene Verbesserungen in seinen JavaScript-Bibliotheken ([!DNL appMeasurement.js], `at.js/mbox.js` und `visitorAPI.js`) vorgenommen. Damit soll sichergestellt werden, dass Daten so effizient wie möglich gesendet werden. Weitere Informationen zu Implementierungsanforderungen finden Sie unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543).

## Welches sind die Best Practices zum Reduzieren partieller Daten? {#section_065C38501527451C8058278054A1818D}

Wenn Sie das Aufkommen an partiellen Daten bei der Datenerfassung reduzieren möchten, folgen Sie diesen Schritten:

| Schritt | Aufgabe |
| --- | --- |
| ![Schritt 1](assets/step1_icon.png) | Stellen Sie sicher, dass die in [!DNL Target] ausgewählte Report Suite die gleiche wie die auf der/den Seite(n) ist, auf denen die Aktivität erfolgen soll. |
| ![Schritt 2](assets/step2_icon.png) | Stellen Sie sicher, dass die Bibliotheken visitorAPI.js, AppMeasurement.js und at.js/mbox.js in A4T-kompatiblen Versionen vorliegen. Weitere Informationen zu Implementierungsanforderungen finden Sie unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md). |
| ![Schritt 3](assets/step3_icon.png) | Stellen Sie sicher, dass die SDID in sämtlichen [!DNL Target]- und [!DNL Analytics]-Aufrufen festgelegt ist, die die Seite verlassen. Und achten Sie auch darauf, dass die SDID-Angaben übereinstimmen.<br/>Dazu können Sie mithilfe eines Netzwerkanalyse- oder Debuggingwerkzeugs überprüfen, dass der `mboxMCSDID`-Parameter in dem/den [!DNL Target]-Aufruf(en) mit dem SDID-Parameter im [!DNL Analytics]-Aufruf übereinstimmt. |
| ![Schritt 4](assets/step4_icon.png) | Überzeugen Sie sich, dass die Bibliotheken für die Implementierung in der richtigen Reihenfolge in Ihren Websites geladen werden. Weitere Informationen finden Sie unter  [Analytics für die Target-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Wie lässt sich feststellen, wie viele partielle Daten man hat? {#section_89B663E2824A4805AB934153508A0F4B}

Auch wenn dies nicht direkt in [!DNL Analytics] angegeben ist, können Sie sich an die Adobe Kundenunterstützung wenden, um einen Bericht zu partiellen Daten zu erhalten. Dieser Bericht soll beim Debugging helfen.

## Wie kann man Verlaufstrends ohne partielle Daten anzeigen? {#section_4C9DED560FAD4428B362DDA2064897C3}

Da diese Änderung bei der Verarbeitung nur Daten nach dem Veröffentlichungsdatum (14. November 2016) betrifft, empfehlen wir, dass Sie ein Segment zum Ausschließen partieller Daten erstellen, wenn Sie Ihre historischen Metriken so anpassen möchten, dass sie übereinstimmen.

Die nachfolgenden Informationen bezüglich dieser Änderung enthalten auch Anweisungen darüber, wie Sie das Segment definieren und es auf eine virtuelle Report Suite anwenden, sodass dieses Segment immer auf Ihre [!DNL Analytics]-Ansichten angewendet wird.

Meistens ist ein Treffer in [!DNL Target] auf jeder einzelnen Website mit einem Treffer in [!DNL Analytics] verknüpft. Diese Verknüpfung wird vorgenommen, wenn eine konsistente SDID sowohl im Aufruf von [!DNL Target] als auch von [!DNL Analytics] verwendet wird und eine [!DNL Experience Cloud ID] (MCID) im Aufruf [!DNL Analytics] auf der gleichen Seite enthalten ist. [!DNL Target] verfügt normalerweise ebenfalls über die MCID, wird [!DNL Target] jedoch vor Rückgabe der Besucher-ID aufgerufen, wird der Treffer aufgrund der SDID trotzdem zugewiesen. Außerdem muss der Besucher lange genug auf der Seite bleiben, um einen [!DNL Analytics]-Anruf auslösen zu können, nachdem ein [!DNL Target]-Anruf ausgelöst wurde. Dies ist das Wunschszenario.

**Treffer mit partiellen Daten:** Manchmal bleiben Besucher nicht lange genug auf einer Seite, um einen Aufruf von [!DNL Analytics] auszulösen, während in [!DNL Target] jedoch eine entsprechende MCID vorliegt. Dies führt zu Treffern, zu denen nur partielle Daten vorliegen (d. h. Treffer, zu denen es keine Seitenaufrufe in [!DNL Analytics] gibt). Kehren solche Besucher auf Ihre Seite zurück und sehen sich eine Seite an, die [!DNL Analytics]-Code enthält, werden sie ordnungsgemäß als wiederkehrende Besucher erfasst. Hierbei handelt es sich um Treffer, die nicht aufgezeichnet worden wären, wenn sich auf der Seite nur [!DNL Analytics]-Code befände. Einige Kunden möchten für diese Treffer keine Daten aufzeichnen, da sie bestimmte Metriken (Besuche) sehr stark in die Höhe treiben, andere Metriken (Seitenansichten pro Besuch, Zeit pro Besuch und so weiter) jedoch stark reduzieren. Außerdem werden ihnen Besuche angezeigt, bei denen keine Seiten angesehen wurden. Es gibt jedoch einige gute Gründe, diese Daten trotzdem zu erfassen.

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

**Verwaiste Treffer:** In einigen wenigen Fällen bleiben Besucher nicht lange genug auf einer Seite, um einen Aufruf von Analytics auszulösen, und Target konnte keine passende MCID erfassen. Solche Treffer werden als „verwaiste“ Treffer bezeichnet. Diese Treffer stehen für Kunden, die nur selten zurückkehren, und treiben die Zählungen der Besuche und Besucher unverhältnismäßig stark in die Höhe.

Möchten Sie die Anzahl dieser „verwaisten“ Treffer minimieren, können Sie eine [virtuelle Report Suite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) erstellen, in der diese Treffer nicht erfasst werden.

## Was bedeutet dies für meine [!DNL Target]-Berichterstellung? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Sobald diese Änderung vorgenommen wurde, wird möglicherweise ein Rückgang an neuen Besuchern und Besuchen zu Live-Tests angezeigt, da [!DNL Adobe] eingehende partielle Daten nicht mehr verarbeitet werden. Bei Konversionen und Treffern in anderen [!DNL Analytics]-Metriken ändert sich nichts.
