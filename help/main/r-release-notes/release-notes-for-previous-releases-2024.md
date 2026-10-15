---
keywords: Versionshinweise;Vorabversionshinweise;zukünftige Verbesserungen;zukünftige Fehlerbehebungen;zukünftige Funktionen;bevorstehende Version
description: Dieser Abschnitt enthält eine Liste der Funktionen, Verbesserungen und Fehlerbehebungen früherer Versionen von Adobe Target.
title: Welche Funktionen sind in früheren Versionen enthalten?
feature: Release Notes
source-git-commit: 53cd01d2406b8a2f8560fe380ebb5044872e6711
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 32%
---
# Versionshinweise für vorherige Versionen

Versionshinweise für frühere Versionen von [!DNL Adobe Target] einschließlich Versionshinweisen für [!DNL Target Standard/Premium], die [!DNL Target]-Plattform und die [!DNL Target] JavaScript-Bibliothek (at.js).

Die Versionshinweise sind in absteigender Reihenfolge nach Monat und Jahr der Veröffentlichung aufgeführt.

>[!NOTE]
>
>Informationen zu den Target-Versionen (Plattform und Target Standard/Premium) finden Sie unter [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A).

## Versionshinweise für 2024

### [!DNL Adobe Experience Platform Web SDK] Optimierung `__view__` Umfangs (22. Oktober 2024)

Zwischen dem 22. Juli 2024 und dem 15. August 2024 optimierte das [!DNL Target]-Team den `__view__` und verbesserte die Genauigkeit der Berichte zu Aktivitätsimpressionen, Besuchen und Besuchern. Diese Optimierung zielt darauf ab, Berichtsdaten für automatisch gerenderte Vorschläge automatisch zu erfassen, und sollte für die meisten Konten transparent sein.

Für alle neuen [!DNL Adobe Experience Platform Web SDK]-Kunden ist diese Optimierung aktiviert. Kunden, die von at.js migriert sind und die unten stehenden Implementierungsschritte nicht befolgt haben, haben die Optimierung jedoch deaktiviert. Wir fordern diese Kundinnen und Kunden dringend auf, ihre Implementierungen bis zum 3. Februar 2025 zu überprüfen. Nach diesem Datum aktivieren wir die Optimierung für alle Kunden. Wird die Umsetzung bis dahin nicht überprüft und angepasst, kann dies Auswirkungen auf die Berichte haben, wie unten erwähnt. Wenden Sie sich an [!DNL Adobe Customer Care], wenn Sie bestätigen müssen, ob Ihre Implementierung betroffen ist, oder wenn Sie mehr Zeit benötigen, um Ihre Implementierung anzupassen.

>[!IMPORTANT]
>
>Wenn Sie Ihre Implementierungsprüfung nicht bis zum 3. Februar 2025 abschließen und keine Probleme beheben können, können Sie eine einmalige Verlängerung um sechs Monate anfordern. Stellen Sie sicher, dass Ihre Anfrage bis zum 31. Januar 2025 gesendet wird. Adobe prüft Ihre Anfrage und entscheidet darüber.

Um im Falle des manuellen Vorschlags-Renderings von dieser Optimierung zu profitieren, überprüfen Sie Ihre [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep/aep-web-sdk-overview){target=_blank}, um sicherzustellen, dass Sie Benachrichtigungen senden, nachdem Sie Erlebnisse manuell gerendert haben, oder wenn Sie die `applyPropositions`-Methode (oder die entsprechende [!DNL Launch]-Aktion als Helper) zum Rendern von Erlebnissen verwenden.

Zu den häufigsten Szenarien, in denen Erlebnisse manuell gerendert werden, gehören:

