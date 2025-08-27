---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: be371f3631d79c65c632a23776ab08de21b031eb
workflow-type: tm+mt
source-wordcount: '2610'
ht-degree: 7%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 27. August 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Die Informationen in diesem Artikel werden häufig aktualisiert, insbesondere vor Versionen.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.8.4 (28. August 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!UICONTROL Activities]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem geplante Aktivitäten in der aktualisierten Benutzeroberfläche während des Erstellungsprozesses der Aktivität fälschlicherweise den Status &quot;[!UICONTROL Live]&quot;**: Aktivitäten mit zukünftigen Aktivierungsdaten zeigen jetzt korrekt den Status &quot;[!UICONTROL Scheduled]&quot; an. (TGT-53187)
* **Geplante Aktivitäten haben fälschlicherweise einen [!UICONTROL Live] Status angezeigt, bis die Seite aktualisiert wurde**: Kunden meldeten, dass beim Planen der Live-Schaltung einer Aktivität zu einem späteren Zeitpunkt der Status zunächst als [!UICONTROL Live] statt als [!UICONTROL Scheduled] angezeigt wurde. Dies führte zu Verwirrung, obwohl die Bestätigungsmeldung das richtige Zeitplanverhalten angibt. Der Aktivitätsstatus spiegelt nun unmittelbar nach dem Speichern die [!UICONTROL Scheduled] korrekt wider, ohne dass die Seite aktualisiert werden muss. (TGT-52937)
* **Änderungen an duplizierten Erlebnissen haben sich unbeabsichtigt auf das ursprüngliche Erlebnis ausgewirkt**: Kundinnen und Kunden berichteten, dass beim Duplizieren eines Erlebnisses innerhalb einer Aktivität und beim Zuweisen einer neuen Zielgruppe alle Änderungen am duplizierten Erlebnis - wie Design oder Kriterien - auch im ursprünglichen Erlebnis widergespiegelt wurden. Dies verhinderte die Erstellung unabhängiger Varianten und beeinträchtigte Produktions-Workflows. Duplizierte Erlebnisse können jetzt unabhängig bearbeitet werden, ohne dass die Originalversion betroffen ist. (TGT-53361)
* **Es wurde ein Problem behoben, das Kunden daran hinderte, eine Aktivität aufgrund eines `InvalidProperty.Json` Fehlers zu speichern**: Zuvor trat beim Versuch, eine Aktivität zu speichern, ohne Änderungen vorzunehmen, der Fehler „Ungültige Benutzereingabe“ auf. Der Fehler wurde durch den nicht erkannten Eigenschaftsnamen „content“ in der JSON-Payload verursacht. Dieses Problem wurde behoben, und Aktivitäten können jetzt erfolgreich in der aktualisierten Benutzeroberfläche gespeichert werden, auch wenn keine Änderungen vorgenommen wurden. (TGT-53513)

+++

**Analytics for Target (A4T)**

+++Details anzeigen
* **Beim Erstellen von A4T-Aktivitäten können keine Report Suite-Namen eingegeben**: Kunden konnten keine Eingaben in die Dropdown-Liste &quot;[!UICONTROL Report Suite]&quot; vornehmen, wenn sie [!UICONTROL Analytics] als Berichtsquelle in der aktualisierten Benutzeroberfläche ausgewählt hatten.  Dieses Problem machte es schwierig, bestimmte Report Suites zu finden, insbesondere für Organisationen mit großen Listen. Die Dropdown-Liste unterstützt jetzt die Eingabe und Suche nach Namen, was die Effizienz beim Erstellen von Aktivitäten verbessert. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++Details anzeigen
* **Abgelaufene „Zeitrahmen“-Zielgruppen blockierten die Aktivitätsspeicherung selbst nach dem Entfernen**: Zuvor konnten Kundinnen und Kunden eine Aktivität nicht speichern, wenn sie zuvor eine abgelaufene „Zeitrahmen“-Zielgruppe enthalten hatte - auch nachdem diese Zielgruppe entfernt wurde. Dieses Problem wurde durch eine verzögerte Validierung in der Zielgruppe „Nur Aktivität“ verursacht, die weiterhin Trigger aufwies. Aktivitäten können jetzt erwartungsgemäß gespeichert werden, sobald abgelaufene Zielgruppen entfernt wurden. (TGT-53517)
* **Zusätzliche Seiten und mehrere Zielgruppen sind nach dem Speichern einer Aktivität verschwunden**: Zuvor hatten Kundinnen und Kunden, die eine [!UICONTROL A/B Test] Aktivität im Prozess zur Aktivitätserstellung erstellt hatten, nach dem Speichern einen Verlust von konfigurierten zusätzlichen Seiten und mehreren Zielgruppen. Dieses Verhalten war unerwartet und führte bei der Einrichtung zu Verwirrung. Diese Konfigurationen bleiben nun nach dem Speichern der Aktivität korrekt erhalten. (TGT-52357)

