---
title: SetImGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d48aa07-8152-4c3d-a519-061253e80174
description: Hier finden Sie Informationen zum SetImGroup-EWS-Vorgang.
ms.openlocfilehash: 37b290559fff0b2de57669741547ba4b1b56c28c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44438075"
---
# <a name="setimgroup-operation"></a>SetImGroup-Vorgang

Hier finden Sie Informationen zum **SetImGroup** -EWS-Vorgang. 
  
Der **SetImGroup** -Vorgang ändert den Anzeigenamen einer Chatgruppe (Instant Messaging). 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-setimgroup-operation"></a>Verwenden des SetImGroup-Vorgangs

Für den **SetImGroup** -Vorgang wird nur ein einzelnes Anzeigename-Argument verwendet. 
  
### <a name="setimgroup-operation-soap-headers"></a>SOAP-Header des SetImGroup-Vorgangs

Der **SetImGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="setimgroup-operation-request-example"></a>SetImGroup-Vorgangsanforderung (Beispiel)

Im folgenden Beispiel einer **SetImGroup** -Vorgangsanforderung wird gezeigt, wie ein Anzeigename einer Chatgruppe in "MyNewGroupName" geändert wird. 
  
> [!NOTE]
> Die Exchange-Informationsspeicher-ID wurde verkürzt, um die Lesbarkeit zu erhalten. 
  
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
      <m:SetImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
         <m:NewDisplayName>MyNewGroupName</m:NewDisplayName>
      </m:SetImGroup>
   </soap:Body>
</soap:Envelope>
```

Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [SetImGroup](setimgroup.md)
    
- [GroupId](groupid.md)
    
- [Neuanzeigename](newdisplayname.md)
    
## <a name="successful-setimgroup-operation-response"></a>Erfolgreiche Reaktion des SetImGroup-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **SetImGroup** -Vorgangsanforderung. 
  
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
      <SetImGroupResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         </SetImGroupResponse>
      </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [SetImGroupResponse](setimgroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="setimgroup-operation-error-response"></a>Fehlerantwort des SetImGroup-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **SetImGroup** -Vorgangsanforderung. Die folgende Fehlermeldung tritt auf, wenn versucht wird, den Anzeigenamen der Gruppe in den vorhandenen Gruppen Anzeigenamen zu ändern. 
  
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
      <SetImGroupResponse ResponseClass="Error" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>An IM group with the specified display name already exists.</MessageText>
         <ResponseCode>ErrorImGroupDisplayNameAlreadyExists</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetImGroupResponse>
   </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [SetImGroupResponse](setimgroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [Personen und Kontakte in EWS in Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [AddImGroup-Vorgang](addimgroup-operation.md)
    
- [RemoveImGroup-Vorgang](removeimgroup-operation.md)
    