* Verwenden von JSON-Angeboten
* Verwenden eines benutzerdefinierten Entscheidungsumfangs in einer Aktivität, die im [[!UICONTROL formularbasierten Experience Composer“ erstellt &#x200B;]](/help/main/c-experiences/form-experience-composer.md)
* Keine Verwendung von `renderDecisions: true` beim Abrufen einer Aktivität, die mit dem [!UICONTROL formularbasierten Experience Composer] erstellt wurde, der den globalen `__view__` verwendet

Wenn Benachrichtigungen nicht wie in [Rendern personalisierter Inhalte](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} im Handbuch *Datenerfassung* dokumentiert sind, fehlen Berichtsdaten möglicherweise in [!DNL Target] und in [Analytics for Target-](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In bestimmten Szenarien kann es vorkommen, dass Traffic falsch aufgeteilt wird, da die Berichtsdaten nicht erfasst werden. Oder in anderen Szenarien, bei denen dasselbe Ereignis wiederholt gemeldet wird.

Überprüfen Sie je nach Implementierung, ob sich [!DNL Analytics]- und A4T-Berichte auswirken.

Die [!DNL Platform Web SDK] unterstützt zwei Implementierungstypen für das Rendering von Erlebnissen und Personalisierungen:

* **Einzelaufruf für Personalisierung und Messung.**

  Ursprünglich wird empfohlen, den Einzelaufruf-Ansatz für die [!DNL Platform Web SDK] zugunsten des Aufspaltungs-Ansatzes zu verwerfen. Adobe empfiehlt allen neuen Implementierungen, den neuen Split-Call-Ansatz zu verwenden, und empfiehlt Bestandskunden, auch auf die Split-Call-Methode umzustellen.

  Wenn Sie den Einzelaufruf-Ansatz weiterhin verwenden, werden Sie möglicherweise die folgenden unerwarteten Änderungen in Ihren [!DNL Analytics] feststellen:

  * Ein Rückgang der Absprünge.
  * Treffer von A4T und [!UICONTROL Seitenansicht] werden nicht zugeordnet, was die Durchführung bestimmter Aufschlüsselungen und Korrelationen Ihrer A4T-Berichte mithilfe [!DNL Analytics] eVars und Ereignisse erschwert.

* **Aufrufe zur Aufspaltung (auch als Seitenanfang und -ende-Ereignisse bezeichnet).**

  Dieser Implementierungstyp ist der neue [Aufspaltungs-Implementierungsansatz](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank} der von [!DNL Adobe] empfohlen wird. Bei diesem Ansatz hat die neue Optimierung keine Auswirkungen auf [!DNL Analytics]- oder A4T-Berichte.

Bei Fragen wenden Sie sich an die [Adobe-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

### at.js-Version 2.11.6 (29. September 2024)

* Es wurde ein Problem behoben, das dazu führte, dass [!DNL Target] mit Umleitungsangeboten in [!UICONTROL Visual Experience Composer] (VEC) oder [!UICONTROL Form-Based Experience Composer) nicht korrekt &#x200B;].

Weitere Informationen zu at.js-Versionen finden Sie unter [at.js](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank} im *Adobe Target-Entwicklerhandbuch*.

### [!DNL Target]-Reporting in [!DNL Adobe Customer Journey Analytics] (8. Mai 2024)

Die Integration zwischen [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/customer-journey-analytics){target=_blank} und [!DNL Target] bietet leistungsstarke Analyse- und Zeitspartools für Ihr Optimierungsprogramm.

Die wichtigsten Vorteile des Verwendens von [!DNL Customer Journey Analytics] als Berichtsquelle für [!DNL Target] sind folgende:

* Marketing-Fachleute können jederzeit dynamisch [!DNL Customer Journey Analytics]-Erfolgsmetriken auf [!DNL Target] Aktivitätsberichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Marketing-Experten können [!DNL Customer Journey Analytics] Funktionen nutzen, z. B. das [Experimentier-Bedienfeld](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, um die Personalisierung ihrer Website weiter zu analysieren.

Weitere Informationen finden Sie unter [Target-Reporting in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

### [!UICONTROL Visual Experience Composer] Helper-Erweiterung (23. April 2024)

Die Vorgängerversion der [!DNL Target] Visual Experience Composer-Helper-Erweiterung wurde mit Manifest V2 erstellt. [!DNL Google] hat angekündigt, dass mit Manifest V2 erstellte Erweiterungen ab Juni 2024 nicht mehr zulässig sind. Weitere Informationen finden Sie unter [[!UICONTROL Visual Experience Composer] Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] empfiehlt Kundinnen und Kunden, so schnell wie möglich auf die neuere [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) umzusteigen.

### Aktualisierungen für `Browser:iPad` und `Browser:iPhone` in [!UICONTROL Browser]-Zielgruppenattributen (30. April 2024)

| Aktualisierungen | Details |
|--- |--- |
| [!UICONTROL Browser:iPad] und [!UICONTROL Browser:iPhone] aktualisiert in [Browser-Attribute](/help/main/c-target/c-audiences/c-target-rules/browser.md) werden beim Erstellen von Zielgruppen verwendet. | Mit [!DNL Adobe Target] können Sie [Zielgruppen für eines von mehreren Kategorieattributen erstellen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), einschließlich der Besucherinnen und Besucher, die zum Besuch Ihrer Seite einen [bestimmten Browser oder bestimmte Browser-Optionen](/help/main/c-target/c-audiences/c-target-rules/browser.md) verwenden.<P>Ab der [!DNL Target] Standard/Premium-Version 24.3.1 (4.–6. März 2024) werden integrierte, über die Target-Benutzeroberfläche erstellte Zielgruppen wie `Browser:iPad` und `Browser:iPhone` aktualisiert, um ein korrektes Targeting für [!DNL iPad] und [!DNL iPhone] mit `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` und `profile.mobile.isTablet` durchzuführen.<P>Diese Aktualisierung erfordert keine Maßnahmen auf Kundenseite.<p><B>Wichtig</b>: Damit Kundinnen und Kunden eine korrekte Zielgruppenbestimmung für [!DNL iPad] und [!DNL iPhone] in Profilskripten (und JavaScript-Segmenten) durchführen können, müssen manuelle Änderungen auf Kundenseite bis zum **30. April 2024** vorgenommen werden. Beispiele für alternative Einstellungen, die manuell geändert werden müssen, finden Sie unter [Updates für [!DNL iPad] und [!DNL iPhone] in [!UICONTROL Browser] Zielgruppenattribute](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

### [!UICONTROL Visual Editing Helper]-Erweiterung (14. März 2024)

Diese Version enthält die folgenden Verbesserungen und Fehlerbehebungen für die [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)-Erweiterung für [!DNL Google Chrome]:

* Der iFrame-Lademechanismus wurde beim Authoring auf den Websites von Kunden verbessert.
* Es wurde ein Fehler behoben, der dazu führte, dass die Erweiterung Cookies duplizierte, während das Authoring in [!UICONTROL Visual Experience Composer] (VEC) durchgeführt wurde.

### [!DNL Target] Standard/Premium 23.3.1 (4. bis 6. März 2024)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Die Logik zur Berechnung der Anzahl eindeutiger Selektoren in einer Aktivität wurde korrigiert. (TGT-47878)
* Es wurde ein Problem behoben, das dazu führte[!UICONTROL &#x200B; dass &#x200B;]Multivarianz-(MVT)-Aktivitäten, die mit der Berichterstellung [!UICONTROL Analytics for Target] (A4T) konfiguriert waren, nicht ordnungsgemäß angezeigt wurden. (TGT-47490)
* Die Warnmeldung, die im Reporting angezeigt wird, wenn ein Erlebnis ohne Traffic als Kontrollerlebnis verwendet wird, wurde verbessert. (TGT-47537)
* Es wurden zahlreiche Backend- und Lokalisierungskorrekturen hinzugefügt.

### [!DNL Target] Standard/Premium 24.1.1 (22., 23. und 25. Januar 2024)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* [!UICONTROL Analytics for Target] (A4T)-Aktivitäten mit Umsatzzielmetriken zeigten nicht den „Umsatz“ als Spaltennamen an, und die Umsatzmetrik wurde nicht im ($)-Format im Reporting angezeigt. Dies war ein kosmetisches Problem, das behoben wurde. (TGT-46995)
* Ein Problem mit nicht ordnungsgemäßer Berichtsdatierung wurde behoben. (TGT-47396)
* Es wurde ein Problem behoben, das dazu führte, dass auf der Seite [!UICONTROL Alle Aktivitäten] ein falscher Status angezeigt wurde, nachdem Kundinnen und Kunden eine Aktivität über das Symbol [!UICONTROL Mehr Aktionen] aktiviert oder deaktiviert hatten. (TGT-47367)
* Es wurde ein Fehler behoben, der dazu führte[!UICONTROL &#x200B; dass der Bericht „Wichtige Attribute] für einen einzelnen Kunden nicht angezeigt wurde. (TGT-47272)
* Ein Fehler, bei dem beim Versuch, die Option „Authentifizierung erfordern“ zu aktivieren, die Meldung „Ungültige Payload“ angezeigt wurde, wurde behoben. (TGT-47195)
* Verschiedene lokalisierte Zeichenfolgen in der [!DNL Target]-Benutzeroberfläche wurden aktualisiert.
