---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 95d8bd994ffdb1d256b7eb0aea1a2462b40ce530
workflow-type: tm+mt
source-wordcount: '2221'
ht-degree: 7%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 21. August 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Die Informationen in diesem Artikel werden häufig aktualisiert, insbesondere vor Versionen.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.8.3 (21. August 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!UICONTROL Activities]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem beim Speichern von Aktivitäten aufgrund fehlerhafter Eigenschaftsdaten ein Fehler wegen ungültiger Benutzereingabe** wurde: Beim Versuch, vorhandene Aktivitäten zu speichern, trat ein kritischer Fehler auf. Die Fehlermeldung wies auf eine ungültige Benutzereingabe hin und verwies insbesondere auf einen nicht erkannten Inhalt mit dem Eigenschaftsnamen in der JSON-Payload. Insbesondere wurden neue Aktivitäten, die dieselbe Eigenschaft verwenden, erfolgreich gespeichert, was darauf hindeutet, dass das Problem auf die alten Aktivitätsdaten beschränkt wurde. Der Prozess zur Erstellung von Aktivitäten verarbeitet jetzt korrekt veraltete Eigenschaftskonfigurationen, verhindert ungültige Eingabefehler und stellt ein konsistentes Speicherverhalten für neue und vorhandene Aktivitäten sicher. (TGT-53507)
* **Es wurde ein Problem behoben, das Kunden daran hinderte, eine Aktivität aufgrund eines InvalidProperty.Json-Fehlers zu speichern**: Beim Versuch, eine Aktivität in der aktualisierten Benutzeroberfläche zu speichern, trat ein Fehler auf, auch ohne dass Änderungen vorgenommen wurden. Die Fehlermeldung weist auf eine ungültige JSON-Struktur hin: „Ungültige JSON. Unbekannter Eigenschaftsname „content“. Speicherort: Zeile - 1, Spalte - 432.“ Dieses Problem wurde durch eine nicht erkannte Eigenschaft in der Anfrage-Payload verursacht und wurde nun behoben. Kunden können Aktivitäten erfolgreich speichern, ohne diesen Fehler zu bemerken. (TGT-53513)
* **Es wurde ein Problem behoben, bei dem geplante Aktivitäten bis zur Seitenaktualisierung fälschlicherweise einen [!UICONTROL Live] angezeigt**: Kunden merkten an, dass beim Planen der Live-Schaltung einer Aktivität zu einem späteren Zeitpunkt der Status sofort als [!UICONTROL Live] anstatt als [!UICONTROL Scheduled] angezeigt wurde. Dies führte zu Verwirrung, obwohl die Bestätigungsmeldung korrekt angibt, dass die Aktivität geplant war. Beim Aktualisieren der Seite wurde die Statusanzeige korrigiert. Dieses Problem wurde jetzt behoben, und geplante Aktivitäten zeigen den Status Geplant korrekt an, ohne dass eine Aktualisierung erforderlich ist. (TGT-52937)

+++

**[!UICONTROL Analytics for Target](A4T)**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem Kundinnen und Kunden während des Prozesses zur Erstellung einer Aktivität keine Report Suite-Namen eingeben konnten**: Kundinnen und Kunden, die [!DNL Adobe Analytics] als Berichtsquelle während des Prozesses zur Erstellung einer Aktivität verwenden, konnten keine Eingaben in die [!UICONTROL Report Suite] Dropdown-Liste vornehmen, um nach bestimmten Report Suites zu suchen. Dies wirkte sich auf Workflows für Unternehmen mit einer großen Anzahl von Report Suites aus, bei denen das manuelle Scrollen die Einrichtung erheblich verzögerte. Die Dropdown-Liste war nicht alphabetisch geordnet und reagierte nicht konsistent auf eingegebene -Eingaben, was es schwierig machte, Report Suites wie „Office + Store - Web - Produktion“ zu finden. Dieses Problem wurde behoben, und Kundinnen und Kunden können jetzt effizient suchen, indem sie Report Suite-Namen eingeben. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem abgelaufene „Zeitrahmen“-Zielgruppen das Speichern von Aktivitäten blockierten, selbst nachdem sie entfernt worden waren**: Kunden konnten Aktivitäten in der aktualisierten Benutzeroberfläche aufgrund eines Fehlers im Zusammenhang mit abgelaufenen „Zeitrahmen“-Zielgruppen nicht speichern. Selbst nach dem Entfernen der betroffenen Zielgruppe blieb die Fehlermeldung bestehen: „Aktivität enthält Zielgruppe mit ungültigem Zeitrahmen.“ Dieses Problem trat auf, weil das System die Zielgruppe „Nur Aktivität“ weiterhin validierte, auch wenn sie nicht mehr verwendet wurde. Das Verhalten wurde durch Zeitzonendiskrepanzen weiter kompliziert. Die Validierungslogik wurde korrigiert, und Kundinnen und Kunden können jetzt Aktivitäten speichern, ohne diesen Fehler zu bemerken. (TGT-53517)

