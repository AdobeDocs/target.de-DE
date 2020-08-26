---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: Durch die Verwendung von Adobe Analytics als verhaltensbasierte Datenquelle können Kunden die Ansichten- und/oder kaufbasierten Verhaltensdaten von Analytics in Adobe Recommendations verwenden.
title: Verwenden von Adobe Analytics mit Zielgruppe Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: abe28722199c74c8b57dbfd0ca893dbf2e862cad
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 2%

---


# Adobe Analytics mit Recommendations verwenden

Mithilfe [!DNL Adobe Analytics] der Verhaltensdatenquelle können Kunden die auf Ansichten und/oder Einkäufen basierenden Verhaltensdaten aus [!DNL Analytics] den Recommendations-Aktivitäten verwenden [!DNL Adobe Target] . Diese Funktion ist besonders hilfreich in Situationen, in denen die [!DNL Target Recommendations] Einrichtung neu ist und viele historische Daten genutzt werden [!DNL Analytics] müssen.

Die Verwendung [!DNL Analytics] als verhaltensbasierte Datenquelle kann als umfassende Informationsquelle über das Benutzerverhalten dienen. Dies kann Daten aus einer Drittanbieter-Quelle oder einem Feed beinhalten, die/der nur für [!DNL Analytics]Benutzer freigegeben wird.

