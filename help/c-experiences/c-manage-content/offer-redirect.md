---
keywords: Umleitungsangebot;Umleitungsangebote erstellen;HTML-Angebot hinzufügen;alle URL-Parameter bei der Umleitung übermitteln;mboxSessionId bei der Umleitung übermitteln (nur erforderlich, wenn eine Umleitung auf eine andere Domäne erfolgt)
description: 'Erfahren Sie, wie Sie Umleitungs-Angebot in Adobe [!DNL Target] erstellen, damit ein Browser zu einer neuen Seite umgeleitet wird. '
title: Wie erstelle ich Umleitungs-Angebote?
feature: Erlebnisse und Angebot
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 48%

---

# Erstellen von Umleitungsangeboten

Angebot umleiten in [!DNL Adobe Target] führen dazu, dass ein Browser zu einer neuen Seite umleitet.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie eine A/B-Test-Aktivität mit zwei Erlebnissen ein: ein Verweis auf die Standardseite A und der andere auf Seite B. Das Angebot ist so konfiguriert, dass der Besucher auf eine andere Seite umgeleitet wird.

>[!NOTE]
>
> * Umgeleitete Angebot können auf der Seite [!UICONTROL Angebot] > [!UICONTROL Code-Angebot] oder auf der Seite [Forms-basierter Experience Composer](/help/c-experiences/form-experience-composer.md) erstellt werden. Im Visual Experience Composer (VEC) können keine Umleitungs-Angebot erstellt oder angewendet werden. Inhalte werden in die Anforderungsspeicherorte [!DNL Target] eingefügt, sodass diese wahrscheinlich nicht für eine globale [!DNL Target]-Anforderung geeignet sind.
   >
   >
* Sie können keine Umleitungsangebote in Ajax-Mboxes (`mboxUpdate`) verwenden.
   >
   >
* Für Umleitungsangebote in Aktivitäten mit A4T muss Ihre Implementation bestimmten Mindestanforderungen entsprechen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
   >
   >
* Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).


Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Daher kann der Besucher die Zurück-Schaltfläche des Browsers wie gewohnt verwenden.

>[!NOTE]
>
>Wenn Sie den Referrer-Wert der Landingpage übergeben möchten, sollten Sie statt eines Umleitungsangebots ein HTML-Angebot verwenden.

## Erstellen eines Umleitungs-Angebots auf der Seite &quot;Code-Angebot&quot;

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.

   ![Registerkarte &quot;Code-Angebot&quot;](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Umleitungsangebot]**.

   ![Dialogfeld &quot;Umleitungs-Angebot erstellen&quot;](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek Assets aufzufinden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Alle URL-Parameter einschließen:** Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden sollen.

      Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Wenn Sie diese Option aktivieren, wird Ihr Umleitungs-Angebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, wenn Sie im Feld &quot;URL&quot;nur `https://www.mycompany.com/mensShirts.html` eingegeben haben.

   * **Sitzungs-ID der Mbox weitergeben:** Erforderlich, um zu einer anderen Domäne umgeleitet zu werden. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn `sessionId` automatisch in die Umleitung einbezogen werden soll. Dies ist nur erforderlich, wenn Sie Klicks aus einer E-Mail oder Klicks aus einer Domäne in eine andere testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

      Wenn Sie die Einrichtung für Erst- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen eines Umleitungs-Angebots mit dem Form-Based Experience Composer

1. Wählen Sie beim Erstellen einer Aktivität mit dem [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Inhalt]** angezeigt werden soll.

   ![Inhaltsabschnitt im Form-Based Experience Composer](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf die Dropdown-Liste **[!UICONTROL Standardinhalt]** und dann auf **[!UICONTROL Angebot umleiten]** ändern.

   ![Option &quot;Angebot umleiten&quot;ändern](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Umleitungsangebot]**.

   ![Dialogfeld &quot;Umleitungs-Angebot erstellen&quot;](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek Assets aufzufinden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Alle URL-Parameter einschließen:** Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden sollen.

      Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Wenn Sie diese Option aktivieren, wird Ihr Umleitungs-Angebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, wenn Sie im Feld &quot;URL&quot;nur `https://www.mycompany.com/mensShirts.html` eingegeben haben.

   * **Sitzungs-ID der Mbox weitergeben:** Erforderlich, um zu einer anderen Domäne umgeleitet zu werden. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn `sessionId` automatisch in die Umleitung einbezogen werden soll. Dies ist nur erforderlich, wenn Sie Klicks aus einer E-Mail oder Klicks aus einer Domäne in eine andere testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

      Wenn Sie die Einrichtung für Erst- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungs-Angeboten in Aktivitäten

Sie müssen Umleitungs-Angebot mit dem [!UICONTROL Form-Based Experience Composer] anwenden. Sie können derzeit keine Umleitungs-Angebot mit VEC anwenden.

Der [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Erlebnis- und Angebot-Erstellungsoberfläche, die beim Erstellen von Erlebnissen für die Verwendung in [!UICONTROL A/B-Tests], [!UICONTROL Erlebnis-Targeting] (XT), [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Recommendations nützlich ist. a10/> Aktivitäten, bei denen der Visual Experience Composer nicht verfügbar oder nicht einsetzbar ist. ] Sie können beispielsweise den [!UICONTROL Form-Based Experience Composer] verwenden, um Erlebnisse zu erstellen, die Umleitungs-Angebot verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Detaillierte Anleitungen finden Sie unter [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md).

1. Geben Sie den gewünschten Speicherort an und fügen Sie bei Bedarf Audiencen hinzu.

1. Klicken Sie im Abschnitt **[!UICONTROL Content]** auf die Dropdown-Liste und dann auf **[!UICONTROL Angebot umleiten]** ändern.

   ![Option &quot;Angebot umleiten&quot;ändern](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Wählen Sie im Dialogfeld [!UICONTROL Remote-Angebot] auswählen das gewünschte Umleitungs-Angebot aus und klicken Sie dann auf **[!UICONTROL Fertig]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Schulungsvideo: Form-Based Composer ![Tutorial badge](/help/assets/tutorial.png)

In diesem Video wird eine Demo des formularbasierten Composers gezeigt, mit dem Sie Umleitungs-Angebot erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
