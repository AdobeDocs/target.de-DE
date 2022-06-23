---
keywords: qa; Vorschau; Vorschau-Link; mobil; mobile Vorschau
description: Verwenden Sie Vorschaulinks für Mobilgeräte, um eine durchgängige Qualitätssicherung für Aktivitäten mobiler Apps durchzuführen. Sie können sich ohne spezielle Testgeräte für verschiedene Erlebnisse anmelden.
title: Wie verwende ich den Vorschau-Link für Mobilgeräte in [!DNL Target] Mobil?
feature: Implement Mobile
role: Developer
exl-id: c66325b3-3995-401e-a1e3-839fdb1cf762
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 82%

---

# Mobile Target-Vorschau

Verwenden Sie die Vorschau für mobile Apps, um mühelos eine ganzheitliche Qualitätssicherung für Aktivitäten von mobilen Apps durchzuführen und sich ohne spezielle Prüfmittel direkt auf Ihrem Gerät für verschiedene Erlebnisse anzumelden.

>[!NOTE]
>
>Für die Vorschaufunktion für die Mobilversion ist es erforderlich, dass Sie die entsprechende Version 4.14 (oder später) des Adobe Mobile-SDK herunterladen und installieren.

## Überblick {#section_981D6FA4AEE64098809EA606E89E4A5E}

Mit der mobilen Vorschaufunktionalität können Sie Aktivitäten in Ihrer mobilen App vollständig testen, bevor Sie sie live schalten.

## Voraussetzungen  {#section_A763C564C9E84B0EB448237B5B1E4068}

