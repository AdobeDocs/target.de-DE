---
keywords: qa; qa-Modus; activity qa; qa url; qa urls; Vorschau-URL; Vorschau-URL
description: Erfahren Sie, wie Sie Adobe verwenden [!DNL Target] QA-URLs zur einfachen End-to-End-Aktivitäts-QAs mit unveränderbaren Vorschaulinks, optionalem Zielgruppen-Targeting und QA-Berichten, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.
title: Wie kann ich QA-Aktivitäten durchführen?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 38%

---

# Aktivitäts-QA

Verwenden von QA-URLs in [!DNL Adobe Target] zur einfachen End-to-End-Aktivitäts-QA mit unveränderbaren Vorschaulinks, optionalem Zielgruppen-Targeting und QA-Berichten, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.

[!UICONTROL Aktivitäts-QA] Sie können Ihre [!DNL Target] -Aktivitäten, bevor sie live geschaltet werden. Die [!UICONTROL Aktivitäts-QA] umfasst:

* Links für die Freigabe für Team-Mitglieder, die sich nie ändern oder nie neu generiert werden müssen. Dies ist unabhängig von an den Erlebnissen oder Aktivitäten vorgenommenen Aktualisierungen. Mit dieser Funktion können Sie Ihre Aktivitäten auf der gesamten Benutzer-Journey vollständig testen.
* Zielgruppenbedingungen werden optional respektiert, sodass Vermarkter Targeting-Kriterien testen oder Targeting-Kriterien für QA ignorieren können, ohne die Zielgruppenbedingungen erfüllen zu müssen.
* QA-Berichte werden erfasst, sodass Vermarkter bestätigen können, dass Metriken erwartungsgemäß inkrementiert werden und die QA-Berichtsdaten von den Produktionsberichten separiert bleiben (für Nicht-A4T-Berichte).
* Die Möglichkeit, eine Vorschau eines Erlebnisses isoliert oder mit anderen Live-Aktivitäten anzuzeigen, die die Versandkriterien erfüllen (Seite/Target-Anforderung/Zielgruppe).
* Die Fähigkeit, einen QA-Bericht der gesamten User Journey zu erstellen. Mit dem QA-Link können Sie einmal auf Ihre Seite zugreifen und die gesamte Seite in Aktivitäts-QA durchsuchen. Sie bleiben in Activity-QA, bis Sie die Sitzung beenden oder Sie das  [QA Target-Bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)[!UICONTROL  verwenden, um das Beenden von Aktivitäts-QA zu erzwingen]. Diese Funktion ist nützlich, wenn Sie eine Aktivität haben, die sich über mehrere Webseiten erstreckt.

   >[!NOTE]
   >
   >Diese Funktion gilt für at.js-Implementierungen mit Version 2.*x* oder höher. Für at.js 1.*x* -Implementierungen ist diese Funktion nur dann wahr, wenn der Browser des Besuchers keine Drittanbieter-Cookies blockiert.

## Zugreifen auf und Freigeben einer QA-URL {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. In einer Aktivität [!UICONTROL Übersicht] klicken Sie auf die **[!UICONTROL Aktivitäts-QA]** Link.

   ![Link „Aktivitäts-QA“](assets/qa_link.png)

1. Konfigurieren Sie die folgenden Einstellungen:

   ![Konfigurationsoptionen für QA-Links](assets/qa_link_config.png)

   * **[!UICONTROL Zielgruppenregeln abgleichen, um Erlebnisse anzuzeigen]:** Manchmal möchten Sie überprüfen, ob die Zielgruppenzuordnung funktioniert. Manchmal möchten Sie das Erscheinungsbild der Aktivität überprüfen. Wenn sich diese Einstellung in der Stellung „ein“ befindet, müssen Tester die Targeting-Anforderungen erfüllen, um sich für die Anzeige der Erlebnisse zu qualifizieren. Für Erlebnis-Targeting (XT)-Aktivitäten wird eine einzelne Aktivitäts-URL bereitgestellt. Das angezeigte Erlebnis richtet sich danach, ob Sie sich für eine der Targeting-Regeln qualifizieren.

      Wenn sich diese Einstellung in der Stellung „aus“ befindet, werden beim Klicken auf die Links die Erlebnisse angezeigt (unabhängig davon, ob Sie sich qualifizieren oder nicht). Bei der QA-Ausführung können Sie die Festlegung einer erforderlichen bzw. nicht erforderlichen Respektierung des Zielgruppen-Targetings ändern.

   * **Standardinhalt für alle anderen Aktivitäten anzeigen:** Wenn diese Option auf die Position &quot;Ein&quot;umgeschaltet wird, wird für alle anderen Aktivitäten Standardinhalt angezeigt. Beispielsweise wird die Vorschau isoliert angezeigt, ohne alle anderen Live-Aktivitäten auf derselben Seite/ zu berücksichtigen[!DNL Target] -Anfrage.

      Achten Sie auf Folgendes, wenn diese Einstellung auf „aus“ festgelegt ist:

      * Wenn Kollisionen zwischen der getesteten und anderen Live-Aktivitäten vorliegen,  [gelten die normalen Prioritätsregeln](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F). Aufgrund von Kollisionen ist es möglich, dass Sie die Aktivität, die Sie zur Qualitätssicherung planen, nicht sehen können.
      * Die Metriken werden für die angezeigten Aktivitäten inkrementiert, jedoch nicht in der QA-Berichtsumgebung.

