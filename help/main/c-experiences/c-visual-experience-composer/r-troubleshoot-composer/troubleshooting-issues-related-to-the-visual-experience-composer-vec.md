---
keywords: Targeting;Visual Experience Composer;VEC;Fehlerbehebung Visual Experience Composer;Fehlerbehebung;TLS;TLS 1.2
description: Erfahren Sie, wie Sie Probleme im VEC (0) beheben können.[!UICONTROL Visual Experience Composer]
title: Wie kann ich Probleme im Zusammenhang mit dem [!UICONTROL Visual Experience Composer] beheben?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: 7c0d0154b81fbd3f89a82b31cd18541a7f0ea1a7
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 24%

---

# Beheben von Problemen im Zusammenhang mit dem [!UICONTROL Visual Experience Composer]

Unter bestimmten Bedingungen treten im VEC (0} [!UICONTROL Visual Experience Composer]) manchmal Anzeigeprobleme auf.[!DNL Adobe Target]

## Wenn ich meine Website in der [!UICONTROL Visual Experience Composer] öffne, werden die [!DNL Target] -Bibliotheken nicht geladen. (Nur VEC)   {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

[!DNL Target] fügt zwei Parameter (`mboxEdit=1` und `mboxDisable=1`) hinzu, während die Website im [!UICONTROL Visual Experience Composer] geöffnet wird.

Wenn Ihre Website (insbesondere Einzelseiten-Apps) Parameter beschneidet oder beim Navigieren von einer Seite zur anderen entfernt (ohne dass die Seite neu geladen wird), wird die [!DNL Target] -Funktionalität nicht mehr genutzt und die [!DNL Target] -Bibliotheken werden nicht geladen.

Stellen Sie zur Vermeidung dieses Problems sicher, dass Sie diese beiden Parameter nicht beschneiden oder entfernen.

## Meine Seite wird im EEC nicht geöffnet oder nur langsam geladen. Aktivitäten oder Erlebnisse werden im VEC langsam geladen. (Nur VEC)   {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Verschiedene Probleme können sich auf die Seitenleistung in den Erlebnis-Composern für [!UICONTROL Target] auswirken. Im Folgenden finden Sie einige gängige Gründe:

* Es befindet sich keine Mbox auf der Seite.
* Ihre Website nutzt Proxy-Sperren, wodurch die Seite in keiner Version von Experience Composer geöffnet werden kann.
* Ihre Website verhindert, dass Sie in einem iFrame geöffnet wird.

Wenn Probleme in der [!UICONTROL Enhanced Experience Composer] auftreten, versuchen Sie, die [!UICONTROL Enhanced Experience Composer] zu deaktivieren und stattdessen die [!UICONTROL Visual Experience Composer] zu verwenden.

Um die [!UICONTROL Enhanced Experience Composer] zu deaktivieren, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und deaktivieren Sie die Option **[!UICONTROL Enable Enhanced Experience Composer]**.

Bei einigen Benutzern wird in der Konsole die folgende Fehlermeldung angezeigt:

![Konsole-Fehlermeldung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Wenn weder das [!UICONTROL Visual Experience Composer] noch das [!UICONTROL Enhanced Experience Composer] funktioniert, verwenden Sie eine Browser-Erweiterung wie [!DNL Requestly] ([!DNL Chrome] oder [!DNL Firefox]) oder Modify Response Headers (Firefox), die die X-Frames-Kopfzeilenoptionen für Ihre Site überschreiben und das Laden in iFrames ermöglichen kann, wodurch VEC aktiviert wird. Wenn Sie keine Browsererweiterungen verwenden können, verwenden Sie den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie die Erweiterung [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper] ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) für [!DNL Google Chrome] verwenden.


