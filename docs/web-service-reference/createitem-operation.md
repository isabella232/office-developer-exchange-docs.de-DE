---
title: CreateItem Operation
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
description: Der Vorgang CreateItem erstellt Elemente im Exchange-Speicher.
ms.openlocfilehash: 7e1808c685cdbaa1e8867aa7425b2cc52218d001
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757781"
---
# <a name="createitem-operation"></a>CreateItem Operation

Der Vorgang CreateItem erstellt Elemente im Exchange-Speicher.
  
## <a name="using-the-createitem-operation"></a>Verwenden den CreateItem-Vorgang

Den CreateItem-Vorgang können Sie Folgendes erstellen:
  
- Kalenderelementen (engl.)
    
- E-Mails
    
- Besprechungsanfragen
    
- Aufgaben
    
- Kontakte
    
Weitere Informationen finden Sie unter [CreateItem Operation (Kalenderelement)](createitem-operation-calendar-item.md), [CreateItem-Vorgang (e-Mail-Nachricht)](createitem-operation-email-message.md), [CreateItem-Vorgang (Besprechungsanfrage)](createitem-operation-meeting-request.md), [CreateItem-Vorgang (Aufgabe)](createitem-operation-task.md)und [CreateItem-Vorgang (Kontakt) ](createitem-operation-contact.md).
  
Die CreateItem Operation unterstützt die Verwendung von Antwort-Objekten. Antwortobjekte unterstützen die Annahme und Ablehnung von Besprechungen und die Behandlung von Abstimmungsoptionen Schaltflächen, die in einer standard-e-Mail-Nachricht enthalten sind. Die folgende Tabelle enthält die Antwortobjekte, die in der CreateItem Operation behandelt werden.
  
|**Response-Objekt**|**Aktion**|
|:-----|:-----|
|AcceptItem  <br/> |Annehmen von Besprechungsanfragen.  <br/> |
|CancelCalendarItem  <br/> |Stornieren einer Besprechung. Dies unterscheidet sich von löschen alle Teilnehmer, da es für den Organisator die Besprechung auch gelöscht.  <br/> |
|DeclineItem  <br/> |Ablehnen einer Besprechungsanfrage.  <br/> |
|ForwardItem  <br/> |Senden Sie eine Besprechungsanfrage an eine andere Person als eine Besprechungsanfrage.  <br/> |
|RemoveItem  <br/> |Entfernen einer abgebrochenen Besprechung aus dem Kalender.  <br/> |
|ReplyAllToItem  <br/> |Senden einer Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage an alle Teilnehmer der Besprechung enthält.  <br/> |
|ReplyToItem  <br/> |Senden einer Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage an den Absender der Besprechungsanfrage enthält.  <br/> |
|SendReadReceipt  <br/> |Senden Sie eine lesebestätigung an den Absender der Besprechungsanfrage.  <br/> |
|TentativelyAcceptItem  <br/> |Mit Vorbehalt annehmen einer Besprechungsanfrage.  <br/> |
   
Die CreateItem Operation unterstützt auch zusätzliche Besprechung-Objekte. Die folgende Tabelle enthält zusätzliche-Objekten, die CreateItem Operation unterstützt.
  
|**Meeting-Objekt**|**Beschreibung**|
|:-----|:-----|
|Meeting-Nachricht  <br/> |Stellt eine Besprechungsnachricht im Exchange-Speicher. Dies ist das Basisobjekt für die Besprechung Objekte.  <br/> |
|Besprechungsanfrage  <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|Antwort auf Besprechungsanfrage  <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|Besprechungsabsagen  <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateItem-Vorgang (Kalenderelement)](createitem-operation-calendar-item.md)
  
[CreateItem-Vorgang (Kontakt)](createitem-operation-contact.md)
  
[CreateItem-Vorgang (e-Mail-Nachricht)](createitem-operation-email-message.md)
  
[CreateItem-Vorgang (Besprechungsanfrage)](createitem-operation-meeting-request.md)
  
[CreateItem-Vorgang (Aufgabe)](createitem-operation-task.md)
  
 **CreateItemType**

