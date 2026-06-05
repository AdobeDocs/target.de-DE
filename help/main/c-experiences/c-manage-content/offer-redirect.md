---
keywords: Umleitungsangebot;Umleitungsangebot erstellen;HTML-Angebot hinzufügen;alle URL-Parameter bei der Umleitung übergeben
description: Erfahren Sie, wie Sie Umleitungsangebote erstellen, um Browser nahtlos zu neuen Seiten zu führen.
title: Wie erstelle ich Umleitungsangebote?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
TQID: https://experienceleague.adobe.com/-kFkgCCbzb34aNAxW-Q1CqmyK9rETL0qVMQeEP9JtrY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 16fb7a1902ea76cab56a93fa141a32a3c6bc4467
workflow-type: tm+mt
source-wordcount: 1190
ht-degree: 24%

---

# Erstellen von Umleitungsangeboten

Erfahren Sie, wie Sie Umleitungsangebote erstellen, um Browser nahtlos zu neuen Seiten zu führen.

Es kann vorkommen, dass Sie zwei vollkommen verschiedene Seiten testen müssen, anstatt lediglich Inhaltselemente innerhalb einer Seite zu ändern. In diesem Fall vergleicht Ihr A/B-Test Seite A mit Seite B. Richten Sie eine [!UICONTROL A/B-Test]-Aktivität mit zwei Erlebnissen ein: einem, der auf die Standardseite A verweist, und einem, der zu Seite B umleitet. Das Angebot ist so konfiguriert, dass der Besucher auf eine andere Seite weitergeleitet wird.

