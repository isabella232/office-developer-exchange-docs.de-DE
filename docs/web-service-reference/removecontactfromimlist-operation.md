---
title: RemoveContactFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Hier finden Sie Informationen zum EWS-Vorgang "RemoveContactFromImList".
ms.openlocfilehash: cc72dc1b0abf9032fabafbaac53d29f41968dafb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523586"
---
# <a name="removecontactfromimlist-operation"></a>RemoveContactFromImList-Vorgang

Hier finden Sie Informationen zum **EWS-Vorgang "RemoveContactFromImList".** 
  
Der **Vorgang "RemoveContactFromImList"** entfernt Kontakte aus der Lync-Chatliste, wenn Lync Exchange für den Kontaktspeicher verwendet. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-removecontactfromimlist-operation"></a>Verwenden des RemoveContactFromImList-Vorgangs

Der **RemoveContactFromImList-Vorgang** akzeptiert ein einzelnes Argument, das einen Kontakt identifiziert, der aus der lync-Kontaktliste entfernt werden soll, die auf einem Exchange Server gespeichert ist. Die Liste der Kontakte, auf die dieser Vorgang abzielt, wird in Outlook 2013 als **Lync-Kontakte** bezeichnet. 
  
> [!CAUTION]
> Verwenden Sie den [DeleteItem-Vorgang](deleteitem-operation.md) nicht, um Kontakte aus einer Kontaktliste zu entfernen. Möglicherweise muss eine zusätzliche serverseitige Verarbeitung erfolgen, um das Entfernen eines Kontakts aus der **Lync-Kontaktliste** zu unterstützen. Beachten Sie, dass die **Lync-Kontaktliste** das konzeptionelle Äquivalent des standardmäßigen Postfachordners für **Lync-Kontakte** ist. 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a>SOAP-Header des RemoveContactFromImList-Vorgangs

Der **RemoveContactFromImList-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a>Beispiel für eine RemoveContactFromImList-Vorgangsanforderung: Entfernen eines Kontakts aus der Lync-Kontaktliste

Das folgende Beispiel einer **RemoveContactFromImList-Vorgangsanforderung** zeigt, wie sie einen Kontakt aus der **Lync-Kontaktliste** entfernt. Der **RemoveContactFromImList-Vorgang** akzeptiert einen einzelnen eindeutigen Kontaktbezeichner, um den Kontakt zu identifizieren, der aus der **Lync-Kontaktliste** entfernt wird. 
  
> [!NOTE]
> Alle Elementbezeichner und Änderungsschlüssel in diesem Artikel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
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

Die folgenden Elemente werden im SOAP-Anforderungstext verwendet:
  
- [RemoveContactFromImList](removecontactfromimlist.md)
    
- [ContactId](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a>Erfolgreiche RemoveContactFromImList-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveContactFromImList-Vorgangsanforderung** zum Entfernen eines Kontakts aus der **Lync-Kontaktliste.** 
  
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

Die folgenden Elemente werden im SOAP-Antworttext verwendet:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a>RemoveContactFromImList-Vorgangsfehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **RemoveContactFromImList-Vorgangsanforderung.** Dies ist eine Antwort auf eine Anforderung zum Entfernen eines Kontakts aus der **Lync-Kontaktliste,** wenn der Kontakt nicht mehr in der Liste vorhanden ist. 
  
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
    

