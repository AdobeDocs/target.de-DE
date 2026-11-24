---
keywords: Empfehlungsentwurf; Entwurf erstellen; Entwurf kopieren
description: Erfahren Sie, wie Sie einen [!DNL Target Recommendations] Entwurf mit einem Standarddesign oder durch Erstellen eines benutzerdefinierten Designs erstellen, das am besten zum Layout einer Seite passt.
title: Erstellen eines Designs
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 0f10ee9d-7210-4e02-9342-e4f85cf46e8c
TQID: 'https://experienceleague.adobe.com/GLWcKaQGl6TmL9i7LYUiYepg6SkAjBtL-78-zlaWCTk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: d5030abcda38bbc6d33b88ce3bb5d64f69e4e492
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 11%
---
# Erstellen eines Designs {#create-design}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie in [!DNL Adobe Target Recommendations] Designs erstellen, bearbeiten, kopieren und löschen und Empfehlungen als JSON zurückgeben.

>[!ENDSHADEBOX]

Mit einem Entwurf wird festgelegt, wie Empfehlungen auf einer Seite dargestellt werden. Ein Design kann auf einem Standarddesign basieren oder als benutzerdefiniertes Design erstellt werden. Der Bildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** zeigt sowohl die Standard-Designkarten als auch die im Konto erstellten Designs an.

* Ein Standarddesign kann nicht bearbeitet oder gelöscht werden.
* Ein benutzerdefiniertes Design kann bearbeitet, kopiert oder gelöscht werden.
* Um einen Entwurf auf der Grundlage eines Standardentwurfs zu erstellen, kopieren Sie zunächst den Entwurf und bearbeiten Sie dann die Kopie.

Ein Design kann während des Aktivitätserstellungsprozesses aus dem **[!UICONTROL Visual Experience Composer]** (VEC) oder aus der Design-Bibliothek außerhalb der Aktivitätserstellung erstellt werden. Bei den folgenden Schritten wird davon ausgegangen, dass der Entwurf aus der Bibliothek erstellt wird, die Schritte sind jedoch ähnlich.

## Erstellen eines Designs aus der Bibliothek {#steps}

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]**, um die **[!UICONTROL Designs]**-Bibliothek anzuzeigen.

1. Starten Sie den Entwurf auf eine der folgenden Arten:

   * Um das Design auf einem Standarddesign oder auf einem vorhandenen Design zu basieren, klicken Sie auf das Symbol Mehr Aktionen ( ![Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) für dieses Design und klicken Sie dann auf **[!UICONTROL Kopieren]**. Das **[!UICONTROL Design erstellen]** wird angezeigt. Die bearbeitete Kopie wird zu einem neuen benutzerdefinierten Design.
   * Um einen benutzerdefinierten Entwurf von Grund auf neu zu erstellen, klicken Sie auf **[!UICONTROL Design erstellen]**.

     ![Designs-Bibliothek mit hervorgehobener Schaltfläche „Design erstellen“](../assets/design_1.png)

1. Geben Sie **[!UICONTROL Name]** ein und wählen Sie ein optionales Vorschaubild aus, das auf der Designkarte angezeigt werden soll.

   Wenn ein Standarddesign verwendet wird, wird der Designname gefolgt von „Kopieren“ im Feld **[!UICONTROL Inhaltsname]** angezeigt. Der Name kann bearbeitet werden.

1. (Bedingt) Bearbeiten Sie den Entwurf **[!UICONTROL Code]** nach Bedarf.

   Empfehlungsentwürfe verwenden die Open Source-Entwurfssprache Velocity. Weitere Informationen zu Velocity finden Sie unter [https://velocity.apache.org](https://velocity.apache.org) und [Anpassen eines Designs mithilfe von Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md).

   Der Entwurf kann ein HTML- oder ein Nicht-HTML-Entwurf sein. Standardmäßig sind HTML-Designs mit einem `<div>`-Tag umschlossen, um Klick-Tracking in einer Web-Umgebung zu ermöglichen. Nicht-HTML-Entwürfe eignen sich für Nicht-Webumgebungen, in denen ein Klick-Tracking nicht möglich ist. Schieben Sie den Umschalter **[!UICONTROL HTML Design]** in die Position „off“, um Nicht-HTML-Code zu verwenden.

   >[!NOTE]
   >
   >Die maximale Anzahl von Entitäten, auf die in einem Entwurf verwiesen werden kann, egal ob hartcodiert oder in Schleife, beträgt 99.

1. Klicken Sie **[!UICONTROL Erstellen]**.

1. Klicken Sie auf das Symbol Mehr Aktionen ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallList.svg) ) für das Design, um es zu bearbeiten, zu kopieren oder zu löschen, und klicken Sie dann auf die entsprechende Option: **[!UICONTROL Bearbeiten]**, **[!UICONTROL Kopieren]** oder **[!UICONTROL Löschen]**.

   ![Designs-Bibliothek mit geöffnetem Menü „Mehr Aktionen“ mit den Optionen Bearbeiten, Kopieren und Löschen](../assets/design_2.png)

Designs sind im gesamten Konto verfügbar. Die kontenübergreifende Verwendung muss berücksichtigt werden, bevor ein Design gelöscht wird. Gelöschte Designs können nicht wiederhergestellt werden.

