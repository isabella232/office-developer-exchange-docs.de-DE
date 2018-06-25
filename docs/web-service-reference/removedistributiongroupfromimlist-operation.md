---
title: RemoveDistributionGroupFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: Hier finden Sie Informationen über die RemoveDistributionGroupFromImList EWS Vorgang.
ms.openlocfilehash: 9999f98a5698dd33c22e22fdf86bd00a2d053b52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831096"
---
# <a name="removedistributiongroupfromimlist-operation"></a><span data-ttu-id="9e640-103">RemoveDistributionGroupFromImList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9e640-103">RemoveDistributionGroupFromImList operation</span></span>

<span data-ttu-id="9e640-104">Hier finden Sie Informationen zum **RemoveDistributionGroupFromImList** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9e640-104">Find information about the **RemoveDistributionGroupFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="9e640-105">**RemoveDistributionGroupFromImList** -Vorgang entfernt eine Verteilergruppe aus der Liste für die Lync-Sofortnachrichten (IM), wenn Lync Exchange, um den Kontaktspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e640-105">The **RemoveDistributionGroupFromImList** operation removes a distribution group from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="9e640-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9e640-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a><span data-ttu-id="9e640-107">Verwenden des RemoveDistributionGroupFromImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="9e640-107">Using the RemoveDistributionGroupFromImList operation</span></span>

<span data-ttu-id="9e640-108">Der **RemoveDistributionGroupFromImList** -Vorgang akzeptiert ein einzelnes Argument, das eine Verteilergruppe zu entfernen aus der Lync im-, die auf einem Exchange-Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9e640-108">The **RemoveDistributionGroupFromImList** operation accepts a single argument that identifies a distribution group to remove from the Lync IM list stored on an Exchange server.</span></span> 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a><span data-ttu-id="9e640-109">RemoveDistributionGroupFromImList Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="9e640-109">RemoveDistributionGroupFromImList operation SOAP headers</span></span>

<span data-ttu-id="9e640-110">Der Vorgang **RemoveDistributionGroupFromImList** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="9e640-110">The **RemoveDistributionGroupFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="9e640-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="9e640-111">**Header name**</span></span>|<span data-ttu-id="9e640-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e640-112">**Element**</span></span>|<span data-ttu-id="9e640-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e640-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e640-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="9e640-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="9e640-115">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="9e640-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="9e640-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="9e640-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="9e640-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9e640-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9e640-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="9e640-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="9e640-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="9e640-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="9e640-120">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e640-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="9e640-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9e640-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9e640-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="9e640-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="9e640-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="9e640-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="9e640-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="9e640-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="9e640-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9e640-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9e640-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="9e640-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="9e640-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9e640-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="9e640-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="9e640-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="9e640-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="9e640-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a><span data-ttu-id="9e640-130">RemoveDistributionGroupFromImList Vorgang-anforderungsbeispiel: entfernen eine Verteilergruppe aus einer Liste von Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="9e640-130">RemoveDistributionGroupFromImList operation request example: Remove a distribution group from an IM list</span></span>

<span data-ttu-id="9e640-131">Im folgenden Beispiel wird eine **RemoveDistributionGroupFromImList** Vorgang Anforderung veranschaulicht, wie eine Verteilergruppe aus einer Instant Messaging-Gruppe zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9e640-131">The following example of a **RemoveDistributionGroupFromImList** operation request shows how to remove a distribution group from an IM group.</span></span> <span data-ttu-id="9e640-132">Der **RemoveDistributionGroupFromImList** -Vorgang akzeptiert den Bezeichner eindeutige Gruppe, um die Verteilergruppe aus der Liste Sofortnachrichten entfernen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9e640-132">The **RemoveDistributionGroupFromImList** operation accepts the unique group identifier to identify the distribution group to remove from the IM list.</span></span> <span data-ttu-id="9e640-133">Das [ExchangeStoreId](exchangestoreid.md) -Element, das in der Antwort, für den [Vorgang GetImItemList](getimitemlist-operation.md) und den [AddDistributionGroupToImList Vorgang zurückgegeben wird](adddistributiongrouptoimlist-operation.md) identifiziert Verteilergruppen, die aus der Liste Sofortnachrichten entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="9e640-133">The [ExchangeStoreId](exchangestoreid.md) element that is returned in the response for the [GetImItemList operation](getimitemlist-operation.md) and the [AddDistributionGroupToImList operation](adddistributiongrouptoimlist-operation.md) identifies distribution groups that can be removed from the IM list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9e640-134">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9e640-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveDistributionGroupFromImList>
         <m:GroupId Id="AAMkADEzO4QrAABmEh5oAAA="/>
      </m:RemoveDistributionGroupFromImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="9e640-135">Die folgenden Elemente werden in der Anforderung SOAP-Body verwendet:</span><span class="sxs-lookup"><span data-stu-id="9e640-135">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="9e640-136">RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="9e640-136">RemoveDistributionGroupFromImList</span></span>](removedistributiongroupfromimlist.md)
    
- [<span data-ttu-id="9e640-137">GroupId</span><span class="sxs-lookup"><span data-stu-id="9e640-137">GroupId</span></span>](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a><span data-ttu-id="9e640-138">Erfolgreiche RemoveDistributionGroupFromImList Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="9e640-138">Successful RemoveDistributionGroupFromImList operation response</span></span>

<span data-ttu-id="9e640-139">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **RemoveDistributionGroupFromImList** -Vorgang zu einer Entfernen einer Verteilergruppe aus einer Gruppe von Instant Messaging.</span><span class="sxs-lookup"><span data-stu-id="9e640-139">The following example shows a successful response to a **RemoveDistributionGroupFromImList** operation request to a remove a distribution group from an IM group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="9e640-140">Die folgenden Elemente werden in der Antwort SOAP-Body verwendet:</span><span class="sxs-lookup"><span data-stu-id="9e640-140">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="9e640-141">RemoveDistributionGroupFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="9e640-141">RemoveDistributionGroupFromImListResponse</span></span>](removedistributiongroupfromimlistresponse.md)
    
- [<span data-ttu-id="9e640-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9e640-142">ResponseCode</span></span>](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a><span data-ttu-id="9e640-143">RemoveDistributionGroupFromImList Vorgang Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="9e640-143">RemoveDistributionGroupFromImList operation error response example</span></span>

<span data-ttu-id="9e640-144">Das folgende Beispiel zeigt eine Fehlerantwort an eine **RemoveDistributionGroupFromImList** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9e640-144">The following example shows an error response to a **RemoveDistributionGroupFromImList** operation request.</span></span> <span data-ttu-id="9e640-145">Dies ist eine Antwort auf eine Anforderung an eine Verteilergruppe zu entfernen, die bereits aus dem Postfach entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="9e640-145">This is a response to a request to remove a distribution group that has already been removed from the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="9e640-146">Die folgenden Elemente werden in die SOAP-Body-Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="9e640-146">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="9e640-147">RemoveDistributionGroupFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="9e640-147">RemoveDistributionGroupFromImListResponse</span></span>](removedistributiongroupfromimlistresponse.md)
    
- [<span data-ttu-id="9e640-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="9e640-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="9e640-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9e640-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9e640-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9e640-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="9e640-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e640-151">See also</span></span>

- [<span data-ttu-id="9e640-152">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e640-152">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="9e640-153">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9e640-153">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="9e640-154">AddDistributionGroupToImList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9e640-154">AddDistributionGroupToImList operation</span></span>](adddistributiongrouptoimlist-operation.md)
    
- [<span data-ttu-id="9e640-155">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e640-155">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

