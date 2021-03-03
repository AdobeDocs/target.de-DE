---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4t; Bereitstellung; Bereitstellen; Adobe Experience Cloud
description: Hier finden Sie Antworten auf häufig gestellte Fragen zur Bereitstellung von Analytics für die Zielgruppe (A4T), mit der Sie Analytics Berichte für Aktivitäten der Zielgruppe verwenden können.
title: Wo finde ich Informationen zur A4T-Erstbereitstellung?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: e45f0d2d2370f9c7aba2c2bd26afdd4c0e401db8
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 68%

---


# Erste Bereitstellung – Häufig gestellte Fragen zu A4T{#initial-provisioning-a-t-faq}

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Bereitstellung von [!DNL Adobe Analytics] als Berichte-Quelle für [!DNL Adobe Target] (A4T).

## Wie kann ich eine mehrseitige A4T-Aktivität einrichten?

So implementieren Sie einen einfachen mehrseitigen A4T-Anwendungsfall:

* Implementieren Sie die JavaScript-Bibliotheken für Target (at.js oder mbox.js) und Analytics auf der Start-URL/-Seite der Aktivität. Bei der Implementierung beider Lösungen werden die Target-Daten mit den Analytics-Daten für jeden Besucher zusammengeführt. Diese Daten bleiben in Analytics, bis sie ablaufen. Der standardmäßige Ablaufzeitraum beträgt 90 Tage.

* Für die verbleibenden Seiten der Website, auf denen nur die Analytics-Metriken verfolgt werden sollen, implementieren Sie Analytics. Es ist nicht erforderlich, Target auf diesen Seiten zu implementieren. Die Analytics-Metriken, die auf diesen Seiten erfasst werden, werden automatisch mit der Target-Aktivität zusammengeführt, für die sich der Benutzer ursprünglich qualifiziert hat, basierend auf den Target-Informationen über diesen Benutzer aus dem vorherigen Punkt.

## Wie finde ich heraus, ob A4T in meinem Target-Konto aktiviert ist? {#section_4437D284448F4313BF953D4B6EDBACA6}

Zur Auswahl einer Report Suite bei der Definition einer Analytics-Aktivität brauchen Sie sowohl ein Analytics-Benutzerkonto als auch ein Target-Benutzerkonto. Ihre Benutzerkonten müssen wie in der Dokumentation beschrieben konfiguriert werden. Siehe [Anforderungen an die Benutzerberechtigungen](/help/c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083).

Nachdem Sie Mitglied einer oder mehrerer Experience Cloud-Gruppen sind, die Zugriff auf Analytics und Zielgruppe haben, und Zugriff auf alle Report Suites haben, sollten Sie unter **[!UICONTROL Aktivität erstellen]** die Option zum Erstellen eines A/B-Tests mit Analytics sehen.

Sollten Probleme bei der Bereitstellung auftreten, überprüfen Sie, ob A4T richtig bereitgestellt wird.

## Warum werden meine Report Suites nicht geladen?   {#section_6CC8B2B3568A46C499895EB9811FDC2E}

Überprüfen Sie, ob eines der folgenden Probleme auftritt:

* Stellen Sie sicher, dass Ihre Analytics- und Zielgruppe-Konten im Experience Cloud verknüpft sind.
* Einige Kunden verwenden mehrere Analytics-Firmen-Anmeldungen in derselben Experience Cloud-Firma. Wenn Sie mehrere Anmeldungen verwenden, stellen Sie sicher, dass die letzte Analytics-Firma, bei der Sie sich angemeldet haben, mit dem Integrationskonto verknüpft ist.
* Wenn Sie seit mehreren Stunden bei Experience Cloud angemeldet sind, kann in einigen Fällen die Sitzung abgelaufen sein. Melden Sie sich ab und dann wieder an und versuchen Sie es dann erneut.

## Warum sehe ich in Target keine Analytics-Optionen?   {#section_EDD996AFB08B4DB196DD934BE55BF48D}

Siehe „Warum werden meine Report Suites nicht geladen?“ Über. Dieses Problem hat im Wesentlichen dieselbe Ursache.

## Warum sehe ich in Analytics keine A4T-Berichte?   {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

Siehe „Warum werden meine Report Suites nicht geladen?“ oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.

## Warum sind meine Berichte in Target leer?   {#section_3837104757464CB488C5A83014A669A1}

Siehe „Warum werden meine Report Suites nicht geladen?“ oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.
