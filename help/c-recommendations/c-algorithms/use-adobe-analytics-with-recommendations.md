---
keywords: Verhaltensdatenquelle;Analysen;Empfehlungen;Kriterien;Produktvariablen
description: Erfahren Sie, wie Sie Adobe Analytics als verhaltensbasierte Datenquelle verwenden, um die Ansicht- und/oder kaufbasierten Verhaltensdaten von Analytics in Zielgruppe Recommendations zu verwenden.
title: Wie verwende ich Adobe Analytics mit Zielgruppe Recommendations?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 2%

---


# Adobe Analytics mit Recommendations verwenden

Durch Verwendung von [!DNL Adobe Analytics] als verhaltensbasierte Datenquelle können Kunden die Ansicht- und/oder kaufbasierten Verhaltensdaten von [!DNL Analytics] in [!DNL Adobe Target]-Recommendations-Aktivitäten verwenden. Diese Funktion ist besonders hilfreich in Situationen, in denen das [!DNL Target Recommendations] Setup neu ist und [!DNL Analytics] viele historische Daten nutzen kann.

Die Verwendung von [!DNL Analytics] als verhaltensbasierte Datenquelle kann als umfassende Informationsquelle zum Benutzerverhalten dienen. Dies kann Daten aus einer Drittanbieter-Quelle oder einem Drittanbieter-Feed beinhalten, die/der nur für [!DNL Analytics] freigegeben wird.

Beim Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations gibt es zwei Optionsfelder, mit denen Sie auswählen können, welche Datenquelle verwendet werden soll: [!UICONTROL mboxes] oder [!UICONTROL Analytics].[

![Schaltflächen für die verhaltensbasierte Datenquelle](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>Wenn diese beiden Schaltflächen nicht in Ihrem Konto angezeigt werden, wenden Sie sich an den [Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Anwendungsfälle für Analytics-Daten in der Zielgruppe

Die Verwendung von [!DNL Analytics] als Verhaltensdatenquelle für Empfehlungen bietet außerdem die Möglichkeit, bestimmte Anwendungsfälle bereitzustellen, ohne dass Entitätsseiten mit allen [!DNL Target]-Entitätsparametern versehen werden müssen. Obwohl dies bestimmte Voraussetzungen erfordert, ist die Verfügbarkeit von &quot;Produktvariablen&quot;das wichtigste Element, damit diese Funktion reibungslos funktioniert. Reguläre eVars und Props reichen nicht aus, damit dieser Handshake automatisch zwischen [!DNL Analytics] und [!DNL Target] ausgeführt wird.

Sie können [!DNL Analytics] als verhaltensbasierte Datenquelle verwenden, um:

* Zeigen Sie Benutzern auf einer PDP-Seite Empfehlungen auf einer für den Handel bestimmten Site an, je nachdem, was andere Benutzer im letzten Monat mit Analytics-Daten von derselben Kategorie gekauft haben.
* Zeigen Sie Inhalte auf dem Startbildschirm einer Mediensite für den beliebtesten Inhalt in einer bestimmten Kategorie an, die aktuell auf [!DNL Analytics]-Daten basiert.

## Implementierung in Analytics

Die folgenden Abschnitte unterstützen Sie bei der Implementierung dieser Funktion auf der [!DNL Analytics] Seite.

### Voraussetzungen: Produktvariablen in Analytics einrichten

Sie müssen Produktvariablen in [!DNL Analytics] mit den erforderlichen Attributen implementieren, die für [!DNL Target Recommendations] erforderlich sind.

Ein Muster-Feed-Format von [!DNL Target Recommendations] dient als Leitfaden, bei dem alle Attribute in den Produktvariablen definiert werden müssen. Später müssen diese Werte in der [!DNL Target]-Benutzeroberfläche für die entsprechenden [!DNL Target]-Entitätswerte &quot;zugeordnet&quot;werden.

>[!NOTE]
>
>Wenn es sich um eine Content-Site handelt, müssen die entsprechenden Inhaltselemente als &quot;Produkte&quot;und zugehörige Attribute zu diesem Inhalt behandelt werden (Beispiel: Autorenname, Veröffentlichungsdatum, Inhaltstitel, Veröffentlichungsmonat usw.) muss als Attribute weitergegeben werden. Die Granularität der Kategorie oder der Kategorie sollte vom Unternehmen auf der Grundlage von Anwendungsfällen festgelegt werden.

Weitere Informationen zum Einrichten von Produktvariablen finden Sie unter [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) im *Analytics-Implementierungshandbuch*. Einige der Hinweise in dieser Dokumentation erfordern einen Ermessensspielraum des Teams, das sie bereitstellt (Beispiel: Kategorie). Es wird immer empfohlen, sich vor dieser Aktivität mit der Adobe zu beraten.

### Zu beachten

[!DNL Analytics] Daten werden über einen täglichen Feed gesendet. Es dauert bis zu 24 Stunden, bis die Ergebnisse der Empfehlungen auf Ihrer Site widergespiegelt werden. Wie bei allen [!DNL Recommendations]-Kriterieneinstellungen kann und sollte diese Datenquelle getestet werden.

Für eine schnelle Entscheidungsfindung darüber, welche Datenquelle verwendet werden soll, wenn täglich viele organische Daten von Benutzern generiert werden und keine große Abhängigkeit von historischen Daten erforderlich ist, kann eine [!DNL Target]-mbox als verhaltensbasierte Datenquelle gut geeignet sein. In Fällen, in denen die Verfügbarkeit organischer Daten, die kürzlich generiert wurden, geringer ist, wenn Sie auf [!DNL Analytics]-Daten zurückgreifen möchten, ist die Verwendung von [!DNL Analytics] als verhaltensbasierte Datenquelle gut geeignet.

### Schritte zur Bereitstellung

Wenn alle Voraussetzungen erfüllt sind, müssen die folgenden Aufgaben vom [!DNL Adobe Target Recommendations]-Team durchgeführt werden:

>[!IMPORTANT]
>
>Die folgenden Schritte dienen nur zur Veranschaulichung. Ein Mitglied des [!DNL Recommendations]-Teams muss diese Schritte derzeit ausführen. [Weitere Informationen erhalten Sie ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) im Kundendienst.

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**, um Ihren [!DNL Target]-Clientcode zu erhalten.

   ![Clientcode](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. Erwerben Sie Ihre [!DNL Analytics] Report Suite.

   Verwenden Sie Ihre [!DNL Analytics] Produktions-Site-Report Suite. Diese Report Suite verfolgt die Site, auf der Sie [!DNL Recommendations] bereitgestellt haben.

1. Klicken Sie in [!DNL Analytics] auf **[!UICONTROL Admin]** > **[!UICONTROL Datenfeeds]**.

   ![Einstellungen > Datenfeeds](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. Klicken Sie auf **[!UICONTROL Hinzufügen]**, um einen neuen Feed zu erstellen.

   ![hinzufügen](/help/c-recommendations/c-algorithms/assets/add-feed.png)

1. Füllen Sie die Feed-Informationen aus:

   * **Name**: Recs Prod Feed
   * **Report Suite**: Ihre vorab festgelegte Report Suite
   * **E-Mail**: Geben Sie eine geeignete Adresse für einen Admin-Benutzer an
   * **Feed-Intervall**: Wählen Sie das gewünschte Intervall
   * **Verarbeitung** verzögern: Keine Verzögerung.
   * **Beginns- und Enddaten**: Kontinuierlicher Feed

   ![Feed-Informationen](/help/c-recommendations/c-algorithms/assets/feed-information.png)

1. Füllen Sie die Details im Abschnitt **[!UICONTROL Ziel]** aus:

   >[!NOTE]
   > 
   >Wenden Sie sich an das [!DNL Adobe Analytics]-Team, bevor Sie diesen Schritt durchführen.

   * **Typ**: FTP
   * **Host**: `xxx.yyy.com`
   * **Pfad**: Ihr  [!DNL Target] Clientcode
   * **Benutzername**: Geben Sie Ihren Benutzernamen ein
   * **Kennwort**: Kennwort angeben

   Screenshot dient nur zu Referenzzwecken. Ihre Bereitstellung hat andere Anmeldeinformationen. Wenden Sie sich bei diesem Schritt an das [!DNL Adobe Analytics]-Team oder den Kundendienst.

   ![Zielabschnitt](/help/c-recommendations/c-algorithms/assets/destination.png)

1. Füllen Sie die Definitionen für **[!UICONTROL Datenspalte]** aus:

   * **Komprimierungsformat**: Gzip
   * **Verpackungstyp**: Einzeldatei
   * **Manifest:** Finish-Datei

      ![Einstellungen für Komprimierungsformat, Verpackungstyp und Manifest](/help/c-recommendations/c-algorithms/assets/compression.png)

   * **Spalten einschließen**:

      >[!IMPORTANT]
      >
      >Die Spalten müssen in der hier beschriebenen Reihenfolge hinzugefügt werden. Wählen Sie die Spalten in der folgenden Reihenfolge aus und klicken Sie für jede Spalte auf **[!UICONTROL Hinzufügen]**.

      * hit_time_gmt
      * visid_high
      * visid_low
      * event_list
      * product_list
      * visit_num

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Datenspaltendefinitionsabschnitt](/help/c-recommendations/c-algorithms/assets/data-column-definitions.png)

Damit ist das Setup auf [!DNL Analytics] Seite abgeschlossen. Jetzt ist es an der Zeit, diese Variablen auf [!DNL Target] Seite zuzuordnen, um eine kontinuierliche Bereitstellung von Verhaltensdaten zu ermöglichen.

## Implementierung in Zielgruppe

1. Klicken Sie in der Zielgruppe auf **[!UICONTROL Recommendations]** und dann auf die Registerkarte **[!UICONTROL Feeds]**.

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Klicken Sie auf **[!UICONTROL Feed erstellen]**.

1. Wählen Sie **[!UICONTROL Analytics-Klassifizierungen]** und geben Sie dann die Report Suite an.

   ![Option &quot;Analytics-Klassifizierungen&quot;](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Klicken Sie auf **[!UICONTROL Zuordnung]** und ordnen Sie dann die Feldspaltenüberschriften den entsprechenden [!UICONTROL Recommendations]-Feldnamen zu.

   ![Zuordnungsabschnitt](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Häufig gestellte Fragen  

Berücksichtigen Sie die folgenden häufig gestellten Fragen, wenn Sie [!DNL Analytics] mit [!DNL Target] verwenden:

### Müssen die Werte `entity.id` und `entity.categoryId` innerhalb des [!DNL Target]-mbox-Aufrufs übergeben werden?

Ja, diese beiden Werte sind weiterhin erforderlich. Die übrigen Attribute können über einen [!DNL Analytics]-Feed übergeben werden, wie in diesem Dokument beschrieben.

### Kann ich dynamische Inklusionsregeln verwenden, z. B. Entitätsparameter stimmen mit Profil-Attributen mit dem Feed-Ansatz [!DNL Analytics] überein?

Ja, das kannst du. Die Methode ist bei Verwendung von [!DNL Target] eigenständig ähnlich. In diesem Fall müssen Sie sich jedoch um den Zeitfaktor kümmern. Die Entitätsvariablen, die mit den Profil-Variablen übereinstimmen sollen, sind von der Datenschicht abhängig, die später auf der Seite angezeigt wird.

