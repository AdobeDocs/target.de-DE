---
keywords: Targeting;EEC;Visual Experience Composer;Fehlerbehebung für Enhanced Experience Composer;Fehlerbehebung
description: Erfahren Sie, wie Sie unter bestimmten Bedingungen Probleme beheben können, die manchmal im Adobe [!DNL Target] Enhanced Experience Composer (EEC) auftreten.
title: Wie kann ich Probleme im Zusammenhang mit Enhanced Experience Composer beheben?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: 7562a1da201b570ee529db9763ef5f4b463f65a8
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 23%

---

# Beheben von Problemen im Zusammenhang mit dem [!UICONTROL Enhanced Experience Composer]

Unter bestimmten Bedingungen treten im [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEC) manchmal Anzeigeprobleme auf.

## Der EEC lädt keine interne QA-URL, auf die nicht über eine öffentliche IP zugegriffen werden kann. {#section_D29E96911D5C401889B5EACE267F13CF}

Dies kann durch auf die Zulassungsliste setz der folgenden IP-Adressen behoben werden. Diese IP-Adressen sind für den Adobe-Server bestimmt, der für den EEC-Proxy verwendet wird. Sie werden nur für die Bearbeitung der Aktivitäten benötigt. Besucher Ihrer Site müssen diese IP-Adressen nicht auf die Zulassungsliste gesetzt haben.

Bitten Sie Ihr IT-Team, die folgenden IP-Adressen in Zulassungsliste zu nehmen:

* 34 254 77 200
* 54 73 207 147
* 54 229 152 123
* 3 224 194 242
* 54 90 51 39
* 34 228 136 112
* 54 150 116 11
* 18 178 142,8
* 54 199 107 77
* 99 80 139 221
* 54 78 56 224
* 54 247 179 246
* 54 80 219 243
* 34 201 235 54
* 54 196 224 236
* 35 75 212 45
* 52 199 184 130
* 18 180 161 176

Möglicherweise wird die folgende Fehlermeldung in [!DNL Target] angezeigt:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error image](assets/EEC_error.png)

Nachstehend sind die Ursachen für diese Fehlermeldung und die Lösungen zum Korrigieren der Situation aufgeführt:

* **Problem:** Ihre Website-Domäne (ISP) blockiert die [!UICONTROL Enhanced Experience Composer].

  **Abhilfe:** Zulassungsliste der oben aufgeführten IP-Adressen.

* **Problem:** Die IP-Adressen werden auf die Zulassungsliste gesetzt, Ihre Website unterstützt jedoch TLS-Version 1.2 nicht. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor dem [!DNL Target] 18.4.1 (25. April 2018) wurde TLS 1.0 von der Standardkonfiguration unterstützt. Weitere Informationen finden Sie unter [TLS (Transport Layer Security)-Verschlüsselungsänderungen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

  **Lösung:** Siehe folgende Frage (Die [!UICONTROL Enhanced Visual Experience Composer] wird auf sicheren Seiten meiner Site, die TLS 1.2 verwenden, nicht geladen).

## Der EEC wird auf sicheren Seiten meiner Website, für die TLS 1.0 verwendet wird, nicht geladen. (nur EEC)   {#section_C5B31E3D32A844F68E5A8153BD17551F}

Möglicherweise wird die oben unter &quot;[!UICONTROL Enhanced Visual Experience Composer] wird auf sicheren Seiten meiner Site nicht geladen&quot;beschriebene Fehlermeldung angezeigt. wenn die oben genannten IP-Adressen auf die Zulassungsliste gesetzt sind, Ihre Website TLS-Version 1.2 jedoch nicht unterstützt. [!DNL Target] verwendet derzeit die Standardkonfiguration 1.2. Vor dem [!DNL Target] 18.4.1 (25. April 2018) wurde TLS 1.0 von der Standardkonfiguration unterstützt. Weitere Informationen finden Sie unter [TLS (Transport Layer Security)-Verschlüsselungsänderungen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

So überprüfen Sie die TLS-Version auf Ihrer Website mit Firefox (bei anderen Browsern sind die Schritte ähnlich):

1. Öffnen Sie die betroffene Website in Firefox.
1. Klicken Sie in der Adressleiste des Browsers auf das Symbol &quot;**[!UICONTROL Show Site Information]**&quot;.

   ![firefox_more_info image](assets/firefox_more_info.png)

1. Klicken Sie auf **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![firefox_more_info_2 image](assets/firefox_more_info_2.png)

1. Prüfen Sie die TLS-Versionsinformationen unter den technischen Details:

   ![firefox_more_info_3 image](assets/firefox_more_info_3.png)

1. Wenn auf Ihrer Website TLS 1.0 angezeigt wird, finden Sie unter [TLS (Transport Layer Security)-Verschlüsselungsänderungen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank} weitere Informationen zur TLS-Unterstützungsrichtlinie für Target. Um die Situation vorerst zu beheben (gültig bis 12. September 2018){target=_blank}, wenden Sie sich zur Konfiguration mit Ihrer TLS-Version und der Domäne an die [Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) .

## Beim Laden von Seiten mit aktiviertem Proxy werden Fehlermeldungen zu Zeitüberschreitungen oder verweigertem Zugriff ausgegeben. (nur EEC)   {#section_60CBB9022DC449F593606C0E6252302D}

Stellen Sie sicher, dass Proxy-IPs in Ihrer Umgebung nicht blockiert werden.
