---
keywords: QA; QA-Modus; Aktivitäts-QA; QA-URL; QA-URL; Vorschau-URL; Vorschau-URLs
description: Erfahren Sie, wie Sie mit Adobe [!DNL Target] QA-URLs eine einfache End-to-End-Aktivitäts-QA mit Vorschau-Links, die sich nie ändern, optionalem Audience-Targeting und QA-Berichten durchführen können, die weiterhin von Live-Aktivitätsdaten segmentiert sind.
title: Wie führe ich QA-Aktivitäten aus?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 99ea312405e397e97e64e32d2685e8a6966d8928
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 27%

---

# Aktivitäts-QA

Verwenden Sie QA-URLs in [!DNL Adobe Target], um eine einfache End-to-End-Aktivitäts-QA mit Vorschau-Links, die sich nie ändern, optionalem Audience-Targeting und QA-Berichten durchzuführen, die weiterhin aus Live-Aktivitätsdaten segmentiert sind.

[!UICONTROL Activity QA] können Sie Ihre [!DNL Target] Aktivitäten vollständig testen, bevor Sie sie live starten. Zu den [!UICONTROL Activity QA] Funktionen gehören:

* Links zur Freigabe für Team-Mitglieder, die sich nie ändern oder neu generiert werden müssen, unabhängig von Aktualisierungen an den Erlebnissen oder Aktivitäten. Mit dieser Funktion können Sie Ihre Aktivitäten auf der gesamten Benutzer-Journey testen.
* Zielgruppenbedingungen werden optional respektiert, sodass Vermarkter Targeting-Kriterien testen oder Targeting-Kriterien für QA ignorieren können, ohne die Zielgruppenbedingungen erfüllen zu müssen.
* QA-Berichte werden erfasst, sodass Vermarkter bestätigen können, dass Metriken erwartungsgemäß inkrementiert werden und die QA-Berichtsdaten von den Produktionsberichten separiert bleiben (für Nicht-A4T-Berichte).
* Die Möglichkeit, eine Vorschau eines Erlebnisses isoliert oder mit anderen Live-Aktivitäten anzuzeigen, die den Versandkriterien entsprechen (Seite/[!DNL Target]/Zielgruppe).
* Die Fähigkeit, einen QA-Bericht der gesamten User Journey zu erstellen. Mit dem QA-Link können Sie einmal auf Ihre Seite zugreifen und die gesamte Seite in Aktivitäts-QA durchsuchen. Sie verbleiben in Aktivitäts-QA, bis Sie die Sitzung beenden oder die [QA-Target-](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) verwenden, um sich selbst aus der [!UICONTROL Activity QA] zu zwingen. Diese Funktion ist nützlich, wenn Sie eine Aktivität haben, die mehrere Web-Seiten umfasst.

  >[!NOTE]
  >
  >Diese Funktion gilt für at.js-Implementierungen mit Version 2.*x* oder höher. Für at.js 1.*x*-Implementierungen ist diese Funktion nur dann verfügbar, wenn der Browser des Besuchers keine Third-Party-Cookies blockiert.

## Zugreifen auf und Freigeben einer QA-URL {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Klicken Sie auf der [!UICONTROL Overview] einer Aktivität auf **[!UICONTROL Activity QA]**.

1. Konfigurieren Sie die folgenden Einstellungen:

   * **[!UICONTROL Match audience rules to see experiences]:** Manchmal möchten Sie bestätigen, dass der Abgleich Ihrer Zielgruppe funktioniert. Andernfalls möchten Sie das Erscheinungsbild der Aktivität überprüfen. Wenn sich diese Einstellung in der Stellung „ein“ befindet, müssen Tester die Targeting-Anforderungen erfüllen, um sich für die Anzeige der Erlebnisse zu qualifizieren. Für Erlebnis-Targeting (XT)-Aktivitäten wird eine einzelne Aktivitäts-URL bereitgestellt. Das angezeigte Erlebnis richtet sich danach, ob Sie sich für eine der Targeting-Regeln qualifizieren.

     Wenn sich diese Einstellung in der Stellung „aus“ befindet, werden beim Klicken auf die Links die Erlebnisse angezeigt (unabhängig davon, ob Sie sich qualifizieren oder nicht). Bei der QA-Ausführung können Sie die Festlegung einer erforderlichen bzw. nicht erforderlichen Respektierung des Zielgruppen-Targetings ändern.

   * **Standardinhalt für alle anderen Aktivitäten anzeigen:** Wenn diese Option auf „ein“ umgeschaltet ist, wird der Standardinhalt für alle anderen Aktivitäten angezeigt. Beispielsweise wird die Vorschau isoliert angezeigt, ohne alle anderen Live-Aktivitäten auf derselben Seite/[!DNL Target]-Anfrage zu berücksichtigen.

     Achten Sie auf Folgendes, wenn diese Einstellung auf „aus“ festgelegt ist:

      * Wenn es zu Kollisionen zwischen der zu testenden Aktivität und anderen Live-Aktivitäten kommt, [normale Prioritätsregeln](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) angewendet. Aufgrund von Kollisionen ist es möglich, dass Sie die Aktivität, die Sie überprüfen möchten, nicht sehen können.
      * Die Metriken werden für die angezeigten Aktivitäten inkrementiert, jedoch nicht in der QA-Berichtsumgebung.

