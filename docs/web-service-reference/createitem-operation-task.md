---
title: CreateItem-Vorgang (Aufgabe)
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
ms.assetid: 12c5da4d-290c-4a8a-a965-0bf5d55c7978
description: Der CreateItem-Vorgang erstellt Aufgabenelemente im Exchange Speicher.
ms.openlocfilehash: 814a32e82cd5c1c95be252d1b53387741898dd40
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510257"
---
# <a name="createitem-operation-task"></a>CreateItem-Vorgang (Aufgabe)

Der CreateItem-Vorgang erstellt Aufgabenelemente im Exchange Speicher.
  
## <a name="task-createitem-request"></a>CreateItem-Anforderung für Aufgaben

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer CreateItem-Anforderung zeigt, wie ein Aufgabenelement in einem Postfach erstellt wird.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

### <a name="comments"></a>Comments

Anforderungen für wiederkehrende Aufgaben werden geändert, wenn sie von dem Computer empfangen werden, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist. Die folgenden Änderungen treten auf:
  
- Nur das Datum wird für die [StartDate (Recurrence)-Eigenschaft](startdate-recurrence.md) des Serienbereichs der Aufgabe gespeichert. Der Zeitteil ist abgeschnitten. 
    
- Die [StartDate (Recurrence)-Eigenschaft](startdate-recurrence.md) kann je nach Serienmuster angepasst werden. Wenn das Serienmuster beispielsweise als jeden Montag angegeben wird und das StartDate auf den 26. Oktober 2006 festgelegt ist, also einen Donnerstag, wird StartDate an den 30. Oktober 2006 angepasst, also den nächsten Montag. 
    
- Wenn die [StartDate-Eigenschaft](startdate.md) des Vorgangs festgelegt ist, wird sie so aktualisiert, dass sie mit dem [StartDate (Recurrence)](startdate-recurrence.md) des Serienbereichs übereinstimmt. Die [DueDate](duedate.md) -Eigenschaft der Aufgabe wird auch basierend auf dem neuen [StartDate](startdate.md)aktualisiert.
    
- Wenn das [StartDate-Objekt](startdate.md) nicht festgelegt ist, wird nur die [DueDate-Eigenschaft](duedate.md) so aktualisiert, dass sie mit dem [StartDate (Recurrence)](startdate-recurrence.md) des Serienbereichs übereinstimmt. 
    
In der folgenden Tabelle sind die Änderungen aufgeführt, die der Clientzugriffsserver an einer wiederkehrenden Aufgabe vornimmt, die jeden Montag ein Task.Recurrence.Pattern aufweist.
  
**Änderungen an einer Wiederkehrenden Aufgabe**

|**Eigenschaft**|**Originalwert**|**Aktualisierter Wert**|
|:-----|:-----|:-----|
|Task.StartDate  <br/> |1. Januar 2006  <br/> |30. Oktober 2006  <br/> |
|Task.DueDate  <br/> |3. Januar 2006  <br/> |1. November 2006  <br/> |
|Task.Recurrence.Range.StartDate  <br/> |26. Oktober 2006  <br/> |30. Oktober 2006  <br/> |
   
Wenn kein Zielordner angegeben ist, werden standardmäßig Aufgabenelemente im Ordner "Aufgaben" erstellt.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateItem](createitem.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Aufgabe](task.md)
    
- [Betreff](subject.md)
    
- [DueDate](duedate.md)
    
- [Status](status.md)
    
## <a name="successful-task-createitem-response"></a>Erfolgreiche CreateItem-Antwort für Aufgabe

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

Die folgenden Elemente sind in der Antwort enthalten:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Aufgabe](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Siehe auch



[CreateItem-Vorgang](createitem-operation.md)


[Erstellen von Aufgaben](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Aktualisieren von Aufgaben](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Deleting Tasks](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

