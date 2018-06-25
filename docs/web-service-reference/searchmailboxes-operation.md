---
title: SearchMailboxes-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: Hier finden Sie Informationen über die SearchMailboxes EWS Vorgang.
ms.openlocfilehash: 141ea466a24f3cb400a8e0b63e2162c1eae5d7f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831296"
---
# <a name="searchmailboxes-operation"></a><span data-ttu-id="e1c5f-103">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1c5f-103">SearchMailboxes operation</span></span>

<span data-ttu-id="e1c5f-104">Hier finden Sie Informationen zum **SearchMailboxes** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-104">Find information about the **SearchMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="e1c5f-105">Der Vorgang **SearchMailboxes** durchsucht Postfächer nach Vorkommen von Ausdrücken in Postfachelemente.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-105">The **SearchMailboxes** operation searches mailboxes for occurrences of terms in mailbox items.</span></span> 
  
<span data-ttu-id="e1c5f-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-searchmailboxes-operation"></a><span data-ttu-id="e1c5f-107">Verwenden des SearchMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e1c5f-107">Using the SearchMailboxes operation</span></span>

<span data-ttu-id="e1c5f-108">Der Vorgang **SearchMailboxes** können viele gleichzeitige Suchabfragen Discovery-Suche auf mehrere Postfächer ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-108">The **SearchMailboxes** operation can use many simultaneous search queries to perform discovery search on multiple mailboxes.</span></span> <span data-ttu-id="e1c5f-109">Die Ergebnisse können entweder statistische Informationen über die Anzahl der Male Suchbegriffe auftreten oder eine Vorschau der Elemente, die die Suchbegriffe enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-109">The results can be either statistical information about the number of times search terms occur, or a preview of the items that contain the search terms.</span></span> 
  
### <a name="searchmailboxes-operation-soap-headers"></a><span data-ttu-id="e1c5f-110">SearchMailboxes Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="e1c5f-110">SearchMailboxes operation SOAP headers</span></span>

<span data-ttu-id="e1c5f-111">Der Vorgang **SearchMailboxes** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-111">The **SearchMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e1c5f-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="e1c5f-112">**Header name**</span></span>|<span data-ttu-id="e1c5f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1c5f-113">**Element**</span></span>|<span data-ttu-id="e1c5f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1c5f-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1c5f-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="e1c5f-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="e1c5f-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="e1c5f-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="e1c5f-117">Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="e1c5f-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e1c5f-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e1c5f-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e1c5f-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e1c5f-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e1c5f-121">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e1c5f-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e1c5f-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e1c5f-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e1c5f-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e1c5f-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e1c5f-125">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e1c5f-126">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a><span data-ttu-id="e1c5f-127">SearchMailboxes Vorgang-anforderungsbeispiel: Suchen Sie Postfächer für die Anzahl der Suche Begriff Treffer</span><span class="sxs-lookup"><span data-stu-id="e1c5f-127">SearchMailboxes operation request example: Search mailboxes for number of search term hits</span></span>

<span data-ttu-id="e1c5f-128">Im folgenden Beispiel wird eine **SearchMailboxes** Vorgang Anforderung veranschaulicht, wie mit zwei verschiedenen Abfragen gesucht drei verschiedene Postfächer für statistische Informationen zu wie oft, dass ein Begriff in jedem Postfach angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-128">The following example of a **SearchMailboxes** operation request shows how to use two different queries to search three different mailboxes for statistical information about how many times a term appears in each mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1c5f-129">In diesem Beispiel wird das [Query](query.md) -Element Intentionaly leer bleiben.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-129">In this example, the [Query](query.md) element is intentionaly left blank.</span></span> <span data-ttu-id="e1c5f-130">Wie eine erfolgreiche Anforderung fehlerbedingungen auf enthalten kann, wird eine Suche pro Postfach.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-130">This shows how a successful request can contain error conditions on a per mailbox search basis.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="e1c5f-131">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e1c5f-131">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e1c5f-132">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="e1c5f-132">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="e1c5f-133">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="e1c5f-133">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="e1c5f-134">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="e1c5f-134">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="e1c5f-135">Query</span><span class="sxs-lookup"><span data-stu-id="e1c5f-135">Query</span></span>](query.md)
    
- [<span data-ttu-id="e1c5f-136">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="e1c5f-136">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="e1c5f-137">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="e1c5f-137">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="e1c5f-138">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-138">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e1c5f-139">SearchScope</span><span class="sxs-lookup"><span data-stu-id="e1c5f-139">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="e1c5f-140">ResultType-Wert</span><span class="sxs-lookup"><span data-stu-id="e1c5f-140">ResultType</span></span>](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a><span data-ttu-id="e1c5f-141">Erfolgreiche SearchMailboxes Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="e1c5f-141">Successful SearchMailboxes operation response</span></span>

<span data-ttu-id="e1c5f-142">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **SearchMailboxes** Vorgang Anforderung abzurufenden statistische Informationen über die Anzahl der Male, Suchbegriffe in die Ziel-Postfächer gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-142">The following example shows a successful response to a **SearchMailboxes** operation request to get statistical information about the number of times search terms are found in the target mailboxes.</span></span> <span data-ttu-id="e1c5f-143">Die letzte Abfrage enthält ein leeres **Abfrage** -Element, das eine fehlerhaften postfachsuche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-143">The last query contains an empty **Query** element, which shows a failed mailbox search.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e1c5f-144">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e1c5f-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e1c5f-145">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e1c5f-145">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="e1c5f-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e1c5f-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e1c5f-147">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e1c5f-147">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="e1c5f-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e1c5f-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e1c5f-149">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="e1c5f-149">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="e1c5f-150">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="e1c5f-150">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="e1c5f-151">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="e1c5f-151">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="e1c5f-152">Query</span><span class="sxs-lookup"><span data-stu-id="e1c5f-152">Query</span></span>](query.md)
    
