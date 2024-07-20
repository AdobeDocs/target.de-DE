---
keywords: Zielgruppe; Zielgruppenregeln; Kombinieren von Zielgruppen; Ausschluss; Ausschluss hinzufügen; Ausschließen; Kombinieren von Zielgruppen; Ad-hoc-Zielgruppe; Adhoc-Zielgruppe
description: Erfahren Sie, wie Sie ohne Zwischenschritte mehrere Zielgruppen (einschließlich Adobe Experience Cloud-Zielgruppen und [!DNL Target] Zielgruppen) kombinieren, um Ad-hoc-Zielgruppen zu erstellen.
title: Kann ich mehrere Zielgruppen kombinieren, um eine neue Zielgruppe zu erstellen?
feature: Audiences
exl-id: 1d9bff9c-f63b-4e15-9809-71b046158b71
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 38%

---

# Kombinieren mehrerer Zielgruppen

Kombinieren mehrerer Zielgruppen (einschließlich [!DNL Adobe Experience Cloud], [!DNL Adobe Experience Platform] und [!DNL Target] Zielgruppen) ohne Zwischenschritte zur Erstellung von Ad-hoc-Zielgruppen. Sie können auch Ausschlussregeln erstellen und darüber Zielgruppen ausschließen.

>[!NOTE]
>
>Die Quelle &quot;[!DNL Adobe Experience Platform]&quot; steht allen [!DNL Target] -Kunden zur Verfügung, die das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=en){target=_blank} verwenden. In der Datei &quot;[!DNL Adobe Experience Platform]&quot;verfügbare Zielgruppen können unverändert verwendet oder mit vorhandenen Zielgruppen kombiniert werden, wie in diesem Thema beschrieben.
>
>Weitere Informationen finden Sie unter [Verwenden von Zielgruppen aus Adobe Experience Platform](/help/main/c-target/c-audiences/audiences.md#aep).

Nehmen wir einmal an, Sie hätten die Zielgruppen „Neue Besucher“ und „Chrome-Anwender“ erstellt. Im Falle einer bestimmten Aktivität möchten Sie diese beiden Zielgruppen möglicherweise miteinander kombinieren, um neue Besucher mit dem Browser Chrome anzusprechen. Anstatt eine dritte Zielgruppe zu erstellen und in der [!UICONTROL Audiences] -Bibliothek zu speichern, können Sie diese beiden Zielgruppen bei der Erstellung einer Aktivität oder während der Bearbeitung einer vorhandenen Aktivität kombinieren.

Als weiteres Beispiel können Sie alle Treuekunden ansprechen. Sie können beispielsweise eine bestimmte [!DNL Audience Manager] Zielgruppe für den Treuestatus hinzufügen und sie mit einer [!DNL Target] -Zielgruppe kombinieren, die aus Personen besteht, die sich während der aktuellen Sitzung für Ihr Treueprogramm angemeldet haben. Die Kombination dieser beiden Zielgruppen ist einfacher als die Erstellung einer dritten, permanenten Zielgruppe.

Mithilfe der Operatoren AND und OR können Sie bis zu 20 Zielgruppen kombinieren.

Sie können kombinierte Zielgruppen an verschiedenen Stellen der [!DNL Target]-Oberfläche verwenden.

## Erstellen einer kombinierten Zielgruppe bei Erstellung einer Aktivität {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

Sie können eine kombinierte Ad-hoc-Zielgruppe während des dreistufigen geführten Workflows auf der Seite &quot;[!UICONTROL Target]&quot; der Aktivität erstellen.

1. Klicken Sie beim Erstellen einer [Aktivität](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Targeting]** auf die drei vertikalen Ellipsen und dann auf **[!UICONTROL Replace Audience]**.

   ![Schrittergebnis](assets/edit_audience.png)

1. Aktivieren Sie auf der Seite **[!UICONTROL Choose Audience]** die Kontrollkästchen neben den gewünschten Zielgruppen, die Sie als Bausteine für Ihre kombinierte Zielgruppe verwenden möchten.

   Verwenden Sie das Feld [!UICONTROL Search Audiences] , um die Suche auf die gewünschte Zielgruppe einzuschränken.

   ![Schrittergebnis](assets/combine_multiple_audiences1.png)

1. Klicken Sie oben rechts auf **[!UICONTROL Combine Multiple Audiences]** .

   ![Schrittergebnis](assets/combine_multiple_audiences2.png)

1. (Bedingt) Bearbeiten Sie die neue kombinierte Zielgruppe nach Wunsch.

   Im Dialogfeld [!UICONTROL Edit Audience] können Sie zusätzliche Bausteine für Zielgruppen von der linken Seite in die neue kombinierte Zielgruppe ziehen. Sie können auch Ausschlussregeln hinzufügen und Zielgruppen ausschließen.

   1. Verwenden Sie Drag &amp; Drop-Funktionen, um Zielgruppen in einem vorhandenen Bereich als Baustein der Stufe 2 hinzuzufügen.

      Nehmen wir beispielsweise an, dass Sie im vorhin beschriebenen Szenario auch Safari-Anwender in die kombinierte Zielgruppe aufnehmen möchten. Suchen Sie nach der Zielgruppe „Safari Browser“ und ziehen Sie sie in das Feld „Firefox Browser“ rechts, wie unten dargestellt:

      ![Bild_multiple_audiences3](assets/combine_multiple_audiences3.png)

      In diesem Fall lautet der Operator für die beiden Browsertypen „AND“. Wählen Sie die Dropdownliste [!UICONTROL And] aus und ändern Sie sie in &quot;ODER&quot;, um eine neue kombinierte Zielgruppe für neue Besucher zu erstellen, die entweder Firefox oder Safari verwenden. Achten Sie darauf, dass Ihre Regeln nicht alle Mitglieder der Zielgruppe ausschließen. So ist es beispielsweise nicht möglich, dass ein Besucher eine Seite mit Safari und gleichzeitig mit Firefox besucht.

      >[!NOTE]
      >
      >Der Operator (AND oder OR) muss beim Kombinieren von Zielgruppen gleich bleiben. Sie können Operatoren nicht mischen und passend machen.

   1. Um einer Regel einen Ausschluss hinzuzufügen, klicken Sie auf **[!UICONTROL Exclude]**.

      ![Combining_multiple_audiences3a image](assets/combine_multiple_audiences3a.png)

      Ziehen Sie eine Zielgruppe in den Arbeitsbereich.

      Um beispielsweise Besucher aus den USA aus neuen Besuchern auszuschließen, können Sie die Zielgruppe &quot;Markt: USA&quot;in das Feld ziehen.

      Diese kombinierte Zielgruppe enthält alle neuen Besucher Ihrer Site (außer denen aus San Francisco), die Safari oder Firefox verwenden.

   1. Um eine Zielgruppe aus einer Regel auszuschließen, klicken Sie auf **[!UICONTROL Exclusion]** > **[!UICONTROL Exclude this Audience.]**.

      Sie können z. B. eine kombinierte Zielgruppe erstellen, die alle neuen Besucher Ihrer Site enthält, ausgenommen diejenigen, die Firefox verwenden. Das Ausschließen der Besucher, die Firefox verwenden, ist leichter, als das Erstellen einer kombinierten Zielgruppe, die explizit mehrere Browser, außer Firefox, einschließt (Safari, Chrome und Internet Explorer).

1. Geben Sie einen beschreibenden Namen für die kombinierte Zielgruppe ein und klicken Sie dann auf **[!UICONTROL Done]**.

## Erstellen einer kombinierten Zielgruppe zur Verwendung im Metrik-Targeting {#section_A42E795AFCBD4575809C5942039910F0}

Sie können eine kombinierte Ad-hoc-Zielgruppe auf der Seite [!UICONTROL Goals & Settings] der Aktivität erstellen, um sie im Metrik-Targeting zu verwenden. So erstellen Sie beispielsweise ein Targeting basierend auf Konversionen mithilfe einer kombinierten Zielgruppe:

1. Wählen Sie beim Bearbeiten oder Erstellen einer [Aktivität](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Goals & Settings]** für die Erfolgsmetrik **[!UICONTROL Conversion]** und dann **[!UICONTROL Viewed an Mbox]** als Aktion aus.
1. Wählen Sie die gewünschte Mbox im Feld **[!UICONTROL Search mbox]** aus.

   ![Bild_multiple_audiences4](assets/combine_multiple_audiences4.png)

1. Klicken Sie auf das Zahnradsymbol und dann auf **[!UICONTROL Add Audience Targeting]**.
1. Klicken Sie auf den Link **[!UICONTROL Add Audience/Targeting Condition]** , um das Dialogfeld [!UICONTROL Choose Audience] anzuzeigen.

   ![kombinieren_multiple_audiences5-Bild](assets/combine_multiple_audiences5.png)

1. Fahren Sie mit [Schritt 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) unter „Erstellen einer kombinierten Zielgruppe bei Erstellung einer Aktivität“ fort, um die kombinierte Zielgruppe zu erstellen.

## Erstellen einer kombinierten Zielgruppe zur Verwendung in Berichten {#section_4682D342EFBB43C38E54B99B3A1E14CD}

Sie können eine kombinierte Ad-hoc-Zielgruppe auf der Seite &quot;[!UICONTROL Goals & Settings]&quot;der Aktivität erstellen, um sie in Berichten zu verwenden.

1. Klicken Sie beim Bearbeiten oder Erstellen einer [Aktivität](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Goals & Settings]** auf das Symbol **[!UICONTROL Add Audience]** unter [!UICONTROL Audiences for Reporting], um die Seite [!UICONTROL Choose Audience] anzuzeigen.

   ![Bild_multiple_audiences6](assets/combine_multiple_audiences6.png)

1. Fahren Sie mit [Schritt 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) unter „Erstellen einer kombinierten Zielgruppe bei Erstellung einer Aktivität“ fort, um die kombinierte Zielgruppe zu erstellen.

## Erstellen einer kombinierten Zielgruppe bei Bearbeitung einer Aktivität {#section_364A12CE96E04B61B7C18113AA586C2C}

Sie können eine kombinierte Ad-hoc-Zielgruppe erstellen, während Sie eine bestehende Aktivität bearbeiten.

1. Halten Sie auf der Seite [!UICONTROL Activities] den Mauszeiger über die gewünschte Aktivität und klicken Sie auf das Symbol **[!UICONTROL Edit]** .

   Oder

   Klicken Sie auf die gewünschte Aktivität, um sie zu öffnen, und klicken Sie dann auf **[!UICONTROL Edit Activity]**.

1. Klicken Sie auf **[!UICONTROL Configure]** > **[!UICONTROL Audiences]** > **[!UICONTROL Multiple Audiences]**.

   ![Konfigurieren > Zielgruppen > Mehrere Zielgruppen](assets/combine_multiple_audiences7.png)

1. Klicken Sie auf das Symbol für weitere Optionen (drei vertikale Ellipsen) neben der aktuellen Zielgruppe der Aktivität und dann auf **[!UICONTROL Change Audience]**.

   ![Zielgruppe ändern](assets/combine_multiple_audiences8.png)

1. Fahren Sie mit [Schritt 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) unter „Erstellen einer kombinierten Zielgruppe bei Erstellung einer Aktivität“ fort, um die kombinierte Zielgruppe zu erstellen.