+++

**Entscheidungsangebote**

+++Details anzeigen
* **Entscheidungsangebote können nicht bearbeitet oder bestimmte Seitenelemente im aktualisierten VEC ausgewählt werden**: Kunden haben in der aktualisierten Benutzeroberfläche mehrere Probleme festgestellt, die ihre Fähigkeit blockiert haben, vorhandene Aktivitäten zu aktualisieren oder neue zu erstellen:

   * Entscheidungsangebote wurden fälschlicherweise als HTML-Angebote angezeigt, was Bearbeitungen verhinderte.
   * Bestimmte Seitenelemente konnten im VEC nicht ausgewählt werden.
   * Änderungen, die während der Bearbeitung vorgenommen wurden, wurden nicht gespeichert.
   * Bestimmte regionale URLs konnten nicht ordnungsgemäß in VEC geladen werden, was manuelle Cookie-Anpassungen erforderlich machte.

  Kunden können jetzt Entscheidungsangebote bearbeiten, Seitenelemente genau auswählen und Änderungen wie erwartet speichern. Regionale Seiten werden auch in VEC korrekt geladen. (TGT-53425)

* **Angebotsentscheidungs-Selektoren konnten nach dem Speichern nicht unerwartet geändert und geändert werden**: Kundinnen und Kunden meldeten, dass bei der Anwendung von Angebotsentscheidungen in der aktualisierten Benutzeroberfläche der Selektor nicht von seinem Standardwert geändert werden konnte. Versuche, den Selektor zu ändern (z. B. auf `#tf-cq-hr or body`), wurden ignoriert, und nach dem Speichern der Aktivität wurde der Selektor durch einen generischen Wert wie `#cdq_element_0` ersetzt. Dieses Problem führte dazu, dass das Angebot aus Visual Experience Composer (VEC) verschwand und weitere Bearbeitungen blockiert wurden. Kunden können jetzt Angebotsentscheidungs-Selektoren wie beabsichtigt ändern, und gespeicherte Selektoren bleiben ohne unerwartete Änderungen korrekt erhalten. (TGT-53433)
* **Angebotsentscheidungen verschwanden nach dem Speichern aus Aktivitäten**: Kundinnen und Kunden berichteten, dass Angebotsentscheidungen, die auf Seitenelemente in der aktualisierten Benutzeroberfläche angewendet wurden, nach dem Speichern der Aktivität nicht mehr sichtbar waren. In einigen Fällen wurde der Selektor unerwartet geändert und das Angebot konnte bei der erneuten Bearbeitung nicht in VEC gerendert werden. Angebotsentscheidungen bleiben nach dem Speichern korrekt erhalten, und die Selektoren bleiben stabil, sodass Angebote wie erwartet sichtbar und bearbeitbar sind. (TGT-53434)

+++

**Experience Fragments**

+++Details anzeigen
* **Kunden erhalten einen Fehler beim Einfügen von [!UICONTROL Experience Fragments] mit [!UICONTROL Insert Before] oder[!UICONTROL Insert After]**: Kunden erhalten einen Fehler beim Versuch, [!UICONTROL Experience Fragments] mithilfe der [!UICONTROL Insert Before]- oder [!UICONTROL Insert After]-Optionen in der aktualisierten Benutzeroberfläche in eine Aktivität einzufügen. Die folgende Fehlermeldung wurde angezeigt:

  „Angebotsinhalte müssen genau ein HTML-Element enthalten.“

  Dieses Problem war spezifisch für die aktualisierte Benutzeroberfläche und trat in der vorherigen Version nicht auf. Sie wurde jetzt behoben, und Kunden können [!UICONTROL Experience Fragments] erfolgreich einfügen, ohne diesen Fehler zu bemerken. (TGT-53432)

