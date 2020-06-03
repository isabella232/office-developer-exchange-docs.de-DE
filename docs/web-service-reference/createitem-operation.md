---
title: CreateItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: Der CreateItem-Vorgang erstellt Elemente in der Exchange-Informationsspeicher.
ms.openlocfilehash: f6aaa9ed8e8257f19780492d6137fb015c1b6136
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458866"
---
# <a name="createitem-operation"></a>CreateItem-Vorgang

Der CreateItem-Vorgang erstellt Elemente in der Exchange-Informationsspeicher.
  
## <a name="using-the-createitem-operation"></a>Verwenden des CreateItem-Vorgangs

Sie können den CreateItem-Vorgang verwenden, um Folgendes zu erstellen:
  
- Kalenderelemente
    
- E-Mails
    
- Besprechungsanfragen
    
- Aufgaben
    
- Kontakte
    
Weitere Informationen finden Sie unter [CreateItem-Vorgang (Kalenderelement)](createitem-operation-calendar-item.md), CreateItem-Vorgang [(e-Mail-Nachricht)](createitem-operation-email-message.md), [CreateItem-Vorgang (Besprechungsanfrage)](createitem-operation-meeting-request.md), CreateItem-Vorgang [(Aufgabe)](createitem-operation-task.md)und [CreateItem-Vorgang (Kontakt)](createitem-operation-contact.md).
  
Der CreateItem-Vorgang unterstützt die Verwendung von Response-Objekten. Antwortobjekte unterstützen die Akzeptanz und Ablehnung von Besprechungen und die Handhabung von Abstimmungsschaltflächen, die in einer Standard-e-Mail-Nachricht enthalten sind. In der folgenden Tabelle sind die Response-Objekte aufgeführt, die im CreateItem-Vorgang behandelt werden.
  
|**Response-Objekt**|**Action**|
|:-----|:-----|
|AcceptItem  <br/> |Annehmen einer Besprechungsanfrage.  <br/> |
|CancelCalendarItem  <br/> |Stornieren einer Besprechung. Dies unterscheidet sich vom Löschen aller Teilnehmer, da die Besprechung auch für den Organisator gelöscht wird.  <br/> |
|DeclineItem  <br/> |Ablehnen einer Besprechungsanfrage.  <br/> |
|ForwardItem  <br/> |Senden Sie eine Besprechungsanfrage als Besprechungsanfrage an eine andere Person.  <br/> |
|RemoveItem  <br/> |Entfernen einer abgebrochenen Besprechung aus dem Kalender.  <br/> |
|ReplyAllToItem  <br/> |Senden Sie eine Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage enthält, an alle Teilnehmer der Besprechung.  <br/> |
|ReplyToItem  <br/> |Senden Sie eine Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage enthält, an den Absender der Besprechungsanfrage.  <br/> |
|SendReadReceipt  <br/> |Senden Sie eine Lesebestätigung an den Absender der Besprechungsanfrage.  <br/> |
|TentativelyAcceptItem  <br/> |Akzeptieren Sie eine Besprechungsanfrage mit Vorbehalt.  <br/> |
   
Der CreateItem-Vorgang unterstützt auch zusätzliche Besprechungsobjekte. In der folgenden Tabelle sind zusätzliche Objekte aufgeführt, die vom CreateItem-Vorgang unterstützt werden.
  
|**Besprechungsobjekt**|**Beschreibung**|
|:-----|:-----|
|Besprechungsnachricht  <br/> |Stellt eine Besprechungsnachricht im Exchange-Informationsspeicher dar. Dies ist das Basisobjekt für die anderen Besprechungsobjekte.  <br/> |
|Besprechungsanfrage  <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|Besprechungsantwort  <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|Besprechungs Abbruch  <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateItem-Vorgang (Kalenderelement)](createitem-operation-calendar-item.md)
  
[CreateItem-Vorgang (Kontakt)](createitem-operation-contact.md)
  
[CreateItem-Vorgang (e-Mail-Nachricht)](createitem-operation-email-message.md)
  
[CreateItem-Vorgang (Besprechungsanfrage)](createitem-operation-meeting-request.md)
  
[CreateItem-Vorgang (Aufgabe)](createitem-operation-task.md)
  
 **CreateItemType**

