---
title: MarkAllItemsAsRead-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: Hier finden Sie Informationen zum EWS-Vorgang "MarkAllItemsAsRead".
ms.openlocfilehash: 104eed826df2b8734aa3159c976a6e1f388c302f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519282"
---
# <a name="markallitemsasread-operation"></a>MarkAllItemsAsRead-Vorgang

Hier finden Sie Informationen zum EWS-Vorgang **"MarkAllItemsAsRead".** 
  
Der **MarkAllItemsAsRead-Vorgang** legt die [IsRead-Eigenschaft](isread.md) für alle Elemente in einem oder mehreren Ordnern fest, um anzugeben, dass alle Elemente entweder gelesen oder ungelesen sind. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-markallitemsasread-operation"></a>Verwenden des MarkAllItemsAsRead-Vorgangs

Der **MarkAllItemsAsRead-Vorgang** kann die [IsRead-Eigenschaft](isread.md) für alle Elemente in Ordnern festlegen, die entweder durch den Exchange Web Services (EWS)-Ordnerbezeichner oder den Standardmäßigen Exchange Ordnernamens identifiziert werden. Der **MarkAllItemsAsRead-Vorgang** kann auch das Senden von Lesebestätigungen für als gelesen markierte Elemente unterdrücken. 
  
### <a name="markallitemsasread-operation-soap-headers"></a>SOAP-Header des MarkAllItemsAsRead-Vorgangs

Der **MarkAllItemsAsRead-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a>Beispiel für MarkAllItemsAsRead-Vorgangsanforderung: Markieren aller Elemente in einem Ordner als gelesen

Das folgende Beispiel einer **MarkAllItemsAsRead-Vorgangsanforderung** zeigt, wie die [IsRead-Eigenschaft,](isread.md) die auch als Leseflags bezeichnet wird, für alle Elemente in einem Ordner auf **"true"** festgelegt wird. Dieses Beispiel zeigt auch, dass Lesebestätigungen nicht als Antwort auf Lesebestätigungsanforderungen gesendet werden. 
  
> [!NOTE]
> Alle Elementbezeichner und Änderungsschlüssel in diesem Artikel wurden gekürzt, um die Lesbarkeit zu gewährleisten. Änderungsschlüssel sind für diesen Vorgang nicht erforderlich. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>true</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [MarkAllItemsAsRead](markallitemsasread.md)
    
- [ReadFlag](readflag.md)
    
- [SuppressReadReceipts](suppressreadreceipts.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a>Erfolgreiche MarkAllItemsAsRead-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MarkAllItemsAsRead-Vorgangsanforderung,** um alle Elemente in einem Ordner als gelesen zu markieren. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [MarkAllItemsAsReadResponse](markallitemsasreadresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAllItemsAsReadResponseMessage](markallitemsasreadresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a>Beispiel für MarkAllItemsAsRead-Vorgangsanforderung: Markieren aller Elemente in einem Ordner als ungelesen

Das folgende Beispiel einer **MarkAllItemsAsRead-Vorgangsanforderung** zeigt, wie die [IsRead-Eigenschaft](isread.md) für alle Elemente in einem Ordner auf **"false"** festgelegt wird. Dieses Beispiel zeigt auch, dass Lesebestätigungen nicht als Antwort auf Lesebestätigungsanforderungen gesendet werden. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>false</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

Eine erfolgreiche Antwort auf eine Anforderung zum Markieren aller Elemente als gelesen ist identisch mit der Antwort auf eine Anforderung, um alle Elemente als ungelesen zu markieren.
  
Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [MarkAllItemsAsRead](markallitemsasread.md)
    
- [ReadFlag](readflag.md)
    
- [SuppressReadReceipts](suppressreadreceipts.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a>MarkAllItemsAsRead-Vorgang – Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **MarkAllItemsAsRead-Vorgangsanforderung,** um alle Elemente in einem Ordner als gelesen oder ungelesen zu markieren, wenn der Ordner nicht im Postfach vorhanden ist. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Error">
               <m:MessageText>The specified object was not found in the store.</m:MessageText>
               <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [MarkAllItemsAsReadResponse](markallitemsasreadresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MarkAllItemsAsReadResponseMessage](markallitemsasreadresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [FindFolder-Vorgang](findfolder-operation.md)
    