+++

**[!UICONTROL Experience Fragment]s**

+++Details anzeigen
* **Es wurde ein Problem behoben, das Kunden daran hinderte, Experience Fragments mithilfe von [!UICONTROL Insert Before] oder [!UICONTROL Insert After] in der Benutzeroberfläche einzufügen** Kunden traten beim Versuch, [!UICONTROL Experience Fragments] mithilfe der Optionen „Einfügen vor“ oder „Einfügen nach“ in der aktualisierten Benutzeroberfläche in eine Aktivität einzufügen, auf einen Fehler auf. Die angezeigte Fehlermeldung war: „Angebotsinhalte müssen genau ein HTML-Element enthalten.“ Dieses Problem war spezifisch für die aktualisierte Benutzeroberfläche und trat in der vorherigen Version nicht auf. Dieses Problem wurde nun behoben, und Kundinnen und Kunden können [!UICONTROL Experience Fragments] erfolgreich einfügen, ohne diesen Fehler zu bemerken. (TGT-53442)

+++

**[!UICONTROL Offer decisions]**

+++Details anzeigen
* **Es wurde ein Problem behoben, das Kunden daran hinderte, Entscheidungsangebote zu bearbeiten und bestimmte Seitenelemente in der aktualisierten Benutzeroberfläche auszuwählen**: Während des aktualisierten Prozesses zum Erstellen von Aktivitäten konnten Kunden keine vorhandenen Entscheidungsangebote bearbeiten oder bestimmte Seitenelemente in Visual Experience Composer (VEC) auswählen. Entscheidungsangebote wurden fälschlicherweise als HTML-Angebote angezeigt und während der Bearbeitung vorgenommene Änderungen wurden nicht gespeichert. Darüber hinaus konnten bestimmte regionale URLs, z. B. die Japan-Site, nicht ordnungsgemäß in VEC geladen werden, was die Erstellung und Aktualisierung von Aktivitäten blockierte. Entscheidungsangebote werden jetzt korrekt angezeigt, Seitenelemente können erwartungsgemäß ausgewählt werden und regionale URLs werden ordnungsgemäß in VEC geladen, wodurch die volle Bearbeitungsfunktion wiederhergestellt wird. (TGT-53425)
* **Es wurde ein Problem behoben, bei dem [!UICONTROL Offer Decision] Selektoren nach dem Speichern nicht unerwartet geändert und geändert werden konnten**: Im aktualisierten Prozess zur Erstellung von Aktivitäten konnten Kundinnen und Kunden den [!UICONTROL Offer Decision] nicht wie beabsichtigt ändern. Der Versuch, den Selektor zu ändern, schlug fehl und der Selektor wurde nach dem Speichern auf einen falschen Wert zurückgesetzt. Dieses Verhalten führte dazu, dass das Entscheidungsangebot aus Visual Experience Composer (VEC) verschwand und weitere Bearbeitungen blockiert wurden. Selektoränderungen werden jetzt korrekt beibehalten, und Entscheidungsangebote bleiben nach dem Speichern im VEC sichtbar und bearbeitbar.(TGT-53433)
* **Es wurde ein Problem behoben, bei dem [!UICONTROL Offer Decisions] nach dem Speichern aus der Aktivität verschwanden**: [!UICONTROL Offer Decisions], die während des Erstellungsprozesses der Aktivität hinzugefügt wurden, wurden nach dem Speichern und erneuten Öffnen der Aktivität nicht beibehalten. Dieses Problem trat beim Bearbeiten dynamischer Inhalte und beim Einfügen ([!UICONTROL Offer Decisions] bestimmten Selektoren und Eigenschaften) auf. [!UICONTROL Offer Decisions] bleiben nun nach dem Speichern korrekt erhalten, und die Selektoren bleiben intakt, was ein konsistentes Targeting- und Bearbeitungsverhalten gewährleistet. (TGT-53434)

+++

**[!DNL Recommendations]**

