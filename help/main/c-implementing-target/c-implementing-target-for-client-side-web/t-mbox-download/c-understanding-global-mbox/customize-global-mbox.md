---
keywords: globale Mbox;globale Mbox anpassen;at.js bearbeiten;at.js;at.js implementieren
description: Erfahren Sie, wie Sie eine globale Mbox für at.js auf der Seite Administration-Implementierung in Adobe Target anpassen.
title: Wie kann ich eine globale Mbox anpassen?
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 16%

---

# Anpassen einer globalen Mbox

Informationen, die Sie bei der Anpassung eines [!DNL Adobe Target] globale Mbox für at.js.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.

1. Deaktivieren **[!UICONTROL Seitenladung aktiviert (globale Mbox automatisch erstellen)]** und fügen Sie dann den Namen der benutzerdefinierten globalen Mbox hinzu, die Sie verwenden möchten, um Aktivitäten aus bereitzustellen. [!DNL Target].

   >[!IMPORTANT]
   >
   >Die Änderung wird automatisch gespeichert, wenn Sie eine andere globale Mbox auswählen.

   Die globale Mbox wird auch für Klick-Tracking eingesetzt.

   ![custom-global-mbox](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Implementieren des [!DNL at.js] -Bibliothek auf Ihrer Site.

   Siehe [Implementieren von &quot;at.js&quot;](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/how-to-deployatjs/){target=_blank} für weitere Informationen.

1. Stimmen Sie die Umstellung mit Ihrer Veröffentlichung zeitlich ab.

   Wenn Sie bereit sind für [!DNL Target] um in Zukunft Ihre globale Mbox für alle Aktivitäten zu verwenden, können Sie mit diesem Schritt fortfahren.

   Aktualisieren Sie den Namen der globalen mbox, sodass er dem in Schritt 2 (siehe oben) verwendeten Namen entspricht.

   >[!IMPORTANT]
   >
   >Alle Aktivitäten in Ihrem Konto werden mit dieser Mbox synchronisiert. Stellen Sie sicher, dass die globale Mbox auf Ihrer Site vorhanden ist, damit die Aktivitäten weiterhin funktionieren. Achten Sie darauf, die betroffenen Aktivitäten zu bearbeiten und erneut zu speichern, die mit dem Visual Experience Composer (VEC) erstellt wurden, der mit dieser Mbox synchronisiert wird. Es ist nicht erforderlich, Aktivitäten, die im formularbasierten Experience Composer oder über API erstellt wurden, erneut zu speichern.

