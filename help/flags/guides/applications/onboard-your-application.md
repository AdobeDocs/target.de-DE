---
title: Onboarding Ihres Programms
description: Erfahren Sie, wie Sie eine neue Anwendung in Flags integrieren, damit Sie Feature Flags erstellen und verwalten können.
badge: label="Beta" type="Informative"
hide: true
exl-id: d88c27a5-f490-4504-9764-5e4ce98fdf20
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# Onboarding Ihres Programms {#onboard-your-application}

Sie müssen über die Rolle **Admin** verfügen, um eine neue Anwendung hinzuzufügen. Wenden Sie sich an Ihren Administrator, wenn Sie Ihre Rolle überprüfen oder aktualisieren müssen.

## Neue Anwendung hinzufügen {#add-application}

1. Melden Sie sich bei der Flags -Konsole an und navigieren Sie zu **Flags > Anwendungen**.

   >[!NOTE]
   >
   >Wenn die Schaltfläche **Neue Anwendung** nicht sichtbar ist, stellen Sie sicher, dass Sie über die Rolle **Admin** verfügen.

2. Wählen Sie **Neue Anwendung** aus.

3. Wählen Sie die **Plattform**, die Ihrem Anwendungstyp (Web oder Mobile) entspricht.

4. Geben Sie die folgenden Informationen an:

   Mit * markierte Felder sind Pflichtfelder.

   | Feld | Beschreibung |
   | --- | --- |
   | **Anwendungsname** * | Ein Anzeigename für die Anwendung. |
   | **Anwendungs-ID** * | Eine eindeutige Kennung, die beim Aufrufen von Flags aus Ihrem Code verwendet wird. Verwenden Sie die Client-ID Ihrer Anwendung. |
   | **Abrufintervall** | Das Abrufintervall (in Sekunden) für die Aktualisierung des Anwendungscache. Gilt nur für Server-seitige SDKs. |

5. Wählen Sie **Hinzufügen** aus. Ihre Anwendung ist jetzt registriert und bereit für die Konfiguration des Feature Flags.

## Wie geht es weiter? {#next-steps}

Sobald sich Ihre Anwendung in der Einarbeitungsphase befindet, können Sie mit der Erstellung von Feature Flags beginnen:

* [Erstellen des ersten Feature Flags](../feature-flags/create-your-first-feature-flag.md)
* [Flags in die App integrieren](../integrate/integrating-in-your-app.md)

## Siehe auch {#see-also}

* [Anwendungen verwalten](manage-applications.md)
* [Melden Sie sich bei der Konsole an](../console/log-in-to-the-console.md)

<!-- -->
