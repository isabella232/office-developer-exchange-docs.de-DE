---
title: RemoveImContactFromGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a190bbec-c71b-4e6a-880b-55854c724d8c
description: Hier finden Sie Informationen zum RemoveImContactFromGroup-EWS-Vorgang.
ms.openlocfilehash: 4750ef57794c3da540ac36baa8ef6ef093939ea1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466969"
---
# <a name="removeimcontactfromgroup-operation"></a>RemoveImContactFromGroup-Vorgang

Hier finden Sie Informationen zum **RemoveImContactFromGroup** -EWS-Vorgang. 
  
Mit dem **RemoveImContactFromGroup** -Vorgang wird ein einzelner Chat Kontakt aus einer Chatgruppe entfernt. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-removeimcontactfromgroup-operation"></a>Verwenden des RemoveImContactFromGroup-Vorgangs

Für den **RemoveImContactFromGroup** -Vorgang werden zwei Argumente verwendet: eine Kontaktelement-ID und die entsprechende Sofortnachrichten Gruppe, aus der der Kontakt entfernt wird. 
  
### <a name="removeimcontactfromgroup-operation-soap-headers"></a>SOAP-Header des RemoveImContactFromGroup-Vorgangs

Der **RemoveImContactFromGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="removeimcontactfromgroup-operation-request-example"></a>RemoveImContactFromGroup-Vorgangsanforderung (Beispiel)

Im folgenden Beispiel einer **RemoveImContactFromGroup** -Vorgangsanforderung wird gezeigt, wie Sie einen sofortnachrichtenkontakt aus einer Chatgruppe entfernen. 
  
> [!NOTE]
> Die Gruppen-und Kontakt-IDs wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveImContactFromGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTcAAAAvcAAA="
                      ChangeKey="EQAAABYAAABtF8oI7iVOQ"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkbWAAAAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImContactFromGroup>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [RemoveImContactFromGroup](removeimcontactfromgroup.md)
    
- [ContactId](contactid.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removeimcontactfromgroup-operation-response"></a>Erfolgreiche Reaktion des RemoveImContactFromGroup-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveImContactFromGroup** -Vorgangsanforderung. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImContactFromGroupResponse ResponseClass="Success" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [RemoveImContactFromGroupResponse](removeimcontactfromgroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removeimcontactfromgroup-operation-errorinvalidimcontactid-error-response"></a>RemoveImContactFromGroup-Vorgang ErrorInvalidImContactId-Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **RemoveImContactFromGroup** -Vorgangsanforderung. Die folgende Fehlermeldung tritt auf, wenn ein Versuch unternommen wird, ein Kontaktelement zu entfernen, das in der Gruppe "Chat" nicht vorhanden ist. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImContactFromGroupResponse ResponseClass="Error" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [RemoveImContactFromGroupResponse](removeimcontactfromgroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [Personen und Kontakte in EWS in Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md)
    
- [AddImContactToGroup](addimcontacttogroup-operation.md)
    
- [AddImGroup-Vorgang](addimgroup-operation.md)
    
- [AddNewImContactToGroup-Vorgang](addnewimcontacttogroup-operation.md)
    
- [GetImItemList-Vorgang](getimitemlist-operation.md)
    
- [GetImItems](getimitems-operation.md)
    
- [RemoveContactFromImList](removecontactfromimlist-operation.md)
    
- [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist-operation.md)
    
- [RemoveImGroup-Vorgang](removeimgroup-operation.md)
    
- [SetImGroup-Vorgang](setimgroup-operation.md)
    
- [SetImListMigrationCompleted](setimlistmigrationcompleted-operation.md)
    

