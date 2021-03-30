---
keywords: IP-Adresse;IP-Adressen;Whitelist;Zulassungsliste;Firewall;recs;Feed;Server;Adobe Marketing Cloud;Empfehlungen
description: Ansicht einer Liste von IP-Adressen, die in Zielgruppe Recommendations-Feed-Verarbeitungsservern verwendet werden, um Ihre Firewall so zu konfigurieren, dass IP-Adressen von Adoben-Servern zugelassen werden.
title: Welche IP-Adressen verwenden Recommendations-Feed-Verarbeitungsserver?
feature: Recommendations
translation-type: tm+mt
source-git-commit: d90069169a23bc432c7731b3129ca7c9572f6cf4
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---


# ![PREMIUM](/help/assets/premium.png) IP-Adressen, die von Empfehlungs-Feed-Verarbeitungsservern verwendet werden

Liste der in [!DNL Adobe Target] [!DNL Recommendations]-Feed-Verarbeitungsservern verwendeten IP-Adressen, um Sie bei der Konfiguration Ihrer Firewall zu unterstützen, damit IP-Adressen von Adoben-Servern zugelassen werden.

[!DNL Target] [!UICONTROL Bei ] Recommendations-Aktivitäten werden die folgenden AWS-Hosts verwendet, wenn auf die FTP-Server von Kunden zugegriffen wird:

| Position | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations-] APIs verwenden auch dieselben AWS-Hosts.

>[!NOTE]
>
>Diese IP-Adressen wurden zuletzt am 16. März 2021 aktualisiert. Zuvor befanden sich die Server, die auf die FTP-Server zugriffen, im CIDR-Block 192.243.242.0/24. Die Server, auf denen Recommendations-APIs gehostet werden, befanden sich im CIDR-Block 192.243.224.0/20.

