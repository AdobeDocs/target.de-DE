---
keywords: Targeting;EEC;Visual Experience Composer;Fehlerbehebung für Enhanced Experience Composer;Fehlerbehebung
description: Erfahren Sie, wie Sie Probleme beheben können, die manchmal im Adobe auftreten [!DNL Target] Enhanced Experience Composer (EEC) unter bestimmten Bedingungen.
title: Wie kann ich Probleme im Zusammenhang mit Enhanced Experience Composer beheben?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: cb16350389e1504c88f1cf97aeda243e1300b65e
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 25%

---

# Beheben von Problemen im Zusammenhang mit [!UICONTROL Enhanced Experience Composer]

Anzeigeprobleme treten manchmal in [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EWG) unter bestimmten Voraussetzungen.

## Der EEC lädt keine interne QA-URL, auf die nicht über eine öffentliche IP zugegriffen werden kann. {#section_D29E96911D5C401889B5EACE267F13CF}

Dies kann durch auf die Zulassungsliste setz der folgenden IP-Adressen behoben werden. Diese IP-Adressen sind für den Adobe-Server bestimmt, der für den EEC-Proxy verwendet wird. Sie werden nur für die Bearbeitung der Aktivitäten benötigt. Besucher Ihrer Site müssen diese IP-Adressen nicht auf die Zulassungsliste gesetzt haben.

Bitten Sie Ihr IT-Team, die folgenden IP-Adressen in Zulassungsliste zu nehmen:

* 99 80 139 221
* 54 78 56 224
* 54 247 179 246
* 54 80 219 243
* 34 201 235 54
* 54 196 224 236
* 35 75 212 45
* 52 199 184 130
* 18 180 161 176

Möglicherweise wird die folgende Fehlermeldung in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error-Bild](assets/EEC_error.png)

Nachstehend sind die Ursachen für diese Fehlermeldung und die Lösungen zum Korrigieren der Situation aufgeführt:

* **Problem:** Ihre Website-Domäne (ISP) blockiert die [!UICONTROL Enhanced Experience Composer].

  **Rechtsmittel:** Zulassungsliste der oben aufgeführten IP-Adressen.

* **Problem:** Die IP-Adressen werden auf die Zulassungsliste gesetzt, Ihre Website unterstützt jedoch nicht TLS-Version 1.2. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor dem [!DNL Target] 18.4.1 (25. April 2018), die Standardkonfiguration unterstützte TLS 1.0. Weitere Informationen finden Sie unter [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

  **Lösung:** Siehe folgende Frage (Die [!UICONTROL Enhanced Visual Experience Composer] wird auf sicheren Seiten meiner Site, die TLS 1.2 verwenden, nicht geladen.

## Der EEC wird auf sicheren Seiten meiner Website, für die TLS 1.0 verwendet wird, nicht geladen. (nur EEC)   {#section_C5B31E3D32A844F68E5A8153BD17551F}

Möglicherweise wird die oben unter &quot;Die [!UICONTROL Enhanced Visual Experience Composer] wird auf sicheren Seiten meiner Site nicht geladen.&quot; wenn die oben genannten IP-Adressen auf die Zulassungsliste gesetzt sind, Ihre Website TLS-Version 1.2 jedoch nicht unterstützt. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor dem [!DNL Target] 18.4.1 (25. April 2018), die Standardkonfiguration unterstützte TLS 1.0. Weitere Informationen finden Sie unter [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

So überprüfen Sie die TLS-Version auf Ihrer Website mit Firefox (bei anderen Browsern sind die Schritte ähnlich):

1. Öffnen Sie die betroffene Website in Firefox.
1. Klicken Sie auf **[!UICONTROL Show Site Information]** in der Adressleiste des Browsers.

   ![firefox_more_info-Bild](assets/firefox_more_info.png)

1. Klicks **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![firefox_more_info_2-Bild](assets/firefox_more_info_2.png)

1. Prüfen Sie die TLS-Versionsinformationen unter den technischen Details:

   ![firefox_more_info_3-Bild](assets/firefox_more_info_3.png)

1. Wenn auf Ihrer Website TLS 1.0 angezeigt wird, lesen Sie [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank} for information about Target's TLS support policy. To remedy the situation for now (valid until September 12, 2018){target=_blank}, wenden Sie sich an [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) für die Konfiguration mit Ihrer TLS-Version und der Domäne.

## Beim Laden von Seiten mit aktiviertem Proxy werden Fehlermeldungen zu Zeitüberschreitungen oder verweigertem Zugriff ausgegeben. (nur EEC)   {#section_60CBB9022DC449F593606C0E6252302D}

Stellen Sie sicher, dass Proxy-IPs in Ihrer Umgebung nicht blockiert werden.
