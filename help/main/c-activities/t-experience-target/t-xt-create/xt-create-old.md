---
keywords: Erlebnis-Targeting;XT;erstellen
description: Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) in verwenden [!DNL Adobe Target]  um eine Aktivität vom Typ [!UICONTROL Experience Targeting] (XT) zu erstellen.
title: Wie erstelle ich eine [!UICONTROL Erlebnis-Targeting]-Aktivität?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 35%

---

# Erstellen einer [!UICONTROL Experience Targeting]-Aktivität (XT)

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC), um eine [!UICONTROL Experience Targeting]-Aktivität (XT) auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Adobe Target] zu ändern.

Beim [!UICONTROL Experience Targeting] (XT) werden Inhalte für eine bestimmte Zielgruppe basierend auf einem Satz aus Regeln und Kriterien, die von den Werbungtreibenden definiert werden, bereitgestellt.

[!UICONTROL Erlebnis-], einschließlich [Geo-Targeting](/help/main/c-target/c-audiences/c-target-rules/geo.md), ermöglicht die Definition von Regeln für Erlebnisse oder Inhalte, die auf eine bestimmte Zielgruppe ausgerichtet sind. Für eine Aktivität können mehrere Regeln definiert werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen.

Weitere Informationen zu [!UICONTROL Erlebnis-Targeting] einem Anwendungsfall und Schulungsvideos finden Sie unter [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md).

**So erstellen Sie eine [!UICONTROL Experience Targeting]-Aktivität:**

1. Klicken Sie in der [!UICONTROL Aktivitäten] auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Experience Targeting]**.

   ![Aktivität erstellen > Erlebnis-Targeting](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist [!UICONTROL Automated Personalization] eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium).
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. Wählen Sie **[!UICONTROL Visual (Standard)]**, falls erforderlich.

   Wenn Sie den [formularbasierten Experience Composer) bevorzugen](/help/main/c-experiences/form-experience-composer.md) wählen Sie [!UICONTROL Formular].

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den Single Page Application VEC. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung bei VEC finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie [!DNL Target Premium] sind, wählen Sie [einen Arbeitsbereich aus](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Die Option [!UICONTROL Arbeitsplatz auswählen] ist eine [Target Premium](/help/main/c-intro/intro.md)-Funktion. Wenn Ihr Unternehmen über eine [!DNL Target Standard]-Lizenz verfügt, diese Option jedoch nicht angezeigt wird.

1. Geben Sie Ihre [Aktivitäts-URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90) an und klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standard-URL zu einer anderen URL wechseln.

   Der VEC wird geöffnet und zeigt die Seite an, auf die die URL verweist.

   ![Erlebnis-Targeting-Aktivität im VEC](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Geben Sie an der verfügbaren Stelle einen Namen für die Aktivität ein.

   ![Namensfeld](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   Der Aktivitätsname darf nicht mit einem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

   Der Aktivitätsname darf keine der folgenden Zeichenfolgen enthalten:

   | Zeichenfolge | Beschreibung |
   |--- |--- |
   | ;= | Semikolon, Gleich |
   | ;+ | Semikolon plus |
   | ;- | Semikolon, Minus |
   | ;@ | Semikolon, at-Zeichen |
   | ,= | Komma, gleich |
   | ,+ | Komma, plus |
   | ,- | Komma, Minus |
   | ,@ | Komma, at-Zeichen |
   | `[`&quot; | Offene eckige Klammer, doppelte Anführungszeichen |
   | &quot;`]` | Doppelte Anführungszeichen, eckige Klammer schließen |

1. Erstellen Sie neue Erlebnisse für unterschiedliche Zielgruppen.

   Schrittweise Anweisungen finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für die Aktivität fest.
