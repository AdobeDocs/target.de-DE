---
keywords: Targeting;Visual Experience Composer;VEC;Fehlerbehebung Visual Experience Composer;Fehlerbehebung;TLS;TLS 1.2
description: Erfahren Sie, wie Sie Probleme in der [!UICONTROL Visual Experience Composer] (VEC).
title: Wie behebe ich Probleme im Zusammenhang mit der [!UICONTROL Visual Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: 7c0d0154b81fbd3f89a82b31cd18541a7f0ea1a7
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 24%

---

# Beheben von Problemen im Zusammenhang mit [!UICONTROL Visual Experience Composer]

Anzeigeprobleme treten manchmal in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) unter bestimmten Bedingungen.

## Wenn ich meine Website in der [!UICONTROL Visual Experience Composer], die [!DNL Target] -Bibliotheken werden nicht geladen. (Nur VEC)   {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

[!DNL Target] fügt zwei Parameter (`mboxEdit=1` und `mboxDisable=1`) beim Öffnen der Website im [!UICONTROL Visual Experience Composer].

Wenn Ihre Website (insbesondere Einzelseiten-Apps) Parameter beschneidet oder beim Navigieren von einer Seite zur anderen (ohne Seitenneuladung) entfernt, wird die [!DNL Target] Funktionsunterbrechungen und [!DNL Target] -Bibliotheken werden nicht geladen.

Stellen Sie zur Vermeidung dieses Problems sicher, dass Sie diese beiden Parameter nicht beschneiden oder entfernen.

## Meine Seite wird im EEC nicht geöffnet oder nur langsam geladen. Aktivitäten oder Erlebnisse werden im VEC langsam geladen. (Nur VEC)   {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Verschiedene Probleme können sich auf die Seitenleistung in [!UICONTROL Target] Experience Composer. Im Folgenden finden Sie einige gängige Gründe:

* Es befindet sich keine Mbox auf der Seite.
* Ihre Website nutzt Proxy-Sperren, wodurch die Seite in keiner Version von Experience Composer geöffnet werden kann.
* Ihre Website verhindert, dass Sie in einem iFrame geöffnet wird.

Wenn Probleme im [!UICONTROL Enhanced Experience Composer], versuchen Sie, die [!UICONTROL Enhanced Experience Composer] und verwenden Sie [!UICONTROL Visual Experience Composer] anstatt.

So deaktivieren Sie die [!UICONTROL Enhanced Experience Composer], gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und deaktivieren Sie die **[!UICONTROL Enable Enhanced Experience Composer]** -Option.

Bei einigen Benutzern wird in der Konsole die folgende Fehlermeldung angezeigt:

![Konsole-Fehlermeldung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Wenn weder die [!UICONTROL Visual Experience Composer] und [!UICONTROL Enhanced Experience Composer] funktioniert, verwenden Sie eine Browser-Erweiterung wie [!DNL Requestly] ([!DNL Chrome] oder [!DNL Firefox]) oder Ändern von Antwortheadern (Firefox), die die X-Frames-Kopfzeilenoptionen für Ihre Site überschreiben können und es ihnen ermöglichen, in iFrames geladen zu werden, wodurch VEC aktiviert wird. Wenn Sie keine Browsererweiterungen verwenden können, verwenden Sie die [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie die [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper] Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) für [!DNL Google Chrome].


>[!NOTE]
>
>Diese Plug-ins sollten nur bei der VEC-Bearbeitung verwendet werden.
>
>Für [!DNL Requestly] -Erweiterung verwenden, sollten Sie bei Bedarf Kopfzeilen entfernen. Führen Sie dazu einen der folgenden Schritte aus:
>
>* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
>
>* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.
>
>Für [!UICONTROL Modify Response Header] Erweiterung ([!DNL Firefox]), da Sie keine URL-Regel hinzufügen können, müssen Sie Folgendes tun:
>
>* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.

**So verwenden Sie die [!DNL Requestly] Erweiterung auf [!DNL Chrome] oder [!DNL Firefox]:**

1. Deaktivieren Sie die [!UICONTROL Enhanced Experienced Composer].
1. Installieren Sie die [!DNL Requestly] Browsererweiterung in [!DNL Chrome] oder [!DNL Firefox].
1. Öffnen Sie die Erweiterung und konfigurieren Sie sie wie folgt:
1. Auswählen **[!UICONTROL Modify headers]**.
1. Geben Sie Folgendes ein:

   * Regelname
   * Änderungsregeln

      * Umschalten **[!UICONTROL Add]** nach **[!UICONTROL Remove]**.
      * Umschalten **[!UICONTROL Request]** nach **[!UICONTROL Response]**.
      * Geben Sie „X-Frame-Options“ als Kopfzeilenname ein.
      * Wiederholen Sie die vorherigen Schritte und geben Sie „x-frame-options“ als Header-Namen ein.

        >[!NOTE]
        >
        >Kopfzeilen, die über bearbeitet werden [!DNL Requestly] zwischen Groß- und Kleinschreibung unterscheiden.

      * Änderung **[!UICONTROL Equals]** nach **[!UICONTROL Contains]** als Bedingung für die Quell-URL und geben Sie die URL der Aktivität ein, die Sie in VEC laden möchten.

     ![Chrome_extension-Bild](assets/chrome_extension.png)

1. Klicken Sie auf **[!UICONTROL Save]**.

   ![Anforderungsbild](assets/requestly.png)

   Sie sollten die Seite jetzt schnell mit der [!UICONTROL Visual Experience Composer].

**So verwenden Sie die [!DNL Modify Response Headers] Erweiterung auf [!UICONTROL Firefox]:**

1. Installieren Sie die [!UICONTROL Modify Response Headers] on [!DNL Firefox] und starten Sie den Browser neu.
1. Von Ihrem [!DNL Firefox] Erweiterungen wählen Sie die Erweiterung &quot;Modify Response Headers&quot;.
1. Klicken Sie auf **[!UICONTROL Preferences]**.
1. Auswählen **[!UICONTROL Filter]** aus dem [!UICONTROL Action] angezeigt.
1. Im [!UICONTROL Header Name] eingeben: **[!UICONTROL X-Frame-Options]**.
1. Wiederholen Sie die Schritte 4 und 5, um einen Filter mit **[!UICONTROL x-frame-options]**.
1. Klicken Sie auf **[!UICONTROL Add]**.
1. Klicken Sie auf **[!UICONTROL Start]**.

![Firefox-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

Öffnen Sie nach dem Einrichten einer Erweiterung [!DNL Target]. Ihre Seiten sollten jetzt im [!UICONTROL Visual Experience Composer], auch wenn die [!UICONTROL Enhanced Experience Composer] deaktiviert ist.

## Meine Seite wird im VEC nicht angezeigt (nur VEC)  {#does-not-load}

* Die beste Kompatibilität mit VEC wird durch die neueste Version der Erweiterung sichergestellt: [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

  Um zu überprüfen, ob Sie die neueste Version verwenden, gehen Sie zu [!UICONTROL Extensions] > [!UICONTROL Manage Extensions] Klicken Sie dann auf [!UICONTROL Details].

* Die [!UICONTROL Visual Experience Composer] erfordert Authoring-Bibliotheken, um Änderungen auf der Webseite vorzunehmen. Diese Bibliotheken sind in die at.js-Bibliothek eingebettet und werden von der -Erweiterung von heruntergeladen [!DNL Adobe] -Server jedes Mal, wenn VEC verwendet wird.

  Die Erweiterung lädt die at.js-Bibliothek herunter, unabhängig davon, ob at.js oder die [!DNL Adobe Experience Platform Web SDK] sind bereits in der Seite enthalten.

  Stellen Sie sicher, dass den in der Konfiguration von at.js konfigurierten Headern keine ungültigen Änderungen hinzugefügt wurden. [!UICONTROL Administration] > [!UICONTROL Implementation] Abschnitt.

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
* Wenn Ihre Website im VEC nicht geladen werden kann oder sich unerwartet verhält, besteht die Möglichkeit, Cookies auf Ihrer Website im Browser zu akzeptieren, bevor versucht wird, die Website in zu laden [!DNL Target].

## Bei der Verwendung des Modus zum Durchsuchen scheint der VEC nicht zu funktionieren. (Nur VEC)   {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

Wenn Sie im Modus &quot;Durchsuchen&quot;auf eine URL zugreifen, die nicht über [!DNL Target] implementierte Bibliotheken ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=de){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}) oder einen Frame-Buster-Header enthält, scheint der VEC beschädigt zu sein. Aus Sicherheitsgründen des Browsers [!DNL Target] kann nicht ordnungsgemäß auf die URL zugreifen, zu der Sie navigiert sind, oder die VEC-URL wird nicht konsistent aktualisiert, wenn die Seite geladen wird.

Dieses Problem tritt auf, weil VEC die Webseite in eine `<iframe>`. Die aktuellen Sicherheitsmechanismen von Browsern verhindern die [!DNL Target] -Benutzeroberfläche kann aufgrund der gleichen Ursprungsrichtlinie nicht auf die Elemente des angegebenen Frames zugreifen. Browser blockieren Skripte, die versuchen, auf einen Frame mit einer anderen Herkunft zuzugreifen, und enthalten Informationen wie die `location.href`.

Sie müssen die neue [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) (empfohlen) oder die [alte Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) um die [!DNL Target] in die Seiten hinein, um sie optimal zu durchsuchen.

## Probleme, die durch CSS-Konflikte in der [!UICONTROL Visual Experience Composer]

Überprüfen Sie, ob CSS-Dateien vorhanden sind, die sich auf die Sichtbarkeit beim Laden der Webseite im Editor auswirken können. Verwenden Sie beispielsweise die `overflow: hidden` -Eigenschaft im Seitentext zu Problemen beim Scrollen oder Trigger-Klick-Ereignissen führen, die das Menü für die Bearbeitung beeinträchtigen könnten.