* **Fehlermeldung beim Hinzufügen eines [!UICONTROL Experience Fragment] zu einer Aktivität**: Zuvor hatten Kundinnen und Kunden, die versuchten, einen [!UICONTROL Experience Fragment] mit der Option [!UICONTROL Insert Before] oder [!UICONTROL Insert After] einzufügen, den Fehler: „Angebotsinhalte müssen genau ein HTML-Element enthalten.“ Dieser Fehler trat auf, obwohl das Fragment gültig war und in der veralteten Benutzeroberfläche akzeptiert wurde. Dazu gehörte ein Umschalter zur Unterstützung dieser Konfiguration. Das Problem wurde in der aktualisierten VEC behoben. (TGT-53442)

+++

**Lokalisierung**

+++Details anzeigen
* **Popup-Nachrichten im [!UICONTROL Goals & Settings]-Schritt wurden nicht lokalisiert**: Zuvor hatten Kundinnen und Kunden beim Eingeben nicht unterstützter Zeichen - wie Emojis - in das Feld [!UICONTROL Objective] während des Erstellungsprozesses der Aktivität eine nicht lokalisierte Popup-Nachricht erhalten. Popup-Meldungen werden nun ordnungsgemäß in allen unterstützten Sprachen lokalisiert, was ein konsistentes und benutzerfreundliches Erlebnis auf globaler Ebene gewährleistet. (TGT-52251)
* **Eine Zeichenfolge im [!UICONTROL Create Audience]-Dialogfeld wurde nicht lokalisiert**: Zuvor war die Meldung „Wählen Sie mindestens ein Start- oder Enddatum für „Wiederholt sich nicht“ im [!UICONTROL Create Audience]-Modal bei der Konfiguration von Zeitrahmenattributen nicht lokalisiert. Die Zeichenfolge ist jetzt ordnungsgemäß in allen unterstützten Sprachen lokalisiert, was im [!UICONTROL Audiences]-Workflow ein konsistentes Kundenerlebnis auf globaler Ebene gewährleistet. (TGT-52253)
* **Die QuickInfo im [!UICONTROL Create Audience]-Dialogfeld war nicht lokalisiert**: Zuvor, als Kunden nach der Eingabe nicht unterstützter Zeichen (wie Emojis) in das Feld Zielgruppenname den Mauszeiger über die Fehler-QuickInfo bewegten, schien die QuickInfo nicht lokalisiert. Die QuickInfo zeigt jetzt ordnungsgemäß lokalisierte Nachrichten in allen unterstützten Sprachen an, um ein konsistentes und barrierefreies Erlebnis im [!UICONTROL Audiences]-Workflow sicherzustellen. (TGT-52254)

+++

**[!DNL Recommendations]**

