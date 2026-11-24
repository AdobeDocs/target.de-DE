---
keywords: Verhaltensdatenquelle;Analysen;Empfehlungen;Kriterien;Produktvariablen
description: Erfahren Sie, wie Sie [!DNL Adobe Analytics] als Verhaltensdatenquelle in [!DNL Target Recommendations] verwenden.
title: Verwenden von Adobe Analytics mit Recommendations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
TQID: 'https://experienceleague.adobe.com/2ryixOT-YoKjDlMbqs8g2DJElNVmlCUFhbdZzpfSnNs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: 374d176c5c40826d958a8b87d220422466433690
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 1%
---
# Verwenden von [!DNL Adobe Analytics] mit [!DNL Recommendations] {#use-analytics-with-recommendations}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie [!DNL Adobe Analytics] als Verhaltensdatenquelle in [!DNL Adobe Target Recommendations] Aktivitäten verwenden.

>[!ENDSHADEBOX]

Durch die Verwendung von [!DNL Adobe Analytics] als Verhaltensdatenquelle können [!DNL Adobe Target Recommendations] Aktivitäten die ansichts- und kaufbasierten Verhaltensdaten aus [!DNL Analytics] verwenden. Dies ist nützlich, wenn die [!DNL Target Recommendations] neu ist und [!DNL Analytics] viele historische Daten zu verwenden hat. Die Daten können auch Informationen aus einer Drittanbieterquelle oder einem Feed enthalten, die bzw. der nur für [!DNL Analytics] freigegeben wird.

