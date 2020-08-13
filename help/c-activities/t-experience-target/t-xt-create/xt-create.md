---
description: Verwendung des Visual Experience Composers, um eine Erlebnis-Targeting-Aktivität (XT) auf einer für Target aktivierten Seite zu erstellen und Teile der Seite in Adobe Target zu verändern.
title: Erstellen einer Erlebnis-Targeting-Aktivität
feature: xt
subtopic: Multivariate Test
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 100%

---


# Erstellen einer Erlebnis-Targeting-Aktivität{#create-an-experience-targeting-activity}

Verwenden des [!UICONTROL Visual Experience Composers] (VEC), um eine [!UICONTROL Erlebnis-Targeting]-Aktivität (XT) auf einer für [!DNL Adobe Target] aktivierten Seite zu erstellen und Teile der Seite in Target zu verändern.

Beim Erlebnis-Targeting (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus vermarkterdefinierten Regeln und Kriterien bereitgestellt.

Erlebnis-Targeting, einschließlich [Geotargeting](/help/c-target/c-audiences/c-target-rules/geo.md), ermöglicht die Definition von Regeln für Erlebnisse oder Inhalte, die auf eine bestimmte Zielgruppe ausgerichtet sind. Für eine Aktivität können mehrere Regeln definiert werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen.

Weitere Informationen zum Erlebnis-Targeting, einen Anwendungsfall und Schulungsvideos finden Sie unter [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md).

**So erstellen Sie eine XT-Aktivität:**

1. Klicken Sie in der Liste [!UICONTROL Aktivitäten] auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Erlebnis-Targeting]**.

   ![Aktivität erstellen > Erlebnis-Targeting](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem Target-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist die [!UICONTROL automatisierte Personalisierung] eine [Target Premium-Funktion](/help/c-intro/intro.md#premium).
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Standard)]** aus.

   ![Erstellen des Dialogfeldes „Erlebnis-Targeting-Aktivität“](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Wenn Sie den formularbasierten Experience Composer bevorzugen, wählen Sie [!UICONTROL Formular] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und zum formularbasierten Experience Composer bietet Target den VEC für Einzelseitenanwendungen und den VEC für Mobile Apps. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >Die Option [!UICONTROL „Arbeitsplatz auswählen“] in der obigen Abbildung ist eine Funktion von [Target Premium](/help/c-intro/intro.md). Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.]

1. (Abhängig von Ihrer Lizenz) Wenn Sie Target Premium-Kunde sind, [wählen Sie einen Arbeitsbereich](/help/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie Ihre [Aktivitäts-URL](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90) ein und klicken Sie dann auf **[!UICONTROL Weiter]**.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standard-URL zu einer anderen URL wechseln.

   Der VEC wird geöffnet und zeigt die Seite an, auf die die URL verweist.

   ![Erlebnis-Targeting-Aktivität im VEC](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Geben Sie an der verfügbaren Stelle einen Namen für die Aktivität ein.

   ![Namensfeld](/help/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   Folgende Zeichen sind im Aktivitätsnamen nicht zulässig:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `/` | Vorwärtsschrägstrich |
   | `?` | Fragezeichen |
   | `#` | Raute |
   | `:` | Doppelpunkt |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

1. Erstellen Sie neue Erlebnisse für unterschiedliche Zielgruppen.

   Schrittweise Anweisungen finden Sie unter [Erlebnis hinzufügen](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Legen Sie [Ziele und Einstellungen](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für die Aktivität fest.