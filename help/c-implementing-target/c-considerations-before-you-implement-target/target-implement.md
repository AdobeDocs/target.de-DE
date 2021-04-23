---
keywords: Dokument.write;Zielgruppe;implementieren;Zielgruppe implementieren;dtm;dynamisches Tag-Management;at.js;mbox.js;Zielgruppe.js;mbox;adobe experience platform web skd;aep web sdk;web sdk
description: Implementieren Sie Adoben [!DNL Target] by referencing the [!DNL Target] Bibliotheken (at.js oder mbox.js) auf Ihren Webseiten.
title: Erläuterung der  [!DNL Target] -JavaScript-Bibliotheken
feature: Implementierung
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 23%

---


# Erläuterung der [!DNL Target]-JavaScript-Bibliotheken

Implementieren Sie [!DNL Adobe Target], indem Sie auf die Bibliotheken [!DNL Adobe Target] (Adobe Experience Platform Web SDK oder at.js) auf Ihren Webseiten verweisen.

>[!NOTE]
>
>Die mbox.js-Bibliothek wird nicht mehr weiterentwickelt. Alle Kunden müssen vor dem 31. März 2021 von &quot;mbox.js&quot;zu &quot;at.js&quot;oder zum [!UICONTROL Adobe Experience Platform Web SDK] migrieren. Weitere Informationen finden Sie unter [Migration von &quot;mbox.js&quot;zu &quot;at.js&quot;oder [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)

## Unterschiede zwischen den [!DNL Target] JavaScript-Bibliotheken {#section_40117C78C2F84FECAC4F1BA40CC4F171}

In der folgenden Tabelle werden die Unterschiede zwischen den JavaScript-Bibliotheken [!DNL Target] erläutert:

| Bibliotheksreferenz | Beschreibung |
|--- |--- |
| Adobe Experience Platform Web SDK | Mit dem [!UICONTROL Adobe Experience Platform Web SDK] können Sie über das Adobe Experience Edge Network mit den verschiedenen Diensten im [!DNL Experience Cloud] (einschließlich [!DNL Target]) interagieren. Wenn Sie eine Migration zu [!DNL Adobe Experience Platform Web SDK] vornehmen, finden Sie weitere Informationen unter [Was ist Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) im *Web SDK Guide*. |
| at.js  | &quot;at.js&quot;ersetzt &quot;mbox.js&quot;für [!DNL [!DNL Target]]-Implementierungen.<br>Neben anderen Vorteilen sorgt at.js für kürzere Ladezeiten von Seiten bei Webimplementierungen, bessere Sicherheit, Vermeidung von document.write-Warnungen in Google Chrome und bessere Implementierungsoptionen für Einzelseiten-Apps.<br>Weitere Informationen finden Sie unter [„at.js“-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md). |

## Auswirkungen von at.js auf die Seitenladezeit {#section_16630CD0FF0A498EB596A51381366A5A}

Viele Kunden und Berater möchten wissen, wie sich [!DNL at.js] auf die Seitenladezeit auswirkt, insbesondere im Zusammenhang mit neuen oder wiederkehrenden Benutzern. Leider ist es schwer zu messen und konkrete Zahlen darüber anzugeben, wie [!DNL at.js] die Seitenladezeit aufgrund der Implementierung jedes Kunden beeinflusst.

Wenn die Besucher-API jedoch auf der Seite vorhanden ist, kann [!DNL Target] besser verstehen, wie [!DNL at.js] die Seitenladezeit beeinflusst.

>[!NOTE]
>
>Die Besucher-API und [!DNL at.js] wirken sich nur dann auf die Seitenladezeit aus, wenn Sie die globale Mbox verwenden (aufgrund der Bodhiding-Technik). Regionale Mboxes sind von der Besucher-API-Integration nicht betroffen.

In den folgenden Abschnitten wird die Aktionssequenz für neue und zurückkehrende Besucher beschrieben:

### Neue Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. &quot;at.js&quot;wird geladen, analysiert und ausgeführt.
1. Wenn die automatische Erstellung einer globalen Mbox aktiviert ist, wird die JavaScript-Bibliothek [!DNL Target] wie folgt aktualisiert:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die [!DNL Target]-Bibliothek versucht, [!UICONTROL Experience Cloud-Besucher-ID]-Daten abzurufen.
   * Bei einem neuen Besucher löst die Besucher-API eine domänenübergreifende Anforderung an `demdex.net` aus.
   * Nachdem [!UICONTROL Experience Cloud-Besucher-ID]-Daten abgerufen wurden, wird eine Anfrage zur Zielgruppe ausgelöst.

### Zurückkehrende Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. &quot;at.js&quot;wird geladen, analysiert und ausgeführt.
1. Wenn die automatische Erstellung einer globalen Mbox aktiviert ist, wird die JavaScript-Bibliothek [!DNL Target] wie folgt aktualisiert:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die [!DNL Target]-Bibliothek versucht, [!UICONTROL Experience Cloud-Besucher-ID]-Daten abzurufen.
   * Die Besucher-API ruft Cookie-Daten ab.
   * Nachdem [!UICONTROL Experience Cloud-Besucher-ID]-Daten abgerufen wurden, wird eine Anforderung an [!DNL Target] ausgelöst.

>[!NOTE]
>
>Bei neuen Besuchern, bei denen die Besucher-API vorhanden ist, wird [!DNL Target] mehrmals über den Draht gesendet, um sicherzustellen, dass [!DNL Target]-Anforderungen [!UICONTROL Experience Cloud-Besucher-ID]-Daten enthalten. Bei zurückkehrenden Besuchern wird [!DNL Target] nur nach [!DNL Target] übergeben, um den personalisierten Inhalt abzurufen.
