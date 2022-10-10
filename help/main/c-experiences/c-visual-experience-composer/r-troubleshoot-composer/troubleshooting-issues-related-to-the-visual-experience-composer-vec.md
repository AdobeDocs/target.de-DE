---
keywords: Targeting;Visual Experience Composer;VEC;Fehlerbehebung Visual Experience Composer;Fehlerbehebung;TLS;TLS 1.2
description: Erfahren Sie, wie Sie Probleme beheben können, die manchmal in der Adobe auftreten [!DNL Target] Visual Experience Composer (VEC) unter bestimmten Bedingungen.
title: Wie kann ich Probleme im Zusammenhang mit Visual Experience Composer beheben?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: ed6b1ef266f2e26cd80b6fa5099a42f6031448b5
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 80%

---

# Beheben von Problemen mit Visual Experience Composer

Anzeigeprobleme treten manchmal in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) unter bestimmten Bedingungen.

## Wenn ich meine Website im Visual Experience Composer öffne, wird die [!DNL Target] -Bibliotheken werden nicht geladen. (Nur VEC)   {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

Target fügt zwei Parameter (`mboxEdit=1` und `mboxDisable=1`) beim Öffnen der Website im Visual Experience Composer hinzu.

Wenn Ihre Website (insbesondere Apps mit einzelnen Seiten) unsere Parameter beschneidet oder beim Navigieren zwischen Seiten entfernt (ohne eine Seite neu zu laden), ist die Target-Funktionalität nicht mehr gegeben, und die Target-Bibliotheken werden nicht geladen. 
Stellen Sie zur Vermeidung dieses Problems sicher, dass Sie diese beiden Parameter nicht beschneiden oder entfernen.

## Meine Seite wird im EEC nicht geöffnet oder nur langsam geladen. Aktivitäten oder Erlebnisse werden im VEC langsam geladen. (Nur VEC)   {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Die Seitenleistung in einer der Versionen von Experience Composer in Target kann durch viele verschiedene Faktoren beeinflusst werden. Im Folgenden finden Sie einige gängige Gründe:

* Es befindet sich keine Mbox auf der Seite.
* Ihre Website nutzt Proxy-Sperren, wodurch die Seite in keiner Version von Experience Composer geöffnet werden kann.
* Ihre Website verhindert, dass Sie in einem iFrame geöffnet wird.

Falls Probleme in Enhanced Experience Composer auftreten, versuchen Sie zunächst, Enhanced Experience Composer zu deaktivieren und stattdessen Visual Experience Composer zu verwenden.

Um den Enhanced Experience Composer zu deaktivieren, navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und deaktivieren Sie die **[!UICONTROL Aktivieren von Enhanced Experience Composer]** -Option.

Bei einigen Benutzern wird in der Konsole die folgende Fehlermeldung angezeigt:

![Konsole-Fehlermeldung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Sollte weder Visual Experience Composer noch Enhanced Experience Composer funktionieren, verwenden Sie eine Browsererweiterung wie Requestly (Chrome oder Firefox) oder Modify Response Headers (Firefox), um die Optionen im „X-Frames“-Header Ihrer Website zu überschreiben und es der Website so zu ermöglichen, in iFrames geladen zu werden, wodurch auch VEC funktionieren sollte. Falls Sie keine Browsererweiterungen verwenden können, nuten Sie Form Composer.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie auch die [Adobe Target VEC Helper-Browsererweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) für Google Chrome verwenden.


>[!NOTE]
>
>Diese Plug-ins sollten nur bei der VEC-Bearbeitung verwendet werden.
>
>Gehen Sie bei der Requestly-Erweiterung wie folgt vor, wenn Sie Header entfernen müssen:
>
>* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
>
>* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.
>
>Bei der Firefox-Erweiterung „Modify Response Headers“ müssen Sie wie folgt vorgehen, da Sie keine URL-Regel hinzufügen können:
>
>* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.


**So nutzen Sie die Requestly-Erweiterung in Chrome oder Firefox:**

1. Deaktivieren Sie Enhanced Experience Composer.
1. Installieren Sie die Browsererweiterung Requestly für Chrome oder Firefox.
1. Öffnen Sie die Erweiterung und konfigurieren Sie sie wie folgt:
1. Wählen Sie **[!UICONTROL Kopfzeilen ändern aus]**.
1. Geben Sie Folgendes ein:

   * Regelname
   * Änderungsregeln

      * Ändern Sie **[!UICONTROL Hinzufügen]** zu **[!UICONTROL Entfernen]**.
      * Ändern Sie **[!UICONTROL Anforderung]** zu **[!UICONTROL Antwort]**.
      * Geben Sie „X-Frame-Options“ als Kopfzeilenname ein.
      * Wiederholen Sie die vorherigen Schritte und geben Sie „x-frame-options“ als Header-Namen ein.

         >[!NOTE]
         >
         >Bei via Requestly bearbeiteten Headern wird zwischen Groß- und Kleinschreibung unterschieden.

      * Ändern Sie **[!UICONTROL Entspricht]** zu **[!UICONTROL Enthält]** als Bedingung für die Quell-URL und geben Sie die URL der Aktivität ein, die Sie in VEC laden möchten.

      ![Chrome_extension-Bild](assets/chrome_extension.png)


1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Anforderungsbild](assets/requestly.png)

   Sie sollten die Seite nun schnell mit Visual Experience Composer laden können.

