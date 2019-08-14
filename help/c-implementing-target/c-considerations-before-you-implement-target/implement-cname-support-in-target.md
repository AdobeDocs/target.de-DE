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
source-git-commit: d21838bdf17327b394f6e3106ea5ce4bc72605e6

---


# CNAME und Adobe Target{#cname-and-adobe-target}

Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target. Um die Anzeigenblockprobleme am besten zu verarbeiten, wird ein CNAME verwendet, sodass eine Aufrufe an eine Domäne durchgeführt werden, die vom Kunden gehört, nicht von einer von Adobe eigenen Domäne.

Führen Sie folgende Schritte aus, um die CNAME-Unterstützung in Target anzufordern:

1. Öffnen Sie ein [Customer Care-Ticket](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), in dem Sie die CNAME-Unterstützung für Ihre Adobe Target-Aufrufe anfordern.
1. Melden Sie sich für das Programm [Adobe Managed Certificate (AMC)](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html) an und führen Sie die Implementierungsschritte in der Anleitung [!DNL Adobe Analytics]*Erstanbieter-Cookies* aus. [!DNL Target] verwendet dieselbe Methode wie [!DNL Analytics] CNAME-Unterstützung.

   Das AMC-Programm erleichtert Kunden die Implementierung von Erstanbieter-Cookies. Nach Anmeldung bei dem Programm erwirbt Adobe das Zertifikat zur Installation auf sicheren Servern und stellt es aus.

   >[!NOTE]
   >
   >Der CNAME muss konfiguriert werden, bevor Sie sich beim AMC-Programm anmelden.

1. Nachdem Sie die vorherigen Aufgaben ausgeführt haben, müssen Sie den `serverDomain` neuen CNAME in at. js aktualisieren.

## Schulungsvideo: Erstanbieter-Cookies und Verwenden von Adobe Managed Certificates

This video is a recording of [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), an initiative led by the Adobe Customer Care team. Die Diskussion des Adobe Managed Certificate-Programms beginnt um 10:21 Uhr.

[Adobe Analytics: Erstanbieter-Cookies und Verwenden von Adobe Managed Certificates](https://helpx.adobe.com/customer-care-office-hours/analytics/first-party-cookies-adobe-managed-certificates.html)
