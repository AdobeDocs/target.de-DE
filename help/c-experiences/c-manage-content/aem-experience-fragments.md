---
description: Informationen zur Verwendung von Erlebnisfragmenten, die in Adobe Experience Manager (AEM) in Target-Aktivitäten erstellt werden, um die Optimierung oder Personalisierung zu unterstützen.
keywords: Erlebnis;AEM;Adobe Experience Manager;nach Adobe Target exportieren;Erlebnisfragmente;Fragmente;XF
seo-description: Informationen zur Verwendung von Erlebnisfragmenten, die in Adobe Experience Manager (AEM) in Target-Aktivitäten erstellt werden, um die Optimierung oder Personalisierung zu unterstützen.
seo-title: AEM-Erlebnisfragmente
solution: Target
title: AEM-Erlebnisfragmente
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# AEM-Erlebnisfragmente{#aem-experience-fragments}

Informationen zur Verwendung von Erlebnisfragmenten, die in Adobe Experience Manager (AEM) in Target-Aktivitäten erstellt werden, um die Optimierung oder Personalisierung zu unterstützen.

## AEM-Erlebnisfragmente {#topic_1E1E4EA01F074349B2CF8785387B5FE8}

Informationen zur Verwendung von Erlebnisfragmenten, die in Adobe Experience Manager (AEM) in Target-Aktivitäten erstellt werden, um die Optimierung oder Personalisierung zu unterstützen.

>[!NOTE]
>
>Für diese Funktion müssen Sie AEM-Kunde (Adobe Experience Manager-) sein. Weitere Informationen finden Sie unten unter [Anforderungen](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A).

## Überblick {#section_95A91830530F493B81C5C9CDB9B783EA}

Mithilfe von in AEM in Target-Aktivitäten erstellten Erlebnisfragmenten können Sie die Benutzerfreundlichkeit und Leistungsfähigkeit von AEM mit den leistungsstarken Funktionen der automatisierten Intelligenz (AI) und des maschinellen Lernens (ML) in Target kombinieren, um Erlebnisse bedarfsgerecht zu testen und zu personalisieren.

AEM kombiniert all Ihre Inhalte und Assets an einer zentralen Stelle, um Ihre Personalisierungsstrategie zu begünstigen. Mit AEM können Sie an einer Stelle problemlos Inhalte für Desktops, Tablets und mobile Geräte erstellen, ohne Code zu schreiben. Es müssen keine Seiten für jedes Gerät erstellt werden - AEM passt die einzelnen Erlebnisse automatisch mit Ihren Inhalten an.

Mit Target können Sie personalisierte Erlebnisse bedarfsgerecht bereitstellen. Dies erfolgt auf der Grundlage einer Kombination aus regelbasierten und AI-gestützten Ansätzen des maschinellen Lernens, zu denen Verhaltens-, Kontext- und Offline-Variablen zählen.  Target ermöglicht Ihnen die problemlose Einrichtung und Ausführung von A/B- und multivariaten Aktivitäten (MVT), um die besten Angebote, Inhalte und Erlebnisse zu bestimmen.

Erlebnisfragmente sind ein großer Schritt in Richtung der Verknüpfung zwischen den Erstellern von Inhalten/Erlebnissen und Managern mit den Optimierungs- und Personalisierungsexperten, die Geschäftsergebnisse mit Target optimieren.

## Voraussetzungen {#section_AE6F0971E1574B3AA324003599B96E5A}

Sie müssen über die Funktion für Erlebnisfragmente in Target verfügen. Darüber hinaus müssen Sie AEM 6.3 mit dem richtigen Service Pack oder AEM 6.4 (oder höher) verwenden. Ihr Kundenbetreuer kann Ihnen helfen, die Anforderungen zur Verwendung dieser Funktion zu erfüllen:

* Adobe Experience Manager 6.4 (oder höher).
* Adobe Experience Manager 6.3 SP2 (oder höher).
* Adobe Target Standard- oder Adobe Target Premium-Konto.
* Wenden Sie sich an die Adobe Target-Kundenunterstützung, um die Integration zu aktivieren und Details zur Authentifizierung zu erhalten.

