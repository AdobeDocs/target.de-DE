---
keywords: Integration; Rollen; Benutzerberechtigungen; Admin Console
description: Erfahren Sie, wie Sie bestehenden Adobe I/O-Integrationen Zugriff auf alle Arbeitsbereiche mit der gewünschten Rolle in Adobe Target gewähren.
title: Wie gewähre ich Adobe I/O Zugriff auf Arbeitsbereiche und weise Rollen zu?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 62f6399f-c590-470c-ac3b-e0c84db63112
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 59%

---

# Zugriff von Adobe I/O-Integrationen auf Arbeitsbereiche gewähren und Rollen zuweisen

[!UICONTROL Enterprise Permissions] können [!DNL Target] Kunden eine einzelne Organisation verwenden, sie jedoch in Arbeitsbereiche für ihre verschiedenen Teams oder Workflows unterteilen.

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung [Target Premium](/help/main/c-intro/intro.md#premium) verfügbar. In [!DNL Target Standard] sind sie nur mit einer [!DNL Target Premium]-Lizenz verfügbar.

Die [!UICONTROL Enterprise Permissions] Funktion ermöglicht eine effektive Skalierung von Optimierungsprogrammen über Teams hinweg. Die Funktion war zwar in der [!DNL Target]-Benutzeroberfläche verfügbar, die Admin-APIs werden aber erst seit Anfang 2019 unterstützt. In der [!DNL Target]-Version vom Februar 2019 aktualisierte Adobe die Admin-APIs, sodass Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. Während Admin-APIs früher nur auf den Standardarbeitsbereich beschränkt waren, gewährte die Aktualisierung vom Februar 2019 Zugriff auf alle Arbeitsbereiche mit [!UICONTROL Approver] Zugriff.

Mit der Version vom [!DNL Target]. September 2019 bietet [!DNL Target] [!UICONTROL Enterprise Permissions] Kunden die folgenden Zugriffssteuerungen:

* Sie können die Arbeitsbereiche auswählen, auf die die Integration angewendet wird.
* Sie können der Adobe I/O-Integration eine Rolle zuweisen: [!UICONTROL Approver], [!UICONTROL Editor] oder [!UICONTROL Observer].

Dieses Update unterstützt die folgenden Anwendungsfälle:

* Gewähren Sie der Adobe I/O-Integration Zugriff auf alle Arbeitsbereiche mit der Rolle [!UICONTROL Observer] zu Berichtszwecken, ohne Rechte zum Erstellen oder Bearbeiten von Ressourcen.
* Sie können der Adobe I/O-Integration Zugriff auf ausgewählte Arbeitsbereiche mit der entsprechenden Rolle gewähren, damit ein zentrales Team API-basierte Änderungen in nur wenigen Arbeitsbereichen vornehmen kann.
* Sie können jedem Team, das seinen eigenen Arbeitsbereich hat und APIs nutzen möchte, seine eigene Integration bereitstellen und eine entsprechende Rolle dafür auswählen.
* Sie können die obigen Szenarien beliebig kombinieren.

**Erforderliche Aktion**: Diejenigen Kunden, die derzeit APIs für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) in allen Arbeitsbereichen verwenden, müssen ihrer vorhandenen Adobe I/O-Integration Zugriff auf alle Arbeitsbereiche erteilen und die entsprechende Rolle gemäß dem Anwendungsfall zuweisen. Wählen Sie dazu die einzelnen [!DNL Target] [!UICONTROL Product Profile] in der [!DNL Adobe Admin Console] aus und fügen Sie die Integrationen auf der Registerkarte [!UICONTROL Integration] hinzu. Vor der Version vom September verwendeten alle Integrationen [!UICONTROL Approver] Zugriff, unabhängig davon, welche Auswahl aus der Dropdown-Liste [!UICONTROL Product Role] getroffen wurde. Jetzt können Sie die gewünschte Rolle auswählen.

>[!NOTE]
>
>Wenn Sie diese Aktion nicht ausführen, wird die Zugriffskontrolle ab der [!DNL Target]-Version vom September 2019 aktiviert und Sie werden nur auf den Standard-Arbeitsbereich zugreifen können, sofern dies Ihre aktuelle Einstellung ist. Das vorzeitige Einrichten von Integrationen hat keine Nachteile. Je früher Sie diese Änderung vornehmen, desto besser. Je nach der Anzahl der Arbeitsbereiche in Ihrer Organisation dauert dieser Prozess nur wenige Klicks, um eine vorhandene Integration in Arbeitsbereiche mit der gewünschten Rolle hinzuzufügen.

**So gewähren Sie Adobe I/O-Integrationen Zugriff auf Arbeitsbereiche und weisen eine Rolle zu:**

1. Öffnen Sie die **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Products]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Produkt in Adobe Admin Console auswählen](/help/main/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Wählen Sie den gewünschten Arbeitsbereich (Produktprofil) aus.

   ![Produktprofil auswählen](/help/main/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Integrations]** .

   ![Tab „Integrationen“](/help/main/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Bedingt) Um eine neue Integration hinzuzufügen, klicken Sie auf **[!UICONTROL Add Integration]**, wählen Sie die gewünschte Integration aus und klicken Sie dann auf **[!UICONTROL Save]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Product Role]** die gewünschte Rolle für diesen Arbeitsbereich aus:

   | Rolle | Beschreibung |
   |--- |--- |
   | Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | Bearbeiter | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | Publisher | Ähnlich wie die Beobachterrolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Publisher-Rolle zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |
