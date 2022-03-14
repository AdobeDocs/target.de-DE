---
keywords: IP-Adresse; IP-Adressen; Whitelist; Zulassungsliste; Firewall; Datensätze; Feed; Server; Adobe Experience Cloud; Recommendations
description: Ansicht einer Liste der IP-Adressen, die von Feed-verarbeitenden  [!DNL Target]  Recommendations-Servern verwendet werden. Diese benötigen Sie, um Ihre Firewall so zu konfigurieren, dass sie von Adobe-Servern ausgehende IP-Adressen durchlässt.
title: Welche IP-Adressen verwenden feed-verarbeitende Target Recommendations-Server?
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 100%

---

# ![PREMIUM](/help/main/assets/premium.png) IP-Adressen, die von feed-verarbeitenden Target Recommendations-Servern verwendet werden

Liste der IP-Adressen, die von Feed-verarbeitenden [!DNL Adobe Target] [!DNL Recommendations]-Servern verwendet werden. Diese benötigen Sie, um Ihre Firewall so zu konfigurieren, dass sie von Adobe-Servern ausgehende IP-Adressen durchlässt.

[!DNL Target] [!UICONTROL Recommendations]-Aktivitäten verwenden beim Zugriff auf die FTP-Server von Kunden die folgenden AWS-Hosts:

| Standort | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations]-APIs verwenden dieselben AWS-Hosts.

>[!NOTE]
>
>Diese IP-Adressen wurden zuletzt am 16. März 2021 aktualisiert. Zuvor befanden sich die Server, die auf die FTP-Server zugreifen, im CIDR-Block mit den IP-Adressen 192.243.242.0/24. Die Server, auf denen Recommendations-APIs gehostet werden, befanden sich im CIDR-Block mit den IP-Adressen 192.243.224.0/20.
