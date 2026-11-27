---
keywords: E-Mail; ESP; E-Mail-Serviceprovider; Rawbox; Bereitstellungs-API; ausschließliche Download-Vorlage; E-Mail-Vorlage; Batchverarbeitung; Build-Time-E-Mail
description: Erfahren Sie, wie Sie E-Mails mit Adobe [!DNL Target Recommendations] integrieren, einschließlich der Verwendung der [!DNL Target]-Bereitstellungs-API, Rawbox-Vorlagen und Nur-Download-Vorlagen.
title: Wie integriere ich Recommendations mit E-Mail?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
TQID: 'https://experienceleague.adobe.com/ZyeOl6ysM03a0mMiNgHuicOLPfgpXnrdqXJE1gHRRvE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1741'
ht-degree: 26%
---
# Integration von [!DNL Recommendations] mit E-Mails {#integrate-recs-email}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie mehr über die Methoden zur Integration von [!DNL Target Recommendations] mit einem E-Mail-Dienstanbieter (ESP) zur Sendezeit-Personalisierung von Recommendations in E-Mails.

>[!ENDSHADEBOX]

[!DNL Adobe Target] unterstützt die Sendezeit-Personalisierung von Recommendations in E-Mails. Die Open-Time-Personalisierung von Recommendations wird nicht unterstützt.

Es stehen drei Methoden zur Integration von [!DNL Target Recommendations] in ein ESP zur Verfügung. Die Fähigkeiten des ESP bestimmen, welche Methode zu verwenden ist, und der Account Manager oder Berater kann bei der Auswahl der besten Option helfen.

