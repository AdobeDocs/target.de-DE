---
keywords: Umleitungsangebot;Umleitungsangebote erstellen;HTML-Angebot hinzufügen;alle URL-Parameter bei der Umleitung übermitteln;mboxSessionId bei der Umleitung übermitteln (nur erforderlich, wenn eine Umleitung auf eine andere Domain erfolgt)
description: Erfahren Sie, wie Sie Umleitungsangebote in Adobe [!DNL Target] erstellen, damit ein Browser zu einer neuen Seite weiterleitet.
title: Wie erstelle ich Umleitungsangebote?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 45%

---

# Erstellen von Umleitungsangeboten

Umleitungsangebote in [!DNL Adobe Target] bewirken, dass ein Browser zu einer neuen Seite umleitet.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie A/B-Test-Aktivitäten mit zwei Erlebnissen ein: eines, das auf die Standardseite A verweist, und das andere, das auf Seite B umleitet. Das Angebot ist so konfiguriert, dass der Besucher auf eine andere Seite umgeleitet wird.

>[!NOTE]
>
> * Umleitungsangebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) erstellt werden. Sie können keine Umleitungsangebote im Visual Experience Composer (VEC) erstellen oder anwenden. Inhalte werden in die [!DNL Target] -Anfragespeicherorte eingefügt, sodass sie höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage geeignet sind.
>
>* Sie können keine Umleitungsangebote in Ajax-Mboxes (`mboxUpdate`) verwenden.
>
>* Für Umleitungsangebote in Aktivitäten mit A4T muss Ihre Implementation bestimmten Mindestanforderungen entsprechen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Daher kann der Besucher die Zurück-Schaltfläche des Browsers wie gewohnt verwenden.

>[!NOTE]
>
>Wenn Sie den Referrer-Wert der Landingpage übergeben möchten, sollten Sie statt eines Umleitungsangebots ein HTML-Angebot verwenden.

## Erstellen eines Umleitungsangebots über die Seite Code-Angebote

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.

   ![Registerkarte &quot;Code-Angebote&quot;](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Dialogfeld &quot;Umleitungsangebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der Assets-Bibliothek.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Alle URL-Parameter einschließen:** Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch zu `https://www.mycompany.com/mensShirts.html?emailId=123`, wenn Sie nur in das URL-Feld `https://www.mycompany.com/mensShirts.html` eingegeben haben.

   * **Mbox-Sitzungs-ID übergeben:** Erforderlich, um zu einer anderen Domäne umzuleiten. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn `sessionId` automatisch in die Umleitung einbezogen werden soll. Dies ist nur erforderlich, wenn Sie Klicks aus einer E-Mail oder aus einer Domain in eine andere testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen eines Umleitungsangebots mit dem formularbasierten Experience Composer

1. Wählen Sie beim Erstellen einer Aktivität mit dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Content]** angezeigt werden soll.

   ![Inhaltsabschnitt im formularbasierten Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf die Dropdownliste **[!UICONTROL Default Content]** und dann auf **[!UICONTROL Change Redirect Offer]**.

   ![Option &quot;Umleitungsangebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Dialogfeld &quot;Umleitungsangebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der Assets-Bibliothek.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Alle URL-Parameter einschließen:** Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch zu `https://www.mycompany.com/mensShirts.html?emailId=123`, wenn Sie nur in das URL-Feld `https://www.mycompany.com/mensShirts.html` eingegeben haben.

   * **Mbox-Sitzungs-ID übergeben:** Erforderlich, um zu einer anderen Domäne umzuleiten. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn `sessionId` automatisch in die Umleitung einbezogen werden soll. Dies ist nur erforderlich, wenn Sie Klicks aus einer E-Mail oder aus einer Domain in eine andere testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungsangeboten in Aktivitäten

Sie müssen Umleitungsangebote mit dem [!UICONTROL Form-Based Experience Composer] anwenden. Sie können Umleitungsangebote derzeit nicht mit dem VEC anwenden.

Der [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten, die beim Erstellen von Erlebnissen für die Verwendung in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting]- (XT), [!UICONTROL Automated Personalization]- (AP) und [!UICONTROL Recommendations]-Aktivitäten nützlich ist, wenn der Visual Experience Composer nicht verfügbar oder praktisch zur Verwendung nicht verfügbar ist. Beispielsweise können Sie mit dem [!UICONTROL Form-Based Experience Composer] Erlebnisse erstellen, die Umleitungsangebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Detaillierte schrittweise Anweisungen finden Sie unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) .

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste im Abschnitt **[!UICONTROL Content]** und dann auf **[!UICONTROL Change Redirect Offer]**.

   ![Option &quot;Umleitungsangebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Wählen Sie im Dialogfeld [!UICONTROL Select Remote Offer] das gewünschte Umleitungsangebot aus und klicken Sie dann auf **[!UICONTROL Done]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Schulungsvideo: Form-Based Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird der formularbasierte Composer vorgestellt, mit dem Sie Umleitungsangebote erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
