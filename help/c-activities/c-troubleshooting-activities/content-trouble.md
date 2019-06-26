---
description: Wenn Ihre Seite nicht den erwarteten Inhalt anzeigt, gibt es ein paar Schritte, die Sie unternehmen können, um eine Fehlerdiagnose für die Inhaltsbereitstellung vorzunehmen.
keywords: Mbox debuggen;Fehlerbehebung für Mbox;Mbox-Probleme;Flackern;mboxDebug;mboxTrace;Token;Debugger;Priorität;Aktivitätspriorität;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst Mbox kaufen;bester Verkauf;bestverkauftes Produkt
seo-description: Wenn Ihre Seite nicht den erwarteten Inhalt anzeigt, gibt es ein paar Schritte, die Sie unternehmen können, um eine Fehlerdiagnose für die Inhaltsbereitstellung vorzunehmen.
seo-title: Fehlerbehebung bei der Inhaltsbereitstellung
solution: Target
subtopic: Multivarianz-Test
title: Fehlerbehebung bei der Inhaltsbereitstellung
topic: Standard
uuid: 8837d07a-f793-495e-a6c1-b9c35fbe18b1
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Fehlerbehebung bei der Inhaltsbereitstellung{#troubleshoot-content-delivery}

Wenn Ihre Seite nicht den erwarteten Inhalt anzeigt, gibt es ein paar Schritte, die Sie unternehmen können, um eine Fehlerdiagnose für die Inhaltsbereitstellung vorzunehmen.

* Prüfen Sie den Code für Ihre Aktivität bzw. Kampagne sorgfältig. Ein Tippfehler oder ein anderweitiger Fehler könnte die Ursache dafür sein, dass der erwartete Inhalt nicht angezeigt wird.
* Verwenden Sie mboxTrace oder mboxDebug, um eine Fehlerdiagnose für die Mbox vorzunehmen.
* Mit dem Adobe Experience Cloud-Debugger erhalten Sie ein einfach verwendbares Werkzeug, das für die Fehlerbehebung bei der Mbox fast die gleiche Informationsmenge bereitstellt wie mboxDebug.

mboxDebug ist insbesondere dann nützlich, wenn Sie Target auf Ihrer Seite einrichten, um zu gewährleisten, dass Mbox anspricht und das Cookie eingestellt wird. Jedoch ist mboxDebug nicht so detailliert, wie es für die Fehlerdiagnose bei der Inhaltsbereitstellung nützlich wäre. Wenn Ihre Aktivität nicht auf Ihrer Seite erscheint oder unerwünschter Inhalt eingeblendet wird, verwenden Sie mboxTrace, um die Seite ausführlich zu untersuchen und Fehler zu diagnostizieren.

## Abrufen des Autorisierungstokens zur Verwendung mit Debuggingwerkzeugen {#section_BED130298E794D1FA229DB7C3358BA54}

Da mboxTrace und mboxDebug Kampagnen- und Profildaten für Dritte enthüllen können, ist ein Autorisierungstoken erforderlich. Das Autorisierungstoken kann in der [!DNL Target]-Benutzeroberfläche abgerufen werden. Das Token ist sechs Stunden lang gültig.

So wird das Autorisierungstoken abgerufen:

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]**.
1. Wählen Sie **[!UICONTROL mbox.js]** oder **[!UICONTROL at.js]** aus.
1. Klicken Sie auf **[!UICONTROL Authentifizierungstoken generieren]**.

   ![Autorisierungstoken generieren](/help/c-activities/c-troubleshooting-activities/assets/generate-auth-token.png)

