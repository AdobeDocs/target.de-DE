---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Laden Sie eine CSV-Datei hoch, um Empfehlungen anzupassen.
title: Hochladen benutzerdefinierter Kriterien
feature: criteria
uuid: e0b4d320-db00-43ad-b49e-ce36c8532320
translation-type: tm+mt
source-git-commit: 66b3c42181daf582c9b3bee1f83a2229b823c5c3
workflow-type: tm+mt
source-wordcount: '1873'
ht-degree: 66%

---


# ![PREMIUM](/help/assets/premium.png) Upload benutzerdefinierter Kriterien{#upload-custom-criteria}

Laden Sie eine CSV-Datei hoch, um Empfehlungen anzupassen.

## Auf den Bildschirm &quot;Neue Kriterien erstellen&quot;zugreifen

Sie haben viele Möglichkeiten, um auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations] Aktivität mit dem [!UICONTROL Visual Experience Composer] (VEC) erstellen, werden Sie sofort zum Bildschirm &quot;Kriterien  auswählen&quot;geleitet, nachdem Sie ein Element auf Ihrer Seite ausgewählt haben und auf &quot;Mit Recommendations ersetzen&quot;, &quot;Recommendations vor [!UICONTROL einfügen&quot;oder &quot;Recommendations nach]einfügen&quot;klicken. Sie können dann ein verfügbares Kriterium auswählen oder auf Kriterien **[!UICONTROL erstellen]** klicken. Wenn Sie ein neues Kriterium erstellen, haben Sie die Möglichkeit, Ihre Kriterien zur Verwendung mit anderen [!DNL Recommendations] Aktivitäten zu speichern. For more information, see [Create a Recommendations activity](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Klicken Sie beim Bearbeiten einer [!DNL Recommendations]Aktivität in ein Feld für die [!UICONTROL Empfehlungsposition] auf Ihrer Seite und wählen Sie **[!UICONTROL Kriterien ändern]**. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create Criteria]**. Sie können Ihre neuen Kriterien speichern, um Sie mit anderen [!DNL Recommendations]-Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mithilfe der ersten Methode auf den Bildschirm &quot;Neue Kriterien [!UICONTROL erstellen] &quot;zugreifen: den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** .

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf Kriterien **[!UICONTROL erstellen]** > Benutzerspezifische Kriterien **[!UICONTROL hochladen]**.

1. Konfigurieren Sie die Informationen in den folgenden Abschnitten.

## Basisinformationen  {#info}

