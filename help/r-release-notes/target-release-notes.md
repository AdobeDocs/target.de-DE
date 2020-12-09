---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
title: Versionshinweise zu Adobe Target
feature: null
translation-type: tm+mt
source-git-commit: f4091506538cd4719302227b88fa11e9d4ae93a6
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 10%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert am: 27. Oktober 2020**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>* **Adobe nochmal als Führer im Gartner Magic Quadrant für Personalisierungsmaschinen**: Adobe wurde im dritten Gartner Magic Quadrant for Personalization Engines 2020-Bericht erneut zum Leader ernannt. Der Gartner Magic Quadrant for Personalization Engines bewertete Anbieter anhand von 15 Kriterien, die in zwei Kategorien unterteilt sind: Vollständigkeit der Sicht und Ausführungsfähigkeit. [Lesen Sie mehr darüber im Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js Ende der Lebensdauer**: Am 18. Januar 2021 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 18. Januar 2021 schlagen alle von &quot;mbox.js&quot;ausgeführten Aufrufe korrekt fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite &quot;Ankündigungen&quot;der Zielgruppe finden Sie Informationen zu den bevorstehenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


## Target Standard/Premium 20.10.1 (27. Oktober 2020)

Diese Version enthält die folgenden neuen Funktionen:

| Funktion | Details |
| --- | --- |
| [Geräteinterne Entscheidungsfindung](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | Mit der gerätegestützten Entscheidungsfindung können sowohl Marketingexperten als auch Produktentwickler experimentelle und maschinelle Learning-gestützte Personalisierung von einem Benutzergerät über Kanal hinweg bei nahezu null Latenz bereitstellen.<br>Schnelligkeit und Leistung sind wichtig - in Kundeneinsichten und Benutzerzufriedenheit.<br>Mit der On-Device-Entscheidungsfindung können Sie wichtige Personalisierungs- und Experimentierungsanweisungen in den Aktivitäten A/B-Test- und Erlebnis-Targeting (XT) in &quot;Optimierungsartefakte:&quot;kompilieren, die über das CDN auf Kundengeräte geladen werden. Und weil die Entscheidung auf dem Gerät eine native Verbindung mit [!DNL Adobe Experience Cloud] Produkten herstellt, erhalten die [!DNL Target] Benutzer eine schnelle Analyse und schnellere Erlebnisdurchläufe.<br>Weitere Informationen finden Sie unter *[On-device-Entscheidungsfindung](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md). |

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass [!UICONTROL durchschnittliches Vertrauensintervall] und [!UICONTROL Konfidenz] für die Zeile [!DNL Auto-Target] Gesamt [!UICONTROL in] Berichte angezeigt wurden. Die Messungen werden für alle einzelnen Erlebnisse korrekt angezeigt. (TGT-37301)
* Es wurde ein Problem behoben, das den Berichte der [!DNL Adobe Target Premium] automatischen Zielgruppe [!UICONTROL von] Benutzern ab dem 15. September 2009 um 14:30 Uhr beeinträchtigte. (PDT) bis 6. Oktober, 9.25 Uhr (PDT). Bei der Anzeige von Berichten für die betroffenen Konversionsmetriken (die entweder mit der Option &quot;[!UICONTROL Angezeigte Seite]&quot;oder &quot;[!UICONTROL Auf mbox]geklickt&quot;konfiguriert wurden) werden die Konversionsraten falsch gemeldet. Es ist derzeit kein Problem mit dem Versand bekannt. Informationen zum Resynchronisieren und Korrigieren Ihres Berichte finden Sie im Berichte [zur automatischen Zielgruppe](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) unter *Behobene Probleme* bei *bekannten Problemen und gelöste Probleme*.
* Es wurde eine auswählbare Spalte [!UICONTROL Letzte Aktualisierung am] in der Tabelle [!UICONTROL Katalogsuche] und ein Filter [!UICONTROL Letzte Aktualisierung am] hinzugefügt. Diese Verbesserung spart Zeit und Mühe, da Sie nicht jedes einzelne Element öffnen müssen, um zu sehen, wann es zuletzt aktualisiert wurde, und Sie nach dem Datum filtern können, an dem die Elemente zuletzt aktualisiert wurden.

   ![Zuletzt aktualisiert bei Spalten- und Filterdarstellung](/help/r-release-notes/assets/column-and-filter.png)

* Es wurden Aktualisierungen vorgenommen, um die Benutzeroberfläche der Zielgruppe mit den [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Level A und AA Success Criteria (WCAG 2.0 AA) kompatibel zu machen. (TGT-34384 und TGT-24679)
* Verbesserungen der Content Security Policy (CSP). (TGT-37035)
* Es wurde eine Methode zur Angabe des Clientcodes als Parameter für Kunden eingeführt, die CNAME verwenden. (TNT-38571)
* [!DNL Adobe Experience Cloud] Dokumentation wird verschoben zu [!DNL Experience League]. Im Oktober wechseln alle Versionshinweise, Artikel, Videos und Tutorials von ihrem aktuellen Speicherort `docs.adobe.com` zu [!DNL Experience League]. Dieser Schritt stellt sicher, dass alle Lern-, Selbsthilfe-, Aktivierungs- und Community-Inhalte an einem Ort bereitgestellt werden. Wenn diese Änderung eintritt, müssen Sie nichts tun, da alle Links weitergeleitet werden [!DNL Experience League]. Wir werden die Versionshinweise aktualisieren, sobald der Cutover beginnt.

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