1. Fügen Sie das generierte Token Ihrer URL als Parameter hinzu, um eines der erweiterten Debuggingwerkzeuge zu aktivieren.

   ![Autorisierungstoken](/help/c-activities/c-troubleshooting-activities/assets/gen-auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace ermöglicht Ihnen, Spureninformationen zu erhalten, die an Mbox-Antworten angehängt werden. Spureninformationen spiegeln das Ergebnis eines Mbox-Aufrufes (zum Beispiel eine Konversion oder eine Impression) sowie alle weiteren Daten wider, die dazu beitragen können zu ermitteln, warum es zu diesem Resultat gekommen ist, wie zum Beispiel eine Reihe verfügbarer Niederlassungen, zwischen denen während einer Kampagne eine Auswahl getroffen wurde. Verwenden Sie diese Informationen für eine Fehlerdiagnose der Inhaltsbereitstellung.

Die folgenden Parameter stehen zur Verfügung:

| mboxTrace-Optionen | Resultat |
|--- |--- |
| `?mboxTrace=console` | Wird im Konsolenprotokoll als Objekt ausgegeben.<br>Bei at.js müssen Sie, anstatt ein neues Browser-Fenster als Pop-up zu öffnen oder die Konsole wie bei mbox.js auszugeben, die Netzwerkanforderung untersuchen und unter „Vorschau“ (Chrome) oder „Antwort“ (Firefox) nachsehen. |
| `?mboxTrace=json` | Wird im Konsolenprotokoll als buchstäbliche JSON-Zeichenfolge ausgegeben |
| `?mboxTrace=window` | Wird im Pop-up-Fenster als JSON-Zeichenfolge ausgegeben |
| `?mboxTrace=disable` | Schaltet den Trace-Sitzungsmodus ab |

**Beispiel für mboxTrace-Aufruf**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

Die Ausgabe zeigt sehr detaillierte Informationen über Ihren Inhalt an. mboxTrace zeigt Details über Ihre Kampagne bzw. Aktivität und Ihr Profil an. Außerdem enthält es eine Momentaufnahme des Profils vor der Ausführung sowie eine Momentaufnahme mit den Änderungen nach der Ausführung. Es zeigt außerdem, welche Kampagnen oder Aktivitäten für jeden Ort ausgewertet wurden.

Ein Teil der Informationen umfasst übereinstimmende und nicht übereinstimmende Segment- und Ziel-IDs:

* **SegmentId**: IDs von Segmenten, entweder aus der Bibliothek mit den wiederverwendbaren Segmenten oder anonyme Segmente, die für die spezifische Kampagne erstellt wurden.
* **TargetId**: IDs von Zielen, entweder aus der Bibliothek mit den Zielausdrücken oder anonyme Ziele für beliebige Segmente aus der Kampagne.
* **Unmatched**: Die Anforderung in diesem Aufruf wurde für diese Segmente oder Ziele nicht zugelassen.
* **Matched**: Die Anforderung wurde für die angegebenen Segmente oder Ziele zugelassen.

**mboxTrace auf Empfehlungsseiten verwenden**: Wenn Sie mboxTrace als Abfrageparameter auf Seiten mit Empfehlungen hinzufügen, wird das Empfehlungsdesign auf der Seite durch ein mboxTrace-Detailfenster ersetzt. In diesem Fenster werden ausführliche Informationen zu Ihren Empfehlungen angezeigt, darunter:

* Zurückgegebene Empfehlungen im Vergleich zu abgefragten Empfehlungen
* Der verwendete Schlüssel und ob er Empfehlungen generiert
* Nach Kriterien erstellte Empfehlungen im Vergleich zu Backup-Empfehlungen
* Kriterienkonfiguration
* Angewendete Aus- und Einschlüsse
* Auflistungsregeln

Das Einschließen von `=console`, `=json` oder `=window` im Abfrageparameter ist nicht erforderlich. Wenn Sie mit den mboxTrace-Details fertig sind, fügen Sie `=disable` hinzu und drücken Sie die **[!UICONTROL Eingabetaste]**, um zum normalen Anzeigemodus zurückzukehren.

Die normale Funktionsweise und Erscheinung Ihrer Website wird durch mboxTrace nicht beeinträchtigt. Besucher sehen Ihr normales Empfehlungsdesign.

## mboxDebug {#section_DC92A0E4388A4A2787365AD9D556FEFA}

Ergänzen Sie zur Verwendung von mboxDebug Ihre URL um einen mboxDebug-Parameter. Die folgende Tabelle enthält Informationen zu Mbox-verwandten URL-Parametern.

>[!NOTE]
>
>Einige mboxDebug-Parameter stehen mit oder ohne Authentifizierung zur Verfügung.

| URL-Parameter | Zielsetzung |
|--- |--- |
| `mboxDebug=1` | Debugger<br>Wenn Sie diesen Parameter zu einer URL mit definierten Mboxes hinzufügen, wird ein Pop-up-Fenster mit hilfreichen Details zur Fehlerbehebung geöffnet. Cookie-Informationen, PCid und Sitzungs-ID-Werte werden ausgeschrieben und alle Mbox-URLs werden angegeben. Klicken Sie auf eine Mbox-URL, um die Antwort für diese Mbox einzublenden. Weitere Details finden Sie unter [mbox_debug.pdf](/help/assets/mbox_debug.pdf). |
| `mboxDebug=x-cookie` | Ändern der Cookies |
| `mboxDisable=1` | Deaktivieren von Mboxes auf der Seite |
| `mboxDebug=x-profile` | Anzeigen des Profilsets. |
| `mboxDebug=x-time` | Anzeigen der Reaktionszeiten für jede Mbox-Anforderung |
| `mboxOverride.browserIp=<Insert IP address>` | Geotargeting-Test<br>Mit diesem URL-Parameter wird das Geotargeting getestet. Geben Sie eine IP-Adresse als Wert für dieses Attribut ein. Daraufhin wertet das Test&amp;Target Geotargeting diese IP-Adresse anhand eines Geotargeting- oder Segmentierungssatzes in einer Kampagne aus. |

## Adobe Experience Cloud-Debugger {#section_A2798ED3A431409690A4BE08A1BFCF17}

Der Adobe Experience Cloud-Debugger ermöglicht die schnelle und einfache Problembehebung in Ihrer Target-Implementierung. Hier können Sie schnell Ihre Bibliothekskonfiguration anzeigen, Anfragen untersuchen, um sicherzustellen, dass Ihre benutzerspezifischen Parameter ordnungsgemäß übergeben werden, die Konsolenprotokollierung aktivieren sowie alle Target-Anfragen deaktivieren. Nach Authentifizierung bei der Experience Cloud können Sie das leistungsstarke Tool „Mbox Trace“ verwenden, um Ihre Aktivität und Ihre Zielgruppenqualifikationen sowie Ihr Besucherprofil zu untersuchen.

Weitere Informationen finden Sie in den Schulungsvideos unten:

Ausführliche Informationen finden Sie in der [*Dokumentation zur Adobe Experience Cloud-Debugger-Erweiterung*](https://marketing.adobe.com/resources/help/en_US/experience-cloud-debugger/).

## Wenn target.js bei der Bereitstellung nicht geladen wird {#section_ABBA5EFDFFB749D8BEE172DB1F973058}

Mbox.js sendet Besuchern ein Cookie namens „em-disabled“, falls target.js bei der Bereitstellung nicht geladen wird. Dieses Cookie verhindert, dass Angebote, die mit dem Visual Experience Composer erstellt wurden, auf der Site gerendert werden. Besucher mit diesem Cookie sehen weder den Testinhalt noch werden sie in diesen Aktivitätsberichten gezählt. Alle anderen Angebotsinhalte (zum Beispiel von Kampagnen in Target Classic) werden weiterhin geladen. Das Cookie hat eine Lebensdauer von 30 Minuten ab dem Zeitpunkt des Ladefehlers.

## Topverkäufe werden nicht in Recommendations angezeigt. {#section_3920C857270A406C80BE6CBAC8221ECD}

Die *`SIteCatalyst: purchase`*-Mbox kann nicht für Traffic-Daten des Einkaufsalgorithmus verwendet werden. Verwenden Sie stattdessen die *`orderConfirmPage`*-Mbox.

## Aktivitätspriorität prüfen {#section_3D0DD07240F0465BAF655D0804100AED}

Formularbasierte Aktivitäten, die mit [!DNL Target Standard/Premium] erstellt wurden, kollidieren möglicherweise mit Aktivitäten, die in der [!DNL Target Classic]-Oberfläche erstellt wurden und über die gleiche Priorität und Mbox verfügen.

## Benutzerdefinierter Code generiert keine erwartungsgemäßen Ergebnisse in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Target unterstützt IE 8 nicht mehr.

## Von der globalen Mbox bereitgestellte JavaScript-Inhalte werden nicht geladen, wenn mbox.js{#section_03EC9B9C410B4F52A7FCD81840311709} verwendet wird.

Führen Sie ein Upgrade auf die [!DNL mbox.js]-Version 58 oder neuer durch.

„mbox.js“, Version 58 oder neuer führt Nicht-JavaScript-Inhalte der globalen Mbox unmittelbar nach dem HTML-Tag `BODY` aus. JavaScript-Inhalte innerhalb des Tags `<script>` der globalen Mbox werden nach Auslösen von `DOMContentLoaded` ausgeführt. Diese Reihenfolge der Inhaltsbereitstellung gewährleistet, dass JavaScript-Inhalte der globalen Mbox ordnungsgemäß bereit- und dargestellt werden.

## Target-Cookie wird nicht gesetzt {#section_77AFEB541C0B495EB67E29A4475DF960}

Wenn Ihre Site eine Unterdomäne besitzt, z. B. [!DNL us.domain.com], das Target-Cookie aber auf [!DNL domain.com] gesetzt werden muss (anstatt auf [!DNL us.domain.com]), dann müssen Sie die Einstellung `cookieDomain` überschreiben. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Target-Inhalt flackert oder wird nicht angezeigt, wenn ein Element auch Teil einer AEM-Personalisierung ist. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

Wenn ein DOM-Element zum Adobe Experience Manager (AEM)-Personalisierungstargeting und zu einer Target-Aktivität gehört, flackert der Target-Inhalt möglicherweise, oder er wird nicht angezeigt.

Um dies zu beheben, können Sie die AEM-Personalisierung für Seiten deaktivieren, auf denen Target ausgeführt wird.

## Umleitungs- und Remote-Angebote können aufgrund einer ungültigen URL nicht bereitgestellt werden. {#section_7D09043B687F43B39DAEDF17D00375AC}

Wenn das Umleitungs- oder Remote-Angebot eine ungültige URL verwendet, kann es möglicherweise nicht bereitgestellt werden.

Bei Umleitungsangeboten kann die Mbox-Antwort `/* invalid redirect offer URL */` enthalten.

Oder

Bei Remote-Angeboten kann die Mbox-Antwort `/* invalid remote offer URL */` enthalten.

Sie können die Mbox-Antwort im Browser oder mithilfe von mboxTrace überprüfen. Weitere Informationen zu gültigen URLs finden Sie unter [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66).

## mboxes werden nicht auf meiner Site ausgelöst.

at. js löst Target-mboxes nicht aus, wenn Sie einen ungültigen Doctype verwenden. at.js erfordert den Doctype HTML 5.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Erweiterung hinzufügen

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/?captions=ger)

### Grundlegendes Target-Debugging

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/?captions=ger)

### Mbox Trace

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/?captions=ger)