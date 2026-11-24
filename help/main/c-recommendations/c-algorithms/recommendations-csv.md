---
keywords: Erstellen benutzerdefinierter Kriterien;Algorithmen;Kriterien;Recommendations-Kriterien;CSV;FTP;SFTP;CSV hochladen
description: Erfahren Sie, wie Sie eine CSV-Datei hochladen, um Recommendations in Adobe [!DNL Target] Recommendations anzupassen.
title: Hochladen benutzerdefinierter Kriterien
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
TQID: 'https://experienceleague.adobe.com/8gSKOQxHGB5TPe6vdhjgy5sAFxN8O7dodITo7wgrR50'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 14%
---
# Hochladen benutzerdefinierter Kriterien {#upload-custom-criteria}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine CSV-Datei mit Empfehlungen hochladen, um benutzerdefinierte Kriterien in [!DNL Adobe Target Recommendations] zu erstellen.

>[!ENDSHADEBOX]

Benutzerdefinierte Kriterien verwenden eine CSV-Datei mit Empfehlungen, die in [!DNL Target] hochgeladen wird. Auf diese Weise können Empfehlungen, die außerhalb von [!DNL Target] berechnet wurden, in [!DNL Recommendations] Aktivitäten bereitgestellt werden. Weitere Informationen zur Funktionsweise benutzerdefinierter Kriterien finden Sie unter [Die Wissenschaft hinter den Empfehlungsalgorithmen von Target](/help/main/c-recommendations/c-algorithms/recommendations-algorithms.md).

