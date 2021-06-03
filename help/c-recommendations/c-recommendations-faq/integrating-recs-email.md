---
keywords: E-Mail; ESP; E-Mail-Serviceprovider; Rawbox; Bereitstellungs-API; ausschließliche Download-Vorlage; E-Mail-Vorlage; Batchverarbeitung; Build-Time-E-Mail
description: Erfahren Sie, wie Sie E-Mails mit der Adobe [!DNL Target Recommendations], including using the [!DNL Target] -Bereitstellungs-API, Rawbox-Vorlagen und Nur-Download-Vorlagen integrieren.
title: Wie integriere ich E-Mail mit Recommendations?
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
translation-type: ht
source-git-commit: f29701f5357e86b694acdf3a48fa7eace8d382cb
workflow-type: ht
source-wordcount: '1524'
ht-degree: 100%

---

# ![PREMIUM](/help/assets/premium.png) Recommendations mit E-Mails integrieren 

Informationen zu den Methoden zum Integrieren der E-Mail-Funktion in [!UICONTROL Recommendations].

Die Möglichkeiten Ihres E-Mail-Service-Anbieters bestimmen die Methode. Ihr Kundenbetreuer oder Berater kann Ihnen bei der Wahl der am besten geeigneten Option behilflich sein.

>[!IMPORTANT]
>
>Die folgenden Kapazitätsrichtlinien gelten für die unten beschriebenen Optionen für die Bereitstellungs-API und die Rawbox-E-Mail-Vorlage (Optionen 1 und 2):
>
>* Anfragen sollten auf den niedrigeren Wert von entweder 1.000 Anfragen pro Sekunde oder das 25-Fache des höchsten Traffics pro Tag beschränkt sein.
>* Erhöhen Sie den Traffic jede Minute in Schritten von 200 Anfragen pro Sekunde.
> 
>Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie höhere Limits verwenden möchten.

## Option 1: Verwenden der Bereitstellungs-API {#section_9F00D271BABA4B7390B461F4C44EC319}

Die Bereitstellungs-API ist eine POST-Anforderung, die zusammen mit der Erstellungszeit-E-Mail verwendet wird. Diese Option ist die bevorzugte Methode für die Erstellungszeit-E-Mail.

Die meisten E-Mail-Clients erlauben keine POST-Anfragen. Aus diesem Grund ist diese API nicht für Anwendungsfälle zu empfehlen, bei denen die Zeit offen ist. Einige E-Mail-Clients wie Gmail oder Outlook speichern unter Umständen den Inhalt im Cache ab oder blockieren ein Bild, sodass der Empfänger die Darstellung eines Bildes proaktiv zulassen muss.

Mithilfe der Bereitstellungs-API können Sie keinen Standardinhalt zurückgeben.

Der folgende Code ist ein Beispiel für eine API-Bereitstellungsanfrage:

```javascript
curl -X POST \ 
  'https://clientcode.tt.omtrdc.net/rest/v1/mbox/?client=clientcode' \ 
  -H 'authorization: Bearer 3423614b-4843-4664-83c4-c6c3f6c8869b' \ 
  -H 'cache-control: no-cache' \ 
  -H 'content-type: application/json' \ 
  -d '{ 
  "mbox" : "email-mbox", 
  "tntId" : "111499796294071-449025.28_44", 
  "requestLocation" : { 
    "host" : "prod" 
  }, 
   "profileParameters" : { 
   }, 
  "mboxParameters" : { 
    "at_property": "b468a242-64a4-32a0-ca0c-890bddd78789", 
    "entity.id": "article-123", 
    "entity.event.detailsOnly" : "true" 
  } 
  "contentAsJson":  true 
}'
```

Dabei ist `clientcode` Ihr [!DNL Target]-Client-Code.

>[!NOTE]
>
>Stellen Sie sicher, dass Sie einen eindeutigen Wert für `sessionId` und entweder `tntId` oder `thirdPartyId` für jeden E-Mail-Empfänger bereitstellen (z. B. für jeden API-Aufruf). Wenn Sie keine eindeutigen Werte für diese Felder angeben, kann die API-Antwort aufgrund der zahlreichen in einem einzigen Profil generierten Ereignisse lange dauern oder sogar fehlschlagen.

