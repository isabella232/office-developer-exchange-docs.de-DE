---
title: GetSearchableMailboxes-Vorgang
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: Hier finden Sie Informationen zum GetSearchableMailboxes-EWS-Vorgang.
ms.openlocfilehash: e893a66eb1b638479eeccc6bd7548cb020f37243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530839"
---
# <a name="getsearchablemailboxes-operation"></a>GetSearchableMailboxes-Vorgang

> [!IMPORTANT]
> Ab dem 1. April 2020 ist der GetSearchableMailboxes-Vorgang in Exchange Online nicht mehr verfügbar. Dieser Vorgang ist in lokalen Versionen von Exchange Server nicht betroffen. Weitere Informationen finden Sie unter [Retirement of Legacy eDiscovery Tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).

Hier finden Sie Informationen zum **GetSearchableMailboxes** -EWS-Vorgang. 
  
Der **GetSearchableMailboxes** -Vorgang ruft einen Bereich mit durchsuchbaren Postfächern für Ermittlungs suchen ab. Der Umfang der durchsuchbaren Postfächer, die in der Antwort zurückgegeben werden, wird durch den Suchfilter bestimmt und ob die Mitgliedschaft in Verteilergruppen erweitert wird. 

> [!NOTE] 
> Dieser Vorgang ist für die Verwendung mit dem Suchfilter und zum Abrufen nur der ersten paar Tausender vorgesehen. Es ist nicht für den vollständigen Abruf vorgesehen.
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getsearchablemailboxes-operation"></a>Verwenden des GetSearchableMailboxes-Vorgangs

Der **GetSearchableMailboxes** -Vorgang ruft Informationen zu durchsuchbaren Postfächern ab. Die folgenden Argumente können in der Anforderung übergeben werden: 
  
- [SearchFilter](searchfilter.md) – akzeptiert einen einzelnen e-Mail-Alias als Argument. 
    
- [ExpandGroupMembership](expandgroupmembership.md) – gibt an, ob die Mitgliedschaft in Verteilergruppen in den Ergebnissen erweitert wird, die in der Antwort zurückgegeben werden. 
    
Wenn der e-Mail-Aliassatz im Suchfilter eine Verteilergruppe ist und die Mitgliedschaft der Verteilergruppe nicht erweitert wird, enthält die Antwort die Postfachinformationen für die Verteilergruppe. Wenn der e-Mail-Aliassatz im Suchfilter eine Verteilergruppe ist und die Mitgliedschaft der Verteilergruppe erweitert wird, enthält die Antwort die Postfachinformationen für jedes Postfach, das Mitglied der Verteilergruppe ist. Wenn der Suchfilter den Alias eines einzelnen Benutzers enthält, enthält die Antwort die Postfachinformationen für den einzelnen Benutzer. Die Antwort enthält alle durchsuchbaren Postfächer, wenn das [GetSearchableMailboxes](getsearchablemailboxes.md) -Element leer ist. Dies ist identisch mit einem leeren [SearchFilter](searchfilter.md) -Element und dem [ExpandGroupMembership](expandgroupmembership.md) -Element, das auf **false**festgelegt ist.
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a>SOAP-Header des GetSearchableMailboxes-Vorgangs

Der **GetSearchableMailboxes** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|Headername|Element|Beschreibung|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a>GetSearchableMailboxes-Vorgangs Anforderungs Beispiel: Anfordern von Informationen zu einer Verteilergruppe

Im folgenden Beispiel einer **GetSearchableMailboxes** -Vorgangsanforderung wird gezeigt, wie die Postfachinformationen für die lolgroup-Verteilergruppe abgerufen werden. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetSearchableMailboxes>
         <m:SearchFilter>lolgroup</m:SearchFilter>
         <m:ExpandGroupMembership>false</m:ExpandGroupMembership>
      </m:GetSearchableMailboxes>
   </soap:Body>
</soap:Envelope>

