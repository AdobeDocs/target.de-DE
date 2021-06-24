---
keywords: Fehlerbehebung;häufig gestellte Fragen;FAQ;FAQs;global;globale Mbox
description: Lesen Sie häufig gestellte Fragen (FAQs) und Antworten zur Adobe [!DNL Target] globalen Mboxes.
title: Welche häufig gestellten Fragen beantworten die globale Mbox?
feature: at.js
role: Developer
exl-id: ec8399df-5222-44bd-9e61-dfce8fd1694d
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 81%

---

# Häufig gestellte Fragen zu globalen Mboxes

Liste der häufig gestellten Fragen (FAQs) zu globalen Mboxes.

## Kann ich mehr als eine globale Mbox haben, wenn mein [!DNL Target]-Konto domänenübergreifend festgelegt ist? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Für Ihr Konto wird nur eine globale Mbox unterstützt.

Sie können den Ausführungsort Ihrer Aktivitäten beschränken, indem Sie Ihren Aktivitäten URL-Regeln hinzufügen. Weitere Informationen finden Sie unter [Gleiches Erlebnis auf ähnlichen Seiten](/help/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

Sie können auch mit [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) einen Parameter auf der Seite übergeben und dann diese Parameter im Abschnitt „URL konfigurieren“ im [!UICONTROL Visual Experience Composer] (VEC) auswählen. Alternativ können Sie die Parameter auch im formularbasierten Experience Composer als „Verfeinerungen“ hinzufügen.

## Wie übergebe ich Umsatzdaten an eine globale Mbox [!DNL Target]? {#section_17AEA933BADA4D169CCEDF5833C41306}

Zum Sammeln von Umsatz- und Auftragsinformationen in der target-global-mbox müssen „mbox-Parameter“ an Target gesendet werden. Bei diesen Parametern handelt es sich um Name/Wert-Paare, die zum Senden weiterer Informationen an Target verwendet werden. Target sucht diese Parameter (reservierte Namen) automatisch, um Umsatzdaten aufzufüllen.

Für die `orderConfirmPage` sollten Sie `orderTotal`, `orderId` und `productPurchasedId` weitergeben. 

Diese Parameter müssen über `targetPageParams()` an die target-global-mbox gesendet werden. Weitere Informationen finden Sie unter [Übergeben von Parametern an eine globale Mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).

Sie sollten dem Konversionsteil auch ein Targeting hinzufügen, sodass Target nur dann Konversionen für die target-global-mbox zählt, wenn die Auftragsbestätigungsseite angezeigt wurde, wie unten dargestellt:

![](assets/revenue1.png)

Der oben abgebildete Abschnitt „Webseiten“ enthält die folgenden Auswahlmöglichkeiten: „Aktuelle Seite“, „URL“, „contains“, „orderconfirm“.

![](assets/revenue2.png)

Die Optionen in der oben gezeigten Abbildung umfassen die folgenden Einstellungen:

* **Was möchten Sie mit dieser Aktivität messen:** Umsatz
* **Standardansicht für Berichte:** Umsatz pro Besucher
* **Welche Aktion hat Ihre Zielgruppe ausgeführt, um anzugeben, dass Ihr Ziel erreicht wurde?** Anzeige einer mbox, target-global-mbox
