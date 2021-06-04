---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen; Zielgruppentargeting; Zielgruppenberichterstellung; Zielgruppenbericht; Segment; benutzerdefinierte Profilparameter; Zielgruppendefinition; Zielgruppenliste
description: Erfahren Sie, wie Sie die Liste [!UICONTROL Zielgruppen] in Adobe [!DNL Target] verwenden und wie Sie Zielgruppendefinitionskarten anzeigen, die Zielgruppendetails und Nutzungsinformationen enthalten.
title: Wie verwende ich die Zielgruppenliste?
feature: Zielgruppen
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: 06a5fda72a649c4037cb78d3e670747cd297a64d
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 58%

---

# Erstellen von Zielgruppen

Zielgruppen in [!DNL Adobe Target] bestimmen, wer Inhalte und Erlebnisse in einer zielgerichteten Aktivität sieht.

Zielgruppen werden überall dort eingesetzt, wo Targeting zur Verfügung steht. Beim Targeting einer Aktivität haben Sie folgende Möglichkeiten:

* Wählen Sie eine wiederverwendbare Zielgruppe aus der Liste [!UICONTROL Zielgruppen] aus.
* [Aktivitätsspezifische ](/help/c-target/creating-activity-only-audience.md) Zielgruppen erstellen und ansprechen
* [Kombinieren mehrerer ](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) Zielgruppen zur Erstellung einer Ad-hoc-Zielgruppe

