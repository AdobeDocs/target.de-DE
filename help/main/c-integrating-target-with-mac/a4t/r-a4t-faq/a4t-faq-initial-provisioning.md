---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4t; Bereitstellung; Bereitstellen; Adobe Experience Cloud
description: Hier finden Sie Antworten auf häufig gestellte Fragen zur Bereitstellung von Analytics für  [!DNL Target] A4T), wo Sie das Analytics-Reporting für - [!DNL Target]  verwenden können.
title: Wo finde ich Informationen über die Erstbereitstellung von A4T?
feature: Analytics for Target (A4T)
exl-id: 4b098444-3e5b-45e3-b635-1857c2c8d183
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 61%

---

# Erste Bereitstellung – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig zu [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) gestellt werden.

## Wie kann ich eine mehrseitige A4T-Aktivität einrichten?

+++Antwort
So implementieren Sie einen einfachen mehrseitigen A4T-Anwendungsfall:

* Implementieren Sie die JavaScript-Bibliotheken für Target und Analytics auf der Landingpage der Aktivität . Bei der Implementierung beider Lösungen werden die Target-Daten mit den Analytics-Daten für jeden Besucher zusammengeführt. Diese Daten bleiben in Analytics, bis sie ablaufen. Der standardmäßige Ablaufzeitraum beträgt 90 Tage.

* Für die verbleibenden Seiten der Website, auf denen nur die Analytics-Metriken verfolgt werden sollen, implementieren Sie Analytics. Es ist nicht erforderlich, Target auf diesen Seiten zu implementieren. Die Analytics-Metriken, die auf diesen Seiten erfasst werden, werden automatisch mit der Target-Aktivität zusammengeführt, für die sich der Benutzer ursprünglich qualifiziert hat, basierend auf den Target-Informationen über diesen Benutzer aus dem vorherigen Punkt.

+++

## Wie kann ich feststellen, ob A4T in meinem [!DNL Target]-Konto aktiviert ist? {#section_4437D284448F4313BF953D4B6EDBACA6}

+++Antwort
Zur Auswahl einer Report Suite bei der Definition einer Analytics-Aktivität brauchen Sie sowohl ein Analytics-Benutzerkonto als auch ein Target-Benutzerkonto. Ihre Benutzerkonten müssen wie in der Dokumentation beschrieben konfiguriert werden. Siehe [Anforderungen an Benutzerberechtigungen](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083).

Sobald Sie Mitglied einer oder mehrerer Experience Cloud-Gruppen sind, die Zugriff auf Analytics und Target haben, und Sie Zugriff auf alle Report Suites haben, sollte unter **[!UICONTROL Create Activity]** die Option zum Erstellen eines A/B-Tests mit Analytics angezeigt werden.

Sollten Probleme bei der Bereitstellung auftreten, überprüfen Sie, ob A4T richtig bereitgestellt wird.

+++

## Warum werden meine Report Suites nicht geladen?  {#section_6CC8B2B3568A46C499895EB9811FDC2E}

+++Antwort
Überprüfen Sie, ob eines der folgenden Probleme auftritt:

* Stellen Sie sicher, dass Ihre Analytics- und Target-Konten in der Experience Cloud verknüpft sind.
* Einige Kunden verwenden mehrere Unternehmensanmeldungen von Analytics im selben Experience Cloud-Unternehmen. Wenn Sie mehrere Anmeldungen verwenden, stellen Sie sicher, dass das letzte Analytics-Unternehmen, bei dem Sie sich angemeldet haben, mit dem Target-Konto für die Integration verknüpft ist.
* Wenn Sie seit mehreren Stunden bei Experience Cloud angemeldet sind, kann in einigen Fällen die Sitzung abgelaufen sein. Melden Sie sich ab und dann wieder an und versuchen Sie es dann erneut.

+++

## Warum sehe ich in Target keine Analytics-Optionen?  {#section_EDD996AFB08B4DB196DD934BE55BF48D}

+++Antwort
Siehe „Warum werden meine Report Suites nicht geladen?“ Oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.

+++

## Warum sehe ich in Analytics keine A4T-Berichte?  {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

+++Antwort
Siehe „Warum werden meine Report Suites nicht geladen?“ oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.

+++

## Warum sind meine Berichte in [!DNL Target] leer? {#section_3837104757464CB488C5A83014A669A1}

+++Antwort
Siehe „Warum werden meine Report Suites nicht geladen?“ oben. Dieses Problem hat im Wesentlichen dieselbe Ursache.

+++
