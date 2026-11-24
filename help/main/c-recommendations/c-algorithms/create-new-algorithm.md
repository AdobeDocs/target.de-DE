---
keywords: Kriterien;Algorithmus;Branche;Vertikal;Seitentyp;Empfehlungsschlüssel;Empfehlungslogik;Logik;Datenbereich;Lookback-Fenster;Verhaltensdatenquelle;Partielles Design;Backup-Empfehlungen;Einschlussregeln;Attributgewichtung;aktuelle Kategorie;benutzerdefiniertes Attribut;zuletzt gekauftes Element;zuletzt angezeigtes Element;am häufigsten angezeigtes Element;bevorzugte Kategorie;Beliebtheit;kürzlich angezeigtes Element;zuletzt gekauft;am häufigsten angezeigt;Favorit;zuletzt angezeigt
description: Erfahren Sie, wie Sie Kriterien erstellen, die den Inhalt Ihrer [!DNL Recommendations] steuern, um die Empfehlungen anzuzeigen, die für Ihre Aktivität am besten geeignet sind.
title: Wie erstelle ich [!UICONTROL Kriterien] in [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 3f4f59b2-6637-4c33-bf17-bff11bef7173
TQID: 'https://experienceleague.adobe.com/r9FWgHWw6NX1CmhqI-7MLoamNFDepeCq1bpiJ8eyISM'
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
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '2840'
ht-degree: 17%
---
# Erstellen von Kriterien {#create-criteria}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie in [!DNL Adobe Target Recommendations] Kriterien erstellen und jeden Abschnitt eines Kriteriums konfigurieren.

>[!ENDSHADEBOX]

Kriterien in [!DNL Adobe Target] [!DNL Recommendations] steuern den Inhalt [!DNL Recommendations] Aktivitäten. Kriterien verwenden die Aktionen des Besuchers, um zu bestimmen, welche Inhalte oder Produkte angezeigt werden sollen, sodass geeignete Kriterien die Empfehlungen zeigen, die für die Aktivität am besten geeignet sind.

## Aufrufen des Bildschirms Neue Kriterien erstellen {#access-create-criteria}

Sie haben viele Möglichkeiten, um auf den Bildschirm **[!UICONTROL Neue Kriterien erstellen]** zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie der Bildschirm erreicht wird.

* Klicken Sie im Bildschirm **&#x200B;**&#x200B;> **[!UICONTROL Kriterien]** Bibliothek auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**. Hier erstellte Kriterien werden automatisch für alle [!DNL Recommendations] Aktivitäten zur Verfügung gestellt.

  ![Kriterienseite mit geöffnetem Menü „Kriterien erstellen“, das die Optionen „Kriterien erstellen“ und „Kriteriensequenz erstellen“ anzeigt](../assets/criteria_create_1.png)

* Beim Erstellen einer [!DNL Recommendations] mit **[!UICONTROL Visual Experience Composer]** (VEC) wird der Bildschirm **[!UICONTROL Kriterien auswählen]** unmittelbar nach Auswahl eines Elements auf der Seite angezeigt und **[!UICONTROL Ersetzen mit Empfehlungen]**, **[!UICONTROL Empfehlungen einfügen vor]** oder **[!UICONTROL Empfehlungen einfügen nach]** angeklickt. Wählen Sie verfügbare Kriterien aus oder klicken Sie auf **[!UICONTROL Kriterien erstellen]**. Neue Kriterien können zur Verwendung mit anderen [!DNL Recommendations]-Aktivitäten gespeichert werden. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

  ![Kriterienbildschirm einer Recommendations -Aktivität mit der Schaltfläche Kriterien erstellen](../assets/criteria_create_2.png)

* Klicken Sie beim Bearbeiten einer [!DNL Recommendations] in ein Feld **[!UICONTROL Recommendations-Speicherort]** auf der Seite und wählen Sie **[!UICONTROL Kriterien ändern]**. Klicken Sie im **[!UICONTROL Kriterien auswählen]** auf **[!UICONTROL Kriterien erstellen]**. Die neuen Kriterien können zur Verwendung mit anderen [!DNL Recommendations]-Aktivitäten gespeichert werden.

## [!UICONTROL Basisinformationen] {#info}

Die grundlegenden Informationen identifizieren die Kriterien und kategorisieren sie für die Wiederverwendung in anderen Aktivitäten.

1. Geben Sie einen **[!UICONTROL Kriteriennamen]** ein.

   Dies ist der interne Name, der zur Beschreibung der Kriterien verwendet wird. Beispielsweise kann ein Kriterium als „Produkte mit der höchsten Spanne“ bezeichnet werden, ohne dass dieser Titel öffentlich angezeigt wird. Der öffentlich zugängliche Titel wird im nächsten Schritt festgelegt.

1. Geben Sie einen öffentlichen Titel **[!UICONTROL Titel anzeigen]** ein, der auf der Seite für alle Empfehlungen angezeigt werden soll, die diese Kriterien verwenden.

   Beispielsweise können „Personen, die dies angesehen haben“ oder „Ähnliche Produkte“ angezeigt werden, wenn dieses Kriterium zum Anzeigen von Empfehlungen verwendet wird.

1. Geben Sie eine kurze **[!UICONTROL Beschreibung]** der Kriterien ein.

   Die Beschreibung sollte dabei helfen, die Kriterien zu identifizieren, und könnte Informationen über ihren Zweck enthalten.

1. Wählen Sie basierend auf den Zielen der Recommendations-Aktivität eine Branche aus.

   | Vertikaler Markt | Ziel |
   |--- |--- |
   | **[!UICONTROL Retail/eCommerce]** | Zum Kauf führende Konversion |
   | **[!UICONTROL Lead-Generierung/B2B/Finanzdienstleistungen]** | Konversion ohne Kauf |
   | **[!UICONTROL Medien/Veröffentlichen]** | Interaktion |

   Andere Kriterienoptionen ändern sich je nach ausgewählter Branche.

   ![Abschnitt „Grundlegende Informationen“ im Dialogfeld „Kriterien erstellen“, in dem die Liste „Branche/Vertikal“ geöffnet und ihre drei Optionen hervorgehoben sind](../assets/criteria_create_3.png)

1. Wählen Sie einen **[!UICONTROL Seitentyp]** aus.

   Es können mehrere Seitentypen ausgewählt werden. Gemeinsam helfen die vertikalen und Seitentypen der Branche dabei, gespeicherte Kriterien zu kategorisieren, wodurch die Wiederverwendung von Kriterien für andere [!DNL Recommendations]-Aktivitäten erleichtert wird.

## [!UICONTROL Empfehlungs-Algorithmus] {#rec-algo}

Der Algorithmus bestimmt, wie die Elemente für die Empfehlungen ausgewählt werden.

>[!CONTEXTUALHELP]
>id="target_recommendations_profile_attribute"
>title="Profilattribut"
>abstract="Sie können ein Profilattribut mithilfe von Profilskripts erstellen."

1. Wählen Sie einen **[!UICONTROL Algorithmustyp]** und **[!UICONTROL Algorithmus]**:

   ![Empfohlener Abschnitt zum Algorithmus](assets/recommended-algorithm.png)

   | Algorithmustyp | Verwendung der verfügbaren Algorithmen / |
   | --- | --- |
   | **[!UICONTROL Warenkorbbasiert]** | Empfehlungen auf der Grundlage des Warenkorbinhalts des Benutzers aussprechen. <ul><li>**[!UICONTROL Personen, die diese angesehen haben, haben auch Folgendes angesehen]** </li><li>**[!UICONTROL Personen, die diese angesehen haben, kauften auch]**</li><li>**[!UICONTROL Personen, die diese gekauft haben, kauften auch]**</li></ul> |
   | **[!UICONTROL Beliebtheitsbasiert]** | Empfehlungen auf der Grundlage der allgemeinen Popularität eines Elements auf der gesamten Website oder der Popularität von Elementen innerhalb der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. des Benutzers geben. <ul><li>**[!UICONTROL Am häufigsten auf der Website angezeigt]**</li><li>**[!UICONTROL Am häufigsten angezeigt nach Kategorie]**</li><li>**[!UICONTROL Am häufigsten angezeigt nach Elementattribut]**</li><li>**[!UICONTROL Meist gesehen nach Profilattribut]**</li><li>**[!UICONTROL Topverkäufe auf der Website]**</li><li>**[!UICONTROL Topverkäufe nach Kategorie]**</li><li>**[!UICONTROL Topverkäufe nach Artikelattribut]**</li><li>**[!UICONTROL Topverkäufe nach Profilattribut]**</li><li>**[!UICONTROL Am besten nach Analytics-Metrik]**</li></ul> |
   | **[!UICONTROL Elementbasiert]** | Empfehlungen auf der Grundlage von Elementen geben, die einem Element ähneln, das der Benutzer gerade anzeigt oder kürzlich angeschaut hat. <ul><li>**[!UICONTROL Personen, die dies angesehen haben, haben dies angesehen]**</li><li>**[!UICONTROL Leute, die das angesehen haben, kauften das]**</li><li>**[!UICONTROL Personen, die das gekauft haben, kauften das]**</li><li>**[!UICONTROL Elemente mit ähnlichen Attributen]**</li></ul> |
   | **[!UICONTROL Benutzerbasiert]** | Empfehlungen auf der Grundlage des Benutzerverhaltens aussprechen.<ul><li>**[!UICONTROL Vor Kurzem aufgerufene Artikel]**</li><li>**[!UICONTROL Empfohlen für Sie]**</li></ul> |
   | **[!UICONTROL Benutzerdefinierte Kriterien]** | Empfehlungen basierend auf einer hochgeladenen benutzerdefinierten Datei aussprechen.<ul><li>Benutzerdefinierter Algorithmus</li></ul> |

   >[!NOTE]
   >
   >Wenn **[!UICONTROL Elemente]**/ **[!UICONTROL Medien mit ähnlichen Attributen]** ausgewählt ist, können [Inhaltsähnlichkeitsregeln](#similarity) festgelegt werden.

1. Konfigurieren Sie den Algorithmus nach Bedarf, indem Sie **[!UICONTROL Empfehlungsschlüssel]**, **[!UICONTROL Filterschlüssel]**, **[!UICONTROL Basis für gleichzeitiges Auftreten]**, **[!UICONTROL Analytics-Metrik]** und/oder **[!UICONTROL Elementattribut]** und **[!UICONTROL Profilattribut abgleichen]**. Die verfügbaren Konfigurationsoptionen variieren je nach ausgewähltem Algorithmus.

   Weitere Informationen zur Auswahl eines **[!UICONTROL Empfehlungsschlüssels]** finden Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. (Bedingt) Wählen Sie für **[!UICONTROL Am häufigsten angezeigt nach Profilattribut]** oder **[!UICONTROL Topverkäufe nach]** Profilattribut) ein **[!UICONTROL Profilattribut]** aus, um die Interaktionsdaten nach folgenden Kriterien zu gruppieren.

   Profilattribute stammen von einem Profilskript, das Besuchermerkmale erfasst, z. B. Region oder Land. Der Skriptname muss das `recsAttribute` Präfix enthalten, sodass er als `user.recsAttribute<Name>` gespeichert wird, z. B. `user.recsAttributeRegion`. Zum Zeitpunkt des Versands stellt [!DNL Target] jedem Besucher die Rangfolgenliste bereit, die seinem eigenen Wert dieses Attributs entspricht.

## [!UICONTROL Inhalt sichern] {#content}

**[!UICONTROL Inhalt sichern]** bestimmen, was passiert, wenn die Anzahl der empfohlenen Elemente nicht dem „Recommendations[Design &#x200B;](/help/main/c-recommendations/c-design-overview/design-overview.md). Kriterien können weniger Empfehlungen zurückgeben als im Design-Aufruf vorgesehen. Wenn das Design beispielsweise Slots für vier Elemente hat, die Kriterien jedoch nur zwei Elemente verursachen, die empfohlen werden, können die verbleibenden Slots leer gelassen oder mit Backup-Empfehlungen gefüllt werden oder es können keine Recommendations angezeigt werden.

1. (Optional) Aktivieren Sie die Option **[!UICONTROL Teilweises Design-Rendering]** .

   Es sind so viele Steckplätze wie möglich belegt, aber die Design-Vorlage kann Leerraum für die verbleibenden Steckplätze enthalten. Wenn diese Option deaktiviert ist und nicht genügend Inhalt vorhanden ist, um alle verfügbaren Slots zu füllen, werden keine Empfehlungen bereitgestellt und stattdessen Standardinhalte angezeigt.

   Aktivieren Sie diese Option, um Empfehlungen mit leeren Slots bereitzustellen. Um die leeren Slots mit ähnlichen oder beliebten Inhalten von der Site zu füllen, verwenden Sie Sicherungsempfehlungen, wie im nächsten Schritt erläutert.

1. (Optional) Aktivieren Sie die Option **[!UICONTROL Sicherungsinhalt anzeigen]**.

   Backup-Empfehlungen füllen alle verbleibenden leeren Slots im Design mit einer zufälligen Auswahl der am häufigsten angezeigten Produkte aus der gesamten Site, sodass das Design immer alle verfügbaren Slots füllt. Im folgenden Beispiel wird ein 4 x 1-Design verwendet:

   ![4 x 1 Design](../assets/velocity_example.png)

   Wenn die Kriterien dazu führen, dass nur zwei Elemente empfohlen werden und die Option **[!UICONTROL Teilweises Design-Rendering]** aktiviert ist, werden die ersten beiden Slots gefüllt und die verbleibenden zwei Slots bleiben leer. Wenn die Option **[!UICONTROL Backup-Inhalt anzeigen]** aktiviert ist, werden die ersten beiden Slots auf der Grundlage der angegebenen Kriterien und die verbleibenden zwei Slots auf der Grundlage der Backup-Empfehlungen gefüllt.

   +++ Die folgende Matrix zeigt das Ergebnis für jede Kombination der Optionen **[!UICONTROL Teilweises Design-Rendering]** und **[!UICONTROL Backup-Inhalt]**

   | Teilweises Entwurfs-Rendering | Backup-Inhalt | Ergebnis |
   |--- |--- |--- |
   | Deaktiviert | Deaktiviert | Wenn weniger Empfehlungen zurückgegeben werden als im Entwurf vorgesehen, wird der Empfehlungsentwurf durch Standardinhalte ersetzt und es erscheinen keine Empfehlungen. |
   | Aktiviert | Deaktiviert | Das Design wird gerendert, kann jedoch Leerzeichen enthalten, wenn weniger Empfehlungen zurückgegeben werden als vom Design angefordert. |
   | Aktiviert | Aktiviert | Backup-Empfehlungen füllen die verfügbaren Design-„Slots“ aus und geben das Design vollständig wieder.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf nur teilweise gerendert.<br>In dem Fall, dass die Kriterien keine Empfehlungen zurückgeben und die Einschlussregeln die Ersatzempfehlungen auf null reduzieren, wird der Entwurf durch Standardinhalte ersetzt. |
   | Deaktiviert | Aktiviert | Backup-Empfehlungen füllen die verfügbaren Design-„Slots“ aus und geben das Design vollständig wieder.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf durch Standardinhalte ersetzt und es werden keine Empfehlungen angezeigt. |

   Weitere Informationen finden Sie unter [Verwenden einer Sicherungsempfehlung](/help/main/c-recommendations/c-algorithms/backup-recs.md).
   +++

1. (Bedingt) Wenn **[!UICONTROL Sicherungsinhalt anzeigen]** aktiviert ist, kann **[!UICONTROL Einschlussregeln auf Sicherungsempfehlungen anwenden]** auch aktiviert werden.

   Einschlussregeln bestimmen, welche Elemente in den Empfehlungen enthalten sind. Die verfügbaren Optionen hängen von der vertikalen Märkte ab.

   Weitere Informationen finden Sie [&#x200B; „Einschlussregeln angeben](#inclusion) unten.

## [!UICONTROL Daten-Source] {#data-source}

Die Datenquelle bestimmt die von den Kriterien verwendeten Verhaltensdaten und den Zeitbereich dieser Daten.

1. Wählen Sie die gewünschte **[!UICONTROL Verhaltensdaten-Source]** aus: **[!UICONTROL Adobe Target]** oder **[!UICONTROL Analytics]**.

   >[!NOTE]
   >
   >Der Abschnitt **[!UICONTROL Verhaltensdaten-Source]** wird nur angezeigt, wenn die Implementierung [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwendet.

   ![Abschnitt „Data Source&quot; mit hervorgehobenen Source-Optionen für Verhaltensdaten, Adobe Target und Analytics](../assets/criteria_create_4.png)

   Wählen **[!UICONTROL unter]** die gewünschte Report Suite aus.

   +++ Verfügbarkeit der Kriterien, wenn Analytics die Datenquelle ist

   Wenn [!DNL Adobe Analytics] die Verhaltensdatenquelle ist, hängt die Zeit bis zur Verfügbarkeit eines neuen Kriteriums davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster für andere Kriterien verwendet wurden:

   * **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitrahmen hängt von der [!DNL Analytics] Systemlast ab.
   * **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn beim Erstellen eines neuen Kriteriums oder Bearbeiten eines vorhandenen Kriteriums die ausgewählte Report Suite bereits mit [!DNL Target Recommendations] verwendet wurde und der Datenbereich gleich oder größer dem ausgewählten Datenbereich ist, sind die Daten sofort verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
   * **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Bei der Empfehlung **[!UICONTROL Angezeigte Affinität]** wird beim Anzeigen eines Produkts durch einen Benutzer nahezu in Echtzeit ein Tracking-Aufruf für die Produktansicht an [!DNL Analytics] übergeben. Die [!DNL Analytics]-Daten werden am Morgen des nächsten Tages an [!DNL Target] gesendet und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

   Weitere Informationen finden Sie unter [Verwenden von Adobe Analytics mit Target Recommendations](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

   +++



1. Legen Sie das **[!UICONTROL Lookback-Fenster]** fest, um den Zeitbereich der verfügbaren historischen Benutzerverhaltensdaten zu bestimmen, die bei der Bestimmung der anzuzeigenden Empfehlungen verwendet werden sollen. Diese Option steht für alle Algorithmen mit Ausnahme von **[!UICONTROL Elementen mit ähnlichen Attributen]** und **[!UICONTROL benutzerdefinierten Algorithmen]** zur Verfügung.

   Wählen Sie für eine Site mit viel Traffic, bei der sich das Verhalten häufig ändert, ein kürzeres Datenfenster. Ein kürzeres Fenster ermöglicht [!DNL Recommendations], besser auf Veränderungen am Markt und im Unternehmen zu reagieren. [!DNL Recommendations] erkennt dann beispielsweise Änderungen im Besucherverhalten, wenn Besucher mit dem saisonalen Einkaufen beginnen, z. B. mit dem Einkaufen in die Schule oder zu Weihnachten, und empfiehlt Artikel, die für diese Einkaufssaisons geeignet sind.

   Wenn die Site nicht viele Daten enthält oder sich das Besucherverhalten nicht häufig ändert, wählen Sie ein längeres Fenster aus. Für viele Sites führt jedoch ein kürzeres Fenster zu qualitativ hochwertigeren Empfehlungen.

   +++ Verfügbare Datenbereiche

   | Option „Lookback-Fenster“ | Aktualisierte Häufigkeit (wird beim Bewegen des Mauszeigers angezeigt) | Unterstützte Algorithmen |
   | --- | --- | --- |
   | Sechs Stunden | Algorithmus wird alle 3-6 Stunden ausgeführt | **[!UICONTROL Beliebtheitsalgorithmen]** wenn die ausgewählte **[!UICONTROL Verhaltensdaten-Source]** [!DNL Adobe Target] wird |
   | Ein Tag | Algorithmus wird alle 12-24 Stunden ausgeführt | **[!UICONTROL Beliebtheitsbasierte]** Algorithmen |
   | Zwei Tage | Algorithmus wird alle 12-24 Stunden ausgeführt | <ul><li>**[!UICONTROL Beliebtheitsbasierte]** Algorithmen</li><li>**[!UICONTROL Elementbasierte]** Algorithmen</li><li>**[!UICONTROL Benutzerbasierte]** Algorithmen</li><li>**[!UICONTROL Warenkorb-basierte]** Algorithmen</li></ul> |
   | Eine Woche | Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>**[!UICONTROL Beliebtheitsbasierte]** Algorithmen</li><li>**[!UICONTROL Elementbasierte]** Algorithmen</li><li>**[!UICONTROL Benutzerbasierte]** Algorithmen</li><li>**[!UICONTROL Warenkorb-basierte]** Algorithmen</li></ul> |
   | Zwei Woche | Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>**[!UICONTROL Beliebtheitsbasierte]** Algorithmen</li><li>**[!UICONTROL Elementbasierte]** Algorithmen</li><li>Alle **[!UICONTROL benutzerbasierten]** Algorithmen</li><li>**[!UICONTROL Warenkorb-basierte]** Algorithmen</li></ul> |
   | Ein Monat (30 Tage) | Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>**[!UICONTROL Beliebtheitsbasierte]** Algorithmen</li><li>**[!UICONTROL Elementbasierte]** Algorithmen</li><li>**[!UICONTROL Benutzerbasierte]** Algorithmen</li><li>**[!UICONTROL Warenkorb-basierte]** Algorithmen</li></ul> |
   | Zwei Monate (61 Tage) | Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>**[!UICONTROL Beliebtheitsbasierte]** Algorithmen</li><li>**[!UICONTROL Elementbasierte]** Algorithmen</li><li>**[!UICONTROL Benutzerbasierte]** Algorithmen</li><li>**[!UICONTROL Warenkorb-basierte]** Algorithmen</li></ul> |

   +++

## Ähnlichkeit von Inhalten {#similarity}

Verwenden Sie Regeln zur **[!UICONTROL Ähnlichkeit von Inhalten]** für die Bereitstellung von Empfehlungen basierend auf Artikeln oder Medienattributen.

![Abschnitt „Inhaltsähnlichkeit“ mit einer entity.name-Regel und den hervorgehobenen Schaltflächen „Regel hinzufügen“ und „Regeln löschen“](../assets/criteria_create_5.png)

Mithilfe der Funktion für Ähnlichkeit von Inhalten werden Artikelattribut-Schlüsselwörter verglichen und Empfehlungen basierend darauf erstellt, wie viele Schlüsselwörter die verschiedenen Artikel gemeinsam haben. Für Empfehlungen, die auf Inhaltsähnlichkeit basieren, sind keine historischen Daten erforderlich.

Die Ähnlichkeit des Inhalts ist für neue Elemente wirksam, die wahrscheinlich nicht in Empfehlungen angezeigt werden, indem *Personen, die diese Ansicht angezeigt haben, auch angezeigt haben* und andere Logiken verwendet werden, die auf vergangenem Verhalten basieren. Es kann auch Empfehlungen für neue Besucher generieren, die keine früheren Käufe oder andere historische Daten haben.

Wenn **[!UICONTROL Elementbasiert/]**&#x200B;**[!UICONTROL Element mit ähnlichen Attributen]** ausgewählt ist, können Regeln erstellt werden, um die Bedeutung bestimmter Elementattribute für die Bestimmung von Empfehlungen zu erhöhen oder zu verringern. Bei Elementen wie Büchern kann die Wichtigkeit von Attributen wie *genre*, *author*, *series* usw. erhöht werden, um ähnliche Bücher zu empfehlen.

Die Inhaltsähnlichkeit verwendet Schlüsselwörter, um Elemente zu vergleichen, sodass einige Attribute, wie *Nachricht* oder *Beschreibung*, „Rauschen“ in den Vergleich einführen können. Es können Regeln erstellt werden, um diese Attribute zu ignorieren.

Standardmäßig sind alle Attribute auf den Wert *Grundlinie* eingestellt. Eine Regel ist nur erforderlich, um diese Einstellung zu ändern.

>[!NOTE]
>
>Der Inhaltsähnlichkeits-Algorithmus kann beim Berechnen der Ähnlichkeit zwischen Elementen ein Zufallsstichprobe verwenden. Infolgedessen können die Ähnlichkeitsbewertungen zwischen Elementen zwischen den Algorithmusausführungen variieren.

## Einschlussregeln {#inclusion}

Einschlussregeln grenzen die in den Empfehlungen angezeigten Elemente ein. Sie können beim Erstellen von Kriterien oder Promotions verwendet werden. Einschlussregeln sind optional. Wenn Sie diese Details festlegen, haben Sie mehr Kontrolle über die Elemente, die in den Empfehlungen angezeigt werden. Jedes konfigurierte Detail grenzt die Anzeigekriterien weiter ein.

Beispielsweise können nur Damenschuhe angezeigt werden, deren Inventar mehr als 50 Dollar und deren Preis zwischen 25 und 45 Dollar liegt. Jedes Attribut kann auch so gewichtet werden, dass die Elemente, die für das Unternehmen wichtiger sind, am wahrscheinlichsten erscheinen. Ein weiteres Beispiel: Stellenangebote können nur Besucherinnen und Besuchern angezeigt werden, die die Website aus bestimmten Städten besuchen und die die erforderlichen Hochschulabschlüsse besitzen.

Die Optionen für die Einschlussregeln variieren je nach vertikalem Markt. Einschlussregeln werden standardmäßig auf Ersatzempfehlungen angewendet. Die Einschlussregeln sind mit einem UND verbunden, sodass alle Regeln erfüllt sein müssen, damit ein Element in eine Empfehlung aufgenommen wird.

>[!IMPORTANT]
>
>Verwenden Sie Einschlussregeln mit Vorsicht. Sie sind beispielsweise nützlich, wenn in einer Organisation Regeln gelten, nach denen eine Marke nicht empfohlen wird, während eine andere Marke angezeigt wird. Diese Funktion hat jedoch Opportunity-Kosten: Durch die Beschränkung von Elementen, die die Aktivitätskriterien normalerweise anzeigen würden, könnte ein Prozentsatz der Steigerung verloren gehen.

Mit den folgenden Schritten wird eine einfache Einschlussregel erstellt, die nur Damenschuhe mit einem Inventar von mehr als 50 und einem Preis zwischen 25 und 45 US-Dollar anzeigt:

1. (Bedingt) Aktivieren Sie **[!UICONTROL Zulassen, dass kürzlich gekaufte Artikel empfohlen werden]**.

   Diese Einstellung basiert auf `productPurchasedId`. Das Standardverhalten ist es, zuvor gekaufte Artikel nicht zu empfehlen. In den meisten Fällen sollten Artikel, die ein Kunde kürzlich gekauft hat, nicht beworben werden. Die Einstellung ist nützlich für Gegenstände, die normalerweise nur einmal gekauft werden, wie Kajaks. Aktivieren Sie diese Option für Artikel, die wiederholt gekauft werden, z. B. Shampoo oder andere persönliche Artikel.

1. Legen Sie eine Preisspanne für die zu empfehlenden Produkte fest.

1. Legen Sie den Mindestinventarbetrag für die zu empfehlenden Produkte fest.

1. Konfigurieren Sie die Empfehlung, um nur Artikel anzuzeigen, wenn sie bestimmte Kriterien erfüllen.

   Elemente können nur einbezogen werden, wenn eines der Attribute in der Liste eine oder mehrere angegebene Bedingungen erfüllt oder nicht erfüllt.

   Die verfügbaren Auswerter hängen vom Wert ab, der in der ersten Dropdown-Liste ausgewählt wurde. Es können mehrere Elemente aufgelistet werden, die mit ODER ausgewertet werden. Mehrere Regeln werden mit „AND“ kombiniert.

   >[!NOTE]
   >
   >Diese Option beschränkt die in der Empfehlung angezeigten Elemente. Sie hat keine Auswirkungen darauf, auf welchen Seiten die Empfehlung angezeigt wird. Um eine Einschränkung bezüglich der Anzeige der Empfehlung vorzunehmen, wählen Sie die Seiten im Experience Composer aus.

Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Attributgewichtung {#weighting}

Es können mehrere Regeln hinzugefügt werden, um den Algorithmus basierend auf wichtigen Informationen oder Metadaten zum Inhaltskatalog „anzustoßen“, sodass bestimmte Elemente mit höherer Wahrscheinlichkeit angezeigt werden.

Beispielsweise kann eine höhere Gewichtung auf Artikel im Angebot angewendet werden, sodass sie häufiger in der Empfehlung angezeigt werden. Artikel, die nicht Teil des Sonderangebots sind, werden nicht vollständig ausgeschlossen, jedoch weniger häufig angezeigt. Auf denselben Algorithmus können mehrere gewichtete Attribute angewendet werden und die gewichteten Attribute können mit dem in der Empfehlung aufgeteilten Traffic getestet werden.

1. Wählen Sie einen Wert aus.

   Der Wert bestimmt den Typ des Elements, das mit größerer Wahrscheinlichkeit und auf der Basis mehrerer verfügbarer Kriterien angezeigt wird.

1. Wählen Sie einen Auswerter.

1. Geben Sie das Keyword ein, um die Regelattribute abzuschließen.

   Die vollständige Regel könnte beispielsweise lauten: „Kategorie enthält Teilzeichenfolgen-Schuhe.“

1. Wählen Sie die Wertigkeit aus, die der Regel zugeordnet werden soll.

   Die Gewichtung kann von 0 bis 100 in 25er-Schritten eingestellt werden.

1. Fügen Sie nach Bedarf weitere Regeln hinzu.

Klicken Sie abschließend auf **[!UICONTROL Erstellen]**.

Wenn eine neue **[!UICONTROL Recommendations]**-Aktivität erstellt oder eine vorhandene bearbeitet wird, ist **[!UICONTROL Kontrollkästchen „Kriterien für später]**&quot; standardmäßig aktiviert. Um die Verwendung der Kriterien in anderen Aktivitäten zu verhindern, deaktivieren Sie vor dem Speichern das Kontrollkästchen.
