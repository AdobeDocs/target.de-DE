---
keywords: Targeting;EEC;Visual Experience Composer;Fehlerbehebung für Enhanced Experience Composer;Fehlerbehebung
description: Erfahren Sie, wie Sie Probleme beheben können, die unter bestimmten Bedingungen manchmal in der  [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EWG) auftreten.
title: Wie kann ich Probleme im Zusammenhang mit der [!UICONTROL Enhanced Experience Composer] beheben?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: ef5df0ae37ca1d07c0e51c06ed78739b2d2983fc
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 22%

---

# Fehlerbehebung bei Problemen im Zusammenhang mit der [!UICONTROL Enhanced Experience Composer]

Anzeigeprobleme treten manchmal unter bestimmten Bedingungen im [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEC) auf.

## Der EEC wird keine interne QA-URL laden, auf die nicht über öffentliche IP-Adressen zugegriffen werden kann. {#section_D29E96911D5C401889B5EACE267F13CF}


+++Details
Dieses Problem kann durch Zulassungsauflistung der folgenden IP-Adressen behoben werden. Diese IP-Adressen sind für den [!DNL Adobe]-Server bestimmt, der für den EEC-Proxy verwendet wird. Diese IP-Adressen sind nur für die Bearbeitung von Aktivitäten erforderlich. Auf die Zulassungsliste setzen Besucherinnen und Besucher Ihrer Site benötigen diese IP-Adressen nicht.

Bitten Sie Ihr IT-Team um die Zulassungsliste der folgenden IP-Adressen:

### USA (va7)

40.70.154.136/29
52.254.106.240/28
52.254.106.160/28
52.254.107.16/28
20.186.185.181
20.22.83.112
20.186.185.227
52.254.106.192/28
52.254.106.0/28
52.254.107.128/28
52.254.107.80/28
52.254.106.176/28
52.254.107.32/28
52.254.105.192/28
52.254.107.64/28
52.254.106.208/28
52.254.107.0/28
52.254.106.224/28
20.14.241.153
20.186.185.239
4.152.211.251
52.254.107.144/28
52.254.106.144/28

### EMEA (nld2)

51.138.17.16/28
51.138.17.48/28
51.138.16.128/28
51.138.17.32/28
51.138.16.240/28
51.138.17.112/28
51.138.16.160/28
51.138.16.208/28
51.138.17.80/28
51.138.17.0/28
51.138.17.96/28
51.138.16.144/28
20.31.145.248
20.126.189.248
51.138.16.224/28
51.138.16.192/28
51.138.12.94
51.138.12.11
51.138.16.176/28
51.138.12.100
51.138.17.64/28
51.138.12.160/28

### APAC (aus)

20.43.104.160/28
20.227.35.177
20.40.188.227
20.43.104.112/28
20.43.104.128/28
20.43.104.144/28
20.40.188.166
20.53.206.128
20.43.104.80/28
20.43.104.16/28
20.43.105.48/28
20.43.104.96/28
20.43.104.48/28
20.40.188.194
20.43.104.32/28
20.40.191.224/28
20.43.105.16/28
20.40.191.96/28
20.43.104.176/28
20.40.191.240/28
20.43.104.64/28
20.43.105.32/28
20.43.104.192/28
20.43.105.0/28
20.43.104.0/28

### Legacy-IP-Adressen

Die folgenden Legacy-IP-Adressen sollten bis auf Weiteres weiter auf die Zulassungsliste gesetzt werden.

34.254.77.200
54.73.207.147
54.229.152.123
3.224.194.242
54.90.51.39
34.228.136.112
54.150.116.11
18.178.142.8
54.199.107.77
99.80.139.221
54.78.56.224
54.247.179.246
54.80.219.243
34.201.235.54
54.196.224.236
35.75.212.45
52.199.184.130
18.180.161.176

Möglicherweise wird die folgende Fehlermeldung in [!DNL Target] angezeigt:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error image](assets/EEC_error.png)

Nachstehend sind die Ursachen für diese Fehlermeldung und die Lösungen zum Korrigieren der Situation aufgeführt:

* **Problem:** Ihre Website-Domain (ISP) blockiert die [!UICONTROL Enhanced Experience Composer].

  auf die Zulassungsliste setzen **Remedy:** die oben aufgeführten IP-Adressen.

* **Problem:** Die IP-Adressen werden auf die Zulassungsliste gesetzt, aber Ihre Website unterstützt keine TLS-Version 1.2. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor [!DNL Target] 18.4.1 (25. April 2018) unterstützte die Standardkonfiguration TLS 1.0. Weitere Informationen finden Sie unter [TLS(Transport Layer Security)-Verschlüsselungsänderungen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html?lang=de){target=_blank}.

  **Lösung:** Sehen Sie sich die folgende Frage an (der [!UICONTROL Enhanced Visual Experience Composer] wird nicht auf sicheren Seiten meiner Site geladen, die TLS 1.2 verwenden).

+++

## Der EEC wird auf sicheren Seiten meiner Website, für die TLS 1.0 verwendet wird, nicht geladen. (nur EEC)   {#section_C5B31E3D32A844F68E5A8153BD17551F}

+++Details
Möglicherweise wird die oben unter „Der [!UICONTROL Enhanced Visual Experience Composer] wird nicht auf sicheren Seiten meiner Site geladen“ beschriebene Fehlermeldung angezeigt. Wenn die oben genannten IP-Adressen auf die Zulassungsliste gesetzt werden, Ihre Website TLS Version 1.2 jedoch nicht unterstützt. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor [!DNL Target] 18.4.1 (25. April 2018) unterstützte die Standardkonfiguration TLS 1.0. Weitere Informationen finden Sie unter [TLS(Transport Layer Security)-Verschlüsselungsänderungen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html?lang=de){target=_blank}.

So überprüfen Sie die TLS-Version auf Ihrer Website mit Firefox (bei anderen Browsern sind die Schritte ähnlich):

1. Öffnen Sie die betroffene Website in Firefox.
1. Klicken Sie auf das **[!UICONTROL Show Site Information]** in der Adressleiste des Browsers.

   ![Firefox_more_info Bild](assets/firefox_more_info.png)

1. Klicken Sie auf **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![Firefox_more_info_2 Bild](assets/firefox_more_info_2.png)

1. Prüfen Sie die TLS-Versionsinformationen unter den technischen Details:

   ![Firefox_more_info_3 Bild](assets/firefox_more_info_3.png)

1. Wenn Sie feststellen, dass Ihre Website TLS 1.0 anzeigt, finden Sie unter [TLS (Transport Layer Security)-](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html?lang=de){target=_blank} Informationen zur TLS-Support-Richtlinie von Target. Um vorläufig Abhilfe zu schaffen (gültig bis 12. September 2018){target=_blank}, wenden Sie sich zur Konfiguration mit Ihrer TLS[Version und der Domain an die &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)Kundenunterstützung“.

+++

## Beim Laden von Seiten mit aktiviertem Proxy werden Fehlermeldungen zu Zeitüberschreitungen oder verweigertem Zugriff ausgegeben. (nur EEC)   {#section_60CBB9022DC449F593606C0E6252302D}

+++Details
Stellen Sie sicher, dass Proxy-IPs in Ihrer Umgebung nicht blockiert werden.

+++
