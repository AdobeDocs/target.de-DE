---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen Versionen der DNL-Adobe-Zielgruppe enthalten.
title: Versionshinweise zu Adobe Zielgruppe
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 578f71f84f4db06dbc91679562007450166a8a22

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert: 9. März 2020**

>[!NOTE]
>
>* Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
   >
   >
* Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.
   >
   >
* **Änderungen** der TLS-Unterstützung: Ab dem 1. März 2020 deaktiviert Zielgruppe die Unterstützung für TLS 1.1- und TLS 1.0-Verschlüsselung. Transport Layer Security (TLS) ist das am weitesten verbreitete Sicherheitsprotokoll, das aktuell in Webbrowsern und anderen Anwendungen Verwendung findet, bei denen über ein Netzwerk übertragene Daten geschützt werden müssen. Diese Änderung ist erforderlich, um den allgemein anerkannten Sicherheitsstandard von TLS 1.2 oder höher zu erfüllen. Überprüfen Sie, welche TLS-Version Sie aktuell verwenden. Wenn Ihre Version niedriger als 1.2 ist, implementieren Sie die erforderlichen Änderungen vor dem 1. März 2020, um die Zielgruppe wie erwartet weiter zu verwenden.
   >
   >   
   Detaillierte Informationen zu den möglichen Auswirkungen und den Schritten, die Sie zur Aktualisierung Ihrer Implementierung unternehmen müssen, finden Sie unter Änderungen [der](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)TLS-Verschlüsselung (Transport Layer Security).
   >
   >
* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Zielgruppe nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.


## Zielgruppe Standard/Premium 20.2.1 (zu bestimmen)

Hier finden Sie das genaue Datum, an dem diese Informationen verfügbar werden.

>[!IMPORTANT]
>
>Siehe Informationen über die Einstellung von &quot;mbox.js&quot;.

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass Kunden beim Durchführen einer Katalogsuche eine Sammlung auswählen konnten. (TGT-36230)
* Es wurde ein Problem behoben, durch das Kriterien, die über API erstellt wurden, aber nicht von einer in der Benutzeroberfläche der Zielgruppe erstellten Aktivität referenziert wurden, fälschlicherweise aus der Benutzeroberfläche gelöscht werden konnten. (TGT-35917)
* Implementierung von Sicherheitsverbesserungen in Content Security Policy (CSP). (TGT-36190)
* Es wurde ein Fehler behoben, der dazu führte, dass &quot;NaN%&quot;angezeigt wurde, wenn die prozentuale Attributgewichtung nach links verschoben wurde. (TGT-36211)
* Es wurden Probleme mit der lokale Anpassung behoben, sodass der Benutzeroberflächentext in verschiedenen Sprachen korrekt angezeigt wird.
* Die folgenden Adobe Analytics-Metriken werden ab Version der Zielgruppe vom März 2020 nicht mehr für Analytics for Zielgruppe (A4T) unterstützt:
   * averagevisitdepth
   * Bots
* Die folgenden Metriken werden nicht mehr unterstützt und beim ersten Ändern einer Aktivität mit der Metrik automatisch in neue Versionen der Metrik konvertiert:

   | Veraltete Metrik | Neue Metrik |
   |--- |--- |
   | `averagetimespentonpage` | `averagetimespentonsite` (Hinweis: gemessen in Minuten statt in Sekunden) |
   | `instances` | `occurrences` |
   | `singleaccess` | `singlepagevisits` |
   | `uniquevisitors` | `visitors` |
   | `visitorsdaily`, `visitorshourly`, `visitorsmonthly`, `visitorsquarterly`, `visitorsweekly`, `visitorsyearly` | `visitors` |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
