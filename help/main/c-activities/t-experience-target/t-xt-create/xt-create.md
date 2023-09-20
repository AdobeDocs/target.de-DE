---
keywords: Erlebnis-Targeting;XT;erstellen
description: Erfahren Sie, wie Sie die [!UICONTROL Visual Experience Composer] (VEC) [!DNL Adobe Target] , um eine [!UICONTROL Erlebnis-Targeting] (XT).
title: Wie erstelle ich eine [!UICONTROL Erlebnis-Targeting] Aktivität?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 4faafcef38d02674072d8b20ae03d3e2ef2115d6
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 51%

---

# Erstellen Sie eine [!UICONTROL Erlebnis-Targeting] (XT)-Aktivität

Verwenden Sie die [!UICONTROL Visual Experience Composer] (VEC), um eine [!UICONTROL Erlebnis-Targeting] (XT) -Aktivität auf einer [!DNL Target]-aktivierte Seite verwenden und Teile der Seite in [!DNL Adobe Target].

Beim [!UICONTROL Experience Targeting] (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus Regeln und Kriterien, die von den Werbungtreibenden definiert werden, bereitgestellt.

Erlebnis-Targeting, einschließlich [Geotargeting](/help/main/c-target/c-audiences/c-target-rules/geo.md), ermöglicht die Definition von Regeln für Erlebnisse oder Inhalte, die auf eine bestimmte Zielgruppe ausgerichtet sind. Für eine Aktivität können mehrere Regeln definiert werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen.

Weitere Informationen finden Sie unter [!UICONTROL Erlebnis-Targeting], ein Anwendungsszenario und Schulungsvideos, siehe [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md).

**So erstellen Sie eine [!UICONTROL Erlebnis-Targeting] Aktivität:**

1. Klicken Sie in der Liste [!UICONTROL Aktivitäten] auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Erlebnis-Targeting]**.

   ![Aktivität erstellen > Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist die [!UICONTROL automatisierte Personalisierung] eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium).
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Standard)]** aus.

   Wenn Sie die [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md)auswählen [!UICONTROL Formular].

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer], [!DNL Target] bietet den VEC für Einzelseiten-Apps an. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung für VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie [!DNL Target Premium] Kunde, [Arbeitsbereich auswählen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Die [!UICONTROL Arbeitsplatz auswählen] -Option ist [Target Premium](/help/main/c-intro/intro.md) Funktion. Wenn Ihr Unternehmen über eine [!DNL Target Standard] -Lizenz, wenn diese Option nicht angezeigt wird.

1. Geben Sie Ihre [Aktivitäts-URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90) an und klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standard-URL zu einer anderen URL wechseln.

   Der VEC wird geöffnet und zeigt die Seite an, auf die die URL verweist.

   ![Erlebnis-Targeting-Aktivität im VEC](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Geben Sie an der verfügbaren Stelle einen Namen für die Aktivität ein.

   ![Namensfeld](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   Der Aktivitätsname darf mit keinem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

   Der Aktivitätsname darf keine der folgenden Zeichensequenzen enthalten:

   | Zeichensequenz | Beschreibung |
   |--- |--- |
   | ;= | Semikolon, Gleich |
   | ;+ | Semikolon, Plus |
   | ;- | Semikolon, Minus |
   | ;@ | Semikolon, At-Zeichen |
   | ,= | Komma, gleich |
   | ,+ | Komma, Plus |
   | ,- | Komma, Minus |
   | ,@ | Komma, At-Zeichen |
   | `[`&quot; | Offene eckige Klammer, doppelte Anführungszeichen |
   | &quot;`]` | Doppelte Anführungszeichen, eckige Klammer schließen |

1. Erstellen Sie neue Erlebnisse für unterschiedliche Zielgruppen.

   Schrittweise Anweisungen finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für die Aktivität fest.
