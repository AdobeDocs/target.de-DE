---
keywords: Browseroptionen; Typ; Browsertyp; Browsersprache; Sprache; Version; Browserversion
description: Erfahren Sie, wie Sie Zielgruppen erstellen in [!DNL Adobe Target] , um Benutzer anzusprechen, die einen bestimmten Browser oder bestimmte Browseroptionen beim Besuch Ihrer Seite verwenden.
title: Kann ich Besucher auf Grundlage des Browsertyps ansprechen?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: c79b1d40e0bf0495dc3f3d5accd196f14d18b934
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 53%

---

# Browser

Sie können Benutzer, die einen speziellen Browser oder spezielle Browseroptionen beim Besuch Ihrer Seite verwenden, als Ziel auswählen.

Die folgenden Browser können als Ziel ausgewählt werden:

* Chrome
* Firefox
* Safari
* Internet Explorer
* Microsoft Edge
* Opera
* iPad  
* iPhone

>[!IMPORTANT]
>
>Ab dem 30. April 2024 werden iPad und iPhone aus der verfügbaren [!UICONTROL Browser] Typ Dropdown-Liste beim Erstellen von Kategorien für Zielgruppen. Informationen zu Umgehungseinstellungen finden Sie unter [Veraltung von iPad und iPhone vom Browserzielgruppenattribut (30. April 2024)](#deprecation) unten.

Es gibt zwei Möglichkeiten, Browser auszurichten:

* **Vordefinierte Zielgruppe:** Verwenden Sie diesen Typ, wenn Sie nur Besucher ansprechen möchten, die für den Besuch auf Ihrer Site einen speziellen Browser verwenden. Wenn Sie zum Beispiel eine Chrome-Erweiterung anbieten, würden Sie nur Chrome-Benutzer ansprechen.

   1. Wählen Sie beim Einrichten Ihrer Aktivität den Browser aus der Dropdown-Liste aus.

      Diese Option richtet die Aktivität nur auf Besucher aus, die den angegebenen Browser verwenden.

      ![Target Chrome-Benutzer](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Benutzerdefinierte Regel für Browserzielgruppe:** Mit einer benutzerdefinierten Zielgruppe können Sie mehrere Browser als Ziel auswählen oder Regeln oder Ausschlüsse für bestimmte Browser, Browserversionen oder Browsersprachen einrichten. Diese Funktion bietet erhebliche Flexibilität beim Targeting einer Aktivität auf der Grundlage von Browserattributen.

   1. Im [!DNL Target] Benutzeroberfläche, klicken Sie auf **[!UICONTROL Zielgruppen]** > **[!UICONTROL Zielgruppe erstellen]**.
   1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
   1. Drag &amp; Drop **[!UICONTROL Browser]** in Audience Builder.

      ![Regeln > Browser](assets/target_browser.png)

   1. Klicken Sie auf **[!UICONTROL Auswählen]** und wählen Sie anschließend eine der folgenden Optionen aus:

      * **Typ:** Schließen Sie einen bestimmten Browser ein oder aus. Weitere Informationen finden Sie unter [Typ](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Sprache:** Schließen Sie bestimmte Browser, die bestimmte Sprachen verwenden, als Ziel ein oder aus. Weitere Informationen finden Sie unter [Sprache](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Version:** Schließen Sie bestimmte Browserversionen ein oder aus. Weitere Informationen finden Sie unter [Version](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

   1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
   1. Klicken Sie auf **[!UICONTROL Fertig]**.

  Das folgende Beispiel zeigt eine Zielgruppe mit Microsoft Edge-Benutzern in den Versionen 91 und 92:

  ![Target Edge 91 oder 92](assets/target_edge.png)

## Browseroptionen {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Wählen Sie Aktivitätsteilnehmer basierend auf ihrem Browsertyp, ihrer Sprache oder Version als Zielgruppe aus oder schließen Sie sie aus.

### Typ  {#section_6ADC758F23F145B3A310151546D83D56}

Schließen Sie einen bestimmten Browser als Ziel ein oder aus.

Wählen Sie **[!UICONTROL Typ]** und entscheiden Sie, ob gleich oder nicht gleich.

* Gleich: Schließt die ausgewählten Browser als Ziel ein.
* Nicht gleich: Schließt die ausgewählten Browser aus.

Wählen Sie einen oder mehrere Browser aus. Mehrfachoptionen sind mit einem ODER verbunden.

### Sprache  {#section_7520D1AA464A45A6843EABE2D2B431A1}

Schließen Sie bestimmte Browserversionen, die spezifische Sprachen verwenden, als Ziel ein oder aus.

Wenn zum Beispiel ein Angebot nur auf Englisch verfügbar ist, können Sie Browser als Ziel einschließen, deren Sprache auf Englisch festgelegt ist. Oder wenn Ihre Seite keine Doppel-Byte-Zeichen unterstützt, können Sie Browser ausschließen, die für asiatische Sprachen eingestellt sind.

In Fällen, in denen die Sprache wichtiger als der Standort ist, bietet das Ein- oder Ausschließen von Browsersprachen eine zielgerichtetere Besucheransprache als die geografisch basierte Kundenansprache. Wenn Sie zum Beispiel einen auf Englisch geschriebenen Artikel anbieten, können Sie entweder englischsprachige Länder oder Länder, deren Sprache auf Englisch festgelegt ist, als Ziel einschließen. Wenn Sie den Browser als Ziel einschließen, steht der Artikel Personen zur Verfügung, die Englisch verstehen, sich jedoch in Ländern befinden, in denen Englisch nicht die Hauptsprache ist.

Wählen Sie **[!UICONTROL Sprache]** aus und entscheiden Sie dann, ob gleich oder nicht gleich.

* Gleich: Schließt die ausgewählten Browsersprachen als Ziel ein.
* Nicht gleich: Schließt die ausgewählten Browsersprachen als Ziel aus.

Wählen Sie eine oder mehrere Sprachen aus. Mehrfachoptionen sind mit einem ODER verbunden.

Folgende Browsersprachen können als Ziel ein- oder ausgeschlossen werden.

* Englisch
* Französisch
* Deutsch
* Japanisch
* Koreanisch
* Portugiesisch
* Russisch
* Spanisch
* Traditionelles Chinesisch

### Version  {#section_37CC8CE45DA04E8682AE6388321BA6EF}

Schließen Sie bestimmte Browserversionen als Ziel ein oder aus.

Wenn Ihre Seite zum Beispiel in Internet Explorer Version 11 oder früher nicht richtig angezeigt wird, können Sie eine Zielgruppe erstellen, die diese Versionen ausschließt. In diesem Fall würden Sie eine Regel aufstellen, bei der der Browsertyp gleich Internet Explorer ist, und eine zweite Regel hinzufügen, bei der die Version kleiner oder gleich 11 lautet.

Wählen Sie **[!UICONTROL Version]** und anschließend einen Betreiber aus:

* Gleich
* Ist nicht gleich
* Größer als
* Größer als oder gleich
* Kleiner als
* Kleiner als oder gleich

Geben Sie die Versionsnummer ein. Es können nur Hauptversionen in das Textfeld eingegeben werden. Die angegebene Version enthält alle kleineren Versionen dieser Version. Wenn Sie beispielsweise Version 10 angeben, werden auch Besucher mit Version 10.1 einbezogen.

Mehrfachoptionen sind mit einem ODER verbunden.

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## Einstellung der Unterstützung von iPad und iPhone für das Zielgruppenattribut „Browser“ (30. April 2024) {#deprecation}

[!DNL Adobe Target] ermöglicht [Zielgruppe für eines oder mehrere Kategorieattribute](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), einschließlich der Benutzer, die beim Besuch Ihrer Seite bestimmte Browser- oder Browseroptionen verwenden.

Ab dem 30. April 2024 werden iPad und iPhone aus der verfügbaren [!UICONTROL Browser] Typ Dropdown-Liste beim Erstellen von Kategorien für Zielgruppen.

Für Zielgruppen, die mit dem Attribut [!UICONTROL Browser] auf iPads oder iPhones abzielen, müssen Sie diese Einstellungen vor dem 30. April 2024 ändern, damit diese Zielgruppen weiterhin erwartungsgemäß funktionieren.

### Zielgruppen, die mithilfe der [!DNL Target] Benutzeroberfläche

Die folgenden Einstellungen können in Zukunft verwendet werden:

* **Für Browserübereinstimmungen[!DNL Apple]**: [!UICONTROL Mobilnummer] > [!UICONTROL Gerätehersteller] [!UICONTROL matches] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **Für Browser-Matches**: [!UICONTROL Mobilnummer] > [!UICONTROL Tablette] > [!UICONTROL true]

  ![Mobil ist Tablet](/help/main/r-release-notes/assets/is-tablet.png)

* **Für Browser stimmt iPad überein**: [!UICONTROL Mobilnummer] > [!UICONTROL Gerätemarketingname] [!UICONTROL matches] [!DNL iPad] mit einem Und-Container mit [!UICONTROL Mobilnummer] > [!UICONTROL Ist Tablet] is [!DNL true]

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **Für Browser stimmt iPhone überein**: [!UICONTROL Mobilnummer] > [!UICONTROL Gerätemarketingname] [!UICONTROL matches] [!DNL iPhone] mit einem Und-Container mit [!UICONTROL Mobilnummer] > [!UICONTROL Ist Mobiltelefon] is [!DNL true]

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

Es gibt viele weitere mögliche Einstellungen, die verwendet werden können, z. B. wenn Bedingungen negiert werden. Beispiele für negierte Bedingungen könnten wie folgt aussehen:

* **Für Browser stimmt iPhone nicht überein**: [!UICONTROL Mobilnummer] > [!UICONTROL Gerätehersteller] [!UICONTROL stimmt nicht überein mit] [!UICONTROL Apple] mit einem ODER-Container mit [!UICONTROL Mobilnummer] > [!UICONTROL Ist Mobiltelefon] is [!UICONTROL false]

  ![Nicht Mobiltelefon](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **Für Browser stimmt iPad nicht überein**: [!UICONTROL Mobilnummer] > [!UICONTROL Gerätehersteller] [!UICONTROL stimmt nicht überein mit] [!UICONTROL Apple] mit einem ODER-Container mit [!UICONTROL Mobilnummer] > [!UICONTROL Ist Tablet] is [!UICONTROL false].

  ![Nicht Tablette](/help/main/r-release-notes/assets/tablet-false.png)

### Mit Profilskripten erstellte Zielgruppen

Wenn Sie `user.browserType` in JavaScript-Segmenten, wie unter [Glossar zu Profil und Variablen](/help/main/c-target/c-visitor-profile/variables-profiles-parameters-methods.md), sollten Änderungen Folgendes umfassen:

>[!NOTE]
>
>Die folgenden Profile sollen ab dem 24. Januar 2024 in den nächsten Tagen veröffentlicht werden. Die [Aktuelle Versionshinweise](/help/main/r-release-notes/release-notes.md) werden aktualisiert, sobald diese Profile verfügbar sind.

Diese Profile ermöglichen die folgenden Änderungen:
>>
* `profile.mobile.isTablet`
>>
* `profile.mobile.isMobilePhone`

* **BrowserType ist iPhone**:

  Ersetzen:

  `user.browserType=="iphone"`

  Mit:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isMobilePhone`

* **BrowserType ist nicht iPhone**:

  Ersetzen:

  `user.browserType!="iphone"`

  Mit:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isMobilePhone`

* **BrowserType ist iPad**:

  Ersetzen:

  `user.browserType=="ipad"`

  Mit:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isTablet`

* **BrowserType ist nicht iPad**:

  Ersetzen:

  `user.browserType!="ipad"`

  Mit:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isTablet`