Benutzerdefinierte Kriterien werden auf dem Bildschirm **[!UICONTROL Neue Kriterien erstellen]** erstellt. Informationen zum Aufrufen dieses Bildschirms finden Sie unter [Zugriff auf den Bildschirm Neue Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#access-create-criteria). Die folgenden Schritte beginnen im Bildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** Bibliothek .

1. Klicken Sie **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**.

   ![Kriterienseite mit geöffnetem Menü „Kriterien erstellen“, das die Optionen „Kriterien erstellen“ und „Kriteriensequenz erstellen“ anzeigt](../assets/criteria_create_1.png)

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Wählen Sie in **[!UICONTROL Dropdown-Liste]** Algorithmustyp auswählen“ **[!UICONTROL Benutzerdefinierte Kriterien]** aus. Wählen Sie in **[!UICONTROL Dropdown]** Liste „Algorithmus“ die Option **[!UICONTROL Benutzerdefinierter Algorithmus]** aus.

   ![Abschnitt Recommendations-Algorithmus mit benutzerdefinierten Kriterien als Algorithmustyp und benutzerdefiniertem Algorithmus als Algorithmus](../assets/criteria_create_9.png)

1. (Bedingt) Füllen Sie die Informationen in den Abschnitten [Backup-](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) und [Einschlussregeln](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) aus.

1. Wählen Sie im **[!UICONTROL CSV hochladen]** den **[!UICONTROL Speicherort]** der CSV-Datei aus.

   Die CSV-Datei muss korrekt formatiert sein, um erfolgreich hochgeladen werden zu können. Um eine korrekt formatierte CSV-Datei zu erhalten, klicken Sie auf **[!UICONTROL CSV-Vorlage herunterladen]**.

   Die folgenden Speicherortoptionen sind verfügbar:

   * **FTP**: Um die CSV-Datei von einem FTP-Server hochzuladen, wählen Sie **[!UICONTROL FTP]** aus und geben Sie dann die erforderlichen Informationen ein. SSL kann verwendet werden, das das FTPS-Protokoll verwendet, um die CSV-Datei sicher zu übertragen.

   * **SFTP**: Um die CSV-Datei von einem SFTP-Server hochzuladen, wählen Sie **[!UICONTROL SFTP]** aus und geben Sie dann den Host-Namen oder die IP-Adresse, den Port (standardmäßig 22), den Benutzernamen, ein Kennwort und/oder den privaten SSH-Schlüssel, das Verzeichnis und den Dateinamen ein. Weitere Informationen finden Sie unter [Unterstützte SFTP-Server-Einstellungen](/help/main/c-recommendations/c-products/feeds.md#steps).

     Das CSV-Format für benutzerdefinierte Kriterien wird durch SFTP nicht geändert. Verwenden Sie das `# Key,Recommendation_1,...`. Eine CSV-Datei im Format eines anderen Feed-Typs führt dazu, dass der Import fehlschlägt.

   * **URL**: Um die CSV-Datei über eine URL hochzuladen, wählen Sie **[!UICONTROL URL]** aus und geben Sie dann eine Feed-URL ein.

     ![Abschnitt „CSV hochladen“ mit hervorgehobenen Speicherortoptionen „FTP“, „SFTP“ und „URL“ und ausgewählter „SFTP“](../assets/criteria_create_10.png)

1. Klicken Sie **[!UICONTROL Erstellen]**.

## Zu beachten

* Benutzerdefinierte Kriterienentitäten (Zeilen) können bis zu 1.000 empfohlene Elemente (Spalten) enthalten.

* Aktualisierungen benutzerdefinierter Kriterien sind standardmäßig „kumulativ“. Neue Schlüssel-Wert-Paare in der CSV-Upload-Datei überschreiben vorhandene Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, deren Schlüssel nicht im CSV-Upload enthalten sind, stehen weiterhin zur Bereitstellung zur Verfügung und laufen 31 Tage nach dem letzten Hochladen als Teil der CSV-Datei ab.

  Um vorhandene Ergebnisse zu verwerfen, die nicht im nächsten CSV-Upload enthalten sind, wenden Sie sich an die Kundenunterstützung, um die entsprechende Einstellung zu aktivieren. Wenn diese Einstellung aktiviert ist, sind nur die in der benutzerdefinierten CSV-Feed-Datei vorhandenen Schlüssel für die Bereitstellung verfügbar. Diese Einstellung gilt für alle benutzerspezifischen Kriterien.

* Benutzerspezifische Kriterien-Feeds werden alle 24 Stunden aktualisiert.

  Der Upload- und Synchronisierungsstatus jedes benutzerdefinierten Kriterien-Uploads wird auf der Seite **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** angezeigt. Der Status wird auch im Dialogfeld **[!UICONTROL Bearbeiten]** angezeigt, wenn benutzerdefinierte Kriterien bearbeitet werden.

* Der Fluss für einen fehlerfreien Upload ist **[!UICONTROL Geplant]** > **[!UICONTROL Feed-Datei herunterladen]** > **[!UICONTROL Importieren]** > **[!UICONTROL Erfolgreich]**.

* Wenn [!DNL Target] beim Hochladen auf ein Problem stößt, sind die folgenden Fehlermeldungen möglich:

  | Fehlermeldung | Details |
  |--- |--- |
  | Unbekannter Fehler | Zeigt einen internen technischen Fehler an. |
  | Parsing-Fehler | Es gibt wahrscheinlich ein Problem mit dem Feed-Dateiformat. Korrigieren Sie das Dateiformat und speichern Sie den Algorithmus erneut, wodurch der Datei-Download-Prozess neu gestartet wird. |
  | Server nicht gefunden | Geben Sie eine IP-Adresse oder einen Hostnamen an, die bzw. der im Internet sichtbar ist. |
  | Zugangsdatenfehler | Geben Sie einen gültigen Benutzernamen und ein gültiges Passwort für ein aktives Konto auf dem Server an. |
  | Verzeichnis nicht gefunden | Geben Sie ein Verzeichnis an, das auf dem Server existiert. |
  | Datei nicht gefunden | Geben Sie den Namen einer Datei an, die auf dem Server im angegebenen Verzeichnis vorhanden ist. |
