---
description: Mithilfe von QA-URLs können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.
keywords: QS; Vorschau; Vorschaulinks
seo-description: Mithilfe von QA-URLs können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.
seo-title: Aktivitäts-QA
solution: Target
title: Aktivitäts-QA
topic: Advanced,Standard,Classic
uuid: 58d99940-7c3d-41ab-a2f5-a87c880dbc17
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Aktivitäts-QA{#activity-qa}

Mithilfe von QA-URLs können Sie einfach End-to-End-Aktivitäts-QAs durchführen und unveränderbare Vorschaulinks, ein optionales Zielgruppen-Targeting und QA-Berichte einfügen, die basierend auf Live-Aktivitätsdaten segmentiert bleiben.

## Überblick {#section_11B761A522A14E61978275772210A4C2}

Mithilfe von Aktivitäts-QAs können Sie Ihre Target-Aktivitäten vor dem Live-Start in vollem Umfang testen. Die QA-Funktionalität für Aktivitäten beinhaltet Folgendes:

* Links für die Freigabe für Team-Mitglieder, die sich nie ändern oder nie neu generiert werden müssen. Dies ist unabhängig von an den Erlebnissen oder Aktivitäten vorgenommenen Aktualisierungen. Dadurch können Sie Ihre Aktivitäten vollständig über die gesamte Benutzerreise hinweg testen.
* Zielgruppenbedingungen werden optional respektiert, sodass Vermarkter Targeting-Kriterien testen oder Targeting-Kriterien für QA ignorieren können, ohne die Zielgruppenbedingungen erfüllen zu müssen.
* QA-Berichte werden erfasst, sodass Vermarkter bestätigen können, dass Metriken erwartungsgemäß inkrementiert werden und die QA-Berichtsdaten von den Produktionsberichten separiert bleiben (für Nicht-A4T-Berichte).
* Die Fähigkeit, eine Vorschau für ein Erlebnis anzuzeigen, das isoliert oder gemeinsam mit anderen Live-Aktivitäten angezeigt wird, die die Bereitstellungskriterien erfüllen (Seite/mbox/Zielgruppe).
* Die Fähigkeit zur Qualitätssicherung der gesamten Benutzerreise. Mit dem QA-Link können Sie einmal auf Ihre Seite zugreifen und die gesamte Seite in Aktivitäts-QA durchsuchen. Sie bleiben in Aktivitäts-QA, bis Sie die Sitzung beenden oder Sie das   [QA Target-Bookmarklet](../../c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) verwenden, um das Beenden von Aktivitäts-QA zu erzwingen. Diese Funktion ist besonders hilfreich, wenn Sie eine Aktivität haben, die sich über mehrere Webseiten erstreckt.

## Zugreifen auf und Freigeben einer QA-URL {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Klicken Sie auf der Seite [!UICONTROL Übersicht] einer Aktivität (alle Typen außer „Automatisierte Personalisierung“) auf den Link **[!UICONTROL Aktivitäts-QA].**

   ![](assets/qa_link.png)

1. Konfigurieren Sie die folgenden Einstellungen:

   ![](assets/qa_link_config.png)

   * **Passen Sie die Zielgruppen-Regeln an, um die Erlebnisse anzuzeigen:** Mitunter möchten Sie sicherstellen, dass die Zielgruppenzuordnung funktioniert. In anderen Situationen möchten Sie lediglich die Anmutung der Aktivität prüfen. Wenn sich diese Einstellung in der Stellung „ein“ befindet, müssen Tester die Targeting-Anforderungen erfüllen, um sich für die Anzeige der Erlebnisse zu qualifizieren. Für Erlebnis-Targeting (XT)-Aktivitäten wird eine einzelne Aktivitäts-URL bereitgestellt. Das angezeigte Erlebnis richtet sich danach, ob Sie sich für eine der Targeting-Regeln qualifizieren.

      Wenn sich diese Einstellung in der Stellung „aus“ befindet, werden beim Klicken auf die Links die Erlebnisse angezeigt (unabhängig davon, ob Sie sich qualifizieren oder nicht). Bei der QA-Ausführung können Sie die Festlegung einer erforderlichen bzw. nicht erforderlichen Respektierung des Zielgruppen-Targetings ändern.

   * **Für alle anderen Aktivitäten Standardinhalt anzeigen:** Wenn sich diese Option in der Stellung „ein“ befindet, wird Standardinhalt für alle anderen Aktivitäten angezeigt (zum Beispiel wird die Vorschau isoliert und ohne die ganzen anderen Live-Aktivitäten derselben Seite/Mbox angezeigt.

      Achten Sie auf Folgendes, wenn diese Einstellung auf „aus“ festgelegt ist:

      * Wenn Kollisionen zwischen der getesteten und anderen Live-Aktivitäten vorliegen,   [gelten die normalen Prioritätsregeln](../../c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F). Aufgrund dessen ist es möglich, dass die gewünschte QA-Aktivität nicht angezeigt wird.
      * Die Metriken werden für die angezeigten Aktivitäten inkrementiert, jedoch nicht in der QA-Berichtsumgebung.

1. Klicken Sie auf **[!UICONTROL Fertig], um Ihre Änderungen zu speichern.**
1. Geben Sie die Activity-Link-URLs zu Testzwecken für Mitglieder Ihrer Organisation frei.

   Activity-Links laufen niemals ab, und die Links müssen nicht erneut gesendet werden, wenn jemand Änderungen an einer Aktivität oder an einem Erlebnis vornimmt. Wenn Sie jedoch eine andere Zielgruppe aus der Zielgruppenbibliothek anwenden, anstatt die Aktivität einfach zu bearbeiten, wird ein neuer Link generiert, den Sie erneut freigeben müssen.

   Mithilfe der einzelnen Activity-Link-URLs (für Exp A, Exp B usw.) können Sie die User Journey vom entsprechenden Erlebnis starten. Sie können auf die für ein Erlebnis generierte URL klicken und dann mit dem normalen Website-Browsing fortfahren, um Erlebnisse auf mehreren Seiten anzuzeigen (wenn mehrere Seiten vorhanden sind). Pro Erlebnis wird nur eine URL generiert. Dies ist selbst dann der Fall, wenn das Erlebnis mehrere Seiten überspannt (Vorlagentest oder Test mit mehreren Seiten). Sie können auf der Website navigieren, um die anderen Seiten anzuzeigen, weil Aktivitäts-QA hängt.

1. Wenn Sie die über Activity-Link-URLs generierten Berichte anzeigen möchten, klicken Sie auf die Seite **[!UICONTROL Berichte]** der Aktivität, klicken Sie auf das Symbol **[!UICONTROL Einstellungen]** (![](assets/icon_gear.png)) und wählen Sie dann **[!UICONTROL QS-Modus]** aus der Dropdown-Liste **[!UICONTROL Umgebung]** aus.

## Zu beachten {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Der Link [!UICONTROL Aktivitäts-QA] wird auf der Seite [!UICONTROL Übersicht] aller Aktivitätstypen angezeigt, außer für die automatisierte Personalisierung (AP). Sie können [Links](../../c-activities/t-automated-personalization/experience-preview.md#task_586C6655A6FD4AF08F5678FC3F481EFC) für AP-Aktivitäten in der Vorschau anzeigen.
* Aktivitäts-QA-URLs sind für Aktivitäten mit Analytics als Berichtsquelle (A4T) verfügbar. Treffer, die generiert werden, während QA mit Aktivitäts-QA ausgeführt wird, werden in dieselbe Report Suite geleitet, wie die Daten der Aktivität, auch nachdem die Aktivität live geschaltet wurde.
* Aktivitäts-QA zeigt keinen Inhalt für archivierte Aktivitäten oder Aktivitäten an, deren Enddatum vorüber ist. Wenn Sie eine beendete Aktivität deaktivieren, müssen Sie die Aktivität erneut speichern, damit Aktivitäts-QA funktioniert.
* In Target Standard/Premium importierte Aktivitäten (beispielsweise aus Target Classic) unterstützen keine QA-URLs.
* Bei Aktivitäten für die automatisierte Zuweisung, das automatische Targeting und für Recommendations wird das Modell nicht von den in Aktivitäts-QA erfassten Besuchen beeinflusst.
* Da Activity-QA nach dem Website-Browsen in Aktivitäts-QA hängt, muss die Target-Sitzung ablaufen oder Target muss Sie aus Aktivitäts-QA freigeben, bevor Sie Ihre Website wie ein normaler Besucher anzeigen können. Verwenden Sie das [Target QS-Bookmarklet](../../c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879), um das Beenden der Aktivitäts-QS zu erzwingen.

   Sie können sich auch manuell selbst aus dem Modus lösen, indem Sie auf Ihrer Site eine Seite laden, wobei der Parameter `at_preview_token` einen leeren Wert hat (beispielsweise `https://www.mysite.com/?at_preview_token=`).

* Wenn Sie während der Erstellung der Aktivitäts-[Feinheiten im Form-Based Composer](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) oder [Seitenbereitstellungsoptionen im Visual Experience Composer](../../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81) „URL ist“ angegeben haben, funktioniert die QS-URL nicht, da die Aktivitäts-QS URL-Parameter anhängt. Klicken Sie zur Lösung dieses Problems auf die QA-URL, um zu Ihrer Site zu navigieren. Entfernen Sie die angehängten Parameter aus der URL und laden Sie dann die neue URL.
* In Safari-Browsern müssen Drittanbieter-Cookies aktiviert werden, damit Aktivitäts-QA ordnungsgemäß funktioniert.
* Wenn eine Aktivität mehrere Erlebniszielgruppen verwendet (z. B. eine in derselben Aktivität enthaltene US- und UK-Site), werden keine QA-Links für die vier Kombinationen generiert (Erlebnis A/US-Site, Erlebnis A/UK-Site, Erlebnis B/US-Site, Erlebnis B/UK-Site). Es werden nur zwei QA-Links (Erlebnis A und Erlebnis B) erstellt, und die Benutzer müssen sich für die entsprechende Zielgruppe qualifizieren, um die Seite anzeigen zu können. Eine Person mit QA für UK kann die US-Site nicht anzeigen.
* Alle Parameter und Werte vom Typ `at_preview` sind bereits URL-kodiert. Meistens funktioniert alles erwartungsgemäß. Möglicherweise haben einige Kunden jedoch Systeme zur Lastverteilung oder Webserver, die versuchen, die Abfragezeichenfolgenparameter erneut zu kodieren.

   Aufgrund dieser doppelten Kodierung kann Target den richtigen Tokenwert nicht extrahieren, wenn Sie versuchen, `at_preview_token` zu dekodieren, wodurch die Vorschau nicht funktioniert.

   Sie sollten mit Ihrem IT-Team Rücksprache halten, um sicherzustellen, dass alle Vorschauparameter auf die Positivliste gesetzt werden, damit diese Werte nicht umgewandelt werden.

   In der folgenden Tabelle finden Sie die Parameter, die in Ihrer Domain zur Whitelist hinzugefügt werden können:

   | Parameter | Typ | Wert | Beschreibung |
   |--- |--- |--- |--- |
   | `at_preview_token` | Verschlüsselte Zeichenfolge | Erforderlich; kein Standardwert | Ein verschlüsseltes Element, das die Liste der Kampagnen-IDs enthält, die im QA-Modus ausgeführt werden dürfen. |
   | `at_preview_index` | Zeichenfolge | Empty | Das Format des Parameters ist `<campaignIndex>` oder `<campaignIndex>_< experienceIndex>`<br>Beide Indexes beginnen mit 1. |
   | `at_preview_listed_activities_only` | Boolescher Wert (true/false) | Standardwert: false | Bei „true“ werden alle in den `at_preview_index`-Parametern angegebenen Kampagnen verarbeitet.<br>Bei „false“ werden alle Kampagnen der Seite bearbeitet, selbst wenn sie nicht im Vorschautoken angegeben wurden. |
   | `at_preview_evaluate_as_true_audience_ids` | Zeichenfolge | Empty | Durch Unterstriche (_) getrennte Liste der segmentIds, die (auf Targeting- und Reporting-Ebene) im Rahmen der Mbox-Anfrage immer mit „true“ bewertet werden sollten. |
   | `_AT_Debug` | Zeichenfolge | Fenster oder Konsole | Konsolenprotokollierung oder neues Fenster. |
   | `adobe_mc_ref` | Übergibt gibt die verweisende URL der Standardseite an die neue Seite. Bei der Nutzung mit `AppMeasurement.js`-Version 2.1 (oder höher) verwendet [!DNL Adobe Analytics] diesen Parameterwert als Verweis-URL auf der neuen Seite. |
   | `adobe_mc_sdid` | Übergibt die [!DNL Supplemental Data Id] (SDID) und [!DNL Experience Cloud Org Id] von der Standardseite an die neue Seite, damit Analytics für Target (A4T) die Target-Anfrage auf der Standardseite mit der Analytics-Anfrage auf der neuen Seite verknüpfen kann. |

* Die Benutzeroberfläche von Target QA Mode zeigt nur die erste URL eines Erlebnisses in einer mehrseitigen Aktivität an. Hierbei wird angenommen, dass Sie einen Reisetest erstellen und Sie von URL 1 zu URL 2 wechseln. Wenn Sie jedoch URL 2 unabhängig aufrufen möchten, kopieren Sie alle URL-Parameter für URL 1 und wenden Sie sie auf URL 2 an, nachdem Sie eine &quot;? « genau wie Sie in URL 1 sehen.