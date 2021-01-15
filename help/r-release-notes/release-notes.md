---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
feature: Release Notes
translation-type: tm+mt
source-git-commit: bffda8c3461998767a002d66fd9340252237ae5d
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 27%

---


# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden.
>
>* **Adobe Experience Platform Web SDK**: Mit dem  [!UICONTROL Adobe Experience Platform Web ] SDK können Sie über das Adobe Experience Edge Network mit den verschiedenen Diensten im  [!DNL Experience Cloud] (einschließlich  [!DNL Target]) interagieren. Wenn Sie eine Migration zu [!DNL Adobe Experience Platform Web SDK] vornehmen, finden Sie weitere Informationen unter [Was ist Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md), im *Web SDK Guide*.
   >
   >
* **at.js**: Die JavaScript-Bibliothek at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen. Wenn Sie zu at.js migrieren möchten, finden Sie weitere Informationen unter [Funktionsweise von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Obwohl &quot;mbox.js&quot;derzeit unterstützt wird (bis 31. März 2021), haben wir seit Juli 2017 keine Funktionsupdates für diese Bibliothek bereitgestellt. Indem wir alle Kunden in das [!UICONTROL Adobe Experience Platform Web SDK] oder at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.

Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## at.js 2.4.0 (14. Januar 2021)

Diese Version von at.js ist ein Maintenance Release und umfasst die folgenden Fehlerbehebungen:

* Unterstützt Versand-API-KundenIDs mit Unified Profil/Platform ID.
* Fehlerhafte Tag-Injektion im Stil wurde behoben.

## Target Standard/Premium 20.10.1 (27. Oktober 2020)

Diese Version enthält die folgenden neuen Funktionen:

| Funktion | Details |
| --- | --- |
| [Geräteinterne Entscheidungsfindung](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | Mit der gerätegestützten Entscheidungsfindung können sowohl Marketingexperten als auch Produktentwickler experimentelle und maschinelle Learning-gestützte Personalisierung von einem Benutzergerät über Kanal hinweg bei nahezu null Latenz bereitstellen.<br>Schnelligkeit und Leistung sind wichtig - in Kundeneinsichten und Benutzerzufriedenheit.<br>Mit der On-Device-Entscheidungsfindung können Sie wichtige Personalisierungs- und Experimentierungsanweisungen in den Aktivitäten A/B-Test- und Erlebnis-Targeting (XT) in &quot;Optimierungsartefakte:&quot;kompilieren, die über das CDN auf Kundengeräte geladen werden. Da die Entscheidungsfindung auf dem Gerät eine native Verbindung mit [!DNL Adobe Experience Cloud]-Produkten herstellt, erhalten [!DNL Target]-Benutzer eine schnelle Analyse und schnellere Erlebnis-Iterationen.<br>Weitere Informationen finden Sie unter *[On-device-Entscheidungsfindung](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md). |

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass [!UICONTROL Durchschnittliches Intervall für die Steigerung des Vertrauens] und [!UICONTROL Konfidenz] im [!DNL Auto-Target]-Berichte für die Zeile [!UICONTROL Gesamt] angezeigt wurden. Die Messungen werden für alle einzelnen Erlebnisse korrekt angezeigt. (TGT-37301)
* Es wurde ein Problem behoben, das den Berichte [!DNL Adobe Target Premium] users’ [!UICONTROL Auto-Zielgruppe] ab 15. September 2009 um 14:30 Uhr beeinträchtigte. (PDT) bis 6. Oktober, 9.25 Uhr (PDT). Bei der Anzeige von Berichten für die betroffenen Konversionsmetriken (die entweder mit der Option &quot;[!UICONTROL Angezeigte Seite]&quot;oder &quot;[!UICONTROL Auf mbox] geklickt&quot;konfiguriert wurden) werden die Konversionsraten fälschlicherweise gemeldet. Es ist derzeit kein Problem mit dem Versand bekannt. Informationen zum Resynchronisieren und Korrigieren Ihres Berichte finden Sie unter [Berichte für die automatische Zielgruppe](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) unter *Behobene Probleme* in *Bekannte Probleme und gelöste Probleme*.
* Es wurde eine auswählbare Spalte [!UICONTROL Zuletzt aktualisiert am] in der Tabelle [!UICONTROL Katalogsuche] und ein Filter [!UICONTROL Zuletzt aktualisiert am] hinzugefügt. Diese Verbesserung spart Zeit und Mühe, da Sie nicht jedes einzelne Element öffnen müssen, um zu sehen, wann es zuletzt aktualisiert wurde, und Sie nach dem Datum filtern können, an dem die Elemente zuletzt aktualisiert wurden.

   ![Zuletzt aktualisiert bei Spalten- und Filterdarstellung](/help/r-release-notes/assets/column-and-filter.png)

* Es wurden Aktualisierungen vorgenommen, um die Benutzeroberfläche der Zielgruppe mit [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Level A und AA Success Criteria (WCAG 2.0 AA) kompatibel zu machen. (TGT-34384 und TGT-24679)
* Verbesserungen der Content Security Policy (CSP). (TGT-37035)
* Es wurde eine Methode zur Angabe des Clientcodes als Parameter für Kunden eingeführt, die CNAME verwenden. (TNT-38571)
* [!DNL Adobe Experience Cloud] Dokumentation wird verschoben zu  [!DNL Experience League]. Im Oktober wechseln alle Versionshinweise, Artikel, Videos und Tutorials von ihrem aktuellen Speicherort unter `docs.adobe.com` zu [!DNL Experience League]. Dieser Schritt stellt sicher, dass alle Lern-, Selbsthilfe-, Aktivierungs- und Community-Inhalte an einem Ort bereitgestellt werden. Wenn diese Änderung eintritt, müssen Sie nichts tun, da alle Links zu [!DNL Experience League] umgeleitet werden. Wir werden die Versionshinweise aktualisieren, sobald der Cutover beginnt.

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu  [Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