+++Details anzeigen
* **[!UICONTROL Front Promotion] in Live-Aktivität kann nicht deaktiviert werden**: Es wurde ein Problem behoben, bei dem Kundinnen und Kunden die [!UICONTROL Front Promotion] in Live-Aktivitäten über die aktualisierte Benutzeroberfläche nicht deaktivieren konnten. Änderungen, die während des Erstellungsprozesses einer Aktivität im Promotion-Abschnitt vorgenommen wurden, bleiben jetzt erwartungsgemäß erhalten, um eine genaue Konfiguration der Live-Aktivitäten in [!UICONTROL Product Catalog Search] sicherzustellen. (TGT-53231)
* **Die Bearbeitung der Empfehlung eines duplizierten Erlebnisses wirkte sich auf das ursprüngliche Erlebnis aus**: Kundinnen und Kunden berichteten, dass beim Duplizieren eines Erlebnisses innerhalb einer Aktivität und beim Ändern des Empfehlungsentwurfs oder der Kriterien im Duplikat diese Änderungen unbeabsichtigt auf das ursprüngliche Erlebnis angewendet wurden.  Dieses Problem verhinderte die Erstellung unabhängiger Varianten und störte das erwartete Verhalten im aktualisierten Prozess der Aktivitätserstellung. Duplizierte Erlebnisse können jetzt unabhängig bearbeitet werden, ohne dass die Originalversion betroffen ist. (TGT-53369)
* **Produktliste kann beim Bearbeiten einer Sammlung oder eines Ausschlusses auf der Registerkarte [!UICONTROL Recommendations] nicht angezeigt**. Zuvor war die Produktliste, die nach angewendeten Regeln gefiltert wurde, im Modal „Bearbeiten“ nicht sichtbar, sodass es für Kunden schwierig war zu bestätigen, welche Produkte einbezogen oder ausgeschlossen wurden. Die Produktliste wird jetzt korrekt angezeigt und in Echtzeit aktualisiert, wenn Regeln geändert werden, was die Sichtbarkeit und Benutzerfreundlichkeit in der aktualisierten [!DNL Recommendations]-Benutzeroberfläche verbessert. (TGT-53481)
* **Das Layout des Dialogfelds &quot;[!UICONTROL View Details]&quot; auf der Registerkarte &quot;[!UICONTROL Recommendations]&quot; wurde**: Zuvor war das Dialogfeld &quot;[!UICONTROL View Details]&quot; nicht klar strukturiert, sodass Kunden nur schwer auf artikelspezifische und inventarbezogene Informationen zugreifen können. Das Layout wurde aktualisiert und enthält jetzt zwei Registerkarten: Eine Registerkarte zeigt Details für das ausgewählte Element an, und die zweite Registerkarte zeigt das Inventar an, das nach den aktuellen Regeln der Sammlung oder des Ausschlusses gefiltert wurde. Diese Verbesserung verbessert die Klarheit und Benutzerfreundlichkeit in der aktualisierten [!DNL Recommendations]-Benutzeroberfläche. (TGT-53503)
* **Kunden konnten keine Report Suites in der Dropdown-Liste &quot;[!UICONTROL Goals & Settings]&quot; durchsuchen**: Zuvor unterstützte die Dropdown-Liste „Report Suites“ im Abschnitt &quot;[!UICONTROL Goals & Settings]&quot; des Prozesses zur Erstellung von Aktivitäten keine Texteingabe für die Suche, sodass es für Kunden mit einer großen Anzahl von Report Suites schwierig war, die richtige Report Suite zu finden. Diese Funktion, die in der alten Benutzeroberfläche verfügbar ist, wurde wiederhergestellt. Kunden können jetzt Tippen, um Report Suites effizienter zu suchen und auszuwählen. (TGT-53514)
* **Kunden können die benutzerdefinierte Kriterien-CSV nicht in der [!DNL Recommendations]-Benutzeroberfläche herunterladen**: Zuvor wurde durch Klicken auf den Download-Link für benutzerdefinierte Kriterien-CSVs auf der Registerkarte &quot;[!UICONTROL Recommendations]&quot; ein 404-Fehler zurückgegeben und der Fehler beim Öffnen in einer neuen Registerkarte gemeldet. Der Download-Link wird jetzt auf einer neuen Registerkarte geöffnet und stellt die CSV-Datei korrekt bereit, was die Barrierefreiheit und Benutzerfreundlichkeit für Kunden, die benutzerdefinierte Kriterien verwalten, verbessert. (TGT-51966)
* **Durch das Aktivieren einer [!UICONTROL Recommendations] Promotion ohne Eingabedaten wurde eine allgemeine Fehlermeldung ausgelöst**: Zuvor hatten Kunden, die eine Front- oder Back-Promotion in einer Recommendations- ohne Angabe erforderlicher Felder aktiviert hatten, beim Code-`error.restapi.missingFields` einen vagen „Fehler: Ungültige Eingabe“ festgestellt. Das System bietet jetzt eine klare und verwertbare Fehlermeldung, die angibt, welche Felder fehlen. Dies verbessert die Benutzerfreundlichkeit und verringert die Verwirrung beim Erstellen von Aktivitäten. (TGT-52616)
* **Produktminiaturen und Bilder wurden in[!UICONTROL Catalog Search]** nicht konsistent geladen: Kundinnen und Kunden meldeten, dass Produktminiaturen und Bilder in voller Größe in [!UICONTROL Catalog Search] zeitweise fehlten oder beschädigt waren, insbesondere nach dem Navigieren oder Ändern der Sichtbarkeit der Spalte. Miniaturansichten und Bilder werden jetzt unabhängig von Spalteneinstellungen oder Navigationsverhalten zuverlässig geladen, was das Gesamterlebnis im [!UICONTROL Recommendations]-Workflow verbessert. (TGT-52778)
* **[!UICONTROL Designs] und [!UICONTROL Criteria] können nicht in der [!UICONTROL Stage] Umgebung erstellt werden**: Beim Versuch, [!UICONTROL Designs] oder [!UICONTROL Criteria] in der [!UICONTROL Recommendations]-Registerkarte der [!UICONTROL Stage]-Umgebung zu erstellen, trat beim Kunden der Fehler „Ungültige Benutzereingabe“ auf. Kunden können jetzt in der [!UICONTROL Designs] Umgebung erfolgreich [!UICONTROL Criteria] und [!UICONTROL Stage] ohne Fehler erstellen. (TGT-53205)
* **[!UICONTROL Promotions]wurden nach dem Speichern nicht aus [!UICONTROL Recommendations] Aktivitäten entfernt**: Kundinnen und Kunden berichteten, dass zu [!DNL Recommendation] Aktivitäten hinzugefügte Promotions auch nach dem Entfernen und Speichern weiterhin angezeigt wurden. Dieses Problem betraf sowohl die Staging- als auch die Produktionsumgebung und blieb über mehrere Speicherversuche hinweg bestehen. Promotions spiegeln jetzt die Änderungen, die während der Bearbeitung der Aktivität im aktualisierten Prozess zur Erstellung der Aktivität vorgenommen wurden, korrekt wider. (TGT-53490)

