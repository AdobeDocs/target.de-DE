---
keywords: Mbox debuggen; Fehlerbehebung für Mbox; Mbox-Probleme; Flackern; mboxDebug; mboxTrace; Token; Debugger; Priorität; Aktivitätspriorität; Adobe Experience Cloud Debugger; orderConfirmPage mbox; SiteCatalyst Mbox kaufen; bester Verkauf; bestverkauftes Produkt
description: Hier finden Sie Tipps zur Fehlerbehebung, wenn der Inhalt auf Ihrer Seite nicht wie erwartet angezeigt wird. Erfahren Sie, wie Sie Fehler bei der Inhaltsbereitstellung beheben.
title: Wie kann ich Fehler bei der Inhaltsbereitstellung beheben?
feature: Aktivitäten
exl-id: 887b7956-1d61-439a-8339-c150deb9a378
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 97%

---

# Fehlerbehebung bei der Inhaltsbereitstellung

Wenn Ihre Seite nicht den erwarteten Inhalt anzeigt, gibt es ein paar Schritte, die Sie unternehmen können, um eine Fehlerdiagnose für die Inhaltsbereitstellung vorzunehmen.

* Prüfen Sie den Code für Ihre Aktivität bzw. Kampagne sorgfältig. Ein Tippfehler oder ein anderweitiger Fehler könnte die Ursache dafür sein, dass der erwartete Inhalt nicht angezeigt wird.
* Verwenden Sie zur Fehlerbehebung bei [!DNL Target]-Anforderungen mboxTrace oder mboxDebug.
* Mit Adobe Experience Cloud Debugger erhalten Sie ein intuitives Tool, das für die Fehlerbehebung von [!DNL Target]-Anforderungen fast die gleichen Informationen wie mboxDebug bereitstellt.

mboxDebug ist insbesondere bei der Einrichtung von [!DNL Target] auf Ihrer Seite hilfreich. Es stellt sicher, dass die [!DNL Target]-Anforderung ausgelöst und das Cookie eingerichtet wird. Jedoch ist mboxDebug nicht so detailliert, wie es für die Fehlerdiagnose bei der Inhaltsbereitstellung nützlich wäre. Wenn Ihre Aktivität nicht auf Ihrer Seite erscheint oder unerwünschter Inhalt eingeblendet wird, verwenden Sie mboxTrace, um die Seite ausführlich zu untersuchen und Fehler zu diagnostizieren.

## Abrufen des Autorisierungstokens zur Verwendung mit Debuggingwerkzeugen {#section_BED130298E794D1FA229DB7C3358BA54}

Da mboxTrace und mboxDebug Kampagnen- und Profildaten für Dritte enthüllen können, ist ein Autorisierungstoken erforderlich. Das Autorisierungstoken kann in der [!DNL Target]-Benutzeroberfläche abgerufen werden. Das Token ist sechs Stunden lang gültig.

Für die Generierung eines Authentifizierungstokens benötigen Sie eine der folgenden Benutzerberechtigungen:

