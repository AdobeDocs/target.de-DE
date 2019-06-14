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
source-git-commit: dcddbf8c1a4f406fdbfb00b9deaa75113aa7b624

---


# Erstellen einer Erlebnis-Targeting-Aktivität{#create-an-experience-targeting-activity}

Verwenden Sie Visual [!UICONTROL Experience Composer] (VEC), um eine [!UICONTROL Erlebnis-Targeting] (XT)-Aktivität auf einer Target-fähigen Seite zu erstellen und Teile der Seite zu [!DNL Adobe Target]ändern.

Beim Erlebnis-Targeting (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus vermarkterdefinierten Regeln und Kriterien bereitgestellt.

Erlebnis-Targeting, einschließlich [Geotargeting](/help/c-target/c-audiences/c-target-rules/geo.md), ist nützlich für die Definition von Regeln, die auf ein bestimmtes Erlebnis oder einen bestimmten Inhalt für eine bestimmte Zielgruppe abzielen. Es können mehrere Regeln für eine Aktivität bereitgestellt werden, um verschiedene Inhaltvarianten für verschiedene Zielgruppen bereitzustellen.

Weitere Informationen zu Erlebnis-Targeting, Anwendungsszenarios und Schulungsvideos finden Sie unter [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md).

**So erstellen Sie eine XT-Aktivität:**

1. Klicken Sie in der Liste [!UICONTROL Aktivitäten] auf **[!UICONTROL Aktivität erstellen]** &gt; **[!UICONTROL Erlebnis-Targeting]**.

   ![Aktivität erstellen &gt; Erlebnis-Targeting](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem Target-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Die [!UICONTROL automatisierte Personalisierung] ist beispielsweise eine [Target Premium-Funktion](/help/c-intro/intro.md#premium).
   >
   >Weitere Informationen zu den verschiedenen verfügbaren Aktivitätstypen [!DNL Target] und ihren Unterschieden finden Sie unter [Aktivitäten](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. Wählen **[!UICONTROL Sie bei Bedarf &quot;Visuell (]** Standard)&quot; aus.

   ![Erlebnis-Targeting-Aktivität erstellen, Dialogfeld](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Wenn Sie den formularbasierten Experience Composer bevorzugen, wählen Sie diese Option aus. Weitere Informationen finden Sie unter [ Form-Based Experience Compose](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und Form-Based Experience Composer bietet Target die Einzelseitenanwendung VEC und VEC für mobile Apps an. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie bei Bedarf unter [Fehlerbehebung für den Visual Experience Composer](../../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4).

1. Geben Sie Ihre [Aktivitäts-URL an](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)und klicken Sie auf **[!UICONTROL Weiter]**.

   Wenn Ihr Konto mit einer Standard-URL [](/help/administrating-target/r-target-account-preferences/target-account-preferences.md)konfiguriert ist, wird diese URL standardmäßig angezeigt. Sie können bei Bedarf vom Standardwert zu einer anderen URL wechseln.

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

   Schrittweise Anweisungen finden Sie unter [Erlebnis hinzufügen](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Legen Sie [Ziele und Einstellungen](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für die Aktivität fest.