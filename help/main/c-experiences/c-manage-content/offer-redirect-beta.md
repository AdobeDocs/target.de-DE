---
keywords: Umleitungsangebot;Umleitungsangebot erstellen;HTML-Angebot hinzufügen;alle URL-Parameter bei der Umleitung übergeben
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
>Dieser Artikel enthält Informationen zu Aktualisierungen der [!DNL Target]-Benutzeroberfläche, die derzeit Teil eines Beta-Programms ist. Das [!DNL Adobe Target]-Team bietet ausgewählten Kunden häufig neue Funktionen zu Test- und Feedback-Zwecken. Nach Abschluss der Testphase werden diese Funktionen für alle Kundinnen und Kunden in zukünftigen [!DNL Target]-Versionen aktiviert und in [Versionshinweisen](/help/main/r-release-notes/release-notes.md) angekündigt.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie eine [!UICONTROL A/B Test] Aktivität mit zwei Erlebnissen ein: einem, das auf die Standardseite A verweist, und einem, das zu Seite B umleitet. Das Angebot ist so konfiguriert, dass der Besucher auf eine andere Seite weitergeleitet wird.

>[!NOTE]
>
> * Umleitungsangebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer erstellt ](/help/main/c-experiences/form-experience-composer.md). Umleitungsangebote in der [!UICONTROL Visual Experience Composer] (VEC) können nicht erstellt oder angewendet werden. Inhalte werden an den [!DNL Target] Anfragespeicherorten eingefügt, sodass diese Speicherorte wahrscheinlich nicht für eine globale [!DNL Target]-Anfrage geeignet sind.
>
>* Umleitungsangebote können nicht in AJAX-Mboxes (`mboxUpdate`) verwendet werden.
>
>* Für Umleitungsangebote in -Aktivitäten, die [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, muss Ihre Implementierung bestimmte Mindestanforderungen erfüllen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Siehe [Umleitungsangebote - A4T-FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Dieser Prozess ermöglicht Besuchern die Verwendung der Zurück-Schaltfläche in ihren Browsern.

>[!NOTE]
>
>Wenn Sie den Wert der verweisenden Stelle der Landingpage weitergeben möchten, verwenden Sie ein HTML-Angebot anstelle eines Umleitungsangebots.

## Erstellen eines Umleitungsangebots über die [!UICONTROL Code Offers]

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.
1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der [!UICONTROL Assets] zu finden.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto verfügen](/help/main/c-intro/intro.md#premium) wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Stellen Sie sicher, dass sich der/die Benutzende nach der Weiterleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **[!UICONTROL Include all URL parameters]:** Aktivieren Sie diese Option, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Sie möchten auch, dass die dynamischen Parameter in der URL übergeben werden, da mit dieser Methode verfolgt wird, ob Personen Ihre Site per E-Mail, Banner, Suchanzeige oder organisch erreicht haben. Wenn diese Option aktiviert ist, wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, sobald alle Eingaben im URL-Feld `https://www.mycompany.com/mensShirts.html` wurden.

   * **[!UICONTROL Pass mbox session ID]:** erforderlich für die Umleitung auf eine andere Domain. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass der `sessionId` automatisch in der Umleitung enthalten ist. Diese Option ist nur erforderlich, wenn Sie Klicks aus E-Mails oder von einer Domain zu einer anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie bei der Domain-übergreifenden Verwendung die Sitzungs-ID der Mbox nicht übergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen eines Umleitungsangebots mithilfe der [!UICONTROL Form-Based Experience Composer]

1. Wählen Sie beim Erstellen einer Aktivität mit [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, um den Abschnitt &quot;**[!UICONTROL Content]**&quot; anzuzeigen.
1. Klicken Sie auf die Dropdown-Liste &quot;**[!UICONTROL Content]**&quot;, dann auf das **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und schließlich auf **[!UICONTROL Change Redirect Offer]**.
1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der [!UICONTROL Assets] zu finden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Stellen Sie sicher, dass sich der/die Benutzende nach der Weiterleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **[!UICONTROL Include all URL parameters]:** Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Sie möchten auch, dass die dynamischen Parameter in der URL übergeben werden, da mit dieser Methode verfolgt wird, ob Personen Ihre Site per E-Mail, Banner, Suchanzeige oder organisch erreicht haben. Wenn diese Option aktiviert ist, wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, sobald alle Eingaben im URL-Feld `https://www.mycompany.com/mensShirts.html` wurden.

   * **[!UICONTROL Pass mbox session ID]:** erforderlich für die Umleitung auf eine andere Domain. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass der `sessionId` automatisch in der Umleitung enthalten ist. Diese Option ist nur erforderlich, wenn Sie Klicks aus E-Mails oder von einer Domain zu einer anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie bei der Domain-übergreifenden Verwendung die Sitzungs-ID der Mbox nicht übergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungsangeboten in -Aktivitäten

Anwenden von Umleitungsangeboten mithilfe der [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md). Umleitungsangebote können derzeit nicht mit dem [!UICONTROL Visual Experience Composer] (VEC) angewendet werden.

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten. Diese Erlebnisse können in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Recommendations]-Aktivitäten verwendet werden, wenn die [!UICONTROL Visual Experience Composer] nicht verfügbar oder unpraktisch in der Anwendung ist. Beispielsweise können Sie die [!UICONTROL Form-Based Experience Composer] verwenden, um Erlebnisse zu erstellen, die Umleitungsangebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) finden Sie detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Speicherort an und fügen Sie gegebenenfalls Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdown-Liste &quot;**[!UICONTROL Content]**&quot;, dann auf das **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und schließlich auf **[!UICONTROL Change Redirect Offer]**.
1. Wählen Sie das gewünschte Umleitungsangebot im Dialogfeld [!UICONTROL Select Redirect Offer] aus und klicken Sie dann auf **[!UICONTROL Add]**.
1. Schließen Sie die Konfiguration der Aktivität ab.
