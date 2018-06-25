---
title: RemoveContactFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Hier finden Sie Informationen über die RemoveContactFromImList EWS Vorgang.
ms.openlocfilehash: 036b295a84e86ad74c467572cc52fdf6bbae5191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831080"
---
# <a name="removecontactfromimlist-operation"></a>RemoveContactFromImList-Vorgang

Hier finden Sie Informationen zum **RemoveContactFromImList** EWS-Vorgang. 
  
Der Vorgang **RemoveContactFromImList** entfernt Kontakte aus der Liste für die Lync-Sofortnachrichten (IM), bei der Lync Exchange für den Kontaktspeicher verwendet. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-removecontactfromimlist-operation"></a>Verwenden des RemoveContactFromImList-Vorgangs

Der **RemoveContactFromImList** -Vorgang akzeptiert ein einzelnes Argument, das einen Kontakt aus der Lync-Kontaktliste auf einem Exchange-Server gespeicherten entfernen identifiziert. Die Liste der Kontakte, dass dieser Vorgang Ziele **Lync-Kontakte** in Outlook 2013 aufgerufen wird. 
  
> [!CAUTION]
> Verwenden Sie die [DeleteItem Vorgang](deleteitem-operation.md) nicht um Kontakte aus einer Kontaktliste entfernen. Zusätzliche serverseitige Verarbeitung möglicherweise zur Unterstützung der Entfernen eines Kontakts aus der Liste **Kontakte Lync** auftreten. Beachten Sie, dass die **Lync** -Kontaktliste konzeptionelle Standardordner **Kontakte Lync** Postfach entspricht. 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a>RemoveContactFromImList Vorgang SOAP-Header

Der Vorgang **RemoveContactFromImList** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a>RemoveContactFromImList Vorgang-anforderungsbeispiel: Entfernen eines Kontakts aus der Liste Lync-Kontakte

Im folgenden Beispiel wird eine **RemoveContactFromImList** Vorgang Anforderung Entfernen eines Kontakts aus der Liste **Kontakte Lync** veranschaulicht. Der **RemoveContactFromImList** -Vorgang akzeptiert einen einzelnen Kontakten, eindeutigen Bezeichner, um den Kontakt zu ermitteln, der von der **Lync** -Kontaktliste entfernt wird. 
  
> [!NOTE]
> Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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

Die folgenden Elemente werden in der Anforderung SOAP-Body verwendet:
  
- [RemoveContactFromImList](removecontactfromimlist.md)
    
- [ContactId](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a>Erfolgreiche RemoveContactFromImList Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveContactFromImList** Vorgang Anforderung zum Entfernen eines Kontakts aus der **Lync** -Kontaktliste. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

Die folgenden Elemente werden in der Antwort SOAP-Body verwendet:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a>RemoveContactFromImList Vorgang Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort an eine **RemoveContactFromImList** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung an einen Kontakt aus der **Lync** -Kontaktliste entfernen, wenn der Kontakt nicht mehr in der Liste vorhanden ist. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

Die folgenden Elemente werden in die SOAP-Body-Fehlerantwort verwendet:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetImItemList-Vorgang](getimitemlist-operation.md)
    

