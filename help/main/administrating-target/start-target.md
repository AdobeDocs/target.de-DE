---
keywords: Administration;Genehmiger-Rolle;Genehmiger
description: Führen Sie die ersten Aufgaben aus [!DNL Adobe Target]  die Administratoren nach Erhalt der per E-Mail gesendeten Einladung an die  [!DNL Adobe Experience Cloud] sollten.
title: Wo kann ich mit der Verwaltung beginnen [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: b60236da-20ae-4bab-b261-6a33d2f70e23
source-git-commit: 0618d39fc5966c64cceea8f5bcccb625fc243ebb
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 32%

---

# Erste Schritte für Administratoren

Dieser Artikel enthält die ersten Schritte, [!DNL Adobe Target] Administratoren nach Erhalt der per E-Mail gesendeten Einladung zum [!DNL Adobe Experience Cloud] ausführen sollten.

## Einladung zum [!DNL Target] {#task_3E0817630774431983FAA3D2CB2E75BD}

Ein Systemadministrator in der [!DNL Adobe Admin Console] muss Sie als Benutzer in der [!DNL Target] hinzufügen, indem er Sie einlädt, der Gruppe beizutreten. Der Systemadministrator sollte Sie dann zu einer oder mehreren rollenspezifischen Gruppen hinzufügen. Beide Aufgaben werden in der [Adobe Admin Console ausgeführt](https://adminconsole.adobe.com).

Weitere Informationen finden Sie unter [Verwalten von Experience Cloud-Benutzern und -Produkten](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html) in der *Hilfe zu Experience Cloud und Core Services*.

Sie erhalten eine Einladungs-E-Mail, nachdem der Systemadministrator diese Schritte ausgeführt hat.

## Annehmen der Einladung {#task_24FE66659E634B24AB61DB8497772E17}

Nachdem Sie die Einladung zum [!DNL Adobe Experience Cloud] erhalten haben, akzeptieren Sie die Einladung, melden Sie sich an und akzeptieren Sie den [!UICONTROL End User License Agreement] (EULA).

1. Nehmen Sie die Einladung in [!DNL Adobe Experience Cloud] an.
1. Wenn Sie noch keine Adobe ID besitzen, werden Sie aufgefordert, eine zu erstellen.

   Wenn Sie über eine Adobe ID verfügen, wird Ihre Adobe ID erkannt, und Sie werden aufgefordert, sich anzumelden.
1. Akzeptieren Sie die [!UICONTROL Terms of Use].
1. Überprüfen Sie die Zusammenfassung Ihrer bisherigen Aktivitäten und klicken Sie dann auf **[!UICONTROL Continue to Experience Cloud]**.
1. Melden Sie sich bei [!DNL Adobe Experience Cloud] an und klicken Sie auf **[!UICONTROL Link Account]**.

   >[!NOTE]
   >
   >Wenn Sie Ihr Konto nicht verknüpfen, können Sie nicht auf [!DNL Target] zugreifen.

   Alle [!UICONTROL Experience Cloud] Produkte werden auf der Verknüpfungsseite angezeigt. Klicken Sie auf `Link Target` und geben Sie Ihren [!DNL Target] Benutzernamen und Ihr Kennwort ein, um auf [!DNL Target] zuzugreifen.
1. Klicken Sie auf **[!UICONTROL Continue to Experience Cloud]**.

   Sie haben zu diesem Zeitpunkt noch keine Gruppen mit Berechtigungen eingerichtet, die verknüpft werden können.
1. Wenn Sie möchten, sehen Sie sich das Einführungsvideo zu [!DNL Adobe Experience Cloud] an.
1. Um Ihre neuen Berechtigungen anzuzeigen und auf das Produkt zuzugreifen, melden Sie sich bei [!DNL Adobe Experience Cloud] ab und dann wieder an.
1. Fahren Sie mit dem nächsten Schritt fort und [weisen Sie sich die Rolle „Genehmiger“](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7) zu.

## Zuweisen der Rolle „Genehmiger“ {#task_15CAA437A71444E2932B333D5E66A3C7}

Nachdem Sie die Einladung zum [!DNL Adobe Experience Cloud] angenommen und sich angemeldet haben, bestätigen Sie, dass [!DNL Target] zu Ihrem [!DNL Experience Cloud] Konto hinzugefügt wurde, und weisen Sie sich dann die [!UICONTROL Approver] Rolle für [!DNL Target] zu.

Wenn Ihr Unternehmen über eine [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905)-Lizenz verfügt, lesen Sie [Rollen und Berechtigungen festlegen](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) im *Benutzerhandbuch*.

Wenn Ihr Unternehmen über eine [Target Premium](/help/main/c-intro/intro.md#premium)-Lizenz verfügt, lesen Sie [Schritt 6: Rollen und Berechtigungen festlegen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) im Abschnitt *Konfigurieren von Unternehmensberechtigungen*.

Ihr nächster Schritt sollte darin bestehen, Benutzer in [!DNL Target Standard] und [!DNL Target Premium] einzurichten. Weitere Informationen finden Sie unter [Benutzerverwaltung](/help/main/administrating-target/c-user-management/user-management.md).

## Erforderliche Berechtigungen zum Bearbeiten von [!UICONTROL Administration] {#admin-permissions}

**Vor dem 22. April 2025**: Benutzer mit [!UICONTROL Approvers] Berechtigungen im [!DNL Adobe Admin Console] können alle Einstellungen auf der [[!UICONTROL Administration] Seite, ](/help/main/administrating-target/administrating-target.md) Seite von [!DNL Target] bearbeiten oder ändern, unabhängig von ihrer [!DNL Target] Rolle.

**Wirksam ab 22. April 2025**: Nur [!UICONTROL Product]- und [!UICONTROL Solutions]-Administratoren können die Einstellungen in den [[!UICONTROL Administration]](/help/main/administrating-target/administrating-target.md) Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzende ohne diese Berechtigung haben schreibgeschützten Zugriff auf die [!UICONTROL Administration].

Diese Aktualisierung verbessert die organisatorische Kontrolle über [!DNL Target] Instanzkonfigurationen und verhindert versehentliche Aktualisierungen, die die Aktivitätsbereitstellung in verschiedenen Test- und Personalisierungsteams beeinträchtigen könnten.
