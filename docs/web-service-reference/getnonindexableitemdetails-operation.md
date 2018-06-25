---
title: GetNonIndexableItemDetails-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a
description: Hier finden Sie Informationen über die GetNonIndexableItemDetails EWS Vorgang.
ms.openlocfilehash: 6b0c5afd54ac98f89bc6c5199300c20862c6f207
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758741"
---
# <a name="getnonindexableitemdetails-operation"></a>GetNonIndexableItemDetails-Vorgang

Hier finden Sie Informationen zum **GetNonIndexableItemDetails** EWS-Vorgang. 
  
Der Vorgang **GetNonIndexableItemDetails** ruft Details zu den Elementen, die nicht indiziert werden können. Dies umfasst, jedoch ist nicht beschränkt auf, die Element-ID, ein Fehlercode, eine fehlerbeschreibung, wenn versucht wurde, das Element und zusätzliche Informationen zur Datei zu indizieren. 
  
> [!NOTE]
> Obwohl das Schema gibt an, dass mehrere Postfächer kann, in der ursprünglich freigegebenen Version von Exchange 2013 durchsucht werden, unterstützt der Dienst nur erste Elementdetails für Nonindexable Elemente in ein einzelnes Postfach. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getnonindexableitemdetails-operation"></a>Verwenden des GetNonIndexableItemDetails-Vorgangs

Der Vorgang **GetNonIndexableItemDetails** identifiziert Postfachelemente, die nicht indiziert werden können und enthält Informationen, warum die Elemente nicht indiziert werden kann. Elemente, die nicht indiziert werden können, werden während eines Suchvorgangs Discovery nicht durchsucht. 
  
### <a name="getnonindexableitemdetails-operation-soap-headers"></a>GetNonIndexableItemDetails Vorgang SOAP-Header

Der Vorgang **GetNonIndexableItemDetails** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getnonindexableitemdetails-operation-request-example-get-the-details-of-an-item-that-cannot-be-indexed"></a>GetNonIndexableItemDetails Vorgang-anforderungsbeispiel: Abrufen der Details eines Elements, die nicht indiziert werden kann

Im folgenden Beispiel wird eine **GetNonIndexableItemDetails** Vorgang Anforderung veranschaulicht, wie die Details für Elemente anfordern, die für ein einzelnes Postfach nicht indiziert werden kann. Die Suche erfolgt über Primär- und Postfächer zu archivieren. 
  
> [!NOTE]
> Alle legacy Domänennamen in diesem Beispiel werden gekürzt, um den Erhaltung der Lesbarkeit. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemDetails>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemDetails>
   </soap:Body>
</soap:Envelope>

```

Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [GetNonIndexableItemDetails](getnonindexableitemdetails.md)
    
- [Postfächer (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [LegacyDN](legacydn.md)
    
- [SearchArchiveOnly](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemdetails-operation-response"></a>Erfolgreiche GetNonIndexableItemDetails Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **GetNonIndexableItemDetails** -Vorgang zum Abrufen von Elementen, die nicht indiziert werden für ein einzelnes Postfach. Das Element in diesem Beispiel wird die nicht indiziert werden ist die binaryfile.abc-Datei, die ein unbekanntes Format ist. 
  
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
      <GetNonIndexableItemDetailsResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemDetailsResult>
            <Items xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <NonIndexableItemDetail>
                  <ItemId Id="AQMkAGVmNDAyOQAAAY2fUAAAAA==" ChangeKey="CQAAAA=="/>
                  <ErrorCode>DocumentParserFailure</ErrorCode>
                  <ErrorDescription>The document parser encountered a processing error.</ErrorDescription>
                  <IsPartiallyIndexed>false</IsPartiallyIndexed>
                  <IsPermanentFailure>true</IsPermanentFailure>
                  <SortValue>502511175756</SortValue>
                  <AttemptCount>0</AttemptCount>
                  <LastAttemptTime>2012-11-15T01:56:11Z</LastAttemptTime>
                  <AdditionalInfo> 301002 Error parsing document 'exchange://localhost/Attachment/d987b1f4-9aa7-42b3-aa8c-9515a35dfa1a/1f3047d4-c287-41e4-910c-feb70c1a59f0/ef402830-3d33-4a0d-a4e9-d8576900060d/85b83861-0026-418f-8464-be2036696333/502511175756.0/binaryfile.abc'. Document has an undetectable format and will not be parsed.</AdditionalInfo>
               </NonIndexableItemDetail>
            </Items>
         </NonIndexableItemDetailsResult>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>

```

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [NonIndexableItemDetailsResult](nonindexableitemdetailsresult.md)
    
- [NonIndexableItemDetail](nonindexableitemdetail.md)
    
- [ItemId](itemid.md)
    
- [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md)
    
- [ErrorDescription](errordescription.md)
    
- [IsPartiallyIndexed](ispartiallyindexed.md)
    
- [IsPermanentFailure](ispermanentfailure.md)
    
- [SortValue](sortvalue.md)
    
- [AttemptCount](attemptcount.md)
    
- [LastAttemptTime](lastattempttime.md)
    
- [AdditionalInfo](additionalinfo.md)
    
## <a name="getnonindexableitemdetails-operation-error-response"></a>GetNonIndexableItemDetails Vorgang Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetNonIndexableItemDetails** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung zum Abrufen von Elementdetails für Elemente, die von mehr als einem Postfach nicht indiziert werden kann. 
  
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
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemDetailsResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>
```

Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:
  
- [GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes-Vorgang](getsearchablemailboxes-operation.md)
    
- [SearchMailboxes-Vorgang](searchmailboxes-operation.md)
    
- [GetHoldOnMailboxes-Vorgang](getholdonmailboxes-operation.md)
    
- [SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration-Vorgang](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemStatistics-Vorgang](getnonindexableitemstatistics-operation.md)
    

