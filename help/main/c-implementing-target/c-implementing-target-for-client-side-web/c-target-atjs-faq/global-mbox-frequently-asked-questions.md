---
keywords: Fehlerbehebung;häufig gestellte Fragen;FAQ;FAQs;global;globale Mbox
description: Häufig gestellte Fragen (FAQs) und Antworten zur Adobe lesen [!DNL Target] globale Mboxes.
title: Welche häufig gestellten Fragen beantworten die globale Mbox?
feature: at.js
role: Developer
exl-id: ec8399df-5222-44bd-9e61-dfce8fd1694d
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 60%

---

# Häufig gestellte Fragen zu globalen Mboxes

Liste der häufig gestellten Fragen (FAQs) zu globalen Mboxes.

## Kann ich mehr als eine globale Mbox haben, wenn meine [!DNL Target] -Konto über mehrere Domänen hinweg festgelegt ist? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Für Ihr Konto wird nur eine globale Mbox unterstützt.

Sie können den Ausführungsort Ihrer Aktivitäten beschränken, indem Sie Ihren Aktivitäten URL-Regeln hinzufügen. Weitere Informationen finden Sie unter [Gleiches Erlebnis auf ähnlichen Seiten](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

Sie können auch einen Parameter auf der Seite mit [targetPageParams](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/){target=_blank} und wählen Sie diese Parameter im Abschnitt &quot;URL konfigurieren&quot;im [!UICONTROL Visual Experience Composer] (VEC){target=_blank} oder indem Sie die Parameter im formularbasierten Experience Composer als &quot;Verfeinerungen&quot;hinzufügen.

## Wie übergebe ich Umsatzdaten an eine [!DNL Target] globale Mbox? {#section_17AEA933BADA4D169CCEDF5833C41306}

Zum Sammeln von Umsatz- und Auftragsinformationen in der target-global-mbox müssen „mbox-Parameter“ an Target gesendet werden. Bei diesen Parametern handelt es sich um Name/Wert-Paare, die zum Senden weiterer Informationen an Target verwendet werden. Target sucht diese Parameter (reservierte Namen) automatisch, um Umsatzdaten aufzufüllen.

Für die `orderConfirmPage` sollten Sie `orderTotal`, `orderId` und `productPurchasedId` weitergeben. 

Diese Parameter müssen an die target-global-mbox über `targetPageParams()`. Weitere Informationen finden Sie unter [Übergeben von Parametern an eine globale Mbox](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/){target=_blank}.

Sie sollten dem Konversionsteil auch ein Targeting hinzufügen, sodass Target nur dann Konversionen für die target-global-mbox zählt, wenn die Auftragsbestätigungsseite angezeigt wurde, wie unten dargestellt:

![](assets/revenue1.png)

Der oben abgebildete Abschnitt „Webseiten“ enthält die folgenden Auswahlmöglichkeiten: „Aktuelle Seite“, „URL“, „contains“, „orderconfirm“.

![](assets/revenue2.png)

Die Optionen in der oben gezeigten Abbildung umfassen die folgenden Einstellungen:

* **Was möchten Sie mit dieser Aktivität messen:** Umsatz
* **Standardansicht für Berichte:** Umsatz pro Besucher
* **Welche Aktion hat Ihre Zielgruppe ausgeführt, um anzugeben, dass Ihr Ziel erreicht wurde?** Anzeige einer mbox, target-global-mbox
