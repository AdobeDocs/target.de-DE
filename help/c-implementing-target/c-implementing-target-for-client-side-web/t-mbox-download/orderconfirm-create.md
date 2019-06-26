---
description: Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.
keywords: Bestellbestätigung;orderConfirmPage
seo-description: Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.
seo-title: Erstellen einer Mbox für Auftragsbestätigungen – mbox.js
solution: Target
subtopic: Erste Schritte
title: Erstellen einer Mbox für Auftragsbestätigungen – mbox.js
uuid: 001da2bd-2ccf-490b-ba84-ac9b9a2a5451
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Erstellen einer Mbox für Auftragsbestätigungen – mbox.js{#create-an-order-confirmation-mbox-mbox-js}

Mit der Mbox für Auftragsbestätigungen werden Informationen zu Bestellungen auf Ihrer Seite gesammelt und die Berichterstellung basierend auf Umsatz und Aufträgen ermöglicht. Mit der Mbox für Auftragsbestätigungen können zudem Empfehlungsalgorithmen abgeleitet werden, beispielsweise „Personen, die x kauften, kauften auch y“.

>[!NOTE]
>
>Tätigen Benutzer auf Ihrer Website Einkäufe, empfehlen wir die Implementierung einer Auftragsbestätigungs-Mbox, selbst wenn Sie für die Berichterstellung Analytics for Target (A4T) einsetzen.

>[!NOTE]
>
>Sie können eine Auftragsbestätigungs-Mbox für auch mit dieser Methode erstellen, die [!DNL at.js]-Methode wird jedoch empfohlen. Weitere Informationen finden Sie unter [Konversions-Tracking](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).

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