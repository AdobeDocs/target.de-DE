---
keywords: globale Mbox;globale Mbox anpassen;at.js bearbeiten;at.js;at.js implementieren
description: Erfahren Sie, wie Sie eine globale Mbox für at.js auf der Seite Administration-Implementierung in Adobe Target anpassen.
title: Wie kann ich eine globale Mbox anpassen?
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: bc5fd0695121ff99838b3df2a59b36b3a89b2cac
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 18%

---

# Anpassen einer globalen Mbox

Informationen, die Sie beim Anpassen einer [!DNL Adobe Target] globalen Mbox für at.js unterstützen.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.

1. Deaktivieren Sie **[!UICONTROL Seitenladung aktiviert (globale Mbox automatisch erstellen)]** und fügen Sie dann den Namen der benutzerdefinierten globalen Mbox hinzu, die Sie verwenden möchten, um Aktivitäten von [!DNL Target] bereitzustellen.

   >[!IMPORTANT]
   >
   >Die Änderung wird automatisch gespeichert, wenn Sie eine andere globale Mbox auswählen.

   Die globale Mbox wird auch für Klick-Tracking eingesetzt.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Implementieren Sie die Bibliothek [!DNL at.js] auf Ihrer Site.

   Weitere Informationen finden Sie unter [Bereitstellen von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) .

1. Stimmen Sie die Umstellung mit Ihrer Veröffentlichung zeitlich ab.

   Wenn [!DNL Target] bereit ist, Ihre globale Mbox für alle zukünftigen Aktivitäten zu verwenden, können Sie mit diesem Schritt fortfahren.

   Aktualisieren Sie den Namen der globalen mbox, sodass er dem in Schritt 2 (siehe oben) verwendeten Namen entspricht.

   >[!IMPORTANT]
   >
   >Alle Aktivitäten in Ihrem Konto werden mit dieser Mbox synchronisiert. Stellen Sie sicher, dass die globale Mbox auf Ihrer Site vorhanden ist, damit die Aktivitäten weiterhin funktionieren. Achten Sie darauf, die betroffenen Aktivitäten zu bearbeiten und erneut zu speichern, die mit dem Visual Experience Composer (VEC) erstellt wurden, der mit dieser Mbox synchronisiert wird. Es ist nicht erforderlich, Aktivitäten, die im formularbasierten Experience Composer oder über API erstellt wurden, erneut zu speichern.

