---
title: AddImGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6df6e504-b7c8-4773-b10f-ffa5defac229
description: Hier finden Sie Informationen zum AddImGroup-EWS-Vorgang.
ms.openlocfilehash: 9aba6a22502c1006da06ce4a9bc925f13b5b5100
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544360"
---
# <a name="addimgroup-operation"></a>AddImGroup-Vorgang

Hier finden Sie Informationen zum AddImGroup-EWS-Vorgang.  
  
Der EWS-Vorgang **(AddImGroup** Exchange Web Services) fügt einem Postfach eine neue Chatgruppe hinzu. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-addimgroup-operation"></a>Verwenden des AddImGroup-Vorgangs

Der **AddImGroup-Vorgang** verwendet nur ein einzelnes Anzeigenamenargument. 
  
Dieser Vorgang gibt den Anzeigenamen, den Gruppentyp und Exchange Speicherbezeichner der neuen Gruppe zurück.
  
Der **AddImGroup-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
**Tabelle 1. SOAP-Header des AddImGroup-Vorgangs**

|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dies gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.  <br/> |
   
## <a name="addimgroup-operation-request-example-create-a-new-im-group"></a>AddImGroup-Vorgangsanforderungsbeispiel: Erstellen einer neuen Chatgruppe

Das folgende Beispiel einer **AddImGroup-Vorgangsanforderung** zeigt, wie Eine Chatgruppe mit dem Namen MyCustomerGroup erstellt wird. 
  
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
      <m:AddImGroup>
         <m:DisplayName>MyCustomGroup</m:DisplayName>
      </m:AddImGroup>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [AddImGroup](addimgroup.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
## <a name="successful-addimgroup-operation-response"></a>Erfolgreiche AddImGroup-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **AddImGroup-Vorgangsanforderung.** 
  
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
      <AddImGroupResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImGroup>
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">MyCustomGroup</DisplayName>
            <GroupType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">IPM.DistList.MOC.UserGroup</GroupType>
            <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MAAA="
                             ChangeKey="EgAAAA=="
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types"/>
         </ImGroup>
      </AddImGroupResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [AddImGroupResponse](addimgroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [ImGroup](imgroup.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [GroupType](grouptype.md)
    
- [ExchangeStoreId](exchangestoreid.md)
    
## <a name="addimgroup-operation-error-response"></a>AddImGroup-Vorgangsfehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **AddImGroup-Vorgangsanforderung.** Dies ist eine Antwort auf eine Anforderung, die ein Zeichen enthält, das nicht in einem Anzeigenamen verwendet werden kann. Beachten Sie, dass dies ein SOAP-Fehler und keine schemabasierte Fehlermeldung ist. Der in der Anforderung übermittelte Anzeigename ist ~!@#$%^ &amp; und der Fehler tritt auf dem Zeichen &amp; auf. Das &amp; Zeichen ist in der 11. Zeile und im 33. Zeichen in der Anforderungsnutzlast aufgetreten. Die Antwort wurde mit einem HTTP 500-Code zurückgegeben. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="https://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
         <faultstring xml:lang="en-US">The request failed schema validation: An error occurred while parsing EntityName. Line 11, position 33.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
            <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
            <t:MessageXml xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
               <t:LineNumber>11</t:LineNumber>
               <t:LinePosition>33</t:LinePosition>
               <t:Violation>An error occurred while parsing EntityName. Line 11, position 33.</t:Violation>
            </t:MessageXml>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [Personen und Kontakte in EWS in Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [RemoveImGroup-Vorgang](removeimgroup-operation.md)
    
- [SetImGroup](setimgroup.md)
    

