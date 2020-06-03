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
description: Der CreateItem-Vorgang erstellt Aufgabenelemente in der Exchange-Informationsspeicher.
ms.openlocfilehash: 502108843193e7ed8377b0fade9e106ef3d1976c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457102"
---
# <a name="createitem-operation-task"></a>CreateItem-Vorgang (Aufgabe)

Der CreateItem-Vorgang erstellt Aufgabenelemente in der Exchange-Informationsspeicher.
  
## <a name="task-createitem-request"></a>Aufgaben-CreateItem-Anforderung

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer CreateItem-Anforderung wird gezeigt, wie ein Aufgabenelement in einem Postfach erstellt wird.
  
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

Anforderungen für wiederkehrende Aufgaben werden geändert, wenn Sie von dem Computer empfangen werden, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist. Die folgenden Änderungen treten auf:
  
- Nur das Datum wird für die StartDate-Eigenschaft [(Serie)](startdate-recurrence.md) des Serien Bereichs des Vorgangs gespeichert. Der Zeitbereich wird abgeschnitten. 
    
- Die [StartDate-Eigenschaft (Serie)](startdate-recurrence.md) kann abhängig vom Serienmuster angepasst werden. Wenn beispielsweise das Serienmuster jeden Montag angegeben wird und das Startwert auf den 26. Oktober 2006 festgelegt ist, was ein Donnerstag ist, wird StartDate auf den 30. Oktober 2006 eingestellt, was der nächste Montag ist. 
    
- Wenn die [StartDate](startdate.md) -Eigenschaft des Vorgangs festgelegt ist, wird Sie entsprechend der [StartDate (Serie)](startdate-recurrence.md) des Serien Bereichs aktualisiert. Die [DueDate](duedate.md) -Eigenschaft des Tasks wird auch basierend auf dem neuen [StartDate](startdate.md)aktualisiert.
    
- Wenn das [Startwert nicht](startdate.md) festgelegt ist, wird nur die [DueDate](duedate.md) -Eigenschaft so aktualisiert, dass Sie der [StartDate (Serie)](startdate-recurrence.md) des Serien Bereichs entspricht. 
    
In der folgenden Tabelle sind die Änderungen aufgeführt, die der Client Zugriffsserver für eine wiederkehrende Aufgabe vornimmt, die ein Task. Serie. Pattern jedes montags aufweist.
  
**Änderungen an einer wiederkehrenden Aufgabe**

|**Eigenschaft**|**Ursprünglicher Wert**|**Aktualisierter Wert**|
|:-----|:-----|:-----|
|Task. StartDate  <br/> |1. Januar 2006  <br/> |30. Oktober 2006  <br/> |
|Task. DueDate  <br/> |3. Januar 2006  <br/> |1. November 2006  <br/> |
|Task. Serie. Range. StartDate  <br/> |26. Oktober 2006  <br/> |30. Oktober 2006  <br/> |
   
Wenn ein Zielordner nicht angegeben ist, werden die Aufgabenelemente standardmäßig im Ordner Aufgaben erstellt.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateItem](createitem.md)
    
- [Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Task](task.md)
    
- [Betreff](subject.md)
    
- [DueDate](duedate.md)
    
- [Status](status.md)
    
## <a name="successful-task-createitem-response"></a>Erfolgreiche Aufgabe CreateItem-Antwort

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

Die Antwort enthält die folgenden Elemente:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [Task](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>Siehe auch



[CreateItem-Vorgang](createitem-operation.md)


[Erstellen von Aufgaben](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Aktualisieren von Aufgaben](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[Deleting Tasks](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

