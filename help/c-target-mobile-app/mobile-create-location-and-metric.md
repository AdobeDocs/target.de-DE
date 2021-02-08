---
keywords: mobile App; Ort der mobilen App; Targeting mobiler Apps; mobile Zielstandorte; Erfolgsmetriken für mobile Apps
description: Beispielcode für die Ansicht, mit dem Sie lernen können, wie Orte und Erfolgsmetriken in iOS-Apps erstellt werden, damit Sie mit Adobe Target Ihre App personalisieren und optimieren können.
title: Wie erstelle ich Orte und Erfolgsmetriken für Zielgruppen in einer iOS-App?
feature: Implement Mobile
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 83%

---


# iOS – Erstellen von Target-Standorten und Erfolgsmetriken{#ios-create-a-target-location-and-success-metric}

Möchten Sie Target in Ihrer mobilen App verwenden, erstellen Sie einen Ort und eine Erfolgsmetrik.

In diesem Abschnitt finden Sie Beispiel-Code, der als Vorlage für Ihre App verwendet werden kann. Die Beispiele in diesem Abschnitt enthalten Code für iOS. Die gleichen Muster gelten jedoch auch für Android. Die Android-spezifische Syntax finden Sie im Lösungsleitfaden [](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/target-main.html)Android SDK 4.x für Experience Cloud.

>[!NOTE]
>
>Eine Liste aller verfügbaren Zielgruppen finden Sie in der [Mobildokumentation](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-target-methods.html).

Möchten Sie einen Target-Ort in Ihrer Anwendung erstellen und eine Abfrage stellen, gibt es hierfür zwei Hauptverfahren:

* `targetCreateRequestWithName`
* `targetLoadRequest`

1. Erstellen Sie einen Target-Ort.

   Hier finden Sie ein Aufrufbeispiel für die Erstellung einer Abfrage:

   ```
   // make your request 
   ADBTargetLocationRequest *myRequest = [ADBMobile targetCreateRequestWithName:@"heroBanner" 
                                                    defaultContent:@"default.png" 
                                                    parameters:nil];
   ```

   | Parameter | Beschreibung |
   |---|---|
   | `ADBTargetLocationRequest *myRequest` | Ersetzen Sie `myRequest` durch den Namen Ihrer `targetLocation` in der App. |
   | `targetCreateRequestWithName:@"heroBanner"` | Ersetzen Sie `heroBanner` durch den Namen Ihrer `targetLocation` in Target. Es handelt sich hierbei auch um den Namen der mbox. Dieses Hero-Banner wird in der Target-Oberfläche angezeigt. |
   | `defaultContent:@"default.png"` | Ersetzen Sie `default.png` durch den Wert, den die App nutzt, falls Target nicht reagiert. |
   | `parameters:nil` | Legen Sie Profil- oder Mbox-Parameter fest. Weitere Informationen finden Sie im Abschnitt über das Übermitteln benutzerdefinierter Daten. |

   Hier finden Sie ein Aufrufbeispiel für das Laden einer Abfrage:

   ```
   // load your request 
   [ADBMobile targetLoadRequest:myRequest callback:^(NSString *content) { 
                                        // do something with content 
                                        heroImage.image = [UIImage imageNamed:content]; 
   }];
   ```

   | Parameter | Beschreibung |
   |---|---|
   | `targetLoadRequest:myRequest` | Ersetzen Sie `myRequest` durch den Namen Ihrer `targetLocation` in der App. |
   | `NSString *content` | Ersetzen Sie Inhalte durch tatsächliche Inhalte, die von Adobe zurückgegeben werden. Die Zeichenfolge kann eine XML-, JSON- oder eine einfache Zeichenfolge sein. Verwenden Sie diesen Codeabschnitt für das Festlegen von Variablen, von Bildpfaden, zur Ansicht von Kontrollflüssen, Transaktionspunkten und anderen gewünschten Aktionen. Target gibt den in der UI eingegebenen Inhalt im selben Format zurück. |
   | `heroImage.image = [UIImage imageNamed:content];` | Beispiel: Nehmen Sie Inhalte und legen Sie den Pfad für ein Hero Image fest. |

1. Erstellen Sie eine Erfolgsmetrik.

   Mit der Methode `targetCreateOrderConfirmRequestWithName` können Sie Konversions-/Erfolgsmetriken in Ihrer App verfolgen.

   ```
   ADBTargetLocationRequest *req = [ADBMobile targetCreateOrderConfirmRequestWithName: "orderConfirm" 
                                              orderId: orderId 
                                              orderTotal: @"39.95" 
                                              productPurchasedId: _galleryItem.title 
                                              parameters: nil]; 
   [ADBMobile targetLoadRequest: req callback: nil];
   ```

   | Parameter | Beschreibung |
   |---|---|
   | `orderId` | Ersetzen Sie sie durch eine dynamische Variable, die für eine eindeutige Bestell-ID steht. |
   | `@"39.95"` | Ersetzen Sie sie durch eine dynamische Variable, die für eine eindeutige Bestellsumme steht. |
   | `_galleryItem.title` | Ersetzen Sie sie durch eine dynamische Variable, die für eine kommagetrennte Liste der erworbenen Produkte steht. |
   | `parameters: nil` | Optionales Wörterbuch weiterer Parameter |

1. Erstellen Sie die Anwendung.

   Führen Sie einen A/B-Test durch, nachdem Sie einen Zielort erstellt und eine Erfolgsmetrik getaggt haben. Die Aktivität kann als Form-based Experience Composer verwendet werden.
