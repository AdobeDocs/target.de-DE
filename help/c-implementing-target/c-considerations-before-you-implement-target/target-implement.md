---
keywords: document.write;Target;implementieren;Target implementieren;DTM;at.js;mbox.js;target.js;mbox;Adobe Experience Platform Web SKD;aep Web SDK;Web SDK
description: Implementieren Sie Adobe [!DNL Target] by referencing the [!DNL Target] -Bibliotheken (at.js oder mbox.js) auf Ihren Webseiten.
title: Erläuterung der  [!DNL Target] -JavaScript-Bibliotheken
feature: Implementierung
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 24%

---


# Erläuterung der [!DNL Target]-JavaScript-Bibliotheken

Implementieren Sie [!DNL Adobe Target] , indem Sie auf Ihren Webseiten auf die [!DNL Adobe Target]-Bibliotheken (Adobe Experience Platform Web SDK oder at.js) verweisen.

>[!NOTE]
>
>Die mbox.js-Bibliothek wird nicht mehr weiterentwickelt. Alle Kunden müssen vor dem 31. März 2021 von mbox.js zu at.js oder zum [!UICONTROL Adobe Experience Platform Web SDK] migrieren.

## Unterschiede zwischen den JavaScript-Bibliotheken [!DNL Target] {#section_40117C78C2F84FECAC4F1BA40CC4F171}

In der folgenden Tabelle werden die Unterschiede zwischen den JavaScript-Bibliotheken [!DNL Target] erläutert:

| Bibliotheksreferenz | Beschreibung |
|--- |--- |
| Adobe Experience Platform Web SDK | Mit dem [!UICONTROL Adobe Experience Platform Web SDK] können Sie über das Adobe Experience Edge Network mit den verschiedenen Diensten in [!DNL Experience Cloud] (einschließlich [!DNL Target]) interagieren. Wenn Sie eine Migration zu [!DNL Adobe Experience Platform Web SDK] vornehmen, finden Sie weitere Informationen unter [Was ist das Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) im *Web SDK Guide*. |
| at.js | at.js ersetzt mbox.js für [!DNL [!DNL Target]]-Implementierungen.<br>Neben anderen Vorteilen sorgt at.js für kürzere Ladezeiten von Seiten bei Webimplementierungen, bessere Sicherheit, Vermeidung von document.write-Warnungen in Google Chrome und bessere Implementierungsoptionen für Einzelseiten-Apps. |

## Auswirkung von at.js auf die Seitenladezeit {#section_16630CD0FF0A498EB596A51381366A5A}

Viele Kunden und Berater möchten wissen, wie sich [!DNL at.js] auf die Seitenladezeit auswirkt, insbesondere im Zusammenhang mit neuen und wiederkehrenden Benutzern. Leider ist es schwierig, zu messen, wie [!DNL at.js] die Seitenladezeit beeinflusst, und genaue Zahlen dazu anzugeben, wie  die Seitenladezeit aufgrund der Implementierung jedes Kunden beeinflusst.

Wenn die Besucher-API jedoch auf der Seite vorhanden ist, kann [!DNL Target] besser verstehen, wie [!DNL at.js] die Seitenladezeit beeinflusst.

>[!NOTE]
>
>Die Besucher-API und [!DNL at.js] wirken sich nur dann auf die Seitenladezeit aus, wenn Sie die globale Mbox verwenden (dies liegt an der Technik, mit der der Haupttext ausgeblendet wird). Regionale Mboxes sind von der Besucher-API-Integration nicht betroffen.

In den folgenden Abschnitten wird die Aktionssequenz für neue und zurückkehrende Besucher beschrieben:

### Neue Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. at.js wird geladen, analysiert und ausgeführt.
1. Wenn die automatische Erstellung einer globalen Mbox aktiviert ist, wird die JavaScript-Bibliothek [!DNL Target]:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die [!DNL Target]-Bibliothek versucht, [!UICONTROL Experience Cloud-Besucher-ID]-Daten abzurufen.
   * Bei einem neuen Besucher sendet die Besucher-API eine domänenübergreifende Anfrage an `demdex.net`.
   * Nachdem die Daten [!UICONTROL Experience Cloud-Besucher-ID] abgerufen wurden, wird eine Anforderung an Target ausgelöst.

### Zurückkehrende Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. at.js wird geladen, analysiert und ausgeführt.
1. Wenn die automatische Erstellung einer globalen Mbox aktiviert ist, wird die JavaScript-Bibliothek [!DNL Target]:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die [!DNL Target]-Bibliothek versucht, [!UICONTROL Experience Cloud-Besucher-ID]-Daten abzurufen.
   * Die Besucher-API ruft Cookie-Daten ab.
   * Nachdem die Daten [!UICONTROL Experience Cloud-Besucher-ID] abgerufen wurden, wird eine Anforderung an [!DNL Target] ausgelöst.

>[!NOTE]
>
>Wenn die Besucher-API vorhanden ist, wird [!DNL Target] bei neuen Besuchern mehrmals über den Draht geschaltet, um sicherzustellen, dass [!DNL Target]-Anforderungen [!UICONTROL Experience Cloud-Besucher-ID]-Daten enthalten. Bei wiederkehrenden Besuchern geht [!DNL Target] nur an [!DNL Target] vorbei, um den personalisierten Inhalt abzurufen.
