---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 322b14629d420601b763fed7597c43a8458b7dbf
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 28%

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Target-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;in Würde fehl und wirken sich auf die Seiten aus, auf denen Target-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie die Datei &quot;mbox.js&quot;in Adobe Target zu &quot;at.js&quot;](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.
   >
   >
* **Target-Mitteilungen**: Auf der Seite &quot;Ankündigungen zum Target&quot;finden Sie Informationen zu kommenden Ereignissen, einschließlich Target Skill Builder-Sitzungen, Entwicklerchats, Webinars und Target Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Target-Mitteilungen](/help/r-release-notes/target-announcements.md).


Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Standard/Premium 20.5.1 (17. Juni 2020) 

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Analytics for Target (A4T) Unterstützung für [!UICONTROL Aktivitäten mit automatisierter Zuordnung] | [!UICONTROL Aktivitäten mit automatisierter Zuordnung] unterstützen jetzt [Analytics zum Target](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Diese Integration ermöglicht Ihnen die Verwendung der [!UICONTROL Funktion &quot;Automatisierte Zuordnung] von Multi-Armed Bandit&quot;, um Traffic zu erfolgreichsten Erlebnissen zu steigern, während Sie eine [!UICONTROL Adobe Analytics] -Zielmetrik und/oder Funktionen für den Berichte und die Analyse von [!UICONTROL Adobe Analytics] verwenden.<br>Wenn Sie bereits A4T [für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben, sind Sie alle bereit!<br>Weitere Informationen finden Sie unter Unterstützung von [Analytics für Target (A4T) für Aktivitäten](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) mit automatisierter Zuordnung bei der Erstellung von *Aktivitäten*. |
| Antwort-Token für die Traffic-Zuordnungsmethode für Aktivitäten mit automatischem Target und automatisierter Personalisierung | Zwei [Antworttokens](/help/administrating-target/response-tokens.md) wurden zu den Aktivitäten [!UICONTROL Automatisches Target] und [!UICONTROL Automatisierte Personalisierung] hinzugefügt, um festzustellen, ob ein Besucher ein bestimmtes Erlebnis erhalten hat, weil ihm &quot;Steuerung&quot;oder &quot;zielgerichteter&quot;Traffic zugewiesen wurde.<ul><li>`experience.trafficAllocationId` gibt 0 zurück, wenn ein Besucher ein Erlebnis aus dem Traffic &quot;Kontrolle&quot;erhalten hat, und 1, wenn ein Besucher ein Erlebnis aus der &quot;gezielten&quot;Traffic-Verteilung erhalten hat.</li><li>`experience.trafficAllocationType` gibt &quot;Kontrolle&quot;oder &quot;Targeting&quot;zurück.</li></ul>Weitere Informationen zu Kontroll- und zielgerichtetem Traffic finden Sie unter [Auswählen des Steuerelements für Ihre automatisierte Personalisierung oder Auto-Target-Aktivität](/help/c-activities/t-automated-personalization/experience-as-control.md). |
| [!UICONTROL Herausgeberrolle] | Diese neue Rolle ähnelt der aktuellen [!UICONTROL Beobachterrolle] (Aktivitäten können zwar Ansicht, aber nicht erstellt oder bearbeitet werden). Die [!UICONTROL Herausgeberrolle] verfügt jedoch über die zusätzliche Berechtigung zum Aktivieren von Aktivitäten.<br>Weitere Informationen finden Sie unter: <ul><li>**Target Standard-Benutzer**: [Legen Sie Rollen und Berechtigungen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Benutzern* fest.</li><li>**Target Premium-Nutzer**: [Schritt 6: Legen Sie Rollen und Berechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) unter *Unternehmensberechtigungen* konfigurieren fest.</li></ul> |
| A4T-Unterstützung am 25. [!DNL Analysis Workspace]<br>Juni 2020 | [!UICONTROL Analytics für Target] (A4T) wird jetzt in unterstützt [!DNL Analysis Workspace]. Im Bedienfeld [!UICONTROL &quot;] Analytics für Target (A4T)&quot;können Sie Ihre [!DNL Adobe Target] Aktivitäten und Erlebnisse in analysieren [!DNL Analysis Workspace].<br>Weitere Informationen finden Sie unter [Berichte in Analytics](/help/c-integrating-target-with-mac/a4t/reporting.md) im Bereich *A4T-Berichte* und [Analytics für Target (A4T) im](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics Tools-Handbuch **. |

### Verbesserungen, Korrekturen von Problemen und Änderungen

* Es wurde ein Fehler behoben, der dazu führte, dass die Metrik &quot;Besucher&quot;in der Definition der Aktivität statt &quot;UniqueVisitors&quot;gespeichert wurde. (TGT-37098)
* Es wurde ein Fehler in der [!DNL Target] Benutzeroberfläche behoben, der dazu führte, dass die vertikale Bildlaufleiste auf der Seite &quot; [!UICONTROL Audiencen] &quot;nicht korrekt funktionierte. (TGT-36968)

## Versionen von &quot;at.js&quot;1.8.2 und &quot;at.js 2.3.1&quot;(15. Juni 2020)

Die folgenden Verbesserungen und Fehlerbehebungen wurden in den [!DNL Target] at.js-Bibliotheken vorgenommen:

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| at.js  1.8.2 | Diese Version von at.js ist ein Maintenance Release und beinhaltet die folgende Fehlerbehebung:<ul><li>Es wurde ein Problem bei der Verwendung von CNAME und Edge Override von at.js 1 behoben.*x* erstellt die Serverdomäne möglicherweise falsch, was dazu führte, dass die [!DNL Target] Anforderung fehlschlug. (TNT-35064)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| at.js 2.3.1 | Diese Version von at.js ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:<ul><li>Die `deviceIdLifetime` Einstellung wurde über [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)überschrieben. (TNT-36349)</li><li>Es wurde ein Problem bei der Verwendung von CNAME und Edge Override von at.js 2 behoben.*x* erstellt die Serverdomäne möglicherweise falsch, was dazu führte, dass die [!DNL Target] Anforderung fehlschlug. (TNT-35065)</li><li>Es wurde ein Problem behoben, das bei Verwendung der [!DNL Target] Erweiterung [!DNL Launch] v2 und der [!DNL Adobe Analytics] Erweiterung [!DNL Launch] den [!DNL Target][!DNL Analytics] `sendBeacon` Aufruf verzögerte. (TNT-36407, TNT-35990, TNT-36000)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Versionshinweise - serverseitige APIs für Targets](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu den serverseitigen APIs von Adobe Target. |
| [Versionshinweise - Target Node.js-SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Node.js-SDK von Adobe Target. |
| [Versionshinweise - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Versionshinweise zum Java-SDK von Adobe Target. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der JavaScript-Bibliothek &quot;at.js&quot;des Adobe Targets. |
| [„mbox.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.<br>Beachten Sie, dass die Bibliothek &quot;mbox.js&quot;nicht mehr entwickelt wird. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu [Experience Cloud](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
