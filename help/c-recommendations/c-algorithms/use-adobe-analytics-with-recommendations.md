---
keywords: Verhaltensdatenquelle;Analysen;Empfehlungen;Kriterien;Produktvariablen
description: Erfahren Sie, wie Sie mit Adobe Analytics als verhaltensbasierte Datenquelle die Ansicht- und/oder kaufbasierten Verhaltensdaten aus Analytics in [!DNL Target] Recommendations verwenden können.
title: Wie verwende ich Adobe Analytics mit [!DNL Target] Recommendations?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 1%

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

Ein Muster-Feed-Format von [!DNL Target Recommendations] dient als Leitfaden, auf dem alle Attribute in den Produktvariablen definiert werden müssen. Später müssen diese Werte in der [!DNL Target]-Benutzeroberfläche für die entsprechenden [!DNL Target]-Entitätswerte &quot;zugeordnet&quot;werden.

>[!NOTE]
>
>Wenn es sich um eine Content-Site handelt, müssen die entsprechenden Inhaltselemente als &quot;Produkte&quot;und zugehörige Attribute zu diesem Inhalt behandelt werden (Beispiel: Autorenname, Veröffentlichungsdatum, Inhaltstitel, Veröffentlichungsmonat usw.) muss als Attribute weitergegeben werden. Die Granularität der Kategorie oder der Kategorie sollte vom Unternehmen auf der Grundlage von Anwendungsfällen festgelegt werden.

Weitere Informationen zum Einrichten von Produktvariablen finden Sie unter [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) im *Analytics-Implementierungshandbuch*. Einige der Hinweise in dieser Dokumentation erfordern einen Ermessensspielraum des Teams, das sie bereitstellt (Beispiel: Kategorie). Es wird immer empfohlen, sich vor dieser Aktivität mit der Adobe zu beraten.

### Zu beachten

[!DNL Analytics] Daten werden über einen täglichen Feed gesendet. Es dauert bis zu 24 Stunden, bis die Ergebnisse der Empfehlungen auf Ihrer Site widergespiegelt werden. Wie bei allen [!DNL Recommendations]-Kriterieneinstellungen kann und sollte diese Datenquelle getestet werden.

Für eine schnelle Entscheidungsfindung darüber, welche Datenquelle verwendet werden soll, wenn täglich viele organische Daten von Benutzern generiert werden und keine große Abhängigkeit von historischen Daten erforderlich ist, kann eine [!DNL Target]-mbox als verhaltensbasierte Datenquelle gut geeignet sein. In Fällen, in denen die Verfügbarkeit organischer Daten, die kürzlich generiert wurden, geringer ist, wenn Sie auf [!DNL Analytics]-Daten zurückgreifen möchten, ist die Verwendung von [!DNL Analytics] als verhaltensbasierte Datenquelle gut geeignet.

Jetzt ist es an der Zeit, diese Variablen auf [!DNL Target] Seite zuzuordnen, um eine kontinuierliche Bereitstellung von Verhaltensdaten zu ermöglichen.

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