```

Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [GetSearchableMailboxes](getsearchablemailboxes.md)   
- [SearchFilter](searchfilter.md)    
- [ExpandGroupMembership](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a>Erfolgreiche GetSearchableMailboxes-Vorgangs Antwort: Abrufen von Informationen zu einer Verteilergruppe

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSearchableMailboxes** -Vorgangsanforderung zum Abrufen der Ermittlungsinformationen für die lolgroup-Verteilergruppe. 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Guid>33a408fe-2574-4e3b-49f5-5e1e000a3035</Guid>
               <PrimarySmtpAddress>LOLgroup@contoso.com</PrimarySmtpAddress>
               <IsExternalMailbox>false</IsExternalMailbox>
               <ExternalEmailAddress/>
               <DisplayName>LOLgroup</DisplayName>
               <IsMembershipGroup>true</IsMembershipGroup>
               <ReferenceId>/o=First/ou=Exchange(FYLT)/cn=Recipients/cn=81213b958a0b5295b13b3f02b812bf1bc-LOLgroup</ReferenceId>
            </SearchableMailbox>
         </SearchableMailboxes>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)   
- [ResponseCode](responsecode.md)   
- [SearchableMailboxes](searchablemailboxes.md)    
- [SearchableMailbox](searchablemailbox.md)    
- [Guid](guid-ex15websvcsotherref.md)    
- [PrimarySmtpAddress](primarysmtpaddress.md)    
- [IsExternalMailbox](isexternalmailbox.md)   
- [ExternalEmailAddress](externalemailaddress.md)    
- [DisplayName (Zeichenfolge)](displayname-string.md)    
- [Ismembershipgroup](ismembershipgroup.md)    
- [ReferenceId](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a>Erfolgreiche GetSearchableMailboxes-Vorgangs Antwort: Abrufen von Informationen zu einer erweiterten Verteilergruppe

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSearchableMailboxes** -Vorgangsanforderung zum Abrufen der Ermittlungsinformationen über Mitglieder der erweiterten lolgroup-Verteilergruppe. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>3c620d04-8b33-435a-95be-5b939375576</Guid>
          <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Steven Brown</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=90312341a742f0e47e392c80a60d13ecf-Steve</ReferenceId>
        </SearchableMailbox>
      </SearchableMailboxes>
    </GetSearchableMailboxesResponse>
  </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)    
- [ResponseCode](responsecode.md)   
- [SearchableMailboxes](searchablemailboxes.md)    
- [SearchableMailbox](searchablemailbox.md)    
- [Guid](guid-ex15websvcsotherref.md)    
- [PrimarySmtpAddress](primarysmtpaddress.md)    
- [IsExternalMailbox](isexternalmailbox.md)    
- [ExternalEmailAddress](externalemailaddress.md)    
- [DisplayName (Zeichenfolge)](displayname-string.md)    
- [Ismembershipgroup](ismembershipgroup.md)    
- [ReferenceId](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a>Fehlerantwort des GetSearchableMailboxes-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetSearchableMailboxes** -Vorgangsanforderung. Dies ist eine Antwort auf eine Anforderung zum Abrufen aller durchsuchbaren Postfächer, wenn das **ExpandGroupMembership** -Argument auf **true**festgelegt ist. 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)  
- [MessageText](messagetext.md)   
- [ResponseCode](responsecode.md)   
- [DescriptiveLinkKey](descriptivelinkkey.md) 
- [SearchableMailboxes](searchablemailboxes.md)
    
Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)   
- [SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md)   
- [SearchMailboxes-Vorgang](searchmailboxes-operation.md)   
- [GetHoldOnMailboxes-Vorgang](getholdonmailboxes-operation.md)    
- [GetDiscoverySearchConfiguration-Vorgang](getdiscoverysearchconfiguration-operation.md)   
- [GetNonIndexableItemDetails-Vorgang](getnonindexableitemdetails-operation.md)   
- [GetNonIndexableItemStatistics-Vorgang](getnonindexableitemstatistics-operation.md)
    

