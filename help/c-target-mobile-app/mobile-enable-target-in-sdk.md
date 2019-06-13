---
description: Fügen Sie Ihrer Anwendung das Adobe Mobile Services SDK hinzu.
keywords: mobile App; mobile app sdk; Targeting mobiler Apps; mobile target sdk; mobile app sdk; target in sdk aktivieren
seo-description: Fügen Sie Ihrer Anwendung das Adobe Mobile Services SDK hinzu.
seo-title: Aktivieren von Target im SDK
title: Aktivieren von Target im SDK
topic: Target
uuid: 673dd5c7-9c09-4a6e-bc41-c6ad27cf269c
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Aktivieren Sie Target im SDK{#enable-target-in-the-sdk}

Fügen Sie Ihrer Anwendung das Adobe Mobile Services SDK hinzu.

1. Wenn Sie das Adobe Mobile Services SDK nicht in Ihrer App installiert haben, verwenden Sie Ihre Analytics- oder Experience Cloud-Anmeldeinformationen und laden Sie das SDK von der [Adobe Mobile Services](https://mobilemarketing.adobe.com)-Website herunter.

1. Fügen Sie Ihrer Anwendung das Adobe Mobile Services SDK hinzu.

   Anweisungen finden Sie unter [Kernimplementierung und Lebenszyklus](https://marketing.adobe.com/resources/help/de_DE/mobile/ios/dev_qs.html).
1. Fügen Sie Kunden-Code und Zeitüberschreitung hinzu und aktivieren Sie SSL.

   Öffnen Sie Mobile Services in Experience Cloud und wechseln Sie dann zu **[!UICONTROL Verwaltung der App-Einstellungen]** &gt; **[!UICONTROL SDK-Target-Optionen]**.

   Fügen Sie Kunden-Code und Zeitüberschreitung für Target hinzu. Der Kunden-Code ist ein eindeutiger Code für Ihr Konto oder Unternehmen. Die Zeitüberschreitung ist die Dauer in Anzahl der Sekunden, die Target auf eine Antwort wartet, bevor der Standardinhalt angezeigt wird. Stellen Sie sicher, dass Sie die Option **[!UICONTROL HTTPS verwenden]** auf der Seite „App-Einstellungen verwalten“ in Adobe Mobile Services aktiviert haben. Ist HTTPS nicht aktiviert, werden alle Aufrufe ab iOS9 blockiert, außer sie werden auf die Whitelist des Target-Servers gesetzt.

   ![](assets/mobile-clientcode.png)

1. Haben Sie Ihre App erstellt/gefunden, suchen Sie die Anwendungseinstellungen und laden Sie das gewünschte SDK herunter.

   ![](assets/download-sdk.png)

>[!IMPORTANT]
>
> Wenn Sie keinen Zugriff auf die mobile Marketing-Oberfläche haben, können Sie Änderungen direkt in der Konfigurationsdatei in Ihrem App-Code vornehmen. Dies wird jedoch nicht mit der Einstellungsseite in der Benutzeroberfläche synchronisiert.

