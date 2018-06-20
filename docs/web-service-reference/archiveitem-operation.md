---
title: ArchiveItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1af216b3-13ea-498e-b4fc-23513755d731
description: Hier finden Sie Informationen über die ArchiveItem EWS Vorgang.
ms.openlocfilehash: 954943acefef8da61e92de5f8857ca023ca4fc9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757375"
---
# <a name="archiveitem-operation"></a><span data-ttu-id="45db8-103">ArchiveItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="45db8-103">ArchiveItem operation</span></span>

<span data-ttu-id="45db8-104">Hier finden Sie Informationen zum **ArchiveItem** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="45db8-104">Find information about the **ArchiveItem** EWS operation.</span></span> 
  
<span data-ttu-id="45db8-105">Der Vorgang **ArchiveItem** verschiebt ein Element in den Postfachbenutzer Archivpostfach.</span><span class="sxs-lookup"><span data-stu-id="45db8-105">The **ArchiveItem** operation moves an item into the mailbox user's archive mailbox.</span></span> 
  
<span data-ttu-id="45db8-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="45db8-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-archiveitem-operation"></a><span data-ttu-id="45db8-107">Verwenden des ArchiveItem-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="45db8-107">Using the ArchiveItem operation</span></span>

<span data-ttu-id="45db8-108">Der Vorgang **ArchiveItem** akzeptiert zwei Argumente in der Anforderung, die die Elemente in das Archivpostfach und den Zielordner für diese Elemente wechseln zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="45db8-108">The **ArchiveItem** operation takes two arguments in the request that identify the items to move to the archive mailbox and the destination folder for those items.</span></span> <span data-ttu-id="45db8-109">Ein Archivpostfach muss in der Reihenfolge für diesen Vorgang funktioniert aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="45db8-109">An archive mailbox must be enabled in order for this operation to work.</span></span> <span data-ttu-id="45db8-110">Informationen zum Aktivieren eines archivpostfachs finden Sie unter [Verwalten von Compliance-Archive](http://technet.microsoft.com/en-us/library/jj651146.aspx).</span><span class="sxs-lookup"><span data-stu-id="45db8-110">For information about how to enable an archive mailbox, see [Manage In-Place Archives](http://technet.microsoft.com/en-us/library/jj651146.aspx).</span></span>
  
### <a name="archiveitem-operation-soap-headers"></a><span data-ttu-id="45db8-111">ArchiveItem Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="45db8-111">ArchiveItem operation SOAP headers</span></span>

<span data-ttu-id="45db8-112">Der Vorgang **ArchiveItem** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="45db8-112">The **ArchiveItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="45db8-113">**Headername**</span><span class="sxs-lookup"><span data-stu-id="45db8-113">**Header name**</span></span>|<span data-ttu-id="45db8-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="45db8-114">**Element**</span></span>|<span data-ttu-id="45db8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45db8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45db8-116">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="45db8-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="45db8-117">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="45db8-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="45db8-118">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="45db8-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="45db8-119">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="45db8-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="45db8-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="45db8-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="45db8-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="45db8-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="45db8-122">Bezeichnet die Kultur gemäß Definition in RFC 3066, **Tags für die Identifizierung der Sprachen**, Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45db8-122">Identifies the culture, as defined in RFC 3066, **Tags for the Identification of Languages**, to be used to access the mailbox.</span></span> <span data-ttu-id="45db8-123">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="45db8-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="45db8-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="45db8-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="45db8-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="45db8-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="45db8-126">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="45db8-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="45db8-127">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="45db8-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="45db8-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="45db8-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="45db8-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="45db8-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="45db8-130">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="45db8-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="45db8-131">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="45db8-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="archiveitem-operation-request-example-move-an-item-to-the-archive-inbox-folder"></a><span data-ttu-id="45db8-132">ArchiveItem Vorgang-anforderungsbeispiel: Verschieben eines Elements in den Posteingang Archivordner</span><span class="sxs-lookup"><span data-stu-id="45db8-132">ArchiveItem operation request example: Move an item to the archive inbox folder</span></span>

<span data-ttu-id="45db8-133">Im folgenden Beispiel wird ein **ArchiveItem** Vorgang Anforderung veranschaulicht, wie ein Element in das Archiv Ordner Posteingang zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="45db8-133">The following example of an **ArchiveItem** operation request shows how to move an item to the archive Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="45db8-134">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="45db8-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:ArchiveItem>
         <m:ArchiveSourceFolderId>
            <t:DistinguishedFolderId Id="inbox"/>
         </m:ArchiveSourceFolderId>
         <m:ItemIds>
            <t:ItemId Id="AQMkG5BBwrQAAAxoAAAA=" ChangeKey="CQAAAHCtAAAAAAB7"/>
         </m:ItemIds>
      </m:ArchiveItem>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="45db8-135">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="45db8-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="45db8-136">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="45db8-136">ArchiveItem</span></span>](archiveitem.md)    
- [<span data-ttu-id="45db8-137">ArchiveSourceFolderId</span><span class="sxs-lookup"><span data-stu-id="45db8-137">ArchiveSourceFolderId</span></span>](archivesourcefolderid.md)    
- [<span data-ttu-id="45db8-138">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="45db8-138">DistinguishedFolderId</span></span>](distinguishedfolderid.md)    
- [<span data-ttu-id="45db8-139">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="45db8-139">ItemIds</span></span>](itemids.md)   
- [<span data-ttu-id="45db8-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="45db8-140">ItemId</span></span>](itemid.md)
    
## <a name="successful-archiveitem-operation-response"></a><span data-ttu-id="45db8-141">Erfolgreiche ArchiveItem Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="45db8-141">Successful ArchiveItem operation response</span></span>

<span data-ttu-id="45db8-142">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **ArchiveItem** Vorgang, um ein Element in ein Archivpostfach verschieben.</span><span class="sxs-lookup"><span data-stu-id="45db8-142">The following example shows a successful response to an **ArchiveItem** operation request to move an item to an archive mailbox.</span></span> 
  
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
      <m:ArchiveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="45db8-143">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="45db8-143">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="45db8-144">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="45db8-144">ArchiveItemResponse</span></span>](archiveitemresponse.md)    
- [<span data-ttu-id="45db8-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="45db8-145">ResponseMessages</span></span>](responsemessages.md)   
- [<span data-ttu-id="45db8-146">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="45db8-146">ArchiveItemResponseMessage</span></span>](archiveitemresponsemessage.md)    
- [<span data-ttu-id="45db8-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="45db8-147">ResponseCode</span></span>](responsecode.md)    
- [<span data-ttu-id="45db8-148">Elemente</span><span class="sxs-lookup"><span data-stu-id="45db8-148">Items</span></span>](items.md)
    
## <a name="archiveitem-operation-error-response"></a><span data-ttu-id="45db8-149">ArchiveItem Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="45db8-149">ArchiveItem operation error response</span></span>

<span data-ttu-id="45db8-150">Das folgende Beispiel zeigt eine Fehlerantwort an eine **ArchiveItem** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="45db8-150">The following example shows an error response to an **ArchiveItem** operation request.</span></span> <span data-ttu-id="45db8-151">Dies ist eine Antwort auf eine gültige Anforderung ein Elements archiviert, wenn ein Archivpostfach nicht für einen Benutzer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="45db8-151">This is a response to a valid request to archive an item when an archive mailbox is not enabled for a user.</span></span> 
  
```xml
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
      <m:ArchiveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Error">
               <m:MessageText>Archive mailbox is not enabled for this user.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="45db8-152">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="45db8-152">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="45db8-153">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="45db8-153">ArchiveItemResponse</span></span>](archiveitemresponse.md)    
- [<span data-ttu-id="45db8-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="45db8-154">ResponseMessages</span></span>](responsemessages.md)    
- [<span data-ttu-id="45db8-155">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="45db8-155">ArchiveItemResponseMessage</span></span>](archiveitemresponsemessage.md)    
- [<span data-ttu-id="45db8-156">MessageText</span><span class="sxs-lookup"><span data-stu-id="45db8-156">MessageText</span></span>](messagetext.md)    
- [<span data-ttu-id="45db8-157">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="45db8-157">ResponseCode</span></span>](responsecode.md)    
- [<span data-ttu-id="45db8-158">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="45db8-158">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)    
- [<span data-ttu-id="45db8-159">Elemente</span><span class="sxs-lookup"><span data-stu-id="45db8-159">Items</span></span>](items.md)
    
<span data-ttu-id="45db8-160">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="45db8-160">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45db8-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45db8-161">See also</span></span>

- [<span data-ttu-id="45db8-162">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="45db8-162">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md) 
- [<span data-ttu-id="45db8-163">Archivierung in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="45db8-163">Archiving in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/78ae179b-ae4f-4f64-911a-e0c70e0fa314%28Office.15%29.aspx)
    

