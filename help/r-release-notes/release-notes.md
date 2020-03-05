---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 336726bef7a8a3a8cf4abed37ccdeb63b8efa369

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Target-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!NOTE]
>
>* **Änderungen** der TLS-Unterstützung: Ab dem 1. März 2020 deaktiviert Target die Unterstützung für TLS 1.1- und TLS 1.0-Verschlüsselung. Transport Layer Security (TLS) ist das am weitesten verbreitete Sicherheitsprotokoll, das aktuell in Webbrowsern und anderen Anwendungen Verwendung findet, bei denen über ein Netzwerk übertragene Daten geschützt werden müssen. Diese Änderung ist erforderlich, um den allgemein anerkannten Sicherheitsstandard von TLS 1.2 oder höher zu erfüllen. Überprüfen Sie, welche TLS-Version Sie aktuell verwenden. Wenn Ihre Version niedriger als 1.2 ist, implementieren Sie die erforderlichen Änderungen vor dem 1. März 2020, um Target wie erwartet weiter zu verwenden.
   >
   >   
   Detaillierte Informationen zu den möglichen Auswirkungen und den Schritten, die Sie zur Aktualisierung Ihrer Implementierung unternehmen müssen, finden Sie unter Änderungen [der](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)TLS-Verschlüsselung (Transport Layer Security).
   >
   >
* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Target-Aktivitäten ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen anbieten und Ihnen den Support anbieten, den Sie von Adobe erwarten.
   >
   >
* Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.


## Target Standard/Premium 20.2.1 (3. März 2020) 

>[!IMPORTANT]
>
>Siehe Informationen über die Einstellung von &quot;mbox.js&quot;.

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass Kunden beim Durchführen einer Katalogsuche eine Sammlung auswählen konnten. (TGT-36230)
* Es wurde ein Problem behoben, durch das Kriterien, die über API erstellt wurden, aber nicht von einer in der Target-Benutzeroberfläche erstellten Aktivität referenziert wurden, fälschlicherweise aus der Benutzeroberfläche gelöscht werden konnten. (TGT-35917)
* Implementierung von Sicherheitsverbesserungen in Content Security Policy (CSP). (TGT-36190)
* Es wurde ein Fehler behoben, der dazu führte, dass &quot;NaN%&quot;angezeigt wurde, wenn die prozentuale Attributgewichtung nach links verschoben wurde. (TGT-36211)
* Lokalisierungsprobleme wurden behoben, sodass der Text der Benutzeroberfläche in verschiedenen Sprachen korrekt angezeigt wird.
* Die folgenden Adobe Analytics-Metriken werden ab der Target-Version März 2020 nicht mehr für Analytics for Target (A4T) unterstützt:
   * averagevisitdepth
   * Bots
* Die folgenden Metriken werden nicht mehr unterstützt und beim ersten Ändern einer Aktivität, die die Metrik enthält, automatisch in neue Versionen der Metrik konvertiert:

   | Veraltete Metrik | Neue Metrik |
   |--- |--- |
   | `averagetimespentonpage` | `averagetimespentonsite` (Hinweis: gemessen in Minuten statt in Sekunden) |
   | `instances` | `occurrences` |
   | `singleaccess` | `singlepagevisits` |
   | `uniquevisitors` | `visitors` |
   | `visitorsdaily`, `visitorshourly`, `visitorsmonthly`, `visitorsquarterly`, `visitorsweekly`, `visitorsyearly` | `visitors` |

## Adobe Experience Cloud-Navigation (22. Februar 2019)

* Wenn Sie sich bei der [!DNL Adobe Experience Cloud]Seite anmelden, werden Sie zur neuen Kopfzeilennavigation geleitet. Es sieht sehr ähnlich wie die vorherige Navigation mit der schwarzen Leiste oben aus, bietet jedoch die folgenden Verbesserungen:

   * Einfacherer Wechsel zwischen [!DNL Identity Management System] (IMS-)Organisationen oder zu einer anderen Lösung.
   * Verbesserte Benutzerhilfe: Zu den Suchergebnissen gehören die Ergebnisse der [!DNL Target] Produktdokumentation sowie Community-Foren und weitere Videoinhalte, sodass Sie leichter auf weitere Inhalte zugreifen können, um das Beste zu erzielen [!DNL Target]. Wir haben auch einen Feedback-Mechanismus direkt im Menü [!UICONTROL Hilfe] hinzugefügt, der es einfacher macht, Probleme zu melden oder Ideen auszutauschen.

   * Verbesserte Feedback-Funktion für Net Promoter Score (NPS), sodass der Umfragemodus Ihren Arbeitsablauf nicht stört.
   * Verbesserter Anmeldefluss. Bisher wurden alle [!DNL Target] Kunden auf der Target-Einstiegsseite gelandet, nachdem sie auf das [!DNL Target] Symbol in der Kopfzeile geklickt hatten. Auf dieser Seite konnten Kunden dann fortfahren, [!DNL Target Standard/Premium], [!DNL Search&Promote]oder [!DNL Recommendations Classic], wie unten dargestellt:

      ![Landingpage](/help/r-release-notes/assets/landing.png)

      Wir haben diese Landingpage für alle unsere Kunden eliminiert. Sie gelangen jetzt immer direkt zur Seite &quot; [!UICONTROL Aktivitätenliste] &quot;, indem Sie auf das [!DNL Target] Symbol in der neuen Kopfzeile der Navigationsleiste klicken.

      Wenn Sie [!DNL Recommendations Classic]diese verwenden, können Sie entweder direkt zur Lösung wechseln oder über den Kurzlink, der auf der Registerkarte &quot; [!UICONTROL Recommendations] &quot;erstellt wurde, wie nachfolgend gezeigt:

      ![Recs Classic Deep-Link](/help/r-release-notes/assets/recs-classic.png)

      Wenn Sie [!DNL Search&Promote]diese verwenden, müssen Sie direkt zur [Search&amp;Promote-URL](https://center.atomz.com/center/?ims=1) (https://center.atomz.com/center/?ims=1) wechseln. Der Pfad, der von innen [!DNL Search&Promote] von [!DNL Adobe Target] zu erreichen ist, wurde vollständig entfernt.

   * Benachrichtigungen für [!DNL Target] sind derzeit nicht in der Dropdown-Liste &quot; [!UICONTROL Benachrichtigungen] &quot;in der Kopfzeile verfügbar.
   >[!NOTE]
   >
   >Bei der Einführung der neuen Navigationsleiste werden Sie auch einige URL-Änderungen feststellen. Alle vorherigen mit Lesezeichen versehenen Links funktionieren weiterhin, aber wir empfehlen Ihnen, neue Links mit einem Lesezeichen zu versehen, um das Öffnen zu beschleunigen.

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Versionshinweise - Target-serverseitige APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu den serverseitigen APIs von Adobe Target. |
| [Versionshinweise - SDK für Target Node.js](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Adobe Target-SDK Node.js. |
| [Versionshinweise - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Versionshinweise zum Java-SDK von Adobe Target. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der JavaScript-Bibliothek von Adobe Target &quot;at.js&quot;. |
| [„mbox.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.<br>Beachten Sie, dass die Bibliothek &quot;mbox.js&quot;nicht mehr entwickelt wird. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter [Experience Cloud-Versionshinweise](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
