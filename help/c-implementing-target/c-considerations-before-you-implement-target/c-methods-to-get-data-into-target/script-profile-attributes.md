---
keywords: implementieren;Implementierung;Einrichten;Setup;Skript-Profil-Attribute
description: Daten mithilfe von Skript-Profil-Attributen in die Zielgruppe laden
title: Wie erhalte ich Daten mithilfe von Skript-Profil-Attributen in die Zielgruppe?
feature: Implementierung
role: Developer
translation-type: tm+mt
source-git-commit: e8c25685341319fea4381386cad1ce0c5b80face
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 83%

---

# Skript-Profilattribute

Skript-Profil-Attribute sind Name/Wert-Paare, die in der [!DNL Adobe Target]-Lösung definiert werden. Der Wert wird durch die Ausführung eines JavaScript-Snippets auf dem Target-Server über den Server-Aufruf ermittelt.

Benutzer schreiben kleine Code-Snippets, die pro Mbox-Aufruf ausgeführt werden, bevor ein Besucher für eine Zielgruppenmitgliedschaft und -aktivität ausgewertet wird.

## Format

Skript-Profilattribute werden im Abschnitt „Zielgruppen“ von Target erstellt. Jeder Attributname ist gültig und der Wert ist das Ergebnis einer JavaScript-Funktion, die vom Target-Benutzer geschrieben wurde. Den Attributnamen wird in Target automatisch ein „user. “ vorangestellt, um sie von den Profilattributen innerhalb der Seite unterscheiden zu können.

Das Code-Snippet ist in der Sprache Rhino JS geschrieben und kann Token und andere Werte referenzieren.

## Beispielhafte Anwendungsfälle

* **Warenkorbabbruch:** das Profilskript auf 1 setzen, wenn der Besucher den Einkaufswagen erreicht. Wenn der Besucher einen Kauf durchführt, setzen Sie ihn auf 0 zurück. Ist der Wert =1, dann hat der Besucher einen Artikel im Warenkorb.
* **Besuchsanzahl:** bei jedem neuen Besuch die Anzahl um 1 erhöhen, um zu verfolgen, wie oft ein Besucher zur Site zurückkehrt.

## Vorteile der Methode

Keine Seiten-Code-Updates erforderlich.

Wird vor Entscheidungen zu Zielgruppen- und Aktivitätsmitgliedschaften ausgeführt, sodass diese Skript-Profilattribute die Mitgliedschaft bei einem einzelnen Server-Aufruf beeinflussen können.

Kann sehr robust sein. Pro Skript können bis zu 2.000 Befehle ausgeführt werden.

## Einschränkungen

JavaScript-Kenntnisse erforderlich.

Die Ausführungsreihenfolge von Profilskripten kann nicht garantiert werden, sodass sie sich nicht aufeinander verlassen können.

Kann schwierig zu debuggen sein.

## Codebeispiele

Profilskripte sind ziemlich flexibel:

`user.purchase_recency: var dayInMillis = 3600 * 24 * 1000; if (mbox.name == 'orderThankyouPage') {  user.setLocal('lastPurchaseTime', new Date().getTime()); } var lastPurchaseTime = user.getLocal('lastPurchaseTime'); if (lastPurchaseTime) {  return ((new Date()).getTime()-lastPurchaseTime)/dayInMillis; }`

### Links zu relevanten Informationen

[Profilskriptattribute](/help/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)