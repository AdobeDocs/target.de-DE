---
keywords: globale Mbox;Globale Mbox anpassen;at.js bearbeiten;at.js;at.js implementieren
description: Erfahren Sie, wie Sie eine globale Mbox für "at.js"auf der Seite "Administration-Implementierung"in Adobe Target anpassen.
title: Wie kann ich eine globale Mbox anpassen?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 50%

---


# Anpassen einer globalen mbox

Informationen zum Anpassen einer globalen Mbox für &quot;at.js&quot;.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.

1. Deaktivieren Sie **[!UICONTROL Seitenladung aktiviert (Globale Mbox automatisch erstellen)]** und fügen Sie dann den Namen der benutzerdefinierten globalen Mbox hinzu, die Sie zur Bereitstellung von Aktivitäten von [!DNL Target] verwenden möchten.

   Die globale Mbox wird auch für Klick-Tracking eingesetzt.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, wenn Sie fertig sind.

1. Implementieren Sie die [!DNL at.js]-Bibliothek auf Ihrer Site.

   Weitere Informationen finden Sie unter [Bereitstellung von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md).

1. Stimmen Sie die Umstellung mit Ihrer Veröffentlichung zeitlich ab.

   Sind Sie bereit dafür, dass [!DNL Target] künftig für alle Aktivitäten Ihre globale Mbox verwendet, können Sie mit diesem Schritt fortfahren.

   Aktualisieren Sie den Namen der globalen mbox, sodass er dem in Schritt 2 (siehe oben) verwendeten Namen entspricht.

   >[!IMPORTANT]
   >
   >Beim Speichern werden alle Aktivitäten in Ihrem Konto mit dieser Mbox synchronisiert. Befindet sich die Mbox nicht auf Ihrer Site, funktionieren Ihre Aktivitäten nicht mehr.