1. Klicken Sie auf **[!UICONTROL Fertig]**, um Ihre Änderungen zu speichern.
1. Geben Sie die Aktivitäts-Link-URLs zu Testzwecken für Mitglieder Ihres Unternehmens frei.

   Aktivitätslinks laufen nie ab und Sie müssen Links nicht erneut senden, wenn jemand eine Aktivität oder ein Erlebnis ändert. Wenn Sie jedoch eine andere Zielgruppe als die [!UICONTROL Zielgruppenbibliothek], anstatt die Aktivität einfach zu bearbeiten, wird ein neuer Link generiert, den Sie erneut freigeben müssen.

   Mit jeder Aktivitäts-Link-URL (für Erlebnis A, Erlebnis B usw.) können Sie die Journey des Benutzers aus dem entsprechenden Erlebnis starten. Klicken Sie auf die für ein Erlebnis generierte URL und fahren Sie dann mit dem normalen Site-Browsen fort, um Erlebnisse auf mehreren Seiten anzuzeigen (wenn mehrere Seiten vorhanden sind). Pro Erlebnis wird nur eine URL generiert. Dies ist selbst dann der Fall, wenn das Erlebnis mehrere Seiten überspannt (Vorlagentest oder Test mit mehreren Seiten).

   Sie können auf der Site navigieren, um die anderen Seiten anzuzeigen, da die [!UICONTROL Aktivitäts-QA] -Modus hängt. Dies gilt für at.js-Implementierungen mit Version 2.*x* oder höher. Für at.js 1.*x* -Implementierungen verwenden, ist diese Situation nur dann wahr, wenn der Browser des Besuchers keine Drittanbieter-Cookies blockiert.

1. Um Berichte anzuzeigen, die über Aktivitäts-Link-URLs generiert wurden, klicken Sie auf die **[!UICONTROL Berichte]** klicken Sie auf die **[!UICONTROL Einstellungen]** Symbol (  ![](assets/icon_gear.png) ), wählen Sie **[!UICONTROL QA-Modus-Traffic]** von **[!UICONTROL Umgebung]** Dropdown-Liste.

