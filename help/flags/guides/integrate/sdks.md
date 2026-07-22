---
title: SDKs
description: Erfahren Sie mehr über die SDK-Architektur in Flags und die verfügbaren AEP Web SDK- und AEP Mobile SDK-Erweiterungen.
badge: label="Beta" type="Informative"
hide: true
exl-id: 110a440d-b52a-4e1e-a94f-86f9741a223a
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 2%

---

# SDKs {#sdks}

Flags bietet SDKs zur Integration von Feature Flags in Ihre Programme. Flags werden über die AEP Web SDK und AEP Mobile SDK bereitgestellt.

## SDK-Architektur {#architecture}

Alle Flags-SDKs verwenden dieselbe Kernarchitektur:

* **Initialisierung** - Die SDK wird beim Start konfiguriert und beim Flags-Service registriert.
* **Funktionsabruf** - Die SDK ruft Feature Flag-Daten ab und wertet Flags lokal aus.
* **Caching** - Die SDK speichert Feature Flag-Daten zwischen und aktualisiert sie in einem konfigurierbaren Abrufintervall.
* **Fehlerbehandlung** - Wenn der Dienst nicht verfügbar ist, stellt SDK weiterhin Feature Flag-Auswertungen aus dem lokalen Cache bereit.

## Verfügbare SDKs {#available-sdks}

### AEP Web SDK {#web-sdk}

Die Flags-Erweiterung für Web lässt sich mit Adobe Experience Platform Web SDK integrieren.

>[!NOTE]
>
>Web SDK-Support wird in Kürze verfügbar sein. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um frühzeitig Zugang zu erhalten.

### Android-Erweiterung {#android-extension}

Die Flags-Erweiterung für Android lässt sich mit Adobe Experience Platform Mobile SDK integrieren.

Einrichtungsanweisungen finden Sie im Handbuch zur Integration [&#128279;](../sdk-releases/android/android-extension-integration-guide.md) Android-Erweiterungen .

### iOS-Erweiterung {#ios-extension}

Die Flags-Erweiterung für iOS lässt sich mit Adobe Experience Platform Mobile SDK integrieren.

Einrichtungsanweisungen finden Sie im Handbuch zur Integration [&#128279;](../sdk-releases/ios/ios-extension-integration-guide.md) iOS-Erweiterungen .

## Siehe auch {#see-also}

* [Handbuch zur Integration von Android-Erweiterungen](../sdk-releases/android/android-extension-integration-guide.md)
* [Handbuch zur Integration von iOS-Erweiterungen](../sdk-releases/ios/ios-extension-integration-guide.md)
* [Handbuch zur Integration von Web-Erweiterungen](../sdk-releases/web/web-extension-integration-guide.md)

<!-- -->
