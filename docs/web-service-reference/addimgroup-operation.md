---
title: AddImGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6df6e504-b7c8-4773-b10f-ffa5defac229
description: Hier finden Sie Informationen über die AddImGroup EWS Vorgang.
ms.openlocfilehash: 91236f9ad2236b3f6bee600b9d57bcf736090ed7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757225"
---
# <a name="addimgroup-operation"></a>AddImGroup-Vorgang

Hier finden Sie Informationen zum **AddImGroup** EWS-Vorgang. 
  
Der Vorgang des **AddImGroup** Exchange-Webdienste (EWS) hinzugefügt ein Postfach eine neue instant messaging (IM)-Gruppe. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-addimgroup-operation"></a>Verwenden des AddImGroup-Vorgangs

Der Vorgang **AddImGroup** dauert nur ein einzelnes Display Name-Argument. 
  
Dieser Vorgang gibt den Anzeigenamen, Gruppentyp und Exchange-Speicher Bezeichner der neuen Gruppe zurück.
  
Der Vorgang **AddImGroup** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
**In Tabelle 1. AddImGroup Vorgang SOAP-Header**

|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Dies gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.  <br/> |
   
## <a name="addimgroup-operation-request-example-create-a-new-im-group"></a>AddImGroup Vorgang-anforderungsbeispiel: Erstellen einer neuen Gruppe Instant Messaging

Im folgenden Beispiel wird ein **AddImGroup** Vorgang Anforderung veranschaulicht, wie eine Instant Messaging-Gruppe mit dem Namen MyCustomerGroup erstellen. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [AddImGroup](addimgroup.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
## <a name="successful-addimgroup-operation-response"></a>Erfolgreiche AddImGroup Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **AddImGroup** -Vorgang. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="349"
                           MinorBuildNumber="0"
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddImGroupResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImGroup>
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">MyCustomGroup</DisplayName>
            <GroupType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">IPM.DistList.MOC.UserGroup</GroupType>
            <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MAAA="
                             ChangeKey="EgAAAA=="
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types"/>
         </ImGroup>
      </AddImGroupResponse>
   </s:Body>
</s:Envelope>
```

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [AddImGroupResponse](addimgroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [ImGroup](imgroup.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [GroupType](grouptype.md)
    
- [ExchangeStoreId](exchangestoreid.md)
    
## <a name="addimgroup-operation-error-response"></a>AddImGroup Vorgang Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort an eine **AddImGroup** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung, die ein Zeichen enthält, die in einen Anzeigenamen verwendet werden kann. Beachten Sie, dass dies ein SOAP-Fehler und keine Schema-basierte Fehlermeldung angezeigt wird. Ist der Anzeigename in der Anforderung übermittelt ~! @# $% ^&amp;, und der Fehler auftritt, klicken Sie auf die &amp; Zeichen. Die &amp; Zeichen auf das 11. Linien- und 33rd Zeichen in der Anforderungsnutzlast aufgetreten ist. Die Antwort wurde mit einem Code HTTP 500 zurückgegeben. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
         <faultstring xml:lang="en-US">The request failed schema validation: An error occurred while parsing EntityName. Line 11, position 33.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
            <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
            <t:MessageXml xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

- [Benutzer und Kontakte in EWS in Exchange](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [RemoveImGroup-Vorgang](removeimgroup-operation.md)
    
- [SetImGroup](setimgroup.md)
    