## JSON-Beispiel {#json-example}

Das folgende Beispiel zeigt, wie JSON-Antworten zurückgegeben werden können, wenn eine Aktivität mit dem [formularbasierten Editor“ konfiguriert &#x200B;](/help/main/c-experiences/form-experience-composer.md).

1. Erstellen Sie einen Entwurf aus der **[!UICONTROL Design-]**) oder dem formularbasierten Workflow. Ein Design, das im Workflow **[!UICONTROL Visual Experience Composer]** (VEC) erstellt wird, kann nur ein HTML-Design sein, das zu Klick-Tracking-Zwecken in eine `<div>` eingeschlossen wird.

1. Stellen Sie sicher, dass die Option **[!UICONTROL HTML Design]** deaktiviert ist:

   ![Umschalter für HTML-Design in der Aus-Position](/help/main/c-recommendations/c-design-overview/assets/html_design_toggle.png)

1. Fügen Sie Code wie den folgenden Beispieltext in das Design ein:

   +++ Beispiel-Design-Code, der eine Liste von Entitäts-IDs zurückgibt

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

   +++

1. Richten Sie eine formularbasierte [!DNL Recommendations]-Aktivität ein, die dieses Design verwendet.

   +++ Erfahren Sie, wie Sie eine formularbasierte [!DNL Recommendations] einrichten 

   1. Navigieren Sie zur Seite **[!UICONTROL Aktivitäten]**.
   1. Klicken Sie **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Recommendations]**.
   1. Wählen **[!UICONTROL unter „Experience Composer auswählen]** die Option **[!UICONTROL Formular]** und klicken Sie dann auf **[!UICONTROL Weiter]**.
   1. Geben Sie unter Standort den Text „Sample_Recs_Response“ ein.
   1. Klicken Sie unter **[!UICONTROL Standard-Content]** auf den Pfeil nach unten und dann auf **[!UICONTROL Empfehlung hinzufügen]**.
   1. Wählen Sie einen Seitentyp aus. Das legt fest, welches Bild Sie als nächstes sehen.
   1. Wählen Sie eine Kriterienkarte aus und klicken Sie dann auf **[!UICONTROL Nächste]**.
   1. Wählen Sie das Design aus, das im vorherigen Schritt erstellt wurde, und klicken Sie dann auf **[!UICONTROL Weiter]**.
   1. Schließen Sie den Setup-Vorgang ab.
   1. Klicken Sie auf den Rechtspfeil neben **[!UICONTROL Inaktiv]** und wählen Sie dann **[!UICONTROL Aktivieren]** aus.

   +++

1. Nachdem die Aktivität eingerichtet und aktiviert wurde, kann eine Beispielanfrage eingerichtet werden, um die bereinigte JSON-Antwort zurückzuerhalten.

   Zum Zeitpunkt der Speicherung der Aktivität muss [!DNL Target] ein Modell erstellen, das die ausgewählte Kriterienkonfiguration unterstützt. Je nach einer Reihe von Faktoren kann dieser Vorgang einige Zeit in Anspruch nehmen. Die Ergebnisse werden angezeigt, sobald das Modell erstellt wurde.

   Beispiel:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   wo

   | Parameter | Wert |
   |--- |--- |
   | `[YOUR_CLIENT_CODE]` | Der [!DNL Target] Client-Code (verfügbar unter /help/target/products.html#recsSettings > Recommendations API Token > Client Code). |
   | `[YOUR_MBOX_NAME]` | Der Name, der im Abschnitt „Standorte“ der formularbasierten Recommendations-Aktivität ausgewählt wurde, in diesem Fall Sample_Recs_Response. |
   | `[ENTITY_ID]` | Die `entity.id` eines Elements im Katalog. |
   | `[AT_PROPERTY_TOKEN]` | (Optional) Wird hinzugefügt, wenn eine Eigenschaft (Teil der Enterprise-Berechtigungen) während der Einrichtung der Aktivität ausgewählt wurde. |

Nachdem der Algorithmus ausgeführt wurde und Ergebnisse verfügbar sind, sieht die Antwort ähnlich der folgenden aus:

![JSON-Antwort mit den empfohlenen Elementen](/help/main/c-recommendations/c-design-overview/assets/json_recommendation.png){width="575px"}

## Zusätzliche Tipps zu JSON-Objekten {#json-tips}

Eine einfache kommagetrennte Liste von Elementen kann auch zurückgesendet werden, indem ein Design mit der folgenden Syntax eingerichtet wird:

```
$entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

In der Antwort können auch zusätzliche Informationen gesendet werden. Der folgende Code ist ein komplexeres Beispiel, das viel mehr zurückgibt als die Entitäts-IDs mit ihren zugehörigen Slots (Reihenfolge). Dieses Design-Beispiel gibt auch Aktivitätsdetails, **[!UICONTROL Zielprofil]** Details (falls zutreffend) und andere `entity.attributes` zurück, die mit den zurückgegebenen Elementen verknüpft sind.

+++ Beispiel-Design-Code, der Aktivitäts-, Profil- und Entitätsdetails zurückgibt

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

+++

