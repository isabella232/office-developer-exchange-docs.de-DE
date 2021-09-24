---
title: ArchiveItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1af216b3-13ea-498e-b4fc-23513755d731
description: Hier finden Sie Informationen zum EWS-Vorgang "ArchiveItem".
ms.openlocfilehash: 9dd753f92a6e6d37a5cf990118d63878508aee5a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525288"
---
# <a name="archiveitem-operation"></a>ArchiveItem-Vorgang

Hier finden Sie Informationen zum **EWS-Vorgang "ArchiveItem".** 
  
Der **ArchiveItem-Vorgang** verschiebt ein Element in das Archivpostfach des Postfachbenutzers. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-archiveitem-operation"></a>Verwenden des ArchiveItem-Vorgangs

Der **ArchiveItem-Vorgang** verwendet zwei Argumente in der Anforderung, die die Elemente identifizieren, die in das Archivpostfach und in den Zielordner für diese Elemente verschoben werden sollen. Ein Archivpostfach muss aktiviert sein, damit dieser Vorgang funktioniert. Informationen zum Aktivieren eines Archivpostfachs finden Sie unter [Verwalten In-Place Archive .](https://technet.microsoft.com/library/jj651146.aspx)
  
### <a name="archiveitem-operation-soap-headers"></a>SOAP-Header des ArchiveItem-Vorgangs

Der **ArchiveItem-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifies the culture, as defined in RFC 3066, **Tags for the Identification of Languages**, to be used to access the mailbox. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="archiveitem-operation-request-example-move-an-item-to-the-archive-inbox-folder"></a>Beispiel für eine ArchiveItem-Vorgangsanforderung: Verschieben eines Elements in den Archiv-Posteingangsordner

Das folgende Beispiel einer **ArchiveItem-Vorgangsanforderung** zeigt, wie ein Element in den Archivordner "Posteingang" verschoben wird. 
  
> [!NOTE]
> Alle Elementbezeichner und Änderungsschlüssel in diesem Artikel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:ArchiveItem>
         <m:ArchiveSourceFolderId>
            <t:DistinguishedFolderId Id="inbox"/>
         </m:ArchiveSourceFolderId>
         <m:ItemIds>
            <t:ItemId Id="AQMkG5BBwrQAAAxoAAAA=" ChangeKey="CQAAAHCtAAAAAAB7"/>
         </m:ItemIds>
      </m:ArchiveItem>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [ArchiveItem](archiveitem.md)    
- [ArchiveSourceFolderId](archivesourcefolderid.md)    
- [DistinguishedFolderId](distinguishedfolderid.md)    
- [ItemIds](itemids.md)   
- [ItemId](itemid.md)
    
## <a name="successful-archiveitem-operation-response"></a>Erfolgreiche ArchiveItem-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **ArchiveItem-Vorgangsanforderung** zum Verschieben eines Elements in ein Archivpostfach. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:ArchiveItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [ArchiveItemResponse](archiveitemresponse.md)    
- [ResponseMessages](responsemessages.md)   
- [ArchiveItemResponseMessage](archiveitemresponsemessage.md)    
- [ResponseCode](responsecode.md)    
- [Items](items.md)
    
## <a name="archiveitem-operation-error-response"></a>Fehlerantwort des ArchiveItem-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **ArchiveItem-Vorgangsanforderung.** Dies ist eine Antwort auf eine gültige Anforderung zum Archivieren eines Elements, wenn ein Archivpostfach für einen Benutzer nicht aktiviert ist. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:ArchiveItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Error">
               <m:MessageText>Archive mailbox is not enabled for this user.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [ArchiveItemResponse](archiveitemresponse.md)    
- [ResponseMessages](responsemessages.md)    
- [ArchiveItemResponseMessage](archiveitemresponsemessage.md)    
- [MessageText](messagetext.md)    
- [ResponseCode](responsecode.md)    
- [DescriptiveLinkKey](descriptivelinkkey.md)    
- [Items](items.md)
    
Weitere Fehlercodes, die für EWS generisch und für diesen Vorgang spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md) 
- [Archivierung in EWS in Exchange](https://msdn.microsoft.com/library/78ae179b-ae4f-4f64-911a-e0c70e0fa314%28Office.15%29.aspx)
    

