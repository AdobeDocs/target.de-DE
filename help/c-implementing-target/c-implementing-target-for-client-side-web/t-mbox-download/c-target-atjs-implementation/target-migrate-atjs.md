---
keywords: Target;at.js;migrate to at.js;readiness;audit at.js;integrate at.js
description: Die Migration von „mbox.js“ zu „at.js“ ist ein unkomplizierter Vorgang.
title: Migration von „mbox.js“ zu „at.js“
feature: null
topic: Standard
uuid: 45f81fe8-7b04-4a36-931d-bbf03ed6cbb3
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 99%

---


# Migration von „mbox.js“ zu „at.js“{#how-to-migrate-to-at-js-from-mbox-js}.

Die Migration von mbox.js zu at.js in [!DNL Adobe Target] ist ein unkomplizierter Vorgang.

Gehen Sie wie folgt vor, um eine Migration von [!DNL mbox.js] zu [!DNL at.js] durchzuführen und sie zu prüfen:

1. Finden Sie heraus, welche Anforderungen an die [Browserunterstützung](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100) in Ihrem Unternehmen vorliegen.
1. Prüfen Sie die aktuelle [!DNL mbox.js]-Implementierung auf Ihrer Website auf Funktionen, die von [!DNL at.js] nicht unterstützt werden.

   Sie sollten bei der Prüfung Ihrer Implementierung auf Folgendes achten:

   **Welche Typen von Mboxes verwenden Sie momentan?**

   | Typ | Details |
   |--- |--- |
   | Automatisch erstellte globale mbox | Die automatisch erstellte globale Mbox wird erstellt, wenn die einzige Zeile an Target-Code auf Ihrer Website die Datei „mbox.js“ ist. Diese Datei generiert automatisch einen Mbox-Aufruf. |
   | Globale, leere mboxCreate | Wir empfehlen, zu der automatisch erstellten globalen Mbox zu wechseln. |
   | Wrapper-mboxCreate | Die Migration sollte einfach sein, solange vor `mboxCreate()` bei Ihnen `<div class="mboxDefault"></div>` steht. |
   | mboxUpdate | Die Migration sollte ebenfalls einfach sein, wenn  `mboxUpdate()` zusammen mit `mboxDefine()` oder `mboxCreate()` verwendet wird. `mboxUpdate()` aktualisiert die automatisch erstellte globale Mbox oder eine Mbox, die von `getOffer()` erstellt wurde, nicht. Unter diesen Umständen sollte eine Kombination aus `getOffer()` und `applyOffer()` verwendet werden, um `mboxUpdate()` bei der Migration zu at.js zu ersetzen. |
   | Benutzerdefinierte Klick-Tracking-Mboxes, einschließlich „mboxTrack“ | Wir empfehlen Ihnen, Code für die Verwendung des Folgenden zu aktualisieren:  `trackEvent()`. |

   >[!NOTE]
   >
   >Weitere Informationen zu den verschiedenen Funktionen in der obigen Tabelle finden Sie unter [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

   **Haben Sie Ihre [!DNL mbox.js]-Datei auf beliebige Art und Weise angepasst?**

   * mboxParameters()
   * mboxSupported()
   * mboxCookieDomain()
   * Extra Javascript
   * Andere Stellen

   Die meisten der [„mbox.js“-Objekte und -Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (z. B. `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` und andere) werden nicht unterstützt. Alternative Ansätze können Ihnen ebenfalls helfen, Ihr Ziel zu erreichen.

   **Befindet sich [!DNL mbox.js] auf all Ihren Webseiten?**

   Sie können [!DNL at.js] und [!DNL mbox.js] nicht auf derselben Webseite verwenden. Sie können jedoch zwei JavaScript-Bibliotheken auf zwei unterschiedlichen Seiten derselben Website verwenden.

   Das Mbox-Cookie ist das Hauptmittel, mit dem Adobe den Besucher von Seite zu Seite zuordnet. Im Zuge der Qualitätssicherung sollten Sie sicherstellen, dass das Cookie erhalten bleibt und korrekt gelesen wird, wenn sich der Besucher zwischen Seiten mit [!DNL at.js] und Seiten mit [!DNL mbox.js] hin- und herbewegt. Stellen Sie sicher, dass in den Mbox-Aufrufen dieselben Werte für `mboxPC` und `mboxSession` übergeben werden, unabhängig davon, in welchem Bereich der Site ([!DNL at.js] oder [!DNL mbox.js]) der Besucher zuerst ankommt und welcher Bereich das Cookie gesetzt hat. Wenn Sie in Ihrer Implementierung Cookies von Drittanbietern verwenden, stellen Sie sicher, dass diese Werte beim Durchsuchen der Site nicht verändert werden.

   **Integrieren Sie [!DNL Target] mit anderen Adobe-Lösungen?**

   * Analytics (A4T)
   * Analytics (ältere Integration)
   * AAM (Backend)
   * AAM (älteres Frondend)
   * AEM
   * Data Workbench

   Einige der älteren Integrationen werden von [!DNL at.js] nicht unterstützt. Weitere Informationen finden Sie auf der Seite [Integrationen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39).

   **Integrieren Sie [!DNL Target] mit Drittanbieter-Tools?**

   * Andere Analysetools
   * Andere DMPs
   * Demandbase
   * ClickTale
   * Sonstige

   Diese müssen für den Einsatz mit [!DNL at.js] möglicherweise angepasst werden. Weitere Informationen finden Sie auf der Seite [Integrationen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39).

   **Verwenden Sie einen Tag-Manager?**

   * Dynamic Tag Management
   * Ensighten
   * Tealium
   * Signal/BrightTag

   Weitere Informationen finden Sie unter [„at.js“-Integrationen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39).

   >[!NOTE]
   >
   >Wenn Sie derzeit keinen Tag-Manager zur Bereitstellung von [!DNL Target] nutzen, ist jetzt ein guter Moment, darüber nachzudenken. Das [Dynamic Tag Management](https://dtm.adobe.com) von Adobe ist für [!DNL Target]-Kunden kostenlos und wird als Bereitstellungsoption für [!DNL Target] wärmstens empfohlen. Weitere Informationen finden Sie in den [Best Practices für die Implementierung von Adobe Target mit Dynamic Tag Management](https://experienceleague.adobe.com/docs/dtm/implementing/overview.html).

1. Stellen Sie sicher, dass alle Aktivitäten und Integrationen ordnungsgemäß funktionieren.

   Im Folgenden finden Sie ein paar Punkte, anhand derer Sie während des Tests überprüfen können, ob [!DNL at.js] erwartungsgemäß funktioniert:

   * Achten Sie darauf, dass alle Ihrer aktuellen Aktivitäten mit der neuen JavaScript-Bibliothek funktionieren.
   * Achten Sie darauf, dass alle erforderlichen  [Integrationen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) und [Plug-ins](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) funktionieren erwartungsgemäß.
   * Stellen Sie sicher, dass Sie die [Fehlerbehebung](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) mit den in [!DNL at.js] verfügbaren Ansätzen problemlos ausführen können.

**Mögliche Probleme bei der Migration zu at.js** Einige Kunden haben nach der Migration zu at.js die folgenden Probleme gemeldet:

* Einige VEC-Aktivitäten, die auf einer Seite mit [!DNL mbox.js] erstellt wurden, müssen möglicherweise aktualisiert werden, um mit [!DNL at.js] zu funktionieren.

   Dieses Problem tritt am häufigsten auf Websites auf, die nicht viele ID- oder Klassenattribute in HTML-Elementen verwenden. Sollte dieses Problem bei Ihnen auftreten, können Sie überprüfen, ob das Erlebnis wie erwartet bereitgestellt wird, indem Sie die Seite mit `?mboxDebug=true` laden und die Meldungen in der Konsole durchsehen.

   ![](assets/mboxdebug.png)In diesen Beispielen würden Elementselektoren vielleicht mit Folgendem starten:

   ```
   HTML > BODY > DIV:nth-of-type(2)
   ```

   Diese wurden unter der Annahme erstellt, dass von [!DNL mbox.js] ein zusätzliches `<div>`-Element zu Beginn der Seite hinzugefügt wird. Da [!DNL at.js] kein `<div>`-Element oben auf der Seite hinzufügt, würde dieser Selektor mit [!DNL at.js] nicht mehr funktionieren.

   Dieses Problem kann gelöst werden, indem man die Aktivität im VEC für die URL unter Verwendung von [!DNL at.js] neu erstellt, oder indem man den Selektor unter Verwendung der VEC-Option **[!UICONTROL &lt;/> Code]** > **[!UICONTROL Änderungen]** manuell aktualisiert.

   Zur Lösung dieses Problems sollten Sie von der n-ten Anzahl im ersten DIV-Element nach dem Körper 1 abziehen. Im oben gezeigten Beispiel sähe der überarbeitete Code wie folgt aus:

   ```
   HTML > BODY > DIV:nth-of-type(1)
   ```

   Weitere Informationen dazu, wie Sie den Code-Editor zu diesem Zweck einsetzen können, finden Sie unter  [Code-Editor](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5).

* Da nun alle Mboxes asynchron arbeiten, blockieren sie nicht das Rendern von Seiten und werden nicht in der Reihenfolge zurückgegeben, in der sie ausgelöst wurden. Weitere Informationen dazu finden Sie unter „Erwägungen für asynchrones Laden“ in  [Einschränkungen von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE).
