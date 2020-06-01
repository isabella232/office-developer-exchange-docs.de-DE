---
title: RemoveContactFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Hier finden Sie Informationen zum RemoveContactFromImList-EWS-Vorgang.
ms.openlocfilehash: 8b3d83a0b53bad169d9f3478540e5087901f3a12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458467"
---
# <a name="removecontactfromimlist-operation"></a>RemoveContactFromImList-Vorgang

Hier finden Sie Informationen zum **RemoveContactFromImList** -EWS-Vorgang. 
  
Der **RemoveContactFromImList** -Vorgang entfernt Kontakte aus der lync-Chat-Liste (Instant Messaging), wenn lync Exchange für den Kontaktspeicher verwendet. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-removecontactfromimlist-operation"></a>Verwenden des RemoveContactFromImList-Vorgangs

Der **RemoveContactFromImList** -Vorgang akzeptiert ein einzelnes Argument, das einen Kontakt identifiziert, der aus der auf einem Exchange-Server gespeicherten lync-Kontaktliste entfernt werden soll. Die Liste der Kontakte, die dieser Vorgang als Ziel hat, wird in Outlook 2013 als **lync-Kontakte** bezeichnet. 
  
> [!CAUTION]
> Verwenden Sie nicht den [DeleteItem-Vorgang](deleteitem-operation.md) , um Kontakte aus einer Kontaktliste zu entfernen. Möglicherweise muss eine weitere serverseitige Verarbeitung durchgeführt werden, um das Entfernen eines Kontakts aus der **lync-Kontakt** Liste zu unterstützen. Beachten Sie, dass die **lync-Kontakt** Liste die konzeptionelle Entsprechung des Standardordners für **lync-Kontakte** ist. 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a>SOAP-Header des RemoveContactFromImList-Vorgangs

Der **RemoveContactFromImList** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a>RemoveContactFromImList-Vorgangs Anforderungs Beispiel: Entfernen eines Kontakts aus der lync-Kontaktliste

Im folgenden Beispiel einer **RemoveContactFromImList** -Vorgangsanforderung wird gezeigt, wie ein Kontakt aus der **lync-Kontakt** Liste entfernt wird. Der **RemoveContactFromImList** -Vorgang akzeptiert eine einzelne eindeutige Kontakt-ID, um den Kontakt zu identifizieren, der aus der **lync-Kontakt** Liste entfernt wurde. 
  
> [!NOTE]
> Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
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
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

Die folgenden Elemente werden im SOAP-Anforderungstext Körper verwendet:
  
- [RemoveContactFromImList](removecontactfromimlist.md)
    
- [ContactId](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a>Erfolgreiche Reaktion des RemoveContactFromImList-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveContactFromImList** -Vorgangsanforderung, um einen Kontakt aus der **lync-Kontakt** Liste zu entfernen. 
  
```XML
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
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

Die folgenden Elemente werden im SOAP-Antworttext Körper verwendet:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a>Fehlerantwort des RemoveContactFromImList-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **RemoveContactFromImList** -Vorgangsanforderung. Dies ist eine Antwort auf eine Anforderung zum Entfernen eines Kontakts aus der **lync** -Kontaktliste, wenn der Kontakt nicht mehr in der Liste vorhanden ist. 
  
```XML
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
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

Die folgenden Elemente werden im SOAP-Textkörper der Fehlerantwort verwendet:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetImItemList-Vorgang](getimitemlist-operation.md)
    

