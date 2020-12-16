---
keywords: Analytics as reporting source;a4t;A4T;requirements
description: Benutzerkontoanforderungen für die Erstellung einer Adobe Analytics-basierten Aktivität in Adobe Target (A4T).
title: Anforderungen hinsichtlich Benutzerberechtigungen
feature: a4t implementation
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 49%

---


# Anforderungen hinsichtlich Benutzerberechtigungen

Informationen zu den Benutzerkontoanforderungen, um eine [!DNL Adobe Analytics]-basierte Aktivität in [!DNL Adobe Target] (A4T) zu erstellen.

Zur Auswahl einer Report Suite bei der Definition einer [!DNL Analytics]-Aktivität brauchen Sie sowohl ein [!DNL Analytics]-Benutzerkonto als auch ein [!DNL Target]-Benutzerkonto.

Ihre Benutzerkonten müssen wie in den folgenden Abschnitten beschrieben konfiguriert werden:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Führen Sie in der [!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com) die folgenden Aufgaben aus:

### Lösungskonten mit der Adobe ID verknüpfen

Ihre [!DNL Analytics]- und [!DNL Target]-Benutzerkonten müssen mit Ihrer Adobe ID verknüpft sein.

Weitere Informationen finden Sie unter [Organisationen und Kontoverknüpfung](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Mitgliedschaft in einer Experience Cloud-Gruppe

Sie müssen Mitglied in mindestens einer [!DNL Experience Cloud]-Gruppe sein, die Zugriff auf [!DNL Analytics] und [!DNL Target] hat.

Weitere Informationen finden Sie unter [Experience Cloud-Benutzer und -Produkte verwalten](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Konfigurieren Sie den Zugriff auf die Report Suite [!DNL Analytics]:

Um A4T für eine bestimmte Report Suite zu verwenden, müssen Sie Zugriff auf diese Report Suite haben.

1. Klicken Sie in **[!UICONTROL Admin Console]** auf ein [!DNL Analytics]-Profil und dann auf die Registerkarte **[!UICONTROL Berechtigungen]**.

   Daraufhin können Sie sehen, auf welche Report Suites das Profil Zugriff hat.

1. Stellen Sie sicher, dass die Report Suite, auf die Sie in [!DNL Target] zugreifen möchten, zu den Report Suites gehört, die im Profil aufgeführt sind, zu dem Sie gehören.

   Die folgende Abbildung zeigt ein Profil eines Produkts mit Zugriff auf alle Report Suites:

   ![Admin Console, Registerkarte Berechtigung](/help/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

Es sind keine zusätzlichen Berechtigungen erforderlich.
