---
keywords: recommendations design;create design;copy design
description: Mit einem Entwurf wird festgelegt, wie Empfehlungen auf einer Seite dargestellt werden.
title: Erstellen eines Designs
feature: designs
uuid: 812258e0-8d28-4ef3-b745-45ed694fcabe
translation-type: tm+mt
source-git-commit: 8d0faeb83e7fe854dcf99c89081fb656cf16c4c0
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 95%

---


# ![PREMIUM](/help/assets/premium.png) Erstellen eines Designs{#create-a-design}

Mit einem Entwurf wird festgelegt, wie Empfehlungen auf einer Seite dargestellt werden.

Sie können einen [!UICONTROL Recommendations]-Entwurf erstellen, indem ein Standardentwurf oder ein benutzerdefinierter Entwurf verwendet wird. Im Bildschirm **[!UICONTROL Recommendations > Entwürfe]** werden sowohl Standardentwurfskarten als auch von Ihnen erstellte Entwürfe angezeigt. Die Standardentwürfe können nicht bearbeitet oder gelöscht werden.

1. Bewegen Sie den Mauszeiger auf dem Bildschirm **[!UICONTROL Empfehlungen > Entwürfe]** über die Karte für den Entwurf, den Sie erstellen möchten.

   ![](assets/Card_CopyDesign.png)

1. Um einen vorhandenen Entwurf zu kopieren und zu bearbeiten, klicken Sie auf das Symbol **[!UICONTROL Kopieren]**.

   Oder

   Möchten Sie einen benutzerdefinierten Entwurf erstellen, klicken Sie auf die Option **[!UICONTROL Entwurf erstellen]**, verfügbar im Bildschirm **[!UICONTROL Recommendations > Entwurf.]**

   ![](assets/createDesign.png)

1. Fügen Sie einen **[!UICONTROL Inhaltsnamen]** hinzu.

   Verwenden Sie einen Standardentwurf, lautet dessen Name „Kopie“. Dieser Name erscheint im Feld **[!UICONTROL Inhaltsname]**. Sie können den Namen bearbeiten. 1. (Optional) Wählen Sie per Klick ein Bild aus, das auf der Entwurfskarte angezeigt werden soll.
1. Bearbeiten Sie den Entwurfs-**[!UICONTROL Code]**.

   Empfehlungsentwürfe verwenden die Open Source-Entwurfssprache Velocity. Informationen über Velocity finden Sie unter [](https://velocity.apache.org)https://velocity.apache.org.

   Der Entwurf kann ein HTML- oder ein Nicht-HTML-Entwurf sein. Standardmäßig werden HTML-Entwürfe mit einem <div> Tag umschlossen, um Clicktracking in einer Webumgebung zuzulassen. Nicht-HTML-Entwürfe eignen sich für Nicht-Webumgebungen, in denen ein Klick-Tracking nicht möglich ist.

   >[!NOTE]
   >
   >Die maximale Anzahl von Entitäten, die in einem Entwurf referenziert werden können, egal ob hardcodiert oder in Schleife, beträgt 99.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## JSON-Beispiel {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

Das folgende Beispiel zeigt, wie JSON-Antworten zurückgesendet werden können, wenn eine Aktivität über den formularbasierten Editor konfiguriert wird.

1. Erstellen Sie ein Design aus der Designbibliothek oder aus dem formularbasierten Workflow heraus. Wenn Sie dies innerhalb des Visual Experience Composer (VEC)-Arbeitsablaufs versuchen, können Sie nichts anderes als ein HTML-Design erstellen, das umschlossen ist von einem  `<div>` für das Klick-Tracking.
1. Achten Sie darauf, dass die Option „HTML-Design“ ausgeschaltet ist:

   ![](assets/html_design_toggle.png)

1. Der folgende Code ist ein Beispiel für das, was Sie in Ihr Design einfügen können:

   ```
       #* 
       * "Return a simple list of recommended entity ids"   
       *#
   
       {   
         "notes":{   
         "purpose": "Return a simple list of recommended entity ids",   
         "use-case": "Use this approach if you prefer to do a real-time lookup of entity attribute details (such as inventory, price, rating) from another system (such as a CMS, PIM or ecommerce platform)",   
         "version": "01"   
         },   
         "recommendedItems": {   
           "key": "$key.id",   
           "slot-01": "$entity1.id",   
           "slot-02": "$entity2.id",   
           "slot-03": "$entity3.id",   
           "slot-04": "$entity4.id",   
           "slot-05": "$entity5.id",   
           "slot-06": "$entity6.id",   
           "slot-07": "$entity7.id",   
           "slot-08": "$entity8.id",   
           "slot-09": "$entity9.id",   
           "slot-10": "$entity10.id"   
         }   
       }  
   ```

1. Richten Sie eine formularbasierte Recommendations-Aktivität ein, die dieses Design verwendet.

   1. Gehen Sie zur Seite „Aktivitäten“.
   1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]**.
   1. Wählen Sie **[!UICONTROL Recommendations aus]**.
   1. Wählen Sie unter **[!UICONTROL Experience Composer wählen]** die Option **[!UICONTROL Formular]** aus.

   1. Geben Sie unter Speicherort den Text „Sample_Recs_Response“ ein.
   1. Klicken Sie unter **[!UICONTROL Standard-Content]** auf den Pfeil nach unten und dann auf **[!UICONTROL Empfehlung hinzufügen]**.
   1. Wählen Sie einen Seitentyp aus. Das legt fest, welches Bild Sie als nächstes sehen.
   1. Wählen Sie eine Kriterienkarte aus und klicken Sie dann auf **[!UICONTROL Nächste]**.
   1. Wählen Sie das Design, das Sie im vorherigen Schritt erstellt haben, und klicken Sie dann auf **[!UICONTROL Speichern]**.
   1. Schließen Sie den Setup-Vorgang ab.
   1. Klicken Sie auf den Pfeil neben **[!UICONTROL Inaktiv]** und wählen Sie dann **[!UICONTROL Aktivieren]**.

