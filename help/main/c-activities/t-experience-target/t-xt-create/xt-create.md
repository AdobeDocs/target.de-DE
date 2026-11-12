---
keywords: Erlebnis-Targeting;XT;erstellen
description: Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] verwenden, um eine Aktivität [!UICONTROL Experience Targeting] (XT) zu erstellen.
title: Wie erstelle ich eine [!UICONTROL Erlebnis-Targeting]-Aktivität?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
TQID: 'https://experienceleague.adobe.com/RKSF7zTO3lb4hs1VaJuTUR9v8AnOlCjHkp-whqBIcKo'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: b6f5758b-84f7-4943-8b05-1297a046943c
    internal-label: Experience target
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: af388cf398e03e4ec7b4c5c44b03f772eacedf51
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 32%
---
# Erstellen einer [!UICONTROL Experience Targeting]-Aktivität (XT) {#create-xt-activity}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine **[!UICONTROL Experience Targeting]**-Aktivität (XT) im **[!UICONTROL Visual Experience Composer]** (VEC) erstellen. Sie erstellen die Aktivität, fügen Erlebnisse für verschiedene Zielgruppen hinzu und konfigurieren dann Ziele und Einstellungen.

>[!ENDSHADEBOX]

Verwenden Sie den **[!UICONTROL Visual Experience Composer]** (VEC), um eine **[!UICONTROL Experience Targeting]**-Aktivität (XT) auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Adobe Target] zu ändern.

Beim **[!UICONTROL Experience Targeting]** (XT) werden Inhalte für eine bestimmte Zielgruppe basierend auf einem Satz aus Regeln und Kriterien, die von den Werbungtreibenden definiert werden, bereitgestellt. Dies ist nützlich für die Definition von Regeln, die auf ein bestimmtes Erlebnis oder bestimmte Inhalte für eine bestimmte Zielgruppe, einschließlich [Geo-Targeting](/help/main/c-target/c-audiences/c-target-rules/geo.md), abzielen. Für eine Aktivität können mehrere Regeln definiert werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen.

Weitere Informationen zu **[!UICONTROL Erlebnis-Targeting]** einem Anwendungsfall und Schulungsvideos finden Sie unter [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md).

1. Klicken Sie in der **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Experience Targeting]**.

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist **[!UICONTROL Automated Personalization]** eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium).
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

   ![](../../assets/create-xt-1.png)

1. Wählen Sie im **[!UICONTROL Experience Targeting]** Aktivität erstellen Ihren Experience Composer:

   * **[!UICONTROL Visual]**.
   * **[!UICONTROL Form-Based Experience Composer]** finden Sie unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) für weitere Informationen.

   >[!NOTE]
   >
   >Zusätzlich zum VEC und **[!UICONTROL Form-Based Experience Composer]** bietet [!DNL Target] den Single Page Application VEC. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung bei VEC finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie [!DNL Target Premium] sind, wählen Sie [einen Arbeitsbereich aus](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geben Sie Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#ab-activity-url) an und klicken Sie dann auf **[!UICONTROL Erstellen]**. Der VEC wird geöffnet und zeigt die Seite an, auf die die URL verweist.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standard-URL zu einer anderen URL wechseln.

1. Um die Aktivität zu benennen, klicken Sie auf das Symbol **[!UICONTROL Bearbeiten]** ( ![Bearbeiten-Symbol](/help/main/assets/icons/Edit.svg) ), geben Sie einen beschreibenden Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

   {{activity-name-rules}}

   ![](../../assets/create-xt-2.png)

1. Erstellen Sie neue Erlebnisse für unterschiedliche Zielgruppen. Schrittweise Anweisungen finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md#xt-add-experience).

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#ab-goals-and-settings) für die Aktivität fest.
