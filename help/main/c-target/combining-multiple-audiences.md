---
keywords: Zielgruppe; Zielgruppenregeln; Kombinieren von Zielgruppen; Ausschluss; Ausschluss hinzufügen; Ausschließen; Kombinieren von Zielgruppen; Ad-hoc-Zielgruppe; Adhoc-Zielgruppe
description: Erfahren Sie, wie Sie mehrere Zielgruppen (einschließlich Adobe Experience Cloud-Zielgruppen und  [!DNL Target] -Zielgruppen) dynamisch kombinieren können, um Ad-hoc-Zielgruppen zu erstellen.
title: Kann ich mehrere Zielgruppen kombinieren, um eine neue Zielgruppe zu erstellen?
feature: Audiences
exl-id: 1d9bff9c-f63b-4e15-9809-71b046158b71
TQID: https://experienceleague.adobe.com/Y46Mlx-YgD1-N5U9tC4stYJeS0SfOpTJ87TAhTrSPQc
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 58%

---

# Kombinieren mehrerer Zielgruppen

Kombinieren Sie mehrere Zielgruppen (einschließlich [!DNL Adobe Experience Cloud], [!DNL Adobe Experience Platform] und [!DNL Target] Zielgruppen) spontan, um Ad-hoc-Zielgruppen zu erstellen. Sie können auch Ausschlussregeln erstellen und darüber Zielgruppen ausschließen.

