---
keywords: Targeting;visual experience composer;vec;troubleshoot visual experience composer;troubleshooting;tls;tls 1.2
description: Unter bestimmten Umständen treten im Adobe Target Visual Experience Composer (VEC) manchmal Anzeigeprobleme auf.
title: Beheben von Problemen mit Visual Experience Composer
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 92%

---


# Fehlerbehebung in Zusammenhang mit Visual Experience Composer

Anzeigeprobleme treten manchmal unter bestimmten Bedingungen im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) auf.

## Wenn ich meine Website im Visual Experience Composer öffne, werden die Target-Bibliotheken nicht geladen. (nur VEC) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

Target fügt zwei Parameter (`mboxEdit=1` und `mboxDisable=1`) beim Öffnen der Website im Visual Experience Composer hinzu.

Wenn Ihre Website (insbesondere Apps mit einzelnen Seiten) unsere Parameter beschneidet oder beim Navigieren zwischen Seiten entfernt (ohne eine Seite neu zu laden), ist die Target-Funktionalität nicht mehr gegeben, und die Target-Bibliotheken werden nicht geladen. 
Stellen Sie zur Vermeidung dieses Problems sicher, dass Sie diese beiden Parameter nicht beschneiden oder entfernen.

## Meine Seite wird im EEC nicht geöffnet oder nur langsam geladen. Aktivitäten oder Erlebnisse werden im VEC langsam geladen. (nur VEC) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Die Seitenleistung in einer der Versionen von Experience Composer in Target kann durch viele verschiedene Faktoren beeinflusst werden. Im Folgenden finden Sie einige gängige Gründe:

* Es befindet sich keine Mbox auf der Seite.
* Ihre Website nutzt Proxy-Sperren, wodurch die Seite in keiner Version von Experience Composer geöffnet werden kann.
* Ihre Website verhindert, dass Sie in einem iFrame geöffnet wird.

Falls Probleme in Enhanced Experience Composer auftreten, versuchen Sie zunächst, Enhanced Experience Composer zu deaktivieren und stattdessen Visual Experience Composer zu verwenden.

Um Enhanced Experience Composer zu deaktivieren, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und deaktivieren Sie die Option **[!UICONTROL Enhanced Experience Composer aktivieren]**.

Bei einigen Benutzern wird in der Konsole die folgende Fehlermeldung angezeigt:

![Konsole-Fehlermeldung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Sollte weder Visual Experience Composer noch Enhanced Experience Composer funktionieren, verwenden Sie eine Browsererweiterung wie Requestly (Chrome oder Firefox) oder Modify Response Headers (Firefox), um die Optionen im „X-Frames“-Header Ihrer Website zu überschreiben und es der Website so zu ermöglichen, in iFrames geladen zu werden, wodurch auch VEC funktionieren sollte. Falls Sie keine Browsererweiterungen verwenden können, nuten Sie Form Composer.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie auch die [Adobe Target VEC Helper-Browsererweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) für Google Chrome verwenden.


>[!NOTE]
>
>Diese Plug-ins sollten nur bei der VEC-Bearbeitung verwendet werden.
>
>Gehen Sie bei der Requestly-Erweiterung wie folgt vor, wenn Sie Header entfernen müssen:
>
>* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
   >
   >
* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.
>
>
Bei der Firefox-Erweiterung „Modify Response Headers“ müssen Sie wie folgt vorgehen, da Sie keine URL-Regel hinzufügen können:
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

      ![](assets/chrome_extension.png)


1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/requestly.png)

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

![](assets/firefox_extension.png)

Öffnen Sie Target, nachdem Sie eine der Erweiterungen eingerichtet haben. Ihre Seiten sollten nun in Visual Experience Composer geladen werden, selbst wenn Enhanced Experience Composer deaktiviert ist.

## Meine Seite wird im VEC nicht angezeigt (nur VEC)   {#section_87B3BEA4B6174CFDA6C9A69A1A051FA1}

* Der Browser wird nicht unterstützt.
* Der Browser blockiert eine nicht sichere Seite auf einer sicheren Site.

   Klicken Sie auf das Symbol links neben der URL in der Browser-Adressleiste und wählen Sie **[!UICONTROL Schutz auf dieser Seite deaktivieren]**.
* Sie haben eine ungültige URL eingegeben.
* Sie haben auf Ihrer Konto-Einrichtungsseite keine Standard-URL eingegeben.

Stellen Sie sicher, dass diese Einstellung aktiviert ist, laden Sie dann mbox.js erneut herunter und aktualisieren Sie damit Ihre Website.

## Bei der Verwendung des Modus zum Durchsuchen scheint der VEC nicht zu funktionieren. (nur VEC) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

Wenn Sie beim Verwenden des Durchsuchen-Modus auf eine URL zugreifen, die nicht über target.js verfügt oder einen Header mit einem zerstörten Frame enthält, scheint der Visual Experience Composer beschädigt. Aufgrund von Sicherheitsbedenken beim Browser kann Target nicht auf die URL zugreifen, zu der Sie navigiert haben.
