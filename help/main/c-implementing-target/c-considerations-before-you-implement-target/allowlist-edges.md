---
keywords: implementieren;implementieren;Whitelist;Whitelist;Zulassungsliste;Zulassungsliste;Edge;Edges
description: Anzeigen einer Hostliste, um die Adobe der Zulassungslisten zu erleichtern [!DNL Target] Edges (geografisch verteilte Serving-Knoten, die optimale Reaktionszeiten für Endbenutzer gewährleisten).
title: Wie kann ich eine Zulassungsliste vornehmen? [!DNL Target] Edge-Knoten?
feature: Privacy & Security
role: Developer
exl-id: 2d8399b9-eec8-40b0-8b35-2812f83ff4dc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 6%

---

# Zulassungsliste [!DNL Target] Edge-Knoten

Informationen und eine aktuelle Liste von Hosts, die Ihnen bei der Zulassungsliste von helfen [!DNL Adobe Target] Kanten.

Ein Vorteil ist eine geografisch verteilte Serving-Architektur, die Endbenutzern, die Inhalte anfordern, optimale Reaktionszeiten gewährleistet, unabhängig davon, wo sie sich befinden. Jeder Edge-Knoten verfügt über alle Informationen, die erforderlich sind, um auf die Inhaltsanforderung des Benutzers zu reagieren und Analysedaten zu dieser Anforderung zu verfolgen. Benutzeranforderungen werden an den nächsten Edge-Knoten weitergeleitet. Weitere Informationen finden Sie unter [Das Edge-Netzwerk](/help/main/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934) in *Adobe [!DNL Target] works*.

Sie können eine Zulassungsliste [!DNL Target] Kantenknoten, falls gewünscht.

## IP-Adressen der NAT (Network Address Translation) von [!DNL Target] Kanten

Liste der ausgehenden IP-Adressen von [!DNL Target] Kanten. Zulassungslisten Sie diese IPs, wenn Sie planen, Target für Ihre Dienste zu kontaktieren.

| Edge-Standort | Ausgehend-IP-Adressen |
| --- | --- |
| Edge31 (Mumbai) | 13 126 131 246<br>13 234 229,8 |
| Edge32 (Tokio) | 3 115 154 28<br>3 115 227 146 |
| Edge34 (Ostküste USA) | 34 232 149 249<br>52 21 139 93 |
| Edge35 (Westküste USA) | 52 10 11 139<br>44 231 171 161 |
| Edge36 (Sydney) | 13 237 227 20<br>13 210 93 142 |
| Edge37 (Irland) | 54 72 21 68<br>52 208 139 19 |
| Edge38 (Singapur) | 18 141 132 96<br>54 179 187 167 |

## IP-Adressen von Target-Edge

Liste der IP-Adressen von [!DNL Target] Kanten. Zulassungsliste dieser IPs, wenn Sie API-Aufrufe an Target-Edges durchführen möchten.

| Edge-Standort | Domain | IP-Adressen |
| --- | --- | --- |
|  | `CLIENTCODE.tt.omtrdc.net`<br>(wobei CLIENTCODE Ihre [!DNL Target] Client-ID) |  |
| Edge31 (Mumbai) | `mboxedge31.tt.omtrdc.net` | 15 207 157 131<br>15.206.8.201 |
| Edge32 (Tokio) | `mboxedge32.tt.omtrdc.net` | 54 199 66 101<br>54 64 93 37 |
| Edge34 (Ostküste USA) | `mboxedge34.tt.omtrdc.net` | 3 225 56 36<br>3 230 207 249<br>34 198 55 51<br>52,3,14,12<br>52 21 222 93<br>52 55 235 132<br>52 70 52 52 52<br>54 165 204 89 |
| Edge35 (Westküste USA) | `mboxedge35.tt.omtrdc.net` | 52 10 244 20<br>52 36 232 38<br>52 88 209 29<br>54 214 180 56<br>35 162 74 35<br>34 214 12 211<br>52 42 35 202<br>54 148 71 13 |
| Edge36 (Sydney) | `mboxedge36.tt.omtrdc.net` | 13 238 34 185<br>3 24 250 17<br>3 104 234,91<br>13 211 248 241 |
| Edge37 (Irland) | `mboxedge37.tt.omtrdc.net` | 52 212 193 208<br>52 19 133 54<br>52 51 251 137<br>34 252 156 174<br>52 213 168 74<br>34 252 166 160<br>52 18 150 20<br>18 203 205 32 |
| Edge38 (Singapur) | `mboxedge38.tt.omtrdc.net` | 52 221 145 65<br>52 220 44 99<br>13 250 75 226<br>54 151 139 123 |
