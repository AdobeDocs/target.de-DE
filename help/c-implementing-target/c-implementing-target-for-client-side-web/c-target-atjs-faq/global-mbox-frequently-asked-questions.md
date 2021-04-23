---
keywords: Fehlerbehebung;häufig gestellte Fragen;FAQ;FAQs;global;globale Mbox
description: Lesen Sie häufig gestellte Fragen (FAQs) und Antworten zur Adobe [!DNL Target] globale Mboxes.
title: Was sind häufig gestellte Fragen zur globalen Mbox?
feature: 'at.js '
role: Developer
exl-id: ec8399df-5222-44bd-9e61-dfce8fd1694d
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 85%

---

# Häufig gestellte Fragen zu globalen Mboxes

Liste der häufig gestellten Fragen (FAQs) zu globalen Mboxes.

## Kann ich über mehr als eine globale Mbox verfügen, wenn mein [!DNL Target]-Konto über mehrere Domänen hinweg eingerichtet ist? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Für Ihr Konto wird nur eine globale Mbox unterstützt.

Sie können den Ausführungsort Ihrer Aktivitäten beschränken, indem Sie Ihren Aktivitäten URL-Regeln hinzufügen. Weitere Informationen finden Sie unter [Gleiches Erlebnis auf ähnlichen Seiten](/help/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

Sie können auch mit [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) einen Parameter auf der Seite übergeben und dann diese Parameter im Abschnitt „URL konfigurieren“ im [!UICONTROL Visual Experience Composer] (VEC) auswählen. Alternativ können Sie die Parameter auch im formularbasierten Experience Composer als „Verfeinerungen“ hinzufügen.

## Wie übergebe ich Umsatzdaten an eine globale Mbox [!DNL Target]? {#section_17AEA933BADA4D169CCEDF5833C41306}

Zum Sammeln von Umsatz- und Auftragsinformationen in der target-global-mbox müssen „mbox-Parameter“ an Target gesendet werden. Bei diesen Parametern handelt es sich um Name/Wert-Paare, die zum Senden weiterer Informationen an Target verwendet werden. Target sucht diese Parameter (reservierte Namen) automatisch, um Umsatzdaten aufzufüllen.

Für die `orderConfirmPage` sollten Sie `orderTotal`, `orderId` und `productPurchasedId` weitergeben. Weitere Informationen finden Sie unter [Erstellen einer Mbox für Auftragsbestätigungen – mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md#task_0036D5F6C062442788BB55E872816D82).

Dieselben Parameter müssen an die target-global-mbox via `targetPageParams()` gesendet werden. Weitere Informationen finden Sie unter [Übergeben von Parametern an eine globale Mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).

Sie sollten dem Konversionsteil auch ein Targeting hinzufügen, sodass Target nur dann Konversionen für die target-global-mbox zählt, wenn die Auftragsbestätigungsseite angezeigt wurde, wie unten dargestellt:

![](assets/revenue1.png)

Der oben abgebildete Abschnitt „Webseiten“ enthält die folgenden Auswahlmöglichkeiten: „Aktuelle Seite“, „URL“, „contains“, „orderconfirm“.

![](assets/revenue2.png)

Die Optionen in der oben gezeigten Abbildung umfassen die folgenden Einstellungen:

* **Was möchten Sie mit dieser Aktivität messen:** Umsatz
* **Standardansicht für Berichte:** Umsatz pro Besucher
* **Welche Aktion hat Ihre Zielgruppe ausgeführt, um anzugeben, dass Ihr Ziel erreicht wurde?** Anzeige einer mbox, target-global-mbox
