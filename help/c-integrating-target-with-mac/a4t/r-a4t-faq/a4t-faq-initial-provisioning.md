---
description: Dieses Thema enthält Antworten auf häufig zur Bereitstellung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4t; Bereitstellung; Bereitstellen; Adobe Experience Cloud
seo-description: Dieses Thema enthält Antworten auf häufig zur Bereitstellung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
seo-title: Erste Bereitstellung – Häufig gestellte Fragen zu A4T
solution: Target
title: Erste Bereitstellung – Häufig gestellte Fragen zu A4T
topic: Standard
uuid: cc80f879-ad2a-46d6-adc2-df616e8ab0b5
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Erste Bereitstellung – Häufig gestellte Fragen zu A4T{#initial-provisioning-a-t-faq}

Dieses Thema enthält Antworten auf häufig zur Bereitstellung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Wie kann ich eine mehrseitige A 4 T-Aktivität einrichten?

So implementieren Sie eine grundlegende mehrseitige A 4 T-Anwendungsanwendung:

* Implementieren Sie die javascript-Bibliotheken für Target (at. js oder mbox. js) und Analytics auf der Startseiten-URL/Seite der Aktivität. Bei der Implementierung beider Lösungen werden die Target-Daten mit den Analytics-Daten für jeden Besucher zusammengeführt. Diese Daten bleiben in Analytics erhalten, bis sie mit dem standardmäßigen Ablauf auf 90 Tage ablaufen.

* Implementieren Sie Analytics auf diesen Seiten, wenn die restlichen Seiten der Site nur die Analytics-Metriken verfolgen sollen. Es ist nicht notwendig, Target auf diesen Seiten zu implementieren. Die Analytics-Metriken, die auf diesen Seiten erfasst werden, werden automatisch an die Target-Aktivität gesendet, für die sich der Benutzer ursprünglich qualifiziert hat, basierend auf den Target-Informationen, die diesem Besucher vom vorhergehenden Aufzählungszeichen gefolgt sind.

## Wie finde ich heraus, ob A4T in meinem Target-Konto aktiviert ist? {#section_4437D284448F4313BF953D4B6EDBACA6}

Zur Auswahl einer Report Suite bei der Definition einer Analytics-Aktivität brauchen Sie sowohl ein Analytics-Benutzerkonto als auch ein Target-Benutzerkonto. Ihre Benutzerkonten müssen wie in der Dokumentation beschrieben konfiguriert werden. Siehe [Anforderungen an die Benutzerberechtigungen](../../../c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083).

Sobald Sie Mitglied einer oder mehrerer Experience Cloud-Gruppen sind, die Zugriff auf Analytics und Target haben, und selbst auf alle Report Suites zugreifen können, sollte Ihnen unter **[!UICONTROL Aktivität erstellen die Option zum Erstellen eines A/B-Tests mithilfe von Analytics angezeigt werden]**.

Sollten Probleme bei der Bereitstellung auftreten, überprüfen Sie, ob A4T richtig bereitgestellt wird.

## Warum werden meine Report Suites nicht geladen?   {#section_6CC8B2B3568A46C499895EB9811FDC2E}

Überprüfen Sie, ob eines der folgenden Probleme auftritt:

* Stellen Sie sicher, dass Ihre Analytics- und Target-Konten mit Experience Cloud verknüpft sind.
* Wenn Sie mehrere Analytics-Firmenanmeldungen im selben Experience Cloud-Unternehmen verwenden, stellen Sie sicher, dass das letzte Analytics-Unternehmen, bei dem Sie angemeldet sind, mit dem Target-Konto für die Integration verknüpft ist.
* Wenn Sie seit mehreren Stunden bei Experience Cloud angemeldet sind, kann in einigen Fällen die Sitzung abgelaufen sein. Melden Sie sich ab und dann wieder an und versuchen Sie es dann erneut.

## Warum sehe ich in Target keine Analytics-Optionen?   {#section_EDD996AFB08B4DB196DD934BE55BF48D}

Siehe „Warum werden meine Report Suites nicht geladen?“ oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.

## Warum sehe ich in Analytics keine A4T-Berichte?   {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

Siehe „Warum werden meine Report Suites nicht geladen?“ oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.

## Warum sind meine Berichte in Target leer?   {#section_3837104757464CB488C5A83014A669A1}

Siehe „Warum werden meine Report Suites nicht geladen?“ oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.
