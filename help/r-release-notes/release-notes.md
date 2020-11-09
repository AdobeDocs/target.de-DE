---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
feature: release notes
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 27%

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!IMPORTANT]
>
>* **mbox.js Ende der Lebensdauer**: Am 18. Januar 2021 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 18. Januar 2021 schlagen alle von &quot;mbox.js&quot;ausgeführten Aufrufe korrekt fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite &quot;Ankündigungen&quot;der Zielgruppe finden Sie Informationen zu den bevorstehenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Standard/Premium 20.10.1 (27. Oktober 2020)

Diese Version enthält die folgenden neuen Funktionen:

| Funktion | Details |
| --- | --- |
| [Geräteinterne Entscheidungsfindung](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | Mit der gerätegestützten Entscheidungsfindung können sowohl Marketingexperten als auch Produktentwickler experimentelle und maschinelle Learning-gestützte Personalisierung von einem Benutzergerät über Kanal hinweg bei nahezu null Latenz bereitstellen.<br>Schnelligkeit und Leistung sind wichtig - in Kundeneinsichten und Benutzerzufriedenheit.<br>Mit der On-Device-Entscheidungsfindung können Sie wichtige Personalisierungs- und Experimentierungsanweisungen in den Aktivitäten A/B-Test- und Erlebnis-Targeting (XT) in &quot;Optimierungsartefakte:&quot;kompilieren, die über das CDN auf Kundengeräte geladen werden. Und weil die Entscheidung auf dem Gerät eine native Verbindung mit [!DNL Adobe Experience Cloud] Produkten herstellt, erhalten die [!DNL Target] Benutzer eine schnelle Analyse und schnellere Erlebnisdurchläufe.<br>Weitere Informationen finden Sie unter *[Einführung in die Geräteentscheidung](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning)* im *Adobe Target SDKs-Handbuch*.<br>**Melden Sie sich jetzt für ein Live-Webinar an.** Nehmen Sie an Adobe Target-Produktexperten teil, wenn Sie besprechen, wie sich Entscheidungen zur Optimierung kritischer Erlebnisse auf dem Gerät zur lokalen Ausführung mit Nulllatenz aufregenden neuen Anwendungsfällen öffnen lassen und gleichzeitig die Site-Performance für Ihre Kunden verbessern können.<ul><li>10. November 2020</li><li>10.00 Uhr PT / 23.00 Uhr CT / 13.00 Uhr ET</li><li>[Hier registrieren](https://www.adobeeventsonline.com/Target/2020/OnDeviceDecisions/invite.html)</li></ul> |

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass [!UICONTROL durchschnittliches Vertrauensintervall] und [!UICONTROL Konfidenz] für die Zeile [!DNL Auto-Target] Gesamt [!UICONTROL in] Berichte angezeigt wurden. Die Messungen werden für alle einzelnen Erlebnisse korrekt angezeigt. (TGT-37301)
* Es wurde ein Problem behoben, das den Berichte der [!DNL Adobe Target Premium] automatischen Zielgruppe [!UICONTROL von] Benutzern ab dem 15. September 2009 um 14:30 Uhr beeinträchtigte. (PDT) bis 6. Oktober, 9.25 Uhr (PDT). Bei der Anzeige von Berichten für die betroffenen Konversionsmetriken (die entweder mit der Option &quot;[!UICONTROL Angezeigte Seite]&quot;oder &quot;[!UICONTROL Auf mbox]geklickt&quot;konfiguriert wurden) werden die Konversionsraten falsch gemeldet. Es ist derzeit kein Problem mit dem Versand bekannt. Informationen zum Resynchronisieren und Korrigieren Ihres Berichte finden Sie im Berichte [zur automatischen Zielgruppe](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) unter *Behobene Probleme* bei *bekannten Problemen und gelöste Probleme*.
* Es wurde eine auswählbare Spalte [!UICONTROL Letzte Aktualisierung am] in der Tabelle [!UICONTROL Katalogsuche] und ein Filter [!UICONTROL Letzte Aktualisierung am] hinzugefügt. Diese Verbesserung spart Zeit und Mühe, da Sie nicht jedes einzelne Element öffnen müssen, um zu sehen, wann es zuletzt aktualisiert wurde, und Sie nach dem Datum filtern können, an dem die Elemente zuletzt aktualisiert wurden.

   ![Zuletzt aktualisiert bei Spalten- und Filterdarstellung](/help/r-release-notes/assets/column-and-filter.png)

* Es wurden Aktualisierungen vorgenommen, um die Benutzeroberfläche der Zielgruppe mit den [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Level A und AA Success Criteria (WCAG 2.0 AA) kompatibel zu machen. (TGT-34384 und TGT-24679)
* Verbesserungen der Content Security Policy (CSP). (TGT-37035)
* Es wurde eine Methode zur Angabe des Clientcodes als Parameter für Kunden eingeführt, die CNAME verwenden. (TNT-38571)
* [!DNL Adobe Experience Cloud] Dokumentation wird verschoben zu [!DNL Experience League]. Im Oktober wechseln alle Versionshinweise, Artikel, Videos und Tutorials von ihrem aktuellen Speicherort `docs.adobe.com` zu [!DNL Experience League]. Dieser Schritt stellt sicher, dass alle Lern-, Selbsthilfe-, Aktivierungs- und Community-Inhalte an einem Ort bereitgestellt werden. Wenn diese Änderung eintritt, müssen Sie nichts tun, da alle Links weitergeleitet werden [!DNL Experience League]. Wir werden die Versionshinweise aktualisieren, sobald der Cutover beginnt.

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
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu [Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
