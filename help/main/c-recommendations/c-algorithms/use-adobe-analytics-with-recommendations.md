---
keywords: Verhaltensdatenquelle;Analysen;Empfehlungen;Kriterien;Produktvariablen
description: Erfahren Sie, wie  [!DNL Adobe Analytics]  als Verhaltensdatenquelle in verwendet  [!DNL Target Recommendations].
title: Wie verwende ich  [!DNL Adobe Analytics] with [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Verwenden von [!DNL Adobe Analytics] mit [!DNL Recommendations]

Durch die Verwendung von [!DNL Adobe Analytics] als Verhaltensdatenquelle können Kunden die ansichts- und kaufbasierten Verhaltensdaten aus [!DNL Analytics] in [!DNL Adobe Target Recommendations] Aktivitäten verwenden. Diese Funktion ist besonders hilfreich in Situationen, in denen die [!DNL Target Recommendations] neu ist und [!DNL Analytics] viele historische Daten zu verwenden hat.

Die Verwendung von [!DNL Analytics] als Verhaltensdatenquelle kann als umfangreiche Quelle für Informationen zum Benutzerverhalten dienen. Diese Informationen können Daten aus einer Drittanbieterquelle oder einem Feed enthalten, die bzw. der nur für [!DNL Analytics] freigegeben wird.

Beim [Erstellen ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) Kriterien“ in [!DNL Recommendations] gibt es zwei Optionsfelder, mit denen Sie auswählen können, welche Datenquelle verwendet werden soll: [!UICONTROL mboxes] oder [!UICONTROL Analytics]. Um ein Kriterium zu erstellen, klicken Sie auf [!UICONTROL Recommendations] > [!UICONTROL Criteria] > [!UICONTROL Create Criteria] > [!UICONTROL Create Criteria]. Weitere Informationen finden Sie unter [Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

>[!NOTE]
>
>Wenn diese beiden Schaltflächen nicht in Ihrem Konto angezeigt werden, wenden Sie sich an die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Anwendungsbeispiele zum [!DNL Analytics] von Daten in [!DNL Target]

Durch die Verwendung von [!DNL Analytics] als Verhaltensdatenquelle für Recommendations können Sie auch bestimmte Anwendungsfälle bereitstellen, ohne dass Entitätsseiten mit allen [!DNL Target] Entitätsparametern getaggt werden müssen. Obwohl dies bestimmte Voraussetzungen erfordert, ist die Verfügbarkeit von „Produktvariablen“ das Wichtigste, damit diese Funktion nahtlos funktioniert. Reguläre eVars und Props reichen nicht aus, damit dieser Handshake automatisch zwischen [!DNL Analytics] und [!DNL Target] stattfindet.

Sie können [!DNL Analytics] als Verhaltensdatenquelle verwenden, um:

* Zeigen Sie Benutzern auf einer Einzelhandels-Website Empfehlungen auf einer Produktdetailseite an, die darauf basieren, was andere Benutzer mithilfe von [!DNL Analytics] im letzten Monat von derselben Kategorie gekauft haben.
* Zeigen Sie Inhalte auf dem Startbildschirm einer Medien-Site für die beliebtesten Inhalte in einer bestimmten Kategorie an, die derzeit auf der Grundlage [!DNL Analytics] Daten im Trend liegt.

## Implementierung in [!DNL Analytics]

Die folgenden Abschnitte helfen Ihnen bei der Implementierung dieser Funktion auf der [!DNL Analytics] Seite.

### Voraussetzungen: Einrichten von Produktvariablen in [!DNL Analytics]

Implementieren Sie Produktvariablen in [!DNL Analytics] mit den erforderlichen Attributen, die für die [!DNL Target Recommendations] erforderlich sind.

Ein [!DNL Target Recommendations] Beispiel-Feed-Format dient als Anleitung, für das alle Attribute in den Produktvariablen definiert werden müssen. Später müssen diese Werte in der [!DNL Target]-Benutzeroberfläche für die jeweiligen [!DNL Target] Entitätswerte „zugeordnet“ werden.

>[!NOTE]
>
>Wenn es sich um eine Inhalts-Site handelt, müssen die entsprechenden Inhaltselemente als „Produkte“ behandelt werden und die zugehörigen Attribute zu diesem Inhalt müssen als Attribute übergeben werden. Zu diesen Attributen gehören u. a. der Name des Autors, das Veröffentlichungsdatum, der Titel des Inhalts, der Monat der Veröffentlichung usw. Die Granularität von Kategorieebenen oder Kategorietypen sollte vom Unternehmen auf der Grundlage von Anwendungsfallanforderungen festgelegt werden.

Weitere Informationen zum Einrichten von Produktvariablen finden Sie unter [Produkte](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) im *Implementieren von Adobe Analytics*. Einige Hinweise in dieser Dokumentation erfordern die Diskretion des Teams, das sie bereitstellt (Beispiel : Kategorie). Es wird immer empfohlen, [!DNL Adobe] vor dieser Aktivität zu konsultieren.

### Zu beachten

[!DNL Analytics] Daten werden über einen täglichen Feed gesendet. Es kann bis zu 24 Stunden dauern, bis Verhaltensergebnisse in den Recommendations-Ergebnissen auf Ihrer Site widergespiegelt werden. Wie bei allen [!DNL Recommendations]-Kriterieneinstellungen kann und sollte diese Datenquelle getestet werden.

Um schnell entscheiden zu können, welche Datenquelle verwendet werden soll, sollten Sie eine [!DNL Target] Mbox als Verhaltensdatenquelle verwenden, wenn täglich viele organische Daten von Benutzenden generiert werden und nicht viel Abhängigkeit von historischen Daten besteht. Wenn Sie in Fällen geringerer Verfügbarkeit von kürzlich generierten organischen Daten auf [!DNL Analytics] Daten bauen möchten, ist die Verwendung von [!DNL Analytics] als Verhaltensdatenquelle eine gute Wahl.

Jetzt ist es an der Zeit, diese Variablen auf [!DNL Target] Seite abzubilden, um eine kontinuierliche Bereitstellung von Verhaltensdaten zu ermöglichen.

## In [!DNL Target] implementieren

1. Klicken Sie [!DNL Target] auf **[!UICONTROL Recommendations]** und dann auf die Registerkarte **[!UICONTROL Feeds]** .

1. Klicken Sie auf **[!UICONTROL Create Feed]**.

1. Wählen Sie **[!UICONTROL Analytics Classifications]** und geben Sie dann die Report Suite an.

1. Klicken Sie auf **[!UICONTROL Next]** , um zu den **[!UICONTROL Schedule]** Einstellungen zu gelangen und einen Häufigkeitszeitraum für den Feed auszuwählen:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 weeks]
   * [!UICONTROL Never]

   Sie können auch die Tageszeit auswählen, zu der der Feed verarbeitet werden soll.

1. Klicken Sie auf **[!UICONTROL Next]** , um zu den **[!UICONTROL Mapping]** Einstellungen zu gelangen, und ordnen Sie dann die Feldspaltenüberschriften den entsprechenden [!UICONTROL Recommendations] Feldnamen zu.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Häufig gestellte Fragen  

Beachten Sie bei der Verwendung von [!DNL Analytics] mit [!DNL Target] die folgenden häufig gestellten Fragen:

### Müssen die `entity.id`- und `entity.categoryId` Werte innerhalb des [!DNL Target]-Mbox-Aufrufs übergeben werden?

Ja, diese beiden Werte sind weiterhin erforderlich. Der Rest der Attribute kann über einen [!DNL Analytics]-Feed übergeben werden, wie in diesem Dokument beschrieben.

### Kann ich dynamische Einschlussregeln verwenden, z. B. Entitätsparameter stimmt mit Profilattributen überein, die den [!DNL Analytics]-Feed-Ansatz verwenden?

Ja, das können Sie. Die Methode ist bei Verwendung [!DNL Target] eigenständigen Journeys ähnlich. In diesem Fall müssen Sie jedoch auf den Faktor Timing achten. Die Entitätsvariablen, die mit den Profilvariablen übereinstimmen sollen, hängen von der Datenschicht ab, die viel später auf der Seite angezeigt werden kann.