Weitere Informationen finden Sie in der [Dokumentation zur Bereitstellungs-API](https://developers.adobetarget.com/api/#server-side-delivery).

## Option 2: Verwenden einer Rawbox-E-Mail-Vorlage {#section_C0D48A42BCCE45D6A68852F722C7C352}

Eine Rawbox ähnelt einer Mbox-Anfrage, die für Nicht-Web-Umgebungen wie E-Mail-Dienstanbieter (ESP) erstellt wurde. Da Sie bei Rawbox-Anfragen nicht mit [!DNL mbox.js] oder [!DNL at.js] arbeiten, müssen die Anfragen manuell erstellt werden. In den unten stehenden Beispielen ist beschrieben, wie Rawbox-Anfragen in E-Mails verwendet werden.

>[!NOTE]
>
>Wenn Sie eine Rawbox mit [!DNL Target] verwenden, lesen Sie den wichtigen Sicherheitshinweis unter [Erstellen von Zulassungslisten mit Hosts, die autorisiert sind, Mbox-Aufrufe an  [!DNL Target]](/help/administrating-target/hosts.md#allowlist) zu senden.

Dieser Ansatz ermöglicht es Ihnen, die Leistung von Recommendations in E-Mails zu verfolgen, die E-Mails unter normalen Bedingungen mit einer Empfehlung zu testen und die Verfolgung auf der Site fortzusetzen.

Richten Sie eine [!DNL Recommendations]-Aktivität in [!DNL Target] mit der Option [Formularbasierter Erlebniseditor](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) ein. Wählen Sie als Speicherort den Namen der Mbox aus, die Sie für die Rawbox-Anfrage des ESP gewählt haben. Wählen Sie das passende Design für Ihre E-Mail aus. Zum Zeitpunkt des E-Mail-Aufbaus generiert der ESP einen Aufruf an die [!DNL Target]-Server für jede Rawbox in jeder E-Mail-Nachricht, die erstellt wird. Ihr ESP muss über eine Möglichkeit verfügen, den zurückgegebenen HTML-Code beim Senden in die E-Mail einzuschließen.

Das von Ihnen verwendete E-Mail-System muss in der Lage sein, mit Folgendem umzugehen:

### Eingang einer gültigen Antwort ohne vorhandene Empfehlungen

* In diesem Fall ist die Antwort der Parameterwert von `mboxDefault`. Eine Erläuterung dieses Parameters finden Sie unten.
* Der E-Mail-Anbieter sollte in diesem Fall über einen Standard-HTML-Block für Empfehlungen verfügen.

### Zeitüberschreitung des [!DNL Target]-Servers und Rückgabe ohne Daten

* In diesem Fall gibt der [!DNL Target]-Server folgenden Inhalt zurück:

   `//ERROR: application server timeout`

* Die E-Mail-Anwendung sollte nach diesem Text suchen und dazu in der Lage sein, mit diesem Fehler umzugehen. Der E-Mail-Anbieter verfügt für den Umgang mit diesem Szenario über mehrere Möglichkeiten:

   * Sofortiger Versuch eines erneuten Server-Aufrufs (empfohlen, möglicherweise mit Versuchszähler).
   * Ignorieren der betroffenen E-Mail und Fortfahren mit der nächsten Nachricht.
   * Einreihen der betroffenen E-Mail in eine Warteschlange und erneute Batch-Verarbeitung der fehlgeschlagenen Nachrichten am Ende des ersten Durchlaufs.

### Beispiel für Anfrage-URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Erforderliche Parameter: {#reqparams}

>[!NOTE]
>
>Um [!DNL Recommendations] in E-Mails zu verwenden, muss der Rawbox-Aufruf je nach Art der Empfehlungskriterien entweder `entity.id` oder `entity.categoryId` oder beide enthalten. Im obigen Beispielaufruf sind beide enthalten.

| Parameter | Wert | Beschreibung | Validierung |
|--- |--- |--- |--- |
| `client_code` | *client_code* | Der in Recommendations verwendete Clientcode. Ihr Adobe-Berater kann Ihnen diesen Wert nennen. |  |
| `mbox` | *mboxName* | Der Mbox-Name, der für das Targeting verwendet wird. | Gleiche Validierung wie alle Mbox-Aufrufe.<br>Längenbeschränkung von 250 Zeichen.<br>Darf keines der folgenden Zeichen enthalten: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | disabled | Hindert die Antwort am Setzen eines Cookies in Nicht-Web-Umgebungen. |  |
| `entity.id`<br>(Erforderlich für bestimmte Kriterientypen: Ansicht/Ansicht, Ansicht/Gekauft, Gekauft/Gekauft) | *entity_id* | Die „productId“, auf der die Empfehlung beruht, beispielsweise ein in den Einkaufskorb gelegtes, aber nicht erworbenes Produkt oder ein in der Vergangenheit getätigter Einkauf.<br>Falls von den Kriterien gefordert, muss der Rawbox-Aufruf `entity.id` enthalten. |  |
| `entity.event.detailsOnly` | wahr | Wenn Sie weitergereicht werden, `entity.id` wird dringend empfohlen, diesen Parameter zu übergeben, um zu verhindern, dass die Anforderung die Anzahl der Seitenansichten für ein Element erhöht, sodass produktansichtsbasierte Algorithmen nicht verfälscht werden. |  |
| `entity.categoryId`<br>(Für bestimmte Kriterientypen erforderlich: am häufigsten angezeigt nach Kategorie und Topverkäufe nach Kategorie) | *category_id* | Die Kategorie, auf der die Empfehlung basiert, beispielsweise die Topverkäufe einer Kategorie.<br>Falls von den Kriterien gefordert, muss der Rawbox-Aufruf `entity.categoryId` enthalten. |  |
| `mboxDefault` | *`https://www.default.com`* | Ist kein `mboxNoRedirect`-Parameter vorhanden, sollte `mboxDefault` eine absolute URL sein, die Standardinhalte zurückgibt, wenn keine Empfehlung zur Verfügung steht. Bei dieser URL kann es sich um Bilder oder statische Inhalte handeln.<br>Wenn der `mboxNoRedirect`-Parameter vorhanden ist, kann es sich bei `mboxDefault` um einen beliebigen Text handeln, der angibt, dass es keine Empfehlungen gibt wie z. B. `no_content`.<br>Der E-Mail-Anbieter muss Situationen handhaben, bei denen dieser Wert zurückgegeben wird, und bei deren Eintreten Standard-HTML-Inhalte in die E-Mail einfügen. <br> **Best Practice für die Sicherheit**: Wenn die in der `mboxDefault`-URL verwendete Domain nicht in der Zulassungsliste enthalten ist, bieten Sie eine Angriffsfläche für Open Redirects. Zur Vermeidung einer unbefugten Nutzung von Weiterleitungs-Links oder `mboxDefault` durch Dritte empfiehlt Adobe die Verwendung von „autorisierten Hosts“, wodurch die Domains der Standard-Weiterleitungs-URL auf die Zulassungsliste gesetzt werden. Target verwendet Hosts, um Domains auf die Zulassungsliste zu setzen, für die Umleitungen erlaubt sind. Weitere Informationen finden Sie im Abschnitt *Hosts* unter [Erstellen von Zulassungslisten mit Hosts, die autorisiert sind, Mbox-Aufrufe an  [!DNL Target]](/help/administrating-target/hosts.md#allowlist) zu senden. |  |
| `mboxHost` | *mbox_host* | Die Domäne, die der Standardumgebung (Hostgruppe) hinzugefügt wird, wenn der Aufruf erfolgt. |  |
| `mboxPC` | Empty | (Für Empfehlungen erforderlich, die das Profil eines Besuchers verwenden.)<br>Wenn keine „thirdPartyId“ angegeben wurde, wird eine neue „tntId“ generiert und als Teil der Antwort zurückgegeben. Ansonsten wird kein Wert angegeben.<br>**Hinweis**: Stellen Sie sicher, dass Sie einen eindeutigen Wert für `mboxSession` und `mboxPC` für jeden einzelnen E-Mail-Empfänger angeben (d. h. für jeden API-Aufruf). Wenn Sie keine eindeutigen Werte für diese Felder angeben, kann die API-Antwort aufgrund der zahlreichen in einem einzigen Profil generierten Ereignisse lange dauern oder sogar fehlschlagen. | 1 &lt; Länge &lt; 128<br>Darf nicht mehr als einen einzelnen „.“ (Punkt) enthalten.<br>Der einzig zulässige Punkt ist derjenige vor dem Suffix für den Profilspeicherort. |

### Optionale Parameter

| Parameter | Wert | Beschreibung | Validierung |
|--- |--- |--- |--- |
| `mboxPC`<br>(Optional) | *mboxPCId* | Target-Besucher-ID. Verwenden Sie diesen Wert, wenn Sie einen Besucher umfassend über mehrere Besuche hinweg auf Ihre Seite zurück verfolgen möchten oder wenn ein Benutzerprofilparameter eingesetzt wird.<br>Dieser Wert muss die [!DNL Adobe Target]-PCID des Benutzers sein, die von der Website in Ihr CRM-System importiert wird. Der E-Mail-Anbieter würde diese ID aus Ihrem CRM-System oder Data Warehouse abrufen und als Wert für diesen Parameter einsetzen.<br>Der Wert `mboxPC` ist auch für die Verfolgung des Site-Verhaltens von Besuchern über mehrere Besuche hinweg sinnvoll. Mit seiner Hilfe lassen sich Metriken verfolgen, wenn eine Empfehlung Teil einer A/B-Aktivität ist.<br>**Hinweis**: Stellen Sie sicher, dass Sie einen eindeutigen Wert für `mboxSession` und `mboxPC` für jeden einzelnen E-Mail-Empfänger angeben (d. h. für jeden API-Aufruf). Wenn Sie keine eindeutigen Werte für diese Felder angeben, kann die API-Antwort aufgrund der zahlreichen in einem einzigen Profil generierten Ereignisse lange dauern oder sogar fehlschlagen. | 1 &lt; Länge &lt; 128<br>Darf nicht mehr als einen einzelnen „.“ (Punkt) enthalten.<br>Der einzig zulässige Punkt ist derjenige vor dem Suffix für den Profilspeicherort. |
| `mboxNoRedirect`<br>(Optional) | 1 | Standardmäßig wird der Anrufer umgeleitet, wenn keine bereitzustellenden Inhalte gefunden werden können. Für die Deaktivierung des Standardverhaltens verwenden. |  |
| `mbox3rdPartyId` | *xxx* | Verwenden Sie diese Option, wenn Sie für Profil-Targeting eigene, benutzerdefinierte IDs einsetzen. |  |

### Mögliche Antworten des [!DNL Target]-Servers

| Antwort | Beschreibung |
|--- |--- |
| //ERROR: | Von einem Lastverteiler generiert, wenn kein Inhalt zurückgegeben werden kann. |
| Erfolg | Der Parameter `mboxNoRedirect` ist als „true“ (wahr) festgelegt und der Server gibt keine Empfehlungen zurück (d. h., es ist keine Übereinstimmung für die Mbox vorhanden oder der Zwischenspeicher des Servers wurde nicht initialisiert). |
| bad request | Der `mbox`-Parameter fehlt.<ul><li>Der `mboxDefault`- oder `mboxNoRedirect`-Parameter wird nicht angegeben.</li><li>Anforderungsparameter `mboxTrace` ist angegeben, aber `mboxNoRedirect` nicht.</li><li>Parameter `mboxTarget` wird nicht angegeben, wenn mbox-Namen mit dem Suffix `-clicked` enden.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` wurde nicht angegeben, wenn für die Anfrage keine Übereinstimmung gefunden wurde oder der Parameter `mboxNoRedirect` nicht angegeben ist. |
| `Invalid mbox name:= MBOX_NAME` | Zeigt an, dass im Parameter `mbox` unzulässige Zeichen enthalten sind. |
| `Mbox name [MBOX_NAME] is too long` | Zeigt an, dass der Parameter `mbox` mehr als 250 Zeichen enthält. |

## Option 3: Verwenden der Nur-Download-Vorlage {#section_518C279AF0094BE780F4EA40A832A164}

Richten Sie die Empfehlung wie gehabt ein, wählen Sie jedoch statt einer Vorlagen-/Mbox-Kombination die Option **nur Download** im Präsentationsbereich. Teilen Sie dem ESP dann mit, welche Empfehlungs-ID Sie erstellt haben. Der ESP greift über API auf die Empfehlungsdaten zu. Diese Daten zeigen, welche Artikel für eine bestimmte Kategorie oder ein Schlüsselelement, wie z. B. im Einkaufswagen liegen gebliebene Artikel, empfohlen werden sollen. Der ESP speichert diese Daten, verbindet sie mit der eigenen Designvorgabe, zeigt Informationen zu den einzelnen Artikeln an und liefert die E-Mails aus.

Bei dieser Option kann der Recommendations-Server die Performance einer Empfehlung weder direkt verfolgen noch den Traffic über mehrere Algorithmus/Vorlagen-Kombinationen verteilen. Außerdem sind Empfehlungen nicht an ein bestimmtes Besucherprofil gebunden.

Weitere Informationen zur Download-API finden Sie unter [Vorgänger-APIs > Download](/help/assets/adobe-recommendations-classic.pdf).
