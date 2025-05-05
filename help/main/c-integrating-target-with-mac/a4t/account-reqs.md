---
keywords: Analytics als Berichtsquelle;a4t;A4T;Anforderungen
description: Erfahren Sie, wie Sie die erforderlichen Benutzerkontenanforderungen konfigurieren, um eine Adobe Analytics-basierte Aktivität in Adobe [!DNL Target] mit Analytics für  [!DNL Target] A4T) zu erstellen.
title: Welche Benutzerberechtigungen sind für A4T erforderlich?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 35%

---

# Anforderungen hinsichtlich Benutzerberechtigungen

Informationen zu den Benutzerkontoanforderungen, um eine [!DNL Adobe Analytics]-basierte Aktivität in [!DNL Adobe Target] (A4T) zu erstellen.

Zur Auswahl einer Report Suite bei der Definition einer [!DNL Analytics]-Aktivität brauchen Sie sowohl ein [!DNL Analytics]-Benutzerkonto als auch ein [!DNL Target]-Benutzerkonto.

Ihre Benutzerkonten müssen wie in den folgenden Abschnitten beschrieben konfiguriert werden:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Führen Sie die folgenden Aufgaben in der [!DNL Adobe Experience Cloud] [Admin Console ](https://adminconsole.adobe.com):

### Lösungskonten mit der Adobe ID verknüpfen

Ihre [!DNL Analytics]- und [!DNL Target]-Benutzerkonten müssen mit Ihrer Adobe ID verknüpft sein.

Weitere Informationen finden Sie unter [ und Kontoverknüpfung](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).

### Mitgliedschaft in einer Experience Cloud-Gruppe

Sie müssen Mitglied in mindestens einer [!DNL Experience Cloud]-Gruppe sein, die Zugriff auf [!DNL Analytics] und [!DNL Target] hat.

Weitere Informationen finden Sie unter [Verwalten von Experience Cloud-Benutzern und -Produkten](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Um A4T in einer bestimmten Report Suite verwenden zu können, müssen Sie Zugriff auf diese Report Suite haben und Zugriff auf die [!DNL Web Services Access] gewähren.

1. Klicken Sie **[!UICONTROL Admin Console]** auf ein [!DNL Analytics] Produktprofil und dann auf die Registerkarte **[!UICONTROL Permissions]** .

   Anschließend können Sie sehen, auf welche Report Suites das Profil Zugriff hat.

1. Stellen Sie sicher, dass die Report Suite, auf die Sie in [!DNL Target] Zugriff haben möchten, zu den Report Suites gehört, die in dem Produktprofil aufgeführt sind, dem Sie angehören.

   Die folgende Abbildung zeigt ein Beispiel für ein Produktprofil, das Zugriff auf alle Report Suites hat:

   Registerkarte für ![Admin Console-Berechtigungen](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Konfigurieren Sie den Zugriff auf die [!UICONTROL Web Services Access].

   Der Zugriff auf die [!UICONTROL Web Services Access] in [!DNL Analytics] ist erforderlich, um [!DNL Analytics] als Berichtsquelle für [!DNL Target] verwenden zu können.


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Es sind keine zusätzlichen Berechtigungen erforderlich.
