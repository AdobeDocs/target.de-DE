---
keywords: Kundenunterstützung;cname;Zertifikatprogramm;Kanonischer Name;Cookies;Zertifikat;amc;adobe-verwaltetes Zertifikat
description: Informationen zur Arbeit mit Adobe Client Care zur Implementierung der CNAME-Unterstützung (Canonical Name) in Adobe Target.
title: CNAME und Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# CNAME und Adobe Target {#cname-and-adobe-target}

Informationen zur Arbeit mit dem Adobe-Kundendienst zur Implementierung der CNAME-Unterstützung (Canonical Name) in [!DNL Target]. Zur bestmöglichen Behandlung von Problemen mit der Werbeblockierung oder von ITP-bezogenen Cookie-Richtlinien wird ein CNAME verwendet, sodass Aufrufe an eine Domäne des Kunden statt an eine Domäne im Besitz von Adobe erfolgen.

Perform the following steps to request CNAME support in [!DNL Target]:

1. Öffnen Sie ein Ticket für die [Kundenunterstützung, um CNAME-Unterstützung](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) für Ihre [!DNL Target] Anrufe anzufordern.

1. Erstellen Sie CNAME-Einträge (siehe unten stehende Anweisungen).

   Nach Erhalt des Tickets sollte Ihnen ein FPSSL-Spezialist ein Paar CNAME-Einträge zur Verfügung stellen. Diese Datensätze müssen auf dem DNS-Server Ihres Unternehmens konfiguriert werden, bevor Adobe das Zertifikat in Ihrem Namen erwerben kann.

   Das CNAMES ähnelt dem folgenden Beispiel:

   `DNS record: metrics.example.com IN CNAME metricsexample-fpssl.tt.omtrdc.net`

1. Wenn diese CNAMES eingerichtet sind, kauft und installiert Adobe zusammen mit DigiCert ein Zertifikat auf den Produktionsservern von Adobe.

1. Nachdem Sie die vorherigen Aufgaben ausgeführt haben, müssen Sie die `serverDomain` auf den neuen CNAME in at.js aktualisieren.
