---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Laden Sie eine CSV-Datei hoch, um Empfehlungen anzupassen.
title: Hochladen benutzerdefinierter Kriterien
feature: criteria
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 63%

---


# ![PREMIUM](/help/assets/premium.png) Upload benutzerdefinierter Kriterien{#upload-custom-criteria}

Laden Sie eine CSV-Datei hoch, um Empfehlungen anzupassen.

Sie haben viele Möglichkeiten, um auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations]-Aktivität mit dem [!UICONTROL Visual Experience Composer] (VEC) erstellen, werden Sie sofort zum Bildschirm [!UICONTROL Kriterien auswählen, nachdem Sie ein Element auf Ihrer Seite ausgewählt haben und auf [!UICONTROL Ersetzen mit Recommendations], [!UICONTROL Recommendations vor] oder [!UICONTROL einfügen Fügen Sie Recommendations nach] ein. ] Sie können dann ein verfügbares Kriterium auswählen oder auf **[!UICONTROL Kriterien erstellen]** klicken. Wenn Sie ein neues Kriterium erstellen, haben Sie die Möglichkeit, Ihre Kriterien für die Verwendung mit anderen [!DNL Recommendations]-Aktivitäten zu speichern. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Klicken Sie beim Bearbeiten einer [!DNL Recommendations]Aktivität in ein Feld für die [!UICONTROL Empfehlungsposition] auf Ihrer Seite und wählen Sie **[!UICONTROL Kriterien ändern]**. Klicken Sie im Bildschirm [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Kriterien erstellen]**. Sie können Ihre neuen Kriterien speichern, um Sie mit anderen [!DNL Recommendations]-Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mithilfe der ersten Methode auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zugreifen: den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Benutzerspezifische Kriterien hochladen]**.

1. Füllen Sie die Informationen im Abschnitt [Grundlegende Informationen](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Füllen Sie die Informationen im Abschnitt [Datenquelle](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) aus.

1. Füllen Sie die Informationen im Abschnitt [Inhalt](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) aus.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Ähnlichkeit des Inhalts](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity) aus.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Einschlussregeln](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) aus.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Attributgewichtung](/help/c-recommendations/c-algorithms/create-new-algorithm.md#weighting) aus.

1. Wählen Sie im Abschnitt **[!UICONTROL CSV]** hochladen die Option **[!UICONTROL Speicherort]** Ihrer CSV-Datei aus.

   ![CSV-Abschnitt hochladen](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   Die CSV-Datei muss korrekt formatiert sein, um erfolgreich hochgeladen werden zu können. Klicken Sie auf **[!UICONTROL CSV-Vorlage herunterladen]**, um eine Vorlage mit richtiger Formatierung zu erhalten.

   Es gibt für Orte zwei Optionen:

   * **FTP:** Um Ihre CSV-Datei von einem FTP-Server hochzuladen, wählen Sie **[!UICONTROL FTP]** aus und geben Sie die erforderlichen Informationen ein. Sie können optional SSL verwenden, wobei die CSV-Datei sicher mittels eines FTPS-Protokolls übermittelt wird.
   * **URL:** Um Ihre CSV-Datei von einer URL hochzuladen, wählen Sie  **[!UICONTROL URL]** und geben Sie dann eine Feed-URL ein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   >[!NOTE]
   >
   >Benutzerdefinierte Kriterienentitäten (Zeilen) können bis zu 1.000 empfohlene Elemente (Spalten) enthalten.

Benutzerspezifische Kriterienupdates sind standardmäßig kumulativ. Neue Schlüssel-Wert-Paare, die in der CSV-Uploaddatei angegeben werden, überschreiben bestehende Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, für die keine Schlüssel im CSV-Upload spezifiziert ist, können trotzdem bereitgestellt werden und laufen 31 Tagen nach dem letzten Hochladen als Teil der CSV-Datei ab.

Wenden Sie sich an Adobe Client Care, um die Einstellung zum Verwerfen bestehender Ergebnisse, die nicht im nächsten CSV-Upload enthalten sind, zu aktivieren. Wenn diese Einstellung aktiviert ist, sind nur die Schlüssel, die in der benutzerspezifischen CSV-Feed-Datei vorhanden sind, zur Bereitstellung verfügbar. Diese Einstellung gilt für alle benutzerspezifischen Kriterien.

Benutzerspezifische Kriterien-Feeds werden alle 24 Stunden aktualisiert.

Sie können den Upload- und Synchronisationsstatus Ihrer benutzerdefinierten Kriterien am Ende jeder Kriterienkarte auf der Seite „Recommendations“ > „Kriterien“ sehen. Sie können den Status auch im Dialogfeld „Bearbeiten“ sehen, wenn Sie benutzerdefinierte Kriterien bearbeiten.

Der Ablauf für einen fehlerfreien Upload sollte folgendermaßen aussehen: „Geplant“ > „Download der Feed-Datei“ > „Import“ > „Erfolgreich“.

Die folgenden Fehlermeldungen können Sie erhalten, wenn [!DNL Target] ein Problem beim Hochladen auftritt:

| Fehlermeldung | Details |
|--- |--- |
| Unbekannter Fehler | Zeigt einen internen technischen Fehler an. |
| Parsing-Fehler | Es gibt wahrscheinlich ein Problem mit dem Feed-Dateiformat. Korrigieren Sie das Dateiformat und speichern Sie den Algorithmus erneut, um den Downloadvorgang erneut zu starten. |
| Server nicht gefunden | Geben Sie einen IP- oder Hostnamen an, der im Internet sichtbar ist. |
| Zugangsdatenfehler | Geben Sie einen gültigen Benutzernamen und ein gültiges Passwort für ein aktives Konto auf dem Server an. |
| Verzeichnis nicht gefunden | Geben Sie ein Verzeichnis an, das auf dem Server existiert. |
| Datei nicht gefunden | Geben Sie den Namen einer Datei an, die auf dem Server im angegebenen Verzeichnis existiert. |

## Schulungsvideo: Kriterien in Recommendations erstellen (12:33)  ![Tutorialzeichen](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen (Details zum Hochladen benutzerdefinierter Kriterien beginnen um 11:43 Uhr):

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)