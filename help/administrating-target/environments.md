---
keywords: Umgebung; Fehlerbehebung; Best Practices; Ubox; Umleitungen; Umleitung; Whitelist; Blacklist; Blockierungsliste; Zulassungsliste
description: Erfahren Sie, wie Sie Umgebungen in Adobe [!DNL Target] verwenden können, um Ihre Sites und Umgebungen vor der Produktion zu organisieren und so eine einfache Verwaltung und separate Berichterstattung zu ermöglichen.
title: Was sind Umgebungen und wie wende ich sie an?
feature: Administration und Konfiguration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: be7b5478006af231aae2b78e4a8c0066e3cb4a5b
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 61%

---

# Umgebungen

Optimieren Sie Ihre Sites und Umgebungen für Schritte vor der Produktion für einfache Verwaltung und separate Berichterstattung.

Zwecks einfacher Verwaltung werden Hosts in Umgebungen zusammengefasst. Es können beispielsweise mehrere Dutzend Hosts in zwei oder drei Umgebungen aufgeteilt werden. Zu den voreingestellten Umgebungen gehören [!UICONTROL Produktion], [!UICONTROL Staging] und [!UICONTROL Entwicklung]. Sie können nach Wunsch neue Umgebungen hinzufügen oder alte umbenennen.

Eine Umgebung, die Standardumgebung, heißt vorab [!UICONTROL Produktion]. Die Standardumgebung kann nicht gelöscht werden, auch nicht, wenn sie umbenannt wird. In [!DNL Target] wird angenommen, dass in dieser Gruppe fertiggestellte, genehmigte Aktivitäten und Tests bereitgestellt werden.

Wenn eine [!DNL Target] -Anforderung von neuen Websites oder Domänen empfangen wird, werden diese neuen Domänen immer in der Umgebung [!UICONTROL Produktion] angezeigt. Die Einstellungen der Umgebung [!UICONTROL Produktion] können nicht geändert werden. Unbekannte oder neue Sites sehen also garantiert nur Inhalte, die aktiv und bereit sind. Über die Hostverwaltung kann außerdem problemlos für die Qualität neuer Aktivitäten und Inhalte in der Testumgebung, Staging-Umgebung und Entwicklungsumgebung vor der Aktivierung der Aktivitäten gesorgt werden.

Um Umgebungen zu verwalten, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Umgebungen]**.

![Umgebungsliste](/help/administrating-target/assets/environments.png)

## Hinzufügen einer Umgebung {#section_32097D0993724DF3A202D164D3F18674}

1. Klicken Sie in der Liste [!UICONTROL Umgebungen] auf **[!UICONTROL Umgebung hinzufügen]**.
1. Geben Sie einen beschreibenden Namen für die Umgebung an.
1. Legen Sie den aktiven Modus für die Umgebung fest: [!UICONTROL Aktive Aktivitäten] oder [!UICONTROL aktive und inaktive Aktivitäten].

   Wenn Sie [!UICONTROL Aktive und inaktive Aktivitäten] angeben, zeigen Hosts aus dieser Umgebung auch inaktive Aktivitäten an.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Festlegen der Standardumgebung für die Berichterstellung {#section_4F8539B07C0C45E886E8525C344D5FB0}

Sie können die Umgebung auswählen, die Sie als Standard für alle Aktivitätsberichte festlegen möchten.

Wenn Sie [!UICONTROL Produktion] als Standard verwenden, werden hier automatisch alle unbekannten Hosts hinzugefügt und Berichtsdaten von dort sind in der standardmäßigen Berichtsansicht enthalten. Die Erstellung einer „reinen“ Umgebung gewährleistet hingegen, dass ausschließlich Coresites/Domänen eingeschlossen werden.

So legen Sie die Standardumgebung für die Berichterstellung fest:

1. Klicken Sie in der Liste [!UICONTROL Umgebungen] auf das Sternsymbol

>[!NOTE]
>
>[!DNL Recommendations]-Benutzer müssen ihre Verhaltens- und Produktdatenbank neu erstellen, wenn Hosts die Hostgruppen wechseln.

## Ändern des Namens einer Umgebung {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klicken Sie in der Liste [!UICONTROL Umgebung] auf das Symbol **[!UICONTROL Bearbeiten]** .
1. Ändern Sie den Namen der Umgebung.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Löschen einer Umgebung {#section_737F8869612047868D03FC755B1223D3}

Sie können eine Umgebung, die nicht mehr benötigt wird, löschen.

1. Klicken Sie in der Liste [!UICONTROL Umgebung] auf das Symbol **[!UICONTROL Löschen]** .
1. Klicken Sie auf **[!UICONTROL Löschen]**, um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Die Umgebung [!UICONTROL Produktion] kann nicht gelöscht werden, Sie können sie jedoch umbenennen.

## Recommendations: Sammlungen und Ausschlüsse nach Umgebung (Hostgruppe) filtern

![Premium-Zeichen](/help/assets/premium.png)

Sie können eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>
>Recommendations-Aktivitäten sind als Bestandteil der Premium-Lösung [!DNL Target] verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.

Eine Umgebung kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Verwendungen zu trennen. Sie können beispielsweise Hostgruppen für [!UICONTROL Entwicklung] und [!UICONTROL Produktion]-Umgebungen, verschiedene Marken oder unterschiedliche geografische Regionen verwenden. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Mit dem Umgebungsfilter können Sie auch eine andere Hostgruppe auswählen, um die Ergebnisse in der Vorschau anzuzeigen.) Neu hinzugefügte Elemente sind standardmäßig in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wurde eine Umgebungs-ID angegeben. Bereitgestellte Empfehlungen hängen von der in der Anfrage angegebenen Hostgruppe ab.

Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.

>[!NOTE]
>Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.

Der Filter [!UICONTROL Umgebung] ist an den folgenden Stellen in der Target-Benutzeroberfläche verfügbar:

* Katalogsuche ([!UICONTROL Recommendations > Katalogsuche])
* Dialogfeld „Sammlung erstellen“ ([!UICONTROL Recommendations > Sammlungen > Neu erstellen])
* Dialogfeld „Sammlung aktualisieren“ ([!UICONTROL Recommendations > Sammlungen > Bearbeiten])
* Dialogfeld „Ausschluss erstellen“ ([!UICONTROL Recommendations > Ausschlüsse > Neu erstellen])
* Dialogfeld „Ausschluss aktualisieren“ ([!UICONTROL Recommendations > Ausschlüsse > Bearbeiten])
