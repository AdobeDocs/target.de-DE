---
title: Starthandbuch
description: Führen Sie diese Schritte aus, um Ihre Anwendung in Flags zu integrieren, von der Zugriffsanfrage bis zur Erstellung Ihres ersten Feature Flags.
badge: label="Beta" type="Informative"
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
source-git-commit: 339de89fff7bb14eb8146d42482b30c86feeedef
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---

# Starthandbuch {#startup-guide}

Führen Sie diese Schritte aus, um Flags in Ihr Programm zu integrieren.

## Schritt 1: Zugriff anfordern {#step-1-access}

Fordern Sie Zugriff auf die Konsole Flags an und schließen Sie sich Ihrem Team an. Eine [&#x200B; Anleitung finden &#x200B;](../console/request-access.md) unter „Zugriff anfordern“.

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

1. Erstellen Sie in der [&#128279;](https://experience.adobe.com/#/data-collection)-Datenerfassung von eine [Tag-Eigenschaft](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start) falls noch keine vorhanden ist, oder verwenden Sie eine vorhandene Tag-Eigenschaft.
1. Öffnen Sie die Eigenschaft des mobilen Tags oder Web-Tags und navigieren Sie zu [Erweiterungen](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/extensions/overview).
1. Installieren und konfigurieren Sie die Erweiterung **Edge Network**. Installieren Sie dann die **Flags**-Erweiterung.
1. Wählen Sie **Datenstrom** aus (er muss den Customer Journey Analytics-Datensatz enthalten) und konfigurieren Sie die Edge-Domain.
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
