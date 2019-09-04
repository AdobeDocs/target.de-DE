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

Informationen zur Arbeit mit dem Adobe-Kundendienst zur Implementierung der CNAME-Unterstützung (Canonical Name) in [!DNL Target]. Um die Anzeigenblockprobleme oder ITP-bezogenen Cookie-Richtlinien am besten zu verarbeiten, wird ein CNAME verwendet, damit eine Domäne aufgerufen wird, die vom Kunden gehört und nicht von einer Domäne, die von Adobe gehört.

Perform the following steps to request CNAME support in [!DNL Target]:

1. Öffnen Sie ein [Kundencare-Ticket, das CNAME-Unterstützung](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) für Ihre [!DNL Target] Aufrufe anfordert.

1. Erstellen Sie CNAME-Datensätze (siehe Anweisungen unten).

   Beim Empfang des Tickets sollte Ihnen ein FPSSL-Spezialist ein Paar von CNAME-Aufzeichnungen bereitstellen. Diese Datensätze müssen auf dem DNS-Server Ihres Unternehmens konfiguriert werden, bevor Adobe das Zertifikat in Ihrem Namen erwerben kann.

   Die CNAMES ähneln dem folgenden Beispiel:

   `DNS record: metrics.example.com IN CNAME metricsexample-fpssl.tt.omtrdc.net`

1. Wenn diese CNAMES vorhanden sind, arbeitet Adobe mit digicert zusammen, um ein Zertifikat auf den Produktionsservern von Adobe zu erwerben und zu installieren.

1. Nachdem Sie die vorherigen Aufgaben ausgeführt haben, müssen Sie den `serverDomain` neuen CNAME in at. js aktualisieren.
