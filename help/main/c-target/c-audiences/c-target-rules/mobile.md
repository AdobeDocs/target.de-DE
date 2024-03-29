---
keywords: Targeting; mobil; target mobile; deviceatlas; iPhone; iPhone-Modelle; deviceatlas; Displaybreite; Display Breite; Displayhöhe; Gerätetyp; Displayhöhe; Mobiltelefon; Tablet; Gerätemodell
description: Erfahren Sie, wie Sie Zielgruppen erstellen in [!DNL Adobe Target] , um Mobilgeräte als Ziel auszuwählen.
title: Kann ich Besucher basierend auf mobilen Optionen ansprechen?
feature: Audiences
exl-id: 73d5c80c-bfa2-4806-8c04-652781b70bf2
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 34%

---

# Mobile

Erstellen von Zielgruppen in [!DNL Adobe Target] , um Mobilgeräte auf Basis von Parametern wie Mobilgerät, Gerätetyp, Geräteanbieter, Bildschirmmaßen usw. auszuwählen.

So können Sie beispielsweise Benutzern, die Ihre Seite über ein Telefon besuchen, andere Inhalte anzeigen, als bei Besuchen auf einem Computer. In diesem Fall können Sie die [!UICONTROL Mobilnummer] Zielgruppe und wählen Sie dann die **[!UICONTROL Ist Mobiltelefon]** -Option. Sie können dann alle spezifischen Details hinzufügen, die für Sie wichtig sind, z. B. den Telefontyp, die Bildschirmgröße (in Pixel) usw.

Das mobile Targeting wird von [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester), einem Service von DotMobi bereitgestellt. DeviceAtlas ist eine umfassende Datenbank mobiler Geräte, die auf Daten beruht, die aus zahlreichen Quellen zusammengefasst wurden, einschließlich von Herstellern und Netzwerkbetreibern. Diese Daten wurden dann geprüft, referenziert und validiert, um eine große, genaue Datenbank der verfügbaren mobilen Geräte zu erstellen.

Für die Geräteerkennung werden die User-Agent-Zeichenfolgen analysiert. Einige Gerätehersteller, z. B. Apple, deaktivieren diese Funktion, indem sie in den User-Agent-Zeichenfolgen keine ausreichenden Informationen bereitstellen.

Apple-Geräte übermitteln beispielsweise in den UA-Daten keine gerätespezifischen Token. Das Ergebnis ist, dass es nicht möglich ist, iPhone-Modelle (wie iPhone 12 Pro, iPhone 12, iPhone 11 Pro Max usw.) mithilfe einer einfachen schlüsselwortbasierten Methode zu erkennen.

Um dieses Problem zu lösen, [!DNL Target] erfasst zusätzliche Daten, um iPhones und andere Apple-Geräte mithilfe der folgenden Parameter genau zu erkennen:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| devicePixelRatio | Zeichenfolge | Verhältnis zwischen physischen Pixeln und geräteunabhängigen Pixeln (Dips) im Browser. Beispiel: &quot;1.5&quot;oder &quot;2&quot; |
| screenOrientation | Zeichenfolge | Das Gerät und die JavaScript-Engine des Browsers unterstützen die Bildschirmdrehung. Mögliche Werte: Querformat oder Hochformat. |
| webGLRenderer | Zeichenfolge | Browser-Renderer des Grafiktreibers. |

>[!NOTE]
>
>Kunden, die das Mobile SDK verwenden, müssen nichts unternehmen, um diese Funktion anzuwenden. Kunden, die at.js verwenden, müssen [Aktualisierung auf at.js , Version 1.5.0](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} (oder höher).

Sie können mehr als eine Geräteeigenschaft auswählen. Mehrere Auswahlen werden mit einem ODER-Operator verbunden.

Kunden, die eine benutzerspezifische Integration (also weder at.js noch das Mobile SDK) verwenden, können diese Parameter selbst erfassen und als Mbox-Parameter übergeben.

1. Im [!DNL Target] Benutzeroberfläche, klicken Sie auf **[!UICONTROL Zielgruppen]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Drag &amp; Drop **[!UICONTROL Mobilnummer]** in den Audience Builder-Bereich.
1. Klicken Sie auf **[!UICONTROL Auswählen]** und wählen Sie anschließend eine der folgenden Optionen aus:

   * Gerätemarketingbezeichnung
   * Gerätemodell
   * Gerätehersteller
   * Ist Mobilgerät
   * Ist Mobiltelefon
   * Ist Tablet
   * Betriebssystem
   * Bildschirmhöhe (px)
   * Bildschirmbreite (px)

   >[!NOTE]
   >
   >Sie können das Targeting nach Mobilnetzbetreiber mithilfe der [Geo-Einstellungen](/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670) vornehmen.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

Die folgende Abbildung zeigt eine Zielgruppe, die Besucher auswählt, die von Google hergestellte Geräte und Mobilgeräte verwenden.

![Zielgruppe mit Mobilgeräten](assets/target_mobile.png)

## Zu beachten

Beachten Sie beim Targeting von Mobilgeräten die folgenden Informationen:

### Targeting-Geräte mit iOS 12.2 oder höher

Aufgrund der neuen Änderungen, die in iOS 12.2 eingeführt wurden, erstellen Sie eine Zielgruppe mit Regeln, die durch [!UICONTROL Gerätemarketingname] und [!UICONTROL Gerätemodell] , die iPhone-Modelle angeben, ist betroffen. [!DNL Target] Benutzer, die iPhones mit iOS 12.2 (oder höher) installiert haben, können nicht mehr als Ziel ausgewählt werden. Wenn diese Benutzer jedoch nicht über iOS 12.2 (oder höher) verfügen, funktioniert das iPhone-Modell-Targeting weiterhin ordnungsgemäß.

Die Aktualisierung von iOS 12.2 (oder höher) wirkt sich nicht auf die Identifizierung der folgenden Modelle aus, da diese Modelle die Aktualisierung auf iOS 12.2 nicht unterstützen: iPhone, iPhone 3G, iPhone 3GS, iPhone 4, iPhone 4s, iPhone 5, iPhone 5c, iPad, iPad 2, iPad/Retina Display, iPad Retina (4th Generation), iPod Touch 4 und iPod Touch 5.

### Targeting-Geräte mit Safari 14.0.2 (oder höher)

Wenn Sie mobile Regeln für Geräte verwenden, auf denen Safari Version 14.0.2 (oder höher) in macOS ausgeführt wird, aufgrund eines bekannten Problems mit den Benutzeragenten und DeviceAtlas von Apple, [!DNL Target] identifiziert Safari auf Mac- und iPad-Geräten falsch. Dieses Problem wird in Zukunft angesprochen werden.

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
