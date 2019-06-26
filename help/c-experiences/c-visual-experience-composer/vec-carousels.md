---
description: In diesem Thema wird erläutert, wie ein Karussell erstellt wird, das im Visual Experience Composer (VEC) bearbeitet werden kann.
keywords: Visual Experience Composer;VEC;Karussell
seo-description: In diesem Thema wird erläutert, wie ein Karussell erstellt wird, das im Visual Experience Composer (VEC) bearbeitet werden kann.
seo-title: Erstellen von Karussells, die in Visual Experience Composer funktionieren
solution: Target
subtopic: Multivarianz-Test
title: Erstellen von Karussells, die in Visual Experience Composer funktionieren
topic: Standard
uuid: 19538f6e-445c-49ca-9f0d-b49fc330b721
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Erstellen von Karussells, die in Visual Experience Composer funktionieren{#creating-carousels-that-work-in-the-visual-experience-composer}

In diesem Thema wird erläutert, wie ein Karussell erstellt wird, das im Visual Experience Composer (VEC) bearbeitet werden kann.

Sollten Sie mit den Anweisungen unten arbeiten, weiß [!DNL Target] stets, dass die ausgewählte Folie die Auswahl für die richtige Folie beinhaltet, selbst wenn sie nach einigen Sekunden im Visual Experience Composer ausgewechselt wird.

1. Erstellen Sie statische HTML-Platzhalter.

   ```
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. Fügen Sie CSS hinzu, um Aussehen und Feeling des Erlebnisses anzupassen.

   Verwenden Sie hierzu keinesfalls JavaScript.

   >[!NOTE]
   >
   >Die Option [!UICONTROL Mit JavaScript rendern] wird derzeit nicht unterstützt, wenn sie im Visual Experience Composer gemeinsam mit benutzerdefiniertem Code verwendet wird.

1. Aktualisieren Sie classNames nur, um andere auszublenden und den Text mit Timer/Animation anzuzeigen.

   Aktualisieren Sie die DOM-Struktur niemals mithilfe von JavaScript.