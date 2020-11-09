---
description: Die Art, mit der Target Aufrufe an Ihre Seite sendet und auf Aufrufe der Seite antwortet, hängt von der Version der verwendeten Target-Bibliothek ab und davon, ob die Implementierung der Experience Cloud-Besucher-ID und die Besucher-ID vorhanden sind.
title: Target-Seitenmethoden nach „mbox.js“-Bibliotheksversion
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 100%

---


# Target-Seitenmethoden nach „mbox.js“-Bibliotheksversion{#target-page-methods-by-mbox-js-library-version}

Die Art, mit der Target Aufrufe an Ihre Seite sendet und auf Aufrufe der Seite antwortet, hängt von der Version der verwendeten Target-Bibliothek ab und davon, ob die Implementierung der Experience Cloud-Besucher-ID und die Besucher-ID vorhanden sind.

>[!NOTE]
>
>Wenn Sie [!DNL at.js] verwenden, erfolgen sämtliche Aufrufe über JSON. Auf dieser Seite finden Sie Einzelheiten zu verschiedenen [!DNL mbox.js]-Bibliotheksversionen. Das in den folgenden Szenarien beschriebene Verhalten trifft nicht auf [!DNL at.js] zu.

Dieser Abschnitt gibt Auskunft darüber, wie die einzelnen Versionen der [!DNL Target]-Bibliothek auf den [!DNL Target]-Aufruf Ihrer Seite in den folgenden Szenarien antworten.

Es gibt viele verschiedene Typen von Endpunkten, abhängig von Ihrer Implementierung und Bibliotheksversion. Sie sollten sich mit allen Typen auskennen, um zu verstehen, wie [!DNL Target] in den verschiedenen Szenarien auf Aufrufe antwortet.

| Typ/Endpunkt | Aufrufmethode | Inhalt der Antwort |
|--- |--- |--- |
| Globale Mbox automatisch erstellen - synchron | „document.write“ für Aufruf | JavaScript ohne document.write() |
| Globale Mbox automatisch erstellen - asynchron | createElement() zum Anfügen des Aufrufs an „body“ | JavaScript ohne document.write() |
| Standard | „document.write“ für Aufruf | JavaScript mit document.write() |
| ajax | createElement() zum Anfügen des Aufrufs an „body“ | JavaScript ohne document.write() |
| json | XMLHTTPrequest() für Aufruf | gibt JSON-Antwort zurück |

>[!IMPORTANT]
>
>Für alle Typen mit Ausnahme des Standardtyps gilt, dass sämtlicher benutzerdefinierter Code und Angebote mit Unterstützung für eine AJAX-Umgebung geschrieben werden sollten. Wenn Sie zum Beispiel ein JavaScript verwenden, das `document.write()` enthält, funktioniert es nicht erwartungsgemäß.

## Keine Implementierung der Besucher-ID {#section_C6F7213FDE4D48E8BBCB1A9A26310FEE}

Wenn Sie [!DNL Target Standard] oder [!DNL Premium] mit [!DNL mbox.js] verwenden und [!UICONTROL Globale Mbox erstellen] für Ihr Konto aktiviert haben, erfolgen Aufruf und Antwort unabhängig von der verwendeten **-Version als Typ** globale Mbox automatisch erstellen - synchron[!DNL mbox.js].

Wenn Sie Ihren eigenen Code statt der Aktionen in [!UICONTROL Visual Experience Composer] verwenden, achten Sie darauf, dass dieser für eine AJAX-Umgebung geeignet ist. Wenn Sie zum Beispiel ein JavaScript verwenden, das `document.write()` enthält, funktioniert es nicht erwartungsgemäß.

>[!NOTE]
>
>Mehrere AJAX-Mbox-Aufrufe mit demselben Mbox-Namen, jedoch verschiedenen Parametern auf derselben Seite funktionieren nicht. Nur der erste Aufruf erfolgt.

Wenn Sie „Globale Mbox automatisch erstellen“ verwenden, sich darüber hinaus aber noch `mboxCreate`-Aufrufe auf Ihrer Seite befinden – etwa wenn Sie [!DNL Target Standard] oder [!DNL Premium] auf einer Seite implementieren, auf der zuvor eine ältere Implementierung zum Einsatz kam –, erfolgen die globalen Mbox-Aufrufe anhand des Endpunkts **autocreate global mbox - standard** und `mboxCreate`-Aufrufe mithilfe des Endpunkts **Standard**. Der Endpunkt **Standard** greift für den Aufruf und die Antwort auf `document.write()` zurück. Dadurch wird das Laden der Seite und aller Inhalte, die in der AJAX-Antwort bereitgestellt werden, verhindert, bis sämtliche Informationen heruntergeladen wurden.