1. **Verwenden Sie eine unterstützte Version des SDK:** Für die mobile Vorschaufunktion ist es erforderlich, dass Sie die entsprechende Version 4.14 (oder später) des Adobe Mobile-SDK in Ihren jeweiligen Apps herunterladen.

   Eine Anleitung zum Herunterladen des erforderlichen SDK finden Sie unter:

   * **iOS:** [Vorbereitung](https://experienceleague.adobe.com/docs/mobile-services/ios/getting-started-ios/requirements.html) im *Hilfe zu Mobile Services iOS*.
   * **Android:** [Vorbereitung](https://experienceleague.adobe.com/docs/mobile-services/android/getting-started-android/requirements.html) im *Hilfe zu Mobile Services für Android*.

1. **URL-Schema einrichten:** Der Vorschau-Link öffnet Ihre App über ein URL-Schema. Sie müssen ein einzigartiges URL-Schema für die Vorschau festlegen.

   Die folgende Illustration stellt ein Beispiel unter iOS dar:

   ![](assets/mobile-preview-url-scheme-ios.png)

   Die folgende Illustration stellt ein Beispiel unter Android dar:

   ![](assets/Android_Deeplink.png)

1. **Adobe DeepLink verfolgen**

   **iOS:** Rufen Sie in App Delegate `[ADBMobile trackAdobeDeepLink:url` auf, wenn der Delegate dazu aufgefordert wird, die Ressource mit dem URL-Schema zu öffnen, das im vorherigen Schritt angegeben wurde.

   Das folgende Code-Snippet dient als Beispiel:

   ```javascript
   - (BOOL) application:(UIApplication *)app openURL:(NSURL *)url 
                options:(NSDictionary<NSString *,id> *)options { 
   
       if ([[url scheme] isEqualToString:@"com.adobe.targetmobile"]) { 
           [ADBMobile trackAdobeDeepLink:url]; 
           return YES; 
       } 
       return NO; 
   } 
   ```

   **Android:** Rufen Sie in der App `Config.trackAdobeDeepLink(URL);` auf, wenn der Aufrufende dazu aufgefordert wird, die Ressource mit dem URL-Schema zu öffnen, das im vorherigen Schritt angegeben wurde.

   ```javascript
    private Boolean shouldOpenDeeplinkUrl() { 
        Intent appLinkIntent = getIntent(); 
        String appLinkAction = appLinkIntent.getAction(); 
        Uri appLinkData = appLinkIntent.getData; 
        if (appLinkData.toString().startsWith("com.adobe.targetmobile")) { 
            Config.trackAdobeDeepLink(appLinkData); 
            return true; 
        } 
        return false; 
     }
   ```

   Damit die Mobile-Vorschau für Android funktioniert, müssen Sie außerdem das folgende Codefragment in [!DNL AndroidManifest.xml] bei Verwendung von Adobe Mobile SDK Version 5:

   ```javascript
   <activity android:name="com.adobe.marketing.mobile.FullscreenMessageActivity" />
   ```

   Wenn Sie Version 4 des Adobe Mobile SDK verwenden, verwenden Sie folgendes Codefragment:

   ```javascript
   <activity android:name="com.adobe.mobile.MessageFullScreenActivity" />
   ```

## Einen Vorschau-Link erstellen {#section_D9D58173FFF34E9BB75EBF357273F128}

1. Klicken Sie in der Target-Benutzeroberfläche auf das Symbol **[!UICONTROL Weitere Optionen]** (drei vertikale Ellipsen) und wählen Sie dann **[!UICONTROL Vorschau für Mobilversion erzeugen]**.

   ![](assets/mobile-preview-create.png)

1. Wählen Sie die Aktivitäten aus, für die Sie eine Vorschau anzeigen möchten, und klicken Sie dann auf **[!UICONTROL Vorschaulink für Mobilversion erzeugen]**.

   >[!NOTE]
   >
   >Es können nur formularbasierte AB- und XT-Aktivitäten ausgewählt werden.

   ![](assets/mobile-preview-select-activities.png)

1. Legen Sie das URL-Schema Ihrer App fest.

   Dieses muss dem Schema in Ihrer iOS- oder Android-App entsprechen. Wiederholen Sie diesen Vorgang bei Bedarf einzeln für iOS und Android.

   ![](assets/mobile-preview-enter-url-scheme.png)

1. Klicken Sie auf **[!UICONTROL Vorschaulink für Mobilversion erzeugen]** und kopieren Sie den Link.

   ![](assets/mobile-preview-generate-and-copy.png)

## Vorschau auf Ihrem Gerät {#section_521F0D46F3DE4A2A98283A1B73FF69F6}

Öffnen Sie den Link in einem mobilen Browser auf einem Gerät, auf dem Ihre App installiert ist. Bei dieser App kann es sich um die aus dem Apple App Store oder dem Google Play Store heruntergeladene Produktions-App handeln. Es muss keine speziell erstellte Version sein. Wenn Sie einen aktiven Vorschaulink haben, können Sie über das Gerät auf die Erlebnisse zugreifen.

1. Öffnen Sie den Link in Ihrem mobilen Browser.

   Geben Sie den Link, den Sie im vorangegangenen Schritt aus der Target-Benutzeroberfläche kopiert haben, auf Ihrem mobilen Gerät frei. Nutzen Sie dazu eine beliebige bequeme Möglichkeit, beispielsweise eine SMS, eine E-Mail oder Slack.

   |![Vorschau Deep Link 1](/help/main/c-target-mobile-app/assets/mobile-preview-open-deeplink.png)|![Vorschau Deep Link 2](/help/main/c-target-mobile-app/assets/mobile-preview-open-app.png)|

   Ihre App wird geöffnet und führt den mobilen Vorschau-Modus von Target aus.

1. Wählen Sie die Kombination aus Erlebnissen aus, die Sie sehen möchten, und klicken Sie auf **[!UICONTROL Erlebnisse starten]**.

   |![mobile preview 1](/help/main/c-target-mobile-app/assets/mobile-preview-experience-selection-1.png)|![mobile Vorschau 2](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-1-france.png)|![mobile Vorschau 3](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-1-shipfree.png)|
|![mobile Vorschau 4](/help/main/c-target-mobile-app/assets/mobile-preview-experience-selection-2.png)|![mobile Vorschau 5](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-2-aus.png)|![mobile Vorschau 6](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-2-10off.png)|

## Einschränkungen   {#section_4E9BDED0F718485292527EFB508305BD}

* Die Ansicht muss erneut laden, damit der neue Inhalt angezeigt werden kann, nachdem die Schaltfläche [!UICONTROL Erlebnisse starten] aktiviert wurde. Die einfachste Möglichkeit ist, zu einem anderen Bildschirm zu wechseln und danach zu dem Bildschirm zurückzukehren, auf dem die Änderung bewirkt werden soll.
* Die mobile Vorschau wird nicht für frühere Android-Versionen als API-19 (KitKat) unterstützt.