| Methode | Details |
| --- | --- |
| [Methode 1: [!DNL Adobe Target Delivery API]](#delivery-api) (Bevorzugt) | Verwenden Sie die [!DNL Adobe Target Delivery API], um pro Kunde und pro E-Mail Anfragen für Recommendations zu stellen. |
| [Methode 2: [!DNL Adobe Rawbox API]](#rawbox) | Verwenden Sie die [!DNL Adobe Target Rawbox API], um pro Kunde und pro E-Mail Anfragen für Recommendations zu stellen. |
| [Methode 3: [!DNL Recommendations Download API]](#download-api) | Verwenden Sie die [!DNL Recommendations Download API] , um Massenempfehlungen für eine Liste von Produkten oder Kategorien im CSV-Format anzufordern. |

Bei den Methoden 1 und 2 muss der ESP eine externe API pro Kunde und E-Mail aufrufen und auf die Rückgabe des Inhalts warten. Nicht alle ESPs unterstützen diese Methoden. Daher muss das ESP kontaktiert werden, um festzustellen, ob es mit diesem Integrationsmuster kompatibel ist.

Methode 3 erfordert, dass der ESP eine Liste von Recommendations nach Produkt-ID oder Kategorie-ID mit der Liste der E-Mails verknüpft. Dieser Join kann auf einem Attribut basieren, z. B. dem zuletzt angezeigten Produkt, dem zuletzt gekauften Produkt oder der am häufigsten angezeigten Kategorie des Kunden. Der ESP muss Zugriff auf diese Daten in seinem Kundenprofil haben, um die Verknüpfung durchführen zu können. Daher muss der ESP kontaktiert werden, um festzustellen, ob er Zugriff auf diese Daten hat und mit diesem Integrationsmuster kompatibel ist.

>[!IMPORTANT]
>
>Die folgenden Kapazitätsrichtlinien gelten für die Methoden der Bereitstellungs-API und der Rawbox-E-Mail-Vorlage (Methoden 1 und 2):
>
>* Anfragen sollten auf den niedrigeren Wert von 1.000 Anfragen pro Sekunde oder das 25-Fache des höchsten täglichen Traffics beschränkt sein.
>* Der Traffic sollte jede Minute in Schritten von 200 Anfragen pro Sekunde erhöht werden.
>
>Wenden Sie sich an den Account Manager, wenn Sie höhere Limits verwenden möchten.

## Methode 1: Verwenden der Bereitstellungs-API (Bevorzugt) {#delivery-api}

Die Bereitstellungs-API ist eine POST-Anfrage, die mit Build-Time-E-Mails funktioniert. Diese Option ist die bevorzugte Methode für die Erstellungszeit-E-Mail.

Die meisten E-Mail-Clients erlauben keine POST-Anfragen, daher wird diese API für Anwendungsfälle mit offenen Zeiten nicht empfohlen. Einige E-Mail-Clients wie Gmail oder Outlook speichern unter Umständen den Inhalt im Cache ab oder blockieren ein Bild und verlangen, dass der Empfänger dem Bild proaktiv das Rendern erlaubt.

Standardinhalt kann nicht mit der Bereitstellungs-API zurückgegeben werden.

Der folgende Code ist eine Beispiel-API-Bereitstellungsanfrage, wobei `clientcode` der [!DNL Target] Client-Code ist:

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

>[!NOTE]
>
>Geben Sie für jeden E-Mail-Empfänger (für jeden API-Aufruf) einen eindeutigen Wert für `sessionId` und entweder `tntId` oder `thirdPartyId` an. Ohne eindeutige Werte für diese Felder kann die API-Antwort aufgrund der vielen in einem einzigen Profil generierten Ereignisse verlangsamt werden oder fehlschlagen.

Weitere Informationen finden Sie in der [Dokumentation zur Bereitstellungs-API](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/overview.html?lang=de){target=_blank}.

## Option 2: Verwenden einer Rawbox-E-Mail-Vorlage {#rawbox}

Eine Rawbox ähnelt einer Mbox-Anfrage, die jedoch für Nicht-Web-Umgebungen wie E-Mail-Provider (ESPs) erstellt wird. [!DNL Adobe Experience Platform Web SDK] und [!DNL at.js] sind für Rawbox-Anfragen nicht verfügbar, daher müssen die Anfragen manuell erstellt werden. In den folgenden Beispielen wird erläutert, wie Rawbox-Anfragen in E-Mails verwendet werden.

Dieser Ansatz ermöglicht es, die Leistung von Empfehlungen in E-Mails zu verfolgen, sie auf die normale Weise mit einer Empfehlung zu testen und das Tracking auf der Website fortzusetzen.

>[!NOTE]
>
>Wenn Sie eine Rawbox mit [!DNL Target] verwenden, lesen Sie den wichtigen Sicherheitshinweis unter [Erstellen von Zulassungslisten mit Hosts, die autorisiert sind, Mbox-Aufrufe an [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist) zu senden.

1. Richten Sie in [!DNL Target] eine [!DNL Recommendations] Aktivität mit der Option [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) ein.

1. Wählen Sie als Speicherort den Namen der Mbox aus, die in der vom ESP kommenden Rawbox-Anfrage verwendet wird.

1. Wählen Sie ein Design mit dem gewünschten Look-and-Feel für die E-Mail.

Zum Zeitpunkt des E-Mail-Aufbaus generiert der ESP einen Aufruf an die [!DNL Target]-Server für jede Rawbox in jeder E-Mail-Nachricht, die erstellt wird. Der ESP muss über eine Möglichkeit verfügen, die zurückgegebene HTML zum Zeitpunkt des Versands in die E-Mail einzuschließen.

Das E-Mail-System muss mit den folgenden Szenarien umgehen können.

### Eingang einer gültigen Antwort ohne vorhandene Empfehlungen

* Die Antwort ist der Wert, der im `mboxDefault` festgelegt ist. Eine Beschreibung dieses Parameters finden Sie in der Tabelle der erforderlichen Parameter.
* Der E-Mail-Anbieter sollte in diesem Fall über einen Standard-HTML-Block für Empfehlungen verfügen.

### Zeitüberschreitung des [!DNL Target]-Servers und Rückgabe ohne Daten

* Der [!DNL Target] gibt den folgenden Inhalt zurück:

  `//ERROR: application server timeout`

* Das E-Mail-Programm sollte nach diesem Text suchen und muss mit diesem Fehler umgehen können. Der E-Mail-Anbieter verfügt für den Umgang mit diesem Szenario über mehrere Möglichkeiten:

  * Sofortiger Versuch eines erneuten Server-Aufrufs (empfohlen, möglicherweise mit Versuchszähler).
  * Verwerfen Sie diese E-Mail und fahren Sie mit der nächsten fort.
  * Diese E-Mail in die Warteschlange stellen und die fehlgeschlagenen E-Mails am Ende des ersten Durchgangs als Batch erneut ausführen.

### Beispiel für eine Anfrage-URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Erforderliche Parameter {#reqparams}

>[!NOTE]
>
>Um [!DNL Recommendations] in E-Mails zu verwenden, muss der Rawbox-Aufruf je nach Art der Empfehlungskriterien entweder die `entity.id` oder die `entity.categoryId` oder beide enthalten. Im obigen Beispielaufruf sind beide enthalten.

| Parameter | Wert | Beschreibung | Validierung |
|--- |--- |--- |--- |
| `client_code` | *client_code* | Der in [!DNL Recommendations] verwendete Clientcode. Der Adobe-Berater kann diesen Wert bereitstellen. |  |
| `mbox` | *mboxName* | Der Mbox-Name, der für das Targeting verwendet wird. | Gleiche Validierung wie für alle Mbox-Aufrufe.<br>250 Zeichen begrenzt.<br>Darf keines der folgenden Zeichen enthalten: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | disabled | Hindert die Antwort am Setzen eines Cookies in Nicht-Web-Umgebungen. |  |
| `entity.id`<br>(Erforderlich für bestimmte Kriterientypen: Ansicht/Ansicht, Ansicht/Gekauft, Gekauft/Gekauft) | *entity_id* | Die Produkt-ID, auf der die Empfehlung basiert, z. B. ein abgebrochenes Produkt im Warenkorb oder ein vorheriger Kauf.<br>Falls von den Kriterien gefordert, muss der Rawbox-Aufruf `entity.id` enthalten. |  |
| `entity.event.detailsOnly` | wahr | Wenn `entity.id` übergeben wird, wird dringend empfohlen, diesen Parameter zu übergeben, um zu verhindern, dass die Anfrage die Anzahl der zusammengeführten Seitenansichten für ein Element erhöht, um die produktansichtsbasierten Algorithmen nicht zu verfälschen. |  |
| `entity.categoryId`<br>(Für bestimmte Kriterientypen erforderlich: am häufigsten angezeigt nach Kategorie und Topverkäufe nach Kategorie) | *category_id* | Die Kategorie, auf der die Empfehlung basiert, z. B. Topverkäufe in einer Kategorie.<br>Falls von den Kriterien gefordert, muss der Rawbox-Aufruf `entity.categoryId` enthalten. |  |
| `mboxDefault` | *`https://www.default.com`* | Ist kein `mboxNoRedirect`-Parameter vorhanden, sollte `mboxDefault` eine absolute URL sein, die Standardinhalte zurückgibt, wenn keine Empfehlung zur Verfügung steht. Bei dieser URL kann es sich um Bilder oder statische Inhalte handeln.<br>Wenn der `mboxNoRedirect` vorhanden ist, kann `mboxDefault` jeder Text sein, der anzeigt, dass es keine Empfehlungen gibt, z. B. `no_content`.<br>Der E-Mail-Anbieter muss den Fall, dass dieser Wert zurückgegeben wird, handhaben und die Standard-HTML in die E-Mail einfügen.<br>Siehe Best Practice für die Sicherheit unter den Tabellen. |  |
| `mboxHost` | *mbox_host* | Die Domain, die der Standardumgebung (Host-Gruppe) hinzugefügt wird, wenn der Aufruf erfolgt. |  |
| `mboxPC` | Empty | (Erforderlich für Empfehlungen, die das Profil eines Besuchers verwenden.)<br>Wenn keine „thirdPartyId“ angegeben wurde, wird eine neue tntId generiert und als Teil der Antwort zurückgegeben. Andernfalls bleibt der Wert leer.<br>Siehe den Hinweis zu eindeutigen Werten unter den Tabellen. | 1 &lt; Länge &lt; 128<br>Darf nicht mehr als einen einzelnen „.“ (Punkt).<br>Der einzige zulässige Punkt ist für das Suffix für die Profilposition. |

### Optionale Parameter

| Parameter | Wert | Beschreibung | Validierung |
|--- |--- |--- |--- |
| `mboxPC`<br>(Optional) | *mboxPCId* | Die [!DNL Target] Besucher-ID. Verwenden Sie diesen Wert, um einen Benutzer über mehrere Besuche hinweg oder bei Verwendung eines Benutzerprofilparameters im Vollkreis zurück zur Website zu verfolgen.<br>Dieser Wert muss die tatsächliche [!DNL Adobe Target]-PCID des Benutzers sein, die von der Website in das CRM exportiert wird. Der E-Mail-Anbieter ruft diese ID aus dem CRM oder Data Warehouse ab und verwendet sie als Wert dieses Parameters.<br>Der `mboxPC` Wert ist auch für die Verfolgung des Site-Verhaltens von Besuchern über mehrere Besuche hinweg sinnvoll. Mit seiner Hilfe lassen sich Metriken verfolgen, wenn eine Empfehlung Teil einer A/B-Aktivität ist.<br>Siehe den Hinweis zu eindeutigen Werten unter den Tabellen. | 1 &lt; Länge &lt; 128<br>Darf nicht mehr als einen einzelnen „.“ (Punkt).<br>Der einzige zulässige Punkt ist für das Suffix für die Profilposition. |
| `mboxNoRedirect`<br>(Optional) | 1 | Standardmäßig wird der Anrufer umgeleitet, wenn keine bereitzustellenden Inhalte gefunden werden können. Verwenden Sie diesen Parameter, um das Standardverhalten zu deaktivieren. |  |
| `mbox3rdPartyId` | *xxx* | Verwenden Sie diese Option, um eine benutzerdefinierte Besucher-ID für Profil-Targeting anzugeben. |  |

Geben Sie für `mboxSession` und `mboxPC` einen eindeutigen Wert für jeden E-Mail-Empfänger an (für jeden API-Aufruf). Ohne eindeutige Werte für diese Felder kann die API-Antwort aufgrund der großen Anzahl der in einem einzelnen Profil generierten Ereignisse verlangsamt werden oder fehlschlagen.

Als Best Practice für die Sicherheit von `mboxDefault` sollten Sie autorisierte Hosts verwenden, um die Standard-Umleitungs-URL-Domains auf die Zulassungsliste setzen. Wenn die in der `mboxDefault`-URL verwendete Domain nicht auf die Zulassungsliste gesetzt ist, besteht die Gefahr einer Open Redirect-Schwachstelle. Autorisierte Hosts vermeiden die unbefugte Nutzung von Weiterleitungs-Links oder `mboxDefault` durch Dritte. [!DNL Target] verwendet Hosts, um die Domains auf die Zulassungsliste setzen, zu denen Umleitungen zulässig sind. Weitere Informationen finden Sie im Sicherheitshinweis am Anfang dieses Abschnitts.

### Mögliche Antworten des [!DNL Target]-Servers

| Antwort | Beschreibung |
|--- |--- |
| //ERROR: | Wird vom Lastenausgleich generiert, wenn er keinen Inhalt zurückgeben kann. |
| Erfolgreich abgeschlossen | Der `mboxNoRedirect` Parameter ist auf „true“ gesetzt und der Server gibt keine Empfehlungen zurück (es gibt keine Übereinstimmung für die Mbox oder der Server-Cache ist nicht initialisiert). |
| bad request | Der `mbox`-Parameter fehlt.<ul><li>Der `mboxDefault`- oder `mboxNoRedirect`-Parameter wird nicht angegeben.</li><li>Der `mboxTrace` Anfrageparameter ist angegeben, `mboxNoRedirect` jedoch nicht.</li><li>Der `mboxTarget` wird nicht angegeben, wenn mbox-Namen mit dem Suffix `-clicked` enden.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` wird nicht angegeben, wenn keine Übereinstimmung für die Anfrage vorhanden ist und der `mboxNoRedirect` nicht angegeben ist. |
| `Invalid mbox name:= MBOX_NAME` | Der `mbox` enthält ungültige Zeichen. |
| `Mbox name [MBOX_NAME] is too long` | Der `mbox` Parameter ist länger als 250 Zeichen. |

## Methode 3: Verwenden der Recommendations Download-API {#download-api}

Richten Sie die Empfehlung wie gehabt ein, wählen Sie jedoch statt einer Vorlagen-/Mbox-Kombination die Option **nur Download** im Präsentationsbereich. Geben Sie dann dem ESP die ID der erstellten Empfehlung an. Das ESP greift über die API auf die Empfehlungsdaten zu. Diese Daten zeigen, welche Artikel für eine bestimmte Kategorie oder ein Schlüsselelement, wie z. B. im Einkaufswagen liegen gebliebene Artikel, empfohlen werden sollen. Der ESP speichert diese Daten, verbindet sie mit seinem eigenen Erscheinungsbild, zeigt Informationen zu jedem Element an und stellt sie in den E-Mails bereit.

Mit dieser Option kann der Recommendations-Server die Leistung einer Recommendation nicht direkt verfolgen oder den Traffic auf mehrere Algorithmus- und Vorlagenkombinationen aufteilen. Außerdem sind Empfehlungen nicht an ein bestimmtes Besucherprofil gebunden.

Weitere Informationen zur Download-API finden Sie unter [Vorgänger-APIs > Download](/help/main/assets/adobe-recommendations-classic.pdf).
