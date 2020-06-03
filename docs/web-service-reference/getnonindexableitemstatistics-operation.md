---
title: GetNonIndexableItemStatistics-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: Hier finden Sie Informationen zum GetNonIndexableItemStatistics-EWS-Vorgang.
ms.openlocfilehash: c7d49f9e0d7b4191c7403cb4d1a20e70a96c3882
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452818"
---
# <a name="getnonindexableitemstatistics-operation"></a>GetNonIndexableItemStatistics-Vorgang

Hier finden Sie Informationen zum **GetNonIndexableItemStatistics** -EWS-Vorgang. 
  
Der **GetNonIndexableItemStatistics** -Vorgang ruft die Anzahl der Elemente ab, die nicht in einem Postfach indiziert werden können. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a>Verwenden des GetNonIndexableItemStatistics-Vorgangs

Der **GetNonIndexableItemStatistics** -Vorgang zählt Postfachelemente, die nicht indiziert werden können. Elemente, die nicht indiziert werden können, werden während einer Discovery-Suche nicht durchsucht. 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a>SOAP-Header des GetNonIndexableItemStatistics-Vorgangs

Der **GetNonIndexableItemStatistics** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a>GetNonIndexableItemStatistics-Vorgangs Anforderungs Beispiel: Abrufen der Anzahl von Elementen, die nicht in einem Postfach indiziert werden können

Im folgenden Beispiel einer **GetNonIndexableItemStatistics** -Vorgangsanforderung wird veranschaulicht, wie die Anzahl der Elemente angefordert wird, die nicht in einem Postfach indiziert werden können. 
  
> [!NOTE]
> Alle Legacy Domänennamen in diesem Beispiel sind verkürzt worden, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemStatistics>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIDLT)/cn=Recipients/cn=3518cf-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemStatistics>
   </soap:Body>
</soap:Envelope>

```

Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)
    
- [Postfächer (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [LegacyDN](legacydn.md)
    
- [SearchArchiveOnly](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a>Erfolgreiche Reaktion des GetNonIndexableItemStatistics-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetNonIndexableItemStatistics** -Vorgangsanforderung zum Abrufen der Anzahl von Elementen, die nicht in einem Postfach indiziert werden können. 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [NonIndexableItemStatistics](nonindexableitemstatistics.md)
    
- [NonIndexableItemStatistic](nonindexableitemstatistic.md)
    
- [Postfach (Zeichenfolge)](mailbox-string.md)
    
- [ItemCount](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a>Fehlerantwort des GetNonIndexableItemStatistics-Vorgangs

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetNonIndexableItemStatistics** -Vorgangsanforderung. Dies ist eine Antwort auf eine Anforderung zum Abrufen der Anzahl von Elementen, die nicht aus mehr als einem Postfach indiziert werden können. 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes-Vorgang](getsearchablemailboxes-operation.md)
    
- [SearchMailboxes-Vorgang](searchmailboxes-operation.md)
    
- [GetHoldOnMailboxes-Vorgang](getholdonmailboxes-operation.md)
    
- [SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration-Vorgang](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails-Vorgang](getnonindexableitemdetails-operation.md)
    

