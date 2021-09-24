---
title: RemoveDistributionGroupFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: Hier finden Sie Informationen zum EWS-Vorgang "RemoveDistributionGroupFromImList".
ms.openlocfilehash: 52b653008b7b14d2c2467cc9bb1f8f1475cee8f5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513395"
---
# <a name="removedistributiongroupfromimlist-operation"></a>RemoveDistributionGroupFromImList-Vorgang

Hier finden Sie Informationen zum EWS-Vorgang **"RemoveDistributionGroupFromImList".** 
  
Der **RemoveDistributionGroupFromImList-Vorgang** entfernt eine Verteilergruppe aus der Lync-Chatliste, wenn Lync Exchange für den Kontaktspeicher verwendet. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a>Verwenden des RemoveDistributionGroupFromImList-Vorgangs

Der **RemoveDistributionGroupFromImList-Vorgang** akzeptiert ein einzelnes Argument, das eine Verteilergruppe identifiziert, die aus der auf einem Exchange Server gespeicherten Lync-Chatliste entfernt werden soll. 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a>SOAP-Header des RemoveDistributionGroupFromImList-Vorgangs

Der **RemoveDistributionGroupFromImList-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a>RemoveDistributionGroupFromImList-Vorgangsanforderungsbeispiel: Entfernen einer Verteilergruppe aus einer Chatliste

Das folgende Beispiel einer **RemoveDistributionGroupFromImList-Vorgangsanforderung** zeigt, wie sie eine Verteilergruppe aus einer Chatgruppe entfernt. Der **RemoveDistributionGroupFromImList-Vorgang** akzeptiert den eindeutigen Gruppenbezeichner, um die Verteilergruppe zu identifizieren, die aus der Chatliste entfernt werden soll. Das [ExchangeStoreId-Element,](exchangestoreid.md) das in der Antwort für den [GetImItemList-Vorgang](getimitemlist-operation.md) zurückgegeben wird, und der [AddDistributionGroupToImList-Vorgang](adddistributiongrouptoimlist-operation.md) identifiziert Verteilergruppen, die aus der Chatliste entfernt werden können. 
  
> [!NOTE]
> Alle Elementbezeichner und Änderungsschlüssel in diesem Artikel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveDistributionGroupFromImList>
         <m:GroupId Id="AAMkADEzO4QrAABmEh5oAAA="/>
      </m:RemoveDistributionGroupFromImList>
   </soap:Body>
</soap:Envelope>
```

Die folgenden Elemente werden im SOAP-Anforderungstext verwendet:
  
- [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a>Erfolgreiche RemoveDistributionGroupFromImList-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveDistributionGroupFromImList-Vorgangsanforderung** zum Entfernen einer Verteilergruppe aus einer Chatgruppe. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

Die folgenden Elemente werden im SOAP-Antworttext verwendet:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a>Fehlerantwortbeispiel für RemoveDistributionGroupFromImList-Vorgang

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **RemoveDistributionGroupFromImList-Vorgangsanforderung.** Dies ist eine Antwort auf eine Anforderung zum Entfernen einer Verteilergruppe, die bereits aus dem Postfach entfernt wurde. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

Die folgenden Elemente werden im SOAP-Textkörper der Fehlerantwort verwendet:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetImItemList-Vorgang](getimitemlist-operation.md)
    
- [AddDistributionGroupToImList-Vorgang](adddistributiongrouptoimlist-operation.md)
    
- [Personen und Kontakte in EWS in Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

