---
keywords: Targeting; mobil; target mobile; deviceatlas; iPhone; iPhone-Modelle; deviceatlas; Displaybreite; Display Breite; Displayhöhe; Gerätetyp; Displayhöhe; Mobiltelefon; Tablet; Gerätemodell
description: Erfahren Sie, wie Sie in [!DNL Adobe Target] Zielgruppen für Mobilgeräte erstellen.
title: Kann ich Besucher basierend auf mobilen Optionen ansprechen?
feature: Audiences
exl-id: 73d5c80c-bfa2-4806-8c04-652781b70bf2
source-git-commit: 1ad86925fb18df469fd1b80205f29f79a20ce4b6
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 40%

---

# Mobil

Erstellen Sie Zielgruppen in [!DNL Adobe Target], um Mobilgeräte auf Basis von Parametern wie Mobilgerät, Gerätetyp, Geräteanbieter, Bildschirmmaßen und mehr als Ziel auszuwählen.

So können Sie beispielsweise Benutzern, die Ihre Seite über ein Telefon besuchen, andere Inhalte anzeigen, als bei Besuchen auf einem Computer. In diesem Fall können Sie die Zielgruppe [!UICONTROL Mobile] und dann die Option **[!UICONTROL Ist Mobiltelefon]** auswählen. Sie können dann alle spezifischen Details hinzufügen, die für Sie wichtig sind, z. B. den Telefontyp, die Bildschirmgröße (in Pixel) usw.

Das mobile Targeting wird von [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester), einem Service von DotMobi bereitgestellt. DeviceAtlas ist eine umfassende Datenbank mobiler Geräte, die auf Daten beruht, die aus zahlreichen Quellen zusammengefasst wurden, einschließlich von Herstellern und Netzwerkbetreibern. Diese Daten wurden dann geprüft, referenziert und validiert, um eine große, genaue Datenbank der verfügbaren mobilen Geräte zu erstellen.

Für die Geräteerkennung werden die User-Agent-Zeichenfolgen analysiert. Einige Gerätehersteller, z. B. Apple, deaktivieren diese Funktion, indem sie in den User-Agent-Zeichenfolgen keine ausreichenden Informationen bereitstellen.

Apple-Geräte übermitteln beispielsweise in den UA-Daten keine gerätespezifischen Token. Das Ergebnis ist, dass es nicht möglich ist, iPhone-Modelle (wie iPhone 12 Pro, iPhone 12, iPhone 11 Pro Max usw.) mithilfe einer einfachen schlüsselwortbasierten Methode zu erkennen.

Um dieses Problem zu beheben, erfasst [!DNL Target] zusätzliche Daten, um iPhones und andere Apple-Geräte mithilfe der folgenden Parameter genau zu erkennen:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| devicePixelRatio | Zeichenfolge | Ein Verhältnis zwischen physischen Pixeln und geräteunabhängigen Pixeln (Dips) im Browser,  Beispiel: &quot;1.5&quot;oder &quot;2&quot; |
| screenOrientation | Zeichenfolge | Das Gerät und die JavaScript-Engine des Browsers unterstützen die Bildschirmdrehung. Mögliche Werte: Querformat oder Hochformat. |
| webGLRenderer | Zeichenfolge | Browser-Renderer des Grafiktreibers. |

>[!NOTE]
>
>Kunden, die das Mobile SDK verwenden, müssen nichts unternehmen, um diese Funktion anzuwenden. Kunden, die at.js verwenden, müssen auf at.js Version 1.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) (oder höher) [ aufrüsten.

Sie können mehr als eine Geräteeigenschaft auswählen. Mehrere Auswahlen werden mit einem ODER-Operator verbunden.

Kunden, die eine benutzerspezifische Integration (also weder at.js noch das Mobile SDK) verwenden, können diese Parameter selbst erfassen und als Mbox-Parameter übergeben.

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Mobile]** in den Bereich Audience Builder .
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
   >Sie können das Targeting nach Mobilnetzbetreiber mithilfe der [Geo-Einstellungen](/help/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670) vornehmen.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

Die folgende Abbildung zeigt eine Zielgruppe, die Besucher auswählt, die von Google hergestellte Geräte verwenden, die Mobilgeräte sind.

![Zielgruppe mit Mobilgeräten](assets/target_mobile.png)

## Zu beachten

Beachten Sie beim Targeting von Mobilgeräten die folgenden Informationen:

### Targeting-Geräte mit iOS 12.2 oder höher

Aufgrund der neuen Änderungen, die in iOS 12.2 eingeführt wurden, wirkt sich das Erstellen einer Zielgruppe mit Regeln aus, die von [!UICONTROL Device Marketing Name] und [!UICONTROL Device Model] definiert werden, die iPhone-Modelle angeben. [!DNL Target] Benutzer, die iPhones mit iOS 12.2 (oder höher) installiert haben, können nicht mehr als Ziel ausgewählt werden. Wenn diese Benutzer jedoch nicht über iOS 12.2 (oder höher) verfügen, funktioniert das iPhone-Modell-Targeting weiterhin ordnungsgemäß.

Die Aktualisierung von iOS 12.2 (oder höher) hat keine Auswirkungen auf die Identifizierung der folgenden Modelle, da diese Modelle die Aktualisierung auf iOS 12.2 nicht unterstützen: iPhone, iPhone 3G, iPhone 3GS, iPhone 4, iPhone 4s, iPhone 5, iPhone 5c, iPad, iPad 2, iPad/Retina Display, iPad Retina (4. Generation), iPod Touch 4 und iPod Touch 5.

### Targeting-Geräte mit Safari 14.0.2 (oder höher)

Wenn Sie mobile Regeln für Geräte verwenden, auf denen Safari Version 14.0.2 (oder höher) unter macOS ausgeführt wird, identifiziert [!DNL Target] fälschlicherweise Safari auf Mac-Geräten als iPad-Version, da ein bekanntes Problem mit den Benutzeragenten von Apple und DeviceAtlas vorliegt. Dieses Problem wird in Zukunft angesprochen werden.

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
