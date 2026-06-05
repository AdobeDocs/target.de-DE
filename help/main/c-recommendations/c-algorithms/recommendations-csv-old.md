---
keywords: Erstellen benutzerdefinierter Kriterien; Algorithmen; Kriterien; Empfehlungskriterien; csv; ftp; CSV hochladen
description: Erfahren Sie, wie Sie eine CSV-Datei hochladen, um Ihre Empfehlungen in Adobe/ [!DNL Target]  anzupassen.
title: Wie lade ich benutzerdefinierte Kriterien in Recommendations hoch?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 32%

---

# Hochladen benutzerdefinierter Kriterien

Laden Sie eine CSV-Datei hoch, um Ihre Empfehlungen in [!DNL Adobe Target] anzupassen.

Sie haben viele Möglichkeiten, um auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bildschirm **&#x200B;**&#x200B;> **[!UICONTROL Kriterien]** Bibliothek auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations] mit dem [!UICONTROL Visual Experience Composer] (VEC) erstellen, gelangen Sie sofort zum Bildschirm [!UICONTROL Kriterien auswählen], nachdem Sie ein Element auf Ihrer Seite ausgewählt haben und auf [!UICONTROL Mit Empfehlungen ersetzen], [!UICONTROL Empfehlungen einfügen vor] oder [!UICONTROL Empfehlungen einfügen nach] klicken. Sie können dann ein verfügbares Kriterium auswählen oder auf **[!UICONTROL Kriterien erstellen]** klicken. Wenn Sie neue Kriterien erstellen, können Sie Ihre Kriterien zur Verwendung mit anderen [!DNL Recommendations] speichern. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Wenn Sie eine [!DNL Recommendations] bearbeiten, klicken Sie in ein Feld [!UICONTROL Recommendations-Speicherort] auf Ihrer Seite und wählen Sie **[!UICONTROL Kriterien ändern]** aus. Klicken Sie im [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Kriterien erstellen]**. Sie können Ihre neuen Kriterien zur Verwendung mit anderen [!DNL Recommendations] speichern.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mit der ersten Methode auf [!UICONTROL &#x200B; Bildschirm „Neue Kriterien &#x200B;]&quot; zugreifen: der Bildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** Bibliothek .

1. Klicken Sie **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie **[!UICONTROL Kriterien erstellen]**.

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

   1. Wählen Sie in **[!UICONTROL Dropdown-Liste]** Algorithmus auswählen) **[!UICONTROL Benutzerdefinierte Kriterien]** aus.

   1. Wählen Sie in **[!UICONTROL Dropdown]** Liste „Algorithmus“ die Option **[!UICONTROL Benutzerdefinierter Algorithmus]** aus.

      >[!NOTE]
      >
      >Durch die vorherigen Schritte wird [!UICONTROL &#x200B; Abschnitt &#x200B;]CSV hochladen“ unten im Dialogfeld [!UICONTROL Neue Kriterien erstellen] angezeigt.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Sicherungsinhalt](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) aus.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Einschlussregeln](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) aus.

1. Wählen Sie im **[!UICONTROL CSV hochladen]** den **[!UICONTROL Speicherort]** Ihrer CSV-Datei aus.

   ![Abschnitt „CSV hochladen“](assets/upload-csv.png)

   Die CSV-Datei muss korrekt formatiert sein, um erfolgreich hochgeladen werden zu können. Klicken Sie auf **[!UICONTROL CSV-Vorlage herunterladen]**, um eine Vorlage mit richtiger Formatierung zu erhalten.

   Es gibt für Orte zwei Optionen:

   * **FTP:** Um Ihre CSV-Datei von einem FTP-Server hochzuladen, wählen Sie **[!UICONTROL FTP]** aus und geben Sie dann die erforderlichen Informationen ein. Sie können SSL verwenden, das das FTPS-Protokoll verwendet, um Ihre CSV-Datei sicher zu übertragen.
   * **URL:** Um Ihre CSV-Datei über eine URL hochzuladen, wählen Sie **[!UICONTROL URL]** aus und geben Sie dann eine Feed-URL ein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Zu beachten

* Benutzerdefinierte Kriterienentitäten (Zeilen) können bis zu 1.000 empfohlene Elemente (Spalten) enthalten.

* Benutzerspezifische Kriterienupdates sind standardmäßig kumulativ. Neue Schlüssel-Wert-Paare, die in der CSV-Uploaddatei angegeben werden, überschreiben bestehende Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, für die im CSV-Upload keine Schlüssel angegeben sind, sind weiterhin verfügbar und laufen in 31 Tagen ab dem Zeitpunkt ab, an dem sie zuletzt als Teil der CSV-Datei hochgeladen werden.

  Wenden Sie sich an Adobe Client Care, um die Einstellung zum Verwerfen bestehender Ergebnisse, die nicht im nächsten CSV-Upload enthalten sind, zu aktivieren. Wenn diese Einstellung aktiviert ist, sind nur die in der benutzerdefinierten CSV-Feed-Datei vorhandenen Schlüssel für die Bereitstellung verfügbar. Diese Einstellung gilt für alle benutzerspezifischen Kriterien.

* Benutzerspezifische Kriterien-Feeds werden alle 24 Stunden aktualisiert.

  Der Upload- und Synchronisierungsstatus Ihres benutzerdefinierten Kriterien-Uploads wird unten auf jeder Kriterienkarte auf der Seite [!UICONTROL Recommendations] > [!UICONTROL Kriterien] angezeigt. Sie können den Status auch im Dialogfeld [!UICONTROL Bearbeiten] sehen, wenn Sie benutzerdefinierte Kriterien bearbeiten.

* Der Fluss für einen fehlerfreien Upload sollte [!UICONTROL Geplant] > [!UICONTROL Feed-Datei herunterladen] > [!UICONTROL Importieren] > [!UICONTROL Erfolgreich] sein.

* Die folgenden Fehlermeldungen können angezeigt werden, wenn [!DNL Target] beim Hochladen auf ein Problem stößt:

  | Fehlermeldung | Details |
  |--- |--- |
  | Unbekannter Fehler | Zeigt einen internen technischen Fehler an. |
  | Parsing-Fehler | Es gibt wahrscheinlich ein Problem mit dem Feed-Dateiformat. Korrigieren Sie das Dateiformat und speichern Sie den Algorithmus erneut, wodurch der Dateidownload-Prozess neu gestartet wird. |
  | Server nicht gefunden | Geben Sie einen IP- oder Hostnamen an, der im Internet sichtbar ist. |
  | Zugangsdatenfehler | Geben Sie einen gültigen Benutzernamen und ein gültiges Passwort für ein aktives Konto auf dem Server an. |
  | Verzeichnis nicht gefunden | Geben Sie ein Verzeichnis an, das auf dem Server existiert. |
  | Datei nicht gefunden | Geben Sie den Namen einer Datei an, die auf dem Server im angegebenen Verzeichnis existiert. |

## Schulungsvideo: Erstellen von Kriterien in Recommendations (12:33) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen (Details zum Hochladen benutzerdefinierter Kriterien beginnen bei 11:43):

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
