---
keywords: Erstellen benutzerdefinierter Kriterien; Algorithmen; Kriterien; Empfehlungskriterien; csv; ftp; CSV hochladen
description: Erfahren Sie, wie Sie eine CSV-Datei hochladen, um Ihre Empfehlungen in Adobe [!DNL Target] Recommendations anzupassen.
title: Wie lade ich benutzerdefinierte Kriterien in hoch [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: ce974152-c83e-46cb-b1cd-c5e2d10c5436
source-git-commit: b7c7e8d85f7f39024ed5e57177e5c9f628460e9c
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 33%

---

# Hochladen benutzerdefinierter Kriterien

Laden Sie eine CSV-Datei hoch, um Ihre Empfehlungen in [!DNL Adobe Target] anzupassen.

Es gibt mehrere Möglichkeiten, den [!UICONTROL Create New Criteria] zu erreichen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliothek auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations] mit dem [!UICONTROL Visual Experience Composer] (VEC) erstellen, gelangen Sie sofort zum [!UICONTROL Select Criteria], nachdem Sie ein Element auf Ihrer Seite ausgewählt und auf [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before] oder [!UICONTROL Insert Recommendations After] geklickt haben. Anschließend können Sie ein verfügbares Kriterium auswählen oder auf **[!UICONTROL Create Criteria]** klicken. Wenn Sie neue Kriterien erstellen, können Sie Ihre Kriterien zur Verwendung mit anderen [!DNL Recommendations] speichern. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Wenn Sie eine [!DNL Recommendations] bearbeiten, klicken Sie in ein [!UICONTROL Recommendations Location] auf Ihrer Seite und wählen Sie **[!UICONTROL Change Criteria]** aus. Klicken Sie auf dem Bildschirm [!UICONTROL Select Criteria] auf **[!UICONTROL Create Criteria]**. Sie können Ihre neuen Kriterien zur Verwendung mit anderen [!DNL Recommendations] speichern.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie auf den [!UICONTROL Create New Criteria] über die erste Methode zugreifen: den Bildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliothek .

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Select Algorithm Type]** die Option **[!UICONTROL Custom Criteria]** aus.

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Algorithm]** die Option **[!UICONTROL Custom Algorithm]** aus.

   >[!NOTE]
   >
   >Durch die vorherigen Schritte wird der Abschnitt [!UICONTROL Upload CSV] unten im Dialogfeld [!UICONTROL Create Criteria] angezeigt.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Sicherungsinhalt](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) aus.

1. (Bedingt) Füllen Sie die Informationen im Abschnitt [Einschlussregeln](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) aus.

1. Wählen Sie im Abschnitt **[!UICONTROL Upload CSV]** den **[!UICONTROL Location]** Ihrer CSV-Datei aus.

Die CSV-Datei muss korrekt formatiert sein, um erfolgreich hochgeladen werden zu können. Klicken Sie auf **[!UICONTROL Download the CSV template]** , um eine korrekt formatierte CSV-Datei zu erhalten.

Es gibt für Orte zwei Optionen:

    * **FTP:** Um Ihre CSV-Datei von einem FTP-Server hochzuladen, wählen Sie **[!UICONTROL FTP]** aus und geben Sie dann die erforderlichen Informationen ein. Sie können SSL verwenden, das das FTPS-Protokoll verwendet, um Ihre CSV-Datei sicher zu übertragen.
    
    * **URL:** Um Ihre CSV-Datei über eine URL hochzuladen, wählen Sie **[!UICONTROL URL]** aus und geben Sie dann eine Feed-URL ein.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Zu beachten

* Benutzerdefinierte Kriterienentitäten (Zeilen) können bis zu 1.000 empfohlene Elemente (Spalten) enthalten.

* Benutzerspezifische Kriterienupdates sind standardmäßig kumulativ. Neue Schlüssel-Wert-Paare, die in der CSV-Uploaddatei angegeben werden, überschreiben bestehende Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, für die im CSV-Upload keine Schlüssel angegeben sind, sind weiterhin verfügbar und laufen in 31 Tagen ab dem Zeitpunkt ab, an dem sie zuletzt als Teil der CSV-Datei hochgeladen werden.

  Wenden Sie sich an Adobe Client Care, um die Einstellung zum Verwerfen bestehender Ergebnisse, die nicht im nächsten CSV-Upload enthalten sind, zu aktivieren. Wenn diese Einstellung aktiviert ist, sind nur die in der benutzerdefinierten CSV-Feed-Datei vorhandenen Schlüssel für die Bereitstellung verfügbar. Diese Einstellung gilt für alle benutzerspezifischen Kriterien.

* Benutzerspezifische Kriterien-Feeds werden alle 24 Stunden aktualisiert.

  Auf der Seite [!UICONTROL Recommendations] > [!UICONTROL Criteria] wird für jedes Kriterium der Upload- und Synchronisierungsstatus der benutzerdefinierten Kriterien angezeigt. Sie können den Status auch im Dialogfeld [!UICONTROL Edit] beim Bearbeiten benutzerdefinierter Kriterien sehen.

* Der Fluss für einen fehlerfreien Upload sollte [!UICONTROL Scheduled] > [!UICONTROL Downloading Feed File] > [!UICONTROL Importing] > [!UICONTROL Successful] sein.

* Die folgenden Fehlermeldungen können angezeigt werden, wenn [!DNL Target] beim Hochladen auf ein Problem stößt:

  | Fehlermeldung | Details |
  |--- |--- |
  | Unbekannter Fehler | Zeigt einen internen technischen Fehler an. |
  | Parsing-Fehler | Es gibt wahrscheinlich ein Problem mit dem Feed-Dateiformat. Korrigieren Sie das Dateiformat und speichern Sie den Algorithmus erneut, wodurch der Datei-Download-Prozess neu gestartet wird. |
  | Server nicht gefunden | Geben Sie einen IP- oder Hostnamen an, der im Internet sichtbar ist. |
  | Zugangsdatenfehler | Geben Sie einen gültigen Benutzernamen und ein gültiges Passwort für ein aktives Konto auf dem Server an. |
  | Verzeichnis nicht gefunden | Geben Sie ein Verzeichnis an, das auf dem Server existiert. |
  | Datei nicht gefunden | Geben Sie den Namen einer Datei an, die auf dem Server im angegebenen Verzeichnis existiert. |
