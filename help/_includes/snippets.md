---
source-git-commit: 8c6f23b495228ab930e6649aa2f9e6dae506cae2
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 6%
---
# Snippets

## Target Premium-Funktionen {#premium-note}

>[!NOTE]
>
>Diese Funktion ist als Teil der [Target Premium](/help/main/c-intro/intro.md#premium)-Lizenz verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht verfügbar.

## Aktualisierung der Zielberechtigungen {#permissions-update}

>[!IMPORTANT]
>
>[!DNL Target] Benutzer mit Berechtigungen [!UICONTROL Produktadministrator] und [!UICONTROL Systemadministrator] können alle Einstellungen auf den Seiten [!UICONTROL Administration] bearbeiten, unabhängig von ihrer Rolle in [!DNL Target]. Benutzende ohne diese Berechtigungen haben schreibgeschützten Zugriff auf diese Einstellungen.

## Aktualisierte Target-Benutzeroberfläche {#updated-ui}

>[!NOTE]
>
>Neu im Jahr 2025 [!DNL Target] eine aktualisierte Benutzeroberfläche und [!UICONTROL Visual Experience Composer] (VEC) eingeführt. Klicken Sie auf die folgenden Links, um mehr zu erfahren:
>
>* [[!DNL Target Standard/Premium] 25.2.1 (17. Februar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für , [!UICONTROL Recommendations] und [!UICONTROL Visual Experience Composer] (VEC).
>
>* [[!DNL Target Standard/Premium] 25.1.1 (9. Januar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für die [!UICONTROL Angebotsbibliothek].
>
>* [Grundlegendes zur  [!DNL Target] -Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md): Bietet einen kurzen Überblick, der Ihnen hilft, sich mit [!DNL Target] vertraut zu machen, und enthält Links für detailliertere Informationen und schrittweise Anweisungen.
>
>* [[!UICONTROL Änderungen &#x200B;] Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird ein aktualisierter [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die Unterschiede zwischen der alten und der aktualisierten Version des VEC erläutert.
>
>* [[!UICONTROL Visual Experience Composer] Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): In diesem Artikel werden die aktualisierte VEC-Benutzeroberfläche und ihre Optionen erläutert.
>
>* [[!DNL Target] Häufig gestellte Fragen zur Aktualisierung der Benutzeroberfläche](/help/main/c-intro/updated-ui-faq.md): In dieser häufig gestellten Frage werden häufige Fragen zur neuen [!DNL Target]-Benutzeroberfläche und zu [!UICONTROL Visual Experience Composer] (VEC) behandelt, einschließlich Navigationsänderungen, Funktionsspeicherorte und der Einstellung des Umschalters für die temporäre Benutzeroberfläche. Unabhängig davon, ob Sie Marketing-Experte, Entwickler oder Administrator sind, hilft Ihnen diese häufig gestellte Frage dabei, den Übergang reibungslos zu gestalten und die aktualisierte Benutzeroberfläche optimal zu nutzen.

## Regeln für Aktivitätsnamen {#activity-name-rules}

Der Aktivitätsname darf nicht mit `=`, `+`, `-` oder `@` beginnen. Der Aktivitätsname darf auch keine der folgenden Zeichenfolgen enthalten: `;=`, `;+`, `;-`, `;@`, `,=`, `,+`, `,-`, `,@`, `["` oder `"]`.

## Zuordnung von Besuchern zu Aktivitäten {#visitor-matching}

Eine Besucherin oder ein Besucher, die bzw. der sich bereits in einer **[!UICONTROL A/B]** Test- oder **[!UICONTROL Multivarianz-Test]**-Aktivität befindet, stimmt mit dieser Aktivität überein, bis diese konvertiert wird. Ein Besucher, der sich zuvor in einer **[!UICONTROL Erlebnis-Targeting]**-Aktivität befand, muss erneut mit ihr übereinstimmen. Wenn der Besucher die Zielgruppenregeln erfüllt, fallen er in diese Aktivitäten und in bestimmte Erlebnisse.
