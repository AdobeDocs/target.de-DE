---
keywords: Visual Experience Composer;VEC;Karussell
description: Erfahren Sie, wie Sie ein Karussell erstellen, das in der Adobe bearbeitet werden kann. [!DNL Target] Visual Experience Composer (VEC).
title: Wie erstelle ich Karussells im Visual Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 70%

---

# Erstellen von Karussells, die in Visual Experience Composer funktionieren

In diesem Thema wird gezeigt, wie ein Karussell erstellt wird, das im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).

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
