---
keywords: Empfehlungsentwurf; Entwurf erstellen; Entwurf kopieren
description: Erfahren Sie, wie Sie ein [!DNL Target Recommendations] Design mit einem Standardentwurf erstellen oder indem Sie ein benutzerdefiniertes Design erstellen, das am besten zum Layout Ihrer Seite passt.
title: Wie erstelle ich ein Design in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: d33fa5b84ccffc20d8db638aafcc0601c060dbcb
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 20%

---

# Erstellen eines Designs

Mit einem Entwurf wird festgelegt, wie Empfehlungen auf einer Seite dargestellt werden.

Sie können einen [!UICONTROL Recommendations]-Entwurf mit einem Standardentwurf oder durch Erstellen eines benutzerdefinierten Entwurfs erstellen. Auf dem Bildschirm **[!UICONTROL Recommendations > Designs]** werden sowohl die Standardentwurfskarten als auch alle Designs angezeigt, die in Ihrem Konto erstellt wurden.

Beachten Sie beim Arbeiten mit Designs die folgenden Informationen:

* Sie können einen Empfehlungsentwurf mit einem Standardentwurf erstellen oder einen benutzerdefinierten Entwurf erstellen.
* Ein Standardentwurf kann nicht bearbeitet oder gelöscht werden.
* Sie können einen benutzerdefinierten Entwurf bearbeiten, kopieren oder löschen.
* Um einen auf einem Standardentwurf basierenden Entwurf zu erstellen, müssen Sie zunächst den Entwurf kopieren und dann die Kopie bearbeiten.

Diese Abbildung zeigt das standardmäßige 1 x 4-Design:

![1 x 4 Standarddesign](/help/main/c-recommendations/c-design-overview/assets/default-design.png)

Diese Abbildung zeigt ein benutzerdefiniertes Design:

![Benutzerdefinierter Entwurf](/help/main/c-recommendations/c-design-overview/assets/custom-design.png)

Sie können ein Design während des Aktivitätserstellungsprozesses innerhalb des [!UICONTROL Visual Experience Composer] (VEC) oder aus der Design-Bibliothek außerhalb der Aktivitätserstellung erstellen. In den folgenden Abschnitten wird davon ausgegangen, dass Sie Designs aus der Bibliothek erstellen, die Schritte sind jedoch ähnlich.

## Erstellen von Entwürfen

Sie können einen Entwurf basierend auf einem Standardentwurf erstellen oder einen benutzerdefinierten Entwurf erstellen.

### Erstellen eines Designs basierend auf einem Standardentwurf

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** , um die Bibliothek [!UICONTROL Designs] anzuzeigen.


1. Bewegen Sie den Mauszeiger über die Karte für das Design, das Sie erstellen möchten, und klicken Sie dann auf das Symbol **[!UICONTROL Copy]** .

   ![Card_CopyDesign image](/help/main/c-recommendations/c-design-overview/assets/card-copy-design.png)

   Das Dialogfeld [!UICONTROL Create Design] wird angezeigt.

1. Fügen Sie im Bedienfeld **[!UICONTROL Information]** ein **[!UICONTROL Content Name]** und ein optionales Vorschaubild hinzu, das auf der Designkarte angezeigt werden soll.

   Wenn Sie einen Standardentwurf verwenden, werden der Designname und &quot;Kopieren&quot;im Feld **[!UICONTROL Content Name]** angezeigt. Sie können den Namen bearbeiten. Sie können auch ein Bild auswählen, das auf der Designkarte angezeigt werden soll.

