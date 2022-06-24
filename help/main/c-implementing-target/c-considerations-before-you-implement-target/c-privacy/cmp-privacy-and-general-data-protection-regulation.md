---
keywords: DSGVO;eu;Europäische Union;Datenschutz;faq;häufig gestellte Fragen;california consumer privacy act;ccpa;Datenschutz;Schutz der Daten;opt-out;abmelden;Gesetz;Vorschrift
description: Hier erhalten Sie Informationen zu  [!DNL Target]  und zur Datenschutz-Grundverordnung (DSGVO) der Europäischen Union, zum California Consumer Privacy Act (CCPA) und zu anderen Datenschutzbestimmungen.
title: Wie handhabt  [!DNL Target]  Datenschutzbestimmungen?
feature: Privacy & Security
role: Developer
exl-id: 5013a9d2-a463-4787-90ee-3248d9cb02b2
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '2235'
ht-degree: 98%

---

# Datenschutz und Datenschutzvorschriften

Hier erhalten Sie Informationen zur Datenschutz-Grundverordnung (DSGVO) der Europäischen Union, zum California Consumer Privacy Act (CCPA) und zu anderen Datenschutzbestimmungen. Erfahren Sie mehr darüber, wie sich diese Vorschriften auf Ihr Unternehmen und [!DNL Adobe Target] auswirken.

## Überblick über den Datenschutz und die Datenschutz-Grundverordnung (DSGVO)  {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Am 25. Mai 2018 trat die DSGVO der Europäischen Union in Kraft. Weitere Informationen darüber, was diese Verordnung für Sie bedeutet, finden Sie unter [GDPR and Your Business](https://business.adobe.com/de/privacy/general-data-protection-regulation.html).

