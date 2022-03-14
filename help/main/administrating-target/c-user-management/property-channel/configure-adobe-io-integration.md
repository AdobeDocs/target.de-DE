---
keywords: Integration; Rollen; Benutzerberechtigungen; Admin Console
description: Erfahren Sie, wie Sie bestehenden Adobe I/O-Integrationen Zugriff auf alle Arbeitsbereiche mit der gewünschten Rolle in Adobe Target gewähren.
title: Wie gewähre ich der Adobe I/O Zugriff auf Arbeitsbereiche und Rollen zuweisen?
feature: Administration & Configuration
role: Admin
exl-id: 62f6399f-c590-470c-ac3b-e0c84db63112
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 84%

---

# ![PREMIUM](/help/main/assets/premium.png) Gewähren von Zugriff von Adobe I/O Integrationen auf Arbeitsbereiche und Zuweisen von Rollen

Mit [!UICONTROL Unternehmensberechtigungen] können [!DNL Target] Kunden eine Organisation in Arbeitsbereiche für verschiedene Teams oder Arbeitsabläufe unterteilen.

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung [Target Premium](/help/main/c-intro/intro.md#premium) verfügbar. In [!DNL Target Standard] sind sie nur mit einer [!DNL Target Premium]-Lizenz verfügbar.

Die Funktion [!UICONTROL Unternehmensberechtigungen] ermöglicht die Aufteilung von Optimierungsprogrammen auf Teams. Die Funktion war zwar in der [!DNL Target]-Benutzeroberfläche verfügbar, die Admin-APIs werden aber erst seit Anfang 2019 unterstützt. In der [!DNL Target]-Version vom Februar 2019 aktualisierte Adobe die Admin-APIs, sodass Sie über das Integrationskonto auf alle in Ihrem Unternehmen erstellten Arbeitsbereiche zugreifen können. Zuvor waren Admin-APIs auf den Standardarbeitsbereich beschränkt. Das Update vom Februar 2019 ermöglichte dann den Zugriff auf alle Arbeitsbereiche mit der Rolle [!UICONTROL Genehmiger].

Mit dem [!DNL Target] Version September 2019, [!DNL Target] [!UICONTROL Unternehmensberechtigungen] bietet Kunden die folgenden Zugriffskontrollen:

* Sie können die Arbeitsbereiche auswählen, auf die die Integration angewendet wird.
* Sie können der Adobe I/O-Integration eine Rolle zuweisen: [!UICONTROL Genehmiger], [!UICONTROL Bearbeiter] oder [!UICONTROL Beobachter].

Dieses Update unterstützt die folgenden Anwendungsfälle:

* Sie können der Adobe I/O-Integration mit der [!UICONTROL Beobachterrolle] Zugriff auf alle Arbeitsbereiche gewähren, sodass Berichte erstellt werden können, aber keine Rechte zum Erstellen oder Bearbeiten von Ressourcen bestehen.
* Sie können der Adobe I/O-Integration Zugriff auf ausgewählte Arbeitsbereiche mit der entsprechenden Rolle gewähren, damit ein zentrales Team API-basierte Änderungen in nur wenigen Arbeitsbereichen vornehmen kann.
* Sie können jedem Team, das seinen eigenen Arbeitsbereich hat und APIs nutzen möchte, seine eigene Integration bereitstellen und eine entsprechende Rolle dafür auswählen.
* Sie können die obigen Szenarien beliebig kombinieren.

**Erforderliche Aktion**: Diejenigen Kunden, die derzeit APIs für CRUD-Vorgänge für Ressourcen (Aktivitäten, Zielgruppen, Angebote und Berichte) in allen Arbeitsbereichen verwenden, müssen ihrer vorhandenen Adobe I/O-Integration Zugriff auf alle Arbeitsbereiche erteilen und die entsprechende Rolle gemäß dem Anwendungsfall zuweisen. Wählen Sie dazu die einzelnen [!DNL Target] [!UICONTROL Produktprofile] in der [!DNL Adobe Admin Console] aus und fügen Sie die Integrationen im Tab [!UICONTROL Integration] hinzu. Vor der September-Version wurden alle Integrationen mit der Rolle [!UICONTROL Genehmiger] ausgeführt, unabhängig davon, welche Option in der Dropdownliste [!UICONTROL Produktrolle] ausgewählt wurde. Jetzt können Sie die gewünschte Rolle auswählen.

>[!NOTE]
>
>Wenn Sie diese Aktion nicht ausführen, wird die Zugriffskontrolle ab der [!DNL Target]-Version vom September 2019 aktiviert und Sie werden nur auf den Standard-Arbeitsbereich zugreifen können, sofern dies Ihre aktuelle Einstellung ist. Das vorzeitige Einrichten von Integrationen hat keine Nachteile. Je früher Sie diese Änderung vornehmen, desto besser. Abhängig von der Anzahl der Arbeitsbereiche in Ihrer Organisation dauert dieser Prozess nur einige Klicks, um eine vorhandene Integration in Arbeitsbereiche mit der gewünschten Rolle hinzuzufügen.

**So gewähren Sie Adobe I/O-Integrationen Zugriff auf Arbeitsbereiche und weisen eine Rolle zu:**

1. Öffnen Sie die **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Klicken Sie auf den Tab **[!UICONTROL Produkte]** und wählen Sie das gewünschte Produkt aus.

   ![Produkt in Adobe Admin Console auswählen](/help/main/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Wählen Sie den gewünschten Arbeitsbereich (Produktprofil) aus.

   ![Produktprofil auswählen](/help/main/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Klicken Sie auf den Tab **[!UICONTROL Integrationen]**.

   ![Tab „Integrationen“](/help/main/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Situationsabhängig) Um eine neue Integration hinzuzufügen, klicken Sie auf **[!UICONTROL Integration hinzufügen]**, wählen Sie die gewünschte Integration aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Produktrolle]** die gewünschte Rolle für diesen Arbeitsbereich aus:

   | Rolle | Beschreibung |
   |--- |--- |
   | Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | Bearbeiter | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | Publisher | Ähnlich wie die Beobachterrolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Rolle Publisher zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |
