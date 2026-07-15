---
title: Starthandbuch
description: Führen Sie diese Schritte aus, um Ihre Anwendung in Flags zu integrieren, von der Zugriffsanfrage bis zur Erstellung Ihres ersten Feature Flags.
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
source-git-commit: 35fa45d2a5374dcc47a02bb737f28f24847d7fc6
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 1%

---

# Starthandbuch {#startup-guide}

Führen Sie diese Schritte aus, um Flags in Ihr Programm zu integrieren.

## Schritt 1: Zugriff anfordern {#step-1-access}

Fordern Sie Zugriff auf die Konsole Flags an und schließen Sie sich Ihrem Team an. Eine [ Anleitung finden ](../console/request-access.md) unter „Zugriff anfordern“.

## Schritt 2: Onboarding der Anwendung {#step-2-onboard}

Nachdem Sie Zugriff erhalten haben, melden Sie sich bei der Konsole Flags an und überprüfen Sie, ob Ihre Anwendung unter Ihrem Team aufgeführt ist. Ist dies nicht der Fall, bitten Sie Ihren Team-Administrator, es hinzuzufügen. Siehe [Onboarden des Programms](../applications/onboard-your-application.md).

Bereiten Sie vor dem Onboarding Folgendes vor:

| Anforderung | Details |
|---|---|
| **Anwendungs-ID** | Eine eindeutige Client-Kennung, die beim Aufrufen der Flags-APIs verwendet wird. Verwenden Sie die vorhandene Client-ID Ihrer Anwendung, sofern verfügbar. |
| **Server-seitige Clients** | Bei der Integration mit einer serverseitigen SDK benötigen Sie eine Admin-Client-ID mit entsprechenden Berechtigungen. |
| **Desktop-Clients** | Anstelle einer Client-ID können ein Produkt-Code und eine Produktversion verwendet werden. |

## Schritt 3: Abrufen Ihrer Anmeldedaten {#step-3-credentials}

Die benötigten Anmeldeinformationen hängen von Ihrem Integrationspfad ab:

* **Web und Mobile (tagbasiert):** Verwenden Sie die **Umgebungsdatei-ID** aus Ihrer veröffentlichten Tag-Eigenschaft. Siehe Schritt 4a, wie Sie dies erreichen.
* **Server-seitige SDKs:** Fordern Sie eine **Service-Token-Client-ID** an und lassen Sie sie von Flags-Unterstützung unterstützen, bevor Sie API-Aufrufe über die SDK durchführen können.
* **Desktop:** Ein Produkt-Code und eine Produktversion können anstelle einer Client-ID verwendet werden.

## Schritt 4: Integrieren mit einer SDK {#step-4-integrate}

Befolgen Sie die [Integrationsschritte](integration-steps.md) für Ihren Anwendungstyp. Wählen Sie den Pfad aus, der zu Ihrem Stack passt:

* **Webservices** → Java SDK oder Node.js SDK
* **Web und Mobile Apps** → AEP Mobile SDK — siehe Handbücher zu [Android](../sdk-releases/android/android-extension-integration-guide.md) und [iOS](../sdk-releases/ios/ios-extension-integration-guide.md)
* **Desktop-Programme** → SDK (in Kürze verfügbar)

## Schritt 4a: Einrichten der Datenerfassung und Veröffentlichen der Konfiguration {#step-4a-data-collection}

Wenn Sie die Integration über einen Tag-basierten Ansatz (Web oder Mobile) durchführen, konfigurieren Sie Ihre Tag-Eigenschaft vor der Initialisierung von SDK:

1. Öffnen Sie in der [Adobe Experience Platform](https://experience.adobe.com/#/data-collection)Datenerfassung Ihre Mobile- oder Web-Eigenschaft.
1. Installieren Sie zuerst die Erweiterung {**}Edge Network** und dann die Erweiterung **Experience Rollout“ (in dieser Reihenfolge).**
1. Wählen Sie Ihren **Daten-Stream** (muss den Customer Journey Analytics-Datensatz enthalten) und Ihre Edge-Domain aus.
1. Veröffentlichen Sie die Konfiguration über **Dev → Staging → Produktion**.
1. Kopieren Sie die **Umgebungsdatei-ID** von der Registerkarte **Umgebungen** - Sie verwenden diese zum Initialisieren der SDK.

>[!IMPORTANT]
>
>Stellen Sie in **Staging**-Umgebung der Umgebungsdatei-ID das Präfix `staging/` voran, d. h. verwenden Sie `staging/<environmentId>`. Verwenden **in der** die Umgebungsdatei-ID direkt.

## Schritt 5: Erstellen und Testen des ersten Feature Flag {#step-5-feature-flag}

Erstellen Sie nach Abschluss der Integration Ihr erstes Feature Flag in der Konsole und testen Sie es:

* [Erstellen des ersten Feature Flags](../feature-flags/create-your-first-feature-flag.md)

## Siehe auch {#see-also}

* [Flags in die App integrieren](integrating-in-your-app.md)
* [Integrationsschritte](integration-steps.md)
* [SDKs](sdks.md)

<!-- -->