Wenn [!DNL Adobe] einem Unternehmen Software und Dienstleistungen bereitstellt, tritt [!DNL Adobe] als Datenverarbeiter für alle personenbezogenen Daten auf, die im Rahmen dieser Dienstleistungen gespeichert und verarbeitet werden. Als Datenverarbeiter verarbeitet [!DNL Adobe] personenbezogene Daten gemäß den gewährten Berechtigungen und Anweisungen Ihres Unternehmens (z. B. gemäß Ihrer Vereinbarung mit [!DNL Adobe]).

Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten [!DNL Adobe] in Ihrem Namen verarbeitet und speichert. Wenn Sie [!DNL Adobe Experience Cloud]-Lösungen nutzen, hostet [!DNL Adobe] abhängig von den verwendeten Lösungen und den Informationen, die Sie an Ihr Adobe [!DNL Adobe Experience Cloud]-Konto senden, möglicherweise personenbezogene Daten für Sie. Eine detaillierte Liste mit Beispielen finden Sie unter [Adobe Experience Cloud-Datenschutz](https://www.adobe.com/de/privacy/experience-cloud.html#collect).

[!DNL Adobe Experience Cloud] stellt Datenverantwortlichen DSGVO-konforme APIs bereit, mit denen sie die folgenden Aufgaben ausführen können:

* Auf die in [!DNL Target] gespeicherten Daten der betroffenen Person zugreifen
* Die in [!DNL Target] gespeicherten Daten der betroffenen Person löschen

Weitere Informationen finden Sie unter:

* [Übersicht über Adobe Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de){target=-blank}
* [Handbuch zur Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de){target=_blank}
* [Übersicht über die Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/overview.html?lang=de){target=_blank}

## Übersicht über den California Consumer Privacy Act (CCPA)

Der California Consumer Privacy Act (CCPA) bietet Verbrauchern in Kalifornien neue Rechte bezüglich ihrer personenbezogenen Daten und überträgt Unternehmen, die in Kalifornien Geschäfte treiben, Pflichten bezüglich des Datenschutzes. Der CCPA trat am 1. Januar 2020 in Kraft.

Das Gesetz überträgt den Bürgern Kaliforniens auf hoher Ebene verschiedene grundlegende Rechte, einschließlich folgender:

* Anforderung von Informationen (Datenzugriff)
* Abmeldung vom Verkauf personenbezogener Daten (ein weit gefasstes Recht zum Ausstieg aus der Freigabe von Informationen für Dritte)
* Löschen der personenbezogenen Daten
* Einholen von Informationen darüber, dass personenbezogene Daten bekannt gemacht oder verkauft werden

Wenn Sie sich im vergangenen Jahr auf das europäische Datenschutzrecht (DSGVO) vorbereitet haben, sind Ihnen einige dieser Rechte wahrscheinlich bekannt. Möglicherweise können Sie viele der bereits durchgeführten Aufgaben für das neue Gesetz verwenden.

>[!NOTE]
>
>Der Zugriff auf und das Löschen von Daten im Sinn des CCPA erfolgt auf dieselbe Weise wie für die DSGVO.

## Opt-in-Funktion in Adobe [!DNL Target] und [!DNL Adobe Experience Platform] {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] unterstützt die Opt-in-Funktionalität über Tags in [!DNL Adobe Experience Platform] und hilft Ihnen bei der Einwilligungsverwaltung. Mit der Opt-in-Funktion können Kunden steuern, wie und wann das [!DNL Target]-Tag ausgelöst wird. Darüber hinaus gibt es eine Option über [!DNL Adobe Experience Platform] zur Vorab-Genehmigung des [!DNL Target]-Tags. Um die Opt-in-Funktion in der [!DNL Target]-at.js-Bibliothek zu aktivieren, sollten Sie `targetGlobalSettings` benutzen und die Einstellung `optinEnabled=true` hinzufügen. Wählen Sie in [!DNL Adobe ExperiencePlatform] in der Dropdown-Liste [!UICONTROL DSGVO-Opt-in] im Installationsfenster der Erweiterung „Aktivieren“ aus. Siehe [Implementierung [!DNL Target] using [!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} für weitere Details.

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
>Es wird empfohlen, zur Verwaltung von Opt-ins [!DNL Adobe Experience Platform] zu verwenden. In [!DNL Adobe Experience Platform] können Sie präziser steuern, ob ausgewählte Elemente Ihrer Seite vor der [!DNL Target]-Auslösung ausgeblendet werden sollen, was Ihnen bei der Einwilligungsverwaltung helfen kann.

In Verbindung mit dem Opt-in gibt es drei Szenarien:

1. **[!DNL Target]-Tag wird vorab über [!DNL Adobe Experience Platform] genehmigt (oder die betroffene Person hat zuvor [!DNL Target] genehmigt):** Das [!DNL Target]-Tag wird nicht für die Einwilligung gespeichert und funktioniert wie erwartet.
1. **Das [!DNL Target]-Tag wird NICHT vorab genehmigt und `bodyHidingEnabled` ist FALSE:** Das [!DNL Target]-Tag wird erst ausgelöst, wenn die Einwilligung vom Kunden eingeholt wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. Nachdem die Einwilligung eingeholt wurde, wird [!DNL Target] aufgerufen und der personalisierte Inhalt wird der betroffenen Person (Besucher) zur Verfügung gestellt. Da vor der Einwilligung nur der Standardinhalt verfügbar ist, ist die richtige Strategie entscheidend, wie z. B. eine Splash-Seite, die Seitenteile mit personalisierten Inhalten überdeckt. So wird gewährleistet, dass das Erlebnis für die betroffene Person (Besucher) einheitlich bleibt.
1. **Das [!DNL Target]-Tag wird NICHT vorab genehmigt und `bodyHidingEnabled` ist TRUE:** Das [!DNL Target]-Tag wird erst ausgelöst, wenn die Einwilligung vom Kunden eingeholt wurde. Bevor die Einwilligung eingeholt wird, ist nur der Standardinhalt verfügbar. Da jedoch `bodyHidingEnabled` auf TRUE festgelegt ist, bestimmt `bodyHiddenStyle`, welcher Inhalt auf der Seite ausgeblendet wird, bis das [!DNL Target]-Tag ausgelöst wird (oder die betroffene Person den Opt-in ablehnt, woraufhin der Standardinhalt angezeigt wird). `bodyHiddenStyle` ist standardmäßig als `body { opacity:0;}` festgelegt, wodurch das HTML-Body-Tag ausblendet wird. Die empfohlene Seitenkonfiguration von Adobe finden Sie unten. So können Sie den gesamten Hauptteil der Seite – abgesehen vom Einwilligungsdialog – ausblenden, indem Sie den Seiteninhalt in einen und den Einwilligungsdialog in einen anderen Container einfügen. Mit diesem Setup wird [!DNL Target] so konfiguriert, dass nur der Container mit dem Seiteninhalt ausgeblendet wird. Siehe [Übersicht über Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de).

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

Häufig gestellte Fragen zur Datenschutz-Grundverordnung (DSGVO) der Europäischen Union, zum California Consumer Privacy Act (CCPA) und zu anderen internationalen Datenschutzanforderungen für [!DNL Target].

### Wie lautet die Richtlinie von [!DNL Adobe] für diese Vorschriften? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] erfüllt seine Verpflichtungen als Datenverarbeiter bereits oder ist dabei, die entsprechenden Maßnahmen zu implementieren. Adobe verfügt durch Sicherheitszertifikate und integrierte Datenschutzoptionen über eine solide Basis, die durch zusätzliche Verbesserungen bis zum Stichtag im Mai 2018 weiter verstärkt wurden. Unternehmenskunden sind dafür verantwortlich, diese Verbesserungen zu implementieren sowie die erforderlichen Richtlinien und Vorgehensweisen zu aktualisieren.

### Muss mein Unternehmen als Datenverantwortlicher eine DSGVO- oder CCPA-Anfrage für jede verwendete [!DNL Adobe Experience Cloud]-Lösung einreichen? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

Nein, [!DNL Adobe] stellt eine zentrale Möglichkeit bereit, um Datenverantwortliche bei der Erfüllung von DSGVO- und CCPA-Anfragen zu unterstützen. Datenverantwortliche müssen dazu nicht jede Lösung einzeln aufrufen.

Alle DSGVO- und CCPA-Anfragen in [!DNL Experience Cloud]-Lösungen, wie [!DNL Target], werden über eine zentrale [!DNL Adobe]-API vorgenommen, die zurzeit als DSGVO-API bezeichnet wird. Die API führt die Anfrage daraufhin in der gesamten [!DNL Experience Cloud]-Lösungs-Suite des Datenverantwortlichen aus.

### Für welche Informationen ermöglicht [!DNL Adobe] eine Löschung, wenn Kunden von betroffenen Personen oder Benutzern dazu aufgefordert werden? {#section_4B51D00924EC4166B2442218B69214F0}

In [!DNL Target] sind die Informationen zu den einzelnen Besuchern im jeweiligen [!DNL Target]-Besucherprofil enthalten. [!DNL Target]-Kunden können alle Daten löschen, die mit einer ID in ihrem Besucherprofil verbunden sind. Beispiele für die Profildaten, die [!DNL Target] speichert, finden Sie unter [Besucherprofil](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

Aggregierte oder anonymisierte Daten (beispielsweise Berichtsdaten), in denen keine Person identifiziert wird, oder Daten, die nicht mit einer bestimmten Person in Verbindung gebracht werden können (beispielsweise Inhaltsdaten), werden bei der Löschungsanfrage eines Benutzers nicht berücksichtigt.

[!DNL Target]-Besucherprofile, die seit 90 Tagen inaktiv sind, werden standardmäßig gelöscht, ohne dass eine weitere Aktion erforderlich ist.

### Welche IDs werden unterstützt, um Kunden zu helfen, Datenzugriffs- und Löschungsanfragen gemäß der DSGVO oder dem CCPA in [!DNL Target]nachzukommen?{#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] unterstützt die folgenden ID-Typen zum Auffinden eines Kundenprofils:

| Benutzer-ID | Namespace-ID-Typ | Namespace-ID | Definition |
|--- |--- |--- |--- |
| Experience Cloud ID (ECID) | Standard | 4 | [!UICONTROL Adobe Experience Cloud ID], früher als Besucher-ID oder Experience Cloud ID bezeichnet. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| TnT-ID/Cookie-ID(TNTID) | Standard | 9 | [!DNL Target]-Kennung, die als Cookie im Browser des Besuchers gespeichert wird. Sie können die JavaScript-API verwenden, um diese ID zu finden (siehe Details unten). |
| Drittanbieter-ID/CRM-ID   (THIRDPARTYID) | [!DNL Target]-spezifisch | K. A. | Wenn Sie für [!DNL Target] Daten aus dem CRM oder andere eindeutige Kennungsinformationen für Ihre Kunden bereitstellen. |

>[!NOTE]
>
>Obwohl [!DNL Target] Domain-übergreifende Cookies von Erstanbietern und Drittanbietern unterstützt, werden Erstanbieter-[!DNL Target]-Cookies nur für die DSGVO und CCPA empfohlen.

### Wie verwaltet [!DNL Target] Einwilligungen? {#section_C86BF5EE4FAA47039659850E7594A6BA}

Die DSGVO und der CCPA schreiben nicht fest, wann Sie eine Einwilligung einholen müssen, sondern nur, wie Sie diese Einwilligung einholen. Die Einwilligungsstrategie jedes Kunden hängt von den erfassten Daten, den Verwendungspraktiken und den Datenschutzrichtlinien des Kunden ab. Das Einwilligungsmanagement für die DSGVO und den CCPA wird nicht von [!DNL Target] unterstützt und sollte auch nicht darüber durchgeführt werden.

[!DNL Adobe] bietet zurzeit keine Lösung zur Verwaltung von Einwilligungen. Auf dem Markt werden jedoch verschiedene Tools entwickelt, durch die einige der neuen Anforderungen abgedeckt werden. Weitere Informationen zu Datenschutztools im Allgemeinen, einschließlich Tools zur Einwilligungsverwaltung, finden Sie auf der Website der [International Association of Privacy Professionals (iapp)](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) unter *2017 Privacy Tech Vendor Report*.

[!DNL Target] bietet Opt-in-Funktionalität über [!DNL Adobe Experience Platform] zur Unterstützung Ihrer Einwilligungsverwaltung. Mit der Opt-in-Funktion können Kunden steuern, wie und wann das [!DNL Target]-Tag ausgelöst wird. Darüber hinaus gibt es eine Option über [!DNL Adobe Experience Platform] zur Vorab-Genehmigung des [!DNL Target]-Tags. Es wird empfohlen, zur Verwaltung von Opt-ins [!DNL Adobe Experience Platform] zu verwenden. In [!DNL Adobe Experience Platform] können Sie außerdem präziser steuern, ob ausgewählte Elemente Ihrer Seite vor der [!DNL Target]-Auslösung ausgeblendet werden. Dies ist nützlich für Ihre Strategie zur Einwilligungsverwaltung.

Weitere Informationen zur DSGVO, zum CCPA und [!DNL Adobe Experience Platform] finden Sie unter [Die Adobe Privacy JavaScript-Bibliothek und die DSGVO](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en). Lesen Sie auch den obigen Abschnitt *Adobe Target- und Adobe Experience Platform-Opt-in*.

### Übermittelt `AdobePrivacy.js` Informationen an die DSGVO-API? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] leitet diese Informationen *nicht* an die API weiter. Dies muss der Kunde übernehmen. Die Bibliothek stellt nur die IDs bereit, die im Browser für einen bestimmten Besucher gespeichert wurden.

### Welche Daten werden von `removeIdentities` entfernt? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL `removeIdentities`] *entfernt nur* die IDs im Browser. Das gilt nur dann, wenn die [!DNL Adobe]-Lösung dies implementiert hat.

[!DNL Target] löscht beispielsweise die Cookies zum Speichern der IDs, aber [!DNL Adobe Audience Manager] (AAM) löscht nicht die in einem Drittanbieter-Cookie gespeicherte demdex-ID.

### Welche Informationen müssen in einer [!DNL Target]-DSGVO- oder -CCPA-Anfrage enthalten sein? {#section_D29A4744AE6344E68AD7710B185FD6D0}

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

### Welche Arten von Antworten von [!DNL Target] sind über die DSGVO-API zu erwarten?  {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Anfragestatus | [!DNL Target]-Antwort | Szenario |
|--- |--- |--- |
| Verarbeitung | Verarbeitung | [!DNL Target] hat die DSGVO- oder CCPA-Anfrage erhalten und hat mit der Verarbeitung begonnen. |
| Abgeschlossen | Nicht zutreffend: Der Unternehmenskontext ist nicht zutreffend | Die IMS-ID in der DSGVO- oder CCPA-Anfrage ist keinem [!DNL Target]-Client zugeordnet.<br>Einige Unternehmen verfügen über mehrere IMS-IDs. Senden Sie die IMS-ID, in der [!DNL Target] bereitgestellt wurde. |
| Abgeschlossen | Nicht zutreffend: Benutzerkontext nicht gefunden | Die in der DSGVO- oder CCPA-Anfrage angegebene ID für den spezifischen Besucher oder die betroffene Person ist nicht im [!DNL Target]-Profilspeicher vorhanden.<br>Diese Antwort erhalten Sie auch, wenn Sie versuchen, einen Namespace-ID-Typ zu übermitteln, der nicht von [!DNL Target] unterstützt wird (unterstützte IDs finden Sie oben). |
| Fehler | Fehlermeldung (abhängig vom Fehlertyp) | Fehler beim Abrufen oder Löschen des angeforderten Profils der betroffenen Person.<br>Fehler beim Hochladen in Azure für die Zugriffsanfrage. |

### Welche Antwort sendet [!DNL Target] bei einer Zugriffsanfrage an die DSGVO-API? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Antworten auf Anfragen zum Datenzugriff enthalten eine Zusammenfassung des [!DNL Target]-Profils für den betroffenen Besucher. Eine solche Antwort wird an die [!DNL Experience Cloud]-DSGVO-API gesendet, die wiederum die Antwort an die Datenverantwortlichen weiterleitet.

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
| namespace | Wird auch als Datenquelle bezeichnet. Siehe „Welche IDs werden unterstützt, um Kunden zu helfen, Datenzugriffs- und Löschungsanfragen gemäß DSGVO oder CCPA in [!DNL Target] nachzukommen?“ in diesem Thema. |
| type | Der Typ der ID, für die Sie den Datenzugriff nach DSGVO oder CCPA angefordert haben. In [!DNL Target] können mehrere standardmäßige und [!DNL Target]-spezifische ID-Typen angegeben werden. Siehe „Welche IDs werden unterstützt, um Kunden zu helfen, Datenzugriffs- und Löschungsanfragen gemäß DSGVO oder CCPA in [!DNL Target] nachzukommen?“ in diesem Thema. |
| value | Die ID des Namespace/der Datenquelle. Siehe „Welche IDs werden unterstützt, um Kunden zu helfen, Datenzugriffs- und Löschungsanfragen gemäß DSGVO oder CCPA in [!DNL Target] nachzukommen?“ für gültige Werte. |
| integration code | Bei Integrationscode handelt es sich um Anzeigenamen für Ihre Datenquellen, die statt Datenquellen-IDs verwendet werden, um Ihnen den Überblick über Ihre Datenquellen zu erleichtern. |

Wenn mehrere Werte zur Bestimmung von Profilen angegeben werden, verfügt jede gültige ID über eine Profildatei. Eine oder mehrere Profildateien werden in Form einer JSON-Antwort des [!DNL Target]-Profils über die zentrale DSGVO-API an das zentrale DSGVO-Azure Blob gesendet.

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
| Sample_Parameter | Viele Informationen im [!DNL Target]-Profil werden vom Datenverantwortlichen hochgeladen oder direkt bereitgestellt. In diesem Beispiel wurde ein Parameter im [!DNL Target]-Profil mithilfe der API zur Profilaktualisierung hochgeladen. Weitere Informationen finden Sie unter [Verfahren für die Datenübernahme [!DNL Target]](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/){target=_blank}. |
| user.ReturnTimeOfDay | Dieses Standardfeld enthält die Tageszeit des letzten Rückkehrbesuchs eines Benutzers. |
| firstSessionStart | Dieses Standardfeld enthält die Tageszeit, zu der die erste Sitzung des Benutzers begann. |
| user.sessionCountScript | Viele Informationen im [!DNL Target]-Profil werden vom Datenverantwortlichen hochgeladen oder direkt bereitgestellt. In diesem Beispiel erhöht ein Profilskript die Anzahl der Sitzungen dieses Besuchers auf der Site des Datenverantwortlichen. Weitere Informationen finden Sie unter [Profilskript-Attribute](/help/main/c-target/c-visitor-profile/profile-parameters.md). |

>[!NOTE]
>
>Dieses Code-Beispiel ist eine gekürzte Version einer [!DNL Target]-Profil-JSON und dient der Veranschaulichung. Bei zahlreichen Feldern im [!DNL Target]-Profil handelt es sich nicht um Standardfelder. Die zurückgegebenen Daten hängen von den Informationen im jeweiligen Besucherprofil ab.

### Unterstützt [!DNL Target] IP-Verschleierung?  {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] unterstützt IP-Verschleierung, wenn Sie sie im Rahmen Ihrer DSGVO- oder CCPA-Implementierungsstrategie einsetzen. Weitere Informationen finden Sie unter   [Datenschutz](https://developer.adobe.com/target/before-implement/privacy/privacy/){target=_blank}.

### Sollte ich etwas unternehmen, um zu verhindern, dass meine Daten an Dritte weitergegeben oder verkauft werden?

[!DNL Target] ermöglicht es Kunden nicht, Daten direkt über [!DNL Target] an Dritte weiterzugeben oder zu verkaufen, weshalb es für [!DNL Target] keine Opt-out-Option für den Verkauf gibt.
