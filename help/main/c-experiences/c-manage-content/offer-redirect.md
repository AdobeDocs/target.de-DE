---
keywords: Umleitungsangebot;Umleitungsangebote erstellen;HTML-Angebot hinzufügen;alle URL-Parameter bei der Umleitung übermitteln;mboxSessionId bei der Umleitung übermitteln (nur erforderlich, wenn eine Umleitung auf eine andere Domain erfolgt)
description: Erfahren Sie, wie Sie in Adobe Umleitungsangebote erstellen [!DNL Target]  damit ein Browser zu einer neuen Seite umleitet.
title: Wie erstelle ich Umleitungsangebote?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 45%

---

# Erstellen von Umleitungsangeboten

Umleitungsangebote in führen [!DNL Adobe Target] dazu, dass ein Browser zu einer neuen Seite umleitet.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie eine A/B-Test -Aktivität mit zwei Erlebnissen ein: ein Erlebnis, das auf die Standardseite A verweist, und das andere, das zu Seite B umleitet. Das Angebot ist so konfiguriert, dass der Besucher auf eine andere Seite weitergeleitet wird.

>[!NOTE]
>
> * Umleitungsangebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer erstellt ](/help/main/c-experiences/form-experience-composer.md). Umleitungsangebote können nicht im Visual Experience Composer (VEC) erstellt oder angewendet werden. Inhalte werden an den [!DNL Target] Anfragespeicherorten eingefügt, sodass diese wahrscheinlich nicht für eine globale [!DNL Target]-Anfrage geeignet sind.
>
>* Umleitungsangebote können nicht in Ajax-Mboxes (`mboxUpdate`) verwendet werden.
>
>* Für Umleitungsangebote in Aktivitäten mit A4T muss Ihre Implementation bestimmten Mindestanforderungen entsprechen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Daher kann der Besucher die Zurück-Schaltfläche des Browsers wie gewohnt verwenden.

>[!NOTE]
>
>Wenn Sie den Referrer-Wert der Landingpage übergeben möchten, sollten Sie statt eines Umleitungsangebots ein HTML-Angebot verwenden.

## Erstellen eines Umleitungsangebots über die Seite „Code-Angebote“

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.

   ![Registerkarte „Angebote codieren“](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Dialogfeld „Umleitungsangebot erstellen“](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der Assets-Bibliothek zu finden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Alle URL-Parameter einschließen:** Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Wenn diese Option aktiviert ist, wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, sobald alle Eingaben im URL-Feld `https://www.mycompany.com/mensShirts.html` wurden.

   * **Sitzungs-ID der Mbox weitergeben:** erforderlich, um zu einer anderen Domain umzuleiten. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn die `sessionId` automatisch in der Umleitung enthalten sein soll. Dies ist nur erforderlich, wenn Sie Klicks aus E-Mails oder von einer Domain zu einer anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie bei der Domain-übergreifenden Verwendung die Sitzungs-ID der Mbox nicht übergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen eines Umleitungsangebots mit dem formularbasierten Experience Composer

1. Wählen Sie beim Erstellen einer Aktivität mit [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, um den Abschnitt &quot;**[!UICONTROL Content]**&quot; anzuzeigen.

   ![Inhaltsabschnitt in Form-Based Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf die Dropdown-Liste **[!UICONTROL Default Content]** und dann auf **[!UICONTROL Change Redirect Offer]**.

   ![Option „Umleitungsangebot ändern“](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Dialogfeld „Umleitungsangebot erstellen“](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der Assets-Bibliothek zu finden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Alle URL-Parameter einschließen:** Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Wenn diese Option aktiviert ist, wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, sobald alle Eingaben im URL-Feld `https://www.mycompany.com/mensShirts.html` wurden.

   * **Sitzungs-ID der Mbox weitergeben:** erforderlich, um zu einer anderen Domain umzuleiten. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn die `sessionId` automatisch in der Umleitung enthalten sein soll. Dies ist nur erforderlich, wenn Sie Klicks aus E-Mails oder von einer Domain zu einer anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie bei der Domain-übergreifenden Verwendung die Sitzungs-ID der Mbox nicht übergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungsangeboten in -Aktivitäten

Sie müssen Umleitungsangebote mithilfe der [!UICONTROL Form-Based Experience Composer] anwenden. Umleitungsangebote können derzeit nicht mit dem VEC angewendet werden.

Der [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten. Diese Erlebnisse können in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Recommendations]-Aktivitäten genutzt werden, wenn der Visual Experience Composer nicht verfügbar oder unpraktisch in der Anwendung ist. Beispielsweise können Sie die [!UICONTROL Form-Based Experience Composer] verwenden, um Erlebnisse zu erstellen, die Umleitungsangebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) finden Sie detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Speicherort an und fügen Sie gegebenenfalls Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdown-Liste im Abschnitt **[!UICONTROL Content]** und dann auf **[!UICONTROL Change Redirect Offer]**.

   ![Option „Umleitungsangebot ändern“](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Wählen Sie das gewünschte Umleitungsangebot im Dialogfeld [!UICONTROL Select Remote Offer] aus und klicken Sie dann auf **[!UICONTROL Done]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Schulungsvideo: Formularbasierter Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video erhalten Sie eine Demo des formularbasierten Composers, mit dem Sie Umleitungsangebote erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
