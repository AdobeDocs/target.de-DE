---
keywords: IP-Adresse;IP-Adressen;Whitelist;Zulassungsliste;Firewall;recs;Feed;Server;Adobe Marketing Cloud;Empfehlungen
description: Ansicht einer Liste von IP-Adressen, die in Zielgruppe Recommendations-Feed-Verarbeitungsservern verwendet werden, um Ihre Firewall so zu konfigurieren, dass IP-Adressen von Adoben-Servern zugelassen werden.
title: Welche IP-Adressen verwenden Recommendations-Feed-Verarbeitungsserver?
feature: Recommendations
translation-type: tm+mt
source-git-commit: 55b246f5f0d660e6c4f71352c5b638347d55ac28
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 13%

---


# ![PREMIUM](/help/assets/premium.png) IP-Adressen, die von Empfehlungs-Feed-Verarbeitungsservern verwendet werden

Liste der in [!DNL Adobe Target] [!DNL Recommendations]-Feed-Verarbeitungsservern verwendeten IP-Adressen, um Sie bei der Konfiguration Ihrer Firewall zu unterstützen, damit IP-Adressen von Adoben-Servern zugelassen werden.

[!DNL Target] [!UICONTROL Bei ] Recommendations-Aktivitäten werden beim Zugriff auf die FTP-Server der Kunden die folgenden IP-Adressen verwendet:

| CIDR-Notation |
|---|
| 44.241.237.28/32 |
| 44.232.167.82/32 |
| 52.41.252.205/32 |

[!DNL Target] [!UICONTROL Die ] Recommendations-APIs verwenden die folgenden IP-Adressen:

| CIDR-Notation |
|---|
| 44.241.237.28/32 |
| 44.232.167.82/32 |
| 52.41.252.205/32 |

>[!NOTE]
>
>Diese IP-Adressen wurden zuletzt am 16. März 2021 aktualisiert. Zuvor befanden sich die Server, die auf die FTP-Server zugriffen, im CIDR-Block 192.243.242.0/24. Die Server, auf denen Recommendations-APIs gehostet werden, befanden sich im CIDR-Block 192.243.224.0/20.

