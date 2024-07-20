---
keywords: Erlebnis-Targeting;XT;erstellen
description: Erfahren Sie, wie Sie mit dem VEC (0) in  [!DNL Adobe Target]  eine [!UICONTROL Experience Targeting] -Aktivität (XT) erstellen.[!UICONTROL Visual Experience Composer]
title: Wie erstelle ich eine [!UICONTROL Experience Targeting] -Aktivität?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 4faafcef38d02674072d8b20ae03d3e2ef2115d6
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 38%

---

# Erstellen einer [!UICONTROL Experience Targeting] -Aktivität (XT)

Verwenden Sie den VEC (0}), um eine [!UICONTROL Experience Targeting] -Aktivität (XT) auf einer für [!DNL Target] aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Adobe Target] zu verändern.[!UICONTROL Visual Experience Composer]

[!UICONTROL Experience Targeting] (XT) stellt Inhalte für eine bestimmte Zielgruppe basierend auf einem Satz von durch Marketingexperten definierten Regeln und Kriterien bereit.

[!UICONTROL Experience Targeting], einschließlich [Geotargeting](/help/main/c-target/c-audiences/c-target-rules/geo.md), ist nützlich zum Definieren von Regeln, die ein bestimmtes Erlebnis oder einen bestimmten Inhalt auf eine bestimmte Zielgruppe ausrichten. Für eine Aktivität können mehrere Regeln definiert werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen.

Weitere Informationen zu [!UICONTROL Experience Targeting], einem Anwendungsfall-Szenario und Schulungsvideos finden Sie unter [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md).

**So erstellen Sie eine [!UICONTROL Experience Targeting] -Aktivität:**

1. Klicken Sie in der Liste [!UICONTROL Activities] auf **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   ![Aktivität erstellen > Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispiel: [!UICONTROL Automated Personalization] ist eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium).
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Default)]** aus.

   Wenn Sie den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) bevorzugen, wählen Sie [!UICONTROL Form] aus.

   >[!NOTE]
   >
   >Zusätzlich zu VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den VEC für Einzelseiten-Apps. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung für VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie ein [!DNL Target Premium] -Kunde sind, wählen Sie [einen Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) aus.

   Die [!UICONTROL Choose Workplace] -Option ist eine [Target Premium](/help/main/c-intro/intro.md) -Funktion. Wenn Ihre Organisation über eine [!DNL Target Standard] -Lizenz verfügt, wird diese Option nicht angezeigt.

1. Geben Sie Ihre [Aktivitäts-URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90) an und klicken Sie dann auf **[!UICONTROL Create]**.

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
