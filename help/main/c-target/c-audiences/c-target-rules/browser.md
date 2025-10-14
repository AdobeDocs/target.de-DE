---
keywords: Browseroptionen; Typ; Browsertyp; Browsersprache; Sprache; Version; Browserversion
description: Erfahren Sie, wie Sie Zielgruppen in erstellen [!DNL Adobe Target]  um Benutzende anzusprechen, die beim Besuch Ihrer Seite einen bestimmten Browser oder bestimmte Browser-Optionen verwenden.
title: Kann ich Besuchende nach Browser-Typ auswählen?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: 784f41a73941877135a5902f2331972ba9d0e880
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 34%

---

# [!UICONTROL Browser]

Sie können Benutzer, die einen speziellen Browser oder spezielle Browseroptionen beim Besuch Ihrer Seite verwenden, als Ziel auswählen.

Die folgenden Browser können als Ziel ausgewählt werden:

* [!UICONTROL Chrome]
* [!UICONTROL Firefox]
* [!UICONTROL Safari]
* [!UICONTROL Internet Explorer]
* [!UICONTROL Microsoft Edge]
* [!UICONTROL Opera]
* [!DNL iPad]
* [!DNL iPhone]

>[!IMPORTANT]
>
>Ab [!DNL Target] Standard/Premium 24.3.1 (4. bis 6. März 2024) wurden integrierte Zielgruppen, die mithilfe der Target-Benutzeroberfläche erstellt wurden, wie `Browser:iPad` und `Browser:iPhone`, aktualisiert, um eine ordnungsgemäße Zielgruppenbestimmung für [!DNL iPad] und [!DNL iPhone] mithilfe von `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` und `profile.mobile.isTablet` durchzuführen.
>
>Diese Aktualisierung erfordert keine Maßnahmen seitens der Kunden. Die Beschriftungen in der [!DNL Target]-Benutzeroberfläche werden in Zukunft geändert und in den [[!DNL Target] Versionshinweisen (aktuell) angekündigt](/help/main/r-release-notes/release-notes.md) sobald diese Änderungen vorgenommen werden.
>
>Informationen zu Problemumgehungseinstellungen finden Sie unter [Aktualisierungen für  [!DNL iPad] / [!DNL iPhone] -in [!UICONTROL Browser] Zielgruppenattributen (30. April 2024)](#updates) unten.

Es gibt zwei Möglichkeiten, Browser auszurichten:

* **Vordefinierte Zielgruppe:** Verwenden Sie diesen Typ, wenn Sie nur Besucher ansprechen möchten, die für den Besuch auf Ihrer Site einen speziellen Browser verwenden. Wenn Sie beispielsweise eine [!DNL Chrome] anbieten, richten Sie sich an nur [!DNL Chrome] Benutzer.

   1. Wählen Sie beim Einrichten Ihrer Aktivität den Browser aus der Dropdown-Liste aus.

      Diese Option richtet die Aktivität nur auf Besucher aus, die den angegebenen Browser verwenden.

      ![Target für Chrome-Benutzer](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Benutzerdefinierte Browser-Zielgruppenregel:** Mit einer benutzerdefinierten Zielgruppe können Sie mehrere Browser als Ziel auswählen oder Regeln oder Ausschlüsse für bestimmte Browser, Browser-Versionen oder Browser-Sprachen einrichten. Diese Funktion bietet eine erhebliche Flexibilität beim Targeting von Aktivitäten auf der Grundlage von Browser-Attributen.

   1. Klicken Sie in der [!DNL Target] auf **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
   1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
   1. Ziehen Sie **[!UICONTROL Browser]** per Drag-and-Drop in Audience Builder.

      ![Regeln > Browser](assets/target_browser.png)

   1. Klicken Sie auf **[!UICONTROL Select]** und wählen Sie dann eine der folgenden Optionen aus:

      * **Typ:** Schließen Sie einen bestimmten Browser ein oder aus. Weitere Informationen finden Sie unter [Typ](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Sprache:** Sie können bestimmte Browser, die bestimmte Sprachen verwenden sollen, als Ziel auswählen oder ausschließen. Weitere Informationen finden Sie unter [Sprache](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Version:** Schließen Sie bestimmte Browserversionen ein oder aus. Weitere Informationen finden Sie unter [Version](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

   1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
   1. Klicken Sie auf **[!UICONTROL Done]**.

  Das folgende Beispiel zeigt eine Zielgruppe, die [!DNL Microsoft Edge] Benutzer der Versionen 91 oder 92 enthält:

  ![Target Edge 91 oder 92](assets/target_edge.png)

## Browser-Optionen {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Wählen Sie Aktivitätsteilnehmer basierend auf ihrem Browsertyp, ihrer Sprache oder Version als Zielgruppe aus oder schließen Sie sie aus.

### Typ  {#section_6ADC758F23F145B3A310151546D83D56}

Schließen Sie einen bestimmten Browser als Ziel ein oder aus.

Wählen Sie **[!UICONTROL Type]** und dann entweder gleich oder ungleich aus.

* [!UICONTROL Equals]: Targeting der ausgewählten Browser
* [!UICONTROL Does not equal]: Ausgewählte Browser ausschließen.

Wählen Sie einen oder mehrere Browser aus. Mehrfachoptionen sind mit einem ODER verbunden.

### Sprache  {#section_7520D1AA464A45A6843EABE2D2B431A1}

Schließen Sie bestimmte Browserversionen, die spezifische Sprachen verwenden, als Ziel ein oder aus.

Wenn zum Beispiel ein Angebot nur auf Englisch verfügbar ist, können Sie Browser als Ziel einschließen, deren Sprache auf Englisch festgelegt ist. Oder wenn Ihre Seite keine Doppel-Byte-Zeichen unterstützt, können Sie Browser ausschließen, die für asiatische Sprachen eingestellt sind.

In Fällen, in denen die Sprache wichtiger als der Standort ist, bietet das Ein- oder Ausschließen von Browsersprachen eine zielgerichtetere Besucheransprache als die geografisch basierte Kundenansprache. Wenn Sie zum Beispiel einen auf Englisch geschriebenen Artikel anbieten, können Sie entweder englischsprachige Länder oder Länder, deren Sprache auf Englisch festgelegt ist, als Ziel einschließen. Wenn Sie den Browser als Ziel einschließen, steht der Artikel Personen zur Verfügung, die Englisch verstehen, sich jedoch in Ländern befinden, in denen Englisch nicht die Hauptsprache ist.

Wählen Sie **[!UICONTROL Language]** und dann entweder gleich oder ungleich aus.

* [!UICONTROL Equals]: Ausgewählte Browser-Sprachen als Ziel auswählen.
* [!UICONTROL Does not equal]: Ausgewählte Browser-Sprachen ausschließen.

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

Wenn Ihre Seite beispielsweise in [!DNL Internet Explorer] Version 11 oder früher nicht korrekt angezeigt wird, können Sie eine Zielgruppe erstellen, die diese Versionen ausschließt. In diesem Fall würden Sie eine Regel einrichten, bei der der Browser-Typ [!DNL Internet Explorer] ist, und eine zweite Regel hinzufügen, bei der die Version kleiner oder gleich 11 ist.

Wählen Sie **[!UICONTROL Version]** und dann einen Operator aus:

* [!UICONTROL Equals]
* [!UICONTROL Does not equal]
* [!UICONTROL Is greater than]
* Größer als oder gleich
* [!UICONTROL Is less than]
* [!UICONTROL Is less than or equal to]

Geben Sie die Versionsnummer ein. Es können nur Hauptversionen in das Textfeld eingegeben werden. Die angegebene Version enthält alle kleineren Versionen dieser Version. Wenn Sie beispielsweise Version 10 angeben, werden auch Besucher in Version 10.1 einbezogen.

Mehrfachoptionen sind mit einem ODER verbunden.

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## Aktualisierungen für [!DNL iPad] und [!DNL iPhone] in [!UICONTROL Browser]-Zielgruppenattribute (30. April 2024) {#updates}

[!DNL Adobe Target] können Sie [auf eines von mehreren Kategorieattributen ansprechen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md) einschließlich Benutzerinnen und Benutzer, die beim Besuch Ihrer Seite eine bestimmte Browser- oder Browser-Option verwenden.

Seit Einführung von [!DNL Target] Standard/Premium 24.3.1 (4.-6. März 2024) wurden integrierte Zielgruppen, die mithilfe der Target-Benutzeroberfläche erstellt wurden (z. B. `Browser:iPad` und `Browser:iPhone`), aktualisiert, um eine ordnungsgemäße Zielgruppenbestimmung für [!DNL iPad] und [!DNL iPhone] mithilfe von `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` und `profile.mobile.isTablet` durchzuführen.

Integrierte Zielgruppen, die mit der [!DNL Target]-Benutzeroberfläche erstellt wurden, wie z. B. `Browser:iPad` und `Browser:iPhone`, werden automatisch in die neue Zielgruppendefinition verschoben und erfordern keine Aktion seitens der Kunden. In Zukunft sollten Sie jedoch die Einstellungen verwenden [wie unten beschrieben](#ui).

Wenn Sie `user.browserType` in Profilskripten verwenden, um zu überprüfen, ob es sich um einen [!DNL iPhone] oder einen [!DNL iPad] handelt (z. B. `user.browserType == 'iphone'` oder `user.browserType != 'ipad'`), sollten diese Profilskripte vor dem 30. April 2024 wie [&#x200B; unten &#x200B;](#profile-scripts) geändert werden, um sicherzustellen, dass diese Zielgruppen weiterhin wie erwartet funktionieren.

JavaScript-Zielgruppen sind ältere Zielgruppen, die [!DNL Target] verwenden, welche in der [!DNL Target Classic]-Benutzeroberfläche veraltet sind. Diese Zielgruppen können nur über die API geändert werden. Kunden dürfen diese Zielgruppen nur aktualisieren, wenn sie weiterhin ältere Zielgruppen in -Aktivitäten verwenden.

### Zielgruppen, die mithilfe der [!DNL Target]-Benutzeroberfläche erstellt wurden {#ui}

Die folgenden Einstellungen können in Zukunft verwendet werden:

* **Für Browser-Übereinstimmungen[!DNL Apple]**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL matches] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **Bei Browser-Übereinstimmungen mit Tablet**: [!UICONTROL Mobile] > [!UICONTROL is Tablet] > [!UICONTROL true]

  ![Mobil ist Tablet](/help/main/r-release-notes/assets/is-tablet.png)

* **Für Browser stimmt überein mit iPad**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPad] mit einem Und-Container mit [!UICONTROL Mobile] > [!UICONTROL Is Tablet] ist [!DNL true]

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **Für Browser stimmt überein mit iPhone**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPhone] mit einem Und-Container mit [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] ist [!DNL true]

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

Es gibt viele andere mögliche Einstellungen, die verwendet werden können, zum Beispiel wenn Bedingungen negiert werden. Beispiele für negierte Bedingungen könnten wie folgt aussehen:

* **Für Browser stimmt nicht mit iPhone überein**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] mit einem ODER-Container mit [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] ist [!UICONTROL false]

  ![Kein Mobiltelefon](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **Für Browser stimmt nicht mit iPad überein**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] mit einem ODER-Container mit [!UICONTROL Mobile] > [!UICONTROL Is Tablet] ist [!UICONTROL false].

  ![Nicht Tablet](/help/main/r-release-notes/assets/tablet-false.png)

### Zielgruppen, die mithilfe von Profilskripten erstellt wurden {#profile-scripts}

Wenn Sie `user.browserType` in veralteten [!DNL Target Classic]-Zielgruppen oder in Profilskripten verwenden, sollten die Änderungen Folgendes umfassen:

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