**So nutzen Sie die Erweiterung „Modify Response Headers“ in Chrome:**

1. Installieren Sie „Modify Response Headers“ in Firefox und starten Sie den Browser neu.
1. Wählen Sie in Ihren Firefox-Erweiterungen die Erweiterung „Modify Response Headers“ aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen]**.
1. Wählen Sie im Dropdownmenü mit Aktionen oben **[!UICONTROL Filtern]** aus.
1. Geben Sie im Feld „Kopfzeilenname“ Folgendes ein: **[!UICONTROL X-Frame-Options]**.
1. Wiederholen Sie die Schritte 4 und 5, um einen Filter mit **[!UICONTROL X-Frame-Optionen hinzuzufügen]**.
1. Klicken Sie auf **[!UICONTROL Hinzufügen]**.
1. Klicken Sie auf **[!UICONTROL Start]**.

![firefox_extension image](assets/firefox_extension.png)

Öffnen Sie Target, nachdem Sie eine der Erweiterungen eingerichtet haben. Ihre Seiten sollten nun in Visual Experience Composer geladen werden, selbst wenn Enhanced Experience Composer deaktiviert ist.

## Meine Seite wird im VEC nicht angezeigt (nur VEC)  {#does-not-load}

* Der Browser wird nicht unterstützt.
* Der Browser blockiert eine nicht sichere Seite auf einer sicheren Site.

   Klicken Sie auf das Symbol links neben der URL in der Browser-Adressleiste und wählen Sie **[!UICONTROL Schutz auf dieser Seite deaktivieren]**.
* Sie haben eine ungültige URL eingegeben.
* Sie haben auf Ihrer Konto-Einrichtungsseite keine Standard-URL eingegeben.

   Stellen Sie sicher, dass diese Einstellung aktiviert ist, laden Sie dann at.js herunter und aktualisieren Sie es auf Ihrer Website.

* Wenn Sie versuchen, die [new [!UICONTROL Visual Editing Helper] Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) und gehen Sie dann zurück zu [alte Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) und [!DNL Target] schlägt das Laden Ihrer Website fehl, löschen Sie alle Browserdaten und deaktivieren Sie die neue Erweiterung.

* Wenn Ihre Website im VEC nicht geladen werden kann oder sich unerwartet verhält, besteht die Möglichkeit, Cookies auf Ihrer Website im Browser zu akzeptieren, bevor versucht wird, die Website in zu laden [!DNL Target].

## Bei der Verwendung des Modus zum Durchsuchen scheint der VEC nicht zu funktionieren. (Nur VEC)   {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

Wenn Sie beim Verwenden des Durchsuchen-Modus auf eine URL zugreifen, die nicht über target.js verfügt oder einen Header mit einem zerstörten Frame enthält, scheint der Visual Experience Composer beschädigt. Aufgrund von Sicherheitsbedenken beim Browser kann Target nicht auf die URL zugreifen, zu der Sie navigiert haben.
