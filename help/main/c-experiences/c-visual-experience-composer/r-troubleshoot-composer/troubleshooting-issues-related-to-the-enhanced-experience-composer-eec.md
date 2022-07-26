---
keywords: Targeting;EEC;Visual Experience Composer;Fehlerbehebung für Enhanced Experience Composer;Fehlerbehebung
description: Erfahren Sie, wie Sie Probleme beheben können, die manchmal in der Adobe auftreten [!DNL Target] Enhanced Experience Composer (EEC) unter bestimmten Bedingungen.
title: Wie kann ich Probleme im Zusammenhang mit Enhanced Experience Composer beheben?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: 5408c0ae5318250fa1f035f8cb8211a16600cf24
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 39%

---

# Beheben von Problemen mit [!UICONTROL Enhanced Experience Composer]

Anzeigeprobleme treten manchmal in [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EWG) unter bestimmten Voraussetzungen.

## Der EEC lädt eine interne QA-URL nicht, auf die nicht über eine öffentliche IP zugegriffen werden kann. {#section_D29E96911D5C401889B5EACE267F13CF}

Dies kann durch auf die Zulassungsliste setz der folgenden IP-Adressen behoben werden. Diese IP-Adressen beziehen sich auf den Server der Adobe, der für den EEC-Proxy verwendet wird. Sie werden nur für die Bearbeitung der Aktivitäten benötigt. Besucher Ihrer Site müssen diese IP-Adressen nicht auf die Zulassungsliste gesetzt haben.

Bitten Sie Ihr IT-Team, die folgenden IP-Adressen in Zulassungsliste zu nehmen:

* 34 253 100 20
* 34 248 100 23
* 52 49 228 246
* 54 205 42 123
* 107 22 177 39
* 52 201 5 105
* 52 193 211 177
* 18 180 24 249
* 52 194 154 154 154

Möglicherweise wird die folgende Fehlermeldung in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error-Bild](assets/EEC_error.png)

Nachstehend sind die Ursachen für diese Fehlermeldung und die Lösungen zum Korrigieren der Situation aufgeführt:

* **Problem:**[!UICONTROL Ihre Website-Domäne (ISP) blockiert den Enhanced Experience Composer].

   **Rechtsmittel:** Zulassungsliste der oben aufgeführten IP-Adressen.

* **Problem:** Die IP-Adressen werden auf die Zulassungsliste gesetzt, Ihre Website unterstützt jedoch nicht TLS-Version 1.2. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor dem [!DNL Target] 18.4.1 (25. April 2018), die Standardkonfiguration unterstützte TLS 1.0. Weitere Informationen finden Sie unter [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank}.

   **Lösung:**[!UICONTROL Siehe die folgende Frage (Der Enhanced Visual Experience Composer wird auf sicheren Seiten auf meiner Website, für die TLS 1.2 verwendet wird, nicht geladen).]

## Der EEC wird auf sicheren Seiten meiner Website, für die TLS 1.0 verwendet wird, nicht geladen. (nur EEC)   {#section_C5B31E3D32A844F68E5A8153BD17551F}

Möglicherweise wird die oben unter &quot;Die [!UICONTROL Enhanced Visual Experience Composer] wird auf sicheren Seiten meiner Site nicht geladen.&quot; wenn die oben genannten IP-Adressen auf die Zulassungsliste gesetzt sind, Ihre Website TLS-Version 1.2 jedoch nicht unterstützt. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor dem [!DNL Target] 18.4.1 (25. April 2018), die Standardkonfiguration unterstützte TLS 1.0. Weitere Informationen finden Sie unter [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank}.

So überprüfen Sie die TLS-Version auf Ihrer Website mit Firefox (bei anderen Browsern sind die Schritte ähnlich):

1. Öffnen Sie die betroffene Website in Firefox.
1. Klicken Sie in der Adresszeile des Browsers auf das Symbol **[!UICONTROL Website-Informationen anzeigen]**.

   ![firefox_more_info-Bild](assets/firefox_more_info.png)

1. Klicken Sie auf **[!UICONTROL Verbindungsdetails anzeigen]** > **[!UICONTROL Weitere Informationen]**.

   ![firefox_more_info_2-Bild](assets/firefox_more_info_2.png)

1. Prüfen Sie die TLS-Versionsinformationen unter den technischen Details:

   ![firefox_more_info_3-Bild](assets/firefox_more_info_3.png)

1. Wenn auf Ihrer Website TLS 1.0 angezeigt wird, lesen Sie [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank} für Informationen zur TLS-Unterstützungsrichtlinie für Target. Wenden Sie sich an , um die Situation vorerst zu beheben (gültig bis 12. September 2018){target=_blank}, und wenden Sie sich an [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) für die Konfiguration mit Ihrer TLS-Version und der Domäne.

## Beim Laden von Seiten mit aktiviertem Proxy werden Fehlermeldungen zu Zeitüberschreitungen oder verweigertem Zugriff ausgegeben. (nur EEC)   {#section_60CBB9022DC449F593606C0E6252302D}

Stellen Sie sicher, dass Proxy-IPs in Ihrer Umgebung nicht blockiert werden.
