---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: dc291b4573e00512edd44b94304be2a25106b234
workflow-type: tm+mt
source-wordcount: '1882'
ht-degree: 11%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: 7. Juli 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.7.1 (Mittwoch, 8. Juli 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem Zielgruppenverfeinerungen nur für Aktivitäten sofort aus der Benutzeroberfläche verschwanden, nachdem sie von einem Speicherort entfernt wurden, noch bevor die Aktivität gespeichert wurde. Dieses Verhalten stand im Widerspruch zu den erwarteten Funktionen und der QuickInfo-Anleitung, in der es heißt: „Alle nicht verwendeten Zielgruppen aus dieser Bibliothek werden gelöscht, sobald die Aktivität gespeichert wurde.“ (TGT-52982)
* Fehlerkorrektur - Jetzt wird nicht mehr versucht, einer Aktivität eine andere Zielgruppe als [!UICONTROL All Visitors] zuzuweisen. Beim Speichern wird die folgende Fehlermeldung angezeigt: „Wir können Ihre Anfrage nicht abschließen. Wenden Sie sich an den Adobe-Kundendienst, wenn das Problem weiterhin besteht.“ (TGT-53008)
* Fehlerkorrektur - Das Speichern einer Aktivität nach dem Erstellen und Zuweisen einer neuen Zielgruppe im Aktivitätseditor wird jetzt problemlos möglich sein. Die folgende Fehlermeldung wurde angezeigt: „Wir können Ihre Anfrage nicht abschließen. Wenden Sie sich an den Adobe-Kundendienst, wenn das Problem weiterhin besteht.“ (TGT-52977)
* Fehlerkorrektur - Jetzt tritt kein Fehler mehr auf, wenn versucht wird, eine Aktivität nach dem Erstellen und Zuweisen einer neuen Reporting-Zielgruppe zu speichern. Die zurückgegebene Fehlermeldung war: „Zugriff verweigert. Um diesen Vorgang auszuführen, sind alle folgenden Berechtigungen erforderlich: [editor]. Dieses Problem trat auf, obwohl der Benutzer Zugriff auf der Ebene der genehmigenden Person hatte. (TGT-53103)
* Es wurde ein Problem behoben, bei dem Benutzende mit der Rolle [!UICONTROL Approver] keine Zielgruppenverfeinerungen nur für Aktivitäten hinzufügen oder speichern konnten. Der Versuch, dies zu tun, führte zu einem 403-Fehler (Forbidden) und gab an, dass die Berechtigung &quot;[editor]&quot; erforderlich war, obwohl der Benutzer über ausreichende Berechtigungen zum Genehmigen und Verwalten von Aktivitäten verfügte. (TGT-52984)
* Fehlerkorrektur - Wenn eine aktivitätsspezifische Zielgruppe mithilfe der Option [!UICONTROL Remove Audience Refinement] entfernt wird, wird die Zielgruppe nicht mehr in der Liste der Zielgruppen für die erneute Auswahl innerhalb derselben Aktivität angezeigt. Dieses Verhalten verhinderte, dass Benutzer dieselbe Zielgruppe erneut hinzufügen konnten, es sei denn, sie wurde von Grund auf neu erstellt. (TGT-52979)
* Ein Problem wurde behoben, das dazu führte, dass Benutzer keine [!UICONTROL Auto-Target] (AT)-Aktivitäten erstellen konnten, wenn bei der Einrichtung der Traffic-Zuordnung zuerst [!UICONTROL Auto-Allocate] (AA) ausgewählt wurde. Dieses Problem führte zu einem Backend-Validierungsfehler und verhindert, dass die Aktivität gespeichert wird. (TGT-53096)
* Es wurde ein Problem behoben, bei dem Benutzende in [!UICONTROL Browse Mode] nicht zu einer anderen URL navigieren konnten. Tester und Bearbeiter konnten dadurch alternative Seiten innerhalb derselben Aktivitätssitzung nicht validieren oder in der Vorschau anzeigen. (TGT-53052)
* Es wurde ein Problem behoben, bei dem die Verwendung der [!UICONTROL Manage Content]-Funktion in [!UICONTROL Automated Personalization] (AP) -Aktivitäten zum Absturz der Seite führte und leer blieb. Dieses Problem trat nach dem Klicken auf [!UICONTROL Done] im Content Manager auf, insbesondere bei Aktivitäten, die in der aktualisierten Benutzeroberfläche erstellt oder bearbeitet wurden. (TGT-53047)
* Es wurde ein Problem behoben, bei dem die [!UICONTROL Manage Content]-Funktion den Status eines Speicherorts nicht ordnungsgemäß validierte, nachdem alle Inhaltsoptionen entfernt wurden. Dies kann zu inkonsistentem Verhalten oder Fehlern beim Speichern oder Fortsetzen der Aktivitätskonfiguration führen. (TGT-52801)
* Es wurde ein Problem behoben, bei dem mehrere [!UICONTROL Visual Experience Composer] (VEC)-Instanzen gleichzeitig während der Aktivitätserstellung geöffnet wurden. Dieses Problem trat auf, wenn Benutzende den [!UICONTROL Enhanced Experience Composer] (EEC) deaktiviert und den nachgestellten Schrägstrich im [!UICONTROL Page Delivery] Schritt aus der Website-URL entfernt haben. (TGT-52782)
* Es wurde ein Problem behoben, bei dem Benutzende auf den Fehler „Ungültige Eingabe“ stießen, wenn eine neue Seite hinzugefügt und bestimmte Elemente in verschiedenen Erlebnissen gelöscht wurden. Der Fehler wurde durch doppelte `LocalIds` ausgelöst, die während der Elementbearbeitung generiert wurden, insbesondere beim Wechseln zwischen Erlebnissen und beim Ändern freigegebener Seitenstrukturen. (TGT-52720)
* Es wurde ein Problem behoben, bei dem die Anwendung einer Änderung auf eine Ansicht dazu führte, dass die Ansicht dupliziert wurde und die Aktivität den Fehler „Ungültige Benutzereingabe“ zurückgab. Durch diese Fehlerbehebung wird sichergestellt, dass Ansichtsänderungen korrekt angewendet werden, ohne dass Duplizierungs- oder Validierungsfehler ausgelöst werden. (TGT-52886)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code fälschlicherweise für das falsche Erlebnis angezeigt wurden. Insbesondere wurden Änderungen, die für ein Erlebnis vorgesehen waren, in einem anderen Erlebnis gezeigt, was zu Verwirrung und einer potenziellen Fehlkonfiguration von Live-Aktivitäten führte. (TGT-52776)
* Ein Problem wurde behoben, das das Bearbeiten oder Speichern benutzerdefinierter Code-Änderungen in der neuen VEC-Benutzeroberfläche verhinderte. Speziell:

   * Nach dem Bearbeiten und Speichern eines benutzerdefinierten Code-Blocks wurden die Änderungen weder in der Benutzeroberfläche noch in der QS-Vorschau angezeigt.
   * In einigen Fällen konnten Änderungen erst gelöscht werden, nachdem die Aktivität geschlossen und erneut geöffnet wurde.
   * Als Problemumgehung mussten Benutzende den Code kopieren, die Änderung löschen und ihn manuell mit den aktualisierten Inhalten neu erstellen. (TGT-53072)

* Es wurde ein Problem behoben, bei dem das Bearbeiten und Speichern von benutzerdefiniertem Code dazu führte, dass das [!UICONTROL Modifications] Bedienfeld nicht mehr reagierte. (TGT-53075)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code in Variantenerlebnissen unbeabsichtigt im [!UICONTROL Control] widergespiegelt wurden. Dies führte zu unbeabsichtigten Änderungen im Versandverhalten. Das [!UICONTROL Control] bleibt jetzt von benutzerdefinierten Code-Bearbeitungen an anderen Erlebnissen isoliert. (TGT-52413)
* Fehlerkorrektur - Im Workflow zum Erstellen von Aktivitäten werden Änderungen an einem Erlebnis (z. B. Erlebnis B) nicht versehentlich in ein anderes Erlebnis (Erlebnis A) dupliziert, wenn Benutzende auf das zweite Erlebnis klicken, bevor der Editor vollständig geladen ist. Dieses Verhalten kann auch dazu führen, dass Änderungen verloren gehen, wenn das ursprünglich ausgewählte Erlebnis keine Änderungen aufwies. (TGT-52597)
* Es wurde ein Problem behoben, bei dem Änderungen, die im [!UICONTROL Modifications] Schritt der Aktivitätserstellung vorgenommen wurden, nicht konsistent gespeichert wurden. In einigen Fällen wird das im Abschnitt [!UICONTROL Save] hinzugefügte benutzerdefinierte Skript nach Abschluss aller Schritte und Klicken auf [!UICONTROL Modifications] nicht auf der Live-Site widergespiegelt, obwohl während des Speichervorgangs keine sichtbaren Fehler aufgetreten sind. (TGT-52661)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code nicht korrekt gespeichert und unbeabsichtigt in mehreren Erlebnissen innerhalb derselben Aktivität gespiegelt wurden. Darüber hinaus traten beim Öffnen oder Aktualisieren bestimmter Aktivitäten Zugriffsprobleme auf, was zu leeren Bildschirmen führte. Diese Probleme wurden nun behoben, um eine stabile Aktivitätsbearbeitung und eine genaue Isolierung der Erlebnisse sicherzustellen. (TGT-52594)
* Es wurde ein Problem behoben, bei dem die Verwendung der [!UICONTROL Generate Adhoc Offer]-Funktion dazu führte, dass undefinierte Positionen im [!UICONTROL Manage Content] angezeigt wurden. (TGT-53076 und TGT-53070)
* Das Verhalten für den Kunden klargestellt, bei dem Änderungen, die mithilfe eines HTML-Angebots vorgenommen wurden, fehlen könnten, wenn vom [!UICONTROL Targeting] Schritt zurück zum [!UICONTROL Experiences] navigiert wird. Für diesen Kunden generierte die betroffene Website dynamisch mehrere DOM-Selektoren, die sich mit jedem Laden der Seite änderten. Daher kann der ursprünglich für die Änderung verwendete Selektor beim erneuten Öffnen des Editors nicht gefunden werden, was dazu führt, dass die Änderung fehlt oder ungültig ist. Dies funktioniert wie vorgesehen. Um sicherzustellen, dass Änderungen visuell im Editor bestehen bleiben, wird empfohlen, dass Clients stabile, konsistente Selektoren verwenden, die sich nicht über Seitenneuladungen hinweg ändern. (TGT-52874)
* Es wurde ein Problem behoben, bei dem der Versuch, ein Angebot zu löschen oder zu deaktivieren, das Teil eines ausgeschlossenen Erlebnisses war, den Fehler „Ungültige Benutzereingabe“ auslöste. Dieses Problem trat auf, obwohl das Angebot in den eingeschlossenen Erlebnissen nicht aktiv verwendet wurde. (TGT-52917)
* Es wurde ein Problem behoben, bei dem die Dropdown-Liste [!UICONTROL Revenue] im [!UICONTROL Goals & Settings] fälschlicherweise auf [!UICONTROL Revenue per Visit] (RPVISIT) eingestellt war, selbst wenn der Benutzer eine andere Metrik ausgewählt hatte.  Beim Reduzieren und erneuten Erweitern des Bedienfelds für die Metrikkonfiguration ist ein Problem aufgetreten, sodass der zuvor ausgewählte Wert zurückgesetzt wurde. (TGT-52811 und TGT-52878)
* Es wurde ein Problem behoben, das blockiert wurde
* Fehlerkorrektur - Im Workflow zum Erstellen von Aktivitäten treten jetzt keine Probleme mehr im Zusammenhang mit der Angebotsbenennung und der Inhaltsübersetzung in [!UICONTROL Automated Personalization] Aktivitäten (AP) und [!UICONTROL Multivariate Testing] (MVT) auf:

  Wichtige angesprochene Probleme:

   * Das Erstellen mehrerer HTML-Angebote mit demselben Namen (z. B. „Erlebnis„) hat den Fehler „Doppelte Angebotsnamen sind nicht zulässig“ ausgelöst, aber die Benutzeroberfläche hat nicht klar angegeben, welche Angebote den Konflikt verursacht haben.
   * Beim Umbenennen von Angeboten über das rechte Bedienfeld wurde der Name in der Benutzeroberfläche aktualisiert, die Änderung wurde jedoch nicht auf der Registerkarte [!UICONTROL Manage Content] oder der Registerkarte [!UICONTROL Offers] angezeigt, was zu anhaltenden Validierungsfehlern führte.
   * Obwohl der Fehler beim Duplizieren des Namens in MVT-Aktivitäten nach dem Umbenennen nicht fortbestand, konnte die Benutzeroberfläche aktualisierte Angebotsnamen weiterhin nicht konsistent auf allen Registerkarten widerspiegeln. (TGT-52933)

* Es wurde ein Problem behoben, bei dem die Auswahl von &quot;[!UICONTROL Export order details to CSV]&quot; auf der Seite &quot;[!UICONTROL Reports]&quot; dazu führte, dass eine leere Datei heruntergeladen wurde. Dieses Problem trat auch dann auf, wenn gültige Bestelldaten in der Aktivität vorhanden waren. (TGT-52225)
* Es wurde ein Problem behoben, bei dem das Kopieren einer vorhandenen Aktivität und das Ändern der Berichtsquelle in [!DNL Adobe Analytics] (A4T) zu einem Fehler „Ungültige Benutzereingabe“ führte. Der Fehler wurde ausgelöst, wenn bestimmte Metrikaktionen, die mit [!DNL Analytics] Reporting nicht kompatibel sind, wie `restart_same_experience`, `restart_random_experience` und `restart_new_experience`, von der ursprünglichen Aktivität beibehalten wurden. (TGT-52900)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine Aktivität zu erstellen oder zu speichern, wenn sie im [!DNL Adobe Analytics] Schritt [!UICONTROL Goals & Settings] (A4T) als Berichtsquelle auswählten. Das Problem trat speziell bei der Auswahl einer [!UICONTROL Custom Event]-Metrik auf (z. B. „Benutzerspezifisches Ereignis 16„), was zu folgendem Fehler führte: „Ungültige Benutzereingabe“. (TGT-52910)
* Es wurde ein Problem behoben, bei dem Benutzer durch Klicken auf den Link &quot;[!UICONTROL View in Analytics]&quot; auf die Homepage anstelle des vorgesehenen [!DNL Analytics]-Dashboards umgeleitet wurden. (TGT-53092 und TGT-53093)
* Fehlerkorrektur - Beim Klonen einer vorhandenen Aktivität und beim Ändern der Berichtsquelle von [!DNL Target] in [!DNL Adobe Analytics] tritt jetzt nicht mehr der Fehler „400 - Ungültige Benutzereingabe“ auf, der das Speichern der Aktivität verhindert. (TGT-52875)
* Es wurde ein Problem behoben, bei dem Vorschau-URLs fälschlicherweise zusätzliche Zielgruppen enthielten, die über die vom Benutzer explizit eingegebene hinausgingen. Dieses Verhalten wurde korrigiert, um sicherzustellen, dass beim Generieren eines QA- oder Vorschau-Links nur die angegebene Zielgruppe angewendet wird. (TGT-52912)
* Es wurde ein Problem behoben, bei dem die [!UICONTROL Activity QA]-URL einen unnötigen Abfrageparameter enthielt: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* Es wurde ein Problem in formularbasierten Aktivitäten behoben, bei dem das Duplizieren eines Erlebnisses und das Bearbeiten des benutzerdefinierten Codes in einem der duplizierten Erlebnisse diese Änderungen unbeabsichtigt auf alle duplizierten Erlebnisse anwenden würden. Jedes Erlebnis behält nun nach der Duplizierung seinen eigenen benutzerdefinierten Code unabhängig bei. (TGT-51600)
* Fehlerkorrektur - Der Workflow zum Erstellen von Aktivitäten beim Hinzufügen von [!DNL Recommendations] mit [!UICONTROL promotions] funktioniert jetzt fehlerfrei. Wenn Benutzende &quot;[!UICONTROL Promote by Attribute]&quot; ausgewählt und eine Filterregel hinzugefügt haben (z. B. [!UICONTROL Parameter Matching]), wurden der ausgewählte Regeltyp und die ausgewählten Operandenwerte nach dem Speichern und erneuten Bearbeiten der Aktivität nicht beibehalten. Beim erneuten Öffnen würde sich der Filterregeltyp unerwartet ändern und Operandenwerte fehlen. (TGT-53059)
* Ein Problem wurde behoben, dass dazu führte, dass beim Anzeigen einer [!DNL Recommendations] -Aktivität in der aktualisierten [!UICONTROL Overview]-Benutzeroberfläche der [!UICONTROL Goals & Settings]-Abschnitt nicht geladen wurde, wenn [!DNL Adobe Analytics] (A4T) als Berichtsquelle ausgewählt wurde. Die folgende Fehlermeldung wurde angezeigt: „Irgendetwas ist schiefgelaufen. Wir können Ihre Anfrage nicht bearbeiten. Wenden Sie sich an den Kundendienst von Adobe, wenn das Problem weiterhin besteht.“ (TGT-52999)
* Es wurde ein Problem in der [!DNL Recommendations]-Benutzeroberfläche behoben, bei dem jede mit einer einzelnen Regel erstellte Promotion falsch interpretiert und als Promotion-Typ „Liste von Elementen“ angezeigt wurde, unabhängig von der Logik der Regel. (TGT-53063)
* Fehlerkorrektur - Bei der Verwendung der aktualisierten [!UICONTROL Overview]Benutzeroberfläche fehlt die Schaltfläche &quot;[!UICONTROL Download Recommendations Data]&quot; für [!UICONTROL Experience Targeting] (XT)-Aktivitäten, die [!DNL Recommendations] enthalten. (TGT-52730 und TGT-52756)
* Zuvor wurde in der Recommendations-Benutzeroberfläche nur die Anzahl der Entitäten angezeigt, die erfolgreich aus einem Feed importiert wurden. Das Backend-Nachrichtenformat umfasst jedoch sowohl die Anzahl der importierten Entitäten als auch die Gesamtzahl der Entitäten im -Format:

  `# of entities imported / # of total entities`

  Aufgrund dieser Diskrepanz wurde den Benutzenden in der Benutzeroberfläche nur der erste Wert (Anzahl der importierten Daten) angezeigt, was zu Verwirrung führte. Die Benutzeroberfläche zeigt jetzt beide Zahlen an. (TGT-53073)

* Es wurde ein kontextuelles Übersetzungsproblem im koreanischen Gebietsschema (ko-KR) für die Zeichenfolge „Vorschau-Erlebnis“ behoben. (TGT-52928)
* Es wurden terminologische Inkonsistenzen behoben, die bei der Übersetzung mehrerer Textzeichenfolgen aus dem vereinfachten Chinesisch (zh_CN) festgestellt wurden. (TGT-52954 und TGT-52955)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
