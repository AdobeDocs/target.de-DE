---
description: Übersichtsinformationen über Designs, die definieren, wie Empfehlungen auf einer Seite angezeigt werden.
keywords: Empfehlungsentwurf; Vorlage; Entwurf erstellen; Lieferung; Ausgabe
seo-description: Übersichtsinformationen über Designs, die definieren, wie Empfehlungen auf einer Seite angezeigt werden.
seo-title: Designübersicht
solution: Target
title: Designübersicht
topic: Premium
uuid: 82cc6a19-bfde-47b3-92b9-b862be70dd87
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Designübersicht{#design-overview}

Übersichtsinformationen über Designs, die definieren, wie Empfehlungen auf einer Seite angezeigt werden.

Target kann, wie in der folgenden Abbildung gezeigt, das komplette Look-and-Feel Ihrer Recommendations darstellen. Das Design kann HTML, JavaScript und CSS enthalten.

![](assets/velocity_example.png)

Target kann Ihre Recommendations auch als JSON-Objekte versenden, die in E-Mail-Nachrichten, IoT-Geräten, Konsolen oder bei Sprachanwendungen (Amazon Alexa oder Google Home) verwendet werden können.

## JSON-Beispiel {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

Das folgende Beispiel zeigt, wie JSON-Antworten zurückgesendet werden können, wenn eine Aktivität über den formularbasierten Editor konfiguriert wird.

1. Erstellen Sie ein Design aus der Designbibliothek oder aus dem formularbasierten Workflow heraus. Wenn Sie dies innerhalb des Visual Experience Composer (VEC)-Arbeitsablaufs versuchen, können Sie nichts anderes als ein HTML-Design erstellen, das umschlossen ist von einem `<div>` für das Klick-Tracking.
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
| `[YOUR_CLIENT_CODE]` | Target-Clientcode (verfügbar unter ../target/products.html#recsSettings &gt; Recommendations API Token &gt; Client Code. |
| `[YOUR_MBOX_NAME]` | Der Name, den Sie im Abschnitt „Speicherorte“ der formularbasierten Recommendations gewählt haben, in diesem Fall YOUR_CLIENT_CODE |
| `[ENTITY_ID`] | Die `entity.id` eines Artikels in Ihrem Katalog |
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