Die Datenquelle wird beim [Erstellen von Kriterien](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in [!DNL Recommendations] mit der **[!UICONTROL Verhaltensdaten-Source]**-Option ausgewählt: **[!UICONTROL Adobe Target]** oder **[!UICONTROL Analytics]**.

>[!NOTE]
>
>Wenn diese beiden Optionen nicht im Konto angezeigt werden, wenden Sie sich an [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Anwendungsbeispiele zum [!DNL Analytics] von Daten in [!DNL Target] {#use-cases}

Die Verwendung von [!DNL Analytics] als Verhaltensdatenquelle ermöglicht auch die Bereitstellung spezifischer Anwendungsfälle, ohne Entitätsseiten mit allen [!DNL Target] Entitätsparametern zu versehen. Dies setzt bestimmte Voraussetzungen voraus, wobei die Verfügbarkeit von „Produktvariablen“ die wichtigste ist. Reguläre eVars und Props reichen nicht aus, um diese Daten automatisch auszutauschen, [!DNL Analytics] und [!DNL Target].

[!DNL Analytics] kann als Verhaltensdatenquelle verwendet werden, um:

* Zeigen Sie Benutzern auf einer Einzelhandels-Website Empfehlungen auf einer Produktdetailseite an, die darauf basieren, was andere Benutzer mithilfe von [!DNL Analytics] im letzten Monat von derselben Kategorie gekauft haben.
* Zeigen Sie Inhalte auf dem Startbildschirm einer Medien-Site für die beliebtesten Inhalte in einer bestimmten Kategorie an, die derzeit auf der Grundlage [!DNL Analytics] Daten im Trend liegt.

## Implementierung in [!DNL Analytics]

### Voraussetzungen: Einrichten von Produktvariablen in [!DNL Analytics] {#prerequisites}

Implementieren Sie Produktvariablen in [!DNL Analytics] mit den Attributen, die für die [!DNL Target Recommendations] erforderlich sind. Ein [!DNL Target Recommendations] Beispiel-Feed-Format führt an, welche Attribute in den Produktvariablen definiert werden müssen. Diese Werte müssen später in der [!DNL Target]-Benutzeroberfläche den jeweiligen [!DNL Target]-Entitätswerten „zugeordnet“ werden.

>[!NOTE]
>
>Wenn es sich um eine Inhalts-Site handelt, müssen die entsprechenden Inhaltselemente als „Produkte“ behandelt werden, und die zugehörigen Attribute dieses Inhalts müssen als Attribute übergeben werden. Zu diesen Attributen gehören u. a. der Name des Autors, das Veröffentlichungsdatum, der Titel des Inhalts, der Monat der Veröffentlichung usw. Das Unternehmen sollte die Granularität der Kategorieebene oder der Kategorietypen basierend auf den Anforderungen des Anwendungsfalls entscheiden.

Weitere Informationen zum Einrichten von Produktvariablen finden Sie unter [Produkte](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html?lang=de) im *Implementieren von Adobe Analytics*. Einige Hinweise in dieser Dokumentation, z. B. zur Kategorie, erfordern das Urteilsvermögen des Teams, das sie bereitstellt. Beratung [!DNL Adobe] vor dieser Aktivität wird empfohlen.

### Zu beachten {#considerations}

[!DNL Analytics] Daten werden über einen täglichen Feed gesendet. Es kann bis zu 24 Stunden dauern, bis Verhaltensergebnisse in den Recommendations-Ergebnissen auf der Site widergespiegelt werden. Wie bei allen [!DNL Recommendations]-Kriterieneinstellungen sollte diese Datenquelle getestet werden.

So wählen Sie eine Datenquelle:

* Eine [!DNL Target] Mbox eignet sich gut, wenn von Benutzern täglich viele organische Daten generiert werden und nur wenig Abhängigkeit von historischen Daten erforderlich ist.
* [!DNL Analytics] passt gut, wenn in letzter Zeit weniger organische Daten generiert wurden und die [!DNL Analytics] Daten verwendet werden sollen.

Die Werte für `entity.id` und `entity.categoryId` müssen noch im [!DNL Target] mbox-Aufruf übergeben werden. Die anderen Attribute können über einen [!DNL Analytics]-Feed übergeben werden, wie auf dieser Seite beschrieben.

Dynamische Einschlussregeln, wie z. B. das Abgleichen eines Entitätsparameters mit einem Profilattribut, können mit dem [!DNL Analytics]-Feed-Ansatz verwendet werden. Die Methode ähnelt der Verwendung von [!DNL Target] eigenständigen , aber der Zeitpunkt muss berücksichtigt werden: Die Entitätsvariablen, die mit den Profilvariablen übereinstimmen sollen, hängen von der Datenschicht ab, die viel später auf der Seite angezeigt werden kann.

## In [!DNL Target] implementieren {#implement-target}

Die Produktvariablen werden in [!DNL Target] zugeordnet, um eine kontinuierliche Bereitstellung von Verhaltensdaten zu ermöglichen.

1. Klicken Sie [!DNL Target] auf **[!UICONTROL Recommendations]** und dann auf die Registerkarte **[!UICONTROL Feeds]**.

1. Klicken Sie **[!UICONTROL Feed erstellen]**.

   ![Seite Feeds mit hervorgehobener Schaltfläche „Feed erstellen“](../assets/feeds_1.png)

1. Wählen Sie **[!UICONTROL Analytics Classifications]** aus und geben Sie dann die Report Suite an.

1. Klicken Sie auf **[!UICONTROL Weiter]**, um zu den **[!UICONTROL Zeitplan]**-Einstellungen zu wechseln und dann eine Häufigkeit für den Feed auszuwählen: **[!UICONTROL Täglich]**, **[!UICONTROL Wöchentlich]**, **[!UICONTROL Alle 2 Wochen]** oder **[!UICONTROL Nie]**. Die Tageszeit, zu der der Feed verarbeitet werden soll, kann ebenfalls ausgewählt werden.

   ![Schritt „Planung“ im Dialogfeld „Feed erstellen“ mit den Optionen „Häufigkeit“: „Täglich“, „Wöchentlich“, „Alle 2 Wochen“ und „Nie“ sowie „Tageszeit“](../assets/feeds_3.png)

1. Klicken Sie **[!UICONTROL Weiter]**, um zu den Einstellungen **[!UICONTROL Zuordnung]** zu gelangen, und ordnen Sie dann die Feldspaltenüberschriften den entsprechenden Feldnamen **[!UICONTROL Recommendations]** zu.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Weitere Informationen zum Erstellen eines Feeds finden Sie unter [Erstellen eines Feeds](/help/main/c-recommendations/c-products/feeds.md#steps).
