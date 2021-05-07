---
keywords: IP-Adresse; IP-Adressen; Whitelist; Zulassungsliste; Firewall; Recs; Feed; Server; Adobe Experience Cloud; Recommendations
description: 'Ansicht einer Liste von IP-Adressen, die auf Recommendations-Feed-Verarbeitungsservern verwendet werden, um Ihre Firewall so zu konfigurieren, dass IP-Adressen von Adoben-Servern zugelassen werden. [!DNL Target] '
title: Welche IP-Adressen verwenden feed-verarbeitende Target Recommendations-Server?
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 24%

---

# ![PREMIUM](/help/assets/premium.png) IP-Adressen, die von feed-verarbeitenden Target Recommendations-Servern verwendet werden

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
