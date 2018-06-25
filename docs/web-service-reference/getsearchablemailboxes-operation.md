---
title: GetSearchableMailboxes-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: Hier finden Sie Informationen über die GetSearchableMailboxes EWS Vorgang.
ms.openlocfilehash: 5e14288280b23e2555eea4fce0f77743d7d210ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758794"
---
# <a name="getsearchablemailboxes-operation"></a>GetSearchableMailboxes-Vorgang

Hier finden Sie Informationen zum **GetSearchableMailboxes** EWS-Vorgang. 
  
Der Vorgang **GetSearchableMailboxes** Ruft eine bestimmte Gruppe von durchsuchbaren Postfächer für Suchvorgänge Ermittlung ab. Der Bereich der durchsuchbar Postfächer in der Antwort zurückgegeben, hängt von den Suchfilter und gibt an, ob die Verteilung der Gruppenmitgliedschaft erweitert ist. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getsearchablemailboxes-operation"></a>Verwenden des GetSearchableMailboxes-Vorgangs

Der Vorgang **GetSearchableMailboxes** Ruft Informationen zu Postfächern durchsuchbar ab. Die folgenden Argumente können in der Anforderung übergeben werden: 
  
- [SearchFilter](searchfilter.md) – einen einzelne e-Mail-Alias als Argument akzeptiert. 
    
- [ExpandGroupMembership](expandgroupmembership.md) – gibt an, ob die Verteilung Gruppenmitgliedschaft in die in der Antwort zurückgegebenen Ergebnisse erweitert ist. 
    
Wenn das e-Mail-Alias im Suchfilter festgelegt, eine Verteilergruppe ist, und die Verteilung der Gruppenmitgliedschaft wird nicht erweitert, enthält die Antwort die Postfachinformationen für die Verteilergruppe. Wenn das e-Mail-Alias im Suchfilter festgelegt, eine Verteilergruppe ist und Gruppenmitgliedschaft Verteilergruppe wird erweitert, enthält die Antwort die Postfachinformationen für jedes Postfach, das Mitglied der Verteilergruppe ist. Wenn der Suchfilter Alias für einen einzelnen Benutzer enthält, wird die Antwort die Postfachinformationen für die einzelnen Benutzer enthalten. Die Antwort enthält alle Postfächer durchsucht werden, wenn das Element [GetSearchableMailboxes](getsearchablemailboxes.md) leer ist. Dies ist dasselbe wie ein leeres Element [SearchFilter](searchfilter.md) und das [ExpandGroupMembership](expandgroupmembership.md) -Element auf **"false"** festgelegt.
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a>GetSearchableMailboxes Vorgang SOAP-Header

Der Vorgang **GetSearchableMailboxes** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a>GetSearchableMailboxes Vorgang-anforderungsbeispiel: Anfordern von Informationen zu einer Verteilergruppe

Im folgenden Beispiel wird eine **GetSearchableMailboxes** Vorgang Anforderung veranschaulicht, wie die Postfachinformationen für die Verteilergruppe Lolgroup abgerufen. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [GetSearchableMailboxes](getsearchablemailboxes.md)
    
- [SearchFilter](searchfilter.md)
    
- [ExpandGroupMembership](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a>Erfolgreiche GetSearchableMailboxes Vorgangsantwort: Abrufen von Informationen zu einer Verteilergruppe

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSearchableMailboxes** Vorgang Anforderung zum Abrufen der Discovery-Informationen für die Verteilergruppe Lolgroup. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchableMailboxes](searchablemailboxes.md)
    
- [SearchableMailbox](searchablemailbox.md)
    
- [Guid](guid-ex15websvcsotherref.md)
    
- [PrimarySmtpAddress](primarysmtpaddress.md)
    
- [IsExternalMailbox](isexternalmailbox.md)
    
- [ExternalEmailAddress](externalemailaddress.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [IsMembershipGroup](ismembershipgroup.md)
    
- [ReferenceId](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a>Erfolgreiche GetSearchableMailboxes Vorgangsantwort: Abrufen von Informationen zu einer erweiterten Verteilergruppe

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **GetSearchableMailboxes** -Vorgang der Mitglieder der Verteilergruppe erweiterten Lolgroup Ermittlungsinformationen zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchableMailboxes](searchablemailboxes.md)
    
- [SearchableMailbox](searchablemailbox.md)
    
- [Guid](guid-ex15websvcsotherref.md)
    
- [PrimarySmtpAddress](primarysmtpaddress.md)
    
- [IsExternalMailbox](isexternalmailbox.md)
    
- [ExternalEmailAddress](externalemailaddress.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [IsMembershipGroup](ismembershipgroup.md)
    
- [ReferenceId](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a>GetSearchableMailboxes Vorgang Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetSearchableMailboxes** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung an alle durchsuchbaren Postfächer zu erhalten, wenn das **ExpandGroupMembership** -Argument auf **true**festgelegt ist. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526"
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [SearchableMailboxes](searchablemailboxes.md)
    
Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md)
    
- [SearchMailboxes-Vorgang](searchmailboxes-operation.md)
    
- [GetHoldOnMailboxes-Vorgang](getholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration-Vorgang](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails-Vorgang](getnonindexableitemdetails-operation.md)
    
- [GetNonIndexableItemStatistics-Vorgang](getnonindexableitemstatistics-operation.md)
    

