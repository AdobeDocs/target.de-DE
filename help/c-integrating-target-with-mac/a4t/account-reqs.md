---
description: Benutzerkontoanforderungen für die Erstellung einer Adobe Analytics-basierten Aktivität in Adobe Target (A4T).
keywords: Analytics als Berichtsquelle; a4t; A4T
seo-description: Benutzerkontoanforderungen für die Erstellung einer Adobe Analytics-basierten Aktivität in Adobe Target (A4T).
seo-title: Anforderungen hinsichtlich Benutzerberechtigungen
solution: Target,Analytics
title: Anforderungen hinsichtlich Benutzerberechtigungen
topic: Reports and Analytics
uuid: cf359bcd-547e-4f8f-bcf6-e646245bb9ce
translation-type: tm+mt
source-git-commit: e1d5f642505ce62900fc55784b178ba0fb320184

---


# Anforderungen hinsichtlich Benutzerberechtigungen {#user-permission-requirements}

Informationen zu den Benutzerkontoanforderungen, um eine [!DNL Adobe Analytics]basierte Aktivität in [!DNL Adobe Target] (A 4 T) zu erstellen.

Bevor eine Report Suite beim Definieren einer [!DNL Analytics] Aktivität ausgewählt werden kann, benötigen Sie ein [!DNL Analytics] Benutzerkonto und ein [!DNL Target] Benutzerkonto.

Ihre Benutzerkonten müssen wie in den folgenden Abschnitten beschrieben konfiguriert werden:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Führen Sie in der [!DNL Adobe Experience Cloud][Admin-Konsole](https://adminconsole.adobe.com)die folgenden Aufgaben aus:

### Lösungskonten mit der Adobe ID verknüpfen

Ihre [!DNL Analytics] und [!DNL Target] Benutzerkonten müssen mit Ihrer Adobe ID verknüpft sein.

Weitere Informationen finden Sie unter [Organisationen und Kontoverknüpfung](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Mitgliedschaft bei der Experience Cloud-Gruppe konfigurieren

Sie müssen Mitglied einer oder mehrerer [!DNL Experience Cloud] Gruppen sein, die Zugriff auf [!DNL Analytics] und [!DNL Target]haben.

Weitere Informationen finden Sie unter [Verwalten von Experience Cloud-Benutzern und -produkten](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html).


## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Führen Sie die folgenden Aufgaben aus [!DNL Adobe Analytics]:

### Zugriff auf die Analytics Report Suite konfigurieren

Bevor Sie Berichte für eine Analytics-gesteuerte Aktivität erstellen oder anzeigen, müssen Sie Mitglied der Gruppe **[!UICONTROL Zugriff auf alle Berichte]** sein oder ein Mitglied einer Gruppe, die Zugriff auf mindestens einen Bericht in der Report Suite hat, die Sie verwenden möchten. Stellen Sie sicher, dass Sie Mitglied dieser Gruppen sind, um Berichte anzeigen zu können.

Weitere Informationen finden Sie unter [Produktprofile und -gruppen](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html#section_AB50558124D541CF80A0D3D76D35A4BF).

### Zugriff auf die Web-Services-Zugriffsgruppe konfigurieren

Sie müssen zur Web-Services-Zugriffsgruppe gehören, damit [!DNL Adobe Analytics] sie [!DNL Analytics] als Berichtsquelle verwendet [!DNL Target]werden können.

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

Es sind keine zusätzlichen Berechtigungen erforderlich.
