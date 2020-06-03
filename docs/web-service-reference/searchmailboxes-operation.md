---
title: SearchMailboxes-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: Hier finden Sie Informationen zum SearchMailboxes-EWS-Vorgang.
ms.openlocfilehash: 9ec7e9dd4ef17f22f236e64ca1fdbeb65e6e56fe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456769"
---
# <a name="searchmailboxes-operation"></a><span data-ttu-id="58c32-103">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58c32-103">SearchMailboxes operation</span></span>

> [!NOTE]
> <span data-ttu-id="58c32-104">Dieser Vorgang ist veraltet und wird von Microsoft nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58c32-104">This operation is deprecated, and no longer supported by Microsoft.</span></span>  <span data-ttu-id="58c32-105">Verwenden Sie als Ersatz den [FindItem](finditem-operation.md) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="58c32-105">As a replacement, please use the [FindItem](finditem-operation.md) operation.</span></span>

<span data-ttu-id="58c32-106">Hier finden Sie Informationen zum **SearchMailboxes** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="58c32-106">Find information about the **SearchMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="58c32-107">Der **SearchMailboxes** -Vorgang durchsucht Postfächer nach Vorkommen von Ausdrücken in Postfachelementen.</span><span class="sxs-lookup"><span data-stu-id="58c32-107">The **SearchMailboxes** operation searches mailboxes for occurrences of terms in mailbox items.</span></span> 
  
<span data-ttu-id="58c32-108">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="58c32-108">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-searchmailboxes-operation"></a><span data-ttu-id="58c32-109">Verwenden des SearchMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="58c32-109">Using the SearchMailboxes operation</span></span>

<span data-ttu-id="58c32-110">Der **SearchMailboxes** -Vorgang kann viele gleichzeitige Suchabfragen verwenden, um Ermittlungs Suche für mehrere Postfächer durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="58c32-110">The **SearchMailboxes** operation can use many simultaneous search queries to perform discovery search on multiple mailboxes.</span></span> <span data-ttu-id="58c32-111">Die Ergebnisse können entweder statistische Informationen über die Häufigkeit, mit der Suchbegriffe auftreten, oder eine Vorschau der Elemente sein, die die Suchbegriffe enthalten.</span><span class="sxs-lookup"><span data-stu-id="58c32-111">The results can be either statistical information about the number of times search terms occur, or a preview of the items that contain the search terms.</span></span> 
  
### <a name="searchmailboxes-operation-soap-headers"></a><span data-ttu-id="58c32-112">SOAP-Header des SearchMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="58c32-112">SearchMailboxes operation SOAP headers</span></span>

<span data-ttu-id="58c32-113">Der **SearchMailboxes** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="58c32-113">The **SearchMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="58c32-114">**Headername**</span><span class="sxs-lookup"><span data-stu-id="58c32-114">**Header name**</span></span>|<span data-ttu-id="58c32-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="58c32-115">**Element**</span></span>|<span data-ttu-id="58c32-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58c32-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="58c32-117">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="58c32-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="58c32-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="58c32-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="58c32-119">Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss.</span><span class="sxs-lookup"><span data-stu-id="58c32-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="58c32-120">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="58c32-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="58c32-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="58c32-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="58c32-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="58c32-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="58c32-123">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="58c32-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="58c32-124">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="58c32-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="58c32-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="58c32-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="58c32-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="58c32-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="58c32-127">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="58c32-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="58c32-128">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="58c32-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a><span data-ttu-id="58c32-129">SearchMailboxes-Vorgangs Anforderungs Beispiel: Such Postfächer für die Anzahl der Suchausdrucks Treffer</span><span class="sxs-lookup"><span data-stu-id="58c32-129">SearchMailboxes operation request example: Search mailboxes for number of search term hits</span></span>

<span data-ttu-id="58c32-130">Im folgenden Beispiel einer **SearchMailboxes** -Vorgangsanforderung wird gezeigt, wie zwei verschiedene Abfragen zum Durchsuchen von drei verschiedenen Postfächern für statistische Informationen verwendet werden, um zu erfahren, wie oft ein Ausdruck in jedem Postfach angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="58c32-130">The following example of a **SearchMailboxes** operation request shows how to use two different queries to search three different mailboxes for statistical information about how many times a term appears in each mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="58c32-131">In diesem Beispiel wird das [Abfrage](query.md) Element absichtlich leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="58c32-131">In this example, the [Query](query.md) element is intentionaly left blank.</span></span> <span data-ttu-id="58c32-132">Dies zeigt, wie eine erfolgreiche Anforderung Fehlerbedingungen pro Post Fach Such Basis enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="58c32-132">This shows how a successful request can contain error conditions on a per mailbox search basis.</span></span> 
  
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

<span data-ttu-id="58c32-133">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="58c32-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="58c32-134">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="58c32-134">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="58c32-135">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="58c32-135">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="58c32-136">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="58c32-136">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="58c32-137">Query</span><span class="sxs-lookup"><span data-stu-id="58c32-137">Query</span></span>](query.md)
    
