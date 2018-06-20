---
title: RemoveDistributionGroupFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: Hier finden Sie Informationen über die RemoveDistributionGroupFromImList EWS Vorgang.
ms.openlocfilehash: 9999f98a5698dd33c22e22fdf86bd00a2d053b52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831096"
---
# <a name="removedistributiongroupfromimlist-operation"></a>RemoveDistributionGroupFromImList-Vorgang

Hier finden Sie Informationen zum **RemoveDistributionGroupFromImList** EWS-Vorgang. 
  
**RemoveDistributionGroupFromImList** -Vorgang entfernt eine Verteilergruppe aus der Liste für die Lync-Sofortnachrichten (IM), wenn Lync Exchange, um den Kontaktspeicher verwendet. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a>Verwenden des RemoveDistributionGroupFromImList-Vorgangs

Der **RemoveDistributionGroupFromImList** -Vorgang akzeptiert ein einzelnes Argument, das eine Verteilergruppe zu entfernen aus der Lync im-, die auf einem Exchange-Server identifiziert. 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a>RemoveDistributionGroupFromImList Vorgang SOAP-Header

Der Vorgang **RemoveDistributionGroupFromImList** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a>RemoveDistributionGroupFromImList Vorgang-anforderungsbeispiel: entfernen eine Verteilergruppe aus einer Liste von Sofortnachrichten

Im folgenden Beispiel wird eine **RemoveDistributionGroupFromImList** Vorgang Anforderung veranschaulicht, wie eine Verteilergruppe aus einer Instant Messaging-Gruppe zu entfernen. Der **RemoveDistributionGroupFromImList** -Vorgang akzeptiert den Bezeichner eindeutige Gruppe, um die Verteilergruppe aus der Liste Sofortnachrichten entfernen zu ermitteln. Das [ExchangeStoreId](exchangestoreid.md) -Element, das in der Antwort, für den [Vorgang GetImItemList](getimitemlist-operation.md) und den [AddDistributionGroupToImList Vorgang zurückgegeben wird](adddistributiongrouptoimlist-operation.md) identifiziert Verteilergruppen, die aus der Liste Sofortnachrichten entfernt werden können. 
  
> [!NOTE]
> Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die folgenden Elemente werden in der Anforderung SOAP-Body verwendet:
  
- [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a>Erfolgreiche RemoveDistributionGroupFromImList Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **RemoveDistributionGroupFromImList** -Vorgang zu einer Entfernen einer Verteilergruppe aus einer Gruppe von Instant Messaging. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

Die folgenden Elemente werden in der Antwort SOAP-Body verwendet:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a>RemoveDistributionGroupFromImList Vorgang Fehler antwortbeispiel

Das folgende Beispiel zeigt eine Fehlerantwort an eine **RemoveDistributionGroupFromImList** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung an eine Verteilergruppe zu entfernen, die bereits aus dem Postfach entfernt wurde. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

Die folgenden Elemente werden in die SOAP-Body-Fehlerantwort verwendet:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetImItemList-Vorgang](getimitemlist-operation.md)
    
- [AddDistributionGroupToImList-Vorgang](adddistributiongrouptoimlist-operation.md)
    
- [Benutzer und Kontakte in EWS in Exchange](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