+++Details anzeigen
* **Es wurde ein Problem in [!DNL Recommendations] Benutzeroberfläche behoben, bei dem der CSV-Download für benutzerdefinierte Kriterien den Fehler 404 zurückgab**: Es wurde ein Problem behoben, bei dem Kunden die CSV-Datei für benutzerdefinierte Kriterien beim Erstellen der Aktivität nicht herunterladen konnten. Der Download-Link funktioniert jetzt ordnungsgemäß, sodass Kunden benutzerdefinierte Kriterien wie erwartet exportieren können. (TGT-51966)
* **Inkonsistentes Laden von Bildern in[!UICONTROL Catalog Search]** behoben: Es wurde ein Problem behoben, bei dem Miniaturansichten und Bilder in [!UICONTROL  Catalog Search] beim Erstellen von Aktivitäten nicht konsistent geladen wurden. Bilder werden nur angezeigt, wenn die Spalte „Miniatur-URL“ sichtbar war und einige Produktbilder nach Navigations- oder Suchaktionen teilweise oder überhaupt nicht geladen wurden. Das Ladeverhalten des Bildes wurde stabilisiert, und Miniaturansichten werden nun unabhängig von der Sichtbarkeit der Spalte oder von Navigationsaktionen zuverlässig angezeigt. (TGT-52778)
* **Es wurde ein Problem behoben, durch das die Bearbeitung einer Empfehlung in einem duplizierten Erlebnis das ursprüngliche Erlebnis beeinträchtigte**: Kundinnen und Kunden berichteten, dass die Änderung einer Empfehlung in einem duplizierten Erlebnis das ursprüngliche Erlebnis unbeabsichtigt veränderte. Insbesondere nach dem Duplizieren von Erlebnis B im Prozess zur Erstellung der Aktivität und dem Bearbeiten des Designs oder der Kriterien wurden dieselben Änderungen im ursprünglichen Erlebnis B widergespiegelt, obwohl es sich um separate Entitäten handelte. Duplizierte Erlebnisse behalten jetzt separate Konfigurationen bei, sodass Änderungen an einem Erlebnis keine Auswirkungen auf das Original haben. (TGT-53369)
* **Es wurde ein Problem behoben, bei dem Änderungen an einem duplizierten Erlebnis das ursprüngliche Erlebnis in einer Aktivität unbeabsichtigt beeinträchtigten**: Kundinnen und Kunden berichteten, dass beim Duplizieren eines Erlebnisses innerhalb einer Aktivität und beim Zuweisen einer neuen Zielgruppe alle Änderungen am Design oder an den Kriterien des duplizierten Erlebnisses auch im ursprünglichen Erlebnis widergespiegelt wurden. Dieses Problem trat auf, obwohl keine direkten Änderungen an der Originalversion vorgenommen wurden, was die Möglichkeit beeinträchtigte, unabhängige Varianten innerhalb derselben Aktivität zu erstellen. Der Prozess zur Erstellung von Aktivitäten isoliert jetzt doppelte Erlebnisse korrekt, sodass Änderungen an einem Erlebnis keine Auswirkungen auf das Original haben. (TGT-53361)
* **Es wurde ein Problem behoben, bei dem der [!UICONTROL Recommendation Catalog] zeitweise nicht in der Lage war, vollständige Produktattributdaten anzuzeigen**: In der aktualisierten [!DNL Recommendations]-Benutzeroberfläche trat ein Problem auf, bei dem bestimmte Produktattribute, wie z. B. Nachricht, nicht konsistent in den [!UICONTROL Catalog Search] Ergebnissen angezeigt wurden, obwohl die Daten im Feed vorhanden waren. Aufgrund dieses Problems mussten Kundinnen und Kunden die Sichtbarkeit der Spalten manuell neu konfigurieren, um die fehlenden Werte abzurufen. [!UICONTROL Catalog Search] zeigt jetzt zuverlässig alle konfigurierten Attribute an, sodass keine manuellen Spaltenzurücksetzungen mehr erforderlich sind. (TGT-52769)
* **Es wurde ein Problem behoben, bei dem eine [!UICONTROL Front Promotion] in einer Live-Aktivität nicht deaktiviert werden konnte**: Versuche, eine [!UICONTROL Front Promotion] in einer Live-Aktivität zu deaktivieren, wurden nicht gespeichert. Nach dem Auswählen und Deaktivieren von [!UICONTROL Change Promotion] blieb die Promotion bei der Neubearbeitung der Aktivität aktiv, was Aktualisierungen an Empfehlungskonfigurationen verhinderte. Die Einstellungen für die Promotion werden jetzt korrekt gespeichert, sodass Kundinnen und Kunden Promotion-Aktionen in Live-Aktivitäten wie erwartet deaktivieren oder ändern können. (TGT-53231)
* **Es wurde ein Problem behoben, bei dem die Aktivierung einer [!DNL Recommendations]-[!UICONTROL Promotion] ohne Daten eine unklare Fehlermeldung auslöste**: Die Aktivierung einer [!UICONTROL Front] oder [!UICONTROL Back Promotion] in einer [!DNL Recommendations]-Aktivität ohne Angabe erforderlicher Werte führte zu einer allgemeinen „Fehler bei ungültiger Eingabe“-Meldung. Das zugrunde liegende Problem war ein fehlendes Konfigurationsfeld, aber die Fehlermeldung gab die Ursache nicht klar an, was die Fehlerbehebung erschwerte. Der Prozess zur Erstellung von Aktivitäten bietet jetzt eine klare und verwertbare Fehlermeldung, wenn erforderliche Felder wie `collectionId` oder Regeln fehlen, sodass Kunden Konfigurationsprobleme schnell identifizieren und beheben können. (TGT-52616)
* **Es wurde ein Problem behoben, das die Anzeige der [!UICONTROL Product]-Liste im modalen [!UICONTROL Edit] auf der Registerkarte [!UICONTROL Recommendations] verhinderte**: Kundinnen und Kunden konnten die gefilterte Produktliste nicht anzeigen, wenn sie eine [!UICONTROL collection] oder [!UICONTROL exclusion] auf der Registerkarte [!UICONTROL Recommendations] bearbeiteten. Es wurde erwartet, dass die Liste in Echtzeit auf der Grundlage der angewendeten Regeln aktualisiert wird, aber sie erschien nicht wie beabsichtigt. Dieses Problem wurde behoben, und die Produktliste wird jetzt korrekt angezeigt und dynamisch aktualisiert, wenn Regeln geändert werden. (TGT-53481)
* **Es wurde ein Problem mit dem Layout des Dialogfelds „Details anzeigen“ in der aktualisierten Benutzeroberfläche behoben**: Das Layout des Modals „Details anzeigen“ in der aktualisierten Benutzeroberfläche wurde geändert, um die Klarheit und Benutzerfreundlichkeit zu verbessern. Das Dialogfeld enthält jetzt zwei Registerkarten:
   * Registerkarte [!UICONTROL Details] : Zeigt alle relevanten Informationen zum ausgewählten Element an.
   * Registerkarte [!UICONTROL Inventory] : Zeigt alle Produkte an, die nach den aktuellen Sammlungs- und Ausschlussregeln gefiltert wurden.

  Diese Verbesserung hilft Kunden, im Rahmen des Prozesses zur Erstellung von Aktivitäten einfacher durch artikelspezifische Daten und den Inventarkontext zu navigieren und diese zu verstehen. (TGT-53503)

   * **Es wurde ein Problem behoben, bei dem entfernte Promotions in Recommendations-Aktivitäten nach dem Speichern wieder auftraten**: Kunden meldeten, dass nach dem Entfernen von [!UICONTROL front] oder [!UICONTROL back] Promotions aus [!DNL Recommendations] Aktivitäten und dem Speichern der Aktivität die Promotions beim erneuten Öffnen weiterhin angezeigt wurden. Dieses Problem trat sowohl in der Staging- als auch in der Produktionsumgebung auf und hatte Auswirkungen auf den aktualisierten Prozess der Aktivitätserstellung. Das Problem wurde behoben. Promotions, die aus einer Aktivität entfernt wurden, bleiben jetzt nach dem Speichern korrekt erhalten. (TGT-53490)

