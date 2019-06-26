---
description: Verwenden Sie den Visual Experience Composer, um eine Erlebnis-Targeting-Aktivität auf einer für Target aktivierten Seite zu erstellen und Teile der Seite in Target zu verändern.
seo-description: Verwenden Sie Visual Experience Composer, um eine Erlebnis-Targeting (XT)-Aktivität auf einer Target-fähigen Seite zu erstellen und Teile der Seite in Adobe Target zu ändern.
seo-title: Erstellen einer Erlebnis-Targeting-Aktivität
solution: Target
subtopic: Multivarianz-Test
title: Erstellen einer Erlebnis-Targeting-Aktivität
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Erstellen einer Erlebnis-Targeting-Aktivität{#create-an-experience-targeting-activity}

Use the [!UICONTROL Visual Experience Composer] (VEC) to create an [!UICONTROL Experience Targeting] (XT) activity on a Target-enabled page and to modify portions of the page within [!DNL Adobe Target].

Beim Erlebnis-Targeting (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus vermarkterdefinierten Regeln und Kriterien bereitgestellt.

Experience Targeting, including [geo-targeting](/help/c-target/c-audiences/c-target-rules/geo.md), is valuable for defining rules that target a specific experience or content to a particular audience. Es können mehrere Regeln für eine Aktivität bereitgestellt werden, um verschiedene Inhaltvarianten für verschiedene Zielgruppen bereitzustellen.

For more information about Experience Targeting, a use-case scenario, and training videos, see [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md).

**So erstellen Sie eine XT-Aktivität:**

1. Klicken Sie in der Liste [!UICONTROL Aktivitäten] auf **[!UICONTROL Aktivität erstellen]** &gt; **[!UICONTROL Erlebnis-Targeting]**.

   ![Aktivität erstellen &gt; Erlebnis-Targeting](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem Target-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. For example, [!UICONTROL Automated Personalization] is a [Target Premium feature](/help/c-intro/intro.md#premium).
   >
   >For more information about the various activity types available in [!DNL Target] and their differences, see [Activities](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). See [Target Activity types](/help/c-activities/target-activities-guide.md) to help you decide which activity type best suites your needs.

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   ![Erlebnis-Targeting-Aktivität erstellen, Dialogfeld](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Wenn Sie den formularbasierten Experience Composer bevorzugen, wählen Sie [!UICONTROL Formular aus]. See [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >Zusätzlich zum VEC und Form-Based Experience Composer bietet Target die Einzelseitenanwendung VEC und VEC für mobile Apps an. For more information about the various composers, see [Experiences and Offers](/help/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie bei Bedarf unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >The [!UICONTROL Choose Workplace] option in the preceding illustration is a [Target Premium](/help/c-intro/intro.md) feature. Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.]

1. (Conditional) If you are a Target Premium customer, [choose a workspace](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specify your [activity URL](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), then click **[!UICONTROL Next]**.

   If your account is [configured with a default URL](/help/administrating-target/r-target-account-preferences/target-account-preferences.md), that URL appears by default. Sie können bei Bedarf vom Standardwert zu einer anderen URL wechseln.

   Das VEC wird geöffnet und zeigt die in der URL angegebene Seite an.

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

1. Erstellen Sie neue Erlebnisse, die auf unterschiedliche Zielgruppen ausgerichtet sind.

   For step-by-step instructions, see [Add experience](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Legen Sie [Ziele und Einstellungen](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für die Aktivität fest.