---
keywords: redirect offer;create redirect offer;add html offer;Pass all URL parameters in redirect;Pass mboxSessionId in redirect (only needed when the redirect is going to a different domain)
description: Informationen über Umleitungsangebote in Adobe Target, die bewirken, dass ein Browser zu einer neuen Seite weiterleitet.
title: Erstellen von Umleitungsangeboten
feature: offers
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 98%

---


# Erstellen von Umleitungsangeboten{#create-redirect-offers}

Bei Umleitungsangeboten wird der Browser zu einer neuen Seite umgeleitet.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie eine A/B-Test-Kampagne mit zwei Erlebnissen ein: einem, das auf die Standardseite A verweist, und einem anderen, das auf die Seite B umleitet. Das Angebot wird so konfiguriert, dass der Besucher auf eine andere Seite umgeleitet wird.

>[!NOTE]
>
>Sie können keine Umleitungsangebote in Ajax-Mboxes (`mboxUpdate`) verwenden.
>
>Für Umleitungsangebote in Aktivitäten mit A4T muss Ihre Implementation bestimmten Mindestanforderungen entsprechen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).

Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Daher kann der Besucher die Zurück-Schaltfläche des Browsers wie gewohnt verwenden.

>[!NOTE]
>
>Wenn Sie den Referrer-Wert der Landingpage übergeben möchten, sollten Sie statt eines Umleitungsangebots ein HTML-Angebot verwenden.

**So erstellen Sie ein Weiterleitungsangebot:**

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.
1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Umleitungsangebot]**.
1. Geben Sie einen Angebotsnamen ein.
1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

* **Beziehen Sie alle URL-Parameter mit ein:** Aktivieren Sie dieses Kontrollkästchen, wenn alle URL-Parameter der vorherigen Seite auf die umgeleitete Seite propagiert werden sollen.

   Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Wenn Sie dieses Kontrollkästchen aktivieren, wird Ihr Umleitungsangebot auf der Seite [!DNL `https://www.mycompany.com/mens.html?emailId=123`] automatisch zu [!DNL `https://www.mycompany.com/mensShirts.html?emailId=123`], wenn in das URL-Feld nur [!DNL `https://www.mycompany.com/mensShirts.html`] eingegeben wurde.

* **Sitzungs-ID der Mbox weitergeben (erforderlich für die Umleitung auf eine andere Domäne):** Aktivieren Sie dieses Kontrollkästchen, wenn die `sessionId` automatisch in der Umleitung enthalten sein soll. Dies ist nur erforderlich, wenn Sie Klicks aus E-Mails oder von einer Domäne zu einer anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

   Wenn Sie die Einstellung für Erst- und Drittanbieter-Cookie verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Schulungsvideo: Das Content-Repository (4:56) ![Übersichtskennzeichnung](/help/assets/overview.png)

In diesem Video wird beschrieben, wie Inhalte verwaltet werden.

* Zusammenhang zwischen der [Experience Cloud-Asset-Bibliothek](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) und der Target-Inhaltsbibliothek
* Benutzerdefinierte HTML-Angebote
* Benutzerdefinierte HTML-Angebote im Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)
