---
keywords: Visual Experience Composer;VEC;Karussell
description: Dieses Thema zeigt, wie Sie ein Karussell erstellen, das im Adobe Target Visual Experience Composer (VEC) bearbeitet werden kann.
title: Erstellen von Karussells, die im Visual Experience Composer funktionieren
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 69%

---


# Erstellen von Karussells, die in Visual Experience Composer funktionieren

Dieses Thema zeigt, wie Sie ein Karussell erstellen, das im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) bearbeitet werden kann.

Sollten Sie mit den Anweisungen unten arbeiten, weiß [!DNL Target] stets, dass die ausgewählte Folie die Auswahl für die richtige Folie beinhaltet, selbst wenn sie nach einigen Sekunden im Visual Experience Composer ausgewechselt wird.

1. Erstellen Sie statische HTML-Platzhalter.

   ```html
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