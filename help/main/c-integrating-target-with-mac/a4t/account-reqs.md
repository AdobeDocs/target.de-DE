---
keywords: Analytics als Berichtsquelle;a4t;A4T;Anforderungen
description: Erfahren Sie, wie Sie die erforderlichen Benutzerkontenanforderungen konfigurieren, um eine Adobe Analytics-basierte Aktivität in Adobe zu erstellen [!DNL Target]  indem Sie Analytics für  [!DNL Target] A4T) verwenden.
title: Welche Benutzerberechtigungen sind für A4T erforderlich?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
TQID: https://experienceleague.adobe.com/SGNIoARqe3yN4WvKF4JPIp0t0JCMiSgj--zrjt-ZXJQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 32%

---

# Anforderungen hinsichtlich Benutzerberechtigungen

Informationen zu den Benutzerkontoanforderungen, um eine [!DNL Adobe Analytics]-basierte Aktivität in [!DNL Adobe Target] (A4T) zu erstellen.

Zur Auswahl einer Report Suite bei der Definition einer [!DNL Analytics]-Aktivität brauchen Sie sowohl ein [!DNL Analytics]-Benutzerkonto als auch ein [!DNL Target]-Benutzerkonto.

Ihre Benutzerkonten müssen wie in den folgenden Abschnitten beschrieben konfiguriert werden:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Führen Sie die folgenden Aufgaben in der [!DNL Adobe Experience Cloud] [Admin Console &#x200B;](https://adminconsole.adobe.com):

### Lösungskonten mit der Adobe ID verknüpfen

Ihre [!DNL Analytics]- und [!DNL Target]-Benutzerkonten müssen mit Ihrer Adobe ID verknüpft sein.

Weitere Informationen finden Sie unter [&#x200B; und Kontoverknüpfung](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).

### Zugehörigkeit zu einer Experience Cloud-Gruppe

Sie müssen Mitglied in mindestens einer [!DNL Experience Cloud]-Gruppe sein, die Zugriff auf [!DNL Analytics] und [!DNL Target] hat.

Weitere Informationen finden Sie unter [Verwalten von Experience Cloud-Benutzern und -Produkten](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Um A4T in einer bestimmten Report Suite verwenden zu können, müssen Sie Zugriff auf diese Report Suite haben und Zugriff auf die [!DNL Web Services Access] gewähren.

1. Klicken Sie **[!UICONTROL Admin Console]** auf ein [!DNL Analytics] Produktprofil und dann auf die Registerkarte **[!UICONTROL Permissions]** .

   Anschließend können Sie sehen, auf welche Report Suites das Profil Zugriff hat.

1. Stellen Sie sicher, dass die Report Suite, auf die Sie in [!DNL Target] Zugriff haben möchten, zu den Report Suites gehört, die in dem Produktprofil aufgeführt sind, dem Sie angehören.

   Die folgende Abbildung zeigt ein Beispiel für ein Produktprofil, das Zugriff auf alle Report Suites hat:

   ![Registerkarte &quot;Admin Console-Berechtigung“](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Konfigurieren Sie den Zugriff auf die [!UICONTROL Web Services Access].

   Der Zugriff auf die [!UICONTROL Web Services Access] in [!DNL Analytics] ist erforderlich, um [!DNL Analytics] als Berichtsquelle für [!DNL Target] verwenden zu können.


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Es sind keine zusätzlichen Berechtigungen erforderlich.
