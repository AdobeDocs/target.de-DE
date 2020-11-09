---
keywords: debug mbox;troubleshoot mbox;mbox issues;flicker;mboxDebug;mboxTrace;token;debugger;priority;activity priority;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst  purchase mbox;top selling;top seller
description: Wenn Ihre Seite nicht den erwarteten Inhalt anzeigt, können Sie einige Schritte zum Debugging von Content Versand in Adobe Target unternehmen.
title: Fehlerbehebung bei Content Versand in Adobe Target
feature: activities
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1386'
ht-degree: 58%

---


# Fehlerbehebung bei der Inhaltsbereitstellung{#troubleshoot-content-delivery}

Wenn Ihre Seite nicht den erwarteten Inhalt anzeigt, gibt es ein paar Schritte, die Sie unternehmen können, um eine Fehlerdiagnose für die Inhaltsbereitstellung vorzunehmen.

* Prüfen Sie den Code für Ihre Aktivität bzw. Kampagne sorgfältig. Ein Tippfehler oder ein anderweitiger Fehler könnte die Ursache dafür sein, dass der erwartete Inhalt nicht angezeigt wird.
* Use mboxTrace or mboxDebug to troubleshoot the [!DNL Target] request.
* Use the Adobe Experience Cloud Debugger, an easy-to-use tool that provides much of the same information as mboxDebug, to troubleshoot the [!DNL Target] request.

mboxDebug is especially useful when you are setting up [!DNL Target] on your page to make sure the [!DNL Target] request is firing and the cookie is being set. Jedoch ist mboxDebug nicht so detailliert, wie es für die Fehlerdiagnose bei der Inhaltsbereitstellung nützlich wäre. Wenn Ihre Aktivität nicht auf Ihrer Seite erscheint oder unerwünschter Inhalt eingeblendet wird, verwenden Sie mboxTrace, um die Seite ausführlich zu untersuchen und Fehler zu diagnostizieren.

## Retrieve the authorization token to use with debugging tools {#section_BED130298E794D1FA229DB7C3358BA54}

Da mboxTrace und mboxDebug Kampagnen- und Profildaten für Dritte enthüllen können, ist ein Autorisierungstoken erforderlich. Das Autorisierungstoken kann in der [!DNL Target]-Benutzeroberfläche abgerufen werden. Das Token ist sechs Stunden lang gültig.

Sie benötigen eine der folgenden Benutzerberechtigungen, um ein Authentifizierungstoken zu generieren:

