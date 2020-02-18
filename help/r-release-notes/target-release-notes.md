---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
title: Versionshinweise zu Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 93ffd24946ad23780b8c141bec79e4492f0e8cda

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert: 18. Februar 2020**

>[!NOTE]
>
>* Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
   >
   >
* Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.
   >
   >
* Ab dem 1. März 2020 deaktiviert Target die Unterstützung für TLS 1.1- und TLS 1.0-Verschlüsselung. Transport Layer Security (TLS) ist das am weitesten verbreitete Sicherheitsprotokoll, das aktuell in Webbrowsern und anderen Anwendungen Verwendung findet, bei denen über ein Netzwerk übertragene Daten geschützt werden müssen. Diese Änderung ist erforderlich, um den allgemein anerkannten Sicherheitsstandard von TLS 1.2 oder höher zu erfüllen. Überprüfen Sie, welche TLS-Version Sie aktuell verwenden. Wenn Ihre Version niedriger als 1.2 ist, implementieren Sie die erforderlichen Änderungen vor dem 1. März 2020, um Target wie erwartet weiter zu verwenden.
   >
   >   
   Detaillierte Informationen zu den möglichen Auswirkungen und den Schritten, die Sie zur Aktualisierung Ihrer Implementierung unternehmen müssen, finden Sie unter Änderungen[der ](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)TLS-Verschlüsselung (Transport Layer Security).


## Target Standard/Premium 20.2.1 (19. Februar 2020)

Diese Version enthält die folgenden Erweiterungen und Fehlerbehebungen:

* Es wurde ein Fehler behoben, der verhinderte, dass Kunden beim Durchführen einer Katalogsuche eine Sammlung auswählen konnten. (TGT-36230)
* Es wurde ein Problem behoben, durch das Kriterien, die über API erstellt wurden, aber nicht von einer in der Target-Benutzeroberfläche erstellten Aktivität referenziert wurden, fälschlicherweise aus der Benutzeroberfläche gelöscht werden konnten. (TGT-35917)
* Implementierung von Sicherheitsverbesserungen in Content Security Policy (CSP). (TGT-36190)
* Es wurde ein Fehler behoben, der dazu führte, dass &quot;NaN%&quot;angezeigt wurde, wenn die prozentuale Attributgewichtung nach links verschoben wurde. (TGT-36211)
* Es wurde ein Problem behoben, das verhinderte, dass Kunden den Algorithmus in einer Aktivität mit automatisierter Personalisierung (AP) von &quot;Random Forest&quot;in &quot;Restabweichung&quot;ändern konnten. (TGT-36321)
* Lokalisierungsprobleme wurden behoben, sodass der Text der Benutzeroberfläche in verschiedenen Sprachen korrekt angezeigt wird.

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