* Mindestens die Berechtigung [!UICONTROL Bearbeiter] (oder [!UICONTROL Genehmiger])

   Weitere Informationen für [!DNL Target Standard]-Kunden finden Sie unter [Festlegen von Rollen und Berechtigungen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) für *Benutzer*. Weitere Informationen für [!DNL Target Premium]-Kunden finden Sie unter [Konfigurieren von Enterprise-Berechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

* Administratorrolle auf der Ebene Arbeitsbereich/Produktprofil

   Arbeitsbereiche stehen nur [!DNL Target Premium]-Kunden zur Verfügung. Weitere Informationen finden Sie unter [Konfigurieren von Enterprise-Berechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

* Administratorrechte (Berechtigung „Sysadmin“) auf der [!DNL Adobe Target]-Produktebene

So wird das Autorisierungstoken abgerufen:

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. Klicken Sie im Abschnitt mit den Debuggingwerkzeugen auf **[!UICONTROL Neues Authentifizierungstoken erstellen]**.

   ![Neues Authentifizierungstoken erstellen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

1. Fügen Sie das generierte Token Ihrer URL als Parameter hinzu, um eines der erweiterten Debuggingwerkzeuge zu aktivieren.

   ![Autorisierungstoken](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

Mit mboxTrace können Sie an [!DNL Target]-Antworten angehängte Trace-Informationen abrufen. Trace-Informationen spiegeln das Ergebnis eines [!DNL Target]-Aufrufs (z. B. eine Konversion oder eine Impression) sowie alle weiteren Daten wider, die dazu beitragen festzustellen, weshalb es zu diesem Ergebnis gekommen ist, beispielsweise eine Reihe verfügbarer Niederlassungen, zwischen denen während einer Kampagne eine Auswahl getroffen wurde. Verwenden Sie diese Informationen für eine Fehlerdiagnose der Inhaltsbereitstellung.

Die folgenden Parameter stehen zur Verfügung:

| mboxTrace-Optionen | Resultat |
|--- |--- |
| `?mboxTrace=console` | Wird im Konsolenprotokoll als Objekt ausgegeben.<br>Bei at.js müssen Sie, anstatt wie in mbox.js ein neues Browser-Fenster zu öffnen oder in der Konsole auszugeben, die Netzwerkanforderung untersuchen und unter &quot;Vorschau&quot;(Chrome) oder &quot;Antwort&quot;(Firefox) nachsehen. |
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

**Verwenden von mboxTrace auf Seiten mit Empfehlungen**: Wenn Sie mboxTrace als Abfrageparameter auf Seiten mit Empfehlungen hinzufügen, wird das Recommendations-Design der Seite durch ein mboxTrace-Detailfenster ersetzt. In diesem Fenster werden ausführliche Informationen zu Ihren Empfehlungen angezeigt, darunter:

* Zurückgegebene Empfehlungen im Vergleich zu abgefragten Empfehlungen
* Der verwendete Schlüssel und ob er Empfehlungen generiert
* Nach Kriterien erstellte Empfehlungen im Vergleich zu Backup-Empfehlungen
* Kriterienkonfiguration
* Angewendete Aus- und Einschlüsse
* Auflistungsregeln

Das Einschließen von   `=console`, `=json` oder `=window` im Abfrageparameter ist nicht erforderlich. Wenn Sie mit den mboxTrace-Details fertig sind, fügen Sie `=disable` hinzu und drücken Sie die **[!UICONTROL Eingabetaste]**, um zum normalen Anzeigemodus zurückzukehren.

Die normale Funktionsweise und Erscheinung Ihrer Website wird durch mboxTrace nicht beeinträchtigt. Besucher sehen Ihr normales Recommendations-Design.

## mboxDebug {#mboxdebug}

Ergänzen Sie zur Verwendung von mboxDebug Ihre URL um einen mboxDebug-Parameter. Die folgende Tabelle enthält Informationen zu URL-Parametern von [!DNL Target] für Antworten.

>[!NOTE]
>
>Einige mboxDebug-Parameter stehen mit oder ohne Authentifizierung zur Verfügung.

| URL-Parameter | Zielsetzung |
|--- |--- |
| `mboxDebug=1` | Debugger<br>Wenn Sie diesen Parameter zu einer URL mit definierten Target-Anforderungen hinzufügen, wird ein Pop-up-Fenster mit hilfreichen Details zur Fehlerbehebung geöffnet. Cookie-Informationen, die PCid und Sitzungs-ID-Werte sind ausgeschrieben und alle URLs sind sichtbar. Klicken Sie auf eine Target-Anforderungs-URL, um die Antwort für diese [!DNL Target]-Anforderung einzublenden. Weitere Details finden Sie unter [mbox_debug.pdf](/help/assets/mbox_debug.pdf). |
| `mboxDebug=x-cookie` | Ändern der Cookies |
| `mboxDisable=1` | Deaktivieren von Mboxes auf der Seite |
| `mboxDebug=x-profile` | Anzeigen des Profilsets. |
| `mboxDebug=x-time` | Anzeigen der Reaktionszeiten von [!DNL Target]-Anforderungen |
| `mboxOverride.browserIp=<Insert IP address>` | Geotargeting-Test<br>Mit diesem URL-Parameter wird das Geotargeting getestet. Geben Sie eine IP-Adresse als Wert für dieses Attribut ein. Daraufhin wertet das Test&amp;Target Geotargeting diese IP-Adresse anhand eines Geotargeting- oder Segmentierungssatzes in einer Kampagne aus. |

>[!NOTE]
>
>Geben Sie das URL-Fragment nach den Zeichenfolgeparametern der Abfrage ein. Alles nach dem ersten `#` wird als Fragmentkennung interpretiert und würde dazu führen, dass die Debugging-Parameter nicht korrekt funktionieren.

## Adobe Experience Cloud-Debugger   {#section_A2798ED3A431409690A4BE08A1BFCF17}

Der Adobe Experience Cloud-Debugger ermöglicht die schnelle und einfache Problembehebung in Ihrer Target-Implementierung. Hier können Sie schnell Ihre Bibliothekskonfiguration anzeigen, Anfragen untersuchen, um sicherzustellen, dass Ihre benutzerspezifischen Parameter ordnungsgemäß übergeben werden, die Konsolenprotokollierung aktivieren sowie alle Target-Anfragen deaktivieren. Nach Ihrer Authentifizierung bei der Experience Cloud können Sie das leistungsstarke Tool „MboxTrace“ verwenden, um Ihre Aktivität und Ihre Zielgruppenqualifikationen sowie Ihr Besucherprofil zu untersuchen.

Weitere Informationen finden Sie in den Schulungsvideos unten:

Weitere Informationen finden Sie unter [Debugging von at.js mit dem Adobe Experience Cloud-Debugger](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md).

## Topverkäufe werden nicht in Recommendations angezeigt.   {#section_3920C857270A406C80BE6CBAC8221ECD}

Der *`SiteCatalyst: purchase`*-Aufruf kann nicht für Traffic-Daten des Einkaufsalgorithmus verwendet werden. Verwenden Sie stattdessen den Aufruf *`orderConfirmPage`*.

## Aktivitätspriorität prüfen {#section_3D0DD07240F0465BAF655D0804100AED}

Formularbasierte Aktivitäten, die mit [!DNL Target Standard/Premium] erstellt wurden, kollidieren möglicherweise mit Aktivitäten, die in der Benutzeroberfläche von [!DNL Target Classic] erstellt wurden und die gleiche [!DNL Target]-Anforderung verwenden.

## Benutzerdefinierter Code generiert keine erwartungsgemäßen Ergebnisse in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Target unterstützt IE 8 nicht mehr.

## Target-Cookie wird nicht gesetzt {#section_77AFEB541C0B495EB67E29A4475DF960}

Wenn Ihre Site eine Unterdomäne besitzt, z. B. [!DNL us.domain.com], das Target-Cookie aber auf [!DNL domain.com] gesetzt werden muss (anstatt auf [!DNL us.domain.com]), dann müssen Sie die Einstellung `cookieDomain` überschreiben. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Target-Inhalt flackert oder wird nicht angezeigt, wenn ein Element auch Teil einer AEM-Personalisierung ist. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

Wenn ein DOM-Element zum Adobe Experience Manager-(AEM)-Personalisierungstargeting und zu einer Target-Aktivität gehört, flackert der Target-Inhalt möglicherweise, oder er wird nicht angezeigt.

Um dies zu beheben, können Sie die AEM-Personalisierung für Seiten deaktivieren, auf denen Target ausgeführt wird.

## Umleitungs- und Remote-Angebote können aufgrund einer ungültigen URL nicht bereitgestellt werden.   {#section_7D09043B687F43B39DAEDF17D00375AC}

Wenn das Umleitungs- oder Remote-Angebot eine ungültige URL verwendet, kann es möglicherweise nicht bereitgestellt werden.

Bei Umleitungsangeboten kann die [!DNL Target]-Antwort `/* invalid redirect offer URL */` enthalten.

Oder

Bei Remote-Angeboten kann die [!DNL Target]-Antwort `/* invalid remote offer URL */` enthalten.

Sie können die [!DNL Target]-Antwort im Browser oder mit mboxTrace überprüfen. Weitere Informationen zu gültigen URLs finden Sie unter [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66).

## Target-Anforderungen werden auf meiner Site nicht ausgelöst.

at. js löst keine Target-Anforderungen aus, wenn Sie einen ungültigen Doctype verwenden. at.js erfordert den Doctype HTML 5.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Erweiterung hinzufügen   ![Tutorial-Badge](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/)

### Grundlegende Fehlerbehebung in Adobe Target ![Tutorial-Badge](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/)

### Mbox Trace ![Tutorial-Badge](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/)
