---
keywords: Zielgruppenbestimmung;Zielgruppenfilter;Zielgruppen;Filter
description: Erfahren Sie, wie Sie Zielgruppenfilter in verwenden [!DNL Adobe Target]  um Daten von Besucherinnen und Besuchern mit gemeinsamen Merkmalen anzuzeigen.
title: Kann ich Zielgruppenfilter für das Reporting verwenden?
feature: Audiences
exl-id: af8dae97-4b10-4edb-a0e6-0d8daf2f0d22
TQID: https://experienceleague.adobe.com/7h16ay64Y1IVu2CbkEJny-rnGms80q8X7G6gOM1P900
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eebid: f69bc5f1-ebdb-4306-a281-f2e77daf734c
subfeature_v2: id: b6f5758b-84f7-4943-8b05-1297a046943cid: e73b329c-f712-4a22-abe7-bfbf3be6d0f9id: ed58f4a1-16eb-4c8c-b505-be9da766a9ecid: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 59%

---

# Zielgruppenfilter für Reporting

Zielgruppenfilter (oder Zielgruppen) in [!DNL Adobe Target] sind Besuchergruppen, die ein bestimmtes Merkmal oder eine Reihe von Merkmalen gemeinsam haben.

Mit Zielgruppenfiltern geben Sie die Zielgruppen für die Berichterstellung an. Sie können eine Zielgruppe auswählen und ihre Leistung mit dem gesamten Traffic vergleichen. Sie möchten möglicherweise wissen, ob Ihre Gewinner bei den verschiedenen Traffic-Quellen im Vergleich zum gesamten Traffic unterschiedlich waren. Zielgruppenfilter helfen Ihnen, Zielgruppen zu finden, die möglicherweise auf verschiedene Inhalte ausgerichtet werden sollten. In vielen Fällen lässt sich ein Gewinner nicht dem gesamten Traffic zuordnen.

Zum Beispiel kann es sich bei Besuchern, die über eine bestimmte Suchmaschine zu Ihrer Webseite gelangen, um eine Zielgruppe handeln. Weitere Zielgruppen können z. B. auf Geschlecht, Alter, Standort, Registrierungsstatus, Kaufverlauf oder jedem weiteren beliebigen Detail basieren, das zu Besuchern erfasst werden kann. Nutzen Sie Zielgruppenfilter, um den Besucher-Traffic zu unterteilen und die Leistung des Erlebnisses für jedes Traffic-Segment zu vergleichen.

Berücksichtigen Sie bei der Planung der Verwendung von Zielgruppenfiltern für eine Aktivität die folgenden Richtlinien:

* **Besucher können sich in mehreren Zielgruppen befinden.** Wenn zwei Audiences eingerichtet sind (z. B. „neue Besucher“ und „Besucher aus Google„) und eine Person beide Kriterien erfüllt, wird diese Person in beiden Audiences gezählt und verfolgt. Daher stimmt die Summe der Besucher in den Zielgruppen nicht mit der Anzahl der Besucher in einer Aktivität überein.
* **Richten Sie Zielgruppen ein, bevor Sie die Aktivität starten.** Zielgruppendaten können nicht rückwirkend abgerufen werden. Wenn Sie Zielgruppenfilter nicht vor dem Start einer Aktivität konfigurieren und sich schließlich dazu entscheiden, diese einzusetzen, nachdem die Aktivität bereits eine bestimmte Zeit läuft, können Sie für die bereits vergangene Dauer der Aktivität keine Daten erfassen.
* **Beginnen Sie mit zwei bis vier Zielgruppen.** Fokussieren Sie sich auf grundlegenden Informationen, wie z. B. der Traffic-Quelle.
* **Benennen Sie Zielgruppen nach Bedarf um.** Sie können eine Zielgruppe umbenennen, ohne die Daten zu beeinflussen, damit der Name der Zielgruppe für die erfassten Ergebnisse aussagekräftiger wird, auch wenn die Aktivität aktiv ist.
* **Geben Sie genaue Werte ein.** Bei den Werten des Zielgruppenfilters wird zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie z. B. eine Zielgruppe verwenden, die eine Filterung von Städten vornimmt, müssen Sie eine „ODER“-Bedingung verwenden, um mögliche Variationen von Recht- und Großschreibung einzubeziehen, wie z. B. „Vienna“, „vienna“, „wien“ und „Wien“.
* **Aus der [!UICONTROL Audiences] Liste erstellte Zielgruppen sind wiederverwendbar.** Zielgruppen, die im Rahmen einer Aktivität erstellt wurden, können nicht wiederverwendet werden.

In den folgenden Abschnitten finden Sie weitere Informationen zum Einrichten von Zielgruppen und zur Berichterstellung:

| Aufgabe | Thema |
|--- |--- |
| Geeignete Aktivität oder geeigneten Test erstellen. | [Aktivitäten und Tests](/help/main/c-intro/target-key-concepts.md) |
| Zielgruppen erstellen, sofern erforderlich. | [Erstellen von Zielgruppen](/help/main/c-target/c-audiences/create-audience.md) |
| Mehrere Zielgruppen kombinieren, sofern erforderlich. | [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md) |
| Zielgruppen auf der Seite Ziele und Einstellungen der Aktivität anwenden. | A/B-Test: [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)<br>Automated Personalization: [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br>Experience Targeting: [Ziele und Einstellungen](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md)<br>Multivariater Test: [Ziele und Einstellungen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md)<br>Recommendations: [Recommendations-Aktivitätseinstellungen](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md)<br>Aktivitätseinstellungen: [Aktivitätseinstellungen](/help/main/c-activities/activity-settings.md) |
| Berichte mit Informationen zu den Zielgruppenfiltern anzeigen. | [Berichtseinstellungen](/help/main/c-reports/c-report-settings/report-settings.md) |
