---
keywords: mobile App; Daten mit mobilen Apps senden; Targeting mobiler Apps; benutzerdefinierte Daten für Mobilbenutzer; benutzerdefinierte Daten für mobile Apps
description: Sie können weitere Informationen über Ort oder Benutzer als Namen-Wert-Paare an Target übermitteln.
title: IOS - Senden benutzerspezifischer Benutzerdaten
feature: Implement Mobile
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 98%

---


# iOS – Senden benutzerdefinierter Benutzerdaten{#ios-send-custom-user-data}

Sie können weitere Informationen über Ort oder Benutzer als Namen-Wert-Paare an Target übermitteln.

Mithilfe dieser Informationen können benutzerdefinierte Zielgruppen (beispielsweise Benutzer mit über 25.000 Meilen) und Berichte erstellt werden.

Es gibt zwei Parametertypen, die Sie mit einem Target-Aufruf übermitteln können:

* Mbox-Parameter

   Mbox-Parameter sind sitzungsübergreifend nicht beständig.
* Profilparameter

   Profilparameter werden im Besucherprofil gespeichert und sind sitzungsübergreifend beständig. Mbox-Parameter sind nicht beständig. Einige Schlüssel sind reserviert, es können jedoch sowohl Profil- als auch Mbox-Parameter als benutzerdefinierte Schlüsselwertpaare festgelegt werden.

Obwohl es einige reservierte Schlüssel gibt, können sowohl Profil- als auch Mbox-Parameter benutzerdefinierte Schlüsselwertpaare enthalten.

1. Erstellen Sie ein Wörterbuch.

   Erstellen Sie zunächst ein Wörterbuch mit den Werten, die Sie an Target übermitteln möchten. Fügen Sie dieses der Einfachheit halber der Methode `welcomeMessageCampaign` hinzu, sodass Sie sich keine Gedanken über den Geltungsbereich machen müssen.

   Im Folgenden finden Sie ein Beispiel für ein Wörterbuch. Sie können dies nach `(void)welcomeMessageCampaign` kopieren. Die Werte von Schlüsseln wie `userLevel` und `userMiles` sind in diesem Beispiel hartcodiert. Allgemein können Sie die entsprechenden Variablen übermitteln.

   ```
   NSDictionary *targetParams = [[NSDictionary alloc] initWithObjectsAndKeys: 
                                 @"platinum",@"userLevel", 
                                 @26500,@"userMiles", 
                                 @"1067007",@"entity.id", 
                                 @"dealsapp.qa", @"host", 
                                 @"fashion",@"entity.categoryId", 
                                 @"millenial", @"profile.persona", 
                                 @"cohort_5", @"profile.cohort", 
                                 nil];
   ```

   * Schlüssel mit Präfixprofil (beispielsweise `profile.persona`) werden im Benutzerprofil gespeichert.

      Diese Profilattribute können für verschiedene Aktivitäten und Kanäle übergreifend eingesetzt werden.

   * Bei Schlüsseln ohne Präfix (beispielsweise `userMiles`) handelt es sich um Mbox-Parameter.

      Diese Parameter sind nur während der Sitzung verfügbar.

   * Schlüssel mit Präfixentität (beispielsweise `entity.category.id`) werden für Produktempfehlungen eingesetzt.

1. Prüfen Sie die Daten.
   1. Entfernen Sie in der Anwendung `didFinishLaunchingWithOptions` den Kommentar oder fügen Sie `[ADBMobile setDebugLogging:YES];` hinzu.

      Durch diese Aktion werden detaillierte Debugging-Protokolle erstellt.
   1. Erstellen Sie die Anwendung.
   1. Prüfen Sie, dass die Parameter im Target-Aufruf übermittelt werden.

      Suchen Sie in Ihrer Debugging-Konsole nach dem Namen Ihres Zielorts. Es wird ein `YOUR-CLIENT-CODE.tt.omtrdc.net` mit allen soeben übermittelten Parametern angezeigt.

      ![](assets/mobile-debug.png)
   Sie können Zielgruppen erstellen und die Anzeige von Inhalten einschränken oder auf eine bestimmte Zielgruppe ausrichten, indem Sie die Parameter in Target Standard verwenden.