1. Klicken Sie auf **[!UICONTROL Done]** , um Ihre Änderungen zu speichern.
1. Geben Sie die Aktivitäts-Link-URLs zum Testen für Mitglieder Ihrer Organisation frei.

   Aktivitäts-Links laufen nie ab und Sie müssen keine Links erneut senden, wenn jemand eine Aktivität oder ein Erlebnis ändert. Wenn Sie jedoch eine andere Zielgruppe als die [!UICONTROL Audience Library] anwenden, anstatt die Aktivität einfach zu bearbeiten, wird ein neuer Link generiert, den Sie erneut freigeben müssen.

   Mit jeder Aktivitäts-Link-URL (für Erlebnis A, Erlebnis B usw.) können Sie die Benutzer-Journey aus dem entsprechenden Erlebnis starten. Klicken Sie auf die für ein Erlebnis generierte URL und fahren Sie dann mit dem normalen Site-Browsing fort, um Erlebnisse auf mehreren Seiten anzuzeigen (wenn mehrere Seiten vorhanden sind). Pro Erlebnis wird nur eine URL generiert, auch wenn das Erlebnis mehrere Seiten umfasst (Vorlagentests oder mehrseitige Tests).

   Sie können auf der Site navigieren, um die anderen Seiten anzuzeigen, da der [!UICONTROL Activity QA] beibehalten wird. Dies gilt für at.js-Implementierungen mit Version 2.*x* oder höher. Für at.js 1.*x*-Implementierungen ist dies nur der Fall, wenn der Browser des Besuchers keine Third-Party-Cookies blockiert.

1. Um Berichte anzuzeigen, die anhand von Aktivitäts-Link-URLs generiert wurden, klicken Sie auf die **[!UICONTROL Reports]** der Aktivität, klicken Sie auf das **[!UICONTROL Settings]** ( ![icon_gear image](assets/icon_gear.png) ) und wählen Sie dann **[!UICONTROL QA Mode Traffic]** aus der **[!UICONTROL Environment]** Dropdown-Liste aus.

## Beenden des QA-Modus

[!UICONTROL Activity QA] klebt. Nachdem Sie eine Website in [!UICONTROL Activity QA] durchsucht haben, muss Ihre [!DNL Target] abgelaufen sein, oder Sie müssen Sie [!DNL Target] von [!UICONTROL Activity QA] freigeben, bevor Sie Ihre Site wie einen typischen Besucher anzeigen können.

### at.js 2.*x* 

Wenn Ihre Site at.js 2.*x* bereitgestellt, verwenden Sie die [Target QA Bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879), um sich selbst aus der [!UICONTROL Activity QA] zu zwingen. Beim Laden einer Seite auf Ihrer Site mit einem leeren Wert, wie im nächsten Aufzählungszeichen beschrieben, wird *nicht* das QA-Cookie aus dem Browser entfernt, wenn at.js 2.*x* eingesetzt wird.

### at.js 1.*x*  

Wenn Ihre Site at.js 1.*x* bereitgestellt, können Sie zusätzlich zur Verwendung der [Target-QA-Lesezeichenliste](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) auch manuell eine Seite auf Ihrer Site laden, die den `at_preview_token`-Parameter mit einem leeren Wert enthält. Beispiel:

`https://www.mysite.com/?at_preview_token=`

### [!DNL Adobe Experience Platform Web SDK]

