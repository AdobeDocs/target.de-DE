---
keywords: Erstellen benutzerdefinierter Kriterien; Algorithmen; Kriterien; Empfehlungskriterien; csv; ftp; CSV hochladen
description: Erfahren Sie, wie Sie eine CSV-Datei hochladen, um Ihre Empfehlungen in Adobe [!DNL Target] Recommendations anzupassen.
title: Wie lade ich benutzerdefinierte Kriterien in [!DNL Recommendations] hoch?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 77bbdd4438aa17f2e8d96e00bd3d37806a474585
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 32%

---

# Hochladen benutzerdefinierter Kriterien

Laden Sie eine CSV-Datei hoch, um Ihre Empfehlungen in [!DNL Adobe Target] anzupassen.

Es gibt mehrere Möglichkeiten, den Bildschirm [!UICONTROL Create New Criteria] zu erreichen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie auf dem Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations] -Aktivität mit dem VEC (1}) erstellen, gelangen Sie sofort zum Bildschirm [!UICONTROL Select Criteria] , nachdem Sie ein Element auf Ihrer Seite ausgewählt und auf [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before] oder [!UICONTROL Insert Recommendations After] geklickt haben. [!UICONTROL Visual Experience Composer] Sie können dann ein verfügbares Kriterium auswählen oder auf **[!UICONTROL Create Criteria]** klicken. Wenn Sie ein neues Kriterium erstellen, können Sie Ihre Kriterien speichern, um sie mit anderen [!DNL Recommendations] -Aktivitäten zu verwenden. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Wenn Sie eine [!DNL Recommendations] -Aktivität bearbeiten, klicken Sie in ein [!UICONTROL Recommendations Location] -Feld auf Ihrer Seite und wählen Sie **[!UICONTROL Change Criteria]** aus. Klicken Sie auf dem Bildschirm [!UICONTROL Select Criteria] auf **[!UICONTROL Create Criteria]**. Sie können Ihre neuen Kriterien speichern, um sie mit anderen [!DNL Recommendations] -Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mit der ersten Methode auf den Bildschirm [!UICONTROL Create New Criteria] zugreifen: auf den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Select Algorithm Type]** die Option **[!UICONTROL Custom Criteria]** aus.

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Algorithm]** die Option **[!UICONTROL Custom Algorithm]** aus.

   >[!NOTE]
   >
   >Die vorhergehenden Schritte führen dazu, dass der Abschnitt [!UICONTROL Upload CSV] unten im Dialogfeld [!UICONTROL Create Criteria] angezeigt wird.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Backup Content](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) aus.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Einschlussregeln](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) aus.

1. Wählen Sie im Abschnitt **[!UICONTROL Upload CSV]** die Option **[!UICONTROL Location]** Ihrer CSV-Datei aus.

   <!--The CSV file must be formatted correctly to upload successfully. Click **[!UICONTROL Download the CSV template]** to get a correctly formatted CSV file.-->

   Es gibt für Orte zwei Optionen:

   * **FTP:** Um Ihre CSV-Datei von einem FTP-Server hochzuladen, wählen Sie **[!UICONTROL FTP]** aus und geben Sie dann die erforderlichen Informationen ein. Sie können SSL verwenden, das das FTPS-Protokoll verwendet, um Ihre CSV-Datei sicher zu übertragen.

     ![FTP-Option zum Hochladen der CSV-Datei](/help/main/c-recommendations/c-algorithms/assets/ftp.png)

   * **URL:** Um Ihre CSV-Datei von einer URL hochzuladen, wählen Sie **[!UICONTROL URL]** und geben Sie dann eine Feed-URL ein.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Zu beachten

* Benutzerdefinierte Kriterienentitäten (Zeilen) können bis zu 1.000 empfohlene Elemente (Spalten) enthalten.

* Benutzerspezifische Kriterienupdates sind standardmäßig kumulativ. Neue Schlüssel-Wert-Paare, die in der CSV-Uploaddatei angegeben werden, überschreiben bestehende Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, für die keine Schlüssel im CSV-Upload angegeben sind, können weiterhin bereitgestellt werden und laufen 31 Tage nach dem letzten Hochladen als Teil der CSV-Datei ab.

  Wenden Sie sich an Adobe Client Care, um die Einstellung zum Verwerfen bestehender Ergebnisse, die nicht im nächsten CSV-Upload enthalten sind, zu aktivieren. Wenn diese Einstellung aktiviert ist, können nur die Schlüssel in der benutzerdefinierten CSV-Feed-Datei bereitgestellt werden. Diese Einstellung gilt für alle benutzerspezifischen Kriterien.

* Benutzerspezifische Kriterien-Feeds werden alle 24 Stunden aktualisiert.

  Sie können den Upload- und Synchronisierungsstatus Ihrer benutzerdefinierten Kriterien für jedes Kriterium auf der Seite [!UICONTROL Recommendations] > [!UICONTROL Criteria] sehen. Sie können den Status auch im Dialogfeld [!UICONTROL Edit] sehen, wenn Sie benutzerdefinierte Kriterien bearbeiten.

* Der Fluss für einen fehlerfreien Upload sollte [!UICONTROL Scheduled] > [!UICONTROL Downloading Feed File] > [!UICONTROL Importing] > [!UICONTROL Successful] lauten.

* Im Folgenden finden Sie mögliche Fehlermeldungen, die Sie erhalten könnten, wenn [!DNL Target] ein Problem mit dem Upload feststellt:

  | Fehlermeldung | Details |
  |--- |--- |
  | Unbekannter Fehler | Zeigt einen internen technischen Fehler an. |
  | Parsing-Fehler | Es gibt wahrscheinlich ein Problem mit dem Feed-Dateiformat. Korrigieren Sie das Dateiformat und speichern Sie den Algorithmus erneut, um den Dateidownload-Prozess neu zu starten. |
  | Server nicht gefunden | Geben Sie einen IP- oder Hostnamen an, der im Internet sichtbar ist. |
  | Zugangsdatenfehler | Geben Sie einen gültigen Benutzernamen und ein gültiges Passwort für ein aktives Konto auf dem Server an. |
  | Verzeichnis nicht gefunden | Geben Sie ein Verzeichnis an, das auf dem Server existiert. |
  | Datei nicht gefunden | Geben Sie den Namen einer Datei an, die auf dem Server im angegebenen Verzeichnis existiert. |