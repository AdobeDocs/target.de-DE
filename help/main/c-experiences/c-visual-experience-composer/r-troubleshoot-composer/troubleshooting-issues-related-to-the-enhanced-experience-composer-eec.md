---
keywords: Targeting;EEC;Visual Experience Composer;Fehlerbehebung für Enhanced Experience Composer;Fehlerbehebung
description: Erfahren Sie, wie Sie Probleme beheben können, die unter bestimmten Bedingungen  [!DNL Target]  Adobe Enhanced Experience Composer (EEC) auftreten.
title: Wie kann ich Probleme im Zusammenhang mit Enhanced Experience Composer beheben?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: 7562a1da201b570ee529db9763ef5f4b463f65a8
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 23%

---

# Fehlerbehebung bei Problemen im Zusammenhang mit der [!UICONTROL Enhanced Experience Composer]

Anzeigeprobleme treten manchmal unter bestimmten Bedingungen im [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEC) auf.

## Der EEC wird keine interne QA-URL laden, auf die nicht über öffentliche IP-Adressen zugegriffen werden kann. {#section_D29E96911D5C401889B5EACE267F13CF}

Dies lässt sich durch die Zulassungsauflistung der folgenden IP-Adressen beheben. Diese IP-Adressen sind für den Adobe-Server bestimmt, der für den EEC-Proxy verwendet wird. Sie werden nur für die Bearbeitung der Aktivitäten benötigt. Auf die Zulassungsliste setzen Besucherinnen und Besucher Ihrer Site benötigen diese IP-Adressen nicht.

Bitten Sie Ihr IT-Team um die Zulassungsliste der folgenden IP-Adressen:

* 34.254.77.200
* 54.73.207.147
* 54.229.152.123
* 3.224.194.242
* 54.90.51.39
* 34.228.136.112
* 54.150.116.11
* 18.178.142.8
* 54.199.107.77
* 99.80.139.221
* 54.78.56.224
* 54.247.179.246
* 54.80.219.243
* 34.201.235.54
* 54.196.224.236
* 35.75.212.45
* 52.199.184.130
* 18.180.161.176

Möglicherweise wird die folgende Fehlermeldung in [!DNL Target] angezeigt:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error image](assets/EEC_error.png)

Nachstehend sind die Ursachen für diese Fehlermeldung und die Lösungen zum Korrigieren der Situation aufgeführt:

* **Problem:** Ihre Website-Domain (ISP) blockiert die [!UICONTROL Enhanced Experience Composer].

  auf die Zulassungsliste setzen **Remedy:** die oben aufgeführten IP-Adressen.

* **Problem:** Die IP-Adressen werden auf die Zulassungsliste gesetzt, aber Ihre Website unterstützt keine TLS-Version 1.2. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor [!DNL Target] 18.4.1 (25. April 2018) unterstützte die Standardkonfiguration TLS 1.0. Weitere Informationen finden Sie unter [TLS(Transport Layer Security)-Verschlüsselungsänderungen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

  **Lösung:** Sehen Sie sich die folgende Frage an (der [!UICONTROL Enhanced Visual Experience Composer] wird nicht auf sicheren Seiten meiner Site geladen, die TLS 1.2 verwenden).

## Der EEC wird auf sicheren Seiten meiner Website, für die TLS 1.0 verwendet wird, nicht geladen. (nur EEC)   {#section_C5B31E3D32A844F68E5A8153BD17551F}

Möglicherweise wird die oben unter „Der [!UICONTROL Enhanced Visual Experience Composer] wird nicht auf sicheren Seiten meiner Site geladen“ beschriebene Fehlermeldung angezeigt. Wenn die oben genannten IP-Adressen auf die Zulassungsliste gesetzt werden, Ihre Website TLS Version 1.2 jedoch nicht unterstützt. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor [!DNL Target] 18.4.1 (25. April 2018) unterstützte die Standardkonfiguration TLS 1.0. Weitere Informationen finden Sie unter [TLS(Transport Layer Security)-Verschlüsselungsänderungen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

So überprüfen Sie die TLS-Version auf Ihrer Website mit Firefox (bei anderen Browsern sind die Schritte ähnlich):

1. Öffnen Sie die betroffene Website in Firefox.
1. Klicken Sie auf das **[!UICONTROL Show Site Information]** in der Adressleiste des Browsers.

   ![Firefox_more_info Bild](assets/firefox_more_info.png)

1. Klicken Sie auf **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![Firefox_more_info_2 Bild](assets/firefox_more_info_2.png)

1. Prüfen Sie die TLS-Versionsinformationen unter den technischen Details:

   ![Firefox_more_info_3 Bild](assets/firefox_more_info_3.png)

1. Wenn Sie feststellen, dass Ihre Website TLS 1.0 anzeigt, finden Sie unter [TLS (Transport Layer Security)-](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank} Informationen zur TLS-Support-Richtlinie von Target. Um vorläufig Abhilfe zu schaffen (gültig bis 12. September 2018){target=_blank}, wenden Sie sich zur Konfiguration mit Ihrer TLS[Version und der Domain an die ](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)Kundenunterstützung“.

## Beim Laden von Seiten mit aktiviertem Proxy werden Fehlermeldungen zu Zeitüberschreitungen oder verweigertem Zugriff ausgegeben. (nur EEC)   {#section_60CBB9022DC449F593606C0E6252302D}

Stellen Sie sicher, dass Proxy-IPs in Ihrer Umgebung nicht blockiert werden.