+++

**[!UICONTROL Reports]**

+++Details anzeigen
* **[!UICONTROL Automated Segments]hat in Aktivitätsberichten eine Null-Zielgruppe angezeigt**: Kundinnen und Kunden haben beobachtet, dass beim Anzeigen von [!UICONTROL Automated Segments] im [!UICONTROL Reports] Abschnitt einer Aktivität das Zielgruppenfeld als null angezeigt wurde, obwohl gültige Segmentdaten erwartet wurden. Dieses Problem wirkte sich auf die Sichtbarkeit der Zielgruppen-Targeting- und Reporting-Genauigkeit aus. [!UICONTROL Automated Segments] zeigen nun die zugehörigen Zielgruppeninformationen in Aktivitätsberichten korrekt an. (TGT-52793)
* **Aktivitätsberichte konnten nicht im CSV-Format heruntergeladen werden**: Beim Versuch, Aktivitätsberichte über die Registerkarte &quot;[!UICONTROL Reports]&quot; zu exportieren, ist bei Auswahl der Option „CSV-Download“ ein Fehler aufgetreten. Dieses Problem betraf sowohl Standardberichte als auch Exporte von Bestelldetails. Berichte werden jetzt korrekt im CSV-Format heruntergeladen. (TGT-53464)

+++

**Single Page Applications (SPAs)**

+++Details anzeigen
* **Beim Wechseln zwischen [!UICONTROL Browse]- und [!UICONTROL Design] wird der Status von Single Page Application (SPA) im Web-Editor zurückgesetzt**: Kunden berichteten, dass der Wechsel zwischen [!UICONTROL Browse]- und [!UICONTROL Design] im VEC dazu führte, dass der Web-Editor neu geladen wurde, der SPA-Status zurückgesetzt wurde und der Prozess zur Erstellung von Aktivitäten unterbrochen wurde. Der SPA-Navigationsstatus bleibt beim Wechsel des Modus jetzt im Editor erhalten, sodass die Bearbeitung reibungsloser und konsistenter erfolgt. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer (VEC)]**

