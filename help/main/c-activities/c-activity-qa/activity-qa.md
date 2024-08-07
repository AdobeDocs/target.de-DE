---
keywords: qa; qa mode; activity qa; qa url; qa urls; Vorschau-URL; Vorschau-URL
description: Erfahren Sie, wie Sie mithilfe von Adobe [!DNL Target] QA-URLs einfach End-to-End-Aktivitäts-QAs durchführen können, indem Sie unveränderbare Vorschaulinks, optionales Zielgruppen-Targeting und QA-Berichte anzeigen, die aus Live-Aktivitätsdaten segmentiert bleiben.
title: Wie kann ich QA-Aktivitäten durchführen?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 4b7c6d82e6988c64ace401d8f749b181b8dc1866
workflow-type: tm+mt
source-wordcount: '1665'
ht-degree: 27%

---

# Aktivitäts-QA

Verwenden Sie QA-URLs in [!DNL Adobe Target], um einfache End-to-End-Aktivitäts-QAs mit unveränderbaren Vorschaulinks, optionalem Zielgruppen-Targeting und QA-Berichten durchzuführen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.

Mit [!UICONTROL Activity QA] können Sie Ihre [!DNL Target] -Aktivitäten vollständig testen, bevor Sie sie live schalten. Die Funktion [!UICONTROL Activity QA] umfasst:

* Links zur Freigabe für Teammitglieder, die nie geändert werden oder eine Neuerstellung erfordern, unabhängig von Aktualisierungen der Erlebnisse oder Aktivitäten. Mit dieser Funktion können Sie Ihre Aktivitäten auf der gesamten Benutzer-Journey vollständig testen.
* Zielgruppenbedingungen werden optional respektiert, sodass Vermarkter Targeting-Kriterien testen oder Targeting-Kriterien für QA ignorieren können, ohne die Zielgruppenbedingungen erfüllen zu müssen.
* QA-Berichte werden erfasst, sodass Vermarkter bestätigen können, dass Metriken erwartungsgemäß inkrementiert werden und die QA-Berichtsdaten von den Produktionsberichten separiert bleiben (für Nicht-A4T-Berichte).
* Die Möglichkeit, eine Vorschau eines Erlebnisses isoliert oder mit anderen Live-Aktivitäten anzuzeigen, die die Versandkriterien erfüllen (Seitenanfrage/Zielgruppe/Seite/[!DNL Target]).
* Die Fähigkeit, einen QA-Bericht der gesamten User Journey zu erstellen. Mit dem QA-Link können Sie einmal auf Ihre Seite zugreifen und die gesamte Seite in Aktivitäts-QA durchsuchen. Sie verbleiben in Aktivitäts-QA, bis Sie die Sitzung beenden oder bis Sie das [QA Target-Lesezeichen](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) verwenden, um das Verlassen von [!UICONTROL Activity QA] zu erzwingen. Diese Funktion ist nützlich, wenn Sie eine Aktivität haben, die sich über mehrere Webseiten erstreckt.

  >[!NOTE]
  >
  >Diese Funktion gilt für at.js-Implementierungen mit Version 2.*x* oder höher. Für at.js 1.*x* -Implementierungen ist diese Funktion nur dann wahr, wenn der Browser des Besuchers keine Drittanbieter-Cookies blockiert.

## Zugreifen auf und Freigeben einer QA-URL {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Klicken Sie auf der [!UICONTROL Overview] -Seite einer Aktivität auf **[!UICONTROL Activity QA]**.

   ![Link „Aktivitäts-QA“](assets/qa_link.png)