>[!NOTE]
>
>Die [!DNL Adobe Experience Platform] steht allen Kundinnen und Kunden zur Verfügung, [!DNL Target] die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=en){target=_blank} verwenden. Zielgruppen, die im [!DNL Adobe Experience Platform] verfügbar sind, können unverändert verwendet oder mit bestehenden Zielgruppen kombiniert werden, wie in diesem Thema erläutert.
>
>Weitere Informationen finden Sie unter [Verwenden von Zielgruppen aus Adobe Experience Platform](/help/main/c-target/c-audiences/audiences.md#aep).

Nehmen wir einmal an, Sie hätten die Zielgruppen „Neue Besucher“ und „Chrome-Anwender“ erstellt. Im Falle einer bestimmten Aktivität möchten Sie diese beiden Zielgruppen möglicherweise miteinander kombinieren, um neue Besucher mit dem Browser Chrome anzusprechen. Anstatt eine neue Zielgruppe zu erstellen und sie in der [!UICONTROL Zielgruppenbibliothek] zu speichern, können Sie die beiden Zielgruppen im Zuge der Aktivitätserstellung oder bei der Bearbeitung einer bereits bestehenden Aktivität miteinander kombinieren.

Ein weiteres Beispiel: Sie können alle Kundinnen und Kunden ansprechen, die am Kundenbindungsprogramm teilnehmen. Sie können beispielsweise eine bestimmte [!DNL Audience Manager] Zielgruppe für den Treuestatus einbeziehen und sie mit einer [!DNL Target] Zielgruppe kombinieren, die sich aus Personen zusammensetzt, die sich während der aktuellen Sitzung für Ihr Treueprogramm angemeldet haben. Die Kombination dieser beiden Zielgruppen ist einfacher als die Erstellung einer dritten, permanenten Zielgruppe.

Sie können mithilfe der AND- und OR-Operatoren bis zu 20 Zielgruppen kombinieren.

Sie können kombinierte Zielgruppen an verschiedenen Stellen der [!DNL Target]-Oberfläche verwenden.

## Kombinierte Zielgruppe beim Erstellen einer Aktivität erstellen {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

Sie können auf der [!UICONTROL Target]-Seite der Aktivität eine kombinierte Ad-hoc-Zielgruppe erstellen, während Sie durch den dreistufigen Prozess geleitet werden.

1. Klicken Sie beim Erstellen [Aktivität](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Targeting]** auf die drei vertikalen Ellipsen und dann auf **[!UICONTROL Zielgruppe ersetzen]**.

   ![Schrittergebnis](assets/edit_audience.png)

1. Aktivieren Sie auf der Seite **[!UICONTROL Zielgruppe auswählen]** diejenigen Kontrollkästchen neben den gewünschten Zielgruppen, die als Teil der kombinierten Zielgruppe dienen sollen.

   Schränken Sie [!UICONTROL  Suche ] die gewünschte Zielgruppe ein.

   ![Schrittergebnis](assets/combine_multiple_audiences1.png)

1. Klicken **[!UICONTROL oben]** auf „Mehrere Zielgruppen kombinieren“.

   ![Schrittergebnis](assets/combine_multiple_audiences2.png)

1. (Bedingt) Bearbeiten Sie die neue kombinierte Zielgruppe nach Wunsch.

   Im Dialogfeld [!UICONTROL Zielgruppe bearbeiten] können Sie weitere Bausteine für Zielgruppen von links in die neue kombinierte Zielgruppe ziehen. Sie können auch Ausschlussregeln hinzufügen und Zielgruppen ausschließen.

   1. Verwenden Sie die Drag-and-Drop-Funktion zum Hinzufügen von Audiences innerhalb eines vorhandenen Abschnitts als Baustein der Ebene 2.

      Nehmen wir beispielsweise an, dass Sie im vorhin beschriebenen Szenario auch Safari-Anwender in die kombinierte Zielgruppe aufnehmen möchten. Suchen Sie nach der Zielgruppe „Safari Browser“ und ziehen Sie sie in das Feld „Firefox Browser“ rechts, wie unten dargestellt:

      ![COMBINDE_MULTIPLE_AUDIENCES3 Bild](assets/combine_multiple_audiences3.png)

      In diesem Fall lautet der Operator für die beiden Browsertypen „AND“. Wählen Sie die [!UICONTROL Und]-Dropdown-Liste aus und ändern Sie sie in „Oder“, um eine neue kombinierte Zielgruppe für neue Besucher zu erstellen, die entweder Firefox oder Safari verwenden. Achten Sie darauf, dass Ihre Regeln nicht alle Mitglieder der Zielgruppe ausschließen. So ist es beispielsweise nicht möglich, dass ein Besucher eine Seite mit Safari und gleichzeitig mit Firefox besucht.

      >[!NOTE]
      >
      >Der Operator (AND oder OR) muss beim Kombinieren von Zielgruppen gleich bleiben. Sie können Operatoren nicht mischen und passend machen.

   1. Um einen Ausschluss zu einer Regel hinzuzufügen, klicken Sie auf &quot;**[!UICONTROL &quot;]**.

      ![COMBINDE_MULTIPLE_AUDIENCES3A Bild](assets/combine_multiple_audiences3a.png)

      Zielgruppe per Drag-and-Drop ablegen.

      Um beispielsweise Besucher aus den USA von neuen Besuchern auszuschließen, könnten Sie die Zielgruppe Markt: Vereinigte Staaten in die Box ziehen.

      Diese kombinierte Zielgruppe enthält alle neuen Besucher Ihrer Site (außer denen aus San Francisco), die Safari oder Firefox verwenden.

   1. Um eine Zielgruppe von einer Regel auszuschließen, klicken Sie auf **[!UICONTROL Ausnahme]** > **[!UICONTROL Diese Zielgruppe ausschließen]**.

      Sie können z. B. eine kombinierte Zielgruppe erstellen, die alle neuen Besucher Ihrer Site enthält, ausgenommen diejenigen, die Firefox verwenden. Das Ausschließen der Besucher, die Firefox verwenden, ist leichter, als das Erstellen einer kombinierten Zielgruppe, die explizit mehrere Browser, außer Firefox, einschließt (Safari, Chrome und Internet Explorer).

1. Geben Sie einen beschreibenden Namen für die kombinierte Zielgruppe ein und klicken Sie dann auf **[!UICONTROL Fertig]**.

## Kombinierte Zielgruppe zur Verwendung beim Metrik-Targeting erstellen {#section_A42E795AFCBD4575809C5942039910F0}

Sie können eine kombinierte Ad-hoc-Zielgruppe, die Sie im Metrik-Targeting verwenden möchten, auf der Seite [!UICONTROL Ziele und Einstellungen] der Aktivität erstellen. So erstellen Sie beispielsweise ein Targeting basierend auf Konversionen mithilfe einer kombinierten Zielgruppe:

1. Wählen Sie beim Bearbeiten oder Erstellen [Aktivität](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Ziele und Einstellungen]** für die Erfolgsmetrik **[!UICONTROL Konversion]** aus und wählen Sie dann **[!UICONTROL Eine Mbox anzeigen]** als Aktion aus.
1. Wählen Sie die gewünschte Mbox aus dem Feld **[!UICONTROL Mbox suchen]** aus.

   ![COMBINDE_MULTIPLE_AUDIENCES4 Bild](assets/combine_multiple_audiences4.png)

1. Klicken Sie auf das Zahnradsymbol und anschließend auf **[!UICONTROL Zielgruppen-Targeting hinzufügen]**.
1. Klicken Sie auf den Link **[!UICONTROL Zielgruppe/Targetingbedingung hinzufügen]**, um das Dialogfeld [!UICONTROL Zielgruppe wählen] zu öffnen.

   ![COMBINDE_MULTIPLE_AUDIENCES5 Bild](assets/combine_multiple_audiences5.png)

1. Fahren Sie mit [Schritt 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) unter „Erstellen einer kombinierten Zielgruppe bei Erstellung einer Aktivität“ fort, um die kombinierte Zielgruppe zu erstellen.

## Kombinierte Zielgruppe zur Verwendung in Berichten erstellen {#section_4682D342EFBB43C38E54B99B3A1E14CD}

Sie können eine kombinierte Ad-hoc-Zielgruppe auch auf der Seite [!UICONTROL Ziele und Einstellungen] der Aktivität erstellen, um sie für Berichterstellungen zu nutzen.

1. Klicken Sie beim Bearbeiten oder Erstellen [Aktivität](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) auf der Seite **[!UICONTROL Ziele und Einstellungen]** auf das Symbol **[!UICONTROL Zielgruppe hinzufügen]** unter [!UICONTROL Zielgruppen für die Berichterstellung], um die Seite [!UICONTROL Zielgruppe auswählen] anzuzeigen.

   ![COMBINDE_MULTIPLE_AUDIENCES6 Bild](assets/combine_multiple_audiences6.png)

1. Fahren Sie mit [Schritt 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) unter „Erstellen einer kombinierten Zielgruppe bei Erstellung einer Aktivität“ fort, um die kombinierte Zielgruppe zu erstellen.

## Kombinierte Zielgruppe beim Bearbeiten einer Aktivität erstellen {#section_364A12CE96E04B61B7C18113AA586C2C}

Sie können eine kombinierte Ad-hoc-Zielgruppe erstellen, während Sie eine bestehende Aktivität bearbeiten.

1. Fahren Sie auf der Seite [!UICONTROL Aktivitäten] mit dem Mauszeiger über die gewünschte Aktivität und klicken Sie anschließend auf das **[!UICONTROL Bearbeitungssymbol]**.

   Oder

   Klicken Sie auf die gewünschte Aktivität, um sie zu öffnen, und klicken Sie anschließend auf **[!UICONTROL Aktivität bearbeiten]**.

1. Klicken Sie auf **[!UICONTROL Konfigurieren]** > **[!UICONTROL Zielgruppen]** > **[!UICONTROL Mehrere Zielgruppen]**.

   ![Konfigurieren > Zielgruppen > Mehrere Zielgruppen](assets/combine_multiple_audiences7.png)

1. Klicken Sie auf das Symbol für weitere Optionen (drei vertikale Ellipsen) neben der aktuellen Zielgruppe der Aktivität und anschließend auf **[!UICONTROL Zielgruppe ändern]**.

   ![Zielgruppe ändern](assets/combine_multiple_audiences8.png)

1. Fahren Sie mit [Schritt 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) unter „Erstellen einer kombinierten Zielgruppe bei Erstellung einer Aktivität“ fort, um die kombinierte Zielgruppe zu erstellen.
