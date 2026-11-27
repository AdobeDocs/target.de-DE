---
keywords: Visual Experience Composer;VEC;Karussell
description: Erfahren Sie, wie Sie ein Karussell erstellen, das in Adobe [!DNL Target] Visual Experience Composer (VEC) bearbeitet werden kann.
title: Wie erstelle ich Karussells im Visual Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
TQID: 'https://experienceleague.adobe.com/RN04MJgC49BI2-h2e-i-kgSRTejpLHzKACm-hOv2VCE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%
---
# Erstellen von Karussells, die in [!UICONTROL Visual Experience Composer) ] {#vec-carousels}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie ein Karussell erstellen, das in Visual **[!UICONTROL Composer (VEC) bearbeitet]** kann.

>[!ENDSHADEBOX]

Ein Karussell, das mit der folgenden Struktur erstellt wurde, kann im [!DNL Adobe Target] (**[!UICONTROL Experience Composer]** (VEC) bearbeitet werden. Die Struktur behält den Selektor jeder Folie bei, sodass [!DNL Target] immer die richtige Folie identifiziert, auch wenn sich die angezeigte Folie einige Sekunden nach dem Laden der Seite im VEC ändert.

1. Erstellen Sie die Folien als statische HTML-Platzhalter, wobei eine sichtbare Folie und die anderen Folien nach Klasse ausgeblendet sind.

   ```html
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. Gestalten Sie das Erscheinungsbild nur mit CSS. Verwenden Sie dafür nicht JavaScript.

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Rendern mit JavaScript]** wird derzeit nicht unterstützt, wenn sie zusammen mit benutzerdefiniertem Code im **[!UICONTROL Visual Experience Composer)]** wird.

1. Zeigen Sie die nächste Folie an, indem Sie nur die Klassennamen aktualisieren: Blenden Sie die anderen Folien aus und zeigen Sie die nächste Folie mit einem Timer oder einer Animation an. Aktualisieren Sie die DOM-Struktur niemals mit JavaScript.