1. Konfigurieren Sie die folgenden Einstellungen:

   ![Konfigurationsoptionen für QA-Links](assets/qa_link_config.png)

   * **[!UICONTROL Match audience rules to see experiences]:** Manchmal möchten Sie überprüfen, ob die Zielgruppenzuordnung funktioniert. Manchmal möchten Sie das Erscheinungsbild der Aktivität überprüfen. Wenn sich diese Einstellung in der Stellung „ein“ befindet, müssen Tester die Targeting-Anforderungen erfüllen, um sich für die Anzeige der Erlebnisse zu qualifizieren. Für Erlebnis-Targeting (XT)-Aktivitäten wird eine einzelne Aktivitäts-URL bereitgestellt. Das angezeigte Erlebnis richtet sich danach, ob Sie sich für eine der Targeting-Regeln qualifizieren.

     Wenn sich diese Einstellung in der Stellung „aus“ befindet, werden beim Klicken auf die Links die Erlebnisse angezeigt (unabhängig davon, ob Sie sich qualifizieren oder nicht). Bei der QA-Ausführung können Sie die Festlegung einer erforderlichen bzw. nicht erforderlichen Respektierung des Zielgruppen-Targetings ändern.

   * **Standardinhalt für alle anderen Aktivitäten anzeigen:** Wenn diese Option auf die &quot;Ein&quot;-Position umgeschaltet wird, wird für alle anderen Aktivitäten Standardinhalt angezeigt. Beispielsweise wird die Vorschau isoliert angezeigt, ohne alle anderen Live-Aktivitäten auf derselben Seite/[!DNL Target] -Anforderung zu berücksichtigen.

     Achten Sie auf Folgendes, wenn diese Einstellung auf „aus“ festgelegt ist:

      * Wenn Kollisionen zwischen der getesteten und anderen Live-Aktivitäten vorliegen, gelten die Regeln für die normale Priorität ](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F). [ Aufgrund von Kollisionen ist es möglich, dass Sie die Aktivität, die Sie zur Qualitätssicherung planen, nicht sehen können.
      * Die Metriken werden für die angezeigten Aktivitäten inkrementiert, jedoch nicht in der QA-Berichtsumgebung.

1. Klicken Sie auf **[!UICONTROL Done]** , um Ihre Änderungen zu speichern.
1. Geben Sie die Aktivitäts-Link-URLs zu Testzwecken für Mitglieder Ihres Unternehmens frei.

   Aktivitätslinks laufen nie ab und Sie müssen Links nicht erneut senden, wenn jemand eine Aktivität oder ein Erlebnis ändert. Wenn Sie jedoch eine andere Zielgruppe als die [!UICONTROL Audience Library] anwenden, anstatt die Aktivität einfach zu bearbeiten, wird ein neuer Link generiert, den Sie erneut freigeben müssen.

   Mit jeder Aktivitäts-Link-URL (für Erlebnis A, Erlebnis B usw.) können Sie die Journey des Benutzers aus dem entsprechenden Erlebnis starten. Klicken Sie auf die für ein Erlebnis generierte URL und fahren Sie dann mit dem normalen Site-Browsen fort, um Erlebnisse auf mehreren Seiten anzuzeigen (wenn mehrere Seiten vorhanden sind). Pro Erlebnis wird nur eine URL generiert, selbst wenn das Erlebnis mehrere Seiten umfasst (Vorlagentest oder mehrseitige Tests).

   Sie können auf der Site navigieren, um die anderen Seiten anzuzeigen, da der Modus [!UICONTROL Activity QA] fixierbar ist. Dies gilt für at.js-Implementierungen mit Version 2.*x* oder höher. Für at.js 1.*x* -Implementierungen verwenden, ist diese Situation nur dann wahr, wenn der Browser des Besuchers keine Drittanbieter-Cookies blockiert.

1. Um Berichte anzuzeigen, die aus Aktivitäts-Link-URLs generiert wurden, klicken Sie auf die Seite &quot;**[!UICONTROL Reports]**&quot; der Aktivität, klicken Sie auf das Symbol &quot;**[!UICONTROL Settings]**&quot;( ![icon_Zahnrad image](assets/icon_gear.png) ) und wählen Sie dann &quot;**[!UICONTROL QA Mode Traffic]**&quot; aus der Dropdownliste &quot;**[!UICONTROL Environment]**&quot;.

## Freigeben im QA-Modus

[!UICONTROL Activity QA] ist klebrig. Nachdem Sie eine Website in [!UICONTROL Activity QA] durchsucht haben, muss Ihre [!DNL Target] Sitzung ablaufen oder Sie müssen [!DNL Target] aus [!UICONTROL Activity QA] freigeben, bevor Sie Ihre Site wie einen normalen Besucher anzeigen können.

### at.js 2.*x* 

Wenn Ihre Site at.js 2.*x* bereitgestellt haben, verwenden Sie das [Target QA-Lesezeichen](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879), um sich von [!UICONTROL Activity QA] zu lösen. Wenn Sie eine Seite auf Ihrer Site mit einem leeren Wert laden, wie im nächsten Aufzählungszeichen beschrieben, wird das QA-Cookie *nicht* beim Laden von Seiten aus dem Browser entfernt, wenn at.js 2.*x* eingesetzt wird.

### at.js 1.*x*  

Wenn Ihre Site at.js 1.*x* bereitgestellt haben, können Sie sich zusätzlich zur Verwendung des [Target QA-Bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) auch manuell selbst erzwingen, indem Sie eine Seite auf Ihrer Site mit dem Parameter `at_preview_token` mit einem leeren Wert laden. Beispiel:

`https://www.mysite.com/?at_preview_token=`

### [!DNL Adobe Experience Platform Web SDK]

Wenn auf Ihrer Site [[!UICONTROL Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} bereitgestellt ist, können Sie sich manuell selbst ausdrücken, indem Sie eine Seite auf Ihrer Site mit dem Parameter `at_qa_mode` mit einem leeren Wert laden. Beispiel:

`https://www.mysite.com/?at_qa_mode=`

## Zu beachten {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Da Aktivitäts-QA jetzt für alle [!DNL Target] Aktivitätstypen verfügbar ist, ist die Funktion &quot;Vorschau von Automated Personalization-Aktivitäten mit Erlebnisvorschau-URLs&quot;nicht mehr erforderlich.
* [!UICONTROL Activity QA] Vorschaulinks für gespeicherte Aktivitäten werden möglicherweise nicht geladen, wenn Ihr Konto zu viele gespeicherte Aktivitäten enthält. Das erneute Wiederholen der Vorschau-Links sollte funktionieren. Um zu verhindern, dass diese Situation weiterhin eintritt, archivieren Sie gespeicherte Aktivitäten, die nicht mehr aktiv verwendet werden.
* [!UICONTROL Activity QA] URLs sind bei Aktivitäten mit [Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verfügbar. Treffer, die bei der Qualitätssicherung mit [!UICONTROL Activity QA] generiert wurden, werden in dieselbe Report Suite geleitet, in der die Daten der Aktivität auch nach der Live-Schaltung der Aktivität fließen.
* [!UICONTROL Activity QA] zeigt keine Inhalte für archivierte Aktivitäten oder Aktivitäten an, die seit ihrem Enddatum liegen. Wenn Sie eine beendete Aktivität deaktivieren, müssen Sie die Aktivität erneut speichern, damit [!UICONTROL Activity QA] funktioniert.
* In [!DNL Target Standard/Premium] importierte Aktivitäten (z. B. aus [!DNL Target Classic]) unterstützen keine QA-URLs.
* In den Aktivitäten [!UICONTROL Auto-Allocate] und [!UICONTROL Recommendations] ist das Modell nicht von den in [!UICONTROL Activity QA] erfassten Besuchen betroffen.
* Wenn Sie beim Erstellen der Aktivität [Verfeinerungen im formularbasierten Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) oder [Seitenbereitstellungsoptionen im Visual Experience Composer)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81) &quot;URL ist&quot;angegeben haben, funktioniert die QA-URL nicht, da [!UICONTROL Activity QA] URL-Parameter anhängt. Klicken Sie zur Lösung dieses Problems auf die QA-URL, um zu Ihrer Site zu navigieren. Entfernen Sie die angehängten Parameter aus der URL und laden Sie dann die neue URL.
* Wenn Sie at.js 1.Der Modus *x*, [!UICONTROL Activity QA] ist nicht fixierbar, wenn Sie Safari oder einen anderen Browser verwenden, der Drittanbieter-Cookies blockiert. In diesen Fällen müssen Sie die Vorschauparameter zu jeder URL hinzufügen, zu der Sie navigieren. Dasselbe gilt für die Implementierung von [CNAME](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html){target=_blank}.
* Wenn eine Aktivität mehrere Erlebniszielgruppen verwendet (z. B. eine Site aus den USA und Großbritannien, die in derselben Aktivität enthalten sind), werden für die vier Kombinationen (Erlebnis A/US Site, Erlebnis A/UK Site, Erlebnis B/US Site, Erlebnis B/UK Site) keine QA-Links generiert. Es werden nur zwei QA-Links (Erlebnis A und Erlebnis B) erstellt, und die Benutzer müssen sich für die entsprechende Zielgruppe qualifizieren, um die Seite anzeigen zu können. Eine QA-Person aus Großbritannien kann die US-Site nicht sehen.
* Alle Parameter und Werte vom Typ `at_preview` sind bereits URL-kodiert. Meistens funktioniert alles erwartungsgemäß. Einige Kunden müssen jedoch einen Lastenausgleich oder Webserver laden, die versuchen, die Abfragezeichenfolgenparameter erneut zu kodieren.

  Aufgrund dieser doppelten Kodierung kann [!DNL Target] den richtigen Tokenwert nicht extrahieren, wenn versucht wird, den `at_preview_token` zu dekodieren, sodass die Vorschau nicht funktioniert.[!DNL Target]

  [!DNL Adobe] empfiehlt, dass Sie sich an Ihr IT-Team wenden, um sicherzustellen, dass alle Vorschauparameter auf die Zulassungsliste gesetzt werden, damit diese Werte nicht umgewandelt werden.

  In der folgenden Tabelle sind die Parameter aufgeführt, die in Ihrer Domäne auf die Zulassungsliste gesetzt werden können:

  | Parameter | Typ | Wert | Beschreibung |
  |--- |--- |--- |--- |
  | `at_preview_token` | Verschlüsselte Zeichenfolge | Erforderlich; kein Standardwert | Eine verschlüsselte Entität mit der Liste der Kampagnen-IDs, die im QA-Modus ausgeführt werden können. |
  | `at_preview_index` | Zeichenfolge | Empty | Das Format des Parameters ist `<campaignIndex>` oder `<campaignIndex>_< experienceIndex>`<br>Beide Indizes beginnen mit 1. |
  | `at_preview_listed_activities_only` | Boolescher Wert (true/false) | Standardwert: false | Bei „true“ werden alle in den `at_preview_index`-Parametern angegebenen Kampagnen verarbeitet.<br>Bei „false“ werden alle Kampagnen der Seite bearbeitet, selbst wenn sie nicht im Vorschau-Token angegeben wurden. |
  | `at_preview_evaluate_as_true_audience_ids` | Zeichenfolge | Empty | Durch Unterstriche (_) getrennte Liste von segmentId-s, die (auf Targeting- und Berichterstellungsebene) im Rahmen der [!DNL Target] -Anfrage immer als &quot;true&quot;bewertet werden sollen. |
  | `_AT_Debug` | Zeichenfolge | Fenster oder Konsole | Konsolenprotokollierung oder neues Fenster. |
  | `adobe_mc_ref` |  |  | Übergibt gibt die verweisende URL der Standardseite an die neue Seite. Bei der Nutzung mit `AppMeasurement.js`-Version 2.1 (oder höher) verwendet [!DNL Adobe Analytics] diesen Parameterwert als Verweis-URL auf der neuen Seite. |
  | `adobe_mc_sdid` |  |  | Übergibt die [!DNL Supplemental Data Id] (SDID) und [!DNL Experience Cloud Org Id] von der Standardseite an die neue Seite. Durch Übergabe dieser IDs kann [!UICONTROL Analytics for Target] (A4T) die [!DNL Target] -Anfrage auf der Standardseite mit der [!DNL Analytics] -Anfrage auf der neuen Seite &quot;zusammenfügen&quot;. |

* Die Benutzeroberfläche von [!UICONTROL Target QA Mode] zeigt nur die erste URL eines Erlebnisses in einer mehrseitigen Aktivität an. Es wird angenommen, dass Sie einen Journey-Test erstellen und von URL1 zu URL2 wechseln. Wenn Sie jedoch unabhängig zu URL 2 wechseln möchten, kopieren Sie alle URL-Parameter, die neben URL1 angegeben sind, und wenden Sie sie nach dem Platzieren eines „?“ auf URL2 an, genau wie Sie sie in URL1 sehen.
* Vorschaulinks für die Aktivitäts-QA gespeicherter Aktivitäten werden möglicherweise nicht geladen, wenn im Konto zu viele gespeicherte Aktivitäten vorhanden sind. Versuchen Sie die Vorschaulinks erneut zu laden. Archivieren Sie gespeicherte Aktivitäten, die nicht mehr aktiv verwendet werden, um zu verhindern, dass dieses Problem weiterhin auftritt.

## Kompatibilität der Target JavaScript-Bibliothek [!UICONTROL QA Mode] {#compatibility}

[!DNL Target] unterstützt die folgenden JavaScript-Bibliotheken:

* [at.js 1.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de)

In der folgenden Tabelle sind die verschiedenen Aktivitätstypen aufgeführt und es wird angegeben, ob der [!UICONTROL Activity QA] -Modus für jede Bibliothek unterstützt wird:

| Aktivitätstyp | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B Test] | Ja | Ja | Ja |
| [!UICONTROL Auto-Allocate] | Ja | Ja | Ja |
| [!UICONTROL Auto-Target] | Ja | Ja | Ja |
| [!UICONTROL Automated Personalization] (AP) | Ja | Ja | Ja |
| [!UICONTROL Experience Targeting] (XT) | Ja | Ja | Ja |
| [!UICONTROL Multivariate Test] (MVT) | Ja | Ja | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja |