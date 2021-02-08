---
keywords: IP-Adresse;IP-Adressen;Whitelist;Zulassungsliste;Firewall;recs;Feed;Server;Adobe Marketing Cloud;Empfehlungen
description: Ansicht einer Liste von IP-Adressen, die in Zielgruppe Recommendations-Feed-Verarbeitungsservern verwendet werden, um Ihre Firewall so zu konfigurieren, dass IP-Adressen von Adoben-Servern zugelassen werden.
title: Welche IP-Adressen verwenden Recommendations-Feed-Verarbeitungsserver?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 61%

---


# ![PREMIUM](/help/assets/premium.png) IP-Adressen, die von Empfehlungs-Feed-Verarbeitungsservern verwendet werden{#ip-addresses-used-by-recommendations-feed-processing-servers}

Mithilfe der Liste der von Servern, die den Recommendations-Feed verarbeiten, verwendeten IP-Adressen, die sich im Data Center in Oregon befinden, können Sie Ihre Firewall so konfigurieren, dass die entsprechenden IP-Adressen der Adobe-Server zugelassen werden.

[!DNL Target] [!UICONTROL Recommendations]-Aktivitäten verwenden die folgenden IP-Adressen, die sich im Data Center in Oregon befinden, wenn sie auf die FTP-Server von Kunden zugreifen (über den folgenden Link finden Sie die neuesten Informationen):

| CIDR-Notation | Start-IP | End-IP |
|---|---|---|
| 192.243.242.0/24 | 192.243.242.0 | 192.243.242.255 |

[!DNL Target] [!UICONTROL Recommendations]-APIs verwenden die folgenden IP-Adressen, die sich im Data Center in Oregon befinden (über den folgenden Link finden Sie die neuesten Informationen):

| CIDR-Notation | Start-IP | End-IP |
|---|---|---|
| 192.243.224.0/20 | 192.243.224.0 | 192.243.239.255 |

>[!NOTE]
>
>Die vollständige, aktuellste Liste finden Sie unter [IP-Adressen, die im Adobe Experience Cloud](https://helpx.adobe.com/analytics/kb/adobe-ip-addresses.html) verwendet werden.