Beim [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations gibt es zwei Optionsfelder, mit denen Sie auswählen können, welche Datenquelle verwendet werden soll: [!UICONTROL mboxes] oder [!UICONTROL Analytics].

![Schaltflächen für die verhaltensbasierte Datenquelle](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>Wenn diese beiden Schaltflächen nicht in Ihrem Konto angezeigt werden, wenden Sie sich an den [Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Nutzungsszenarios

Die Verwendung [!DNL Analytics] als Verhaltensdatenquelle für Empfehlungen bietet außerdem die Möglichkeit, bestimmte Anwendungsfälle bereitzustellen, ohne dass Entitätsseiten mit allen [!DNL Target] Entitätsparametern versehen werden müssen. Obwohl dies bestimmte Voraussetzungen erfordert, ist die Verfügbarkeit von &quot;Produktvariablen&quot;das wichtigste Element, damit diese Funktion reibungslos funktioniert. Reguläre eVars und Props reichen nicht aus, damit dieser Handshake automatisch zwischen [!DNL Analytics] und [!DNL Target]erfolgt.

Sie können [!DNL Analytics] als Verhaltensdatenquelle Folgendes verwenden:

* Zeigen Sie Benutzern auf einer PDP-Seite Empfehlungen auf einer für den Handel bestimmten Site an, je nachdem, was andere Benutzer im letzten Monat mit Analytics-Daten von derselben Kategorie gekauft haben.
* Zeigen Sie Inhalte auf dem Startbildschirm einer Mediensite für die beliebtesten Inhalte einer bestimmten Kategorie an, die aktuell auf der Grundlage von [!DNL Analytics] Daten als Trend fungiert.

## Implementierung in Analytics

Die folgenden Abschnitte unterstützen Sie bei der Implementierung dieser Funktion auf der [!DNL Analytics] Seite.

### Voraussetzungen: Produktvariablen in Analytics

Sie müssen Produktvariablen in [!DNL Analytics] die erforderlichen Attribute implementieren, für die [!DNL Target Recommendations]dies erforderlich ist.

Ein [!DNL Target Recommendations] Beispiel-Feed-Format dient als Leitfaden, an dem alle Attribute in den Produktvariablen definiert werden müssen. Später müssen diese Werte innerhalb der [!DNL Target] Benutzeroberfläche für die jeweiligen [!DNL Target] Entitätswerte &quot;zugeordnet&quot;werden.

>[!NOTE]
>
>Wenn es sich um eine Content-Site handelt, müssen die entsprechenden Inhaltselemente als &quot;Produkte&quot;und zugehörige Attribute zu diesem Inhalt behandelt werden (Beispiel: Autorenname, Veröffentlichungsdatum, Inhaltstitel, Veröffentlichungsmonat usw.) muss als Attribute weitergegeben werden. Die Granularität der Kategorie oder der Kategorie sollte vom Unternehmen auf der Grundlage von Anwendungsfällen festgelegt werden.

Weitere Informationen zum Einrichten von Produktvariablen finden Sie unter [Produkte](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/products.html) im *Analytics-Implementierungshandbuch*. Einige der Hinweise in dieser Dokumentation erfordern einen Ermessensspielraum des Teams, das sie bereitstellt (Beispiel: Kategorie). Es wird immer empfohlen, sich vor dieser Aktivität mit der Adobe zu beraten.

### Zu beachten

[!DNL Analytics] Daten werden über einen täglichen Feed gesendet. Es dauert bis zu 24 Stunden, bis die Ergebnisse der Empfehlungen auf Ihrer Site widergespiegelt werden. Wie bei allen [!DNL Recommendations] Kriterieneinstellungen kann und sollte diese Datenquelle getestet werden.

Für eine schnelle Entscheidungsfindung darüber, welche Datenquelle verwendet werden soll, wenn täglich viele organische Daten von Benutzern generiert werden und keine große Abhängigkeit von historischen Daten erforderlich ist, kann eine [!DNL Target] Mbox als verhaltensbasierte Datenquelle gut geeignet sein. In Fällen, in denen die Verfügbarkeit organischer Daten, die kürzlich generiert wurden, geringer ist, wenn Sie auf [!DNL Analytics] Daten zurückgreifen möchten, ist die Verwendung [!DNL Analytics] als verhaltensbasierte Datenquelle eine gute Wahl.

### Schritte zur Bereitstellung

Gehen Sie wie folgt vor, wenn alle Voraussetzungen erfüllt sind:

1. Klicken Sie [!DNL Target]auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** , um Ihren [!DNL Target] Clientcode zu erhalten.

   ![Clientcode](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. Erwerben Sie Ihre [!DNL Analytics] Report Suite.

   Verwenden Sie die Report Suite Ihrer [!DNL Analytics] Produktions-Site. Dies ist die Report Suite, die die Site verfolgt, auf der Sie [!DNL Recommendations] bereitgestellt haben.

1. Klicken Sie [!DNL Analytics]in &quot; **[!UICONTROL Admin]** &quot;> &quot; **[!UICONTROL Datenfeeds]**&quot;.

   ![Einstellungen > Datenfeeds](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. Click **[!UICONTROL Add]** to create a new feed.

   ![hinzufügen](/help/c-recommendations/c-algorithms/assets/add-feed.png)

1. Füllen Sie die Feed-Informationen aus:

   * **Name**: Recs Prod Feed
   * **Report Suite**: Ihre vorab festgelegte Report Suite
   * **E-Mail**: Geben Sie eine geeignete Adresse für einen Admin-Benutzer an
   * **Feed-Intervall**: Wählen Sie das gewünschte Intervall
   * **Verarbeitung** verzögern: Keine Verzögerung.
   * **Beginns- und Enddaten**: Kontinuierlicher Feed

   ![Feed-Informationen](/help/c-recommendations/c-algorithms/assets/feed-information.png)

1. Fill in the details in the **[!UICONTROL Destination]** section:

   >[!NOTE]
   > 
   >Sprechen Sie mit dem [!DNL Adobe Analytics] Team, bevor Sie diesen Schritt durchführen.

   * **Typ**: FTP
   * **Host**: xxx.yyy.com
   * **Pfad**: Ihr Zielgruppe-Client-Code
   * **Benutzername**: xxxyyy
   * **Kennwort**: xxxxxxxxxxx

   Screenshot dient nur zu Referenzzwecken. Ihre Bereitstellung hat andere Anmeldeinformationen. Wenden Sie sich bei diesem Schritt an das [!DNL Adobe Analytics] Team oder den Kundendienst.

   ![Zielabschnitt](/help/c-recommendations/c-algorithms/assets/destination.png)

1. Füllen Sie die **[!UICONTROL Datenspaltendefinitionen]** aus:

   * **Komprimierungsformat**: Gzip
   * **Verpackungstyp**:  Einzeldatei
   * **Manifest:** Datei beenden

      ![Einstellungen für Komprimierungsformat, Verpackungstyp und Manifest](/help/c-recommendations/c-algorithms/assets/compression.png)

   * **Spalten einschließen**:

      >[!IMPORTANT]
      >
      >Die Spalten müssen in der hier beschriebenen Reihenfolge hinzugefügt werden. Wählen Sie die Spalten in der folgenden Reihenfolge aus und klicken Sie für jede Spalte auf **[!UICONTROL Hinzufügen]** .

      * hit_time_gmt
      * visid_high
      * visid_low
      * event_list
      * product_list
      * visit_num

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Datenspaltendefinitionsabschnitt](/help/c-recommendations/c-algorithms/assets/data-column-definitions.png)

Damit ist das auf der [!DNL Analytics] Seite eingerichtete Setup abgeschlossen. Jetzt ist es an der Zeit, diese Variablen für eine kontinuierliche Bereitstellung von Verhaltensdaten [!DNL Target] nebeneinander zu ordnen.

## Umsetzung in Zielgruppe

1. Klicken Sie in Zielgruppe auf **[!UICONTROL Recommendations]** und dann auf die Registerkarte **[!UICONTROL Feeds]** .

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Klicken Sie auf Feed **[!UICONTROL erstellen]**.

1. Wählen Sie **[!UICONTROL Analytics-Klassifizierungen]** und geben Sie dann die Report Suite an.

   ![Option &quot;Analytics-Klassifizierungen&quot;](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Klicken Sie auf **[!UICONTROL Zuordnung]** und ordnen Sie dann die Spaltenüberschriften der Felder den entsprechenden [!UICONTROL Recommendations] -Feldnamen zu.

   ![Zuordnungsabschnitt](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.