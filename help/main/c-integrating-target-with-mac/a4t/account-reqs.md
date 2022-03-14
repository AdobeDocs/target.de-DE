---
keywords: Analytics als Berichtsquelle; a4t; A4T; Anforderungen
description: Erfahren Sie, wie Sie die Benutzerkontoanforderungen konfigurieren, die zum Erstellen einer Adobe Analytics-basierten Aktivität in Adobe erforderlich sind. [!DNL Target] Verwenden von Analytics für [!DNL Target] (A4T).
title: Welche Anforderungen an Benutzerberechtigungen sind für A4T erforderlich?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 34%

---

# Anforderungen hinsichtlich Benutzerberechtigungen

Informationen zu den Benutzerkontoanforderungen, um eine [!DNL Adobe Analytics]-basierte Aktivität in [!DNL Adobe Target] (A4T) zu erstellen.

Zur Auswahl einer Report Suite bei der Definition einer [!DNL Analytics]-Aktivität brauchen Sie sowohl ein [!DNL Analytics]-Benutzerkonto als auch ein [!DNL Target]-Benutzerkonto.

Ihre Benutzerkonten müssen wie in den folgenden Abschnitten beschrieben konfiguriert werden:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Führen Sie in der [!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com) die folgenden Aufgaben aus:

### Lösungskonten mit der Adobe ID verknüpfen

Ihre [!DNL Analytics]- und [!DNL Target]-Benutzerkonten müssen mit Ihrer Adobe ID verknüpft sein.

Weitere Informationen finden Sie unter [Organisationen und Kontoverknüpfung](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en).

### Mitgliedschaft in einer Experience Cloud-Gruppe

Sie müssen Mitglied in mindestens einer [!DNL Experience Cloud]-Gruppe sein, die Zugriff auf [!DNL Analytics] und [!DNL Target] hat.

Weitere Informationen finden Sie unter [Verwalten von Experience Cloud-Benutzern und -produkten](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Um A4T für eine bestimmte Report Suite verwenden zu können, müssen Sie Zugriff auf diese Report Suite haben und Zugriff auf [!DNL Web Services Access] hinzugefügt.

1. In **[!UICONTROL Admin Console]**, klicken Sie auf [!DNL Analytics] Produktprofil und klicken Sie dann auf das **[!UICONTROL Berechtigungen]** Registerkarte.

   Anschließend können Sie sehen, auf welche Report Suites das Profil Zugriff hat.

1. Stellen Sie sicher, dass die Report Suite, auf die Sie Zugriff haben möchten, in [!DNL Target] ist eines der Produkte, die im Produktprofil aufgeführt sind, zu dem Sie gehören.

   Die folgende Abbildung zeigt ein Beispiel eines Produktprofils, das Zugriff auf alle Report Suites hat:

   ![Registerkarte &quot;Admin Console Permission&quot;](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Zugriff auf die [!UICONTROL Zugriff auf Webdienste] hinzugefügt.

   Zugriff auf [!UICONTROL Zugriff auf Webdienste] Gruppe in [!DNL Analytics] muss [!DNL Analytics] als Berichtsquelle für [!DNL Target].


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Es sind keine zusätzlichen Berechtigungen erforderlich.