>[!NOTE]
>
>Diese Plug-ins sollten nur bei der VEC-Bearbeitung verwendet werden.
>
>Wenn Sie Kopfzeilen für die Erweiterung [!DNL Requestly] entfernen müssen, sollten Sie einen der folgenden Schritte ausführen:
>
>* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
>
>* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.
>
>Da Sie für die Erweiterung [!UICONTROL Modify Response Header] ([!DNL Firefox]) keine URL-Regel hinzufügen können, müssen Sie Folgendes tun:
>
>* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.

**So verwenden Sie die [!DNL Requestly]-Erweiterung für [!DNL Chrome] oder [!DNL Firefox]:**

1. Deaktivieren Sie die [!UICONTROL Enhanced Experienced Composer].
1. Installieren Sie die Browsererweiterung [!DNL Requestly] für [!DNL Chrome] oder [!DNL Firefox].
1. Öffnen Sie die Erweiterung und konfigurieren Sie sie wie folgt:
1. Wählen Sie **[!UICONTROL Modify headers]** aus.
1. Geben Sie Folgendes ein:

   * Regelname
   * Änderungsregeln

      * Schaltet **[!UICONTROL Add]** auf **[!UICONTROL Remove]** um.
      * Schaltet **[!UICONTROL Request]** auf **[!UICONTROL Response]** um.
      * Geben Sie „X-Frame-Options“ als Kopfzeilenname ein.
      * Wiederholen Sie die vorherigen Schritte und geben Sie „x-frame-options“ als Header-Namen ein.

        >[!NOTE]
        >
        >Bei Kopfzeilen, die über [!DNL Requestly] bearbeitet werden, wird zwischen Groß- und Kleinschreibung unterschieden.

      * Ändern Sie **[!UICONTROL Equals]** in **[!UICONTROL Contains]** als Bedingung für die Quell-URL und geben Sie die URL der Aktivität ein, die Sie in VEC laden möchten.

     ![Chrome_extension image](assets/chrome_extension.png)

1. Klicken Sie auf **[!UICONTROL Save]**.

   ![requestly image](assets/requestly.png)

   Sie sollten jetzt in der Lage sein, die Seite schnell mit dem [!UICONTROL Visual Experience Composer] zu laden.

**So verwenden Sie die [!DNL Modify Response Headers]-Erweiterung für [!UICONTROL Firefox]:**

1. Installieren Sie die [!UICONTROL Modify Response Headers] auf [!DNL Firefox] und starten Sie den Browser neu.
1. Wählen Sie in Ihren [!DNL Firefox] -Erweiterungen die Erweiterung &quot;Modify Response Headers&quot;aus.
1. Klicken Sie auf **[!UICONTROL Preferences]**.
1. Wählen Sie **[!UICONTROL Filter]** aus der Dropdownliste [!UICONTROL Action] aus.
1. Geben Sie im Feld [!UICONTROL Header Name] Folgendes ein: **[!UICONTROL X-Frame-Options]**.
1. Wiederholen Sie die Schritte 4 und 5, um einen Filter mit **[!UICONTROL x-frame-options]** hinzuzufügen.
1. Klicken Sie auf **[!UICONTROL Add]**.
1. Klicken Sie auf **[!UICONTROL Start]**.

