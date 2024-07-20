---
keywords: Umgebung; Fehlerbehebung; Best Practices; Ubox; Umleitungen; Umleitung; Whitelist; Blacklist; Blockierungsliste; Zulassungsliste
description: Erfahren Sie, wie Sie Umgebungen in Adobe [!DNL Target] verwenden können, um Ihre Sites und Umgebungen vor der Produktion zu organisieren, um die Verwaltung und die separate Berichterstellung zu erleichtern.
title: Was sind Umgebungen und wie wende ich sie an?
feature: Administration & Configuration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: 516d3969c8a6ed073b9f8d53c842e4d759cee8a2
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 49%

---

# Umgebungen

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

Zwecks einfacher Verwaltung werden Hosts in Umgebungen zusammengefasst. Es können beispielsweise mehrere Dutzend Hosts in zwei oder drei Umgebungen aufgeteilt werden. Zu den voreingestellten Umgebungen gehören [!UICONTROL Production], [!UICONTROL Staging] und [!UICONTROL Development]. Sie können nach Wunsch neue Umgebungen hinzufügen oder alte umbenennen.

Eine Umgebung, die Standardumgebung, heißt vorab [!UICONTROL Production]. Die Standardumgebung kann nicht gelöscht werden, auch nicht, wenn sie umbenannt wird. In [!DNL Target] wird angenommen, dass in dieser Gruppe fertiggestellte, genehmigte Aktivitäten und Tests bereitgestellt werden.

Wenn eine [!DNL Target] -Anfrage von neuen Websites oder Domänen empfangen wird, werden diese neuen Domänen immer in der [!UICONTROL Production] -Umgebung angezeigt. Die Einstellungen der [!UICONTROL Production] -Umgebung können nicht geändert werden. Unbekannte oder neue Sites sehen also garantiert nur Inhalte, die aktiv und bereit sind. Über die Hostverwaltung kann außerdem problemlos für die Qualität neuer Aktivitäten und Inhalte in der Testumgebung, Staging-Umgebung und Entwicklungsumgebung vor der Aktivierung der Aktivitäten gesorgt werden.

Klicken Sie zum Verwalten von Umgebungen auf **[!UICONTROL Administration]** > **[!UICONTROL Environments]**.

![Liste der Umgebungen](/help/main/administrating-target/assets/environments.png)

## Hinzufügen einer Umgebung {#section_32097D0993724DF3A202D164D3F18674}

1. Klicken Sie in der Liste [!UICONTROL Environments] auf **[!UICONTROL Add Environment]**.
1. Geben Sie einen beschreibenden Namen für die Umgebung an.
1. Geben Sie den gewünschten aktiven Modus für die Umgebung an: [!UICONTROL Active Activities] oder [!UICONTROL Active and Inactive Activities].

   Wenn Sie [!UICONTROL Active and Inactive Activities] angeben, zeigen Hosts aus dieser Umgebung auch inaktive Aktivitäten an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Festlegen der Standardumgebung für die Berichterstellung {#section_4F8539B07C0C45E886E8525C344D5FB0}

Sie können die Umgebung auswählen, die Sie als Standard für alle Aktivitätsberichte festlegen möchten.

Wenn Sie [!UICONTROL Production] als Standard verwenden, werden hier automatisch alle unbekannten Hosts hinzugefügt und die Berichtsdaten daraus werden in die standardmäßige Berichtsansicht aufgenommen. Die Erstellung einer „reinen“ Umgebung gewährleistet hingegen, dass ausschließlich Coresites/Domänen eingeschlossen werden.

So legen Sie die Standardumgebung für die Berichterstellung fest:

1. Klicken Sie in der Liste [!UICONTROL Environments] auf das Sternsymbol .

>[!NOTE]
>
>[!DNL Recommendations]-Benutzer müssen ihre Verhaltens- und Produktdatenbank neu erstellen, wenn Hosts die Hostgruppen wechseln.
>
>Wenn Sie eine [Standardumgebung in einem [!DNL Adobe Experience Platform] Datastream](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=en#target){target=_blank} angeben, überschreibt diese Einstellung die Einstellung in [!DNL Target].

## Ändern des Namens einer Umgebung {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klicken Sie in der Liste [!UICONTROL Environment] auf das Symbol **[!UICONTROL Edit]** .
1. Ändern Sie den Namen der Umgebung.
1. Klicken Sie auf **[!UICONTROL Save]**.

## Löschen einer Umgebung {#section_737F8869612047868D03FC755B1223D3}

Sie können eine Umgebung, die nicht mehr benötigt wird, löschen.

1. Klicken Sie in der Liste [!UICONTROL Environment] auf das Symbol **[!UICONTROL Delete]** .
1. Klicken Sie auf **[!UICONTROL Delete]** , um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Die Umgebung [!UICONTROL Production] kann nicht gelöscht werden, Sie können sie jedoch umbenennen.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."}

Sie können eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

{{premium-note}}

Eine Umgebung kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Verwendungen zu trennen. Sie können beispielsweise Hostgruppen für [!UICONTROL Development] - und [!UICONTROL Production] -Umgebungen, verschiedene Marken oder verschiedene geografische Regionen verwenden. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Mit dem Umgebungsfilter können Sie auch eine andere Hostgruppe auswählen, um die Ergebnisse in der Vorschau anzuzeigen.) Neu hinzugefügte Elemente sind standardmäßig in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wurde eine Umgebungs-ID angegeben.

>[!NOTE]
>
>Bereitgestellte Empfehlungen hängen von der Hostgruppe oder Umgebungs-ID ab, die in der Anfrage angegeben ist.


Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.

Der Filter [!UICONTROL Environment] ist an den folgenden Stellen in der Target-Benutzeroberfläche verfügbar:

* Katalogsuche ([!UICONTROL Recommendations > Catalog Search])
* Dialogfeld &quot;Sammlung erstellen&quot;([!UICONTROL Recommendations > Collections > Create New])
* Dialogfeld &quot;Sammlung aktualisieren&quot;([!UICONTROL Recommendations > Collections > Edit]
* Dialogfeld &quot;Ausschluss erstellen&quot;([!UICONTROL Recommendations > Exclusions > Create New])
* Dialogfeld &quot;Ausschluss aktualisieren&quot;([!UICONTROL Recommendations > Exclusions > Edit])