Wenn auf Ihrer Site die [[!UICONTROL Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} bereitgestellt sind, können Sie sich manuell selbst aus dem System entfernen, indem Sie eine Seite auf Ihrer Site laden, die den Parameter `at_qa_mode` mit einem leeren Wert enthält. Beispiel:

`https://www.mysite.com/?at_qa_mode=`

## Zu beachten {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Da die Aktivitäts-QA jetzt für alle [!DNL Target] Aktivitätstypen verfügbar ist, ist die Funktion „Vorschau von Automated Personalization-Aktivitäten mit Erlebnisvorschau-URLs“ nicht mehr erforderlich.
* [!UICONTROL Activity QA] Vorschau-Links für gespeicherte Aktivitäten werden möglicherweise nicht geladen, wenn im Konto zu viele gespeicherte Aktivitäten vorhanden sind. Das Wiederholen der Vorschau-Links sollte funktionieren. Um zu verhindern, dass dies weiterhin geschieht, archivieren Sie gespeicherte Aktivitäten, die nicht mehr aktiv verwendet werden.
* [!UICONTROL Activity QA]-URLs sind für Aktivitäten mit [Analytics als Berichtsquelle) ](/help/main/c-integrating-target-with-mac/a4t/a4t.md)A4T) verfügbar. Treffer, die bei der QS mithilfe [!UICONTROL Activity QA] Flusses zu derselben Report Suite generiert werden, in der die Daten der Aktivität auch nach der Live-Schaltung der Aktivität fließen.
* [!UICONTROL Activity QA] zeigt keine Inhalte für archivierte Aktivitäten oder Aktivitäten an, die nach dem Enddatum liegen. Wenn Sie eine beendete Aktivität deaktivieren, müssen Sie die Aktivität erneut speichern, damit [!UICONTROL Activity QA] funktioniert.
* In [!DNL Target Standard/Premium] importierte Aktivitäten (z. B. aus [!DNL Target Classic]) unterstützen keine QA-URLs.
* In [!UICONTROL Auto-Allocate]- und [!UICONTROL Recommendations]-Aktivitäten ist das Modell von den in [!UICONTROL Activity QA] erfassten Besuchen nicht betroffen.
* Wenn Sie beim Erstellen der Aktivität „URL ist[ angegeben haben (Verbesserungen im formularbasierten ](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) oder [Seitenbereitstellungsoptionen im Visual Experience Composer)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81) funktioniert die QA-URL nicht, da [!UICONTROL Activity QA] URL-Parameter anhängt. Klicken Sie zur Lösung dieses Problems auf die QA-URL, um zu Ihrer Site zu navigieren. Entfernen Sie die angehängten Parameter aus der URL und laden Sie dann die neue URL.
* Wenn Sie at.js 1.*x* bleibt der [!UICONTROL Activity QA]-Modus nicht hängen, wenn Sie Safari oder einen anderen Browser verwenden, der Drittanbieter-Cookies blockiert. In diesen Fällen müssen Sie die Vorschauparameter zu jeder URL hinzufügen, zu der Sie navigieren. Dasselbe gilt, wenn Sie &quot;[&quot; ](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html){target=_blank} haben.
* Wenn für eine Aktivität mehrere Erlebnis-Zielgruppen verwendet werden (z. B. eine Website aus den USA und Großbritannien, die Teil derselben Aktivität ist), werden für die vier Kombinationen (Experience A/US-Website, Experience A/UK-Website, Experience B/US-Website, Experience B/UK-Website) keine QA-Links erzeugt. Es werden nur zwei QA-Links (Erlebnis A und Erlebnis B) erstellt, und die Benutzer müssen sich für die entsprechende Zielgruppe qualifizieren, um die Seite anzeigen zu können. Eine Person, die für Fragen zur britischen Qualitätssicherung zuständig ist, kann die US-Website nicht sehen.
* Alle Parameter und Werte vom Typ `at_preview` sind bereits URL-kodiert. Meistens funktioniert alles wie erwartet. Einige Kunden müssen jedoch Lastenausgleichsmodule oder Webserver verwenden, die versuchen, die Abfragezeichenfolgenparameter erneut zu codieren.

  [!DNL Target] Aufgrund dieser doppelten Codierung kann [!DNL Target] beim Versuch, den `at_preview_token` zu decodieren, nicht den richtigen Token-Wert extrahieren, was dazu führt, dass die Vorschau nicht funktioniert.

  [!DNL Adobe] empfiehlt, mit Ihrem IT-Team zu sprechen, um sicherzustellen, dass alle Vorschauparameter auf die Zulassungsliste gesetzt werden, damit diese Werte nicht umgewandelt werden.

  In der folgenden Tabelle sind die Parameter aufgeführt, die in Ihrer Domain auf die Zulassungsliste gesetzt werden können:

  | Parameter | Typ | Wert | Beschreibung |
  |--- |--- |--- |--- |
  | `at_preview_token` | Verschlüsselte Zeichenfolge | Erforderlich; kein Standardwert | Eine verschlüsselte Entität, die die Liste der Kampagnen-IDs enthält, die im QA-Modus ausgeführt werden können. |
  | `at_preview_index` | Zeichenfolge | Empty | Format des Parameters ist `<campaignIndex>` oder `<campaignIndex>_< experienceIndex>`<br>Beide Indizes beginnen mit 1. |
  | `at_preview_listed_activities_only` | Boolescher Wert (true/false) | Standardwert: false | Bei „true“ werden alle in den `at_preview_index`-Parametern angegebenen Kampagnen verarbeitet.<br>Bei „false“ werden alle Kampagnen der Seite bearbeitet, selbst wenn sie nicht im Vorschau-Token angegeben wurden. |
  | `at_preview_evaluate_as_true_audience_ids` | Zeichenfolge | Empty | Durch Unterstrich getrennte („_„) Liste der segmentId-s, die immer (auf Targeting- und Reporting-Ebene) im Gültigkeitsbereich der [!DNL Target]-Anfrage als „true“ ausgewertet werden sollen. |
  | `_AT_Debug` | Zeichenfolge | Fenster oder Konsole | Konsolenprotokollierung oder neues Fenster. |
  | `adobe_mc_ref` |  |  | Übergibt gibt die verweisende URL der Standardseite an die neue Seite. Bei der Nutzung mit `AppMeasurement.js`-Version 2.1 (oder höher) verwendet [!DNL Adobe Analytics] diesen Parameterwert als Verweis-URL auf der neuen Seite. |
  | `adobe_mc_sdid` |  |  | Übergibt die [!DNL Supplemental Data Id] (SDID) und [!DNL Experience Cloud Org Id] von der Standardseite an die neue Seite. Durch Übergeben dieser IDs kann [!UICONTROL Analytics for Target] (A4T) die [!DNL Target]-Anfrage auf der Standardseite mit der [!DNL Analytics]-Anfrage auf der neuen Seite „zusammenfügen“. |