## Zu beachten {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Die [!UICONTROL Aktivitäts-QA] Der Link wird auf der Seite [!UICONTROL Übersicht] Seite aller Aktivitätstypen außer [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization] (AP).
* [!UICONTROL Vorschaulinks für die Aktivitäts-QA gespeicherter Aktivitäten werden möglicherweise nicht geladen, wenn im Konto zu viele gespeicherte Aktivitäten vorhanden sind. ] Das erneute Wiederholen der Vorschau-Links sollte funktionieren. Um zu verhindern, dass diese Situation weiterhin eintritt, archivieren Sie gespeicherte Aktivitäten, die nicht mehr aktiv verwendet werden.
* [!UICONTROL Aktivitäts-QA-URLs sind für Aktivitäten mit Analytics als Berichtsquelle (A4T) verfügbar. ] Treffer, die bei der Qualitätssicherung mithilfe von [!UICONTROL Aktivitäts-QA] fließen in dieselbe Report Suite, in die die Daten der Aktivität fließen, auch wenn die Aktivität aktiv ist.
* [!UICONTROL Aktivitäts-QA zeigt keinen Inhalt für archivierte Aktivitäten oder Aktivitäten an, deren Enddatum vorüber ist. ] Wenn Sie eine beendete Aktivität deaktivieren, müssen Sie die Aktivität erneut für [!UICONTROL Aktivitäts-QA] arbeiten.
* Importierte Aktivitäten in [!DNL Target Standard/Premium] (von [!DNL Target Classic](z. B.) keine QA-URLs unterstützen.
* In [!UICONTROL Automatische Zuordnung] und [!UICONTROL Recommendations] -Aktivitäten, ist das Modell nicht von den Besuchen betroffen, die in [!UICONTROL Aktivitäts-QA].
* [!UICONTROL Aktivitäts-QA] klebrig ist. Nachdem Sie eine Website in [!UICONTROL Aktivitäts-QA], Ihre [!DNL Target] -Sitzung muss ablaufen oder Sie müssen [!DNL Target] freigeben von [!UICONTROL Aktivitäts-QA] bevor Sie Ihre Site wie einen normalen Besucher anzeigen können. Verwenden Sie das [Target QS-Bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)[!UICONTROL , um das Beenden der Aktivitäts-QS zu erzwingen].

   Sie können sich auch manuell selbst aus dem Modus lösen, indem Sie auf Ihrer Site eine Seite laden, wobei der Parameter `at_preview_token` einen leeren Wert hat (beispielsweise `https://www.mysite.com/?at_preview_token=`).

* Wenn Sie bei der Erstellung der Aktivität &quot;URL ist&quot;angegeben haben [Verfeinerungen im formularbasierten Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) oder [Seitenbereitstellungsoptionen im Visual Experience Composer)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), funktioniert die QA-URL nicht, da [!UICONTROL Aktivitäts-QA] hängt URL-Parameter an. Klicken Sie zur Lösung dieses Problems auf die QA-URL, um zu Ihrer Site zu navigieren. Entfernen Sie die angehängten Parameter aus der URL und laden Sie dann die neue URL.
* Wenn Sie at.js 1.*x*, [!UICONTROL Aktivitäts-QA] -Modus hängt nicht an, wenn Sie Safari oder einen anderen Browser verwenden, der Drittanbieter-Cookies blockiert. In diesen Fällen müssen Sie die Vorschauparameter zu jeder URL hinzufügen, zu der Sie navigieren. Dasselbe gilt, wenn Sie [CNAME](/help/main/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md).
* Wenn eine Aktivität mehrere Erlebniszielgruppen verwendet (z. B. eine Site aus den USA und Großbritannien, die in derselben Aktivität enthalten sind), werden für die vier Kombinationen (Erlebnis A/US Site, Erlebnis A/UK Site, Erlebnis B/US Site, Erlebnis B/UK Site) keine QA-Links generiert. Es werden nur zwei QA-Links (Erlebnis A und Erlebnis B) erstellt, und die Benutzer müssen sich für die entsprechende Zielgruppe qualifizieren, um die Seite anzeigen zu können. Eine QA-Person aus Großbritannien kann die US-Site nicht sehen.
* Alle Parameter und Werte vom Typ `at_preview` sind bereits URL-kodiert. Meistens funktioniert alles erwartungsgemäß. Einige Kunden müssen jedoch einen Lastenausgleich oder Webserver laden, die versuchen, die Abfragezeichenfolgenparameter erneut zu kodieren.

   Aufgrund dieser doppelten Kodierung, wenn [!DNL Target] versucht, die `at_preview_token`, [!DNL Target] kann nicht den richtigen Tokenwert extrahieren, was dazu führt, dass die Vorschau nicht funktioniert.

   Adobe empfiehlt, dass Sie sich an Ihr IT-Team wenden, um sicherzustellen, dass alle Vorschauparameter auf die Zulassungsliste gesetzt werden, damit diese Werte nicht umgewandelt werden.

   In der folgenden Tabelle sind die Parameter aufgeführt, die in Ihrer Domäne auf die Zulassungsliste gesetzt werden können:

   | Parameter | Typ | Wert | Beschreibung |
   |--- |--- |--- |--- |
   | `at_preview_token` | Verschlüsselte Zeichenfolge | Erforderlich; kein Standardwert | Eine verschlüsselte Entität, die die Liste der Kampagnen-IDs enthält, die im QA-Modus ausgeführt werden können. |
   | `at_preview_index` | Zeichenfolge | Empty | Das Format des Parameters ist `<campaignIndex>` oder `<campaignIndex>_< experienceIndex>`<br>Beide Indexes beginnen mit 1. |
   | `at_preview_listed_activities_only` | Boolescher Wert (true/false) | Standardwert: false | Bei „true“ werden alle in den `at_preview_index`-Parametern angegebenen Kampagnen verarbeitet.<br>Bei „false“ werden alle Kampagnen der Seite bearbeitet, selbst wenn sie nicht im Vorschau-Token angegeben wurden. |
   | `at_preview_evaluate_as_true_audience_ids` | Zeichenfolge | Empty | Durch Unterstriche (_) getrennte Liste von segmentId-s, die immer (auf Targeting- und Berichtsebene) im Bereich der [!DNL Target] -Anfrage. |
   | `_AT_Debug` | Zeichenfolge | Fenster oder Konsole | Konsolenprotokollierung oder neues Fenster. |
   | `adobe_mc_ref` |  |  | Übergibt gibt die verweisende URL der Standardseite an die neue Seite. Bei der Nutzung mit `AppMeasurement.js`-Version 2.1 (oder höher) verwendet [!DNL Adobe Analytics] diesen Parameterwert als Verweis-URL auf der neuen Seite. |
   | `adobe_mc_sdid` |  |  | Übergibt die [!DNL Supplemental Data Id] (SDID) und [!DNL Experience Cloud Org Id] von der Standardseite zur neuen Seite. Die Übergabe dieser IDs ermöglicht Folgendes: [!UICONTROL Analytics for Target] (A4T), um die [!DNL Target] -Anfrage auf der Standardseite mit der [!DNL Analytics] -Anfrage auf der neuen Seite. |

