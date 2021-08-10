---
keywords: DSGVO; eu; Europäische Union; Datenschutz; faq; häufig gestellte Fragen; california consumer privacy act; ccpa; Datenschutz; Schutz der Daten; opt-out; abmelden; Regierung; Vorschrift
description: Erfahren Sie mehr über [!DNL Target] und die Datenschutz-Grundverordnung (DSGVO) der Europäischen Union, den California Consumer Privacy Act (CCPA) und andere Datenschutzanforderungen.
title: Wie geht [!DNL Target] mit Datenschutzbestimmungen um?
feature: Datenschutz und Sicherheit
role: Developer
exl-id: 5013a9d2-a463-4787-90ee-3248d9cb02b2
source-git-commit: 2ee87e2c6e8bbdb62eedf709e6454a0467197749
workflow-type: tm+mt
source-wordcount: '2204'
ht-degree: 56%

---

# Vorschriften zur Privatsphäre und zum Datenschutz

Informationen über die Datenschutz-Grundverordnung (DSGVO) der Europäischen Union, den California Consumer Privacy Act (CCPA) und andere internationale Datenschutzanforderungen. Erfahren Sie, wie sich diese Vorschriften auf Ihr Unternehmen und [!DNL Adobe Target] auswirken.

## Überblick über den Datenschutz und die Datenschutz-Grundverordnung (DSGVO)  {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Am 25. Mai 2018 trat die DSGVO der Europäischen Union in Kraft. Weitere Informationen dazu, was diese Verordnung für Sie bedeutet, finden Sie unter [DSGVO und Ihr Unternehmen](https://business.adobe.com/privacy/general-data-protection-regulation.html).

