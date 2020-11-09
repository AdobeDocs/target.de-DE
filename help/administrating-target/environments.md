---
keywords: environment;troubleshooting;best practices;ubox;redirects;redirect;whitelist;blacklist;blocklist;allowlist
description: Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.
title: Umgebung
feature: hosts and environments
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 67%

---


# Umgebung

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

Zwecks einfacher Verwaltung werden Hosts in Umgebungen zusammengefasst. Es können beispielsweise mehrere Dutzend Hosts in zwei oder drei Umgebungen aufgeteilt werden. The preset environments include [!UICONTROL Production], [!UICONTROL Staging], and [!UICONTROL Development]. Sie können nach Wunsch neue Umgebungen hinzufügen oder alte umbenennen.

One environment, the default environment, is pre-named [!UICONTROL Production]. Die Standardumgebung kann nicht gelöscht werden, auch nicht, wenn sie umbenannt wird. In [!DNL Target] wird angenommen, dass in dieser Gruppe fertiggestellte, genehmigte Aktivitäten und Tests bereitgestellt werden.

When a [!DNL Target] request is received from new websites or domains, these new domains always appear in the [!UICONTROL Production] environment. The [!UICONTROL Production] environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. Über die Hostverwaltung kann außerdem problemlos für die Qualität neuer Aktivitäten und Inhalte in der Testumgebung, Staging-Umgebung und Entwicklungsumgebung vor der Aktivierung der Aktivitäten gesorgt werden.

Um Umgebung zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Umgebung]**.

![Liste der Umgebung](/help/administrating-target/assets/environments.png)

## hinzufügen einer Umgebung {#section_32097D0993724DF3A202D164D3F18674}

1. Klicken Sie in der Liste [!UICONTROL Umgebung] auf **[!UICONTROL Hinzufügen Umgebung]**.
1. Geben Sie einen beschreibenden Namen für die Umgebung an.
1. Legen Sie den aktiven Modus für die Umgebung fest: [!UICONTROL Aktive Aktivitäten] oder [!UICONTROL aktive und inaktive Aktivitäten].
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Set the default environment for reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

Sie können die Umgebung auswählen, die Sie als Standard für alle Aktivitätsberichte festlegen möchten.

If you use [!UICONTROL Production] as your default, all unknown hosts automatically are added here and report data from there is included in the default report view. Die Erstellung einer „reinen“ Umgebung gewährleistet hingegen, dass ausschließlich Coresites/Domänen eingeschlossen werden.

So legen Sie die Standardumgebung für die Berichterstellung fest:

1. Klicken Sie in der Liste [!UICONTROL Umgebung] auf das Symbol Stern

>[!NOTE]
>
>[!DNL Recommendations]-Benutzer müssen ihre Verhaltens- und Produktdatenbank neu erstellen, wenn Hosts die Hostgruppen wechseln.

## Change the name of an environment {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klicken Sie in der Liste [!UICONTROL Umgebung] auf das Symbol **[!UICONTROL Bearbeiten]** .
1. Ändern Sie den Namen der Umgebung.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Delete an environment {#section_737F8869612047868D03FC755B1223D3}

Sie können eine Umgebung, die nicht mehr benötigt wird, löschen.

1. Klicken Sie in der Liste [!UICONTROL Umgebung] auf das Symbol **[!UICONTROL Löschen]** .
1. Klicken Sie auf **[!UICONTROL Löschen]**, um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>You cannot delete the [!UICONTROL Production] environment, but you can rename it.

## Recommendations: Sammlungen und Ausschlüsse nach Umgebung (Hostgruppe) filtern

![Premium-Zeichen](/help/assets/premium.png)

Sie können eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>
>Recommendations activities are available as part of the [!DNL Target] Premium solution. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.

Eine Umgebung kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Zwecke zu trennen. For example, you can use host groups for [!UICONTROL Development] and [!UICONTROL Production] environments, different brands, or different geographies. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Mit dem Umgebungsfilter können Sie auch eine andere Hostgruppe auswählen, um die Ergebnisse in der Vorschau anzuzeigen.) Neu hinzugefügte Elemente sind standardmäßig in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wurde eine Umgebungs-ID angegeben. Bereitgestellte Empfehlungen hängen von der in der Anfrage angegebenen Hostgruppe ab.

Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.

The [!UICONTROL Environment] filter is available from the following places in the Target UI:

* Katalogsuche ([!UICONTROL Recommendations > Katalogsuche])
* Dialogfeld „Sammlung erstellen“ ([!UICONTROL Recommendations > Sammlungen > Neu erstellen])
* Dialogfeld „Sammlung aktualisieren“ ([!UICONTROL Recommendations > Sammlungen > Bearbeiten])
* Dialogfeld „Ausschluss erstellen“ ([!UICONTROL Recommendations > Ausschlüsse > Neu erstellen])
* Dialogfeld „Ausschluss aktualisieren“ ([!UICONTROL Recommendations > Ausschlüsse > Bearbeiten])