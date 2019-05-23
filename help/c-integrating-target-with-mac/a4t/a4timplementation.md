---
description: Zur Implementierung von Adobe Analytics als Berichterstellungsquelle für Target (A4T) sind einige Schritte erforderlich.
keywords: A4T; Adobe Analytics; Analytics-basierte Aktivität; Analytics Report Suite; Report Suite; Analytics-Target-Integration; Report Suite konfigurieren
seo-description: Zur Implementierung von Adobe Analytics als Berichterstellungsquelle für Target (A4T) sind einige Schritte erforderlich.
seo-title: Implementieren von Analytics for Target
solution: Target
title: Implementieren von Analytics for Target
topic: Premium
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: 1be00210754e8fa3237fdbccf48af625c2aafe65

---


# Implementieren von Analytics for Target{#analytics-for-target-implementation}

Zur Implementierung von Adobe Analytics als Berichterstellungsquelle für Target (A4T) sind einige Schritte erforderlich.

## Implementierungsschritte {#section_73961BAD5BB4430A95E073DE5C026277}

In der folgenden Tabelle werden die Schritte beschrieben, die für die Bereitstellung dieser Integration auf Ihrer Site ausgeführt werden müssen.

## Schritt 1: Anfordern der Bereitstellung für Analytics und Target

Nach der Implementierung von Analytics als Berichtsquelle für Target sind Sie auf die Bereitstellung von Analytics und Target angewiesen. [Verwenden Sie dieses Formular, um die Bereitstellung anzufordern](http://www.adobe.com/go/audiences).

## Schritt 2: Einrichten der Benutzerberechtigungen

Die Benutzerkontoanforderungen müssen erfüllt sein, bevor Sie eine Adobe Analytics-basierte Aktivität in Adobe Target erstellen können. Siehe   [Anforderungen hinsichtlich Benutzerberechtigungen](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Schritt 3: Implementieren des Experience Cloud-Besucher-ID-Service

Mit dem Besucher-ID-Service können Sie Benutzer über Experience Cloud-Lösungen hinweg identifizieren. Die erforderliche Version der Experience Cloud-Besucher-ID muss implementiert oder migriert werden. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Informationen finden Sie unter [Implementieren des Experience Cloud ID-Service mit Target](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-target.html) in der Dokumentation zum Experience Cloud-Besucher-ID-Service.

## Schritt 4: Aktualisierung von AppMeasurement für JavaScript oder s_code

Sie müssen die erforderliche Version von appMeasurement.js implementieren oder migrieren. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Weitere Informationen zu neuen Implementierungen finden Sie unter [Analytics JavaScript-Implementierung](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html).

Weitere Informationen zur Migration finden Sie unter [Migration zu AppMeasurement for JavaScript](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=appmeasure_mjs_migrate).

## Schritt 5: Herunterladen und Aktualisieren von at.js oder mbox.js

Sie müssen die erforderliche Version von at.js oder mbox.js mithilfe des Produktionskontos migrieren oder implementieren. Es müssen keine Änderungen am Code vorgenommen werden.

Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Schritt 6: Hosten von at.js oder mbox.js

Wenn Sie at.js oder mbox.js zuvor bereitgestellt haben, können Sie Ihre vorhandene Datei durch die aktualisierte Version ersetzen. Weitere Informationen finden Sie in den „Implementierungsanforderungen“ unter [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Alternativ kann diese Datei zusammen mit dem Besucher-ID-Service und AppMeasurement for JavaScript-Dateien gehostet werden. Diese Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Site zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien.

## Schritt 7: Verweisen auf at.js oder mbox.js auf allen Seiten der Website

Fügen Sie at.js oder mbox.js unterhalb der visitorAPI.js ein, indem Sie die folgende Codezeile <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> im Tag auf jeder Seite hinzufügen:

Für at.js:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Für mbox.js:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"></script>
```

Es ist wichtig, dass VisitorAPI.js vor at.js oder mbox.js geladen wird. Achten Sie daher beim Aktualisieren einer vorhandenen at.js- oder mbox.js-Datei darauf, dass die richtige Ladereihenfolge festgelegt ist.

## Schritt 8: Validieren der Implementierung

Laden Sie Ihre Seiten nach der Aktualisierung der JavaScript-Bibliotheken, um sicherzustellen, dass die mboxMCSDID-Parameterwerte in Target-Aufrufen mit dem sdid-Parameterwert im Analytics-Seitenansichtsaufruf übereinstimmen.

Dies ist besonders für einseitige Anwendungen (Single Page Applications, SPA) wichtig, bei denen die Reihenfolge der Aufrufe nicht immer vorhersehbar ist.

**Hinweis:** Diese Werte müssen übereinstimmen, um die korrekte Funktionsweise von A4T sicherzustellen.

## Schritt 9: (Optional) Entfernen des vorherigen Integrationscodes

Wir empfehlen, dass Sie die vorherige Integration entfernen, um Ihre Implementierung zu vereinfachen und die Notwendigkeit zur Regelung von Diskrepanzen zwischen den Systemen zu beseitigen. Sie können sämtlichen Code entfernen, den Sie für die vorherige Integration von SC zu T&amp;T bereitgestellt haben, einschließlich `mboxLoadSCPlugin`.

## Schritt 10: Aktivieren der Optionen für die Verwendung von Analytics als Berichtsquelle für Target

Klicken Sie in Target auf [!UICONTROL Setup &gt; Voreinstellungen], und wählen Sie entweder [!UICONTROL Pro Aktivität auswählen] oder [!UICONTROL Adobe Analytics] aus, um die Optionen zu aktivieren.

* Pro Aktivität auswählen ermöglicht Ihnen die Auswahl zwischen Target und Analytics beim Erstellen der einzelnen Aktivitäten.
* Adobe Analytics legt Analytics als Berichtsquelle für alle von Ihnen erstellten Aktivitäten fest.

