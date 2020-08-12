---
keywords: Targeting;audience filter;audiences;filter
description: Audience-Filter in Adobe Target (oder Audiencen) sind Gruppen von Besuchern, die ein bestimmtes Merkmal oder eine Reihe von Merkmalen aufweisen.
title: Audience filters for reporting in Adobe Target
feature: null
uuid: ca2632c0-87e4-4a85-95e6-e63cf800ab2f
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 80%

---


# Zielgruppenfilter für Reporting{#audience-filters-for-reporting}

Zielgruppenfilter (oder Zielgruppen) sind Gruppen von Besuchern, die eine bestimmte Eigenschaft oder mehrere Eigenschaften teilen.

Mit Zielgruppenfiltern geben Sie die Zielgruppen für die Berichterstellung an. Sie können eine Zielgruppe auswählen und ihre Leistung mit dem gesamten Traffic vergleichen. Sie möchten möglicherweise wissen, ob Ihre Gewinner bei den verschiedenen Traffic-Quellen im Vergleich zum gesamten Traffic unterschiedlich waren. Hierdurch können Sie Zielgruppen finden, die potenziell auf unterschiedliche Inhalte ausgerichtet sein sollten. In vielen Fällen lässt sich ein Gewinner nicht dem gesamten Traffic zuordnen.

Zum Beispiel kann es sich bei Besuchern, die über eine bestimmte Suchmaschine zu Ihrer Webseite gelangen, um eine Zielgruppe handeln. Weitere Zielgruppen können z. B. auf Geschlecht, Alter, Standort, Registrierungsstatus, Kaufverlauf oder jedem weiteren beliebigen Detail basieren, das zu Besuchern erfasst werden kann. Nutzen Sie Zielgruppenfilter, um den Besucher-Traffic zu unterteilen und die Leistung des Erlebnisses für jedes Traffic-Segment zu vergleichen.

Berücksichtigen Sie bei der Planung der Verwendung von Zielgruppenfiltern für eine Aktivität die folgenden Richtlinien:

* **Besucher können mehreren Zielgruppen angehören.** Wenn zwei Audiencen eingerichtet sind (z. B. &quot;neue Besucher&quot;und &quot;Besucher von Google&quot;) und eine Person beide Kriterien erfüllt, wird dieser Besucher in beiden Audiencen gezählt und verfolgt. Daher stimmt die Summe der Besucher in den Zielgruppen nicht mit der Anzahl der Besucher in einer Aktivität überein.
* **Richten Sie Audiencen ein, bevor Sie die Aktivität starten.** Zielgruppendaten können nicht nachträglich hinzugefügt werden. Wenn Sie Zielgruppenfilter nicht vor dem Start einer Aktivität konfigurieren und sich schließlich dazu entscheiden, diese einzusetzen, nachdem die Aktivität bereits eine bestimmte Zeit läuft, können Sie für die bereits vergangene Dauer der Aktivität keine Daten erfassen.
* **Starten Sie mit zwei bis vier Zielgruppen.** Fokussieren Sie sich auf grundlegende Informationen, wie z. B. die Traffic-Quelle.
* **Benennen Sie Zielgruppen nach Bedarf um.** Sie können eine Zielgruppe ohne Beeinträchtigung der Daten umbenennen, um die Bedeutung des Zielgruppennamens besser an die erfassten Ergebnisse anzupassen, selbst wenn die Aktivität aktiv ist.
* **Geben Sie genaue Werte ein.** Bei Zielgruppenfilterwerten wird zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. eine Zielgruppe verwenden, die eine Filterung von Städten vornimmt, müssen Sie eine „ODER“-Bedingung verwenden, um mögliche Variationen von Recht- und Großschreibung einzubeziehen, wie z. B. „Vienna“, „vienna“, „wien“ und „Wien“.
* **Über die Liste „Zielgruppen“ erstellte Zielgruppen können wiederverwendet werden.** Zielgruppen, die als Teil einer Aktivität erstellt werden, können nicht wiederverwendet werden.

In den folgenden Abschnitten finden Sie weitere Informationen zum Einrichten von Zielgruppen und zur Berichterstellung:

| Aufgabe | Thema |
|--- |--- |
| Geeignete Aktivität oder geeigneten Test erstellen. | [Aktivitäten und Tests](/help/c-intro/target-key-concepts.md) |
| Zielgruppen erstellen, sofern erforderlich. | [Erstellen von Zielgruppen](/help/c-target/c-audiences/create-audience.md) |
| Mehrere Zielgruppen kombinieren, sofern erforderlich. | [Mehrere Zielgruppen kombinieren](/help/c-target/combining-multiple-audiences.md) |
| Zielgruppen auf der Seite Ziele und Einstellungen der Aktivität anwenden. | A/B Test: [Goals and Settings](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)<br>Automated Personalization:  [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>Experience Targeting: [Goals and Settings](/help/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md)<br>Multivariate Test:  [Goals and Settings](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md)<br>Recommendations: [Recommendations activity settings](/help/c-recommendations/t-create-recs-activity/recs-activity-settings.md)<br>Activity Settings: [Activity Settings](/help/c-activities/activity-settings.md) |
| Berichte mit Informationen zu den Zielgruppenfiltern anzeigen. | [Berichtseinstellungen](/help/c-reports/c-report-settings/report-settings.md) |

