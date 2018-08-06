---
title: DeleteItem-Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 3e26c416-fa12-476e-bfd2-5c1f4bb7b348
description: Über den DeleteItem-Vorgang können Elemente im Exchange-Speicher gelöscht werden.
ms.openlocfilehash: 87d7853daa5db0cd87b3f6469c228a584b4d9caf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757927"
---
# <a name="deleteitem-operation"></a>DeleteItem-Operation

Über den **DeleteItem**-Vorgang können Elemente im Exchange-Speicher gelöscht werden. 
  
> [!NOTE]
> Für einen **DeleteItem**-Vorgang wird eine Fehlerantwort inklusive des ErrorCannotDeleteObject-Fehlercodes zurückgegeben, wenn ein Stellvertreter versucht, ein Element im Postfach eines Prinzipals zu löschen, indem er für DisposalType MoveToDeletedItems festlegt. Zum Löschen eines Elements durch Verschieben in den Ordner „Gelöschte Elemente" muss ein Stellvertreter die [MoveItem Operation](moveitem-operation.md) verwenden. 
  
## <a name="deleteitem-request-example"></a>DeleteItem-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **DeleteItem**-Anforderung wird veranschaulicht, wie ein Element endgültig aus einem Postfach gelöscht werden kann. 
  
> [!NOTE]
> Die Element-ID wurde zur besseren Lesbarkeit gekürzt. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [DeleteItem](deleteitem.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
Um weitere Optionen für die Anforderungsnachricht des **DeleteItem**-Vorgangs zu finden, sehen Sie sich die Schemahierarchie an. Beginnen Sie beim [DeleteItem](deleteitem.md)-Element. 
  
## <a name="successful-deleteitem-response"></a>Erfolgreiche DeleteItem-Antwort

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine erfolgreiche Antwort auf eine **DeleteItem**-Anforderung veranschaulicht. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteItemResponse](deleteitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
Um weitere Optionen für die Antwortnachricht des **DeleteItem**-Vorgangs zu finden, sehen Sie sich die Schemahierarchie an. Beginnen Sie beim [DeleteItemResponse](deleteitemresponse.md)-Element. 
  
## <a name="deleteitem-error-response"></a>DeleteItem-Fehlerantwort

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Fehlerantwort auf eine **DeleteItem**-Anforderung veranschaulicht. Der Fehler wurde ausgegeben, da der Vorgang versucht hat, ein Element zu löschen, das im Exchange-Speicher nicht gefunden werden konnte. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteItemResponse](deleteitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Andere Optionen für die Fehlerantwortnachricht des **DeleteItem**-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie beim [DeleteItemResponse](deleteitemresponse.md)-Element. 
  
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Löschen von Kontakten](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [Deleting E-mail Messages](http://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [Deleting Tasks](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

