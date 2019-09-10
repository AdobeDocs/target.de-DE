---
description: Informationen über die Gewährung von Adobe I/O-Integrationen auf alle Arbeitsbereiche mit der gewünschten Rolle.
keywords: Integration; Rollen; Benutzerberechtigungen; admin Console
seo-description: Informationen über die Gewährung von vorhandenen Adobe I/O-Integrationen auf alle Arbeitsbereiche mit der gewünschten Rolle in Adobe Target
seo-title: Gewähren Sie Adobe I/O Integrationen Zugriff auf Arbeitsbereiche und weisen Sie ihnen Rollen in Adobe Target zu.
solution: Target
subtopic: Erste Schritte
title: Gewähren Sie den Adobe I/O Integrationen Zugriff auf Arbeitsbereiche und weisen Sie Rollen zu.
translation-type: tm+mt
source-git-commit: 13ad42da73dd3fcbf4e07be1de646e0eac8c991e

---


# ![PREMIUM](/help/assets/premium.png) Gewährt Zugriff auf Adobe I/O-Integrationen auf Arbeitsflächen und weisen Rollen Rollen zu.

[!UICONTROL Mit der Enterprise-Berechtigung] können [!DNL Target] Kunden eine einzige Organisation verwenden, sie jedoch in Arbeitsflächen für verschiedene Teams oder Arbeitsabläufe unterteilen.

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung [Target Premium](/help/c-intro/intro.md#premium) verfügbar. Sie sind in [!DNL Target Standard] nicht ohne [!DNL Target Premium]-Lizenz verfügbar.

Mit der [!UICONTROL Funktion für Unternehmensberechtigungen] können optimierte Optimierungsprogramme für Teams optimiert werden. Obwohl die Funktion in der [!DNL Target] Benutzeroberfläche verfügbar war, konnten die Admin-apis bis zu Beginn 2019 die entsprechende Unterstützung ablesen. In der [!DNL Target] Version vom Februar 2019 hat Adobe die Admin-apis aktualisiert, damit Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. Zuvor waren Admin-apis also nur auf den Standardarbeitsbereich beschränkt. Das Update vom Februar 2019 ermöglichte den Zugriff auf alle Arbeitsbereiche mit [!UICONTROL dem Genehmigerzugriff.]

Mit der [!DNL Target] Version vom September [!DNL Target][!UICONTROL 2019] stehen Kunden die folgenden Zugriffssteuerungsmöglichkeiten zur Verfügung:

* Sie können die Arbeitsflächen auswählen, auf die die Integration angewendet werden kann.
* Sie können eine Rolle auf die Integration von Adobe I/O anwenden: [!UICONTROL Genehmigende Person], [!UICONTROL Editor]oder [!UICONTROL Beobachter].

Dieses Update unterstützt die folgenden Anwendungsfälle:

* Gewähren Sie der Adobe I/O-Integration Zugriff auf alle Arbeitsbereiche mit der [!UICONTROL Beobachterrolle] für Berichterstellungszwecke ohne Rechte zum Erstellen oder Bearbeiten von Ressourcen.
* Gewähren Sie der Adobe I/O-Integration Zugriff auf ausgewählte Arbeitsbereiche mit der entsprechenden Rolle, damit ein zentrales Team API-basierte Änderungen in nur wenigen Arbeitsbereichen vornehmen kann.
* Weisen Sie jedem Team, das seinen Arbeitsbereich besitzt, seine eigene Integration zu, sobald das Team bereit ist, apis zu entdecken und die Rolle entsprechend auszuwählen.
* Kombinieren Sie die obigen Szenarien und stimmen Sie überein.

**Erforderliche Aktion**: Diejenigen Kunden, die derzeit apis für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) über alle Arbeitsflächen hinweg nutzen, müssen ihren vorhandenen Adobe I/O-Integrationszugriff auf alle Arbeitsbereiche mit der gewünschten Rolle gemäß ihrem Verwendungsfall erteilen. Dazu wählen Sie die einzelnen [!DNL Target][!UICONTROL Produktprofile] aus und fügen die [!DNL Adobe Admin Console] Integration (en) auf der [!UICONTROL Registerkarte "Integration] " hinzu. Vor der September-Version wurden alle Integrationen, die mit [!UICONTROL dem Genehmiger ausgeführt wurden,] unabhängig von der Auswahl aus der Dropdownliste [!UICONTROL "Produktrolle] " ausgeführt. Sie können jetzt die gewünschte Rolle auswählen.

>[!NOTE]
>
>Wenn diese Aktion nicht durchgeführt wird, werden die Zugriffssteuerungselemente nach der Version [!DNL Target] vom September 2019 aktiviert, und Sie werden nur auf den Standardarbeitsbereich zugreifen, wenn Sie aktuell eingerichtet sind. Es gibt keine negative Reaktion auf die Einrichtung von Integrationen im Voraus. Je früher Sie diese Änderung vornehmen, desto besser. Je nach Anzahl der Arbeitsbereiche in Ihrer Organisation dauert dieser Prozess nur einige Klicks, um eine vorhandene Integration in Arbeitsflächen mit der gewünschten Rolle zu integrieren.

**So erteilen Sie Adobe I/O-Integrationen Zugriff auf Arbeitsflächen und weisen Rollen zu:**

1. Öffnen Sie die **[Adobe Admin-Konsole](https://adminconsole.adobe.com)**.

1. Click the **[!UICONTROL Products]** tab, then select the name of the desired product.

   ![Produkt in Adobe Admin Console auswählen](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Wählen Sie den gewünschten Arbeitsbereich aus (Produktprofil).

   ![Produktprofil auswählen](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Click the **[!UICONTROL Integrations]** tab.

   ![Integrations-Registerkarte](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Bedingt) Um eine neue Integration hinzuzufügen, klicken Sie auf **[!UICONTROL Integration hinzufügen]**, wählen Sie die gewünschte Integration aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

1. Wählen Sie aus der **[!UICONTROL Dropdownliste "Produktrolle]** " die gewünschte Rolle für diesen Arbeitsbereich aus:

   * [!UICONTROL Genehmigende Person]
   * [!UICONTROL Editor]
   * [!UICONTROL Beobachter]
   ![Rolle "Produktprofil" wählen](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
