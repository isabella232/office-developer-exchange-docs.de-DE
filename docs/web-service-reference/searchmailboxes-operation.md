---
title: SearchMailboxes-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: Hier finden Sie Informationen zum SearchMailboxes-EWS-Vorgang.
ms.openlocfilehash: 6e154525f5ff2c3d4f24ddc50e1dae1b04a891ba
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521680"
---
# <a name="searchmailboxes-operation"></a>SearchMailboxes-Vorgang

> [!NOTE]
> Dieser Vorgang ist veraltet und wird von Microsoft nicht mehr unterstützt.  Verwenden Sie als Ersatz den [FindItem-Vorgang.](finditem-operation.md)

Hier finden Sie Informationen zum SearchMailboxes-EWS-Vorgang.  
  
Der **SearchMailboxes-Vorgang** durchsucht Postfächer nach Vorkommen von Begriffen in Postfachelementen. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-searchmailboxes-operation"></a>Verwenden des SearchMailboxes-Vorgangs

Der **SearchMailboxes-Vorgang** kann viele gleichzeitige Suchabfragen verwenden, um die Ermittlungssuche für mehrere Postfächer durchzuführen. Die Ergebnisse können entweder statistische Informationen darüber sein, wie oft Suchbegriffe auftreten, oder eine Vorschau der Elemente, die die Suchbegriffe enthalten. 
  
### <a name="searchmailboxes-operation-soap-headers"></a>Soap-Header des SearchMailboxes-Vorgangs

Der **SearchMailboxes-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifiziert die Serverrollen, die erforderlich sind, damit der Aufrufer die Anforderung stellen kann. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a>SearchMailboxes-Vorgangsanforderungsbeispiel: Durchsuchen von Postfächern nach der Anzahl von Suchbegriffstreffern

Das folgende Beispiel einer **SearchMailboxes-Vorgangsanforderung** zeigt, wie Sie mithilfe von zwei verschiedenen Abfragen drei verschiedene Postfächer nach statistischen Informationen durchsuchen, wie oft ein Ausdruck in jedem Postfach angezeigt wird. 
  
> [!NOTE]
> In diesem Beispiel ist das [Query-Element](query.md) absichtlich leer. Dies zeigt, wie eine erfolgreiche Anforderung Fehlerbedingungen pro Postfachsuchbasis enthalten kann. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SearchMailboxes>
         <m:SearchQueries>
            <t:MailboxQuery>
               <t:Query>Test Item</t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=12311a742f0e47e392c8201a60d13ecf-Steve</t:Mailbox>
                     <t:SearchScope>All</t:SearchScope>
                  </t:MailboxSearchScope>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=f00c9f70539844beb52341d8f40c572e-Antho</t:Mailbox>
                     <t:SearchScope>PrimaryOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
            <t:MailboxQuery>
               <t:Query></t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=accba4fd5ddf12214a0e82ce1645f4e-Danie</t:Mailbox>
                     <t:SearchScope>ArchiveOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
         </m:SearchQueries>
         <m:ResultType>StatisticsOnly</m:ResultType>
      </m:SearchMailboxes>
   </soap:Body>
</soap:Envelope>

```

Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [SearchMailboxes](searchmailboxes.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [Postfach (Zeichenfolge)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a>Erfolgreiche SearchMailboxes-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **SearchMailboxes-Vorgangsanforderung,** um statistische Informationen darüber abzurufen, wie oft Suchbegriffe in den Zielpostfächern gefunden werden. Die letzte Abfrage enthält ein leeres **Query-Element,** das eine fehlgeschlagene Postfachsuche anzeigt. 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=35181a94327e392c8201a60d13ecf-Steve</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=f00c9f789572-beb04001d8f40c572e-Antho</t:Mailbox>
                              <t:SearchScope>PrimaryOnly</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>2</t:ItemCount>
                  <t:Size>20206</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:KeywordStats>
                     <t:KeywordStat>
                        <t:Keyword>Test Item</t:Keyword>
                        <t:ItemHits>2</t:ItemHits>
                        <t:Size>20206</t:Size>
                     </t:KeywordStat>
                  </t:KeywordStats>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=accba4as3df234234a0e82ce1645f4e-Danie</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>The search query can't be empty.</t:ErrorMessage>
                        <t:IsArchive>true</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [SearchMailboxesResponse](searchmailboxesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchMailboxesResult](searchmailboxesresult.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [Postfach (Zeichenfolge)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
- [ItemCount](itemcount.md)
    
- [Größe (lang)](size-long.md)
    
- [PageItemCount](pageitemcount.md)
    
- [KeywordStats](keywordstats.md)
    
- [KeywordStat](keywordstat.md)
    
- [Schlüsselwort](keyword.md)
    
- [ItemHits](itemhits.md)
    
- [FailedMailboxes](failedmailboxes.md)
    
- [FailedMailbox](failedmailbox.md)
    
- [Postfach (Zeichenfolge)](mailbox-string.md)
    
- [ErrorCode (Int)](errorcode-int.md)
    
- [ErrorMessage](errormessage.md)
    
- [IsArchive](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a>SearchMailboxes-Vorgang – Fehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **SearchMailboxes-Vorgangsanforderung.** Dies ist eine Antwort auf eine Anforderung zum Durchsuchen eines Postfachs, wenn der Postfachbezeichner falsch ist. 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Error">
               <m:MessageText>No mailbox is specified for search operation. If specified in the request, 
               then it could be due to permission issue.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>subject:Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>0</t:ItemCount>
                  <t:Size>0</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>No mailbox is specified for search operation. If specified in the request, 
                        then it could be due to permission issue.</t:ErrorMessage>
                        <t:IsArchive>false</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [SearchMailboxesResponse](searchmailboxesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchMailboxesResult](searchmailboxesresult.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [Postfach (Zeichenfolge)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
- [ItemCount](itemcount.md)
    
- [Größe (lang)](size-long.md)
    
- [PageItemCount](pageitemcount.md)
    
- [PageItemSize](pageitemsize.md)
    
- [FailedMailboxes](failedmailboxes.md)
    
- [FailedMailbox](failedmailbox.md)
    
- [Postfach (Zeichenfolge)](mailbox-string.md)
    
- [ErrorCode (Int)](errorcode-int.md)
    
- [ErrorMessage](errormessage.md)
    
- [IsArchive](isarchive.md)
    
Weitere Fehlercodes, die für EWS generisch und für diesen Vorgang spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes-Vorgang](getsearchablemailboxes-operation.md)
    
- [SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md)
    
- [GetHoldOnMailboxes-Vorgang](getholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration-Vorgang](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails-Vorgang](getnonindexableitemdetails-operation.md)
    
- [GetNonIndexableItemStatistics-Vorgang](getnonindexableitemstatistics-operation.md)
    

