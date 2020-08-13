---
keywords: Analytics as reporting source;a4t;A4T
description: Benutzerkontoanforderungen für die Erstellung einer Adobe Analytics-basierten Aktivität in Adobe Target (A4T).
title: Anforderungen hinsichtlich Benutzerberechtigungen
feature: a4t implementation
solution: Target,Analytics
topic: Reports and analytics
uuid: cf359bcd-547e-4f8f-bcf6-e646245bb9ce
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 63%

---


# Anforderungen hinsichtlich Benutzerberechtigungen {#user-permission-requirements}

Informationen zu den Benutzerkontoanforderungen, um eine [!DNL Adobe Analytics]-basierte Aktivität in [!DNL Adobe Target] (A4T) zu erstellen.

Zur Auswahl einer Report Suite bei der Definition einer [!DNL Analytics]-Aktivität brauchen Sie sowohl ein [!DNL Analytics]-Benutzerkonto als auch ein [!DNL Target]-Benutzerkonto.

Ihre Benutzerkonten müssen wie in den folgenden Abschnitten beschrieben konfiguriert werden:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Führen Sie in der [!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com) die folgenden Aufgaben aus:

### Lösungskonten mit der Adobe ID verknüpfen

Ihre [!DNL Analytics]- und [!DNL Target]-Benutzerkonten müssen mit Ihrer Adobe ID verknüpft sein.

For more information, see [Organizations and account linking](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Mitgliedschaft in einer Experience Cloud-Gruppe

Sie müssen Mitglied in mindestens einer [!DNL Experience Cloud]-Gruppe sein, die Zugriff auf [!DNL Analytics] und [!DNL Target] hat.

For more information, see [Manage Experience Cloud users and products](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Führen Sie die folgenden Aufgaben in [!DNL Adobe Analytics] aus:

### Zugriff auf die Analytics Report Suite konfigurieren

Before creating or viewing reports for an [!DNL Analytics]-powered activity, you must be a member of the **[!UICONTROL All Report Access]** group, or a member of a group that has access to at least one report in the report suite that you want to use. Stellen Sie sicher, dass Sie Mitglied dieser Gruppen sind, um Berichte anzeigen zu können.

Weitere Informationen finden Sie unter [Profil und Gruppen](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html#section_AB50558124D541CF80A0D3D76D35A4BF).

### Zugriff auf die Webdienste-Zugriffsgruppe konfigurieren

Sie müssen zur Zugriffsgruppe für Webdienste in [!DNL Analytics] gehören, um [!DNL Analytics] als Berichtsquelle für [!DNL Target] nutzen zu können.

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

Es sind keine zusätzlichen Berechtigungen erforderlich.
