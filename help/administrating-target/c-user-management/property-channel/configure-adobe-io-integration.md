---
description: Informationen über die Gewährung von Adobe I/O-Integrationen auf alle Arbeitsbereiche mit der gewünschten Rolle.
keywords: Integration; Rollen; Benutzerberechtigungen; admin Console
seo-description: Informationen über die Gewährung von vorhandenen Adobe I/O-Integrationen auf alle Arbeitsbereiche mit der gewünschten Rolle in Adobe Target
seo-title: Gewähren Sie Adobe I/O Integrationen Zugriff auf Arbeitsbereiche und weisen Sie ihnen Rollen in Adobe Target zu.
solution: Target
subtopic: Erste Schritte
title: Gewähren Sie den Adobe I/O Integrationen Zugriff auf Arbeitsbereiche und weisen Sie Rollen zu.
translation-type: tm+mt
source-git-commit: e1174aacc5610878c8671e88fbd20d51fedffe6c

---


# ![PREMIUM](/help/assets/premium.png) Gewährt Zugriff auf Adobe I/O-Integrationen auf Arbeitsflächen und weisen Rollen Rollen zu.

[!UICONTROL Mit der Enterprise-Berechtigung] können [!DNL Target] Kunden eine einzige Organisation verwenden, sie jedoch in Arbeitsflächen für verschiedene Teams oder Arbeitsabläufe unterteilen.

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung [Target Premium](/help/c-intro/intro.md#premium) verfügbar. Sie sind in [!DNL Target Standard] nicht ohne [!DNL Target Premium]-Lizenz verfügbar.

The [!UICONTROL Enterprise Permissions] feature facilitates effective scaling of optimization programs across teams. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier in 2019. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!DNL Target] [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

Dieses Update unterstützt die folgenden Anwendungsfälle:

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Gewähren Sie der Adobe I/O-Integration Zugriff auf ausgewählte Arbeitsbereiche mit der entsprechenden Rolle, damit ein zentrales Team API-basierte Änderungen in nur wenigen Arbeitsbereichen vornehmen kann.
* Weisen Sie jedem Team, das seinen Arbeitsbereich besitzt, seine eigene Integration zu, sobald das Team bereit ist, apis zu entdecken und die Rolle entsprechend auszuwählen.
* Kombinieren Sie die obigen Szenarien und stimmen Sie überein.

**Erforderliche Aktion**: Diejenigen Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihren vorhandenen Adobe I/O-Integrationszugriff auf alle Arbeitsbereiche mit der gewünschten Rolle gemäß ihrem Verwendungsfall erteilen. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of choice made from the [!UICONTROL Product Role] drop-down list. Sie können jetzt die gewünschte Rolle auswählen.

This action should be performed during the month of **August 2019** to not face any disruption on your end. If this action is not performed, after the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. Es gibt keine negative Reaktion auf die Einrichtung von Integrationen im Voraus. Je früher Sie diese Änderung vornehmen, desto besser. Es ist nur wenig Zeit erforderlich, um diese Einstellung einzurichten, je nach Anzahl der Arbeitsbereiche in Ihrer Organisation. Dieser Vorgang erfordert nur einige Klicks, um eine vorhandene Integration in Arbeitsflächen mit der gewünschten Rolle zu integrieren.

**So erteilen Sie Adobe I/O-Integrationen Zugriff auf Arbeitsflächen und weisen Rollen zu:**

1. Open the **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Click the **[!UICONTROL Products]** tab, then select the name of the desired product.

   ![Produkt in Adobe Admin Console auswählen](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Wählen Sie den gewünschten Arbeitsbereich aus (Produktprofil).

   ![Produktprofil auswählen](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Click the **[!UICONTROL Integrations]** tab.

   ![Integrations-Registerkarte](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Conditional) To add a new integration, click **[!UICONTROL Add Integration]**, select the desired integration, then click **[!UICONTROL Save]**.

1. From the **[!UICONTROL Product Role]** drop-down list, select the desired role for that workspace:

   * [!UICONTROL Genehmigende Person]
   * [!UICONTROL Editor]
   * [!UICONTROL Beobachter]
   ![Rolle "Produktprofil" wählen](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