+++

**Berichte**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem der [!UICONTROL Automated Segments]-Bericht Zielgruppenwerte null anzeigte**: Kunden meldeten, dass [!UICONTROL Automated Segments] in Aktivitätsberichten für Zielgruppendaten null zeigten, was eine genaue Analyse der Segmentleistung verhinderte. Dieses Problem trat beim Zugriff auf den Abschnitt [!UICONTROL Reports] und bei der Auswahl von [!UICONTROL Automated Segments] auf, obwohl gültige Zielgruppendaten erwartet wurden. [!UICONTROL Automated Segments] zeigt jetzt die Zielgruppenwerte korrekt an, was zuverlässige Berichte und Segmentierungseinblicke gewährleistet. (TGT-52793)

+++

**Single Page Applications (SPAs)**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem der SPA-Status in der aktualisierten Benutzeroberfläche beim Wechsel zwischen [!UICONTROL Browse]- und [!UICONTROL Design] zurückgesetzt wurde**: Kunden berichteten, dass der Wechsel zwischen [!UICONTROL Browse]- und [!UICONTROL Design] in der aktualisierten Benutzeroberfläche dazu führte, dass der Web-Editor neu geladen wurde, wodurch der Status der SPA zurückgesetzt wurde. Durch dieses Problem wurden Workflows unterbrochen und Kunden mussten die Informationen erneut eingeben. Das Problem wurde behoben. Der SPA-Status wird jetzt beim Wechseln zwischen Modi beibehalten, was ein reibungsloseres und konsistenteres Erlebnis bei der Erstellung von Aktivitäten gewährleistet. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Details anzeigen
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das die Progression zum [!UICONTROL Targeting] Schritt in AP-Aktivitäten blockierte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden in [!UICONTROL Targeting] (AP)-Aktivitäten nicht zum [!UICONTROL Automated Personalization] Schritt wechseln konnten, es sei denn, zwei Standorte wurden hinzugefügt. Dieses Verhalten unterschied sich vom vorherigen Erlebnis, bei dem ein einzelner Standort mit mehreren Angeboten ausreichend war. Die Anforderung wurde korrigiert, sodass Kundinnen und Kunden weiterhin Einzelspeicherort-Setups als Teil ihrer API-Workflows verwenden können. (TGT-53426)
* **Es wurde ein Problem behoben, bei dem der neue Prozess zum Erstellen von Aktivitäten den Parameter „fmt=png-alpha“ für transparente Bilder nicht**: In der aktualisierten Benutzeroberfläche enthielten Bilder, die während des Prozesses zum Erstellen von Aktivitäten eingefügt wurden, nicht mehr standardmäßig den Parameter &quot;`fmt=png-alpha`&quot;, was zu einem Verlust der Transparenz führte. Dieses Verhalten unterschied sich von dem der vorherigen Benutzeroberfläche, die den -Parameter automatisch an Bild-URLs angehängt hat, wobei transparente Hintergründe beibehalten wurden. Der Prozess zur Erstellung von Aktivitäten wendet nun den `fmt=png-alpha`-Parameter korrekt auf Bild-URLs an, wenn Transparenz erforderlich ist, um ein konsistentes Rendering transparenter Assets sicherzustellen. (TGT-52615)
* **Es wurde ein Problem behoben, das Kunden daran hinderte, in der aktualisierten Benutzeroberfläche nach Report Suites zu suchen**: In der aktualisierten Benutzeroberfläche erlaubte die Dropdown-Liste [!UICONTROL Report Suites] im [!UICONTROL Goals & Settings]-Abschnitt Kunden nicht, einzugeben und zu suchen, was es schwierig machte, bestimmte Report Suites zu finden, insbesondere für Mandanten mit einer großen Anzahl von Einträgen. Im Gegensatz zur vorherigen Benutzeroberfläche war die Liste nicht sortiert und es fehlte eine eingabebasierte Filterung. Dieses Problem wurde behoben. Kunden können jetzt tippen, um Report Suites zu suchen und zu filtern, und so die in der alten Benutzeroberfläche verfügbaren Funktionen wiederherstellen. (TGT-53514)

