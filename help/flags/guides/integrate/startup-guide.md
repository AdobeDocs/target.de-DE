---
title: Starthandbuch
description: Führen Sie diese Schritte aus, um Ihre Anwendung in Flags zu integrieren, von der Zugriffsanfrage bis zur Erstellung Ihres ersten Feature Flags.
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
source-git-commit: 9a4e16418c93fa163d821409a0eecb251f2a9929
workflow-type: tm+mt
source-wordcount: '352'
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

## Schritt 3: Umgebungsdatei-ID abrufen {#step-3-credentials}

Die benötigte Umgebungsdatei-ID hängt von Ihrem Integrationspfad ab:

* **Web und Mobile (tagbasiert):** Verwenden Sie die **Umgebungsdatei-ID** aus Ihrer veröffentlichten Tag-Eigenschaft. Siehe Schritt 4a, wie Sie dies erreichen.

## Schritt 4: Integrieren mit einer SDK {#step-4-integrate}

Befolgen Sie die Anleitung zur Integration für Ihren Anwendungstyp. Wählen Sie den Pfad aus, der zu Ihrem Stack passt:

* **Web und Mobile Apps** - Siehe [Handbücher zu Android](../sdk-releases/android/android-extension-integration-guide.md), [iOS](../sdk-releases/ios/ios-extension-integration-guide.md) und [Web](../sdk-releases/web/web-extension-integration-guide.md) im Abschnitt Integrationshandbuch

## Schritt 4a: Einrichten der Datenerfassung und Veröffentlichen der Konfiguration {#step-4a-data-collection}

Wenn Sie die Integration über einen Tag-basierten Ansatz (Web oder Mobile) durchführen, konfigurieren Sie Ihre Tag-Eigenschaft vor der Initialisierung von SDK:

1. Öffnen Sie in der [Adobe Experience Platform](https://experience.adobe.com/#/data-collection)Datenerfassung Ihre Mobile- oder Web-Eigenschaft.
1. Installieren Sie zuerst die Erweiterung {0 **Edge Network** und dann die Erweiterung Flags **(in dieser Reihenfolge).**
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
* [SDKs](sdks.md)

<!-- -->
