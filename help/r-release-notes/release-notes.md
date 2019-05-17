---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Erweiterungen, Fehlerbehebungen und bekannten Problemen in jeder Target Standard- und Target Premium-Version.
keywords: Versionshinweise; Vorabversion
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
seo-title: Target-Versionshinweise (aktuell)
solution: Target
title: Target-Versionshinweise (aktuell)
topic: 'Recommendations '
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version.

## Mitteilungen

Folgende wichtige Ankündigungen sollten Sie kennen:

* Am 20. Februar 2019 wurde die Adobe Target-Infrastruktur in den Regionen EMEA, Japan und APAC aktualisiert, um keine Daten mehr von Endbenutzern mit älteren Geräten oder Webbrowsern zu erfassen, die TLS 1.1 oder höher nicht unterstützen. Dieses Upgrade ist für den Nordamerikanischen Bereich für den **1. April 2019 geplant**. Die Migration zu TLS 1.2 bietet eine verbesserte Sicherheit. Es ist wichtig, dass Sie die Details durchgehen und die Änderungen an Ihrem IT-Team planen, um einen glatten Übergang zu erhalten. Weitere Informationen finden Sie [unter TLS (Transport Layer Security)-](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)Verschlüsselung.
* [!DNL Target] und [!DNL Adobe Marketing Cloud] werden ab März 2019 die Unterstützung für Microsoft Internet Explorer 11 beenden. Diese Änderung betrifft nur [!DNL Target]-Authoring. Diese Änderung wirkt sich nicht auf die Bereitstellung von Erlebnissen aus. Wechseln Sie zu Microsoft Edge oder einem anderen Browser. Weitere Informationen finden Sie unter [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## Visual Experience Composer für Mobilgeräte (14. Mai 2019) {mobile-vec}

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer (VEC) für mobile Apps | Mit Mobile App VEC können Sie Aktivitäten erstellen und Inhalte auf nativen Mobil-Apps ohne ständige Entwicklungsabhängigkeiten und App-Versionszyklen personalisieren.<br>Weitere Informationen finden Sie unter:<ul><li>[Visual Experience Composer für mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Einrichten des Klick-Trackings im Mobile VEC](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li></ul> |

## [!DNL Target] Standard/Premium 19.4.2 (30. April 2019) {#release-19-4-2}

Dieses Release umfasst die folgenden Funktionen, Änderungen und Erweiterungen:

(Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

### Funktionsaktualisierungen

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| [!UICONTROL Visual Experience Composer] | [!UICONTROL Visual Experience Composer] (VEC) umfasst die folgenden Erweiterungen, um Ihre Arbeit schneller und effizienter zu gestalten:<ul><li>Die DOM-Pfad-Funktion steht jetzt beim Einrichten der Klick-Tracking zur Verfügung.<br>Weitere Informationen finden Sie unter [Klick-Tracking](/help/c-activities/r-success-metrics/click-tracking.md#considerations).</li><li>Verwenden Sie das Stilbedienfeld, um den Wert vorhandener Stile für das ausgewählte Element anzuzeigen oder zu bearbeiten. Sie können auch zusätzliche Formatierungen hinzufügen.<br>Um auf das Stile-Bedienfeld zuzugreifen, klicken Sie innerhalb des VEC auf ein Seitenelement und dann auf [!UICONTROL Bearbeiten] &gt; [!UICONTROL Stile].<br>Das Stile-Bedienfeld wird rechts im VEC angezeigt. Das Bedienfeld enthält eine Liste der Stile, mit denen Sie das ausgewählte Element bearbeiten oder zum ausgewählten Element hinzufügen können. Mit einem Echtzeit-CSS-Editor können Sie Änderungen anzeigen und Stile hinzufügen, wenn Sie Cascading Style Sheets (CSS) problemlos verwenden oder Code von Ihrem Entwickler erhalten.<br>Weitere Informationen finden Sie [unter Stile](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in *Visual Experience Composer-Optionen*.</li><li>Der Rich Text Editor unterstützt jetzt verschachtelte HTML 5-Elemente.<br>HTML 5-Spezifikationen ermöglichen neue Kombinationen von Tags zum Verschachteln. Die vorherige Version des Rich-Text-Editors unterstützt keine neue Verschachtelung von Tags, wie von der HTML 5-Spezifikation zugelassen. Daher wurden verschachtelte Elemente, die im VEC ausgewählt wurden, nicht ordnungsgemäß verarbeitet, was zu unerwünschten HTML-Änderungen führte. (TGT -33618)<br>Weitere Informationen finden Sie unter [Text/HTML](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) in *Visual Experience Composer bearbeiten*.</li> |

### Verbesserungen, Fehlerbehebungen und Änderungen

* Wir haben den Arbeitsablauf beim Löschen von Assets mit dem VEC verbessert. Gelöschte Assets werden nun aus der [!UICONTROL Angebotsbibliothek] und aus [!DNL Scene7] (falls zutreffend) entfernt. Gelöschte Elemente werden nicht mehr in den Suchergebnissen angezeigt. (TGT-31981)
* Sie können Asset-Ordner jetzt auch dann löschen, wenn sie Bilder (nicht leere Ordner) enthalten. (TGT-33265)

   Zuvor war es nicht möglich, einen nicht leeren Ordner aus dem Target-Bild zu löschen ([!UICONTROL Angebote] &gt; [!UICONTROL Bildangebote]). Sie erhalten einen &quot;Ordner ist nicht leer! « Benachrichtigung beim Versuch, den Ordner aus der Benutzeroberfläche zu löschen. Mit dieser Funktion fügen wir die Funktion hinzu, mit der Sie den Ordner löschen können, um einen ganzen Ordner mit beliebig vielen Assets und Unterordnern zu entfernen. Diese Funktion ist auch in der Target-Benutzeroberfläche in der Benutzeroberfläche von Adobe Experience Cloud Assets verfügbar.

   * Nicht leere Ordner in der Bildangebotsbibliothek können gelöscht werden. Wenn alle Bilder im Ordner in keiner Aktivität referenziert werden, werden der gesamte Ordner und dessen Inhalt gelöscht. Wenn in einer Aktivität auf einige Bilder im Ordner verwiesen wird, werden alle nicht referenzierten Bilder gelöscht. Referenzierte Bilder und Ordner, die diese Bilder enthalten, bleiben erhalten.
   * Das Rendering von Bildangeboten in der Bild-Asset-Auswahl erfolgt schneller und effizienter.
   Weitere Informationen finden Sie unter [Arbeiten mit Inhalten in der Bibliothek](/help/c-experiences/c-manage-content/assets-working.md). (TGT-32897)

* Wir haben die Darstellung von Bildangeboten im Asset Picker verbessert. Das Anzeigen und Auswählen von Bildangeboten ist jetzt schneller und effizienter. (TGT-32897)
* Wir haben die Verarbeitung von Umleitungen auf URLs verbessert, wenn Sie das Laden einer Seite innerhalb des VEC abbrechen. (TGT-33815)
* Nachdem Sie eine [!UICONTROL Recommendations] -Sammlung aus der Sammlungsauswahl ausgewählt haben, müssen Sie jetzt auf [!UICONTROL die Schaltfläche &quot;Speichern] &quot; klicken. Dieser Arbeitsablauf ist konsistent mit anderen Arbeitsabläufen innerhalb von [!DNL Target]. (TGT-33205)
* Es wurde ein Fehler behoben, der dazu führte, dass ein kleiner Satz an Insight-Berichten anstelle der tatsächlichen Konversionsraten 0% Konversionsraten zurückgab. (TNT-32125)

## [!DNL Target] Standard/Premium 19.4.1 (15. April 2019) {#release-19-4-1}

Diese Version ist eine Wartungsversion und beinhaltet die folgenden Änderungen:

(Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

* Die [!DNL Adobe Experience Cloud] Benutzeroberfläche wurde aktualisiert, um Änderungen an Markenmarken und Produkten widerzuspiegeln. (TGT-33546, TGT-33272 und TGT-33331)

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter [Experience Cloud-Versionshinweise](https://marketing.adobe.com/resources/help/en_US/whatsnew/). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |