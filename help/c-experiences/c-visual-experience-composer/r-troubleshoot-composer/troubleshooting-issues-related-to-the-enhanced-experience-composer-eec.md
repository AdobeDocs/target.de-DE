---
description: Unter bestimmten Umständen treten im Enhanced Experience Composer (VEC) manchmal Anzeigeprobleme auf.
keywords: Targeting;EEC;Visual Experience Composer;Fehlerbehebung für Enhanced Experience Composer;Fehlerbehebung
seo-description: Unter bestimmten Umständen treten im Enhanced Experience Composer (VEC) manchmal Anzeigeprobleme auf.
seo-title: Beheben von Problemen mit Enhanced Experience Composer
solution: Target
title: Beheben von Problemen mit Enhanced Experience Composer
uuid: 2ea9a91f-08ca-4a06-ad5d-35ced140db14
translation-type: tm+mt
source-git-commit: 5dbccff982ce59d98b152f24ffa2eec046e4069f

---


# Beheben von Problemen mit Enhanced Experience Composer{#troubleshooting-issues-related-to-the-enhanced-experience-composer}

Unter bestimmten Umständen treten im Enhanced Experience Composer (VEC) manchmal Anzeigeprobleme auf.

## Der EEC lädt eine interne QA-URL nicht, auf die nicht über eine öffentliche IP zugegriffen werden kann. (nur EEC) {#section_D29E96911D5C401889B5EACE267F13CF}

Dieses Problem kann durch Hinzufügen der folgenden IP-Adressen zur „Weißen Liste“ behoben werden. Diese IP-Adressen stehen für den Server von Adobe zur Verfügung, der für den Proxy des Enhanced Experience Composer verwendet wird. Sie werden nur für die Bearbeitung der Aktivitäten benötigt. Besucher Ihrer Seite müssen diese IP-Adressen nicht auf ihre „Weiße Liste“ setzen

Bitten Sie Ihr IT-Team, folgende IP-Adressen zur Whitelist hinzuzufügen:

| Region | IP-Adressen | Hostnamen |
|--- |--- |--- |
| Vereinigte Staaten | 52.55.99.45 | `us1-proxy.adobemc.com` |
| Europa, Naher Osten und Afrika (EMEA) | 52.51.238.221 | `emea1-proxy.adobemc.com` |
| Asien-Pazfik (APAC) | 52.193.67.35 | `apac1-proxy.adobemc.com` |

Möglicherweise wird in Target die folgende Fehlermeldung angezeigt:

`Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can whitelist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

Nachstehend sind die Ursachen für diese Fehlermeldung und die Lösungen zum Korrigieren der Situation aufgeführt:

* **Problem:** Ihre Website-Domäne (ISP) blockiert den Enhanced Experience Composer.

   **Abhilfe:** Fügen Sie die oben aufgeführten IP-Adressen der Whitelist hinzu.

* **Problem:** Die IP-Adressen befinden sich auf der Whitelist, Ihre Website unterstützt jedoch nicht TLS 1.2. Target verwendet zurzeit 1.2 in der Standardkonfiguration. Vor Target 18.4.1 (25. April 2018) wurde TLS 1.0 von der Standardkonfiguration unterstützt. Weitere Informationen finden Sie unter   [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](../../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

   **Lösung:** Siehe die folgende Frage (Der Enhanced Visual Experience Composer wird auf sicheren Seiten auf meiner Website, für die TLS 1.2 verwendet wird, nicht geladen).

## Der EEC wird auf sicheren Seiten meiner Website, für die TLS 1.0 verwendet wird, nicht geladen. (nur EEC) {#section_C5B31E3D32A844F68E5A8153BD17551F}

Möglicherweise wird die zuvor unter „Der Enhanced Visual Experience Composer wird auf sicheren Seiten auf meiner Website, für die TLS 1.2 verwendet wird, nicht geladen“ beschriebene Fehlermeldung angezeigt. Dies kann geschehen, wenn die IP-Adressen sich auf der Whitelist befinden, Ihre Website jedoch TLS 1.2 nicht unterstützt. Target verwendet zurzeit 1.2 in der Standardkonfiguration. Vor Target 18.4.1 (25. April 2018) wurde TLS 1.0 von der Standardkonfiguration unterstützt. Weitere Informationen finden Sie unter   [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](../../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

So überprüfen Sie die TLS-Version auf Ihrer Website mit Firefox (bei anderen Browsern sind die Schritte ähnlich):

1. Öffnen Sie die betroffene Website in Firefox.
1. Klicken Sie in der Adresszeile des Browsers auf das Symbol **[!UICONTROL Website-Informationen anzeigen].**

   ![](assets/firefox_more_info.png)

1. Klicken Sie auf **[!UICONTROL Verbindungsdetails anzeigen]** &gt; **[!UICONTROL Weitere Informationen]**.

   ![](assets/firefox_more_info_2.png)

1. Prüfen Sie die TLS-Versionsinformationen unter den technischen Details:

   ![](assets/firefox_more_info_3.png)

1. Wenn für Ihre Website TLS 1.0 angezeigt wird, finden Sie unter   [Änderungen hinsichtlich der Verschlüsselung mit TLS (Transport Layer Security)](../../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) weitere Informationen über die TLS-Unterstützungsrichtlinie für Target. Um vorläufig Abhilfe zu schaffen (gültig bis 12. September 2018), wenden Sie sich zur Konfiguration mit Ihrer TLS-Version und der Domäne an die [Kundenunterstützung](../../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Beim Laden von Seiten mit aktiviertem Proxy werden Fehlermeldungen zu Zeitüberschreitungen oder verweigertem Zugriff ausgegeben. (nur EEC) {#section_60CBB9022DC449F593606C0E6252302D}

Stellen Sie sicher, dass Proxy-IPs in Ihrer Umgebung nicht blockiert werden.