* Die [!UICONTROL Target QA-Modus] Die Benutzeroberfläche zeigt nur die erste URL eines Erlebnisses in einer mehrseitigen Aktivität an. Es wird angenommen, dass Sie einen Journey-Test erstellen und von URL1 zu URL2 wechseln. Wenn Sie jedoch unabhängig zu URL 2 wechseln möchten, kopieren Sie alle URL-Parameter, die neben URL1 angegeben sind, und wenden Sie sie nach dem Platzieren eines „?“ auf URL2 an, genau wie Sie sie in URL1 sehen.

## Kompatibilität der JavaScript-Target-Bibliothek [!UICONTROL QA-Modus] {#compatibility}

[!DNL Target] unterstützt die folgenden JavaScript-Bibliotheken:

* [at.js 1.x](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)
* [at.js 2.x](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)
* [Adobe Experience Platform Web SDK](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)

In der folgenden Tabelle sind die verschiedenen Aktivitätstypen aufgeführt und es wird angegeben, ob [!UICONTROL Aktivitäts-QA] -Modus wird für jede Bibliothek unterstützt:

| Aktivitätstyp | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B-Test] | Ja | Ja | Ja |
| [!UICONTROL Automatische Zuordnung] | Ja | Ja | Ja |
| [!UICONTROL Automatisches Targeting] | Nein | Nein | Nein |
| [!UICONTROL Automatisierte Personalisierung] (AP) | Nein | Nein | Nein |
| [!UICONTROL Erlebnis-Targeting] (XT) | Ja | Ja | Ja |
| [!UICONTROL Multivariate Tests] (MVT) | Ja | Ja | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja |

## Vorschau von URLs {#preview}

URLs für die Erlebnisvorschau können für alle [!DNL Target] Aktivitätstypen. Mithilfe von Vorschau-URLs können Sie Erlebnisinhalte direkt auf Ihrer Site anzeigen, bevor die Aktivität für Vorschau- und QA-Zwecke live ist. URLs für die Erlebnisvorschau umgehen das Targeting, um die Anzeige eines bestimmten Erlebnisses zu erzwingen.

Informationen zur Funktion von Vorschau-URLs mit [!UICONTROL Automated Personalization] (AP)-Aktivitäten, siehe [Vorschau von Automated Personalization-Aktivitäten mit Erlebnisvorschau-URLs](/help/main/c-activities/t-automated-personalization/experience-preview.md).

Um auf eine Vorschau-URL zuzugreifen und diese freizugeben, verwenden Sie **[!UICONTROL Übersicht]** klicken Sie auf die **[!UICONTROL Aktivitäts-QA]** Link.

>[!NOTE]
>
>Die [!UICONTROL Aktivitäts-QA] und die Vorschau-URL für alle anderen Aktivitäten als [!DNL Target] AP-Aktivitäten.

In der folgenden Tabelle sind die verschiedenen Aktivitätstypen aufgeführt und es wird angegeben, ob die Vorschau-URLs-Funktion für jede Bibliothek oder API unterstützt wird:

| Aktivitätstyp | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B-Test] | Ja | Ja | Ja |
| [!UICONTROL Automatische Zuordnung] | Ja | Ja | Ja |
| [!UICONTROL Automatisches Targeting] | Ja | Ja | Ja |
| [!UICONTROL Automatisierte Personalisierung] (AP) | Ja | Ja | Ja |
| [!UICONTROL Erlebnis-Targeting] (XT) | Ja | Ja | Ja |
| [!UICONTROL Multivariate Tests] (MVT) | Ja | Ja | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja |

