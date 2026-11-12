---
keywords: Aktivitäts-URL;URL;andere URL
description: Erfahren Sie, wie Sie die [!UICONTROL Aktivitäts-URL] in einer A/B-, Erlebnis-Targeting- oder Multivarianz-Test-Aktivität festlegen, um Testseiten zu definieren und ein korrektes Testdesign sicherzustellen.
title: Was ist die Aktivitäts-URL in einer A/B-, Erlebnis-Targeting- oder Multivarianz-Test-Aktivität?
feature: A/B Tests
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
reason: republish
TQID: 'https://experienceleague.adobe.com/arQWsSfBKYtrayq9AI8ejU1T-Uor-oL5j2Sp2JKKXZE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: aad553690f1f399177214c94a2276d038f46d9cb
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 25%
---
# Aktivitäts-URL {#ab-activity-url}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie die Aktivitäts-URL einer A/B-, Experience Targeting (XT)- oder Multivarianz-Test (MVT)-Aktivität angeben, wie Sie eine andere Seite anzeigen und wie Sie Regeln für weitere Seiten oder Abschnitte hinzufügen.

>[!ENDSHADEBOX]

Die [!UICONTROL Aktivitäts-URL] bestimmt die Seite, die in der Aktivität verwendet wird. Diese Seite wird in [!UICONTROL Visual Experience Composer] (VEC) oder im [!UICONTROL Form-Based Experience Composer) geöffnet] wenn die Aktivität in [!DNL Adobe Target] entworfen wird.

## Angeben der Aktivitäts-URL {#specify-url}

Geben Sie die Aktivitäts-URL ein, wenn Sie während der Erstellung der Aktivität dazu aufgefordert werden. Geben Sie die vollständige URL ein (einschließlich `https://`) und klicken Sie dann auf **[!UICONTROL Erstellen]**.

>[!NOTE]
>
>[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://www.adobe.com`] überein.

Wenn Sie eine URL für eine Site angeben, die nicht die [!DNL Target]at.js[JavaScript-Bibliothek oder  [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank} enthält, können Sie keine Seitenelemente auswählen.

## Eine andere Seite anzeigen {#different-page}

Standardmäßig öffnet der VEC oder der [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) die Seite, die in Ihren Einstellungen von [Visual Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md) angegeben ist. Sie können während der Erstellung der Aktivität eine andere Seite angeben.

So zeigen Sie nach dem Öffnen des VEC eine andere Seite an:

1. Klicken Sie **[!UICONTROL der]** oben auf der Seite auf **[!UICONTROL Konfigurieren]** und wählen Sie dann **[!UICONTROL Seitenbereitstellung]** aus.

1. Geben Sie die URL im Feld **[!UICONTROL URL]** an.

1. Klicken Sie auf **[!UICONTROL „Speichern“]**, wenn Sie damit fertig sind.

Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können **[!UICONTROL Rendern mit JavaScript&quot; deaktivieren]** wenn Sie diese Elemente mithilfe des VEC ändern möchten.

>[!NOTE]
>
>Wenn Sie die URL ändern, nachdem Sie für ein oder mehrere Erlebnisse Änderungen auf der Seite vorgenommen haben, wird das Erlebnis bei der Verwendung der neuen Seite zurückgesetzt und die vorgenommenen Änderungen gehen verloren.

## Hinzufügen von Regeln für weitere Seiten oder Abschnitte {#add-rules}

Um der Aktivität weitere Seiten oder Abschnitte hinzuzufügen, klicken Sie in den Einstellungen für **[!UICONTROL Seitenbereitstellung]** auf **[!UICONTROL Regel hinzufügen]** und anschließend auf **[!UICONTROL Speichern]**, wenn Sie fertig sind.

Zusätzliche Regeln können auf Folgendem basieren:

* URL
* Domain
* Pfad
* Hashfragment (#)
* Abfrage
* Parameter „mbox“
* Benutzerdefiniert

Zusätzliche Regeln können mit UND oder ODER mit der Aktivitäts-URL verbunden werden. Alle hinzugefügten Regeln werden per „AND“ miteinander verglichen.
