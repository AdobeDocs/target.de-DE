---
keywords: Implementierung;Implementierung;Whitelist;Weiße Liste;Zulassungsliste;Zulassungsliste;Kante;Kanten
description: Ansicht einer Hosts zur Liste der Adobe Target-Kanten (geografisch verteilte Serving-Knoten, die optimale Reaktionszeiten für Endbenutzer gewährleisten).
title: Wie kann ich Zielgruppe-Edge-Knoten in Zulassungslisten einordnen?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: 806c52e69cce636a56eb067759612f80829418f9
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---


# Zulassungsliste Zielgruppe Edge-Knoten

Informationen und eine aktuelle Liste von Hosts zur Unterstützung der Zulassungsliste von [!DNL Adobe Target] Kanten.

Eine Kante ist eine geografisch verteilte Serving-Architektur, die Endbenutzern, die Inhalte anfordern, optimale Reaktionszeiten gewährleistet, unabhängig davon, wo sie sich befinden. Jeder Edge-Knoten verfügt über alle erforderlichen Informationen, um auf die Inhaltsanforderung des Benutzers zu reagieren und Analysedaten zu dieser Anforderung zu verfolgen. Benutzeranforderungen werden an den nächsten Edge-Knoten weitergeleitet. Weitere Informationen finden Sie unter [Das Edge-Netzwerk](/help/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934) in *Wie Adobe [!DNL Target] funktioniert*.

Sie können bei Bedarf [!DNL Target]-Edge-Knoten in Zulassungslisten einfügen.

## NAT-IP-Adressen (Network Address Translation) von Zielgruppen-Rändern

Liste der IP-Adressen der Präzision von [!DNL Target] Kanten. Zulassungslisten dieser IPs, wenn Sie planen, dass die Zielgruppe Ihre Dienste anruft.

| Edge-Position | IP-Adressen von Kongressen |
| --- | --- |
| Edge31 (Mumbai) | 13.126.131.246<br>13.234.229.8 |
| Edge 32 (Tokio) | 3.115.154.28<br>3.115.227.146 |
| Edge34 (Ostküste USA) | 34.232.149.249<br>52.21.139.93 |
| Edge35 (Westküste USA) | 52.10.11.139<br>44.231.171.161 |
| Edge 36 (Sydney) | 13.237.227.20<br>13.210.93.142 |
| Edge 37 (Irland) | 54.72.21.68<br>52.208.139.19 |
| Edge38 (Singapur) | 18.141.132.96<br>54.179.187.167 |

## IP-Adressen von Zielgruppen-Edge

Liste der IP-Adressen von [!DNL Target]-Kanten. Zulassungslisten diese IPs, wenn Sie API-Aufrufe an Zielgruppen-Ränder vornehmen möchten.

| Edge-Position | Domäne | IP-Adressen |
| --- | --- | --- |
|  | `CLIENTCODE.tt.omtrdc.net`<br>(wobei CLIENTCODE Ihre  [!DNL Target] Client-ID ist) |  |
| Edge31 (Mumbai) | `mboxedge31.tt.omtrdc.net` | 15.207.157.131<br>15.206.8.201 |
| Edge 32 (Tokio) | `mboxedge32.tt.omtrdc.net` | 54.199.66.101<br>54.64.93.37 |
| Edge34 (Ostküste USA) | `mboxedge34.tt.omtrdc.net` | 3.225.56.36<br>3.230.207.249<br>34.198.55.51<br>52.3.14.12<br>52.21.222.9 3<br>52.55.235.132<br>52.70.52.52<br>54.165.204.89 |
| Edge35 (Westküste USA) | `mboxedge35.tt.omtrdc.net` | 52.10.244.20<br>52.36.232.38<br>52.88.209.29<br>54.214.180.56<br>35.162 74.35<br>34.214.12.211<br>52.42.35.202<br>54.148.71.13 |
| Edge 36 (Sydney) | `mboxedge36.tt.omtrdc.net` | 13.238.34.185<br>3.24.250.17<br>3.104.234.91<br>13.211.248.241 |
| Edge 37 (Irland) | `mboxedge37.tt.omtrdc.net` | 52.212.193.208<br>52.19.133.54<br>52.51.251.137<br>34.252.156.174<br>5 2.213.168.74<br>34.252.166.160<br>52.18.150.20<br>18.203.205.32 |
| Edge38 (Singapur) | `mboxedge38.tt.omtrdc.net` | 52.221.145.65<br>52.220.44.99<br>13.250.75.226<br>54.151.139.123 |





