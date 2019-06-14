---
description: Verwenden Sie den Visual Experience Composer, um eine Erlebnis-Targeting-Aktivität auf einer für Target aktivierten Seite zu erstellen und Teile der Seite in Target zu verändern.
seo-description: Verwenden Sie Visual Experience Composer, um eine Erlebnis-Targeting-Aktivität auf einer Target-fähigen Seite zu erstellen und Teile der Seite in Adobe Target zu ändern.
seo-title: Erstellen einer Erlebnis-Targeting-Aktivität
solution: Target
subtopic: Multivarianz-Test
title: Erstellen einer Erlebnis-Targeting-Aktivität
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
translation-type: tm+mt
source-git-commit: 5eb79fcd0407e0da841048bcd0a1b64393490fcf

---


# Erstellen einer Erlebnis-Targeting-Aktivität{#create-an-experience-targeting-activity}

Verwenden Sie Visual [!UICONTROL Experience Composer] (VEC), um eine [!UICONTROL Erlebnis-Targeting] (XT)-Aktivität auf einer Target-fähigen Seite zu erstellen und Teile der Seite zu [!DNL Adobe Target]ändern.

1. Klicken Sie in der Liste [!UICONTROL Aktivitäten] auf **[!UICONTROL Aktivität erstellen]** &gt; **[!UICONTROL Erlebnis-Targeting]**.

   ![Aktivität erstellen &gt; Erlebnis-Targeting](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem Target-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Die automatisierte Personalisierung ist beispielsweise eine [Target Premium-Funktion](/help/c-intro/intro.md#premium).

   Informationen zu den Aktivitätstypen finden Sie unter [Aktivitäten](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) und [Zielaktivitätstypen](/help/c-activities/target-activities-guide.md).

1. Wählen **[!UICONTROL Sie bei Bedarf &quot;Visuell (]** Standard)&quot; aus.

   ![Erlebnis-Targeting-Aktivität erstellen, Dialogfeld](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Wenn Sie den formularbasierten Experience Composer bevorzugen, wählen Sie diese Option aus. Weitere Informationen finden Sie unter [ Form-Based Experience Compose](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und Form-Based Experience Composer bietet Target die Einzelseitenanwendung VEC und VEC für mobile Apps an. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/c-experiences/experiences.md).

   Informationen zur Problembehebung für den VEC finden Sie bei Bedarf unter [Fehlerbehebung für den Visual Experience Composer](../../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4).

1. Geben Sie Ihre [Aktivitäts-URL an](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)und klicken Sie auf **[!UICONTROL Weiter]**.

   Wenn Ihr Konto mit einer Standard-URL konfiguriert wurde, dann wird diese URL standardmäßig angezeigt. Sie können von der Standard-URL zu einer anderen URL wechseln.

   Der Visual Experience Composer wird geöffnet und zeigt die Seite an, die in der URL angegeben ist.

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

1. Erstellen Sie neue Erlebnisse, indem Sie die Elemente auf der Seite ändern.

   Schrittweise Anweisungen finden Sie unter [Erlebnis hinzufügen](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

   Standardmäßig gestattet der Visual Experience Composer das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können JavaScript deaktivieren, wenn Sie diese Elemente mit dem Visual Experience Composer ändern möchten.

   Wenn Sie den Mauszeiger über die Elemente auf Ihrer Seite bewegen, werden diese Elemente hervorgehoben. Jedes hervorgehobene Element kann mithilfe des VEC geändert werden. Eine Liste der Aktionen, die für ein Element durchgeführt werden können, um das Erlebnis zu ändern, finden Sie unter [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   Wenn Sie mit Target Classic (früher Test&amp;Target) eine Mbox auf der Seite erstellt haben, wird diese Mbox als Element mit dem Mbox-Namen angezeigt und kann wie jedes andere Element bearbeitet werden.

1. Legen Sie [Ziele und Einstellungen](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für die Aktivität fest.
