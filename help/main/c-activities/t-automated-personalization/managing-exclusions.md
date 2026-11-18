---
keywords: Deduplizierung;Duplikate zulassen;doppelte Angebote ausschließen;Automated Personalization;doppelte Angebote nicht zulassen;ausschließen;Standardinhalt;
description: Verwalten Sie Ausschlüsse in [!UICONTROL Automated Personalization]-Aktivitäten (AP).
title: Wie verwalte ich Ausschlüsse in [!UICONTROL Automated Personalization]-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
TQID: 'https://experienceleague.adobe.com/ERpNwQPsIRBmU0vTZbGa-lYg30BYl-uJxA8UT0f6060'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 4%
---
# Verwalten von Ausschlüssen {#manage-exclusions}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie in **[!UICONTROL Automated Personalization-Aktivitäten doppelte Angebote verhindern, bestimmte Erlebnisse ausschließen und Standardinhalte]**.

>[!ENDSHADEBOX]

Ausschlüsse steuern, welche Angebote und Erlebnisse eine **[!UICONTROL Automated Personalization]** (AP)-Aktivität bereitstellt. Sie verhindern, dass dasselbe Angebot zweimal angezeigt wird, entfernen Angebotskombinationen, die nicht zusammenarbeiten, und entfernen Standardinhalte, sodass die Aktivität sauberere und relevantere Erlebnisse bietet, die mit Ihren Zielen und Ihrer Audience übereinstimmen.

## Doppelte Angebote zulassen oder nicht zulassen {#allow-duplicate-offers}

<a id="concept_4EF78013F80E48EFA024AE0274C9F037"></a>

Verhindern Sie, dass Angebote aus der Angebotsbibliothek dupliziert werden, wenn sie an verschiedenen Stellen in AP-Aktivitäten verwendet werden.

Eine Aktivität kann beispielsweise sechs Orte auf einer Seite mit zwölf Angeboten umfassen, sodass dasselbe Angebot an mehr als einer Stelle platziert werden kann. Durch das Deaktivieren doppelter Angebote wird verhindert, dass dasselbe Angebot gleichzeitig an verschiedenen Stellen innerhalb derselben Aktivität angezeigt wird.

1. Klicken [&#x200B; beim Erstellen oder Bearbeiten einer AP](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity)Aktivität auf das Symbol **[!UICONTROL Konfigurieren]** ( ![Symbol „Konfigurieren](/help/main/assets/icons/Setting.svg) ).

1. Klicken Sie **[!UICONTROL Duplizierte Angebote zulassen]**, um diese Funktion je nach Bedarf zu aktivieren oder zu deaktivieren.

   ![Symbol „Konfigurieren“](../assets/exclusion-1.png)

## Ausschließen spezifischer Erlebnisse {#exclude-experiences}

<a id="task_C17D36EF58AF4908B17A3D84CA6DE85A"></a>

Schließen Sie bestimmte Erlebnisse aus, um bestimmte Angebotskombinationen aus Ihrer API-Aktivität zu entfernen. Einige Kombinationen funktionieren möglicherweise nicht zusammen oder die Anzahl der getesteten Erlebnisse kann begrenzt werden, um die Traffic-Anforderungen der Aktivität zu senken.

1. Klicken [&#x200B; beim Erstellen oder Bearbeiten einer AP](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity)Aktivität auf das Symbol **[!UICONTROL Inhalt verwalten]** ( ![Symbol Inhalt verwalten](/help/main/assets/icons/Experience.svg) ).

   Die Liste **[!UICONTROL Erlebnisse]** zeigt jedes Erlebnis an, das anhand der Permutationen sämtlicher Inhalts- und Positionsoptionen generiert wurde.

1. Schließen Sie die Erlebnisse aus, die Sie nicht testen möchten.

   * Um ein einzelnes Erlebnis auszuschließen, klicken Sie auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmall.svg) ) und dann auf **[!UICONTROL Ausschließen]**.
   * Um mehrere Erlebnisse gleichzeitig auszuschließen, aktivieren Sie das Kontrollkästchen für jedes Erlebnis und klicken Sie dann auf **[!UICONTROL Ausschließen]**. Das Symbol **[!UICONTROL Ausschließen]** wird angezeigt, wenn ein oder mehrere Erlebnisse ausgewählt sind.

   ![Erlebnisse im Batch-Modus ausschließen](/help/main/c-activities/t-automated-personalization/assets/exclude1.png)

   Die Erlebnisse sind jetzt von der Aktivität ausgeschlossen und ihr **[!UICONTROL Status]** wird als **[!UICONTROL Ausgeschlossen]** angezeigt.

## Standardinhalt ausschließen {#exclude-default-content}

<a id="task_DCB4528989DF4C05A3A4729E5891D18F"></a>

Schließen Sie Standardinhalte aus, wenn sie nicht Teil Ihrer API-Aktivität sein sollen, sodass ein Speicherort nur ein Angebot enthält, das sich von Ihrem Standardinhalt unterscheidet. Mit diesem Ansatz können Sie auch das Erscheinungsbild der restlichen Seite ändern, sodass sie zu den getesteten Angeboten passt. Um beispielsweise die Farbpalette der Angebote abzustimmen, können Sie die Hintergrundfarbe der Seite ändern und die standardmäßige Hintergrundfarbe ausschließen.

1. Wählen [&#x200B; beim Erstellen oder Bearbeiten &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) AP-Aktivität den zu ersetzenden Inhalt aus und klicken Sie dann auf **[!UICONTROL Text/HTML ändern]**, **[!UICONTROL Bildangebot ändern]** oder **[!UICONTROL Hintergrundfarbe ändern]**. Die verfügbaren Optionen variieren je nach Inhaltstyp.

   ![Optionen ändern](../assets/exclusion-1.png)

1. Erstellen neuer Inhalte.

1. Klicken Sie auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/Setting.svg) ) und klicken Sie dann auf den **Standardangebot ausschließen/Standardangebot einschließen** , um das Standardangebot auszuschließen oder einzuschließen.

   <!--
   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![Include checkbox in Edit Text/HTML dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   For Image/Video content: 

   ![Include checkbox in Select Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   For background color: 

   ![Include checkbox in Edit Background Color dialog box](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)
   -->

<!--
1. Click **[!UICONTROL Save]**.

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_vec_4 image](assets/exclude_content_vec_4.png)

**To exclude default content using the [!UICONTROL Form-Based Experience Composer]:** 

1. While creating or editing an AP activity, click **[!UICONTROL Change Text/HTML]** or **[!UICONTROL Change Image Offer]** under **[!UICONTROL Content]**. 
1. In the dialog box, create your new content and uncheck **[!UICONTROL Include]** to the right of the default content (or uncheck the Default Image/Video in the [!UICONTROL Select Content] screen). 

   Depending on the content or offer type, the [!UICONTROL Include] checkbox is in a slightly different place. 

   For Text/HTML content: 

   ![exclude_content_form_1 image](assets/exclude_content_form_1.png)

   For Image/Video content: 

   ![exclude_content_form_2 image](assets/exclude_content_form_2.png)

1. Click **[!UICONTROL Save]**. 

   You can see the experiences created from the offers you specified under [!UICONTROL Manage Content]. You notice that no experiences are created in [!UICONTROL Manage Content] using the default offer you excluded. 

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)
-->