+++Details anzeigen
* **Das Umbenennen eines Speicherorts in einer [!UICONTROL Automated Personalization] (AP)- oder [!UICONTROL Multivariate Test] (MVT)-Aktivität blieb nach der Navigation zum [!UICONTROL Targeting] Schritt und der Rückkehr nicht bestehen.** Kunden können jetzt Standortnamen erfolgreich bearbeiten und speichern, und die Änderungen bleiben während des gesamten Erstellungsprozesses der Aktivität sichtbar. (TGT-52367)
* **Die alte VEC-Benutzeroberfläche, die für Mandanten in der [!UICONTROL Stage]-Umgebung angezeigt wird**: Es wurde ein Problem behoben, bei dem beim Zugriff auf bestimmte Mandanten in der [!UICONTROL Stage]-Umgebung fälschlicherweise die alte Benutzeroberfläche anstelle des aktualisierten VEC angezeigt wurde. Dieses Problem war über mehrere Anmeldepfade hinweg reproduzierbar und betraf den [!UICONTROL Activities]. Die aktualisierte Benutzeroberfläche wird jetzt für beide Mandanten in der [!UICONTROL Stage] korrekt angezeigt. (TGT-52261)
* **Durch Auswahl einer Hintergrundfarbe stürzt die Seite im aktualisierten VEC ab**:
Es wurde ein Problem behoben, bei dem die Auswahl einer Hintergrundfarbe aus dem Bedienfeld [!UICONTROL Style] im aktualisierten VEC zum Absturz der Seite und zu einem Leerlauf führte. Konsolenfehler deuteten auf einen Fehler beim Lesen von Eigenschaften aus einem nicht definierten Element hin, insbesondere im Zusammenhang mit `querySelector`. Kunden können jetzt Hintergrundfarben sicher auswählen, ohne einen Absturz auszulösen. (TGT-53561)
* **Aktivitäten konnten aufgrund eines Fehlers bei der ungültigen Benutzereingabe nicht gespeichert werden**: Fehlerkorrektur: Beim Versuch, vorhandene Aktivitäten im aktualisierten VEC zu speichern, tritt jetzt kein Fehler mehr auf. Der Fehler trat nur bei Bearbeitungen auf, nicht beim Erstellen neuer Aktivitäten mit derselben Eigenschaft. Die folgende Fehlermeldung wurde angezeigt:

  `Invalid Json. Unrecognized property name 'content'. Location: line - 1, column - 432.`

  Aktivitäten, die die betroffene Eigenschaft verwenden, können jetzt nach der Bearbeitung erfolgreich gespeichert werden. (TGT-53507)

