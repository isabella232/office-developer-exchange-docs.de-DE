---
title: CreateItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: Der CreateItem-Vorgang erstellt Elemente im Exchange Speicher.
ms.openlocfilehash: 2aee80d883aa623b8074ecc523d1a45fa71962da
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538401"
---
# <a name="createitem-operation"></a>CreateItem-Vorgang

Der CreateItem-Vorgang erstellt Elemente im Exchange Speicher.
  
## <a name="using-the-createitem-operation"></a>Verwenden des CreateItem-Vorgangs

Mit dem CreateItem-Vorgang können Sie Folgendes erstellen:
  
- Kalenderelemente
    
- E-Mails
    
- Besprechungsanfragen
    
- Aufgaben
    
- Kontakte
    
Weitere Informationen finden Sie unter [CreateItem-Vorgang (Kalenderelement),](createitem-operation-calendar-item.md) [CreateItem-Vorgang (E-Mail-Nachricht),](createitem-operation-email-message.md) [CreateItem-Vorgang (Besprechungsanfrage),](createitem-operation-meeting-request.md) [CreateItem-Vorgang (Aufgabe)](createitem-operation-task.md)und [CreateItem-Vorgang (Kontakt)](createitem-operation-contact.md).
  
Der CreateItem-Vorgang unterstützt die Verwendung von Antwortobjekten. Antwortobjekte unterstützen die Annahme und Ablehnung von Besprechungen und die Behandlung von Abstimmungsschaltflächen, die in einer standardmäßigen E-Mail-Nachricht enthalten sind. In der folgenden Tabelle sind die Antwortobjekte aufgeführt, die im CreateItem-Vorgang behandelt werden.
  
|**Response-Objekt**|**Aktion**|
|:-----|:-----|
|AcceptItem  <br/> |Akzeptieren Sie eine Besprechungsanfrage.  <br/> |
|CancelCalendarItem  <br/> |Abbrechen einer Besprechung. Dies unterscheidet sich vom Löschen aller Teilnehmer, da auch die Besprechung für den Organisator gelöscht wird.  <br/> |
|DeclineItem  <br/> |Ablehnen einer Besprechungsanfrage.  <br/> |
|ForwardItem  <br/> |Senden Sie eine Besprechungsanfrage als Besprechungsanfrage an eine andere Person.  <br/> |
|RemoveItem  <br/> |Entfernen sie eine abgebrochene Besprechung aus dem Kalender.  <br/> |
|ReplyAllToItem  <br/> |Senden Sie eine Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage enthält, an alle Teilnehmer der Besprechung.  <br/> |
|ReplyToItem  <br/> |Senden Sie eine Nachricht, die den Text der ursprünglichen Besprechungsanfrage enthält, an den Absender der Besprechungsanfrage.  <br/> |
|SendReadReceipt  <br/> |Senden Sie eine Lesebestätigung an den Absender der Besprechungsanfrage.  <br/> |
|TentativelyAcceptItem  <br/> |Nehmen Sie mit Vorbehalt eine Besprechungsanfrage an.  <br/> |
   
Der CreateItem-Vorgang unterstützt auch zusätzliche Besprechungsobjekte. In der folgenden Tabelle sind weitere Objekte aufgeführt, die vom CreateItem-Vorgang unterstützt werden.
  
|**Meeting-Objekt**|**Beschreibung**|
|:-----|:-----|
|Besprechungsnachricht  <br/> |Stellt eine Besprechungsnachricht im Exchange Store dar. Dies ist das Basisobjekt für die anderen Besprechungsobjekte.  <br/> |
|Besprechungsanfrage  <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|Besprechungsantwort  <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|Besprechungsabsage  <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateItem-Vorgang (Kalenderelement)](createitem-operation-calendar-item.md)
  
[CreateItem-Vorgang (Kontakt)](createitem-operation-contact.md)
  
[CreateItem-Vorgang (E-Mail-Nachricht)](createitem-operation-email-message.md)
  
[CreateItem-Vorgang (Besprechungsanforderung)](createitem-operation-meeting-request.md)
  
[CreateItem-Vorgang (Aufgabe)](createitem-operation-task.md)
  
 **CreateItemType**

