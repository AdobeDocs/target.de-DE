---
description: Adobe Target wird mithilfe der JavaScript-Bibliothek „at.js“ oder „mbox.js“ in Ihre Webseiten integriert.
keywords: Targeting; Cookie; Erstanbieter-Cookie; Erstanbietercookie
seo-description: Adobe Target wird mithilfe der JavaScript-Bibliothek „at.js“ oder „mbox.js“ in Ihre Webseiten integriert.
seo-title: Funktionsweise von Targeting
solution: Target
title: Funktionsweise von Targeting
uuid: 8b5a36c0-555d-42c5-8b24-c08d07440a53
translation-type: tm+mt
source-git-commit: 74a6f402bc0c9dae6f89cbdb632d7dbc53743593

---


# Funktionsweise von Targeting{#how-targeting-works}

Adobe Target wird mithilfe der JavaScript-Bibliothek „at.js“ oder „mbox.js“ in Ihre Webseiten integriert.

[!DNL Target Classic] verwendet Mboxes für jeden Bereich Ihrer Seite, in dem Sie zielgerichtete Inhalte anzeigen oder Daten erfassen möchten. Diese Mboxes sind in [!DNL Target Standard] nicht erforderlich. Zum Ausführen Ihrer Optimierungsaktivitäten benötigen Sie stattdessen nur eine [JavaScript-Bibliothek](../c-implementing-target/c-considerations-before-you-implement-target/target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB), auf die auf jeder Seite verwiesen wird.

Jedes Mal, wenn ein Besucher eine [!DNL Target]-aktivierte Seite anfordert, verwendet Target den folgenden Prozess zur Bereitstellung von Angeboten:

1. Ein Kunde ruft eine Seite von Ihrem Server auf und zeigt sie im Browser an.
1. Ein Erstanbieter-Cookie wird im Browser des Kunden eingerichtet, um eine Unique Visitor-ID festzulegen.

   Ein [!DNL Experience Cloud visitor ID] wird auch dann festgelegt, wenn Sie das Master-Marketing-Profil verwenden.

1. Die Seite führt entweder über die Datei [!DNL Target] oder eine Mbox auf Ihrer Seite einen [!DNL target.js]-Aufruf durch.
1. [!DNL Target] referenziert das dem Besucher zugehörige Profil.
1. [!DNL Target] führt zu diesem Profil zugehörige Profilskripte aus.
1. [!DNL Target] berechnet die Antwort.
1. Inhalte werden basierend auf Ihren Aktivitäts- oder Kampagnenregeln angezeigt.

Das Angebot, das in einem Basis-A/B-Test angezeigt wird, wird per Zufall ausgewählt. Als Folge dieser zufälligen Trennung des Traffic kann es anfänglich zu einem hohen Traffic-Aufkommen kommen, bevor sich die Prozentwerte ausgleichen. Wenn Sie beispielsweise eine Aktivität mit zwei Erlebnissen haben, wird das Anfangserlebnis per Zufall ausgewählt. Bei wenig Traffic besteht die Möglichkeit, dass der Prozentsatz von Besuchern auf ein Erlebnis ausgerichtet wird. Mit zunehmendem Traffic sollten sich die Prozentsätze langsam angleichen.