1. (Bedingt) Bearbeiten Sie den Entwurf **[!UICONTROL Code]** nach Bedarf.

   Empfehlungsentwürfe verwenden die Open Source-Entwurfssprache Velocity. Informationen zu Velocity finden Sie unter [https://velocity.apache.org](https://velocity.apache.org) und in [Anpassen eines Designs mit Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md).

   Der Entwurf kann ein HTML- oder ein Nicht-HTML-Entwurf sein. Standardmäßig werden HTML-Designs mit einem `<div>` -Tag umschlossen, um Klick-Tracking in einer Webumgebung zu ermöglichen. Nicht-HTML-Designs eignen sich für Nicht-Webumgebungen, in denen Klick-Tracking nicht möglich ist. Schalten Sie den Umschalter [!UICONTROL HTML Design] in die Stellung &quot;Aus&quot;, um Nicht-HTML-Code zu verwenden.

   >[!NOTE]
   >
   >Die maximale Anzahl von Entitäten, die in einem Entwurf referenziert werden können (fest codiert oder in Schleifen), beträgt 99.

1. Klicken Sie auf **[!UICONTROL Save]**.

### Erstellen eines benutzerdefinierten Entwurfs

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** , um die Bibliothek [!UICONTROL Designs] anzuzeigen.

1. Klicken Sie auf **[!UICONTROL Create Design]**.

   Wenn Sie Ihr neues benutzerdefiniertes Design auf einem vorhandenen Entwurf basieren möchten, halten Sie den Mauszeiger über das gewünschte Design und klicken Sie dann auf das Symbol [!UICONTROL Copy] . Anschließend können Sie die Kopie bearbeiten, um ein neues benutzerdefiniertes Design zu erstellen.

1. Fügen Sie einen **[!UICONTROL Content Name]** und ein optionales Vorschaubild hinzu.

1. (Bedingt) Bearbeiten Sie den Entwurf **[!UICONTROL Code]** nach Bedarf.

   Weitere Informationen finden Sie in den Informationen in Schritt 4.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Bearbeiten, Kopieren oder Löschen eines Entwurfs

Beachten Sie, dass Sie einen Standardentwurf nicht bearbeiten oder kopieren können. Sie können nur Standardentwürfe kopieren.

Bewegen Sie den Mauszeiger über das gewünschte Design in der [!UICONTROL Design] -Bibliothek und klicken Sie dann auf das entsprechende Symbol: Bearbeiten, Kopieren oder Löschen.

Sie können einen vorhandenen Entwurf kopieren, um einen Entwurf zu erstellen, den Sie dann ändern können. Auf diese Weise können Sie ein ähnliches Design mit geringerem Aufwand erstellen.

Beachten Sie, dass Designs für das gesamte Konto verfügbar sind. Stellen Sie sicher, dass Sie die kontenübergreifende Verwendung berücksichtigen, bevor Sie einen Entwurf löschen. Gelöschte Designs können nicht wiederhergestellt werden.

## JSON-Beispiel {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

Das folgende Beispiel zeigt, wie JSON-Antworten zurückgegeben werden können, wenn eine Aktivität über den [formularbasierten Editor](/help/main/c-experiences/form-experience-composer.md) konfiguriert wird.

1. Erstellen Sie einen Entwurf innerhalb des [!UICONTROL Design library] oder innerhalb des formularbasierten Workflows. Wenn Sie versuchen, einen Entwurf innerhalb des Arbeitsablaufs für [!UICONTROL Visual Experience Composer] (VEC) zu erstellen, können Sie nichts anderes als einen HTML-Entwurf erstellen, der zu Klick-Tracking-Zwecken in ein `<div>` eingeschlossen ist.

1. Achten Sie darauf, dass die Option „HTML-Design“ ausgeschaltet ist:

   ![html_design_toggle image](assets/html_design_toggle.png)

1. Der folgende Code ist ein Beispiel dafür, was Sie in Ihren Entwurf einfügen können:

   ```javascript
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

1. Richten Sie eine formularbasierte [!DNL Recommendations] -Aktivität ein, die diesen Entwurf verwendet.

   1. Navigieren Sie zur Seite &quot;**[!UICONTROL Activities]**&quot;.
   1. Klicken Sie auf **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.
   1. Wählen Sie unter &quot;**[!UICONTROL Choose Experience Composer]**&quot;**[!UICONTROL Form]** und klicken Sie dann auf &quot;**[!UICONTROL Next]**&quot;.
   1. Geben Sie unter Speicherort den Text „Sample_Recs_Response“ ein.
   1. Klicken Sie unter **[!UICONTROL Default Content]** auf den Abwärtspfeil und dann auf **[!UICONTROL Add Recommendation]**.
   1. Wählen Sie einen Seitentyp aus. Das legt fest, welches Bild Sie als nächstes sehen.
   1. Wählen Sie eine Kriterienkarte aus und klicken Sie dann auf **[!UICONTROL Next]**.
   1. Wählen Sie das Design aus, das Sie im vorherigen Schritt erstellt haben, und klicken Sie dann auf **[!UICONTROL Next]**.
   1. Schließen Sie den Setup-Vorgang ab.
   1. Klicken Sie auf den Pfeil neben **[!UICONTROL Inactive]** und wählen Sie dann **[!UICONTROL Activate]** aus.

1. Nachdem Ihre Aktivität eingerichtet und aktiviert wurde, können Sie eine Musteranforderung einrichten, um die korrekte JSON-Antwort zurückzubekommen.

   Ab dem Zeitpunkt, zu dem Sie Ihre Aktivität speichern, muss [!DNL Target] ein Modell erstellen, das die ausgewählte Kriterienkonfiguration unterstützt. Dieser Prozess kann abhängig von einer Reihe von Faktoren einige Zeit in Anspruch nehmen. Die Ergebnisse werden angezeigt, sobald das Modell aufgebaut wurde.

   Beispiel:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   wo

   | Parameter | Wert |
   |--- |--- |
   | `[YOUR_CLIENT_CODE]` | Target-Client-Code (verfügbar unter /help/target/products.html#recsSettings > Recommendations API Token > Client Code). |
   | `[YOUR_MBOX_NAME]` | Der Name, den Sie im Abschnitt &quot;Speicherorte&quot;des formularbasierten Recommendations ausgewählt haben, in diesem Fall Sample_Recs_Response. |
   | `[ENTITY_ID` | Die `entity.id` eines Artikels in Ihrem Katalog |
   | `[AT_PROPERTY_TOKEN]` | (Optional) Fügen Sie dies hinzu, wenn Sie bei der Einrichtung Ihrer Aktivität eine Eigenschaft (Teil der Unternehmensberechtigungen) ausgewählt haben. |

Nachdem Ihr Algorithmus ausgeführt wurde und Sie Ergebnisse erhalten haben, sollte Ihre Antwort ungefähr so aussehen:

![json_recommendations image](assets/json_recommendation.png){width="575px"}

## Zusätzliche Tipps und Tricks für JSON-Objekte {#section_C305673C68944749969DB239E3221DC2}

Sie können auch eine einfache kommagetrennte Liste von Elementen zurücksenden, indem Sie einen Entwurf mit der folgenden Syntax einrichten:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

Außerdem können Sie mit der Antwort zusätzliche Informationen senden. Die folgende Codedatei ist ein komplexeres Beispiel, das viel mehr zurücksendet als die Entity-IDs mit den zugehörigen Slots (Bestellung). Dieses Designbeispiel gibt auch Aktivitätsdetails, [!UICONTROL Target Profile] Details (falls zutreffend) und andere `entity.attributes` zurück, die mit den zurückgegebenen Elementen verknüpft sind.

```javascript
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

## Schulungsvideo: Erstellen benutzerdefinierter Designs in Recommendations (3:20) ![Badge &quot;Überblick&quot;](/help/main/assets/overview.png)

Dieses Video enthält die folgenden Informationen:

* Erstellen eines benutzerdefinierten Entwurfs
* Verstehen Sie, wie Sie in Ihren Entwürfen auf Anzeigevariablen verweisen.

>[!VIDEO](https://video.tv.adobe.com/v/27687)