1. Nachdem Ihre Aktivität eingerichtet und aktiviert wurde, können Sie eine Musteranforderung einrichten, um die korrekte JSON-Antwort zurückzubekommen.

   Ab dem Zeitpunkt, zu dem Sie Ihre Aktivität speichern, muss Target ein Modell aufbauen, das die Konfiguration der ausgewählten Kriterien unterstützt. Abhängig von einer Reihe von Faktoren kann dies einige Zeit in Anspruch nehmen. Die Ergebnisse werden angezeigt, sobald das Modell aufgebaut wurde.

   Beispiel:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   wo

| Parameter | Wert |
|--- |--- |
| `[YOUR_CLIENT_CODE]` | Target-Clientcode (verfügbar unter ../target/products.html#recsSettings > Recommendations API Token > Client Code. |
| `[YOUR_MBOX_NAME]` | Der Name, den Sie im Abschnitt &quot;Speicherorte&quot;des formularbasierten Recommendations ausgewählt haben, in diesem Fall Sample_Recs_Response. |
| `[ENTITY_ID` | Die `entity.id` eines Artikels in Ihrem Katalog |
| `[AT_PROPERTY_TOKEN]` | (Optional) Fügen Sie dies hinzu, wenn Sie bei der Einrichtung Ihrer Aktivität eine Eigenschaft (Teil der Unternehmensberechtigungen) ausgewählt haben. |

Nachdem Ihr Algorithmus ausgeführt wurde und Sie Ergebnisse erhalten haben, sollte Ihre Antwort ungefähr so aussehen:

![](assets/json_recommendation.png){width=&quot;575px&quot;}

## Zusätzliche Tipps und Tricks zu JSON-Objekten {#section_C305673C68944749969DB239E3221DC2}

Sie können auch einfach eine durch Kommas getrennte Liste von Elementen zurücksenden, indem Sie ein Design mit folgender Syntax erstellen:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

Außerdem können Sie mit der Antwort zusätzliche Informationen senden. Die folgende Codedatei ist ein komplexeres Beispiel, das viel mehr zurücksendet als die Entity-IDs mit den zugehörigen Slots (Bestellung). Dieses Designbeispiel sendet auch Aktivitätsdetails, Target-Profildetails (falls vorhanden) und andere `entity.attributes` zurück, die mit den zurückgesendeten Elementen verknüpft sind.

```
    {   
     "adobeRecommendations": {   
      "notes": {   
       "purpose": "Return a list of entity ids with their associated entity.attributes",   
       "use-case": "Use this approach to avoid looking up attribute details after receiving a response from Target",   
       "version": "01"   
      },   
      "recommendedItems": {   
       "slot-01": "$entity1.id",   
       "slot-02": "$entity2.id",   
       "slot-03": "$entity3.id",   
       "slot-04": "$entity4.id",   
       "slot-05": "$entity5.id",   
       "slot-06": "$entity6.id",   
       "slot-07": "$entity7.id",   
       "slot-08": "$entity8.id",   
       "slot-09": "$entity9.id",   
       "slot-10": "$entity10.id"   
      },   
      "activityDetails": {   
       "mbox.name": "email-mbox",   
       "campaign.name": "\${campaign.name}",   
       "campaign.id": "\${campaign.id}",   
       "campaign.recipe.name": "\${campaign.recipe.name}",   
       "campaign.recipe.id": "\${campaign.recipe.id}",   
       "offer.name": "\${offer.name}",   
       "offer.id": "\${offer.id}",   
       "criteria.title": "$criteria.title",   
       "algorithm.name": "$algorithm.name",   
       "algorithm.dayCount": "$algorithm.dayCount"   
      },   
      "visitorProfile": {   
       "profile.favorite-category": "\${profile.favorite-category}",   
       "profile.test": "\${profile.test}",   
       "user.endpoint.lastPurchasedEntity": "\${user.endpoint.lastPurchasedEntity}",   
       "user.endpoint.lastViewedEntity": "\${user.endpoint.lastViewedEntity}",   
       "user.endpoint.mostViewedEntity": "\${user.endpoint.mostViewedEntity}",   
       "user.endpoint.categoryAffinity": "\${user.endpoint.categoryAffinity}",   
       "profile.geolocation.city": "\${profile.geolocation.city}",   
       "profile.geolocation.dma": "\${profile.geolocation.dma}",   
       "profile.geolocation.state": "\${profile.geolocation.state}",   
       "profile.geolocation.country": "\${profile.geolocation.country}",   
       "profile.sessionCount": "\${profile.sessionCount}",   
       "profile.averageDaysBetweenVisits": "\${profile.averageDaysBetweenVisits}",   
       "profile.browserTime": "\${profile.browserTime}",   
       "user.activeActivities": "\${user.activeActivities}",   
       "user.pcId": "\${user.pcId}",   
       "user.isFirstSession": "\${user.isFirstSession}",   
       "user.isNewSession": "\${user.isNewSession}",   
       "user.header": "\${user.header}",   
       "user.parameter": "\${user.parameter}"   
      },   
      "recKey": {   
       "recKeyDetails": {   
        "id": "$key.id",   
        "name": "$key.name",   
        "category": "$key.category",   
        "pageUrl": "$key.pageUrl",   
        "thumbnailUrl": "$key.thumbnailUrl"   
       }   
      },   
      "recDetailedResults": {   
       "recEntity1Details": {   
        "id": "$entity1.id",   
        "name": "$entity1.name",   
        "category": "$entity1.category",   
        "pageUrl": "$entity1.pageUrl",   
        "thumbnailUrl": "$entity1.thumbnailUrl"   
       },   
       "recEntity2Details": {   
        "id": "$entity2.id",   
        "name": "$entity2.name",   
        "category": "$entity2.category",   
        "pageUrl": "$entity2.pageUrl",   
        "thumbnailUrl": "$entity2.thumbnailUrl"   
       },   
       "recEntity3Details": {   
        "id": "$entity3.id",   
        "name": "$entity3.name",   
        "category": "$entity3.category",   
        "pageUrl": "$entity3.pageUrl",   
        "thumbnailUrl": "$entity3.thumbnailUrl"   
       },   
       "recEntity4Details": {   
        "id": "$entity4.id",   
        "name": "$entity4.name",   
        "category": "$entity4.category",   
        "pageUrl": "$entity4.pageUrl",   
        "thumbnailUrl": "$entity4.thumbnailUrl"   
       },   
       "recEntity5Details": {   
        "id": "$entity5.id",   
        "name": "$entity5.name",   
        "category": "$entity5.category",   
        "pageUrl": "$entity5.pageUrl",   
        "thumbnailUrl": "$entity5.thumbnailUrl"   
       },   
       "recEntity6Details": {   
        "id": "$entity6.id",   
        "name": "$entity6.name",   
        "category": "$entity6.category",   
        "pageUrl": "$entity6.pageUrl",   
        "thumbnailUrl": "$entity6.thumbnailUrl"   
       },   
       "recEntity7Details": {   
        "id": "$entity7.id",   
        "name": "$entity7.name",   
        "category": "$entity7.category",   
        "pageUrl": "$entity7.pageUrl",   
        "thumbnailUrl": "$entity7.thumbnailUrl"   
       },   
       "recEntity8Details": {   
        "id": "$entity8.id",   
        "name": "$entity8.name",   
        "category": "$entity8.category",   
        "pageUrl": "$entity8.pageUrl",   
        "thumbnailUrl": "$entity8.thumbnailUrl"   
       },   
       "recEntity9Details": {   
        "id": "$entity9.id",   
        "name": "$entity9.name",   
        "category": "$entity9.category",   
        "pageUrl": "$entity9.pageUrl",   
        "thumbnailUrl": "$entity9.thumbnailUrl"   
       },   
       "recEntity10Details": {   
        "id": "$entity10.id",   
        "name": "$entity10.name",   
        "category": "$entity10.category",   
        "pageUrl": "$entity10.pageUrl",   
        "thumbnailUrl": "$entity10.thumbnailUrl"   
       }   
      }   
     }   
    }  
```

## Training video: Create custom designs in Recommendations (3:20) ![Overview badge](/help/assets/overview.png)

Dieses Video enthält die folgenden Informationen:

* Erstellen eines benutzerdefinierten Entwurfs
* Informationen zur Referenzierung von Anzeigevariablen in Entwürfen

>[!VIDEO](https://video.tv.adobe.com/v/27687)
