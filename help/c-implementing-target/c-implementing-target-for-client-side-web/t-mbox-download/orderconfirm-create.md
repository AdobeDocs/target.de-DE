---
keywords: Bestellbestätigung;orderConfirmPage
description: Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.
title: Erstellen einer Mbox für Auftragsbestätigungen – mbox.js
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 69%

---


# Erstellen einer Mbox für Auftragsbestätigungen – mbox.js

Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

>[!NOTE]
>
>* Tätigen Benutzer auf Ihrer Website Einkäufe, empfehlen wir die Implementierung einer Auftragsbestätigungs-Mbox, selbst wenn Sie für die Berichterstellung Analytics for Target (A4T) einsetzen.
   >
   >
* Sie können auch eine Auftragsbestätigungs-mbox für &quot;at.js 1&quot;erstellen.*Verwendung* derselben Methode; jedoch wird die  [!DNL at.js] Methode bevorzugt. Weitere Informationen finden Sie unter [Konversions-Tracking](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).
   >
   >
* Wenn Sie at.js 2 verwenden.*x*,  `mboxCreate` wird nicht mehr unterstützt. Zur Auftragsbestätigung mit at.js 2.*x* verwenden Sie die folgenden tracking-bezogenen APIs:  [trackEvent()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md)  und  [sendNotifications()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).


1. Fügen Sie auf Ihrer Bestellungsdetailseite das Mbox-Skript ein. Befolgen Sie dabei das folgende Modell:
1. Ersetzen Sie die WORTE IN GROSSBUCHSTABEN entweder durch dynamische oder statische Werte aus Ihrem Katalog.

   >[!NOTE]
   >
   >Trennen Sie mehrere Produkt-IDs mithilfe von Kommas.

   **Tipp:** Sie können Informationen auch in beliebigen anderen Mboxes senden (sie müssen nicht `orderConfirmPage` genannt werden). Darüber hinaus können Bestellinformationen auch an mehrere Mboxes innerhalb derselben Kampagne weitergegeben werden.

   ```
   <div class="mboxDefault"> 
      <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
   </div> 
   <script type="text/javascript">    
      mboxCreate('orderConfirmPage', 
      'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
      'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
      'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
   </script> 
   ```

Die Mbox für die Auftragsbestätigung verwendet die folgenden Parameter:

| Parameter | Beschreibung |
|--- |--- |
| `orderId` | Eindeutiger Wert zur Identifizierung einer Bestellung für die Konversionszählung.<br>`orderId` muss eindeutig sein. Doppelte Bestellungen werden in Berichten ignoriert. |
| `orderTotal` | Geldwert des Einkaufs.<br>Das Währungssymbol wird nicht übergeben. Verwenden Sie einen Dezimalpunkt (kein Komma), um die Dezimalwerte anzugeben. |
| `productPurchasedId` (Optional) | Kommagetrennte Liste von Produkt-IDs, die innerhalb der Bestellung gekauft wurden.<br>Diese Produkt-IDs werden im Audit-Bericht angezeigt, um die zusätzliche Berichtanalyse zu unterstützen. |