---
description: Informationen über die allgemeine Datenschutzregel (GDPR) der Europäischen Union und den California Privacy Act (CCPA) von Kalifornien sowie die Auswirkungen dieser Regeln auf Ihre Organisation und Adobe Target.
keywords: gdpr; eu; european union; Datenschutz; faq; häufig gestellte Fragen; california consumer privacy act; ccpa
seo-description: Informationen über die allgemeine Datenschutzregel (GDPR) der Europäischen Union und den California Privacy Act (CCPA) von Kalifornien sowie die Auswirkungen dieser Regeln auf Ihre Organisation und Adobe Target.
seo-title: Allgemeine Datenschutzregeln (GDPR), California Consumer Privacy Act (CCPA) und Adobe Target
solution: Target
title: Datenschutz und Datenschutz
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
translation-type: tm+mt
source-git-commit: 222fb66f58ea5bcecabfaa2ab966ad9a686dc9ef

---


# Datenschutz und Datenschutz {#privacy-and-general-data-protection-regulation-gdpr}

Informationen über die allgemeine Datenschutzregel (GDPR) der Europäischen Union und den California Privacy Act (CCPA) von Kalifornien sowie die Auswirkungen dieser Regeln [!DNL Adobe Target]auf Ihr Unternehmen.

## Übersicht zu Privatsphäre und Datenschutz-Grundverordnung (DSGVO) {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Hier finden Sie Informationen dazu, wie Adobe bei der Zusammenarbeit mit Ihnen die Compliance mit der Datenschutz-Grundverordnung (DSGVO) der Europäischen Union gewährleistet.

### Übersicht über die DSGVO {#section_8C99434A431B4494998B01B869E7EA5D}