Wenn [!DNL Adobe] einem Unternehmen Software und Dienstleistungen bereitstellt, tritt [!DNL Adobe] als Datenverarbeiter für alle personenbezogenen Daten auf, die im Rahmen dieser Dienstleistungen gespeichert und verarbeitet werden. Als Datenverarbeiter verarbeitet [!DNL Adobe] personenbezogene Daten gemäß den gewährten Berechtigungen und Anweisungen Ihres Unternehmens (z. B. gemäß Ihrer Vereinbarung mit [!DNL Adobe]).

Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten [!DNL Adobe] in Ihrem Namen verarbeitet und speichert. Wenn Sie [!DNL Adobe Experience Cloud]-Lösungen nutzen, hostet [!DNL Adobe] abhängig von den verwendeten Lösungen und den Informationen, die Sie an Ihr Adobe [!DNL Adobe Experience Cloud]-Konto senden, möglicherweise personenbezogene Daten für Sie. Eine detaillierte Liste mit Beispielen finden Sie unter [Adobe Experience Cloud-Datenschutz](https://www.adobe.com/privacy/experience-cloud.html#collect).

[!DNL Adobe Experience Cloud] stellt Datenverantwortlichen DSGVO-kompatible APIs bereit, mit denen sie die folgenden Aufgaben ausführen können:

* Auf die in [!DNL Target] gespeicherten Daten der betroffenen Person zugreifen
* Die in [!DNL Target] gespeicherten Daten der betroffenen Person löschen

Weitere Informationen finden Sie unter:

* [Website der Adobe-DSGVO-API](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [DSGVO-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en)

## Übersicht über den California Consumer Privacy Act (CCPA)

Der California Consumer Privacy Act (CCPA) bietet Verbrauchern in Kalifornien neue Rechte bezüglich ihrer personenbezogenen Daten und überträgt Unternehmen, die in Kalifornien Geschäfte treiben, Pflichten bezüglich des Datenschutzes. Der CCPA trat am 1. Januar 2020 in Kraft.

Das Gesetz überträgt den Bürgern Kaliforniens auf hoher Ebene verschiedene grundlegende Rechte, einschließlich folgender:

* Anforderung von Informationen (Datenzugriff)
* Opt-out vom Verkauf personenbezogener Daten (ein weit gefasstes Recht, sich gegen die Weitergabe von Informationen an Dritte zu entscheiden)
* Löschen der personenbezogenen Daten
* Einholen von Informationen darüber, dass personenbezogene Daten bekannt gemacht oder verkauft werden

Wenn Sie im vergangenen Jahr damit beschäftigt waren, sich auf das europäische Datenschutzrecht (DSGVO) vorzubereiten, könnten einige dieser Rechte bekannt sein und ein Großteil der Arbeit, die Sie geleistet haben, kann umgewidmet werden.

>[!NOTE]
>
>Der Zugriff auf und das Löschen von Daten, da sie für den CCPA gelten, folgt demselben Prozess wie für die DSGVO.

## Adobe [!DNL Target] und [!DNL Adobe Experience Platform Launch] Opt-in {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] unterstützt die Opt-in-Funktionalität über [!DNL Platform Launch] und hilft Ihnen bei der Einwilligungsverwaltung. Mit der Opt-in-Funktion können Kunden steuern, wie und wann das [!DNL Target]-Tag ausgelöst wird. Darüber hinaus gibt es eine Option über [!DNL Platform Launch] zur Vorab-Genehmigung des [!DNL Target]-Tags. Um die Opt-in-Funktion in der [!DNL Target]-at.js-Bibliothek zu aktivieren, sollten Sie `targetGlobalSettings` benutzen und die Einstellung `optinEnabled=true` hinzufügen. Wählen Sie in [!DNL Platform Launch] in der Dropdownliste [!UICONTROL DSGVO-Opt-in] in der Installationsansicht der Erweiterung [!DNL Platform Launch] die Option &quot;Aktivieren&quot;. Weitere Informationen finden Sie in der [Platform launch-Dokumentation](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) .

Im folgenden Code-Snippet wird gezeigt, wie Sie die `optinEnabled=true`-Einstellung aktivieren:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>Die Opt-in-Funktionalität wird in at.js-Version 1.7.0 und at.js 2.1.0 oder höher unterstützt. Die Opt-in-Funktion wird nicht in at.js-Version 2.0.0 und 2.0.1 unterstützt.
>
>Es wird empfohlen, zur Verwaltung von Opt-ins [!DNL Platform Launch] zu verwenden. In [!DNL Platform Launch] gibt es eine weitere detaillierte Steuerung, um ausgewählte Elemente Ihrer Seite vor der [!DNL Target]-Auslösung auszublenden. Dies ist hilfreich bei der Verwendung im Rahmen Ihrer Einwilligungsstrategie.

In Verbindung mit dem Opt-in gibt es drei Szenarien:

1. **[!DNL Target]-Tag wird vorab über [!DNL Platform Launch] genehmigt (oder die betroffene Person hat zuvor [!DNL Target]genehmigt):** Das [!DNL Target]-Tag wird nicht für die Einwilligung gespeichert und funktioniert wie erwartet.
1. **Das [!DNL Target]-Tag wird NICHT vorab genehmigt und `bodyHidingEnabled` ist FALSE:** Das [!DNL Target]-Tag wird erst ausgelöst, wenn die Einwilligung vom Kunden eingeholt wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. Nachdem die Einwilligung eingeholt wurde, wird [!DNL Target] aufgerufen und der personalisierte Inhalt wird der betroffenen Person (Besucher) zur Verfügung gestellt. Da vor der Zustimmung nur Standardinhalte verfügbar sind, ist es wichtig, eine geeignete Strategie zu verwenden, z. B. eine Begrüßungsseite, die einen beliebigen Teil der Seite oder Inhalte abdeckt, die möglicherweise personalisiert sind. Dadurch wird sichergestellt, dass das Erlebnis für die betroffene Person (den Besucher) konsistent bleibt.
1. **Das [!DNL Target]-Tag wird NICHT vorab genehmigt und `bodyHidingEnabled` ist TRUE:** Das [!DNL Target]-Tag wird erst ausgelöst, wenn die Einwilligung vom Kunden eingeholt wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. Da jedoch `bodyHidingEnabled` auf TRUE festgelegt ist, bestimmt `bodyHiddenStyle`, welcher Inhalt auf der Seite ausgeblendet wird, bis das [!DNL Target]-Tag ausgelöst wird (oder die betroffene Person den Opt-in ablehnt, woraufhin der Standardinhalt angezeigt wird). Standardmäßig ist `bodyHiddenStyle` auf `body { opacity:0;}` gesetzt, wodurch das HTML-Body-Tag ausgeblendet wird. Die von der Adobe empfohlene Seitenkonfiguration ist unten so festgelegt, dass der gesamte Hauptteil der Seite, mit Ausnahme des Dialogfelds des Zustimmungsverwalters, ausgeblendet wird, indem der Seiteninhalt in einen Container und das Dialogfeld des Zustimmungsverwalters in einen separaten Container eingefügt werden. Mit diesem Setup wird [!DNL Target] so konfiguriert, dass nur der Container mit dem Seiteninhalt ausgeblendet wird. Weitere Informationen zur Konfiguration dieser Einstellungen finden Sie in der [Platform launch-Dokumentation .](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en)

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

## Häufig gestellte Fragen zu Datenschutz und Datenschutzvorschriften {#concept_41F88DE95D2943178BEC382736B5C038}

Häufig gestellte Fragen zur Datenschutz-Grundverordnung (DSGVO) der Europäischen Union, zum California Consumer Privacy Act (CCPA) und anderen internationalen Datenschutzanforderungen für [!DNL Target].

### Wie lautet die [!DNL Adobe]-Richtlinie für diese Vorschriften? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] erfüllt seine Verpflichtungen als Datenverarbeiter bereits oder ist dabei, sie umzusetzen. Adobe verfügt über eine solide Grundlage zertifizierter Sicherheitskontrollen und Datenschutzkontrollen, die vorab bis zum Stichtag Mai 2018 vorgenommen wurden. Unternehmenskunden sind dafür verantwortlich, diese Verbesserungen zu implementieren und alle erforderlichen Richtlinien und Verfahren zu aktualisieren.

### Muss mein Unternehmen, der Datenverantwortliche, eine DSGVO- oder CCPA-Anfrage an jede verwendete [!DNL Adobe Experience Cloud]-Lösung senden? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

Nein, [!DNL Adobe] bietet eine zentrale Möglichkeit, Datenverantwortliche bei der Erfüllung ihrer DSGVO- und CCPA-Anforderungen zu unterstützen. Datenverantwortliche müssen nicht direkt zu jeder Lösung navigieren.

Alle DSGVO- und CCPA-Anfragen für [!DNL Experience Cloud]-Lösungen, einschließlich [!DNL Target], erfolgen über eine zentrale [!DNL Adobe]-API, die derzeit als DSGVO-API bezeichnet wird. Die API führt dann die Anfrage über die [!DNL Experience Cloud] -Lösungssuite des Datenverantwortlichen aus.

### Welche Informationen ermöglicht es [!DNL Adobe] Kunden, diese zu löschen, wenn eine betroffene Person/ein Benutzer darum ersucht wird? {#section_4B51D00924EC4166B2442218B69214F0}

In [!DNL Target] sind die Informationen zu den einzelnen Besuchern im jeweiligen [!DNL Target]-Besucherprofil enthalten. [!DNL Target] ermöglicht Kunden das Löschen aller Daten, die mit einer ID in ihrem Besucherprofil verknüpft sind. Beispiele für die Profildaten, die [!DNL Target] speichert, finden Sie unter [Besucherprofil](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

Aggregierte oder anonymisierte Daten (beispielsweise Berichtsdaten), in denen keine Person identifiziert wird, oder Daten, die nicht mit einer bestimmten Person in Verbindung gebracht werden können (beispielsweise Inhaltsdaten), werden bei der Löschungsanfrage eines Benutzers nicht berücksichtigt.

[!DNL Target]-Besucherprofile, die seit 90 Tagen inaktiv sind, werden standardmäßig gelöscht, ohne dass eine weitere Aktion erforderlich ist.

### Welche IDs werden unterstützt, um Kunden zu helfen, Datenzugriffs- und Löschungsanfragen gemäß der DSGVO oder dem CCPA in [!DNL Target]nachzukommen?{#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] unterstützt die folgenden ID-Typen zum Auffinden eines Kundenprofils:

| Benutzer-ID | Namespace-ID-Typ | Namespace-ID | Definition |
|--- |--- |--- |--- |
| Experience Cloud ID (ECID) | Standard | 4 | [!UICONTROL Adobe Experience Cloud ID], früher als Besucher-ID oder Experience Cloud-ID bezeichnet. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| TnT-ID/Cookie-ID(TNTID) | Standard | 9 | [!DNL Target] Kennung, die als Cookie im Browser des Besuchers gesetzt wird. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| Drittanbieter-ID/CRM-ID  (THIRDPARTYID) | [!DNL Target]-Spezifische/s | nicht angegeben | Wenn Sie [!DNL Target] mit Ihrem CRM-System oder anderen eindeutigen Kennungsinformationen für Ihre Kunden angeben. |

>[!NOTE]
>
>Obwohl [!DNL Target] domänenübergreifende Cookies von Erstanbietern und Drittanbietern unterstützt, werden Erstanbieter-[!DNL Target]-Cookies nur für die DSGVO und CCPA empfohlen.

### Wie verwaltet [!DNL Target] Einwilligungen? {#section_C86BF5EE4FAA47039659850E7594A6BA}

Die DSGVO und der CCPA ändern sich nicht, wann Sie die Einwilligung einholen müssen, sondern wie Sie sie einholen. Die Einwilligungsstrategie jedes Kunden hängt von den Datenerfassungs- und Nutzungspraktiken und den Datenschutzrichtlinien des Kunden ab. Das Einwilligungsmanagement für die DSGVO und den CCPA wird nicht von [!DNL Target] unterstützt und sollte auch nicht darüber durchgeführt werden.

[!DNL Adobe] bietet zurzeit keine Lösung zur Verwaltung von Einwilligungen. Auf dem Markt werden jedoch verschiedene Tools entwickelt, durch die einige der neuen Anforderungen abgedeckt werden. Weitere Informationen zu Datenschutztools im Allgemeinen, einschließlich Tools für die Einwilligungsverwaltung, finden Sie im [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) auf der Website *International Association of Privacy Professionals (iaap)* .

[!DNL Target] bietet Opt-in-Funktionalität über  [!DNL Platform Launch] zur Unterstützung Ihrer Einwilligungsverwaltung. Mit der Opt-in-Funktion können Kunden steuern, wie und wann das [!DNL Target]-Tag ausgelöst wird. Darüber hinaus gibt es eine Option über [!DNL Platform Launch] zur Vorab-Genehmigung des [!DNL Target]-Tags. Es wird empfohlen, zur Verwaltung von Opt-ins [!DNL Platform Launch] zu verwenden. In [!DNL Platform Launch] gibt es eine weitere detaillierte Steuerung, um ausgewählte Elemente Ihrer Seite vor der [!DNL Target]-Auslösung auszublenden. Dies kann hilfreich sein, wenn Sie diese im Rahmen Ihrer Einwilligungsstrategie verwenden.

Weitere Informationen zu DSGVO, CCPA und [!DNL Launch] finden Sie unter [Die Adobe Privacy JavaScript Library und die DSGVO](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en). Lesen Sie auch den Abschnitt *Adobe Target- und Adobe Launch-Opt-in*.

### Übermittelt `AdobePrivacy.js` Informationen an die DSGVO-API? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] leitet diese Informationen *nicht* an die API weiter. Dies muss der Kunde übernehmen. Die Bibliothek stellt nur die IDs bereit, die im Browser für einen bestimmten Besucher gespeichert wurden.

### Was entfernt `removeIdentities`? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL `removeIdentities`] *entfernt nur* die IDs im Browser. Das gilt nur dann, wenn die [!DNL Adobe]-Lösung dies implementiert hat.

[!DNL Target] löscht beispielsweise die Cookies zum Speichern der IDs, aber [!DNL Adobe Audience Manager] (AAM) löscht nicht die in einem Drittanbieter-Cookie gespeicherte demdex-ID.

### Welche Informationen müssen in einer [!DNL Target] DSGVO- oder CCPA-Anfrage enthalten sein? {#section_D29A4744AE6344E68AD7710B185FD6D0}

Neben den Anforderungen des Central Privacy Service enthält eine gültige DSGVO- oder CCPA-Anfrage für [!DNL Target] folgende Elemente:

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

### Welche Arten von Antworten kann ich von [!DNL Target] über die DSGVO-API erwarten? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Anfragestatus | [!DNL Target] Antwortmeldung | Szenario |
|--- |--- |--- |
| Verarbeitung | Verarbeitung | [!DNL Target] hat die DSGVO- oder CCPA-Anfrage erhalten und hat mit der Verarbeitung begonnen. |
| Abgeschlossen | Nicht zutreffend: Der Unternehmenskontext ist nicht zutreffend. | Die IMS-ID in der DSGVO- oder CCPA-Anfrage wird keinem [!DNL Target]-Client zugeordnet.<br>Einige Unternehmen verfügen über mehrere IMS-IDs. Senden Sie die IMS-ID, wobei [!DNL Target] bereitgestellt wird. |
| Abgeschlossen | Nicht zutreffend: Benutzerkontext nicht gefunden. | Die in der DSGVO- oder CCPA-Anfrage angegebene ID für den spezifischen Besucher oder die betroffene Person ist nicht im Profilspeicher [!DNL Target] vorhanden.<br>Dieses Ergebnis gibt auch zurück, wenn Sie versuchen, einen Namespace-ID-Typ zu übermitteln, der von nicht unterstützt wird  [!DNL Target] (unterstützte IDs finden Sie oben). |
| Fehler | Fehlermeldung (abhängig vom Fehlertyp) | Fehler beim Abrufen oder Löschen des angeforderten Profils der betroffenen Person.<br>Fehler beim Hochladen in Azure für die Zugriffsanfrage. |

### Welche Antwort sendet [!DNL Target] für eine Zugriffsanfrage an die DSGVO-API? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Antworten auf Anfragen zum Datenzugriff enthalten eine Zusammenfassung des [!DNL Target]-Profils für den betroffenen Besucher. Diese Antwort wird an die DSGVO-API [!DNL Experience Cloud] gesendet, die wiederum den Datenverantwortlichen eine Antwort sendet.

Beispiel für eine Antwort der [!DNL Target]-API auf eine Zugriffsanfrage:

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
| jobId | Gibt die DSGVO- oder CCPA-Auftrags-ID aus der zentralen DSGVO-API an. |
| imsOrgID | Stellt eine eindeutige Kennung für Ihr Unternehmen bereit. |
| namespace | Wird auch als Datenquelle bezeichnet. Siehe &quot;Welche IDs werden unterstützt, um Kunden zu helfen, eine DSGVO- oder CCPA-Zugriffs- und Löschungsanfrage für [!DNL Target] durchzuführen?&quot; in diesem Thema. |
| type | Der Typ der ID, für die Sie den Datenzugriff nach DSGVO oder CCPA angefordert haben. [!DNL Target] akzeptiert mehrere ID-Typen, von denen einige Standard- und einige spezifisch für  [!DNL Target]sind. Siehe &quot;Welche IDs werden unterstützt, um Kunden zu helfen, eine DSGVO- oder CCPA-Zugriffs- und Löschungsanfrage für [!DNL Target] durchzuführen?&quot; in diesem Thema. |
| value | Die ID des Namespace/der Datenquelle. Siehe &quot;Welche IDs werden unterstützt, um Kunden zu helfen, eine DSGVO- oder CCPA-Zugriffs- und Löschungsanfrage für [!DNL Target] durchzuführen?&quot; für gültige Werte. |
| integration code | Bei Integrationscode handelt es sich um Anzeigenamen für Ihre Datenquellen, die statt Datenquellen-IDs verwendet werden, um Ihnen den Überblick über Ihre Datenquellen zu erleichtern. |

Wenn mehrere Werte zur Bestimmung von Profilen angegeben werden, verfügt jede gültige ID über eine Profildatei. Über die zentrale DSGVO-API werden eine oder mehrere Profildateien im Format [!DNL Target] Profil-JSON-Antwort an das zentrale DSGVO-Azure Blob gesendet.

Im Folgenden finden Sie ein Beispiel für eine [!DNL Target]-Profil-JSON:

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
| Sample_Parameter | Viele Informationen im [!DNL Target]-Profil werden vom Datenverantwortlichen hochgeladen oder direkt bereitgestellt. In diesem Beispiel wurde ein Parameter im [!DNL Target]-Profil mithilfe der API zur Profilaktualisierung hochgeladen. Weitere Informationen finden Sie unter [Verfahren für die Datenübernahme in [!DNL Target]](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md). |
| user.ReturnTimeOfDay | Dieses Standardfeld enthält die Tageszeit des letzten Rückkehrbesuchs eines Benutzers. |
| firstSessionStart | Dieses Standardfeld enthält die Tageszeit, zu der die erste Sitzung des Benutzers begann. |
| user.sessionCountScript | Viele Informationen im [!DNL Target]-Profil werden vom Datenverantwortlichen hochgeladen oder direkt bereitgestellt. In diesem Beispiel erhöht ein Profilskript die Anzahl der Sitzungen dieses Besuchers auf der Site des Datenverantwortlichen. Weitere Informationen finden Sie unter [Profilskript-Attribute](/help/c-target/c-visitor-profile/profile-parameters.md). |

>[!NOTE]
>
>Dieses Codebeispiel ist eine gekürzte Version eines JSON-Profils [!DNL Target] zur Veranschaulichung. Bei zahlreichen Feldern im [!DNL Target]-Profil handelt es sich nicht um Standardfelder. Die zurückgegebenen Daten hängen von den Informationen im jeweiligen Besucherprofil ab.

### Unterstützt [!DNL Target] IP-Verschleierung? {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] unterstützt IP-Verschleierung, wenn Sie sie im Rahmen Ihrer DSGVO- oder CCPA-Implementierungsstrategie einsetzen. Weitere Informationen finden Sie unter  [Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0).

### Sollte ich etwas unternehmen, um zu verhindern, dass meine Daten an Dritte weitergegeben oder verkauft werden?

[!DNL Target] ermöglicht es Kunden nicht, Daten direkt von  [!DNL Target] an Dritte weiterzugeben oder zu verkaufen, sodass kein Opt-out vom Verkauf für  [!DNL Target]erfolgt.