- [<span data-ttu-id="e1c5f-153">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="e1c5f-153">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="e1c5f-154">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="e1c5f-154">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="e1c5f-155">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-155">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e1c5f-156">SearchScope</span><span class="sxs-lookup"><span data-stu-id="e1c5f-156">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="e1c5f-157">ResultType-Wert</span><span class="sxs-lookup"><span data-stu-id="e1c5f-157">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="e1c5f-158">ItemCount</span><span class="sxs-lookup"><span data-stu-id="e1c5f-158">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="e1c5f-159">Größe (Long)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-159">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="e1c5f-160">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="e1c5f-160">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="e1c5f-161">KeywordStats</span><span class="sxs-lookup"><span data-stu-id="e1c5f-161">KeywordStats</span></span>](keywordstats.md)
    
- [<span data-ttu-id="e1c5f-162">KeywordStat</span><span class="sxs-lookup"><span data-stu-id="e1c5f-162">KeywordStat</span></span>](keywordstat.md)
    
- [<span data-ttu-id="e1c5f-163">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e1c5f-163">Keyword</span></span>](keyword.md)
    
- [<span data-ttu-id="e1c5f-164">ItemHits</span><span class="sxs-lookup"><span data-stu-id="e1c5f-164">ItemHits</span></span>](itemhits.md)
    
- [<span data-ttu-id="e1c5f-165">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="e1c5f-165">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="e1c5f-166">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="e1c5f-166">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="e1c5f-167">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-167">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e1c5f-168">ErrorCode (Int)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-168">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="e1c5f-169">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="e1c5f-169">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="e1c5f-170">IsArchive</span><span class="sxs-lookup"><span data-stu-id="e1c5f-170">IsArchive</span></span>](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a><span data-ttu-id="e1c5f-171">SearchMailboxes Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="e1c5f-171">SearchMailboxes operation error response</span></span>

<span data-ttu-id="e1c5f-172">Das folgende Beispiel zeigt eine Fehlerantwort an eine **SearchMailboxes** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-172">The following example shows an error response to a **SearchMailboxes** operation request.</span></span> <span data-ttu-id="e1c5f-173">Dies ist eine Antwort auf eine Anforderung zum Durchsuchen eines Postfachs, wenn die Postfach-ID falsch ist.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-173">This is a response to a request to search a mailbox when the mailbox identifier is incorrect.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e1c5f-174">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e1c5f-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e1c5f-175">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e1c5f-175">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="e1c5f-176">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e1c5f-176">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e1c5f-177">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e1c5f-177">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="e1c5f-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e1c5f-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e1c5f-179">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="e1c5f-179">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="e1c5f-180">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="e1c5f-180">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="e1c5f-181">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="e1c5f-181">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="e1c5f-182">Query</span><span class="sxs-lookup"><span data-stu-id="e1c5f-182">Query</span></span>](query.md)
    
- [<span data-ttu-id="e1c5f-183">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="e1c5f-183">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="e1c5f-184">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="e1c5f-184">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="e1c5f-185">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-185">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e1c5f-186">SearchScope</span><span class="sxs-lookup"><span data-stu-id="e1c5f-186">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="e1c5f-187">ResultType-Wert</span><span class="sxs-lookup"><span data-stu-id="e1c5f-187">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="e1c5f-188">ItemCount</span><span class="sxs-lookup"><span data-stu-id="e1c5f-188">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="e1c5f-189">Größe (Long)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-189">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="e1c5f-190">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="e1c5f-190">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="e1c5f-191">PageItemSize</span><span class="sxs-lookup"><span data-stu-id="e1c5f-191">PageItemSize</span></span>](pageitemsize.md)
    
- [<span data-ttu-id="e1c5f-192">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="e1c5f-192">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="e1c5f-193">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="e1c5f-193">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="e1c5f-194">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-194">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e1c5f-195">ErrorCode (Int)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-195">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="e1c5f-196">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="e1c5f-196">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="e1c5f-197">IsArchive</span><span class="sxs-lookup"><span data-stu-id="e1c5f-197">IsArchive</span></span>](isarchive.md)
    
<span data-ttu-id="e1c5f-198">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="e1c5f-198">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1c5f-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1c5f-199">See also</span></span>

- [<span data-ttu-id="e1c5f-200">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="e1c5f-200">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e1c5f-201">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1c5f-201">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="e1c5f-202">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1c5f-202">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e1c5f-203">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1c5f-203">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e1c5f-204">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1c5f-204">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="e1c5f-205">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1c5f-205">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="e1c5f-206">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1c5f-206">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

