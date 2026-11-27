---
keywords: Targeting;Visual Experience Composer;VEC;Fehlerbehebung bei Visual Experience Composer;Fehlerbehebung;TLS;TLS 1.2
description: Erfahren Sie, wie Sie Probleme im [!UICONTROL Visual Experience Composer] (VEC) beheben.
title: Wie behebe ich Probleme mit dem [!UICONTROL Visual Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
TQID: 'https://experienceleague.adobe.com/VNkydzzU-WRRAL0pqQPOs-sKrY8a6DS5Go764UGh0Hs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 4%
---
# Beheben von Problemen mit [!UICONTROL Visual Experience Composer] {#vec-issues}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie die Probleme beheben, die nur den **[!UICONTROL Visual Experience Composer]** (VEC) betreffen.

>[!ENDSHADEBOX]

In Visual Experience Composer (VEC[!DNL Adobe Target] treten unter bestimmten Bedingungen manchmal **[!UICONTROL auf]** um Probleme anzuzeigen. In den folgenden Elementen werden die Probleme beschrieben, die nur den VEC betreffen, und wie diese behoben werden.

+++ Die [!DNL Target] werden beim Öffnen der Website in Visual Experience Composer nicht geladen

Wenn eine Website im **[!UICONTROL Visual Experience Composer]** geöffnet wird, fügt [!DNL Target] die Parameter `mboxEdit=1` und `mboxDisable=1` zur URL hinzu.

Wenn eine Website, insbesondere eine Einzelseiten-App, diese Parameter zuschneidet oder entfernt, während sie ohne erneutes Laden von Seiten von einer Seite zur anderen navigiert, funktioniert die [!DNL Target] nicht, und die [!DNL Target] Bibliotheken werden nicht geladen. Um dieses Problem zu vermeiden, behalten Sie beide Parameter in der URL bei.

+++

+++ In Visual Experience Composer wird eine Seite nicht geöffnet oder langsam geladen, oder Aktivitäten und Erlebnisse werden in Visual Experience Composer nur langsam geladen

Mehrere Probleme können die Seitenleistung in [!DNL Target] Experience Composers beeinträchtigen. Die häufigsten sind die folgenden:

* Die Seite hat keine Mbox.
* Die Site verwendet die Proxy-Blockierung, wodurch verhindert wird, dass die Seite in Experience Composer geöffnet wird.
* Die Site erlaubt es nicht, sich in einem iFrame zu öffnen.

Wenn ein Problem im **[!UICONTROL Enhanced Experience Composer]** auftritt, deaktivieren Sie es und verwenden Sie stattdessen **[!UICONTROL Visual Experience Composer]**. Wechseln Sie dazu zu **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und deaktivieren Sie die Option **[!UICONTROL Enhanced Experience Composer aktivieren]**.

Die folgende Fehlermeldung kann in der Konsole angezeigt werden:

![Fehlermeldung der Browser-Konsole, dass die Anzeige der Seite in einem Frame abgelehnt wurde, da X-Frame-Options auf SAMEORIGIN gesetzt ist](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Wenn keiner der Composer funktioniert, ermöglicht eine Browser-Erweiterung, die die Kopfzeile „X-Frame-Options“ der Site überschreibt, z. B. &quot;[!DNL Requestly]&quot; ([!DNL Chrome] oder &quot;[!DNL Firefox]„) oder „Modify Response Headers“ ([!DNL Firefox]), das Laden der Site in iFrames und aktiviert so den VEC. Wenn Browser-Erweiterungen nicht verwendet werden können, verwenden Sie [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md). Zusätzlich zu den nachfolgenden Verfahren kann auch [[!DNL Adobe Target] **[!UICONTROL &#x200B; Erweiterung &#x200B;]**&#x200B;Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) für [!DNL Google Chrome] verwendet werden.

>[!NOTE]
>
>Diese Erweiterungen sind nur für die VEC-Bearbeitung vorgesehen.
>
>Führen Sie mit [!DNL Requestly] immer dann, wenn Kopfzeilen entfernt werden müssen, einen der folgenden Schritte aus:
>
>* Fügen Sie URL-Regeln für die URL hinzu, die in Visual Experience Composer geöffnet werden soll, sodass Header nur für diese URLs entfernt werden.
>* Aktivieren Sie die Regel während der Bearbeitung im VEC und deaktivieren Sie die Regel, wenn der VEC nicht verwendet wird.
>
>Bei **[!UICONTROL Modify Response Headers]** ([!DNL Firefox]) sind keine URL-Regeln verfügbar, sodass die Regel während der Bearbeitung im VEC aktiviert und deaktiviert werden muss, wenn der VEC nicht verwendet wird.

Sobald eine Erweiterung eingerichtet ist, werden Seiten in **[!UICONTROL Visual Experience Composer]** geladen, selbst wenn **[!UICONTROL Enhanced Experience Composer]** deaktiviert ist.

+++

+++ Entfernen Sie die Kopfzeile X-Frame-Options mit Requestly (Chrome oder Firefox)

1. Deaktivieren Sie den **[!UICONTROL Enhanced Experience Composer]**.
1. Installieren Sie die [!DNL Requestly] Browser-Erweiterung auf [!DNL Chrome] oder [!DNL Firefox].
1. Öffnen Sie die Erweiterung und wählen Sie **[!UICONTROL Kopfzeilen ändern]** aus.
1. Geben Sie einen Regelnamen ein.
1. Erstellen Sie in den Änderungsregeln eine Regel, die die Kopfzeile entfernt:

   * Ändern Sie **[!UICONTROL Hinzufügen]** zu **[!UICONTROL Entfernen]**.
   * Ändern Sie **[!UICONTROL Anforderung]** zu **[!UICONTROL Antwort]**.
   * Geben Sie „X-Frame-Options“ als Kopfzeilenname ein.

1. Wiederholen Sie den vorherigen Schritt und geben Sie „x-frame-options“ als Kopfzeilennamen ein.

   >[!NOTE]
   >
   >Bei Kopfzeilen, die mit [!DNL Requestly] bearbeitet werden, wird zwischen Groß- und Kleinschreibung unterschieden.

1. Ändern Sie **[!UICONTROL Gleich]** in **[!UICONTROL Enthält]** als Bedingung für die Quell-URL und geben Sie die URL der Aktivität ein, die in den VEC geladen werden soll.

   ![Requestly-Regel namens Umgehen von iframe-Busting-Code, die den Antwort-Header „X-Frame-Options“ für URLs mit „adobe.com“ entfernt](assets/chrome_extension.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Requestly-Regel, die die Antwort-Header „X-FRAME-OPTIONS“ und „X-FRAME-OPTIONS“ für alle URLs entfernt](assets/requestly.png)

Die Seite sollte jetzt schnell in „Visual **[!UICONTROL Composer“ geladen]**.

+++

+++ Entfernen der Kopfzeile „X-Frame-Options“ mit Antwort-Headern ändern (Firefox)

1. Installieren Sie die [!DNL Modify Response Headers]-Erweiterung auf [!DNL Firefox] und starten Sie den Browser neu.
1. Wählen Sie in den [!DNL Firefox] Erweiterungen die [!DNL Modify Response Headers] Erweiterung aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen]**.
1. Wählen **[!UICONTROL Filter]** aus der Dropdown **[!UICONTROL Liste]** Aktion“ aus.
1. Geben Sie **[!UICONTROL Feld Kopfzeilenname]** &quot;**[!UICONTROL -Frame-Options“]**.
1. Wiederholen Sie die vorherigen beiden Schritte, um einen Filter mit **[!UICONTROL x-frame-options“]**.
1. Klicken Sie auf **[!UICONTROL Hinzufügen]**.
1. Klicken Sie auf **[!UICONTROL Start]**.

![Ändern des Fensters „Antwort-Header“ in Firefox mit einem Filter für die X-Frame-Options-Kopfzeile, die als aktiviert angezeigt wird](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

+++

+++ In VEC wird keine Seite angezeigt

Überprüfen Sie die folgenden Ursachen:

* **Erweiterungsversion:** neueste Version der Erweiterung [[!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper &#x200B;]**&#x200B;bietet &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) beste Kompatibilität mit VEC. Um die installierte Version zu überprüfen, gehen Sie zu&#x200B;**[!UICONTROL &#x200B; Erweiterungen &#x200B;]**>**[!UICONTROL &#x200B; Erweiterungen verwalten &#x200B;]**&#x200B;und klicken Sie dann auf&#x200B;**[!UICONTROL &#x200B; Details &#x200B;]**.
* **Autorenbibliotheken:** VEC Autorenbibliotheken benötigt, um die Web-Seite zu ändern. Sie sind in die at.js-Bibliothek eingebettet, die die Erweiterung jedes Mal von [!DNL Adobe]-Servern herunterlädt, wenn VEC verwendet wird, unabhängig davon, ob at.js oder das [!DNL Adobe Experience Platform Web SDK] bereits auf der Seite vorhanden ist. Überprüfen Sie, ob die at.js-Header, die in **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** konfiguriert sind, keine ungültigen Änderungen enthalten.
* **Blockierte Anfragen:** Die Seite darf die Anforderungen, die zum Laden erforderlich sind, wenn sie in einen iFrame eingebettet ist, nicht blockieren. Zu diesen Sperren gehören `frame-ancestors` CSP-Anweisungen, benutzerdefinierter JavaScript-Code in der Website, Meta-HTML-Tags und der `x-frame-options`-Header.
* **Reservierte Dateinamen:** der JavaScript der Seite darf die Authoring-Bibliotheken nicht beeinträchtigen. Verwenden oder schließen Sie keine Dateien mit den folgenden reservierten Namen ein:

  * `target-vec-helper.js`
  * `target-vec.js`
  * `target.js`
  * `admin.css`
  * `sizzle.js`
  * `mixContentCheck.html`

  Das versehentliche Überschreiben von Variablen oder Ereignissen, die in diesen Dateien definiert sind, kann ebenfalls zu Problemen mit dem VEC führen.

* **Nicht sichere Seite auf einer sicheren Website:** Browser blockiert die Seite. Klicken Sie links neben der URL in der Adressleiste auf das Symbol und dann auf **[!UICONTROL Schutz auf dieser Seite deaktivieren]**.
* **Ungültige URL:** eingegebene URL ist ungültig.
* **Cookies:** wenn die Website nicht in VEC geladen werden kann oder sich unerwartet verhält, kann das Problem behoben werden, indem die Cookies im Browser akzeptiert werden, bevor die Website in geladen [!DNL Target].

+++

+++ Der VEC scheint im Durchsuchen-Modus fehlerhaft zu sein

Im **[!UICONTROL Durchsuchen]**-Modus scheint der VEC fehlerhaft zu sein, wenn eine URL geöffnet wird, der die [!DNL Target] Bibliotheken ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=de){target=_blank} oder [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}) fehlen oder die eine Frame-Buster-Kopfzeile enthält. Aus Gründen der Browser-Sicherheit können [!DNL Target] nicht ordnungsgemäß auf die URL zugreifen, zu der navigiert wurde, oder die VEC-URL wird beim Laden der Seite nicht konsistent aktualisiert.

Der VEC lädt die Web-Seite in einem `<iframe>`, und die aktuellen Sicherheitsmechanismen von Browsern verhindern, dass die [!DNL Target]-Benutzeroberfläche unter der Richtlinie „Gleicher Ursprung“ auf die Elemente des Rahmens zugreift. Browser blockieren Skripte, die versuchen, auf einen Frame mit einem anderen Ursprung zuzugreifen, einschließlich Informationen wie `location.href`.

Verwenden Sie die neue [Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)-Erweiterung, um die [!DNL Target]-Bibliothek in die Seiten einzufügen, damit die Seiten optimal durchsucht werden können.

+++

+++ Probleme werden durch CSS-Konflikte in VEC verursacht

Überprüfen Sie, ob CSS-Dateien die Sichtbarkeit beeinflussen, während die Seite im Editor geladen wird. Beispielsweise kann die `overflow: hidden`-Eigenschaft im Seitentext zu Scroll-Problemen oder Trigger-Klickereignissen führen, die das Authoring-Menü beeinträchtigen.

+++