Am 25. Mai 2018 wurde das GDPR der europäischen Union in Kraft getreten. Weitere Informationen darüber, was dies für Sie bedeutet, finden Sie unter [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

Wenn Adobe einem Unternehmen Software und Dienstleistungen bereitstellt, tritt Adobe als Datenverarbeiter für alle personenbezogenen Daten auf, die im Rahmen dieser Dienstleistungen gespeichert und verarbeitet werden. Als Datenverarbeiter verarbeitet Adobe personenbezogene Daten gemäß den gewährten Berechtigungen und Anweisungen Ihres Unternehmens (z. B. über Angaben in Ihrer Vereinbarung mit Adobe).

Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten Adobe in Ihrem Namen verarbeitet und speichert. Wenn Sie Adobe Experience Cloud-Lösungen nutzen, hostet Adobe abhängig von den verwendeten Lösungen und den Informationen, die Sie an Ihr Adobe Experience Cloud-Konto senden, möglicherweise personenbezogene Daten für Sie. Eine detaillierte Liste mit Beispielen finden Sie unter [Adobe Experience Cloud-Datenschutz](https://www.adobe.com/privacy/marketing-cloud.html#collect).

Adobe Experience Cloud bietet Datenverantwortlichen APIs, die auf die DSGVO vorbereitet sind und die folgenden Aufgaben vor dem Inkrafttreten der DSGVO ermöglichen:

* Auf die in Target gespeicherten Daten der betroffenen Person zugreifen
* Die in Target gespeicherten Daten der betroffenen Person löschen

### Die Adobe-Website zur API für die Datenschutz-Grundverordnung {#section_51B8FA3CBE234E9592BDA7083B5CE4CD}

Weitere Informationen finden Sie unter:

* [Website der Adobe-DSGVO-API](https://www.adobe.io/apis/cloudplatform/gdpr.html)
* [DSGVO-Dokumentation](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## Übersicht über den California Privacy Act (CCPA) von Kalifornien

Der Adobe California Privacy Act (CCPA) ist am 1. Januar 2020 gültig. Im Design gibt das Gesetz dem California-Regulator das Recht, Anpassungen vorzunehmen und die Details zu verdeutlichen. Dies bedeutet, dass Sie möglicherweise viele Fragen haben. Wenn Sie Fragen haben, sind Sie nicht allein mit den Unsicherheiten im Gesetz beschäftigt, und versuchen Sie, einen Ansatz zur Behebung der rechtlichen, operativen und technischen Anforderungen zu verstehen und zu entwickeln.

Die CCPA bietet Kalifornien-Verbrauchern neue Rechte bezüglich ihrer persönlichen Informationen und stellt für bestimmte Unternehmen, die in Kalifornien Geschäfte durchführen, Datenschutz vor. Auf einer hohen Ebene stellt das Gesetz Phennians verschiedene wichtige Rechte bereit, einschließlich Berechtigungen für: (1) Request Information (Data Access) (Datenzugriff), (2) deaktiviert aus dem Verkauf persönlicher Informationen (ein sehr weit definiertes Recht zur Deaktivierung von Informationen mit Dritten), (3) haben persönliche Informationen gelöscht und (4) werden darüber informiert, dass persönliche Informationen bekannt gemacht oder verkauft werden.

Wenn Sie im vergangenen Jahr beschäftigt waren, um sich für das Datenschutzrecht (GDPR) Europas zu entscheiden, können einige dieser Rechte bekannt sein und viele der Aufgaben, die Sie durchgeführt haben, können möglicherweise reproduziert werden.

## Adobe Target- und Adobe Launch-Opt-in {#section_6F7B53F5E40C4425934627B653E831B0}

Target bietet Opt-in-Funktionalität über Adobe Launch zur Unterstützung Ihrer Einwilligungsverwaltung. Mit der Opt-in-Funktion können Kunden steuern, wie und wann das Target-Tag ausgelöst wird. Darüber hinaus bietet Adobe Launch die Option, das Target-Tag vorab zu genehmigen. Um Opt-in in Target at.js zu aktivieren, sollten Sie `targetGlobalSettings` benutzen und die Einstellung `optinEnabled=true` hinzufügen. In Launch müssen Sie in der DSGVO-Opt-in-Dropdownliste im Installationsfenster der Target Launch-Erweiterung „Aktivieren“ auswählen. Weitere Details finden Sie in der [Dokumentation zu Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md).

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
>Die Verwendung von Adobe Launch zur Verwaltung von Opt-ins ist der empfohlene Ansatz. In Adobe Launch können Sie außerdem präziser steuern, ob ausgewählte Elemente Ihrer Seite vor der Target-Auslösung ausgeblendet werden. Dies ist nützlich für Ihre Strategie zur Einwilligungsverwaltung.

Es gibt drei Szenarien, in denen Sie die Verwendung des Opt-ins in Betracht ziehen sollten:

1. **Das Target-Tag wird vorab über Adobe Launch genehmigt (oder die betroffene Person hat Target zuvor genehmigt):** Das Target-Tag wird nicht für die Einwilligung gespeichert und funktioniert wie erwartet.
1. **Das Target-Tag wird NICHT vorab genehmigt und`bodyHidingEnabled`ist FALSE:** Das Target-Tag wird erst ausgelöst, wenn die Einwilligung vom Kunden eingeholt wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. Nachdem die Einwilligung eingeholt wurde, wird Target aufgerufen und der personalisierte Inhalte wird der betroffenen Person (Besucher) zur Verfügung gestellt. Da vor der Einwilligung nur der Standardinhalt verfügbar ist, ist die richtige Strategie entscheidend, wie z. B. eine Splash-Seite, die Seitenteile mit personalisierten Inhalten überdeckt. So wird gewährleistet, dass das Erlebnis für die betroffene Person (Besucher) einheitlich bleibt.
1. **Das Target-Tag wird NICHT vorab genehmigt und`bodyHidingEnabled`ist TRUE:** Das Target-Tag wird erst ausgelöst, wenn die Einwilligung vom Kunden eingeholt wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. Da jedoch `bodyHidingEnabled` auf TRUE festgelegt ist, bestimmt `bodyHiddenStyle`, welcher Inhalt auf der Seite ausgeblendet wird, bis das Target-Tag ausgelöst wird (oder die betroffene Person den Opt-in ablehnt, woraufhin der Standardinhalt angezeigt wird). `bodyHiddenStyle` ist standardmäßig als `body { opacity:0;`} festgelegt, was das HTML-Body-Tag ausblendet. Die empfohlene Seitenkonfiguration finden Sie unten. So können Sie den gesamten Body der Seite – abgesehen von der Einwilligungsdialog – ausblenden, indem Sie den Seiteninhalt in einen und den Einwilligungsdialog in einen anderen Container einfügen. Mit diesem Setup wird Target so konfiguriert, dass nur der Container mit dem Seiteninhalt ausgeblendet wird. Weitere Informationen zur Konfiguration dieser Einstellungen finden Sie in der [Adobe Launch-Dokumentation](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html).

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

Häufig gestellte Fragen zum allgemeinen Data Protection Protection (GDPR) und zum California Consumer Privacy Act (CCPA) für Adobe Target.

### Was ist die Richtlinie von Adobe für diese Regeln? {#section_A6849628D6524C80A6E16946DC5D25A9}

Adobe erfüllt seine Verpflichtungen als Datenverarbeiter bereits oder ist dabei, die entsprechenden Maßnahmen zu implementieren. Adobe verfügt durch Sicherheitszertifikate und integrierte Datenschutzoptionen über eine solide Basis, die durch zusätzliche Verbesserungen bis zum Stichtag im Mai 2018 weiter verstärkt wird. Unternehmenskunden sind dafür verantwortlich, diese Verbesserungen zu implementieren sowie die erforderlichen Richtlinien und Vorgehensweisen zu aktualisieren.

### Will my company, the Data Controller, need to submit a GDPR or CCPA request to each Adobe Experience Cloud solution that it uses? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

Nein, Adobe stellt eine zentrale Methode zur Unterstützung von Datencontrollern zur Erfüllung ihrer GDPR- und CCPA-Anforderungen bereit. Datenverantwortliche müssen dazu nicht jede Lösung einzeln aufrufen.

Alle GDPR- und CCPA-Anforderungen in Experience Cloud-Lösungen, einschließlich Target, erfolgen über eine zentrale Adobe API, die derzeit als GDPR-API bezeichnet wird. Die API führt die Anfrage daraufhin in der gesamten Experience Cloud-Lösungssuite des Datenverantwortlichen aus.

### Für welche Informationen ermöglicht Adobe eine Löschung, wenn Kunden von betroffenen Personen oder Benutzern dazu aufgefordert werden? {#section_4B51D00924EC4166B2442218B69214F0}

In Target sind die Informationen zu den einzelnen Besuchern im jeweiligen Target-Besucherprofil enthalten. Kunden können in Adobe Target alle Daten löschen, die mit einer ID in ihrem Besucherprofil verbunden sind. Beispiele in Adobe Target gespeicherter Profildaten finden Sie unter [Besucherprofil](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

Aggregierte oder anonymisierte Daten (beispielsweise Berichtsdaten), in denen keine Person identifiziert wird, oder Daten, die nicht mit einer bestimmten Person in Verbindung gebracht werden können (beispielsweise Inhaltsdaten), werden bei der Löschungsanfrage eines Benutzers nicht berücksichtigt.

Target-Besucherprofile, die seit 90 Tagen inaktiv sind, werden standardmäßig gelöscht, ohne dass eine weitere Aktion erforderlich ist.

### What IDs are supported to help customers complete a GDPR or CCPA access and deletion request for Target? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

Target unterstützt die folgenden ID-Typen zum Auffinden eines Kundenprofils:

| Benutzer-ID | Namespace-ID-Typ | Namespace-ID | Definition |
|--- |--- |--- |--- |
| Experience Cloud ID (ECID) | Standard | 4 | Adobe Experience Cloud ID, früher als Besucher-ID oder Experience Cloud ID bezeichnet. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| TnT-ID/Cookie-ID(TNTID) | Standard | 9 | Target-Kennung, die als Cookie im Browser des Besuchers gespeichert wird. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| Drittanbieter-ID/CRM-ID (THIRDPARTYID) | Target-spezifisch | Nicht zutreffend | Wenn Sie Target mit Ihrem CRM oder andere eindeutige Kennungsinformationen für Ihre Kunden bereitstellen. |

>[!NOTE]
>
>Adobe Target unterstützt sowohl domänenübergreifende als auch domänenübergreifende Cookies von Drittanbietern, die Adobe Target-Cookies von Erstanbietern werden jedoch nur für GDPR und CCPA empfohlen.

### Wie werden Einwilligungen in Adobe Target verwaltet? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR und CCPA ändern sich nicht, wenn Sie die Zustimmung erhalten, aber wie Sie es erhalten. Die Einwilligungsstrategie jedes Kunden hängt von den erfassten Daten, den Verwendungspraktiken und den Datenschutzrichtlinien des Kunden ab. Die Genehmigungsverwaltung wird nicht unterstützt und sollte nicht über Target für GDPR und CCPA erreicht werden.

Adobe bietet zurzeit keine Lösung zur Verwaltung von Einwilligungen. Auf dem Markt werden jedoch verschiedene Tools entwickelt, durch die einige der neuen Anforderungen abgedeckt werden. Weitere Informationen zu Datenschutztools im Allgemeinen, einschließlich Tools zur Einwilligungsverwaltung, finden Sie auf der Website der International Association of Privacy Professionals (IAAP) unter [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf).

Adobe Target bietet Opt-in-Funktionalität über Adobe Launch zur Unterstützung Ihrer Einwilligungsverwaltung. Mit der Opt-in-Funktion können Kunden steuern, wie und wann das Adobe Target-Tag ausgelöst wird. Darüber hinaus bietet Adobe Launch die Option, das Adobe Target-Tag vorab zu genehmigen. Die Verwendung von Adobe Launch zur Verwaltung von Opt-ins ist der empfohlene Ansatz. In Adobe Launch können Sie außerdem präziser steuern, ob ausgewählte Elemente Ihrer Seite vor der Adobe Target-Auslösung ausgeblendet werden. Dies ist nützlich für Ihre Strategie zur Einwilligungsverwaltung.

For more information on GDPR, CCPA and Adobe Launch, see [The Adobe Privacy JavaScript Library and GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html). sowie im obigen Abschnitt „Adobe Target- und Adobe Launch-Opt-in“.

### Übermittelt AdobePrivacy.js Informationen an die DSGVO-API? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] leitet diese Informationen *nicht* an die API weiter. Dies muss der Kunde übernehmen. Die Bibliothek stellt nur die IDs bereit, die im Browser für einen bestimmten Besucher gespeichert wurden.

### Welche Daten werden von removeIdentities entfernt? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities] *entfernt nur* die IDs im Browser. Das gilt nur dann, wenn die Adobe-Lösung dies implementiert hat.

Target löscht beispielsweise die Cookies zum Speichern der IDs, Adobe Audience Manager (AAM) löscht die in einem Drittanbieter-Cookie gespeicherte demdex-ID jedoch nicht.

### What information needs to be included in a Target GDPR or CCPA request? {#section_D29A4744AE6344E68AD7710B185FD6D0}

Zusätzlich zu den Anforderungen des Central Privacy Service gibt es eine gültige GDPR- oder CCPA-Nachricht für Target:

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

Antworten auf Anfragen nach Zugriff auf Daten enthalten eine Zusammenfassung des Target-Profils für den betroffenen Besucher. Beachten Sie, dass eine solche Antwort an die Experience Cloud-DSGVO-API gesendet wird, die wiederum die Antwort an die Datenverantwortlichen weiterleitet.

Beispiel für eine Antwort der Target-API auf eine Zugriffsanfrage:

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

Wenn mehrere Werte zur Bestimmung von Profilen angegeben werden, verfügt jede gültige ID über eine Profildatei. Die Profildateien werden in Form einer JSON-Antwort des Target-Profils über die zentrale DSGVO-API an das zentrale DSGVO-Azure Blob gesendet.

Im Folgenden finden Sie ein Beispiel für eine Target-Profil-JSON:

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
| Sample_Parameter | Viele Informationen im Target-Profil werden vom Datenverantwortlichen hochgeladen oder direkt bereitgestellt. In diesem Beispiel wurde ein Parameter im Target-Profil mithilfe der API zur Profilaktualisierung hochgeladen. Weitere Informationen finden Sie unter [Verfahren für die Datenübernahme in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md). |
| user.ReturnTimeOfDay | Dieses Standardfeld enthält die Tageszeit des letzten Rückkehrbesuchs eines Benutzers. |
| firstSessionStart | Dieses Standardfeld enthält die Tageszeit, zu der die erste Sitzung des Benutzers begann. |
| user.sessionCountScript | Viele Informationen im Target-Profil werden vom Datenverantwortlichen hochgeladen oder direkt bereitgestellt. In diesem Beispiel erhöht ein Profilskript die Anzahl der Sitzungen dieses Besuchers auf der Site des Datenverantwortlichen. Weitere Informationen finden Sie unter [Profilskript-Attribute](/help/c-target/c-visitor-profile/profile-parameters.md). |

>[!NOTE]
>
>Dies ist eine gekürzte Version des JSON-Codes für ein Target-Profil zur Veranschaulichung. Bei zahlreichen Feldern im Target-Profil handelt es sich nicht um Standardfelder. Die zurückgegebenen Daten hängen von den Informationen in diesem spezifischen Besucherprofil ab.

## Unterstützt Target IP-Verschleierung? {#section_428907B0CD9842D9B245B38C66A53C6A}

Target unterstützt IP-Verschleierung in Target, wenn Sie ihn als Teil Ihrer GDPR- oder CCPA-Implementierungsstrategie verwenden möchten. Weitere Informationen finden Sie unter [Datenschutz](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0).