* Mindestens [!UICONTROL Editor] -Berechtigung (oder [!UICONTROL Genehmiger])

   Weitere Informationen für [!DNL Target Standard] Kunden finden Sie unter [Festlegen von Rollen und Berechtigungen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Benutzern*. Weitere Informationen für [!DNL Target Premium] Kunden finden Sie unter [Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md)konfigurieren.

* Administratorrolle auf der Profil-/Arbeitsbereich-Ebene

   Arbeitsbereiche stehen nur [!DNL Target Premium] Kunden zur Verfügung. For more information, see [Configure enterprise permissions](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

* Administratorrechte (Berechtigung &quot;Sysadmin&quot;) auf der [!DNL Adobe Target] Produktebene

So wird das Autorisierungstoken abgerufen:

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. Klicken Sie im Abschnitt Debugger-Tools auf Neues Authentifizierungstoken **[!UICONTROL erstellen]**.

   ![Neues Authentifizierungstoken erstellen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

1. Fügen Sie das generierte Token Ihrer URL als Parameter hinzu, um eines der erweiterten Debuggingwerkzeuge zu aktivieren.

   ![Autorisierungstoken](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace enables you to receive trace information attached to [!DNL Target] responses. Trace information reflects the outcome of a [!DNL Target] call (for example, a conversion or an impression) and any additional data that may help in determining why this particular outcome happened, such as a set of available branches among which the selection was made in a campaign. Verwenden Sie diese Informationen für eine Fehlerdiagnose der Inhaltsbereitstellung.

Die folgenden Parameter stehen zur Verfügung:

| mboxTrace-Optionen | Resultat |
|--- |--- |
| `?mboxTrace=console` | Wird im Konsolenprotokoll als Objekt ausgegeben.<br>Bei at.js müssen Sie, anstatt ein neues Browser-Fenster als Pop-up zu öffnen oder die Konsole wie bei mbox.js auszugeben, die Netzwerkanforderung untersuchen und unter „Vorschau“ (Chrome) oder „Antwort“ (Firefox) nachsehen. |
| `?mboxTrace=json` | Wird im Konsolenprotokoll als buchstäbliche JSON-Zeichenfolge ausgegeben |
| `?mboxTrace=window` | Wird im Pop-up-Fenster als JSON-Zeichenfolge ausgegeben |
| `?mboxTrace=disable` | Schaltet den Trace-Sitzungsmodus ab |

**Beispiel für einen mboxTrace-Aufruf**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

Die Ausgabe zeigt sehr detaillierte Informationen über Ihren Inhalt an. mboxTrace zeigt Details über Ihre Kampagne bzw. Aktivität und Ihr Profil an. Außerdem enthält es eine Momentaufnahme des Profils vor der Ausführung sowie eine Momentaufnahme mit den Änderungen nach der Ausführung. Es zeigt außerdem, welche Kampagnen oder Aktivitäten für jeden Ort ausgewertet wurden.

Ein Teil der Informationen umfasst übereinstimmende und nicht übereinstimmende Segment- und Ziel-IDs:

* **SegmentId**: IDs von Segmenten, entweder aus der Bibliothek mit den wiederverwendbaren Segmenten oder anonyme Segmente, die für die spezifische Kampagne erstellt wurden.
* **TargetId**: IDs von Zielen, entweder aus der Bibliothek mit den Zielausdrücken oder anonyme Ziele für beliebige Segmente aus der Kampagne.
* **Unmatched**: Die Anforderung in diesem Aufruf wurde für diese Segmente oder Ziele nicht zugelassen.
* **Matched**: Die Anforderung wurde für die angegebenen Segmente oder Ziele zugelassen.

**Verwenden von mboxTrace auf Empfehlungsseiten**: Durch das Hinzufügen von mboxTrace als Abfrage-Parameter auf Seiten mit Empfehlungen wird das Recommendations-Design auf der Seite durch ein mboxTrace-Detailfenster ersetzt, das detaillierte Informationen zu Ihren Empfehlungen enthält, darunter:

* Zurückgegebene Empfehlungen im Vergleich zu abgefragten Empfehlungen
* Der verwendete Schlüssel und ob er Empfehlungen generiert
* Nach Kriterien erstellte Empfehlungen im Vergleich zu Backup-Empfehlungen
* Kriterienkonfiguration
* Angewendete Aus- und Einschlüsse
* Auflistungsregeln

Das Einschließen von  `=console`, `=json` oder `=window` im Abfrageparameter ist nicht erforderlich. Wenn Sie mit den mboxTrace-Details fertig sind, fügen Sie `=disable` hinzu und drücken Sie die **[!UICONTROL Eingabetaste]**, um zum normalen Anzeigemodus zurückzukehren.

Die normale Funktionsweise und Erscheinung Ihrer Website wird durch mboxTrace nicht beeinträchtigt. Besucher sehen Ihr normales Empfehlungsdesign.

## mboxDebug {#mboxdebug}

Ergänzen Sie zur Verwendung von mboxDebug Ihre URL um einen mboxDebug-Parameter. The following table contains information about [!DNL Target] response-related URL parameters.

>[!NOTE]
>
>Einige mboxDebug-Parameter stehen mit oder ohne Authentifizierung zur Verfügung.

| URL-Parameter | Zielsetzung |
|--- |--- |
| `mboxDebug=1` | <br>DebuggerDurch Hinzufügen dieses Parameters zu einer beliebigen URL mit definierten Zielgruppen-Anforderungen wird ein Popup-Fenster mit wertvollen Debugging-Details geöffnet. Cookie-Informationen, PCid- und Sitzungs-ID-Werte werden ausgeschrieben und alle URLs sind sichtbar. Click on a Target request URL to show the response for that [!DNL Target] request. Weitere Details finden Sie unter [mbox_debug.pdf](/help/assets/mbox_debug.pdf). |
| `mboxDebug=x-cookie` | Ändern der Cookies |
| `mboxDisable=1` | Deaktivieren von Mboxes auf der Seite |
| `mboxDebug=x-profile` | Anzeigen des Profilsets. |
| `mboxDebug=x-time` | Show response time for each [!DNL Target] request |
| `mboxOverride.browserIp=<Insert IP address>` | Geotargeting-Test<br>Mit diesem URL-Parameter wird das Geotargeting getestet. Geben Sie eine IP-Adresse als Wert für dieses Attribut ein. Daraufhin wertet das Test&amp;Target Geotargeting diese IP-Adresse anhand eines Geotargeting- oder Segmentierungssatzes in einer Kampagne aus. |

>[!NOTE]
>
>Stellen Sie sicher, dass das URL-Fragment nach den Zeichenfolgenparametern der Abfrage steht. Alles nach dem ersten `#` ist ein Fragmentbezeichner und führt dazu, dass Debugging-Parameter nicht korrekt funktionieren.

## Adobe Experience Cloud-Debugger  {#section_A2798ED3A431409690A4BE08A1BFCF17}

Der Adobe Experience Cloud-Debugger ermöglicht die schnelle und einfache Problembehebung in Ihrer Target-Implementierung. Hier können Sie schnell Ihre Bibliothekskonfiguration anzeigen, Anfragen untersuchen, um sicherzustellen, dass Ihre benutzerspezifischen Parameter ordnungsgemäß übergeben werden, die Konsolenprotokollierung aktivieren sowie alle Target-Anfragen deaktivieren. Authentifizieren Sie sich im Experience Cloud und verwenden Sie das leistungsstarke MboxTrace-Tool, um Ihre Aktivität- und Audience-Qualifikationen sowie Ihr Besucher-Profil zu überprüfen.

Weitere Informationen finden Sie in den Schulungsvideos unten:

Weitere Informationen finden Sie unter [Debuggen von at.js mit dem Adobe Experience Cloud-Debugger](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md).

## Wenn target.js bei der Bereitstellung nicht geladen wird {#section_ABBA5EFDFFB749D8BEE172DB1F973058}

Mbox.js sendet Besuchern ein Cookie namens „em-disabled“, falls target.js bei der Bereitstellung nicht geladen wird. Dieses Cookie verhindert, dass Angebote, die mit dem Visual Experience Composer erstellt wurden, auf der Site gerendert werden. Besucher mit diesem Cookie sehen weder den Testinhalt noch werden sie in diesen Aktivitätsberichten gezählt. Alle anderen Angebotsinhalte (zum Beispiel von Kampagnen in Target Classic) werden weiterhin geladen. Das Cookie hat eine Lebensdauer von 30 Minuten ab dem Zeitpunkt des Ladefehlers.

## Topverkäufe werden nicht in Recommendations angezeigt.  {#section_3920C857270A406C80BE6CBAC8221ECD}

The *`SiteCatalyst: purchase`* call can&#39;t be used for Purchase algorithm traffic data. Verwenden Sie stattdessen den *`orderConfirmPage`* Aufruf.

## Check activity priority {#section_3D0DD07240F0465BAF655D0804100AED}

Form-based activities created with [!DNL Target Standard/Premium] might collide with activities created in the [!DNL Target Classic] UI that have the same priority and use the same [!DNL Target] request.

## Benutzerdefinierter Code generiert keine erwartungsgemäßen Ergebnisse in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Target unterstützt IE 8 nicht mehr.

## JavaScript content delivered by the global [!DNL Target] request doesn&#39;t load when using mbox.js. {#section_03EC9B9C410B4F52A7FCD81840311709}

Führen Sie ein Upgrade auf die [!DNL mbox.js]-Version 58 oder neuer durch.

mbox.js version 58 and later executes non-JavaScript content for the global [!DNL Target] request immediately after the HTML `BODY` tag is present. JavaScript content inside `<script>` tags for the global [!DNL Target] request executes after the `DOMContentLoaded` event is fired. This order of content delivery ensures that JavaScript content for the global [!DNL Target] request is delivered and rendered properly.

## Target cookie does not get set {#section_77AFEB541C0B495EB67E29A4475DF960}

Wenn Ihre Site eine Unterdomäne besitzt, z. B. [!DNL us.domain.com], das Target-Cookie aber auf [!DNL domain.com] gesetzt werden muss (anstatt auf [!DNL us.domain.com]), dann müssen Sie die Einstellung `cookieDomain` überschreiben. Weitere Informationen finden Sie unter [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Target-Inhalt flackert oder wird nicht angezeigt, wenn ein Element auch Teil einer AEM-Personalisierung ist. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

Wenn ein DOM-Element zum Adobe Experience Manager (AEM)-Personalisierungstargeting und zu einer Target-Aktivität gehört, flackert der Target-Inhalt möglicherweise, oder er wird nicht angezeigt.

Um dies zu beheben, können Sie die AEM-Personalisierung für Seiten deaktivieren, auf denen Target ausgeführt wird.

## Umleitungs- und Remote-Angebote können aufgrund einer ungültigen URL nicht bereitgestellt werden.  {#section_7D09043B687F43B39DAEDF17D00375AC}

Wenn das Umleitungs- oder Remote-Angebot eine ungültige URL verwendet, kann es möglicherweise nicht bereitgestellt werden.

For redirect offers, the [!DNL Target] response can contain `/* invalid redirect offer URL */`

Oder

For remote offers, the [!DNL Target] response can contain `/* invalid remote offer URL */`

You can check the [!DNL Target] response in the browser or using mboxTrace. Weitere Informationen zu gültigen URLs finden Sie unter [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66).

## Anfragen zur Zielgruppe werden nicht auf meiner Site ausgelöst.

at.js löst keine Anfragen zur Zielgruppe aus, wenn Sie einen ungültigen doctype verwenden. at.js erfordert den Doctype HTML 5.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Erweiterung hinzufügen ![Tutorialzeichen](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/)

### Grundlegende Zielgruppe Debugging- ![Tutorialzeichen](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/)

### Mbox Trace- ![Tutorial-Abzeichen](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/)