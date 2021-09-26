---
title: SetHoldOnMailboxes-Vorgang
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: Hier finden Sie Informationen zum EWS-Vorgang "SetHoldOnMailboxes".
ms.openlocfilehash: d4774af88e94a14103aa883774f193e84338c9f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542788"
---
# <a name="setholdonmailboxes-operation"></a>SetHoldOnMailboxes-Vorgang

> [!IMPORTANT]
> Ab dem 1. April 2020 ist der SetHoldOnMailboxes-Vorgang in Exchange Online nicht mehr verfügbar. Dieser Vorgang ist in lokalen Versionen von Exchange Server nicht betroffen. Weitere Informationen finden Sie unter ["Ausmustern älterer eDiscovery-Tools" in Exchange Online.](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api)

Hier finden Sie Informationen zum EWS-Vorgang **"SetHoldOnMailboxes".** 
  
Der **SetHoldOnMailboxes-Vorgang** legt eine Aufbewahrungsrichtlinie für Postfächer fest. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-setholdonmailboxes-operation"></a>Verwenden des SetHoldOnMailboxes-Vorgangs

Der **SetHoldOnMailboxes-Vorgang** legt eine Postfachsperre auf ein oder mehrere Postfächer fest. 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a>SOAP-Header des SetHoldOnMailboxes-Vorgangs

Der **SetHoldOnMailboxes-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifiziert die Serverrollen, die erforderlich sind, damit der Aufrufer die Anforderung stellen kann. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a>SetHoldOnMailboxes-Vorgangsanforderungsbeispiel: Anwenden einer Aufbewahrung auf ein Postfach

Das folgende Beispiel einer **SetHoldOnMailboxes-Vorgangsanforderung** zeigt, wie eine Aufbewahrung auf zwei Postfächer angewendet wird. Die Postfachsperre wurde mithilfe des [Befehls "New-MailboxSearch"](https://technet.microsoft.com/library/dd298064.aspx) erstellt. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SetHoldOnMailboxes>
         <m:ActionType>Create</m:ActionType>
         <m:HoldId>HoldId2</m:HoldId>
         <m:Query>test</m:Query>
         <m:Mailboxes>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</t:String>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</t:String>
         </m:Mailboxes>
         <m:Language>English</m:Language>
         <m:IncludeNonIndexableItems>false</m:IncludeNonIndexableItems>
         <m:Deduplication>true</m:Deduplication>
      </m:SetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [SetHoldOnMailboxes](setholdonmailboxes.md)
    
- [ActionType (HoldActionType)](actiontype-holdactiontype.md)
    
- [HoldId](holdid.md)
    
- [Query](query.md)
    
- [Postfächer (ArrayOfStringsType)](mailboxes-arrayofstringstype.md)
    
- [String](string.md)
    
- [Language](language.md)
    
- [IncludeNonIndexableItems](includenonindexableitems.md)
    
- [Deduplizierung](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a>Erfolgreiche Antwort des SetHoldOnMailboxes-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **SetHoldOnMailboxes-Vorgangsanforderung,** um zwei Postfächer in die Warteschleife zu setzen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="https://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [SetHoldOnMailboxesResponse](setholdonmailboxesresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [MailboxHoldResult](mailboxholdresult.md)
    
- [HoldId](holdid.md)
    
- [Query](query.md)
    
- [MailboxHoldStatuses](mailboxholdstatuses.md)
    
- [MailboxHoldStatus](mailboxholdstatus.md)
    
- [Postfach (Zeichenfolge)](mailbox-string.md)
    
- [Status (HoldStatusType)](status-holdstatustype.md)
    
- [AdditionalInfo](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a>Fehlerantwort des SetHoldOnMailboxes-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **SetHoldOnMailboxes-Vorgangsanforderung.** Dies ist eine Antwort auf eine Anforderung, die einen falsch angegebenen Postfachbezeichner enthält. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013"
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [SetHoldOnMailboxesResponse](setholdonmailboxesresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Fehlercodes, die für EWS generisch und für diesen Vorgang spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes-Vorgang](getsearchablemailboxes-operation.md)
    
- [SearchMailboxes-Vorgang](searchmailboxes-operation.md)
    
- [GetHoldOnMailboxes-Vorgang](getholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration-Vorgang](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails-Vorgang](getnonindexableitemdetails-operation.md)
    
- [GetNonIndexableItemStatistics-Vorgang](getnonindexableitemstatistics-operation.md)
    