## Erstellen und Konfigurieren von Erlebnisfragmenten in AEM {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Um AEM-Erlebnisfragmente in Target verwenden zu können, müssen Sie die folgenden Schritte ausführen:

### Schritt 1: AEM in Target integrieren

Weitere Informationen finden Sie unter:

* **AEM 6.3:**[Abonnieren von Adobe Analytics und Adobe Target](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) in der Dokumentation zu _Adobe Experience Manager 6.3_.
* **AEM 6.4:**[Abonnieren von Adobe Analytics und Adobe Target](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) in der Dokumentation zu _Adobe Experience Manager 6.4_.

### Schritt 2: Erlebnisfragment erstellen

Erlebnisfragmente werden in AEM erstellt. Weitere Informationen finden Sie unter:

* **AEM 6.3:** [Erlebnisfragmente](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) in der Dokumentation zu *Adobe Experience Manager 6.3*.
* **AEM 6.4:**[Erlebnisfragmente](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) in der Dokumentation zu *Adobe Experience Manager 6.4*.

### Schritt 3: AEM für das Teilen des Erlebnisfragments mit Target konfigurieren

1. Wählen Sie in AEM das gewünschte Erlebnisfragment oder den Ordner, der dieses Fragment enthält, und klicken Sie dann auf [!UICONTROL Eigenschaften].
2. Klicken Sie auf die Registerkarte [!UICONTROL Cloud-Services] und wählen Sie dann in der Dropdownliste [!UICONTROL Cloud-Servicekonfiguration] den Eintrag [!UICONTROL Adobe Target] aus.

   >[!NOTE]
   >
   >Beim vorherigen Schritt wird davon ausgegangen, dass die Adobe Target-Konfiguration von einem Benutzer in Ihrem Unternehmen erstellt wurde.

3. Klicken Sie auf [!UICONTROL Speichern &amp; Schließen].

### Schritt 4: Das Erlebnisfragment veröffentlichen und nach Target exportieren

**AEM 6.3:**

1. Wählen Sie in AEM das gewünschte Erlebnisfragment aus, klicken Sie auf die Registerkarte [!UICONTROL Veröffentlichen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Veröffentlichen].
2. Wählen Sie in AEM das gewünschte Erlebnisfragment aus, klicken Sie auf [!UICONTROL Nach Adobe Target exportieren] und klicken Sie dann auf [!UICONTROL OK].

   ![](assets/experience_fragment_export_to_target.png)

**AEM 6.4:**

1. Wählen Sie in AEM das gewünschte Erlebnisfragment aus und klicken Sie auf [!UICONTROL Nach Adobe Target exportieren].

   ![](assets/experience_fragment_export_to_target.png)

2. Wählen Sie im anschließend angezeigten Dialogfeld [!UICONTROL Veröffentlichen] aus, um alle Assets innerhalb des Erlebnisfragments in [!DNL Target] zu veröffentlichen.

## Using Experience Fragments in Target Activities {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nach dem Ausführen der zuvor genannten Aufgaben wird das Erlebnisfragment auf der Seite [!UICONTROL Angebote] in Target angezeigt.

>[!NOTE]
>
>Target sucht derzeit alle zehn Minuten nach zu importierenden Erlebnisfragmenten. Das importierte Erlebnisfragment sollte innerhalb von zehn Minuten in Target verfügbar sein. Dieser Zeitraum soll in Zukunft weiter reduziert werden.

>[!IMPORTANT]
>
>Das Erlebnisfragment wird derzeit in Target als HTML-Angebot importiert. Beachten Sie, dass die „Master“-Version des Erlebnisfragments in AEM verbleibt. Sie können das Erlebnisfragment nicht in Target bearbeiten.