* **Transparente Bilder enthalten den Parameter „fmt=png-alpha“ nicht mehr im aktualisierten VEC**: Kundinnen und Kunden berichteten, dass beim Ersetzen von Bildern in der aktualisierten Benutzeroberfläche transparente Hintergründe nicht mehr beibehalten wurden. Bei den Bild-URLs, die vom aktualisierten VEC generiert wurden, wurde der `fmt=png-alpha`-Parameter weggelassen, was zuvor für Transparenz in der alten Benutzeroberfläche gesorgt hat. Die aktualisierte Benutzeroberfläche hängt jetzt den `fmt=png-alpha`-Parameter für transparente Bilder korrekt an und stellt das erwartete Rendering-Verhalten wieder her. (TGT-52615)
* **Kunden konnten in AP-Aktivitäten nicht zum Abschnitt „Targeting“ wechseln, ohne zwei Standorte hinzuzufügen**: Kunden, die in der aktualisierten Benutzeroberfläche [!UICONTROL Automated Personalization] (AP)-Aktivitäten erstellen, konnten erst dann zum Abschnitt „Targeting“ wechseln, wenn zwei Standorte hinzugefügt wurden. Dieses Verhalten unterschied sich von dem der vorherigen Benutzeroberfläche, bei der ein einzelner Speicherort ausreichend war. Das Problem blockierte die Erstellung und Speicherung von Aktivitäten für Kunden, die nur einen Standort bevorzugen. Kunden können jetzt mit der Zielgruppenbestimmung und der Speicherung von API-Aktivitäten an einem einzigen Ort fortfahren und so die erwartete Funktionalität wiederherstellen. (TGT-53426)
* **HTML-Angebote, die beim Wechsel zwischen Erlebnissen im Arbeitsbereich dupliziert**: Zuvor hatten Kundinnen und Kunden, die nach dem Wechsel zwischen Erlebnissen HTML-Angebote in den Arbeitsbereich eingefügt haben, doppelte Inhalte. Dieses Problem führte auch dazu, dass der Arbeitsbereich nicht mehr gescrollt werden konnte, was sich auf die Benutzerfreundlichkeit auswirkte. HTML-Angebote werden nicht mehr dupliziert und der Arbeitsbereich bleibt beim Wechseln der Erlebnisse in der aktualisierten VEC bildlauffähig. (TGT-53487)
* **Durch das manuelle Aktualisieren einer CSS-Auswahl wurde der VEC-Bildschirm leer angezeigt**: Kunden meldeten, dass beim Bearbeiten eines Angebots in VEC durch das manuelle Aktualisieren der CSS-Auswahl ein leerer Bildschirm ausgelöst wurde, selbst wenn die Auswahl gültig und auf der Seite vorhanden war. Der VEC-Bildschirm bleibt nun stabil, wenn Selektoren während des Erstellungsprozesses der Aktivität manuell aktualisiert werden. (TGT-53553)
* **Problem mit dem Abschneiden im Feld „Startdatum“ bei Auswahl von „Angegebenes Datum und Uhrzeit“ in[!UICONTROL Goals & Settings]**: Bei Kunden trat ein Problem mit dem Abschneiden im Feld &quot;[!DNL Start date]&quot; auf, wenn die Option „Angegebenes Datum und Uhrzeit“ im Abschnitt „Dauer“ der Seite &quot;[!UICONTROL Goals & Settings]&quot; während der Erstellung einer Aktivität ausgewählt wurde. Das vollständige Datum und die Uhrzeit werden nun korrekt in allen unterstützten Gebietsschemata angezeigt. (TGT-47843)
* **Filtersymbol wurde beim Minimieren des Browsers in der [!UICONTROL Manage Content] Leiste ausgeblendet**: Kundinnen und Kunden meldeten, dass das Filtersymbol in der [!UICONTROL Manage Content] Leiste des Flusses [!UICONTROL Automated Personalization] Aktivitätserstellung ausgeblendet wurde, wenn die Größe oder Minimierung des Browser-Fensters geändert wurde. Das Filtersymbol bleibt jetzt unabhängig von der Browser-Größe sichtbar und zugänglich, was die Benutzerfreundlichkeit über Bildschirmauflösungen hinweg verbessert. (TGT-51449)

+++

**[!UICONTROL Workspaces]**

+++Details anzeigen
* **Kunden, die auf einen einzelnen Arbeitsbereich beschränkt sind, konnten Aktivitäten aus anderen Arbeitsbereichen anzeigen**: Kunden, deren Zugriff auf einen bestimmten Arbeitsbereich beschränkt war, konnten weiterhin [!UICONTROL All Workspaces] in der aktualisierten Benutzeroberfläche auswählen und Aktivitäten aus anderen Arbeitsbereichen anzeigen. Dieses Verhalten birgt das Risiko von unbeabsichtigten Änderungen an Live-Aktivitäten außerhalb ihres zugewiesenen Bereichs. Workspace-Einschränkungen werden jetzt korrekt durchgesetzt und Kundinnen und Kunden können Aktivitäten nur in ihrem zugewiesenen Arbeitsbereich anzeigen. (TGT-53101)
* **Kunden konnten Aktivitäten von der [!UICONTROL Default Workspace] ohne Zugriff anzeigen**: Kunden konnten Aktivitäten von der [!UICONTROL Default Workspace] sehen, obwohl sie keinen Zugriff darauf hatten. Workspace-Berechtigungen werden jetzt in der aktualisierten Benutzeroberfläche korrekt durchgesetzt, sodass Kundinnen und Kunden nur die Aktivitäten sehen, die mit ihrem zugewiesenen Arbeitsbereich verbunden sind. (TGT-53297)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
