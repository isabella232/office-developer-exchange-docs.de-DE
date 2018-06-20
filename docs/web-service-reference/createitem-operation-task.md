---
title: CreateItem-Vorgang (Aufgabe)
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
ms.assetid: 12c5da4d-290c-4a8a-a965-0bf5d55c7978
description: Der Vorgang CreateItem erstellt Aufgabenelementen im Exchange-Speicher.
ms.openlocfilehash: 5a5203202071ae9391faa9348902424317ee96d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757780"
---
# <a name="createitem-operation-task"></a>CreateItem-Vorgang (Aufgabe)

Der Vorgang CreateItem erstellt Aufgabenelementen im Exchange-Speicher.
  
## <a name="task-createitem-request"></a>CreateItem Aufgabenanfrage

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung CreateItem veranschaulicht, wie ein Aufgabenelement in einem Postfach zu erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                MessageDisposition="SaveOnly">
      <Items>
        <t:Task>
          <t:Subject>My task</t:Subject>
          <t:DueDate>2006-10-26T21:32:52</t:DueDate>
          <t:Status>NotStarted</t:Status>
        </t:Task>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Anforderungen für wiederkehrende Aufgaben werden geändert, wenn sie von dem Computer empfangen werden, die Microsoft Exchange Server 2007 ausgeführt wird, dem die Clientzugriffs-Serverrolle installiert ist. Die folgenden Änderungen auftreten:
  
- Für die Eigenschaft ["StartDate" (Wiederholung)](startdate-recurrence.md) von den Serienbereich des Vorgangs wird nur das Datum gespeichert. Die Zeitkomponente werden abgeschnitten. 
    
- [StartDate (Serie)](startdate-recurrence.md) -Eigenschaft kann je nach das Serienmuster angepasst werden. Wenn beispielsweise das Serienmuster wie jeden Montag angegeben ist und das Startdatum auf 26. Oktober 2006 festgelegt ist, ist ein Donnerstag, StartDate angepasst ist und dem 30. Oktober 2006, das den nächsten Montag ist. 
    
- Wenn die [StartDate](startdate.md) -Eigenschaft des Vorgangs festgelegt ist, wird es entsprechend dem [StartDate (Wiederholung)](startdate-recurrence.md) von den Serienbereich aktualisiert. [DueDate](duedate.md) -Eigenschaft des Vorgangs wird ebenfalls aktualisiert basierend auf den neuen [StartDate](startdate.md).
    
- Wenn die [StartDate](startdate.md) nicht festgelegt ist, wird nur die [DueDate](duedate.md) -Eigenschaft aktualisiert, damit die [StartDate (Wiederholung)](startdate-recurrence.md) von den Serienbereich übereinstimmt. 
    
Die folgende Tabelle enthält die Änderungen, die einen sich wiederholenden Vorgang der Clientzugriffsserver gemacht werden, die ein Task.Recurrence.Pattern eines jeden Montag hat.
  
**Änderungen an einer Aufgabenserie**

|**Eigenschaft**|**Originalwert**|**Aktualisierte Wert**|
|:-----|:-----|:-----|
|Task.StartDate  <br/> |1. Januar 2006  <br/> |30 Oktober 2006  <br/> |
|Task.DueDate  <br/> |3. Januar 2006  <br/> |1. November 2006  <br/> |
|Task.Recurrence.Range.StartDate  <br/> |26. Oktober 2006  <br/> |30 Oktober 2006  <br/> |
   
Wenn Sie ein Zielordner nicht angegeben wird, werden Aufgabenelementen standardmäßig im Ordner "Aufgaben" erstellt.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateItem](createitem.md)
    
- [Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Aufgabe](task.md)
    
- [Betreff](subject.md)
    
- [DueDate](duedate.md)
    
- [Status](status.md)
    
## <a name="successful-task-createitem-response"></a>Erfolgreicher CreateItem Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Task>
              <t:ItemId Id="AAAtAE=" ChangeKey="EwAAABYA"/>
            </t:Task>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

Die folgenden Elemente werden in der Antwort enthalten:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Aufgabe](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Siehe auch



[CreateItem Operation](createitem-operation.md)


[Erstellen von Aufgaben](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Aktualisieren der Vorgänge](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Deleting Tasks](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

