---
keywords: Umleitungsangebot;Umleitungsangebote erstellen;HTML-Angebot hinzufügen;alle URL-Parameter bei der Umleitung übermitteln;mboxSessionId bei der Umleitung übermitteln (nur erforderlich, wenn eine Umleitung auf eine andere Domain erfolgt)
description: Erfahren Sie, wie Sie Umleitungsangebote in Adobe erstellen. [!DNL Target] , sodass ein Browser zu einer neuen Seite umleitet.
title: Wie erstelle ich Umleitungsangebote?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 48%

---

# Erstellen von Umleitungsangeboten

Umleitungsangebote in [!DNL Adobe Target] verursacht, dass ein Browser zu einer neuen Seite umleitet.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie A/B-Test-Aktivitäten mit zwei Erlebnissen ein: einen Verweis auf die Standardseite A und den anderen Verweis auf Seite B. Das Angebot ist so konfiguriert, dass der Besucher zu einer anderen Seite weitergeleitet wird.

>[!NOTE]
>
> * Umleitungsangebote können auf der [!UICONTROL Angebote] > [!UICONTROL Code-Angebote] oder in der [Forms-basierter Experience Composer](/help/main/c-experiences/form-experience-composer.md). Sie können keine Umleitungsangebote im Visual Experience Composer (VEC) erstellen oder anwenden. Der Inhalt wird in die [!DNL Target] Anfragespeicherorte, sodass diese höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage.
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

## Erstellen eines Umleitungsangebots über die Seite &quot;Code-Angebote&quot;

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.

   ![Registerkarte &quot;Code-Angebote&quot;](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Umleitungsangebot]**.

   ![Dialogfeld &quot;Umleitungsangebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek Assets aufzufinden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Schließen Sie alle URL-Parameter ein:** Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

      Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf der Seite `https://www.mycompany.com/mens.html?emailId=123` wird automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` als alles, was Sie in das URL-Feld eingegeben haben, `https://www.mycompany.com/mensShirts.html`.

   * **Sitzungs-ID der Mbox übergeben:** Erforderlich für die Umleitung zu einer anderen Domäne. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn Sie die `sessionId` automatisch in die Umleitung einbezogen werden. Dies ist nur erforderlich, wenn Sie Klicks aus einer E-Mail oder aus einer Domain in eine andere testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

      Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen eines Umleitungsangebots mit dem formularbasierten Experience Composer

1. Beim Erstellen einer Aktivität mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md), wählen Sie den Speicherort aus, an dem die **[!UICONTROL Inhalt]** Abschnitt.

   ![Inhaltsbereich in Form-Based Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf **[!UICONTROL Standardinhalt]** Dropdown-Liste und klicken Sie auf **[!UICONTROL Umleitungsangebot ändern]**.

   ![Option &quot;Umleitungsangebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Umleitungsangebot]**.

   ![Dialogfeld &quot;Umleitungsangebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek Assets aufzufinden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Hierbei muss es sich um eine absolute URL handeln.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Sie sollten sicherstellen, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Schließen Sie alle URL-Parameter ein:** Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

      Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf der Seite `https://www.mycompany.com/mens.html?emailId=123` wird automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` als alles, was Sie in das URL-Feld eingegeben haben, `https://www.mycompany.com/mensShirts.html`.

   * **Sitzungs-ID der Mbox übergeben:** Erforderlich für die Umleitung zu einer anderen Domäne. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn Sie die `sessionId` automatisch in die Umleitung einbezogen werden. Dies ist nur erforderlich, wenn Sie Klicks aus einer E-Mail oder aus einer Domain in eine andere testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

      Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Wenden Sie sich an Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungsangeboten in Aktivitäten

Sie müssen Umleitungsangebote mit der [!UICONTROL Form-Based Experience Composer]. Sie können Umleitungsangebote derzeit nicht mit dem VEC anwenden.

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Erlebnis- und Angebotserstellungsoberfläche, die beim Erstellen von Erlebnissen zur Verwendung in [!UICONTROL A/B-Tests], [!UICONTROL Erlebnis-Targeting] (XT), [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Recommendations] Aktivitäten, wenn der Visual Experience Composer nicht verfügbar oder nicht praktisch zur Verwendung ist. Sie können beispielsweise die [!UICONTROL Form-Based Experience Composer] , um Erlebnisse zu erstellen, die Umleitungsangebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Siehe [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) für detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste im **[!UICONTROL Inhalt]** und klicken Sie auf **[!UICONTROL Umleitungsangebot ändern]**.

   ![Option &quot;Umleitungsangebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Wählen Sie das gewünschte Umleitungsangebot aus dem [!UICONTROL Remote-Angebot auswählen] Dialogfeld und klicken Sie auf **[!UICONTROL Fertig]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Schulungsvideo: Form-Based Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird der formularbasierte Composer vorgestellt, mit dem Sie Umleitungsangebote erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
