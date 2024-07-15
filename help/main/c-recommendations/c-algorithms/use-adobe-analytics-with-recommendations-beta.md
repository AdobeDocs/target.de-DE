---
keywords: Verhaltensdatenquelle; Analysen; Empfehlungen; Kriterien; Produktvariablen
description: Erfahren Sie, wie Sie [!DNL Adobe Analytics] in  [!DNL Target Recommendations] als Verhaltens-Datenquelle verwenden.
title: Wie verwende ich [!DNL Adobe Analytics] mit [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 6d2a313b0e54aa5f6717eee850c79e4092309e7d
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Verwenden Sie [!DNL Adobe Analytics] mit [!DNL Recommendations]

Durch Verwendung von [!DNL Adobe Analytics] als Verhaltens-Datenquelle können Kunden die ansichtsbasierten und kaufbasierten Verhaltensdaten aus [!DNL Analytics] in [!DNL Adobe Target Recommendations] -Aktivitäten verwenden. Diese Funktion ist besonders hilfreich in Situationen, in denen das [!DNL Target Recommendations]-Setup neu ist und [!DNL Analytics] viele historische Daten verwendet.

Die Verwendung von [!DNL Analytics] als Verhaltensdatenquelle kann als umfassende Informationsquelle zum Benutzerverhalten dienen. Diese Informationen können Daten aus einer Drittanbieterquelle oder einem Feed enthalten, die/der nur für [!DNL Analytics] freigegeben ist.

Beim Erstellen von Kriterien ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) in [!DNL Recommendations] gibt es zwei Optionsfelder, mit denen Sie auswählen können, welche Datenquelle verwendet werden soll: [!UICONTROL mboxes] oder [!UICONTROL Analytics]. [ Um ein Kriterium zu erstellen, klicken Sie auf [!UICONTROL Recommendations] > [!UICONTROL Criteria] > [!UICONTROL Create Criteria] > [!UICONTROL Create Criteria]. Weitere Informationen finden Sie unter [Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

>[!NOTE]
>
>Wenn diese beiden Schaltflächen nicht in Ihrem Konto angezeigt werden, wenden Sie sich an die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Anwendungsfälle für [!DNL Analytics] -Daten in [!DNL Target]

Durch die Verwendung von [!DNL Analytics] als Verhaltens-Datenquelle für Empfehlungen können Sie auch bestimmte Anwendungsfälle bereitstellen, ohne dass Entitätsseiten mit allen Entitätsparametern von [!DNL Target] markiert werden müssen. Obwohl dies bestimmte Voraussetzungen erfordert, ist die Verfügbarkeit von &quot;Produktvariablen&quot;das wichtigste Element, damit diese Funktion nahtlos funktioniert. Reguläre eVars und Props reichen nicht aus, damit dieser Handshake automatisch zwischen [!DNL Analytics] und [!DNL Target] auftritt.

Sie können [!DNL Analytics] als Verhaltens-Datenquelle verwenden, um:

* Zeigen Sie den Benutzern auf einer Einzelhandelssite Empfehlungen auf einer Produktdetailseite an, basierend darauf, was andere Benutzer im letzten Monat unter Verwendung von [!DNL Analytics] -Daten von derselben Kategorie gekauft haben.
* Zeigen Sie Inhalte auf dem Startbildschirm einer Medien-Site für den beliebtesten Inhalt einer bestimmten Kategorie an, der derzeit auf der Grundlage von [!DNL Analytics] -Daten als Trend läuft.

## Implementierung in [!DNL Analytics]

Die folgenden Abschnitte helfen Ihnen bei der Implementierung dieser Funktion auf der Seite [!DNL Analytics] .

### Voraussetzungen: Einrichten von Produktvariablen in [!DNL Analytics]

Implementieren Sie Produktvariablen in [!DNL Analytics] mit den erforderlichen Attributen, die für [!DNL Target Recommendations] erforderlich sind.

Ein Beispiel-Feed-Format [!DNL Target Recommendations] dient als Anleitung, anhand dessen alle Attribute in den Produktvariablen definiert werden müssen. Später müssen diese Werte in der Benutzeroberfläche von [!DNL Target] für die jeweiligen [!DNL Target]-Entitätswerte &quot;zugeordnet&quot;werden.

>[!NOTE]
>
>Wenn es sich um eine Inhalts-Site handelt, müssen die jeweiligen Inhaltselemente als &quot;Produkte&quot;behandelt und die zugehörigen Attribute zu diesem Inhalt müssen als Attribute übergeben werden. Zu diesen Attributen können der Name des Autors, das Veröffentlichungsdatum, der Titel des Inhalts, der Veröffentlichungsmonat usw. gehören. Die Granularität der Kategoriestufe oder Kategorietypen sollte vom Unternehmen auf der Grundlage von Anwendungsfallanforderungen festgelegt werden.

Weitere Informationen zum Einrichten von Produktvariablen finden Sie unter [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) im Handbuch *Adobe Analytics implementieren* . Einige der Hinweise in dieser Dokumentation erfordern ein Ermessen des Teams, das sie bereitstellt (Beispiel: Kategorie). Es wird immer empfohlen, sich mit [!DNL Adobe] zu beraten, bevor Sie diese Aktivität durchführen.

### Zu beachten

[!DNL Analytics] -Daten werden über einen täglichen Feed gesendet. Es kann bis zu 24 Stunden dauern, bis die Verhaltensergebnisse in den Empfehlungsergebnissen auf Ihrer Site widergespiegelt werden. Wie bei allen [!DNL Recommendations] -Kriterieneinstellungen kann und sollte diese Datenquelle getestet werden.

Für eine schnelle Entscheidungsfindung darüber, welche Datenquelle verwendet werden soll, wenn täglich viele organische Daten von Benutzern generiert werden und nicht viel Abhängigkeit von historischen Daten erforderlich ist, kann die Verwendung einer [!DNL Target] -Mbox als Verhaltens-Datenquelle eine gute Idee sein. Wenn Sie in letzter Zeit weniger organische Daten generieren und auf [!DNL Analytics]-Daten zurückgreifen möchten, empfiehlt sich die Verwendung von [!DNL Analytics] als Verhaltens-Datenquelle.

Jetzt ist es an der Zeit, diese Variablen für die kontinuierliche Bereitstellung von Verhaltensdaten auf [!DNL Target] Seite zuzuordnen.

## Implementieren in [!DNL Target]

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Recommendations]** und dann auf die Registerkarte **[!UICONTROL Feeds]**.

1. Klicken Sie auf **[!UICONTROL Create Feed]**.

1. Wählen Sie &quot;**[!UICONTROL Analytics Classifications]**&quot;und geben Sie dann die Report Suite an.

1. Klicken Sie auf **[!UICONTROL Next]** , um zu den Einstellungen für **[!UICONTROL Schedule]** zu wechseln. Wählen Sie dann einen Frequenzzeitraum für den Feed aus:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 weeks]
   * [!UICONTROL Never]

   Sie können auch die Tageszeit für die Verarbeitung des Feeds auswählen.