* In der [!UICONTROL Target QA Mode] Benutzeroberfläche wird nur die erste URL eines Erlebnisses in einer mehrseitigen Aktivität angezeigt. Es wird davon ausgegangen, dass Sie einen Journey-Test erstellen und von URL1 zu URL2 wechseln. Wenn Sie jedoch unabhängig zu URL 2 wechseln möchten, kopieren Sie alle URL-Parameter, die neben URL1 angegeben sind, und wenden Sie sie nach dem Platzieren eines „?“ auf URL2 an, genau wie Sie sie in URL1 sehen.
* Vorschaulinks für die Aktivitäts-QA gespeicherter Aktivitäten werden möglicherweise nicht geladen, wenn im Konto zu viele gespeicherte Aktivitäten vorhanden sind. Versuchen Sie die Vorschaulinks erneut zu laden. Archivieren Sie gespeicherte Aktivitäten, die nicht mehr aktiv verwendet werden, um zu verhindern, dass dieses Problem weiterhin auftritt.

## Kompatibilität der Target JavaScript-[!UICONTROL QA Mode] {#compatibility}

[!DNL Target] unterstützt die folgenden JavaScript-Bibliotheken:

* [at.js 1.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de)

In der folgenden Tabelle sind die verschiedenen Aktivitätstypen aufgeführt und angegeben, ob [!UICONTROL Activity QA] Modus für jede Bibliothek unterstützt wird:

| Aktivitätstyp | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B Test] | Ja | Ja | Ja |
| [!UICONTROL Auto-Allocate] | Ja | Ja | Ja |
| [!UICONTROL Auto-Target] | Ja | Ja | Ja |
| [!UICONTROL Automated Personalization] (AP) | Ja | Ja | Ja |
| [!UICONTROL Experience Targeting] (XT) | Ja | Ja | Ja |
| [!UICONTROL Multivariate Test] (MVT) | Ja | Ja | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja |