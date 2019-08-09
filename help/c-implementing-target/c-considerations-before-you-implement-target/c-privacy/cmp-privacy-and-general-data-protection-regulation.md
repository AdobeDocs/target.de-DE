---
description: Informationen über die allgemeine Datenschutzregel (GDPR) der Europäischen Union, den California Privacy Act (CCPA) von Kalifornien sowie andere internationale Datenschutzanforderungen und wie sich diese Regeln auf Ihre Organisation und Adobe Target auswirken.
keywords: gdpr; eu; european union; Datenschutz; faq; häufig gestellte Fragen; california consumer privacy act; ccpa; Datenschutz; Datenschutz; opt-out; opt-out; Behörden; Regel
seo-description: Informationen über die allgemeine Datenschutzregel (GDPR) der Europäischen Union, den California Privacy Act (CCPA) von Kalifornien sowie andere internationale Datenschutzanforderungen und wie sich diese Regeln auf Ihre Organisation und Adobe Target auswirken.
seo-title: Informationen über die allgemeine Datenschutzregel (GDPR) der Europäischen Union, den California Privacy Act (CCPA) von Kalifornien sowie andere internationale Datenschutzanforderungen und wie sich diese Regeln auf Ihre Organisation und Adobe Target auswirken.
solution: Target
title: Datenschutz und Datenschutz
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
translation-type: tm+mt
source-git-commit: ec69199fe85c9d8f2abb4826195ff894bd80af4a

---


# Datenschutz und Datenschutz {#privacy-and-general-data-protection-regulation-gdpr}

Informationen über die allgemeine Datenschutzregel (GDPR) der Europäischen Union, den California Privacy Act (CCPA) von Kalifornien sowie andere internationale Datenschutzanforderungen und wie sich diese Regeln auf Ihre Organisation und Adobe Target auswirken.

## Privacy and General Data Protection Regulation (GDPR) overview {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Am 25. Mai 2018 wurde das GDPR der europäischen Union in Kraft getreten. Weitere Informationen darüber, was dies für Sie bedeutet, finden Sie unter [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

When [!DNL Adobe] is providing software and services to an enterprise, [!DNL Adobe] is acting as a Data Processor for any personal data it processes and stores as part of providing these services. [!DNL Adobe] Verarbeitet als Datenprozessor persönliche Daten in Übereinstimmung mit der Berechtigung und den Anweisungen Ihres Unternehmens (z. [!DNL Adobe]B. laut Vereinbarung).

As the Data Controller, you determine the personal data that [!DNL Adobe] processes and stores on your behalf. If you use [!DNL Adobe Experience Cloud] solutions, [!DNL Adobe] might host personal data for you, depending on the solutions you use and the information you choose to send to your [!DNL Adobe Experience Cloud] account. Eine detaillierte Liste mit Beispielen finden Sie unter [Adobe Experience Cloud-Datenschutz](https://www.adobe.com/privacy/marketing-cloud.html#collect).

[!DNL Adobe Experience Cloud] Bereitstellen von GDPR-fertigen apis für Datencontroller, mit denen sie die folgenden Aufgaben ausführen können:

* Auf die in gespeicherten Daten der betroffenen Person zugreifen[!DNL Target]
* Die in gespeicherten Daten der betroffenen Person löschen[!DNL Target]

Weitere Informationen finden Sie unter:

* [Website der Adobe-DSGVO-API](https://www.adobe.io/apis/cloudplatform/gdpr.html)
* [DSGVO-Dokumentation](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## Übersicht über den California Privacy Act (CCPA)

Der California Privacy Act (CCPA) von Kalifornien bietet Kalifornien neue Rechte bezüglich ihrer persönlichen Informationen und stellt für bestimmte Unternehmen, die in Kalifornien Geschäfte durchführen, Datenschutz vor. Auf einer hohen Ebene stellt das Gesetz Phennians verschiedene wichtige Rechte bereit, einschließlich Berechtigungen für:

* Anforderungsinformationen (Datenzugriff)
* Ausschluss von dem Verkauf persönlicher Informationen (sehr weit gefasst, um die Freigabe von Informationen mit Dritten auszuschließen)
* Persönliche Informationen gelöscht
* Werden Sie informiert, dass persönliche Informationen bekannt gemacht oder verkauft werden

Wenn Sie im vergangenen Jahr beschäftigt waren, um sich für das Datenschutzrecht (GDPR) Europas zu entscheiden, können einige dieser Rechte bekannt sein und viele der Aufgaben, die Sie durchgeführt haben, können möglicherweise reproduziert werden.

## Adobe Target und [!DNL Experience Platform Launch] Teilnahme {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] bietet Unterstützung für die Teilnahme an Funktionen, über [!DNL Launch] die Ihre Strategie zur Genehmigungsbestätigung unterstützt wird. Opt-in functionality lets customers control how and when the [!DNL Target] tag is fired. There is also an option via [!DNL Launch] to pre-approve the [!DNL Target] tag. To enable the ability to use Opt-In in the [!DNL Target] at.js library, you should use `targetGlobalSettings` and add the `optinEnabled=true` setting. In [!DNL Launch] you'll need to select "enable" from the [!UICONTROL GDPR Opt-In] drop-down list in the [!DNL Launch] extension installation view. Weitere Details finden Sie in der [Dokumentation zu Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md).

Im folgenden Code-Snippet wird gezeigt, wie Sie die `optinEnabled=true`-Einstellung aktivieren:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>Die Teilnahme an der Teilnahme wird in at. js Version 1.7.0 und at. js 2.1.0 oder höher unterstützt. Die Anmeldung wird in at. js Version 2.0.0 und 2.0.1 nicht unterstützt.
>
>Using [!DNL Experience Platform Launch] to manage opt-in is the recommended approach. Further granular control exists in [!DNL Launch] to hide selected elements of your page prior to [!DNL Target] firing that are helpful to leverage as part of your consent strategy.

Es gibt drei Szenarien, in denen Sie die Verwendung des Opt-ins in Betracht ziehen sollten:

1. **Das[!DNL Target]Tag wird bereits genehmigt ([!DNL Launch]oder der zuvor genehmigte[!DNL Target]Datenbetreff):** Das [!DNL Target] Tag wird nicht zur Zustimmung und Funktionen wie erwartet gehalten.
1. **Das[!DNL Target]Tag ist NICHT VORAB GENEHMIGT und`bodyHidingEnabled`lautet FALSE:** Das [!DNL Target] Tag wird erst ausgelöst, nachdem die Zustimmung vom Kunden erfasst wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. After consent is received, [!DNL Target] is called and personalized content is available to the data subject (visitor). Da vor der Einwilligung nur der Standardinhalt verfügbar ist, ist die richtige Strategie entscheidend, wie z. B. eine Splash-Seite, die Seitenteile mit personalisierten Inhalten überdeckt. So wird gewährleistet, dass das Erlebnis für die betroffene Person (Besucher) einheitlich bleibt.
1. **Das[!DNL Target]Tag wird NICHT VORAB GENEHMIGT und`bodyHidingEnabled`ist TRUE:** Das [!DNL Target] Tag wird erst ausgelöst, nachdem die Zustimmung vom Kunden erfasst wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. However, because `bodyHidingEnabled` is set to true, `bodyHiddenStyle` dictates what content on the page is hidden until the [!DNL Target] tag is fired (or the data subject declines opt-in, in which case default content is displayed). `bodyHiddenStyle` ist standardmäßig als `body { opacity:0;`} festgelegt, was das HTML-Body-Tag ausblendet. Die empfohlene Seitenkonfiguration finden Sie unten. So können Sie den gesamten Body der Seite – abgesehen von der Einwilligungsdialog – ausblenden, indem Sie den Seiteninhalt in einen und den Einwilligungsdialog in einen anderen Container einfügen. This setup configures [!DNL Target] so that it hides the page content container only. Weitere Informationen zur Konfiguration dieser Einstellungen finden Sie in der [ Launch-Dokumentation](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html).

   Die empfohlene Seitenkonfiguration für Szenario 3 lautet wie folgt:

   ```
   <html> 
   <head> 
   //visitor, at.js 
   </head> 
   
   <body> 
   <div id = "consentManagerDialog"> 
   
   //consent manager html dialog goes here 
   </div> 
   
   <div id="pageContent"> 
   // page content goes here 
   </div> 
   
   </body> 
   </html> 
   ```

   Davon ausgehend, dass `bodyHiddenStyle` folgenden Wert aufweist:

   ```
   #pageContent { opacity:0;}
   ```

## Häufig gestellte Fragen zu Datenschutz und Datenschutz {#concept_41F88DE95D2943178BEC382736B5C038}

Häufig gestellte Fragen zur allgemeinen Datenschutzregel (GDPR) der Europäischen Union, zum Adobe California Privacy Act (CCPA) und anderen spezifischen Datenschutzanforderungen für Target.

### Was ist die Richtlinie von Adobe für diese Regeln? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] erfüllt seine Verpflichtungen als Datenverarbeiter bereits oder ist dabei, die entsprechenden Maßnahmen zu implementieren. Wir haben eine solide Grundlage für zertifizierte Sicherheitskontrollen und Datenschutzkontrollen, die Sie entwerfen und vor dem Termin Mai 2018 Produktverbesserungen vorgenommen haben. Unternehmenskunden sind dafür verantwortlich, diese Verbesserungen zu implementieren sowie die erforderlichen Richtlinien und Vorgehensweisen zu aktualisieren.

### Will my company, the Data Controller, need to submit a GDPR or CCPA request to each [!DNL Adobe Experience Cloud] solution that it uses? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

No, [!DNL Adobe] is providing a central way to help Data Controllers meet their GDPR and CCPA requirements. Datenverantwortliche müssen dazu nicht jede Lösung einzeln aufrufen.

All GDPR and CCPA requests across [!DNL Experience Cloud] solutions, including [!DNL Target], will be made through a central Adobe API, currently called the GDPR API. The API will then complete the request across the Data Controller's [!DNL Experience Cloud] solution suite.

### What information will [!DNL Adobe] enable our customers to delete in response to a data subject/user request? {#section_4B51D00924EC4166B2442218B69214F0}

The information related to an individual visitor within [!DNL Target] is contained within the [!DNL Target] Visitor Profile. [!DNL Target]Kunden können in alle Daten löschen, die mit einer ID in ihrem Besucherprofil verbunden sind. Beispiele für die Profildatenspeicherung [!DNL Target] finden Sie unter [Besucherprofil](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

Aggregierte oder anonymisierte Daten (beispielsweise Berichtsdaten), in denen keine Person identifiziert wird, oder Daten, die nicht mit einer bestimmten Person in Verbindung gebracht werden können (beispielsweise Inhaltsdaten), werden bei der Löschungsanfrage eines Benutzers nicht berücksichtigt.

[!DNL Target] Besucherprofile, die für 90 Tage inaktiv waren, werden standardmäßig gelöscht, ohne dass eine Aktion erforderlich ist.

### What IDs are supported to help customers complete a GDPR or CCPA access and deletion request for [!DNL Target]? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] unterstützt die folgenden ID-Typen zum Auffinden eines Kundenprofils:

| Benutzer-ID | Namespace-ID-Typ | Namespace-ID | Definition |
|--- |--- |--- |--- |
| Experience Cloud ID (ECID) | Standard | 4 | Adobe Experience Cloud ID, früher als Besucher-ID oder Experience Cloud ID bezeichnet. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| TnT-ID/Cookie-ID(TNTID) | Standard | 9 | Target-Kennung, die als Cookie im Browser des Besuchers gespeichert wird. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| Drittanbieter-ID/CRM-ID (THIRDPARTYID) | Target-spezifisch | Nicht zutreffend | Wenn Sie Target mit Ihrem CRM oder andere eindeutige Kennungsinformationen für Ihre Kunden bereitstellen. |

>[!NOTE]
>
>Obwohl [!DNL Target] domänenübergreifende Cookies von Erstanbietern und Drittanbietern unterstützt werden, werden Erstanbieter [!DNL Target] -Cookies nur für GDPR und CCPA empfohlen.

### How does [!DNL Target] handle consent management? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR und CCPA ändern sich nicht, wenn Sie die Zustimmung erhalten, aber wie Sie es erhalten. Die Einwilligungsstrategie jedes Kunden hängt von den erfassten Daten, den Verwendungspraktiken und den Datenschutzrichtlinien des Kunden ab. Consent management isn’t supported by and shouldn’t be achieved via [!DNL Target] for GDPR and CCPA.

[!DNL Adobe] bietet zurzeit keine Lösung zur Verwaltung von Einwilligungen. Auf dem Markt werden jedoch verschiedene Tools entwickelt, durch die einige der neuen Anforderungen abgedeckt werden. For more information on privacy tools in general, including consent managers, see the [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) on the *International Association of Privacy Professionals (iaap)* website.

[!DNL Target] bietet Unterstützung für die Teilnahme an Funktionen über Support [!DNL Launch] zur Unterstützung Ihrer Genehmigungsmanagementstrategie. Opt-in functionality lets customers control how and when the [!DNL Target] tag is fired. There is also an option via [!DNL Launch] to pre-approve the [!DNL Target] tag. Using [!DNL Launch] to manage opt-in is the recommended approach. Further granular control exists in [!DNL Launch] to hide select elements of your page prior to the [!DNL Target] firing that might be helpful to leverage as part of your consent strategy.

For more information on GDPR, CCPA, and [!DNL Launch], see [The Adobe Privacy JavaScript Library and GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html). Also, see the *Adobe Target and Experience Platform Launch opt-in* section above.

### Übermittelt AdobePrivacy.js Informationen an die DSGVO-API? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] leitet diese Informationen *nicht* an die API weiter. Dies muss der Kunde übernehmen. Die Bibliothek stellt nur die IDs bereit, die im Browser für einen bestimmten Besucher gespeichert wurden.

### Welche Daten werden von removeIdentities entfernt? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities]** entfernt diese Identitäten nur aus dem Browser und hängt davon ab, ob die [!DNL Adobe] Lösung es implementiert hat.

[!DNL Target] Löscht beispielsweise die Cookies, die seine IDs speichern, [!DNL Adobe Audience Manager] aber (AAM) löscht die demdex-ID nicht, die in einem Drittanbieter-Cookie gespeichert ist.

### What information needs to be included in a Target GDPR or CCPA request? {#section_D29A4744AE6344E68AD7710B185FD6D0}

In addition to the requirements from Central Privacy Service, a valid GDPR or CCPA message for [!DNL Target] contains:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            "namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            "namespace":"TNTID", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"THIRDPARTYID", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
}
```

### Welche Arten von Antworten von Target über die DSGVO-API kann ich erwarten? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Anfragestatus | Target-Antwortnachricht | Szenario |
|--- |--- |--- |
| Verarbeitung | Verarbeitung | Target hat die GDPR- oder CCPA-Anforderung erhalten und verarbeitet. |
| Abgeschlossen | Nicht zutreffend: Der Unternehmenskontext ist nicht zutreffend. | Die IMS-ID in der GDPR- oder CCPA-Anfrage wird keinem Target-Client zugeordnet.<br>Beachten Sie, dass manche Unternehmen über mehrere IMS-IDs verfügen. Sie müssen die IMS-ID übermitteln, über die Target bereitgestellt wird. |
| Abgeschlossen | Nicht zutreffend: Benutzerkontext nicht gefunden. | Die in der GDPR- oder CCPA-Anfrage angegebene ID für den jeweiligen Besucher oder Datenbetreff ist im Target-Profilspeicher nicht vorhanden.<br>Diese Antwort erhalten Sie auch, wenn Sie versuchen, einen Namespace-ID-Typ zu übermitteln, der nicht von Target unterstützt wird (unterstützte IDs finden Sie oben). |
| Fehler | Fehlermeldung (abhängig vom Fehlertyp) | Fehler beim Abrufen oder Löschen des angeforderten Profils der betroffenen Person.<br>Fehler beim Hochladen in Azure für die Zugriffsanfrage. |

### Welche Antwort sendet Target bei einer Zugriffsanfrage an die DSGVO-API? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Responses to access data requests contain a summary of the [!DNL Target] profile for the visitor in question. Note that this return is sent to the [!DNL Experience Cloud] GDPR API, which in turn sends Data Controllers a response.

A sample [!DNL Target] access API response could look like this:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            ~"namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            ~"namespace":"tntId", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"thirdPartyId", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
} 
```

| Feld | Beschreibung |
|--- |--- |
| jobId | Gibt die GDPR- oder CCPA-Auftrags-ID aus der Central GDPR API an. |
| imsOrgID | Stellt eine eindeutige Kennung für Ihr Unternehmen bereit. |
| namespace | Wird auch als Datenquelle bezeichnet. Siehe "Welche IDs werden unterstützt, damit Kunden einen GDPR- oder CCPA-Zugriff abschließen und Anfrage für Target löschen können? « in diesem Thema. |
| type | Der ID-Typ, für den Sie den GDPR- oder CCPA-Datenzugriff angefordert haben. In Target können mehrere standardmäßige und Target-spezifische ID-Typen angegeben werden. Siehe "Welche IDs werden unterstützt, damit Kunden einen GDPR- oder CCPA-Zugriff abschließen und Anfrage für Target löschen können? « in diesem Thema. |
| value | Die ID des Namespace/der Datenquelle. Siehe "Welche IDs werden unterstützt, damit Kunden einen GDPR- oder CCPA-Zugriff abschließen und Anfrage für Target löschen können? « für gültige Werte. |
| integration code | Bei Integrationscode handelt es sich um Anzeigenamen für Ihre Datenquellen, die statt Datenquellen-IDs verwendet werden, um Ihnen den Überblick über Ihre Datenquellen zu erleichtern. |

Wenn mehrere Werte zur Bestimmung von Profilen angegeben werden, verfügt jede gültige ID über eine Profildatei. The profile file(s) are sent to the central GDPR Azure Blob through the GDPR Central API, in the format of [!DNL Target] Profile JSON response.

A sample [!DNL Target] Profile JSON could look like the following example:

```
{"profileAttributes": 
 
"Sample_Parameter":{"value":"Gold Loyalty Status","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"user.ReturnTimeOfDay":{"value":"44.0","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"firstSessionStart":{"value":"1523497450602","modifiedAt":"2018-04-11T21:44:10.000-04:00"}, 
 
"user.sessionCountScript":{"value":"1","modifiedAt":"2018-04-11T21:44:14.000-04:00"} 
   } 
} 
```

Die im Beispiel verwendeten JSON-Felder des Profils werden in der folgenden Tabelle beschrieben:

| Feld | Beschreibung |
|--- |--- |
| Sample_Parameter | Many pieces of information in the [!DNL Target] profile are uploaded or directly provided by the Data Controller. In this example, a parameter was uploaded into the [!DNL Target] profile using the Profile Update API. Weitere Informationen finden Sie unter [Methoden zum Abrufen von Daten in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md). |
| user.ReturnTimeOfDay | Dieses Standardfeld enthält die Tageszeit des letzten Rückkehrbesuchs eines Benutzers. |
| firstSessionStart | Dieses Standardfeld enthält die Tageszeit, zu der die erste Sitzung des Benutzers begann. |
| user.sessionCountScript | Many pieces of information in the [!DNL Target] profile are uploaded or directly provided by the Data Controller. In diesem Beispiel erhöht ein Profilskript die Anzahl der Sitzungen dieses Besuchers auf der Site des Datenverantwortlichen. Weitere Informationen finden Sie unter [Profilskript-Attribute](/help/c-target/c-visitor-profile/profile-parameters.md). |

>[!NOTE]
>
>This is a shortened version of a [!DNL Target] profile JSON for the purpose of illustration. Many of the fields of the [!DNL Target] profile are not standard. Die zurückgegebenen Daten hängen von den Informationen in diesem spezifischen Besucherprofil ab.

### Unterstützt Target IP-Verschleierung? {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] unterstützt IP-Verschleierung, wenn Sie ihn als Teil Ihrer GDPR- oder CCPA-Implementierungsstrategie verwenden möchten. Weitere Informationen finden Sie unter [Datenschutz](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0).