1. Klicken Sie auf **[!UICONTROL Next]** , um zu den Einstellungen für **[!UICONTROL Mapping]** zu wechseln, und ordnen Sie dann die Spaltenüberschriften der Felder den entsprechenden [!UICONTROL Recommendations] Feldnamen zu.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Häufig gestellte Fragen  

Beachten Sie die folgenden häufig gestellten Fragen, wenn Sie [!DNL Analytics] mit [!DNL Target] verwenden:

### Müssen die Werte `entity.id` und `entity.categoryId` innerhalb des Mbox-Aufrufs [!DNL Target] übergeben werden?

Ja, diese beiden Werte sind weiterhin erforderlich. Die übrigen Attribute können über einen [!DNL Analytics] -Feed übergeben werden, wie in diesem Dokument beschrieben.

### Kann ich dynamische Einschlussregeln verwenden, z. B. Entitätsparameter stimmt mit Profilattributen über den Feed-Ansatz [!DNL Analytics] überein?

Ja, das kannst du. Die Methode ist bei Verwendung von eigenständigem [!DNL Target] ähnlich. In diesem Fall müssen Sie jedoch auf den Zeitfaktor achten. Die Entitätsvariablen, die mit den Profilvariablen übereinstimmen sollen, hängen von der Datenschicht ab, die viel später auf der Seite angezeigt werden kann.