Wenn Sie mboxCreate nutzen, etwa auf Seiten, die mithilfe von [!DNL Target Classic] erstellt wurden, funktioniert die Seite wie immer.

| Erstellungsmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| Globale Mbox automatisch erstellen | Globale Mbox automatisch erstellen - synchron | Globale Mbox automatisch erstellen - synchron | Globale Mbox automatisch erstellen - synchron | Globale Mbox automatisch erstellen - synchron |
| mboxCreate | Standard | Standard | Standard | Standard |

## Implementierung der Besucher-ID vorhanden, jedoch keine Besucher-ID festgelegt  {#section_29888A119C7A4753AD287FC845AA63F4}

Wenn keine Besucher-ID festgelegt wurde, steht kein [!DNL Experience Cloud]-Besuchercookie für den Benutzer bereit. Die Seite sendet einen Aufruf an den Besucher-ID-Service, um die Besucher-ID zu erhalten. wartet auf die Antwort mit der ID, bevor ein Aufruf an [!DNL Target]Target erfolgt.

>[!NOTE]
>
>Version 58 von [!DNL Mbox.js] wird dringend empfohlen, um sicherzustellen, dass die Besucher-ID zurückgegeben wird, bevor der Target-Aufruf erfolgt.

Wenn Sie in diesem Szenario Version 57 von [!DNL mbox.js] verwenden, funktioniert alles so, als gäbe es keine Implementierung der Besucher-ID, wie im vorherigen Szenario beschrieben. Ab [!DNL mbox.js], Version 58, gibt der [!DNL Experience Cloud Visitor ID]-Dienst eine Besucher-ID zurück, bevor [!DNL Target]-Aufrufe durchgeführt werden. Dadurch wird sichergestellt, dass die Zielgruppendaten, die über die Profil- und Zielgruppen-Kerndienste freigegeben werden, für den ersten [!DNL Target]-Aufruf in der Benutzersitzung zur Verfügung stehen. Um das Flackern von Standardinhalten vor der Rückgabe der Testinhalte zu vermeiden, blendet [!DNL Target] den `<BODY>` aus, bis der Besucher-ID-Service antwortet. In Version 58 kommt `display:none` zum Einsatz, um die Seite zu verstecken. Dies kann zu Problemen mit einigen responsiven Websites führen, weshalb ab Version 59 `opacity:0` zum Verstecken von Inhalten verwendet wird.

| Erstellungsmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| Globale Mbox automatisch erstellen | Globale Mbox automatisch erstellen - synchron | Globale Mbox automatisch erstellen - asynchron | Globale Mbox automatisch erstellen - asynchron | Globale Mbox automatisch erstellen - asynchron |
| mboxCreate | Standard | ajax | ajax | ajax |

## Sowohl Implementierung der Besucher-ID als auch Besucher-ID vorhanden  {#section_9CD4AE4C8186425D886398BC3CE6C46D}

Ist das Besucher-ID-Cookie vorhanden, muss [!DNL Target] keinen Aufruf an den Besucher-ID-Service richten. In diesem Fall muss nicht auf den Besucher-ID-Service gewartet werden, bevor Inhalte angezeigt werden können. In den Versionen 57 bis 59 wird der Typ **Globale Mbox automatisch erstellen - synchron** verwendet, weshalb die Seite nach dem Aufruf an [!DNL Target] auf die Antwort wartet, bevor sie weiter lädt. Dies gewährleistet, dass kein Flimmern bei den Standardinhalten entsteht. Bei Version 60 kommt der Typ **Globale Mbox - asynchron** zum Einsatz, um sicherzustellen, dass [!DNL Target] auf die Antwort des [!DNL Experience Cloud]-Abmeldeservice wartet. Der Abmeldeservice ist Teil der Datenkooperation, die im Herbst 2016 veröffentlicht wird. Da auf alle Aufrufe über AJAX geantwortet wird, sollte `document.write()` nicht mit Version 60 von [!DNL mbox.js] verwendet werden.

| Erstellungsmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| Globale Mbox automatisch erstellen | Globale Mbox automatisch erstellen - synchron | Globale Mbox automatisch erstellen - synchron | Globale Mbox automatisch erstellen - synchron | Globale Mbox automatisch erstellen - asynchron (zur Unterstützung der Entwicklung der Datenkooperation, die im Herbst 2016 veröffentlicht wird) |
| mboxCreate | Standard | Standard | Standard | ajax |