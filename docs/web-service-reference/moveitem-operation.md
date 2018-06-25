---
title: MoveItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: dcf40fa7-7796-4a5c-bf5b-7a509a18d208
description: MoveItem-Vorgang wird verwendet, um ein oder mehrere Elemente in einen gemeinsamen Zielordner zu verschieben.
ms.openlocfilehash: c5619befb02ec20ef0911992484dcc00cc2c5e92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830492"
---
# <a name="moveitem-operation"></a>MoveItem Operation

**MoveItem** -Vorgang wird verwendet, um ein oder mehrere Elemente in einen gemeinsamen Zielordner zu verschieben. 
  
## <a name="moveitem-request-example"></a>MoveItem-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **MoveItem** veranschaulicht, wie ein Element im Ordner Entwürfe zu verschieben. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ToFolderId>
        <t:DistinguishedFolderId Id="drafts"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AAAtAEF/swbAAA=" ChangeKey="EwAAABYA/s4b"/>
      </ItemIds>
    </MoveItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Das [ToFolderId](tofolderid.md) -Element gibt den Ordner, in dem die Elemente verschoben werden sollen. Beachten Sie, dass alle Elemente in der Auflistung [Artikelnummern ein.](itemids.md) im Zielordner resultiert. Sie müssen separate **MoveItem** platzieren Sie Elemente in unterschiedlichen Zielordner aufrufen. 
  
> [!NOTE]
> Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [MoveItem](moveitem.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [Artikelnummern ein.](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="moveitem-response-example"></a>MoveItem-Antwort-Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **MoveItem** . 
  
Der Elementbezeichner des neuen Elements wird in der Antwortnachricht zurückgegeben. Element-IDs werden nicht auf Öffentliche Ordner **MoveItem** Vorgänge in Antworten für postfachübergreifenden oder Postfach zurückgegeben. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <MoveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:MoveItemResponseMessage>
      </m:ResponseMessages>
    </MoveItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

**MoveItem** -Vorgang wird Erfolg anzuzeigen, wenn die Verschiebung erfolgreich war. 
  
### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [MoveItemResponse](moveitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveItemResponseMessage](moveitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elemente](items.md)
    
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

