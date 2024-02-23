---
keywords: IP-Adresse; IP-Adressen; Whitelist; Zulassungsliste; Firewall; Datensätze; Feed; Server; Adobe Experience Cloud; Recommendations
description: Ansicht einer Liste der IP-Adressen, die von Feed-verarbeitenden  [!DNL Target]  Recommendations-Servern verwendet werden. Diese benötigen Sie, um Ihre Firewall so zu konfigurieren, dass sie von Adobe-Servern ausgehende IP-Adressen durchlässt.
title: Welche IP-Adressen verwenden feed-verarbeitende Target Recommendations-Server?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: 558de92e672c276474bc76fad19e5461ae7d4c88
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 49%

---

# Von [!DNL Recommendations] Feed-Verarbeitungsserver

Liste der in [!DNL Adobe Target] [!DNL Recommendations] Feed-Verarbeitungsserver, damit Sie Ihre Firewall so konfigurieren können, dass IP-Adressen von [!DNL Adobe] Server.

>[!IMPORTANT]
>
>23. Februar 2023: Die [!DNL Target] -Team aktualisiert derzeit die NAT-Gateway-Adressen für das Herunterladen [!DNL Recommendations] Feeds. Wenn Sie IP-auf die Zulassungsliste setz implementieren, stellen Sie sicher, dass Sie die folgenden neuen AWS-Hosts auf die Zulassungsliste gesetzt haben. Die vorhandenen Hosts sollen in Zukunft eingestellt werden. Alle neun Hosts sind jetzt einsatzbereit.

[!DNL Target] [!UICONTROL Recommendations]-Aktivitäten verwenden beim Zugriff auf die FTP-Server von Kunden die folgenden AWS-Hosts:

**Neue Hosts**:

| Standort | Host |
| --- | --- |
| Oregon | `52.40.124.129` |
| Oregon | `54.148.219.69` |
| Oregon | `54.189.208.212` |
| Oregon | `44.230.236.35` |
| Oregon | `54.190.78.243` |
| Oregon | `52.41.73.133` |

**Vorhandene Hosts**:

| Standort | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations]-APIs verwenden dieselben AWS-Hosts.
