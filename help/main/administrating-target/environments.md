---
keywords: Umgebung;Fehlerbehebung;Best Practices;ubox;umleitungen;umleiten;Whitelist;Blacklist;Blockierungsliste auf die Zulassungsliste setzte
description: Erfahren Sie, wie Sie Umgebungen in Adobe [!DNL Target]  verwenden, um Ihre Sites und Vorproduktionsumgebungen zu organisieren und so eine einfache Verwaltung und getrennte Berichterstellung zu ermöglichen.
title: Was sind Umgebungen und wie verwende ich sie?
feature: Administration & Configuration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: 484971ab0fcd07205935c0fef3ea1484f40c3e96
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 47%

---

# Umgebungen

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

Zwecks einfacher Verwaltung werden Hosts in Umgebungen zusammengefasst. Es können beispielsweise mehrere Dutzend Hosts in zwei oder drei Umgebungen aufgeteilt werden. Zu den voreingestellten Umgebungen gehören [!UICONTROL Production], [!UICONTROL Staging] und [!UICONTROL Development]. Sie können nach Wunsch neue Umgebungen hinzufügen oder alte umbenennen.

Eine Umgebung, die Standardumgebung, ist [!UICONTROL Production] vorbenannt. Die Standardumgebung kann nicht gelöscht werden, auch nicht, wenn sie umbenannt wird. In [!DNL Target] wird angenommen, dass in dieser Gruppe fertiggestellte, genehmigte Aktivitäten und Tests bereitgestellt werden.

Wenn eine [!DNL Target] Anfrage von neuen Websites oder Domains empfangen wird, erscheinen diese neuen Domains immer in der [!UICONTROL Production]. Die Einstellungen der [!UICONTROL Production]-Umgebung können nicht geändert werden, sodass unbekannte oder neue Sites garantiert nur aktive und fertige Inhalte sehen. Über die Hostverwaltung kann außerdem problemlos für die Qualität neuer Aktivitäten und Inhalte in der Testumgebung, Staging-Umgebung und Entwicklungsumgebung vor der Aktivierung der Aktivitäten gesorgt werden.

Um Umgebungen zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Environments]**.

## Hinzufügen einer Umgebung {#section_32097D0993724DF3A202D164D3F18674}

1. Klicken Sie in der [!UICONTROL Environments] auf **[!UICONTROL Add Environment]**.
1. Geben Sie einen beschreibenden Namen für die Umgebung an.
1. Geben Sie den gewünschten aktiven Modus für die Umgebung an: [!UICONTROL Active Activities] oder [!UICONTROL Active and Inactive Activities].

   Wenn Sie [!UICONTROL Active and Inactive Activities] angeben, zeigen Hosts aus dieser Umgebung auch inaktive Aktivitäten an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Festlegen der Standardumgebung für das Reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

Sie können die Umgebung auswählen, die Sie als Standard für alle Aktivitätsberichte festlegen möchten.

Wenn Sie [!UICONTROL Production] als Standard verwenden, werden alle unbekannten Hosts automatisch hier hinzugefügt und die Berichtsdaten von dort werden in die standardmäßige Berichtsansicht aufgenommen. Die Erstellung einer „reinen“ Umgebung gewährleistet hingegen, dass ausschließlich Coresites/Domänen eingeschlossen werden.

So legen Sie die Standardumgebung für die Berichterstellung fest:

1. Klicken Sie in der [!UICONTROL Environments] auf das Sternsymbol

>[!NOTE]
>
>[!DNL Recommendations]-Benutzer müssen ihre Verhaltens- und Produktdatenbank neu erstellen, wenn Hosts die Hostgruppen wechseln.
>
>Wenn Sie eine [Standardumgebung in einem Datenstrom [!DNL Adobe Experience Platform]  angeben](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=en#target){target=_blank} überschreibt diese Einstellung die Einstellung in [!DNL Target].

## Ändern des Namens einer Umgebung {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klicken Sie in der [!UICONTROL Environment] auf das Symbol **[!UICONTROL Edit]** .
1. Ändern Sie den Namen der Umgebung.
1. Klicken Sie auf **[!UICONTROL Save]**.

## Löschen einer Umgebung {#section_737F8869612047868D03FC755B1223D3}

Sie können eine Umgebung, die nicht mehr benötigt wird, löschen.

1. Klicken Sie in der [!UICONTROL Environment] auf das Symbol **[!UICONTROL Delete]** .
1. Klicken Sie auf **[!UICONTROL Delete]** , um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Sie können die [!UICONTROL Production] Umgebung nicht löschen, aber Sie können sie umbenennen.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."}

Sie können eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

{{premium-note}}

Eine Umgebung kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Verwendungszwecke zu trennen. Sie können beispielsweise Hostgruppen für [!UICONTROL Development] und [!UICONTROL Production] Umgebungen, verschiedene Marken oder verschiedene Regionen verwenden. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Sie können auch eine andere Hostgruppe auswählen, um Ergebnisse in der Vorschau anzuzeigen, indem Sie den Umgebungsfilter verwenden.) Standardmäßig sind neu hinzugefügte Elemente in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wird eine Umgebungs-ID angegeben.

>[!NOTE]
>
>Die gesendeten Empfehlungen hängen von der in der Anfrage angegebenen Hostgruppen- oder Umgebungs-ID ab.


Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.

Der [!UICONTROL Environment] ist an den folgenden Stellen in der Target-Benutzeroberfläche verfügbar:

* Katalogsuche ([!UICONTROL Recommendations > Catalog Search])
* Dialogfeld Sammlung erstellen ([!UICONTROL Recommendations > Collections > Create New])
* Dialogfeld Sammlung aktualisieren ([!UICONTROL Recommendations > Collections > Edit])
* Dialogfeld „Ausschluss erstellen“ ([!UICONTROL Recommendations > Exclusions > Create New])
* Dialogfeld „Ausschluss aktualisieren“ ([!UICONTROL Recommendations > Exclusions > Edit])
