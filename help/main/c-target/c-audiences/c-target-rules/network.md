---
keywords: Targeting; Netzwerk; Zielnetzwerk; ISP; Domänenname; Verbindungsgeschwindigkeit; Target ISP; Zieldomänenname; Zielverbindungsgeschwindigkeit
description: Erfahren Sie, wie Sie Zielgruppen in  [!DNL Adobe Target]  basierend auf Netzwerkdetails erstellen.
title: Kann ich Besuchende auf der Grundlage von Netzwerkoptionen ansprechen?
feature: Audiences
exl-id: 0a479d6d-ca17-43b8-9a42-8e68f31d4d54
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 64%

---

# Netzwerk

Sie können Zielgruppen in [!DNL Adobe Target] basierend auf Netzwerkdetails wie ISP, Domain-Name und Verbindungsgeschwindigkeit erstellen.

1. Klicken Sie in der [!DNL Target] auf **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Network]** per Drag-and-Drop in den Bereich Audience Builder .
1. Klicken Sie auf **[!UICONTROL Select]** und wählen Sie dann eine der folgenden Optionen aus:

   * **ISP:** Ein ISP ist eine Organisation, die ihren Abonnenten Internetzugang ermöglicht, in der Regel gegen eine monatliche oder jährliche Gebühr. Viele ISPs bieten weitere Services, wie Webhosting oder E-Mail. Das ISP-Feld enthält entweder einen kommerziellen ISP (beispielsweise Telekom oder Vodafone) oder eine andere Entität, wie beispielsweise ein Unternehmen oder eine Bildungseinrichtung.

     Die folgenden ISPs sind einige der beliebten ISPs in den USA:

     | Beliebter Name | ISP-Name | Domänenname | Beispiel-IP-Address |
     |---|---|---|---|
     | Cablevision | Cablevision Systems Corp. | &#42;.optonline.net | 68.196.130.239 |
     | CenturyLink | Qwest Communications Company, LLC | &#42;.centurylink.net | 64.40.65.0 |
     | Charter Communications | Charter Communications | &#42;.charter.com | 71.85.225.124 |
     | Comcast | Comcast Cable Communications, Inc. | &#42;.comcast.net | 76.27.24.28 |
     | Cox | Cox Communications Inc. | &#42;cox.net | 68.224.174.22 |
     | Speakeasy | MegaPath Corporation | &#42;.speakeasy.net | 66.93.240.0 |
     | Time Warner | Time Warner Cable Internet LLC | &#42;.res.rr.com | 72.229.28.185 |
     | Verizon FiOS | MCI Communications Services, Inc. d/b/a Verizon Business | &#42;.fios.verizon.net | 173.68.112.34 |
     | Vivint | Smartrove Inc. | &#42;.vivintwireless.net | 170.72.26.105 |
     | AT&amp;T Wireless | AT | &#42;.mycingular.net |  |
     | Sprint mobile | Sprint Personal Communications Systems | IP-Adresse |  |
     | T-Mobile | T-Mobile USA, Inc. | IP-Adresse | 208.54.86.0 |
     | Verizon Wireless | Cellco Partnership DBA Verizon Wireless | &#42;.myvzw.com | 70.195.74.199 |

     >[!NOTE]
     >
     >Verwenden Sie beim ISP-basierten Targeting den ISP-Namen, nicht den bekannten Namen. Stellen Sie bei der Erstellung von Regeln sicher, dass sie nicht von der Groß-/Kleinschreibung abhängig sind, oder verwenden Sie nur Kleinbuchstaben.

     Sie können die Werte des ISP und des Domänennamens testen. [https://www.whoismyisp.org](https://www.whoismyisp.org) ist eine gute Ressource für Targeting-Zwecke. Sie können die oben in der Tabelle angegebenen Beispiel-IP-Adressen verwenden oder eine eigene eingeben. Verwenden Sie dann den Parameter `mboxOverride.browserIp= URL`, um diese IP-Adresse zu imitieren.

   * **Domain-Name** Dieser Name ist der Domain-Name für die IP-Adresse des Besuchers. Dieser Name ist nicht der Domain-Name der Website, die Sie mit [!DNL Target] verwenden. Dieser Domänenname bezieht sich auf die IP-Adresse des Besuchers und wird manchmal auch als Hostname bezeichnet. Er ähnelt dem Namen des ISPs. Manchmal verweist der Hostname auf ältere Namen von Unternehmen, die ihren ISP-Namen umbenannt haben, aber nicht auf den Domain-Namen.
   * **Verbindungsgeschwindigkeit:** Diese Geschwindigkeit ist die Geschwindigkeit der Internetverbindung des Besuchers. Es sind unter anderem folgende Optionen verfügbar: Breitband, Kabel, Einwahl, Mobil, OC3, OC12, Satellit, T1, T2 und Drahtlos, xDSL.

     Dieses Feld basiert auf dem Verbindungstyp, nicht auf der tatsächlichen Geschwindigkeit. [!DNL Target] kann die genauen Geschwindigkeiten von Verbindungen nicht ermitteln. Der Breitband-Verbindungstyp wird verwendet, wenn kein Hinweis auf andere Verbindungstypen vorhanden ist und somit keine bestimmte Verbindung gewählt werden kann.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Done]**.

Die folgende Abbildung zeigt eine Zielgruppe, die Besucher, die AT&amp;T verwenden, mit einer Verbindungsgeschwindigkeit von [!UICONTROL Mobile] anspricht.

![Netzwerk als Zielgruppe](assets/target_network.png)

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