![Firefox-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

Öffnen Sie nach dem Einrichten einer Erweiterung [!DNL Target]. Ihre Seiten sollten jetzt im [!UICONTROL Visual Experience Composer] geladen werden, selbst wenn der [!UICONTROL Enhanced Experience Composer] deaktiviert ist.

## Meine Seite wird im VEC nicht angezeigt (nur VEC)  {#does-not-load}

* Die beste Kompatibilität mit VEC wird durch die neueste Version der Erweiterung sichergestellt: [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

  Um zu überprüfen, ob Sie die neueste Version verwenden, gehen Sie zu [!UICONTROL Extensions] > [!UICONTROL Manage Extensions] und klicken Sie dann auf [!UICONTROL Details].

* Die [!UICONTROL Visual Experience Composer] erfordert Authoring-Bibliotheken, um Änderungen auf der Webseite vorzunehmen. Diese Bibliotheken sind in die at.js-Bibliothek eingebettet und werden von der Erweiterung bei jeder Verwendung von VEC von den [!DNL Adobe] -Servern heruntergeladen.

  Die Erweiterung lädt die at.js-Bibliothek herunter, unabhängig davon, ob at.js oder [!DNL Adobe Experience Platform Web SDK] bereits auf der Seite enthalten sind.

  Stellen Sie sicher, dass den im Abschnitt [!UICONTROL Administration] > [!UICONTROL Implementation] konfigurierten at.js-Headern keine ungültigen Änderungen hinzugefügt wurden.

* Stellen Sie sicher, dass die Web-Seite keine Anforderungen blockiert, die zum Laden erforderlich sind, wenn sie in einen iFrame eingebettet wird. Dazu gehören die Verwendung von CSP-Direktiven von Frame-Vorgängern oder benutzerdefiniertem JS-Code, der in die Kundenwebsite eingebettet ist, Meta-HTML-Tags oder die Kopfzeile für X-Frame-Optionen.

* Stellen Sie sicher, dass das JavaScript der Web-Seite nicht in die Authoring-Bibliotheken eingreift. Verwenden oder schließen Sie keine Dateien mit den folgenden reservierten Namen ein:

   * `target-vec-helper.js`
   * `target-vec.js`
   * `target.js`
   * `admin.css`
   * `sizzle.js`
   * `mixContentCheck.html`

     Darüber hinaus kann das versehentliche Überschreiben von Variablen oder Ereignissen, die in diesen Dateien definiert sind, zu Problemen mit VEC führen.

* Der Browser blockiert eine nicht sichere Seite auf einer sicheren Site.

  Klicken Sie auf das Symbol links neben der URL in der Browser-Adressleiste und klicken Sie auf **[!UICONTROL Disable protection on this page]**

* Sie haben eine ungültige URL eingegeben.
* Wenn Ihre Website im VEC nicht geladen werden kann oder sich unerwartet verhält, besteht die Möglichkeit, Cookies auf Ihrer Website im Browser zu akzeptieren, bevor versucht wird, die Website in [!DNL Target] zu laden.

## Bei der Verwendung des Modus zum Durchsuchen scheint der VEC nicht zu funktionieren. (Nur VEC)   {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

Wenn Sie im Durchsuchen-Modus auf eine URL zugreifen, für die keine [!DNL Target] Bibliotheken implementiert sind ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=de){target=_blank} oder [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}) oder die eine Header mit Frame-Buster enthält, scheint der VEC beschädigt zu sein. Aus Sicherheitsgründen des Browsers kann [!DNL Target] nicht ordnungsgemäß auf die URL zugreifen, zu der Sie navigiert sind, oder die VEC-URL wird nicht konsistent aktualisiert, wenn die Seite geladen wird.

Dieses Problem tritt auf, weil VEC die Webseite in einen `<iframe>` lädt. Die aktuellen Sicherheitsmechanismen von Browsern verhindern, dass die Benutzeroberfläche von [!DNL Target] aufgrund der gleichen Ursprungsrichtlinie auf die Elemente des angegebenen Rahmens zugreift. Browser blockieren Skripte, die versuchen, auf einen Frame mit einer anderen Herkunft zuzugreifen, und die Informationen wie den `location.href` enthalten.

Sie müssen die neue Erweiterung [Visual Editing Helper Extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) (empfohlen) oder die [alte Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) verwenden, um die Bibliothek [!DNL Target] in die Seiten einzufügen, damit Sie sie optimal durchsuchen können.

## Probleme aufgrund von CSS-Konflikten in [!UICONTROL Visual Experience Composer]

Überprüfen Sie, ob CSS-Dateien vorhanden sind, die sich auf die Sichtbarkeit beim Laden der Webseite im Editor auswirken können. Beispielsweise kann die Verwendung der Eigenschaft `overflow: hidden` im Seitentext zu Problemen beim Scrollen oder zu Trigger-Klick-Ereignissen führen, die das Menü für die Bearbeitung beeinträchtigen könnten.