- [<span data-ttu-id="58c32-138">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="58c32-138">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="58c32-139">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="58c32-139">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="58c32-140">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="58c32-140">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="58c32-141">SearchScope</span><span class="sxs-lookup"><span data-stu-id="58c32-141">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="58c32-142">ResultType</span><span class="sxs-lookup"><span data-stu-id="58c32-142">ResultType</span></span>](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a><span data-ttu-id="58c32-143">Erfolgreiche Reaktion des SearchMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="58c32-143">Successful SearchMailboxes operation response</span></span>

<span data-ttu-id="58c32-144">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **SearchMailboxes** -Vorgangsanforderung zum Abrufen statistischer Informationen über die Häufigkeit, mit der Suchbegriffe in den Ziel Postfächern gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="58c32-144">The following example shows a successful response to a **SearchMailboxes** operation request to get statistical information about the number of times search terms are found in the target mailboxes.</span></span> <span data-ttu-id="58c32-145">Die letzte Abfrage enthält ein leeres **Abfrage** Element, das eine fehlerhafte Postfachsuche zeigt.</span><span class="sxs-lookup"><span data-stu-id="58c32-145">The last query contains an empty **Query** element, which shows a failed mailbox search.</span></span> 
  
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

<span data-ttu-id="58c32-146">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="58c32-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="58c32-147">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="58c32-147">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="58c32-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="58c32-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="58c32-149">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="58c32-149">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="58c32-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="58c32-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="58c32-151">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="58c32-151">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="58c32-152">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="58c32-152">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="58c32-153">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="58c32-153">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="58c32-154">Query</span><span class="sxs-lookup"><span data-stu-id="58c32-154">Query</span></span>](query.md)
    
- [<span data-ttu-id="58c32-155">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="58c32-155">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="58c32-156">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="58c32-156">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="58c32-157">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="58c32-157">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="58c32-158">SearchScope</span><span class="sxs-lookup"><span data-stu-id="58c32-158">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="58c32-159">ResultType</span><span class="sxs-lookup"><span data-stu-id="58c32-159">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="58c32-160">ItemCount</span><span class="sxs-lookup"><span data-stu-id="58c32-160">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="58c32-161">Größe (lang)</span><span class="sxs-lookup"><span data-stu-id="58c32-161">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="58c32-162">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="58c32-162">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="58c32-163">KeywordStats</span><span class="sxs-lookup"><span data-stu-id="58c32-163">KeywordStats</span></span>](keywordstats.md)
    
- [<span data-ttu-id="58c32-164">KeywordStat</span><span class="sxs-lookup"><span data-stu-id="58c32-164">KeywordStat</span></span>](keywordstat.md)
    
- [<span data-ttu-id="58c32-165">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="58c32-165">Keyword</span></span>](keyword.md)
    
- [<span data-ttu-id="58c32-166">ItemHits</span><span class="sxs-lookup"><span data-stu-id="58c32-166">ItemHits</span></span>](itemhits.md)
    
- [<span data-ttu-id="58c32-167">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="58c32-167">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="58c32-168">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="58c32-168">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="58c32-169">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="58c32-169">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="58c32-170">ErrorCode (Int)</span><span class="sxs-lookup"><span data-stu-id="58c32-170">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="58c32-171">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="58c32-171">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="58c32-172">IsArchive</span><span class="sxs-lookup"><span data-stu-id="58c32-172">IsArchive</span></span>](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a><span data-ttu-id="58c32-173">Fehlerantwort des SearchMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="58c32-173">SearchMailboxes operation error response</span></span>

<span data-ttu-id="58c32-174">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **SearchMailboxes** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="58c32-174">The following example shows an error response to a **SearchMailboxes** operation request.</span></span> <span data-ttu-id="58c32-175">Dies ist eine Antwort auf eine Anforderung zum Durchsuchen eines Postfachs, wenn die Postfachbezeichner falsch ist.</span><span class="sxs-lookup"><span data-stu-id="58c32-175">This is a response to a request to search a mailbox when the mailbox identifier is incorrect.</span></span> 
  
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

<span data-ttu-id="58c32-176">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="58c32-176">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="58c32-177">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="58c32-177">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="58c32-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="58c32-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="58c32-179">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="58c32-179">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="58c32-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="58c32-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="58c32-181">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="58c32-181">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="58c32-182">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="58c32-182">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="58c32-183">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="58c32-183">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="58c32-184">Query</span><span class="sxs-lookup"><span data-stu-id="58c32-184">Query</span></span>](query.md)
    
- [<span data-ttu-id="58c32-185">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="58c32-185">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="58c32-186">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="58c32-186">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="58c32-187">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="58c32-187">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="58c32-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="58c32-188">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="58c32-189">ResultType</span><span class="sxs-lookup"><span data-stu-id="58c32-189">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="58c32-190">ItemCount</span><span class="sxs-lookup"><span data-stu-id="58c32-190">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="58c32-191">Größe (lang)</span><span class="sxs-lookup"><span data-stu-id="58c32-191">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="58c32-192">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="58c32-192">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="58c32-193">PageItemSize</span><span class="sxs-lookup"><span data-stu-id="58c32-193">PageItemSize</span></span>](pageitemsize.md)
    
- [<span data-ttu-id="58c32-194">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="58c32-194">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="58c32-195">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="58c32-195">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="58c32-196">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="58c32-196">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="58c32-197">ErrorCode (Int)</span><span class="sxs-lookup"><span data-stu-id="58c32-197">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="58c32-198">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="58c32-198">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="58c32-199">IsArchive</span><span class="sxs-lookup"><span data-stu-id="58c32-199">IsArchive</span></span>](isarchive.md)
    
<span data-ttu-id="58c32-200">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="58c32-200">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58c32-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58c32-201">See also</span></span>

- [<span data-ttu-id="58c32-202">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="58c32-202">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="58c32-203">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58c32-203">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="58c32-204">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58c32-204">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="58c32-205">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58c32-205">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="58c32-206">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58c32-206">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="58c32-207">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58c32-207">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="58c32-208">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="58c32-208">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

