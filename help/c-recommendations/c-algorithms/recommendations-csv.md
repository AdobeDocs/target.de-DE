---
keywords: Erstellen benutzerdefinierter Kriterien; Algorithmen; Kriterien; Empfehlungskriterien; csv; ftp; CSV hochladen
description: Erfahren Sie, wie Sie eine CSV-Datei hochladen, um Ihre Empfehlungen in Adobe [!DNL Target] Recommendations anzupassen.
title: Wie lade ich benutzerdefinierte Kriterien in Recommendations hoch?
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 7a52f7c046fb00672ef1b13704308be39f89c7ad
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 39%

---

# ![PREMIUM](/help/assets/premium.png) Upload benutzerdefinierter Kriterien

Laden Sie eine CSV-Datei hoch, um Ihre Empfehlungen in [!DNL Adobe Target] anzupassen.

Sie haben viele Möglichkeiten, um auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations] -Aktivität mit dem [!UICONTROL Visual Experience Composer] (VEC) erstellen, gelangen Sie sofort zum Bildschirm [!UICONTROL Kriterien auswählen] , nachdem Sie ein Element auf Ihrer Seite ausgewählt und auf [!UICONTROL Ersetzen mit Recommendations], [!UICONTROL Recommendations einfügen vor] oder [!UICONTROL Einfügen geklickt haben. Recommendations After]. Sie können dann ein verfügbares Kriterium auswählen oder auf **[!UICONTROL Kriterien erstellen]** klicken. Wenn Sie ein neues Kriterium erstellen, können Sie Ihre Kriterien speichern, um sie mit anderen [!DNL Recommendations] -Aktivitäten zu verwenden. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Klicken Sie beim Bearbeiten einer [!DNL Recommendations]Aktivität in ein Feld für die [!UICONTROL Empfehlungsposition] auf Ihrer Seite und wählen Sie **[!UICONTROL Kriterien ändern]**. Klicken Sie im Bildschirm [!UICONTROL Kriterien] auswählen auf **[!UICONTROL Kriterien erstellen]**. Sie können Ihre neuen Kriterien speichern, um sie mit anderen [!DNL Recommendations] -Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mithilfe der ersten Methode auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zugreifen: den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Kriterien erstellen]**.

1. Füllen Sie die Informationen im Abschnitt [Grundlegende Informationen](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

   1. Wählen Sie aus der Dropdownliste **[!UICONTROL Algorithm]** Typ die Option **[!UICONTROL Benutzerdefinierte Kriterien]** aus.

   1. Wählen Sie aus der Dropdownliste **[!UICONTROL Algorithm]** die Option **[!UICONTROL Benutzerspezifischer Algorithmus]** aus.

      >[!NOTE]
      >
      >Die vorherigen Schritte führen dazu, dass der Abschnitt [!UICONTROL CSV] hochladen unten im Dialogfeld [!UICONTROL Neue Kriterien erstellen] angezeigt wird.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Backup Content](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) aus.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Einschlussregeln](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) aus.

1. Wählen Sie im Abschnitt **[!UICONTROL CSV]** hochladen den **[!UICONTROL Speicherort]** Ihrer CSV-Datei aus.

   ![CSV-Abschnitt hochladen](assets/upload-csv.png)

   Die CSV-Datei muss korrekt formatiert sein, um erfolgreich hochgeladen werden zu können. Klicken Sie auf **[!UICONTROL CSV-Vorlage herunterladen]**, um eine Vorlage mit richtiger Formatierung zu erhalten.

   Es gibt für Orte zwei Optionen:

   * **FTP:** Um Ihre CSV-Datei von einem FTP-Server hochzuladen, wählen Sie **[!UICONTROL FTP]** aus und geben Sie die erforderlichen Informationen ein. Sie können SSL verwenden, das das FTPS-Protokoll verwendet, um Ihre CSV-Datei sicher zu übertragen.
   * **URL:** Um Ihre CSV-Datei von einer URL hochzuladen, wählen Sie  **[!UICONTROL URL]** aus und geben Sie dann eine Feed-URL ein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Zu beachten

* Benutzerdefinierte Kriterienentitäten (Zeilen) können bis zu 1.000 empfohlene Elemente (Spalten) enthalten.

* Benutzerspezifische Kriterienupdates sind standardmäßig kumulativ. Neue Schlüssel-Wert-Paare, die in der CSV-Uploaddatei angegeben werden, überschreiben bestehende Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, für die keine Schlüssel im CSV-Upload angegeben sind, können weiterhin bereitgestellt werden und laufen 31 Tage nach dem letzten Hochladen als Teil der CSV-Datei ab.

   Wenden Sie sich an Adobe Client Care, um die Einstellung zum Verwerfen bestehender Ergebnisse, die nicht im nächsten CSV-Upload enthalten sind, zu aktivieren. Wenn diese Einstellung aktiviert ist, können nur die Schlüssel in der benutzerdefinierten CSV-Feed-Datei bereitgestellt werden. Diese Einstellung gilt für alle benutzerspezifischen Kriterien.

* Benutzerspezifische Kriterien-Feeds werden alle 24 Stunden aktualisiert.

   Sie können den Upload- und Synchronisierungsstatus Ihrer benutzerdefinierten Kriterien unten auf jeder Kriterienkarte auf der Seite [!UICONTROL Recommendations] > [!UICONTROL Kriterien] sehen. Der Status wird auch im Dialogfeld [!UICONTROL Bearbeiten] angezeigt, wenn Sie benutzerdefinierte Kriterien bearbeiten.

* Der Ablauf für einen fehlerfreien Upload sollte [!UICONTROL Geplant] > [!UICONTROL Herunterladen der Feed-Datei] > [!UICONTROL Importieren] > [!UICONTROL Erfolgreich] lauten.

* Im Folgenden finden Sie mögliche Fehlermeldungen, die Sie erhalten könnten, wenn [!DNL Target] ein Problem mit dem Upload auftritt:

   | Fehlermeldung | Details |
   |--- |--- |
   | Unbekannter Fehler | Zeigt einen internen technischen Fehler an. |
   | Parsing-Fehler | Es gibt wahrscheinlich ein Problem mit dem Feed-Dateiformat. Korrigieren Sie das Dateiformat und speichern Sie den Algorithmus erneut, der den Dateidownload-Prozess neu startet. |
   | Server nicht gefunden | Geben Sie einen IP- oder Hostnamen an, der im Internet sichtbar ist. |
   | Zugangsdatenfehler | Geben Sie einen gültigen Benutzernamen und ein gültiges Passwort für ein aktives Konto auf dem Server an. |
   | Verzeichnis nicht gefunden | Geben Sie ein Verzeichnis an, das auf dem Server existiert. |
   | Datei nicht gefunden | Geben Sie den Namen einer Datei an, die auf dem Server im angegebenen Verzeichnis existiert. |

## Schulungsvideo: Kriterien in Recommendations erstellen (12:33) ![Tutorial-Badge](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen (Details zum Hochladen benutzerdefinierter Kriterien beginnen um 11:43 Uhr):

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
