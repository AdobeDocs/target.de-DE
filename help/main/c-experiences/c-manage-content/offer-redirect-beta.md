---
keywords: Umleitungsangebot; Umleitungsangebot erstellen; HTML-Angebot hinzufügen; alle URL-Parameter bei der Umleitung übergeben
description: Erfahren Sie, wie Sie Umleitungsangebote erstellen, um Browser nahtlos zu neuen Seiten zu führen.
title: Wie erstelle ich Umleitungsangebote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
exl-id: 751a8d97-2e35-4527-99f3-d7a42c104fcb
source-git-commit: 4b57712b838906611702db521b51af84077501e6
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 24%

---

# Erstellen von Umleitungsangeboten

Erfahren Sie, wie Sie Umleitungsangebote erstellen, um Browser nahtlos zu neuen Seiten zu führen.

>[!NOTE]
>
>Dieser Artikel enthält Informationen zu Aktualisierungen der [!DNL Target] -Benutzeroberfläche, die derzeit Teil eines Beta-Programms ist. Das [!DNL Adobe Target]-Team ermöglicht für ausgewählte Kunden oft neue Funktionen zu Test- und Feedback-Zwecken. Nach Abschluss des Testzeitraums werden diese Funktionen für alle Kunden in zukünftigen [!DNL Target]-Versionen aktiviert und in den [Versionshinweisen](/help/main/r-release-notes/release-notes.md) angekündigt.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie eine [!UICONTROL A/B Test] -Aktivität mit zwei Erlebnissen ein: eines, das auf die Standardseite A verweist, und das andere, das auf Seite B umleitet. Das Angebot ist so konfiguriert, dass der Besucher auf eine andere Seite umgeleitet wird.

>[!NOTE]
>
> * Umleitungsangebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) erstellt werden. Sie können keine Umleitungsangebote im VEC (0) erstellen oder anwenden. [!UICONTROL Visual Experience Composer] Inhalte werden in die [!DNL Target] -Anfragespeicherorte eingefügt, sodass diese Orte höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage geeignet sind.
>
>* Sie können keine Umleitungsangebote in AJAX Mboxes (`mboxUpdate`) verwenden.
>
>* Bei Umleitungsangeboten in Aktivitäten mit [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) muss Ihre Implementierung bestimmte Mindestanforderungen erfüllen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Siehe [Umleitungsangebote - Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Auf diese Weise können Besucher die Zurück-Schaltfläche in ihren Browsern verwenden.

>[!NOTE]
>
>Wenn Sie den Referrer-Wert der Landingpage übergeben möchten, verwenden Sie anstelle eines Umleitungsangebots ein HTML-Angebot.

## Erstellen eines Umleitungsangebots über die Seite [!UICONTROL Code Offers]

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.
1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der [!UICONTROL Assets] -Bibliothek.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto](/help/main/c-intro/intro.md#premium) verfügen, wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Stellen Sie sicher, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **[!UICONTROL Include all URL parameters]:** Aktivieren Sie diese Option, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Sie möchten auch, dass die dynamischen Parameter in der URL übergeben werden, da Sie auf diese Weise verfolgen können, ob Besucher über E-Mail, Banneranzeige, Suchanzeige oder organisch auf Ihre Site gelangt sind. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch zu `https://www.mycompany.com/mensShirts.html?emailId=123`, wenn Sie nur in das Feld &quot;URL&quot;den Wert `https://www.mycompany.com/mensShirts.html` eingegeben haben.

   * **[!UICONTROL Pass mbox session ID]:** Erforderlich, um zu einer anderen Domäne umzuleiten. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn die `sessionId` automatisch in die Umleitung einbezogen werden soll. Diese Option ist nur erforderlich, wenn Sie Klicks von einer E-Mail oder von einer Domain zur anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen eines Umleitungsangebots mit dem [!UICONTROL Form-Based Experience Composer]

1. Wählen Sie beim Erstellen einer Aktivität mit dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Content]** angezeigt werden soll.
1. Klicken Sie auf die Dropdownliste **[!UICONTROL Content]**, klicken Sie auf das Symbol **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Change Redirect Offer]**.
1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der [!UICONTROL Assets] -Bibliothek.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Stellen Sie sicher, dass sich der Benutzer nach der Umleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **[!UICONTROL Include all URL parameters]:** Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite propagiert werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Sie möchten auch, dass die dynamischen Parameter in der URL übergeben werden, da Sie auf diese Weise verfolgen können, ob Besucher über E-Mail, Banneranzeige, Suchanzeige oder organisch auf Ihre Site gelangt sind. Durch Aktivierung dieser Option wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch zu `https://www.mycompany.com/mensShirts.html?emailId=123`, wenn Sie nur in das Feld &quot;URL&quot;den Wert `https://www.mycompany.com/mensShirts.html` eingegeben haben.

   * **[!UICONTROL Pass mbox session ID]:** Erforderlich, um zu einer anderen Domäne umzuleiten. Schalten Sie den Umschalter um, um diese Option zu aktivieren, wenn die `sessionId` automatisch in die Umleitung einbezogen werden soll. Diese Option ist nur erforderlich, wenn Sie Klicks von einer E-Mail oder von einer Domain zur anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie die Sitzungs-ID der Mbox beim Wechseln von Domänen nicht weitergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungsangeboten in Aktivitäten

Wenden Sie Umleitungsangebote mit dem Wert [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) an. Sie können Umleitungsangebote derzeit nicht mit dem VEC (0) anwenden.[!UICONTROL Visual Experience Composer]

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten, die beim Erstellen von Erlebnissen für die Verwendung in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting]- (XT), [!UICONTROL Automated Personalization]- (AP) und [!UICONTROL Recommendations]-Aktivitäten nützlich ist, wenn die [!UICONTROL Visual Experience Composer] nicht verfügbar oder praktisch zur Verwendung ist. Beispielsweise können Sie mit dem [!UICONTROL Form-Based Experience Composer] Erlebnisse erstellen, die Umleitungsangebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Detaillierte schrittweise Anweisungen finden Sie unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) .

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste **[!UICONTROL Content]**, klicken Sie auf das Symbol **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Change Redirect Offer]**.
1. Wählen Sie im Dialogfeld [!UICONTROL Select Redirect Offer] das gewünschte Umleitungsangebot aus und klicken Sie dann auf **[!UICONTROL Add]**.
1. Schließen Sie die Konfiguration der Aktivität ab.