1. Geben Sie einen **[!UICONTROL Kriteriennamen]** ein.

   Dies ist der „interne“ Name, der für die Beschreibung der Kriterien verwendet wird. Sie möchten zum Beispiel Ihre Kriterien „Produkte mit der höchsten Marge“ nennen, Sie möchten jedoch nicht, dass dieser Titel öffentlich angezeigt wird. Sehen Sie sich den nächsten Schritt an, um den öffentlichen Titel festzulegen.

   ![Abschnitt &quot;Grundlegende Informationen&quot;](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. Geben Sie einen öffentlichen **[!UICONTROL Anzeigetitel]** ein, der auf der Seite für alle Empfehlungen angezeigt wird, die diesen Kriterien entsprechen.

   So wäre es möglicherweise sinnvoll, „Personen, die das ansahen, sahen auch dies an“ oder „Ähnliche Produkte“ einzublenden, wenn Sie diese Kriterien zum Einblenden von Empfehlungen verwenden.

1. Geben Sie eine kurze **[!UICONTROL Beschreibung]** des Kriteriums ein.

   Die Beschreibung sollte Ihnen dabei helfen, die Kriterien zu identifizieren, und kann Informationen über den Zweck der Kriterien enthalten.

1. Wählen Sie eine **[!UICONTROL Branche]** aus:

   * [!UICONTROL Einzelhandel/E-Commerce]
   * [!UICONTROL Lead-Generierung/B2B/Finanzdienstleistungen]
   * [!UICONTROL Medien/Verlagswesen]

   Andere Optionen für Kriterien ändern sich auf Grundlage des vertikalen Markts, den Sie auswählen.

1. Wählen Sie einen **[!UICONTROL Seitentyp]** aus.

   Verschiedene Seitentypen stehen zur Verfügung.

   Vertikaler Markt und Seitentyp werden zusammen genutzt, um Ihre gespeicherten Kriterien zu kategorisieren, wodurch die Wiederverwendung der Kriterien für andere [!DNL Recommendations]-Aktivitäten erleichtert wird.

1. Wählen Sie einen **[!UICONTROL Empfehlungsschlüssel]** aus.

   Weitere Informationen zum Stützen von Kriterien auf einen Schlüssel finden Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. Wählen Sie die **[!UICONTROL Empfehlungslogik]** aus.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](../../c-recommendations/c-algorithms/algorithms.md).

   >[!NOTE]
   >
   >If you select **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]**, you will have the option to set [content similarity rules](#similarity).

## Inhalt {#content}

Content rules determine what happens if the number of recommended items does not fill your [recommendations design](/help/c-recommendations/c-design-overview/design-overview.md). Möglicherweise geben [!DNL Recommendations]-Kriterien weniger Empfehlungen zurück, als im Entwurf angegeben sind. Wenn Ihr Entwurf z. B. Slots für vier Elemente enthält, Ihre Kriterien jedoch nur zwei Artikel empfehlen, können Sie die verbleibenden Slots leer lassen oder Reserveempfehlungen verwenden, um die zusätzlichen Slots zu füllen.

![Inhaltsabschnitt](/help/c-recommendations/c-algorithms/assets/content.png)

1. (Optional) Schieben Sie den Umschalter für die **[!UICONTROL teilweise]** Entwurfswiedergabe an die Position &quot;Ein&quot;.

   Es werden so viele Plätze wie möglich ausgefüllt, die Designvorlage kann jedoch Leerzeichen für die verbleibenden Plätze enthalten. Wenn diese Option deaktiviert ist und nicht genügend Inhalte vorhanden sind, um alle verfügbaren Plätze auszufüllen, werden keine Empfehlungen bereitgestellt und stattdessen Standardinhalte angezeigt.

   Aktivieren Sie diese Option, wenn Empfehlungen mit leeren Slots versorgt werden sollen. Verwenden Sie Reserveempfehlungen, wenn Sie möchten, dass Empfehlungszeiträume mit Inhalten gefüllt werden, die auf Ihren Kriterien basieren und mit leeren Slots gefüllt werden, die mit ähnlichen oder beliebten Inhalten Ihrer Site gefüllt sind, wie im nächsten Schritt beschrieben.

1. (Optional) Schieben Sie den Umschalter &quot;Sicherung **[!UICONTROL anzeigen&quot;Recommendations]** auf die &quot;Ein&quot;-Position.

   Füllen Sie alle verbleibenden leeren Slots im Design mit einer zufälligen Auswahl der am häufigsten angezeigten Produkte aus Ihrer gesamten Site.

   Die Verwendung von Reserveempfehlungen stellt sicher, dass Ihr Empfehlungsentwurf alle verfügbaren Plätze ausfüllt. Angenommen, Sie haben ein Design im Format 4 x 1, wie unten dargestellt:

   ![4 x 1 Design](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Nehmen wir einmal an, Ihre Kriterien führen dazu, dass nur zwei Artikel empfohlen werden. Wenn Sie die Option &quot; [!UICONTROL Teilweises Design-Rendering] &quot;aktivieren, werden die ersten beiden Slots ausgefüllt, aber die restlichen zwei Slots bleiben leer. Wenn Sie jedoch die Option &quot;Recommendations [!UICONTROL Sicherung] anzeigen&quot;aktivieren, werden die ersten beiden Slots nach Ihren angegebenen Kriterien ausgefüllt und die restlichen zwei Slots werden basierend auf Ihren Reserveempfehlungen ausgefüllt.

   Die folgende Matrix zeigt das Ergebnis, das Sie bei Verwendung der [!UICONTROL Optionen für das Rendering] und [!UICONTROL Backup von Recommendations] bei partiellen Designs beobachten werden:

   | Teilweises Entwurfs-Rendering | Ersatzempfehlungen | Ergebnis |
   |--- |--- |--- |
   | Deaktiviert | Deaktiviert | Wenn weniger Empfehlungen zurückgegeben werden als im Entwurf vorgesehen, wird der Empfehlungsentwurf durch Standardinhalte ersetzt und es erscheinen keine Empfehlungen. |
   | Aktiviert | Deaktiviert | Der Entwurf wird gerendert, kann jedoch leere Positionen enthalten, falls weniger Empfehlungen zurückgegeben werden, als im Entwurf vorgesehen. |
   | Aktiviert | Aktiviert | Ersatzempfehlungen erscheinen an solchen leeren Positionen und vervollständigen den Entwurf.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf nur teilweise gerendert.<br>In dem Fall, dass die Kriterien keine Empfehlungen zurückgeben und die Einschlussregeln die Ersatzempfehlungen auf null reduzieren, wird der Entwurf durch Standardinhalte ersetzt. |
   | Deaktiviert | Aktiviert | Ersatzempfehlungen erscheinen an solchen leeren Positionen und vervollständigen den Entwurf.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf durch Standardinhalte ersetzt und es werden keine Empfehlungen angezeigt. |

   Weitere Informationen finden Sie unter [Verwenden einer Reserveempfehlung](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (Bedingt) Wenn Sie im vorherigen Schritt die Option Backup-Recommendations **** anzeigen ausgewählt haben, können Sie Einschlussregeln **[!UICONTROL anwenden aktivieren, um Reserveempfehlungen]** zu erstellen.

   Einschlussregeln bestimmen, welche Artikel in Ihren Empfehlungen enthalten sind. Die verfügbaren Optionen hängen von Ihrem vertikalen Markt ab.

   For more details, see [Specify inclusion rules](#inclusion) below.

1. (Optional) Schieben Sie den Umschalter &quot;Vorab gekaufte Artikel **[!UICONTROL empfehlen&quot;]** auf die Position &quot;Ein&quot;.

   Diese Einstellung basiert auf `productPurchasedId`. Das Standardverhalten ist es, zuvor gekaufte Artikel nicht zu empfehlen. In den meisten Fällen ist es nicht sinnvoll, Artikel zu bewerben, die Kunden kürzlich gekauft haben. Es ist nützlich, wenn Sie Artikel verkaufen, die Kunden in der Regel nur einmal kaufen, zum Beispiel Kayaks. Wenn Sie Artikel verkaufen, die Personen wiederholt kaufen, z. B. Shampoo oder andere persönliche Artikel, sollten Sie diese Option aktivieren.

## Einschlussregeln {#inclusion}

Mehrere Optionen ermöglichen es Ihnen, die in Ihren Empfehlungen angezeigten Elemente einzuschränken. Sie können Einschlussregeln beim Erstellen von Kriterien oder Promotions verwenden.

![Einschlussregeln](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

Einschlussregeln sind optional. Das Festlegen dieser Regeln jedoch ermöglicht Ihnen die bessere Steuerung der Artikel, die in Ihren Empfehlungen erscheinen. Jedes konfigurierte Detail schränkt die Anzeigekriterien weiter ein.

Beispiel: Sie können nur Damenschuhe anzeigen, deren Bestand über 50 und deren Preis zwischen 25 und 45 Euro liegt. Sie können auch jedes Attribut gewichten, sodass die für Ihr Unternehmen wichtigeren Artikel am ehesten angezeigt werden.

Weiteres Beispiel: Sie können Stellenangebote ausschließlich für Besucher Ihrer Website anzeigen, die aus bestimmten Orten stammen und über die erforderlichen Abschlüsse verfügen.

Die Optionen für die Einschlussregeln variieren je nach vertikalem Markt. Einschlussregeln werden standardmäßig auf Ersatzempfehlungen angewendet.

>[!IMPORTANT]
>
>Sie sollten mit Einschlussregeln vorsichtig umgehen. Sie sind nützlich, wenn Ihr Unternehmen beispielsweise mit Regeln arbeitet, die erfordern, dass eine Marke nicht empfohlen wird, während eine andere Marke gezeigt wird. Bei dieser Funktion kommt es jedoch zu Opportunitätskosten. Ein gewisser Lift-Prozentsatz geht möglicherweise verloren, wenn Artikel nicht angezeigt werden, die normalerweise durch die Aktivitätskriterien angezeigt werden würden.

Die Einschlussregeln werden mit „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Führen Sie zum Erstellen einer einfachen Einschlussregel die folgenden Schritte aus, um - wie im oben stehenden Beispiel - nur Damenschuhe mit einem Bestand von mehr als 50 und einem Preis von zwischen 25 und 45 € anzuzeigen.

1. Legen Sie einen Preisbereich für die Produkte fest, die Sie empfehlen möchten.
1. Legen Sie den Mindestbestand für die Produkte fest, die Sie empfehlen möchten.
1. Konfigurieren Sie die Empfehlung, um nur Artikel anzuzeigen, wenn sie bestimmte Kriterien erfüllen.

   ![](assets/Recs_InclusionRules.png)

   Sie können angeben, dass Artikel nur berücksichtigt werden, wenn eines der Attribute in der Liste eine oder mehrere angegebene Bedingungen erfüllt oder nicht erfüllt.

   Die verfügbaren Auswerter sind von dem Wert abhängig, den Sie in der ersten Dropdownliste auswählen. Sie können mehrere Elemente auflisten. Diese Artikel werden durch ODER ausgewertet.

   Mehrere Regeln werden mit „AND“ kombiniert.

   >[!NOTE]
   >
   >Diese Option beschränkt die in der Empfehlung angezeigten Elemente. Sie hat keine Auswirkungen darauf, auf welchen Seiten die Empfehlung angezeigt wird. Um eine Einschränkung bezüglich der Anzeige der Empfehlung vorzunehmen, wählen Sie die Seiten im Experience Composer aus.

For more information, see [Use dynamic and static inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## CSV hochladen

1. Wählen Sie den **[!UICONTROL Speicherort]** Ihrer CSV-Datei aus.

   ![CSV-Abschnitt hochladen](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   Die CSV-Datei muss korrekt formatiert sein, um erfolgreich hochgeladen werden zu können. Klicken Sie auf **[!UICONTROL CSV-Vorlage herunterladen]**, um eine Vorlage mit richtiger Formatierung zu erhalten.

   Es gibt für Orte zwei Optionen:

   * **FTP:** Um Ihre CSV-Datei von einem FTP-Server hochzuladen, wählen Sie **[!UICONTROL FTP]** aus und geben Sie die erforderlichen Informationen ein. Sie können optional SSL verwenden, wobei die CSV-Datei sicher mittels eines FTPS-Protokolls übermittelt wird.
   * **URL:** Um Ihre CSV-Datei von einer URL hochzuladen, wählen Sie &quot; **[!UICONTROL URL]**&quot;und geben Sie dann eine Feed-URL ein.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   >[!NOTE]
   >
   >Benutzerdefinierte Kriterienentitäten (Zeilen) können bis zu 1.000 empfohlene Elemente (Spalten) enthalten.

Benutzerspezifische Kriterienupdates sind standardmäßig kumulativ. Neue Schlüssel-Wert-Paare, die in der CSV-Uploaddatei angegeben werden, überschreiben bestehende Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, für die keine Schlüssel im CSV-Upload spezifiziert ist, können trotzdem bereitgestellt werden und laufen 31 Tagen nach dem letzten Hochladen als Teil der CSV-Datei ab.

Wenden Sie sich an Adobe Client Care, um die Einstellung zum Verwerfen bestehender Ergebnisse, die nicht im nächsten CSV-Upload enthalten sind, zu aktivieren. Wenn diese Einstellung aktiviert ist, sind nur die Schlüssel, die in der benutzerspezifischen CSV-Feed-Datei vorhanden sind, zur Bereitstellung verfügbar. Diese Einstellung gilt für alle benutzerspezifischen Kriterien.

Benutzerspezifische Kriterien-Feeds werden alle 24 Stunden aktualisiert.

Sie können den Upload- und Synchronisationsstatus Ihrer benutzerdefinierten Kriterien am Ende jeder Kriterienkarte auf der Seite „Recommendations“ > „Kriterien“ sehen. Sie können den Status auch im Dialogfeld „Bearbeiten“ sehen, wenn Sie benutzerdefinierte Kriterien bearbeiten.

Der Ablauf für einen fehlerfreien Upload sollte folgendermaßen aussehen: „Geplant“ > „Download der Feed-Datei“ > „Import“ > „Erfolgreich“.

The following are possible error messages you might receive if [!DNL Target] encounters a problem with the upload:

| Fehlermeldung | Details |
|--- |--- |
| Unbekannter Fehler | Zeigt einen internen technischen Fehler an. |
| Parsing-Fehler | Es gibt wahrscheinlich ein Problem mit dem Feed-Dateiformat. Korrigieren Sie das Dateiformat und speichern Sie den Algorithmus erneut, um den Downloadvorgang erneut zu starten. |
| Server nicht gefunden | Geben Sie einen IP- oder Hostnamen an, der im Internet sichtbar ist. |
| Zugangsdatenfehler | Geben Sie einen gültigen Benutzernamen und ein gültiges Passwort für ein aktives Konto auf dem Server an. |
| Verzeichnis nicht gefunden | Geben Sie ein Verzeichnis an, das auf dem Server existiert. |
| Datei nicht gefunden | Geben Sie den Namen einer Datei an, die auf dem Server im angegebenen Verzeichnis existiert. |

## Schulungsvideo: Kriterien in Recommendations erstellen (12:33) ![Tutorialzeichen](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen (Details zum Hochladen benutzerdefinierter Kriterien beginnen um 11:43 Uhr):

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)