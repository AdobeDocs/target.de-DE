---
keywords: Verhaltensdatenquelle; Analysen; Empfehlungen; Kriterien; Produktvariablen
description: Erfahren Sie, wie Sie Adobe Analytics als Verhaltens-Datenquelle verwenden können, um die ansichtsbasierten und/oder kaufbasierten Verhaltensdaten aus Analytics in [!DNL Target] Recommendations.
title: Wie verwende ich Adobe Analytics mit [!DNL Target] Recommendations?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 2a4cae206bf634bf3fbec65c5c4b289aadefede1
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 1%

---

# Verwenden von Adobe Analytics mit Recommendations

Verwenden [!DNL Adobe Analytics] als Verhaltens-Datenquelle, über die Kunden die ansichtsbasierten und/oder kaufbasierten Verhaltensdaten aus [!DNL Analytics] in [!DNL Adobe Target] Recommendations-Aktivitäten. Diese Funktion ist besonders hilfreich in Situationen, in denen die Variable [!DNL Target Recommendations] Setup ist neu und [!DNL Analytics] verfügt über viele historische Daten, die genutzt werden können.

Verwenden [!DNL Analytics] da die Verhaltensdatenquelle als umfassende Quelle von Informationen über das Benutzerverhalten dienen kann. Dies kann Daten aus einer Drittanbieterquelle oder einem Feed umfassen, die/der nur für [!DNL Analytics].

while [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) In Recommendations gibt es zwei Optionsfelder, mit denen Sie auswählen können, welche Datenquelle verwendet werden soll: [!UICONTROL Mboxes] oder [!UICONTROL Analytics].

![Schaltflächen für Verhaltensdatenquellen](assets/behavioral-data-source.png)

>[!NOTE]
>
>Wenn diese beiden Schaltflächen nicht in Ihrem Konto angezeigt werden, wenden Sie sich an [Kundenunterstützung](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Anwendungsfälle für Analytics-Daten in Target

Verwenden [!DNL Analytics] da die Verhaltensdatenquelle für Empfehlungen auch die Möglichkeit bietet, bestimmte Anwendungsfälle bereitzustellen, ohne dass Entitätsseiten mit allen [!DNL Target] Entitätsparameter. Obwohl dies bestimmte Voraussetzungen erfordert, ist die Verfügbarkeit von &quot;Produktvariablen&quot;das wichtigste Element, damit diese Funktion nahtlos funktioniert. Reguläre eVars und Props reichen nicht aus, damit dieser Handshake zwischen [!DNL Analytics] und [!DNL Target].

Sie können [!DNL Analytics] als Verhaltens-Datenquelle zu:

* Zeigen Sie mithilfe von Analytics-Daten Empfehlungen auf einer Einzelhandelssite für Benutzer auf einer PDP-Seite an, basierend darauf, was andere Benutzer im letzten Monat von derselben Kategorie gekauft haben.
* Anzeigen von Inhalten auf dem Startbildschirm einer Medien-Site für den beliebtesten Inhalt einer bestimmten Kategorie, die derzeit als Trend verfolgt wird, basierend auf [!DNL Analytics] Daten.

## Implementierung in Analytics

Die folgenden Abschnitte helfen Ihnen bei der Implementierung dieser Funktion in [!DNL Analytics] Seite.

### Voraussetzungen: Produktvariablen in Analytics einrichten

Sie müssen Produktvariablen in [!DNL Analytics] mit den erforderlichen Attributen, die für [!DNL Target Recommendations].

A [!DNL Target Recommendations] Das Beispiel-Feed-Format dient als Anleitung, anhand dessen alle Attribute in den Produktvariablen definiert werden müssen. Später müssen diese Werte im [!DNL Target] Benutzeroberfläche für die entsprechenden [!DNL Target] Entitätswerte.

>[!NOTE]
>
>Wenn es sich um eine Inhalts-Site handelt, müssen die jeweiligen Inhaltselemente als &quot;Produkte&quot;und zugehörige Attribute zu diesem Inhalt behandelt werden (Beispiel: Name des Autors, Veröffentlichungsdatum, Titel des Inhalts, Monat der Veröffentlichung usw.) muss als Attribute übergeben werden. Die Granularität der Kategoriestufe oder Kategorietypen sollte vom Unternehmen auf der Grundlage von Anwendungsfallanforderungen festgelegt werden.

Weitere Informationen zum Einrichten von Produktvariablen finden Sie unter [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) im *Implementierungshandbuch für Analytics*. Einige der Hinweise in dieser Dokumentation erfordern einen Ermessensspielraum des Teams, das sie bereitstellt (Beispiel: Kategorie). Es wird immer empfohlen, sich mit Adobe zu beraten, bevor Sie diese Aktivität durchführen.

### Zu beachten

[!DNL Analytics] Daten werden über einen täglichen Feed gesendet. Es dauert bis zu 24 Stunden, bis die Verhaltensergebnisse in den Empfehlungsergebnissen auf Ihrer Site widergespiegelt werden. Wie bei allen [!DNL Recommendations] -Kriterieneinstellungen festgelegt ist, kann und sollte diese Datenquelle getestet werden.

Für eine schnelle Entscheidungsfindung darüber, welche Datenquelle verwendet werden soll, wenn täglich viele organische Daten von Benutzern generiert werden und nicht viel Abhängigkeit von historischen Daten erforderlich ist, verwenden Sie dann eine [!DNL Target] Mbox als Verhaltens-Datenquelle geeignet sein. Wenn die Verfügbarkeit organischer Daten, die kürzlich generiert wurden, geringer ist, wenn Sie auf [!DNL Analytics] -Daten und dann mithilfe der [!DNL Analytics] da die Verhaltensdatenquelle gut geeignet ist.

Jetzt ist es an der Zeit, diese Variablen [!DNL Target] zur kontinuierlichen Bereitstellung von Verhaltensdaten.

## Implementieren in Target

1. Klicken Sie in Target auf **[!UICONTROL Recommendations]** und klicken Sie dann auf **[!UICONTROL Feeds]** Registerkarte.

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Klicken **[!UICONTROL Feed erstellen]**.

1. Auswählen **[!UICONTROL Analytics Classifications]** und geben Sie dann die Report Suite an.

   ![Option &quot;Analytics Classifications&quot;](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Klicken **[!UICONTROL Zuordnung]** und ordnen Sie dann die Feldspaltenüberschriften den entsprechenden zu [!UICONTROL Recommendations] Feldnamen.

   ![Zuordnungsabschnitt](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Häufig gestellte Fragen  

Beachten Sie die folgenden häufig gestellten Fragen bei der Verwendung von [!DNL Analytics] mit [!DNL Target]:

### Sind die `entity.id` und `entity.categoryId` Werte, die innerhalb der [!DNL Target] Mbox-Aufruf?

Ja, diese beiden Werte sind weiterhin erforderlich. Die übrigen Attribute können über eine [!DNL Analytics] Feed, wie in diesem Dokument beschrieben.

### Kann ich dynamische Einschlussregeln verwenden, z. B. Entitätsparameter stimmt mit Profilattributen mit der [!DNL Analytics] Feed-Ansatz?

Ja, das kannst du. Die Methode ist bei Verwendung von [!DNL Target] eigenständig. In diesem Fall müssen Sie jedoch auf den Zeitfaktor achten. Die Entitätsvariablen, die mit den Profilvariablen übereinstimmen sollen, hängen von der Datenschicht ab, die viel später auf der Seite angezeigt werden kann.
