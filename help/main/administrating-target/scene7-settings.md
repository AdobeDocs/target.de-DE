---
keywords: scene7;Dynamic Media Classic;Digital Asset Management;Assets;DAM;Inhaltsbibliothek;Bild tauschen
description: Verbinden Sie Adobe Target mit Adobe Dynamic Media Classic (Scene7), damit Autoren Bildangebote verwenden und Bilder aus Experience Cloud-Assets in -Aktivitäten austauschen können.
landing-page-description: Konfigurieren Sie die Scene7-Konfiguration in Administration, um Bildangebote, DAM-Workflows für die Inhaltsbibliothek und Bildaustauschaktionen im VEC und dem formularbasierten Experience Composer zu aktivieren.
short-description: Konfigurieren Sie die Scene7-Konfiguration in Administration, um Bildangebote, DAM-Workflows für die Inhaltsbibliothek und Bildaustauschaktionen im VEC und dem formularbasierten Experience Composer zu aktivieren.
title: Wie konfiguriere ich die Integration von Dynamic Media Classic (Scene7)?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
TQID: 'https://experienceleague.adobe.com/LKbjwlGIxrgaU-2i6Ddn1wi-VjsSmpQPAxYkFHRNOYQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: da3860b0-d637-47df-bef0-273751180266
    internal-label: Digital asset management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 553aa8fb523a62f72f0e2be7d7fd1b4eb663da6b
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 5%
---
# Konfigurieren von Dynamic Media Classic (Scene7)

Verwenden Sie die **[!UICONTROL Scene7-Konfiguration]** unter **[!UICONTROL Administration]**, um [!DNL Adobe Target] mit [!DNL Adobe Dynamic Media Classic] (früher [!DNL Scene7]) zu verbinden. Die Integration bringt Digital Asset Management (DAM) in die [!UICONTROL Inhaltsbibliothek] und ermöglicht Workflows zum Austauschen von Bildern in -Aktivitäten.

Informationen dazu, wie diese Registerkarte zu anderen Verwaltungsaufgaben passt, finden Sie unter [Wie verwalte ich Target?](/help/main/administrating-target/administrating-target.md). Informationen zum **[!UICONTROL von]** in der Benutzeroberfläche finden Sie unter [Grundlegendes zur  [!DNL Target] -Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md).

**Übersicht**

1. [Was die Integration ermöglicht](#what-it-enables): Bildangebote, Bildaustausch und geeignete Assets.
1. [Konto und Anmeldeinformationen](#account-and-credentials): Vorhandene [!DNL Dynamic Media] Konten und unterstützte Kontotypen.
1. [Nutzungsrichtlinien](#usage-guidelines): URLs, Bereitstellung und nicht unterstützte Elemente.
1. [Konfigurieren von Scene7 in Target](#configure-scene7): Einstellungen für Anmeldung und Region.

{{permissions-update}}

## Was die Integration ermöglicht {#what-it-enables}

Nach der **[!UICONTROL der Scene7]** Konfiguration können Autoren in [!DNL Target] Aktivitäten Bilder verwenden, die in den [!DNL Adobe Experience Cloud] Assets-Ordner hochgeladen wurden. Die Option **[!UICONTROL Bild austauschen]** wird im Aktivitäts-Workflow angezeigt, einschließlich [Visual Experience Composer und Form-Based Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Informationen zum Swap-Verhalten in VEC finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

Wenn diese Einstellung nicht konfiguriert ist **[!UICONTROL steht das Angebot „Bild austauschen]** bei der Erstellung einer Aktivität nicht zur Verfügung.

Die Integration stellt Assets bereit, die Teil von -Aktivitäten sind, und zwar über den Experience Cloud Assets-Ordner. Es **nicht** alle Assets in [!DNL Dynamic Media Classic] für die Verwendung in [!DNL Target] Aktivitäten verfügbar gemacht.

Verwalten Sie nach der Konfiguration Bildangebote in der Bibliothek [!UICONTROL Angebote]. Siehe [Inhalt verwalten](/help/main/c-experiences/c-manage-content/manage-content.md).

## Konto und Anmeldedaten {#account-and-credentials}

Wenn Sie bereits über ein [!DNL Dynamic Media]-Konto verfügen, geben Sie diese Anmeldeinformationen auf der Seite **[!UICONTROL Scene7-Konfiguration]** ein.

Adobe bietet keine beschränkten, gebührenfreien [!DNL Dynamic Media Classic] mehr für neue [!DNL Target] oder neue Benutzer. Wenn Ihr Unternehmen bereits über Anmeldedaten für diese Integration verfügt, funktionieren diese weiterhin. Bei Fragen zum Konto wenden Sie sich an Ihren [!DNL Adobe].

## Nutzungsrichtlinien {#usage-guidelines}

Beachten Sie bei der Verwendung von Bildern mit dieser Integration die folgenden Einschränkungen:

* **Bildangebote, keine Speicher-URLs.** [!DNL Dynamic Media] Speicher-URLs und veröffentlichte Versand-URLs sind unterschiedlich. Erstellen Sie keine Angebote über Speicher-Links, da der Versand fehlschlägt. Verwenden Sie [ Workflows ](/help/main/c-experiences/c-manage-content/manage-content.md)Bildangebote“ und „Bild austauschen“.
* **Öffentliche URLs in benutzerdefiniertem Code.** Um auf eine öffentliche Bild-URL direkt in einem Angebot oder in benutzerdefiniertem Code zu verweisen, hosten Sie das Bild auf Ihren eigenen Webservern und verwenden Sie diese URL. Es ist nicht möglich, eine veröffentlichte URL für ein von Experience Cloud hochgeladenes Bild zur Verwendung außerhalb [!DNL Target] Zielgruppen-Workflows zu erhalten. Diese Verwendung ist gemäß Vertrag nicht zulässig.
* **Geeignete Assets.** Nur Assets, die in den Experience Cloud Assets-Ordner hochgeladen wurden (und Workflows, die von dieser Integration unterstützt werden), sind im Umfang enthalten - nicht im vollständigen [!DNL Dynamic Media Classic].

## Konfigurieren von Scene7 in Target {#configure-scene7}

Gehen Sie wie folgt vor, um eine Verbindung mit [!DNL Dynamic Media Classic] herzustellen ([!DNL Scene7]):

1. Klicken Sie **[!UICONTROL Administration]** > **[!UICONTROL Scene7-Konfiguration]**.
1. Geben Sie Ihre [!DNL Dynamic Media Classic] Kontoinformationen ein:

   | Feld | Beschreibung |
   | --- | --- |
   | **Region** | Region Ihres [!DNL Dynamic Media]: Nordamerika, Europa oder Asien. |
   | **Ad-hoc-Ordner** | Speicherort für Inhalte außerhalb des Zielordners, die Sie manuell in [!DNL Dynamic Media] hochladen. |
   | **E-Mail-Adresse** | Für die Anmeldung bei [!DNL Dynamic Media Classic] verwendete E-Mail-Adresse ([!DNL Scene7]). |
   | **Kennwort** | Passwort für die Anmeldung bei [!DNL Dynamic Media Classic] ([!DNL Scene7]). |

   ![Scene7-Konfigurationsfelder](/help/main/administrating-target/assets/scene7-1.png)

1. Klicken Sie auf **[!UICONTROL Absenden]**.
