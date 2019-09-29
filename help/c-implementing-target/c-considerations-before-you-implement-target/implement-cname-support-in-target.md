---
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
keywords: Client Care;CNAME;Zertifikatsprogramm;kanonischer Name;Cookies;Zertifikat; amc; adobe managed certificate
seo-description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
seo-title: CNAME und Adobe Target
solution: Target
title: CNAME und Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: b7a80326b0b89f6fe3bac70ccc6941be09d14ac1

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Informationen zur Arbeit mit dem Adobe-Kundendienst zur Implementierung der CNAME-Unterstützung (Canonical Name) in [!DNL Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, sodass Aufrufe an eine Domäne des Kunden statt an eine Domäne im Besitz von Adobe erfolgen.

Perform the following steps to request CNAME support in [!DNL Target]:

1. Open a Customer Care ticket requesting CNAME support for your  calls.[](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)[!DNL Target]

1. Create CNAME records (see instructions below).

   Nach Erhalt des Tickets sollte Ihnen ein FPSSL-Spezialist ein Paar CNAME-Einträge zur Verfügung stellen. These records must be configured on your company's DNS server before Adobe can purchase the certificate on your behalf.

   The CNAMES will be similar to the following example:

   `DNS record: metrics.example.com IN CNAME metricsexample-fpssl.tt.omtrdc.net`

1. When these CNAMES are in place, Adobe will work with DigiCert to purchase and install a certificate on Adobe's production servers.

1. Nachdem Sie die vorherigen Aufgaben ausgeführt haben, müssen Sie die `serverDomain` auf den neuen CNAME in at.js aktualisieren.