Sie können den Mauszeiger über ein Erlebnisfragment in der Liste bewegen und dann auf das Ansichtssymbol (![](assets/icon_info.png)

) klicken, um weitere Informationen über das Erlebnisfragment anzuzeigen, einschließlich der Bereitstellungs-URL für das öffentliche Angebot, des AEM-Pfades und eines Deep-Links zum Öffnen des Erlebnisfragments innerhalb von AEM.

Mit dem Visual Experience Composer (VEC) oder dem Form-Based Experience Composer können Sie Erlebnisfragmente in Target-Aktivitäten verwenden.

>[!NOTE]
>
>Um die KI- und ML-Funktionen von Target vollständig zu nutzen, können Sie beim Erstellen von A/B-Tests die Option [Automatische Zuordnung](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) oder [Automatisierte Personalisierung](../../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) auswählen.

**So verwenden Sie Erlebnisfragmente mit dem VEC:**

1. Wählen Sie in Target beim Erstellen oder Bearbeiten eines Erlebnisses im [Visual Experience Composer](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D) auf die Stelle auf der Seite, an der Sie AEM-Inhalt einfügen möchten. Wählen Sie dann **[!UICONTROL Mit Erlebnisfragment tauschen]** aus, um die Liste [!UICONTROL Erlebnisfragment auswählen] anzuzeigen.

   >[!NOTE]
   >
   >Die Option [!UICONTROL Mit Erlebnisfragment tauschen] ist nicht für Bilder verfügbar. Wenn Sie diese Option mit einem Bild verwenden möchten, klicken Sie auf das Containerelement, das das gewünschte Bild enthält.

   In der Liste [!UICONTROL Erlebnisfragment] werden alle in AEM erstellten Inhalte angezeigt, die von nun an in Target verfügbar sind.

   ![](assets/experience_fragment_list.png)

1. Wählen Sie das gewünschte Erlebnisfragment aus und klicken Sie dann auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

   Weitere Informationen über die Konfiguration der verschiedenen Aktivitätstypen finden Sie in den folgenden Themen:

   * **A/B-Test:** [Erstellen eines A/B-Tests](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)
   * **Automatische Zuordnung:** [Automatische Zuordnung](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisches Targeting:** [Automatisches Targeting für personalisierte Erlebnisse](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3)
   * **Automatisierte Personalisierung (AP):**[Erstellen einer Aktivität zur automatisierten Personalisierung](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Erlebnis-Targeting (XT):** [Erstellen einer Erlebnis-Targeting-Aktivität](../../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Multivarianz-Tests (MVT):** [Erstellen eines Multivarianz-Tests](../../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Recommendations:** [Erstellen einer Recommendations-Aktivität](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**So verwenden Sie Erlebnisfragmente mit dem Form-Based Experience Composer:**

1. Wählen Sie in Target beim Erstellen oder Bearbeiten eines Erlebnisses im [Form-Based Experience Composer](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) die Stelle auf der Seite aus, an der Sie AEM-Inhalt einfügen möchten. Wählen Sie dann **[!UICONTROL Mit Erlebnisfragment tauschen]** aus, um die Liste [!UICONTROL Erlebnisfragment auswählen] anzuzeigen.

   ![](assets/experience_fragment_list.png)

   In der Liste [!UICONTROL Erlebnisfragment] werden alle in AEM erstellten Inhalte angezeigt, die von nun an in Target verfügbar sind.

1. Wählen Sie das gewünschte Erlebnisfragment aus und klicken Sie dann auf **[!UICONTROL Speichern]**.
1. Schließen Sie die Konfiguration der Aktivität ab.

## Schulungsvideo: Verwenden von AEM-Erlebnisfragmenten mit Adobe Target {#section_C0EDC54063464F41A182492D2045BC64}

Das folgende Video zeigt, wie Sie Erlebnisfragmente einrichten und verwenden können: [Verwenden von AEM-Erlebnisfragmenten in Adobe Target](https://helpx.adobe.com/experience-manager/kt/sites/using/experience-fragment-target-feature-video-use.html).