>[!NOTE]
>
> * Umleitungsangebote können auf der Seite [!UICONTROL Angebote] > [!UICONTROL Code-Angebote] oder im [Forms-basierten Experience Composer erstellt &#x200B;](/help/main/c-experiences/form-experience-composer.md). Umleitungsangebote können nicht im [!UICONTROL Visual Experience Composer) (]) erstellt oder angewendet werden. Inhalte werden an den [!DNL Target] Anfragespeicherorten eingefügt, sodass diese Speicherorte wahrscheinlich nicht für eine globale [!DNL Target]-Anfrage geeignet sind.
>
>* Umleitungsangebote können nicht in AJAX-Mboxes (`mboxUpdate`) verwendet werden.
>
>* Für Umleitungsangebote in -Aktivitäten, die [[!UICONTROL Analytics als Berichtsquelle]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, muss Ihre Implementierung bestimmte Mindestanforderungen erfüllen. Darüber hinaus gibt es wichtige Informationen, die Sie benötigen. Siehe [Umleitungsangebote - A4T-FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Weitere Informationen zum Einrichten eines Erlebnisses mit Umleitung finden Sie unter [Zu einer URL umleiten](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Bei diesem Umleitungsangebot wird JavaScript-Code ausgeführt, um den Browser umzuleiten. Hierbei wird die Methode `window.location.replace();` verwendet, sodass die Seite, von der der Besucher umgeleitet wird, nicht im Browserverlauf gespeichert wird. Dieser Prozess ermöglicht Besuchern die Verwendung der Zurück-Schaltfläche in ihren Browsern.

>[!NOTE]
>
>Wenn Sie den Wert der verweisenden Stelle der Landingpage weitergeben möchten, verwenden Sie ein HTML-Angebot anstelle eines Umleitungsangebots.

## Erstellen eines Umleitungsangebots über die Seite [!UICONTROL Code-Angebote]

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.
1. Klicken Sie **[!UICONTROL Angebot erstellen]** > **[!UICONTROL Umleitungsangebot]**.
1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek [!UICONTROL Assets] aufzufinden.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto verfügen](/help/main/c-intro/intro.md#premium) wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Um dies zu verhindern, fügen Sie einen Abfrageparameter zur Umleitungs-URL hinzu (z. B. `?redirect=true`). Vergewissern Sie sich dann in der Audience-Aktivität oder in der Vorlagenregel, dass dieser Abfrageparameter nicht vorhanden ist. Dadurch wird sichergestellt, dass sich der Benutzer nach der Weiterleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **[!UICONTROL Alle URL-Parameter einschließen]:** Aktivieren Sie diese Option, wenn alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden sollen.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Sie möchten auch, dass die dynamischen Parameter in der URL übergeben werden, da mit dieser Methode verfolgt wird, ob Personen Ihre Site per E-Mail, Banner, Suchanzeige oder organisch erreicht haben. Wenn diese Option aktiviert ist, wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, sobald alle Eingaben im URL-Feld `https://www.mycompany.com/mensShirts.html` wurden.

   * **[!UICONTROL Sitzungs-ID der Mbox weitergeben]:** erforderlich, um zu einer anderen Domain umzuleiten. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass der `sessionId` automatisch in der Umleitung enthalten ist. Diese Option ist nur erforderlich, wenn Sie Klicks aus E-Mails oder von einer Domain zu einer anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie bei der Domain-übergreifenden Verwendung die Sitzungs-ID der Mbox nicht übergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie **[!UICONTROL Erstellen]**.

>[!IMPORTANT]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Erstellen eines Umleitungsangebots mit dem [!UICONTROL formularbasierten Experience Composer]

1. Wählen Sie beim Erstellen einer Aktivität mit [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Inhalt]** angezeigt werden soll.
1. Klicken Sie auf **[!UICONTROL Inhalt]** Dropdown-Liste, klicken Sie auf das Symbol **[!UICONTROL Liste]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Umleitungsangebot ändern]**.
1. Klicken Sie **[!UICONTROL Angebot erstellen]** > **[!UICONTROL Umleitungsangebot]**.
1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek [!UICONTROL Assets] aufzufinden.

1. Geben Sie die URL für den eindeutigen Inhalt oder das eindeutige Ziel an, zu dem Sie umleiten möchten. Diese URL muss eine absolute URL sein.

   >[!NOTE]
   >
   >Umleitungsangebote führen zu einer Endlosschleife, wenn die Umleitungs-URL auch den Benutzer für dieselbe Aktivität qualifiziert. Um dies zu verhindern, fügen Sie einen Abfrageparameter zur Umleitungs-URL hinzu (z. B. `?redirect=true`). Vergewissern Sie sich dann in der Audience-Aktivität oder in der Vorlagenregel, dass dieser Abfrageparameter nicht vorhanden ist. Dadurch wird sichergestellt, dass sich der Benutzer nach der Weiterleitung nicht erneut für die Aktivität qualifiziert.

1. Wählen Sie die gewünschten Optionen aus, um Ihr Umleitungsangebot anzupassen:

   * **[!UICONTROL Alle URL-Parameter einschließen]:** Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass alle auf der vorherigen Seite vorhandenen URL-Parameter auf die umgeleitete Seite übertragen werden.

     Wenn Sie beispielsweise Besucher von einer Seite für Herrenmode direkt zu einer Kategorieseite für Herrenhemden umleiten möchten. Sie möchten auch, dass die dynamischen Parameter in der URL übergeben werden, da mit dieser Methode verfolgt wird, ob Personen Ihre Site per E-Mail, Banner, Suchanzeige oder organisch erreicht haben. Wenn diese Option aktiviert ist, wird Ihr Umleitungsangebot auf Seite `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123`, sobald alle Eingaben im URL-Feld `https://www.mycompany.com/mensShirts.html` wurden.

   * **[!UICONTROL Sitzungs-ID der Mbox weitergeben]:** erforderlich, um zu einer anderen Domain umzuleiten. Schieben Sie den Umschalter, um diese Option zu aktivieren, wenn Sie möchten, dass der `sessionId` automatisch in der Umleitung enthalten ist. Diese Option ist nur erforderlich, wenn Sie Klicks aus E-Mails oder von einer Domain zu einer anderen testen. Die `sessionId` passt das Cookie des Besuchers an, damit der Besucher auch weiterhin verfolgt und der richtige Inhalt angezeigt werden kann.

     Wenn Sie die Einrichtung von Erstanbieter- und Drittanbieter-Cookies verwenden, müssen Sie bei der Domain-übergreifenden Verwendung die Sitzungs-ID der Mbox nicht übergeben. Sie bleibt beim Drittanbieter-Cookie erhalten, deshalb ist sie in der URL nicht erforderlich.

1. Klicken Sie **[!UICONTROL Erstellen]**.

>[!IMPORTANT]
>
>Fragen Sie Ihren Implementierungsberater, bevor Sie diese Tests starten.

## Verwenden von Umleitungsangeboten in -Aktivitäten

Anwenden von Umleitungsangeboten mit dem [[!UICONTROL formularbasierten Experience Composer]](/help/main/c-experiences/form-experience-composer.md). Umleitungsangebote können derzeit nicht mit dem [!UICONTROL Visual Experience Composer) (]) angewendet werden.

Der [!DNL Adobe Target] [!UICONTROL formularbasierte Experience Composer] ist eine nicht visuelle Oberfläche zur Erlebnis- und Angebotserstellung, die beim Erstellen von Erlebnissen für [!UICONTROL A/B-]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Recommendations]-Aktivitäten nützlich ist, wenn der [!UICONTROL Visual Experience Composer] nicht verfügbar oder unpraktisch in der Anwendung ist. Beispielsweise können Sie den [!UICONTROL formularbasierten Experience Composer) verwenden] um Erlebnisse zu erstellen, die Umleitungsangebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL formularbasierten Experience Composer].

   Unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) finden Sie detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Speicherort an und fügen Sie gegebenenfalls Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf **[!UICONTROL Inhalt]** Dropdown-Liste, klicken Sie auf das Symbol **[!UICONTROL Liste]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Umleitungsangebot ändern]**.
1. Wählen Sie das gewünschte Umleitungsangebot im Dialogfeld [!UICONTROL Umleitungsangebot auswählen] aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.
1. Schließen Sie die Konfiguration der Aktivität ab.