+++

**[!UICONTROL Workspaces]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem Kundinnen und Kunden, die auf einen einzigen Arbeitsbereich beschränkt waren, Aktivitäten aus anderen Arbeitsbereichen anzeigen konnten**: Kundinnen und Kunden mit Zugriff auf einen Arbeitsbereich konnten unerwartet Aktivitäten in allen Arbeitsbereichen anzeigen, wenn sie [!UICONTROL All Workspaces] im Prozess zur Erstellung einer Aktivität auswählten. Diese Sichtbarkeit birgt das Risiko von unbeabsichtigten Änderungen an Live-Aktivitäten in anderen Arbeitsbereichen, die sich möglicherweise auf die Website-Leistung auswirken. Die Zugriffssteuerungen für Workspace wurden verbessert, um sicherzustellen, dass Kunden nur Aktivitäten in ihrem zugewiesenen Arbeitsbereich anzeigen und mit ihnen interagieren können. (TGT-53101)
* **Es wurde ein Problem behoben, bei dem eine Kundin oder ein Kunde Aktivitäten aus der [!UICONTROL Default Workspace] anzeigen konnte, ohne Zugriff zu haben:** Eine Kundin oder ein Kunde mit eingeschränktem Zugriff auf den Staging-Arbeitsbereich konnte Aktivitäten aus der [!UICONTROL Default Workspace] über den Prozess zur Erstellung einer Aktivität anzeigen. Dieses Verhalten trat trotz korrekter Backend-Konfiguration und Zugriffsrechten auf. Die Zugriffskontrollen für Workspace wurden verbessert, um sicherzustellen, dass Kunden Aktivitäten nur innerhalb ihres zugewiesenen Arbeitsbereichs sehen können.(TGT-53297)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