Sie können auch Zielgruppendaten verwenden, die von [!DNL Adobe Analytics] für Echtzeit-Targeting und Personalisierung in [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Anwendungen erfasst wurden. Siehe [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) im Handbuch *Experience Cloud Central Interface Components* .

In [!DNL Target] stehen zwei Zielgruppentypen zur Verfügung:

* **Target-Zielgruppen:** Dieser Typ wird verwendet, um verschiedenen Besuchertypen unterschiedliche Inhalte bereitzustellen.
* **Berichtszielgruppen:** Dieser Typ wird verwendet, um zu bestimmen, wie verschiedene Benutzertypen auf den gleichen Inhalt reagieren, und unterstützt Sie bei der Analyse Ihrer Testergebnisse.

   In [!DNL Target] können Sie Berichtszielgruppen nur dann konfigurieren, wenn Sie [!DNL Target] als Berichtsquelle verwenden. Wenn Sie [ Adobe Analytics als Berichtsquelle](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, müssen Sie Ihre Berichterstellungszielgruppen in [!DNL Analytics] konfigurieren.

## Verwenden Sie die Liste [!UICONTROL Zielgruppen] .

Wenn Sie auf die Liste [!UICONTROL Zielgruppen] zugreifen möchten, klicken Sie in der oberen Menüzeile auf **[!UICONTROL Zielgruppen]**:

![Zielgruppenliste](/help/c-target/c-audiences/assets/audiences_list.png)

Die [!UICONTROL Zielgruppenliste] enthält alle Zielgruppen, die Sie in Ihren Aktivitäten verwenden können. Verwenden Sie die [!UICONTROL Zielgruppenliste], um Zielgruppen zu erstellen, zu bearbeiten, zu löschen, zu kopieren oder miteinander zu kombinieren. Die Liste zeigt auch die Quelle an, an der die Zielgruppe erstellt wurde ([!DNL Target], [!DNL Target Classic] und [!DNL Experience Cloud]. Vordefinierte Zielgruppen wie &quot;[!UICONTROL Neue Besucher]&quot;und &quot;[!UICONTROL Wiederkehrende Besucher]&quot;können nicht umbenannt werden.

Beim Arbeiten mit Zielgruppen, die ursprünglich in [!DNL Experience Cloud] erstellt wurden, werden Sie von Target benachrichtigt, wenn Sie in [!DNL Target] -Aktivitäten auf eine Zielgruppe verweisen, die später in [!DNL Experience Cloud] gelöscht wurden.

* Wenn eine Zielgruppe in [!DNL Experience Cloud] gelöscht wurde, wird sowohl in der Liste [!UICONTROL Zielgruppe] ein Warnsymbol angezeigt als auch die Zielgruppenauswahl. Eine QuickInfo in der Benutzeroberfläche zeigt auch an, dass die Zielgruppe in [!DNL Experience Cloud] gelöscht wurde.
* Wenn Sie versuchen, mehrere Zielgruppen mit einer gelöschten Zielgruppe zu kombinieren oder eine Aktivität zu speichern, die auf eine gelöschte Zielgruppe verweist, wird eine Warnmeldung angezeigt.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Klicken Sie beim Hinzufügen einer Zielgruppe auf das Attribut, das Sie für das Targeting Ihrer Aktivität verwenden möchten. Wenn das gewünschte Attribut nicht angezeigt wird, wurde es nicht von einer Mbox ausgelöst. In der Dropdownliste [!UICONTROL Benutzerdefinierte Parameter] sind weitere benutzerdefinierte Mbox-Parameter verfügbar.

Verwenden Sie die Schaltfläche [!UICONTROL Filter] , um die Liste [!UICONTROL Zielgruppen] nach Quelle zu filtern: [!DNL Adobe Target], [!DNL Adobe Target Classic] und [!DNL Experience Cloud].

![Filteroption in der   Zielgruppenliste](/help/c-target/c-audiences/assets/filters.png)

Verwenden Sie das Feld [!UICONTROL Zielgruppen suchen] , um die Liste [!UICONTROL Zielgruppen] zu durchsuchen. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die [!UICONTROL Zielgruppenliste] nach Zielgruppennamen oder dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Anzeigen von Zielgruppendefinitionen {#section_11B9C4A777E14D36BA1E925021945780}

Sie können Details zur Zielgruppendefinition auf einer Pop-up-Karte an verschiedenen Stellen der Target-Benutzeroberfläche anzeigen, ohne die Zielgruppe öffnen zu müssen. Diese Funktion gilt für Zielgruppen, die in [!DNL Target Standard/Premium] erstellt wurden, sowie für Zielgruppen, die aus [!DNL Target Classic] importiert oder über API erstellt wurden.

Beispielsweise wird auf die folgende Zielgruppendefinitionskarte zugegriffen, indem Sie für die gewünschte Zielgruppe auf das Symbol [!UICONTROL Details anzeigen] klicken:

![Aktivitäten > Zielgruppendefinition](assets/audience_definition_list.png)

Auf die folgende Zielgruppendefinitionskarte kann durch Klicken auf das Symbol [!UICONTROL Details anzeigen] auf der Seite [!UICONTROL Übersicht] einer Aktivität zugegriffen werden:

![Aktivitäten > Zielgruppendefinition](/help/c-target/c-audiences/assets/view-details-activity-overview.png)

Auf der Karte zur Zielgruppendefinition werden Typ, Quelle und Attribute der Zielgruppe angezeigt. Klicken Sie auf **[!UICONTROL Vollständige Details anzeigen]** , um weitere Aktivitäten anzuzeigen, die auf diese Zielgruppe verweisen (falls zutreffend). Wenn Sie eine Zielgruppendefinitionskarte auf der Seite [!UICONTROL Übersicht] einer Aktivität anzeigen, klicken Sie auf **[!UICONTROL Zielgruppennutzung]**.

Mithilfe der Informationen zur Zielgruppennutzung können Sie beim Bearbeiten von Zielgruppen unbeabsichtigte Auswirkungen auf andere Aktivitäten vermeiden. Zu „Informationen“ zählen „Live-Aktivitäten“, „Inaktive Aktivitäten“, „Archivierte Aktivitäten“ und „Aktivitätssynchronisierung“. Diese Funktion ist für alle Zielgruppen (Bibliothekszielgruppen und  [Zielgruppen vom Typ „Nur Aktivität“](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)) verfügbar.

Wenn eine Zielgruppe mit einer anderen Zielgruppe kombiniert wird und die kombinierte Zielgruppe zum Erstellen einer Aktivität verwendet wird, werden in den Nutzungsinformationen für beide Zielgruppen die neu erstellte Aktivität aufgelistet.

![](assets/audience_definition_list_usage.png)

Die folgende Zielgruppendefinitionskarte ist für eine aus der Adobe Experience Cloud importierte Zielgruppe vorgesehen. In dieser Instanz wurde die Zielgruppe aus Adobe Audience Manager (AAM) importiert.

![Registerkarte „Nutzung“ auf der Karte für die Zielgruppendefinition](assets/audience_definition_mc.png)

Für diese importierten Zielgruppentypen sind die folgenden Details verfügbar:

| Zielgruppentyp | Details |
|--- |--- |
| Mobile Zielgruppe | Marketing-Name, Hersteller und Modell.<br>Der `matches | does not match`-Operator wird anstelle `equals | does not equal`<br>![ der Importierten Mobilen Zielgruppe](/help/c-target/c-audiences/assets/imported_mobile_audience.png) angezeigt. |
| Besucherverhalten-Zielgruppe | **user.categoryAffinity:** `categoryAffinity` mit `FAVORITE`-Parameter.<br>![Importierte Kategorieaffinität ](/help/c-target/c-audiences/assets/imported_category_affinity.png)<br>**-Überwachung:** Überwachungsdienst ist True.<br>**Kein Überwachungsdienst:**&#x200B;Überwachungsdienst ist False.<br>![Importierte Überwachung](/help/c-target/c-audiences/assets/imported_monitoring.png) |
| Zielgruppen mit dem Operator NOT | **Einzelregel:** Target zeigt die Zielgruppe im Format `[All Visitor AND [NOT [rule]` an. Einzelne NOT-Regel wird mit UND mit `AllVisitor`-Zielgruppe angezeigt.<br>![Importierte Not-Zielgruppe](/help/c-target/c-audiences/assets/imported_not_audience.png) |

Berücksichtigen Sie beim Arbeiten mit importierten Zielgruppen Folgendes:

* Ausdrucksziel-Zielgruppen werden in Target Standard/Premium nicht mehr unterstützt.
* Target Standard/Premium unterstützt einige veraltete Zielgruppen nicht oder verfügt über verbesserte Operatoren zur einfachen Nutzung. Daher bedeutet die Definition einer importierten Zielgruppe trotz definitionsgemäßer Funktion nicht zwingendermaßen, dass dieselbe nun für die Erstellung in der Standard/Premium-Schnittstelle verfügbar ist. Beispielsweise sind soziale Zielgruppen zwar mit den zugehörigen Regeln sichtbar, aber Target Standard/Premium lässt die Erstellung sozialer Zielgruppen nicht zu.

## Schulungsvideo: Verwenden von Zielgruppen ![Tutorial-Badge](/help/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppen.

* Erläuterung des Begriffs „Zielgruppe“
* Erläuterung der beiden Arten, auf die Zielgruppen zur Optimierung eingesetzt werden
* Auffinden von Zielgruppen in der Zielgruppenliste
* Zuordnung einer Aktivität zu einer Zielgruppe
* Verwenden von Zielgruppen für die passive Berichterstattung zu einer Aktivität

>[!VIDEO](https://video.tv.adobe.com/v/17398)
