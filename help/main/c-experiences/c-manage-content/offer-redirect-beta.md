---
keywords: Umleitungsangebot;Umleitungsangebote erstellen;HTML-Angebot hinzufügen;alle URL-Parameter bei der Umleitung übermitteln;mboxSessionId bei der Umleitung übermitteln (nur erforderlich, wenn eine Umleitung auf eine andere Domain erfolgt)
description: Erfahren Sie, wie Sie Umleitungsangebote in erstellen [!DNL Target] , sodass ein Browser zu einer neuen Seite umleitet.
title: Wie erstelle ich Umleitungsangebote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
source-git-commit: bd19686d2aa716af64f520fb0be798a300ed9fa3
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 31%

---

# Erstellen von Umleitungsangeboten

Erstellen von Umleitungsangeboten in [!DNL Adobe Target] , sodass ein Browser zu einer neuen Seite umleitet.

>[!NOTE]
>
>Dieser Artikel enthält Informationen zu Aktualisierungen des [!DNL Target] -Benutzeroberfläche, die derzeit Teil eines Beta-Programms ist. Die [!DNL Adobe Target] -Team ermöglicht oft neuen Funktionen für ausgewählte Kunden zu Test- und Feedback-Zwecken. Nach Abschluss des Testzeitraums werden diese Funktionen in Zukunft für alle Kunden aktiviert [!DNL Target Standard/Premium] veröffentlicht und in den Versionshinweisen angekündigt.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie eine [!UICONTROL A/B Test] Aktivität mit zwei Erlebnissen: eines, das auf die Standardseite A verweist, und das andere, das auf Seite B umleitet. Das Angebot ist so konfiguriert, dass der Besucher auf eine andere Seite umgeleitet wird.

>[!NOTE]
>
> * Umleitungsangebote können auf der [!UICONTROL Offers] > [!UICONTROL Code Offers] oder in der [Forms-basierter Experience Composer](/help/main/c-experiences/form-experience-composer.md). Sie können keine Umleitungsangebote im [!UICONTROL Visual Experience Composer] (VEC). Der Inhalt wird in die [!DNL Target] -Anfragespeicherorte anfordern, sodass diese Orte höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage.
>
>* Umleitungsangebote können nicht in AJAX Mboxes (`mboxUpdate`).
>
>* Bei Umleitungsangeboten in Aktivitäten, die Analytics als Berichtsquelle verwenden (A4T), muss Ihre Implementierung bestimmte Mindestanforderungen erfüllen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Auf diese Weise können Besucher die Zurück-Schaltfläche in ihren Browsern verwenden.

>[!NOTE]
>
>Wenn Sie den Referrer-Wert der Landingpage übergeben möchten, verwenden Sie anstelle eines Umleitungsangebots ein HTML-Angebot.

## Erstellen Sie ein Umleitungsangebot aus dem [!UICONTROL Code Offers] page

1. Klicks **[!UICONTROL Offers]** und wählen Sie dann die **[!UICONTROL Code Offers]** Registerkarte.

   ![Registerkarte &quot;Code-Angebote&quot;](/help/main/c-experiences/c-manage-content/assets/offers-code-offers-new.png)

1. Klicks **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.

   ![Dialogfeld &quot;Umleitungsangebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer-new.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell im [!UICONTROL Assets] -Bibliothek.

1. (Bedingt) Wenn Sie eine [Target Premium-Konto](/help/main/c-intro/intro.md#premium), wählen Sie die gewünschte [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Stellen Sie sicher, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Schließen Sie alle URL-Parameter ein:** Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf der Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` als alles, was Sie in das URL-Feld eingegeben haben, `https://www.mycompany.com/mensShirts.html`.

   * **Sitzungs-ID der Mbox übergeben:** Erforderlich für die Umleitung zu einer anderen Domäne. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn Sie die `sessionId` automatisch in die Umleitung einbezogen werden. Diese Option ist nur erforderlich, wenn Sie Klicks von einer E-Mail oder von einer Domain zur anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!NOTE]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen Sie ein Umleitungsangebot mit der [!UICONTROL Form-Based Experience Composer]

1. Beim Erstellen einer Aktivität mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md), wählen Sie den Speicherort aus, an dem die **[!UICONTROL Content]** Abschnitt.

   ![Inhaltsabschnitt im formularbasierten Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf **[!UICONTROL Default Content]** Dropdown-Liste und klicken Sie auf **[!UICONTROL Change Redirect Offer]**.

   ![Option &quot;Umleitungsangebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klicks **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Dialogfeld &quot;Umleitungsangebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell im [!UICONTROL Assets] -Bibliothek.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Stellen Sie sicher, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **Schließen Sie alle URL-Parameter ein:** Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Die dynamischen Parameter in der URL sollen ebenfalls übergeben werden, da Sie auf diese Weise verfolgen, ob Besucher per E-Mail, Banneranzeige, Suchanzeige oder auf sonstige Weise auf Ihre Site gelangen. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf der Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` als alles, was Sie in das URL-Feld eingegeben haben, `https://www.mycompany.com/mensShirts.html`.

   * **Sitzungs-ID der Mbox übergeben:** Erforderlich für die Umleitung zu einer anderen Domäne. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn Sie die `sessionId` automatisch in die Umleitung einbezogen werden. Diese Option ist nur erforderlich, wenn Sie Klicks von einer E-Mail oder von einer Domain zur anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungsangeboten in Aktivitäten

Sie müssen Umleitungsangebote mit der [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md). Umleitungsangebote können derzeit nicht mit der [!UICONTROL Visual Experience Composer] (VEC).

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Erlebnis- und Angebotserstellungsoberfläche, die beim Erstellen von Erlebnissen zur Verwendung in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Recommendations] Aktivitäten, wenn der Visual Experience Composer nicht verfügbar oder nicht praktisch zur Verwendung ist. Sie können beispielsweise die [!UICONTROL Form-Based Experience Composer] , um Erlebnisse zu erstellen, die Umleitungsangebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Siehe [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) für detaillierte Schritt-für-Schritt-Anweisungen.

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste im **[!UICONTROL Content]** und klicken Sie auf **[!UICONTROL Change Redirect Offer]**.

   ![Option &quot;Umleitungsangebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Wählen Sie das gewünschte Umleitungsangebot aus dem [!UICONTROL Select Remote Offer] Dialogfeld und klicken Sie auf **[!UICONTROL Done]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Schulungsvideo: Form-Based Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird eine Demo der [!UICONTROL Form-Based Experience Composer], mit dem Sie Umleitungsangebote erstellen können.

* Erstellen Sie eine Aktivität mit der [!UICONTROL Form-Based Experience Composer]
* wann die [!UICONTROL Form-Based Experience Composer] im Vergleich zur [!UICONTROL Visual Experience Composer]
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)