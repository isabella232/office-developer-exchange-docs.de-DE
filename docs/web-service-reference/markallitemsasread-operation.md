---
title: MarkAllItemsAsRead-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: Hier finden Sie Informationen über die MarkAllItemsAsRead EWS Vorgang.
ms.openlocfilehash: 995a6219f0a3b41bddb0d65c875d981322e1ce78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830354"
---
# <a name="markallitemsasread-operation"></a><span data-ttu-id="c8de7-103">MarkAllItemsAsRead-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c8de7-103">MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="c8de7-104">Hier finden Sie Informationen zum **MarkAllItemsAsRead** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c8de7-104">Find information about the **MarkAllItemsAsRead** EWS operation.</span></span> 
  
<span data-ttu-id="c8de7-105">Der Vorgang **MarkAllItemsAsRead** die [IsRead](isread.md) -Eigenschaft für alle Elemente, in einen oder mehrere Ordner, um anzugeben, dass alle Elemente entweder gelesen oder ungelesen werden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c8de7-105">The **MarkAllItemsAsRead** operation sets the [IsRead](isread.md) property on all items, in one or more folders, to indicate that all items are either read or unread.</span></span> 
  
<span data-ttu-id="c8de7-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c8de7-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markallitemsasread-operation"></a><span data-ttu-id="c8de7-107">Verwenden des MarkAllItemsAsRead-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="c8de7-107">Using the MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="c8de7-108">**MarkAllItemsAsRead** -Vorgang kann für alle Elemente in Ordnern, die durch die Exchange-Webdienste (EWS) Ordner-ID oder der Name des Standardordners Exchange identifiziert die [IsRead](isread.md) -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c8de7-108">The **MarkAllItemsAsRead** operation can set the [IsRead](isread.md) property on all items in folders identified by either the Exchange Web Services (EWS) folder identifier or the default Exchange folder name.</span></span> <span data-ttu-id="c8de7-109">Der Vorgang **MarkAllItemsAsRead** kann auch unterdrücken, das Senden von lesebestätigungen für Elemente, die als gelesen markiert.</span><span class="sxs-lookup"><span data-stu-id="c8de7-109">The **MarkAllItemsAsRead** operation can also suppress the sending of read receipts for items marked as read.</span></span> 
  
### <a name="markallitemsasread-operation-soap-headers"></a><span data-ttu-id="c8de7-110">MarkAllItemsAsRead Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="c8de7-110">MarkAllItemsAsRead operation SOAP headers</span></span>

<span data-ttu-id="c8de7-111">Der Vorgang **MarkAllItemsAsRead** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="c8de7-111">The **MarkAllItemsAsRead** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c8de7-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="c8de7-112">**Header name**</span></span>|<span data-ttu-id="c8de7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8de7-113">**Element**</span></span>|<span data-ttu-id="c8de7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8de7-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8de7-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="c8de7-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c8de7-116">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="c8de7-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c8de7-117">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="c8de7-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c8de7-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c8de7-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c8de7-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c8de7-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c8de7-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c8de7-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c8de7-121">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8de7-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="c8de7-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c8de7-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c8de7-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c8de7-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c8de7-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c8de7-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c8de7-125">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c8de7-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c8de7-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c8de7-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c8de7-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c8de7-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c8de7-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c8de7-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c8de7-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c8de7-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c8de7-130">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="c8de7-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a><span data-ttu-id="c8de7-131">MarkAllItemsAsRead Vorgang-anforderungsbeispiel: alle Elemente in einem Ordner als gelesen markieren</span><span class="sxs-lookup"><span data-stu-id="c8de7-131">MarkAllItemsAsRead operation request example: Mark all items in a folder as read</span></span>

<span data-ttu-id="c8de7-132">Im folgenden Beispiel wird eine **MarkAllItemsAsRead** Vorgang Anforderung veranschaulicht, die [IsRead](isread.md) -Eigenschaft, die auch das Lese-Flag bezeichnet wird, auf **"true"** für alle Elemente in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="c8de7-132">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property, which is also called the read flag, to **true** on all items in a folder.</span></span> <span data-ttu-id="c8de7-133">Dieses Beispiel zeigt auch, dass das Read, Empfangsbestätigungen nicht als Reaktion auf Anfragen lesebestätigung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8de7-133">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c8de7-134">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8de7-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="c8de7-135">Ändern von Schlüsseln sind nicht für diesen Vorgang erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8de7-135">Change keys are not required for this operation.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>true</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c8de7-136">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c8de7-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c8de7-137">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="c8de7-137">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="c8de7-138">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="c8de7-138">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="c8de7-139">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="c8de7-139">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="c8de7-140">FolderIds</span><span class="sxs-lookup"><span data-stu-id="c8de7-140">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="c8de7-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="c8de7-141">FolderId</span></span>](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a><span data-ttu-id="c8de7-142">Erfolgreiche MarkAllItemsAsRead Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="c8de7-142">Successful MarkAllItemsAsRead operation response</span></span>

<span data-ttu-id="c8de7-143">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **MarkAllItemsAsRead** Vorgang, markieren Sie alle Elemente in einem Ordner als gelesen.</span><span class="sxs-lookup"><span data-stu-id="c8de7-143">The following example shows a successful response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="c8de7-144">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c8de7-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c8de7-145">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="c8de7-145">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="c8de7-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c8de7-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c8de7-147">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c8de7-147">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="c8de7-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c8de7-148">ResponseCode</span></span>](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a><span data-ttu-id="c8de7-149">MarkAllItemsAsRead Vorgang-anforderungsbeispiel: alle Elemente in einem Ordner als ungelesen markieren</span><span class="sxs-lookup"><span data-stu-id="c8de7-149">MarkAllItemsAsRead operation request example: Mark all items in a folder as unread</span></span>

<span data-ttu-id="c8de7-150">Im folgenden Beispiel wird eine **MarkAllItemsAsRead** Vorgang Anforderung veranschaulicht die [IsRead](isread.md) -Eigenschaft für alle Elemente in einem Ordner auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c8de7-150">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property to **false** on all items in a folder.</span></span> <span data-ttu-id="c8de7-151">Dieses Beispiel zeigt auch, dass das Read, Empfangsbestätigungen nicht als Reaktion auf Anfragen lesebestätigung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8de7-151">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>false</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c8de7-152">Eine erfolgreiche Antwort auf eine Anforderung an alle Elemente als gelesen markiert ist identisch mit der Antwort auf eine Anforderung an alle Elemente als ungelesen markiert.</span><span class="sxs-lookup"><span data-stu-id="c8de7-152">A successful response to a request to mark all items as read is the same as the response to a request to mark all items as unread.</span></span>
  
<span data-ttu-id="c8de7-153">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c8de7-153">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c8de7-154">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="c8de7-154">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="c8de7-155">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="c8de7-155">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="c8de7-156">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="c8de7-156">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="c8de7-157">FolderIds</span><span class="sxs-lookup"><span data-stu-id="c8de7-157">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="c8de7-158">FolderId</span><span class="sxs-lookup"><span data-stu-id="c8de7-158">FolderId</span></span>](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a><span data-ttu-id="c8de7-159">MarkAllItemsAsRead Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="c8de7-159">MarkAllItemsAsRead operation error response</span></span>

<span data-ttu-id="c8de7-160">Das folgende Beispiel zeigt eine Fehlerantwort an eine **MarkAllItemsAsRead** Operation-Anforderung an alle Elemente in einem Ordner als gelesen oder ungelesen markieren, wenn der Ordner im Postfach nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c8de7-160">The following example shows an error response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read or unread when the folder does not exist in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Error">
               <m:MessageText>The specified object was not found in the store.</m:MessageText>
               <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="c8de7-161">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c8de7-161">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c8de7-162">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="c8de7-162">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="c8de7-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c8de7-163">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c8de7-164">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c8de7-164">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="c8de7-165">MessageText</span><span class="sxs-lookup"><span data-stu-id="c8de7-165">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c8de7-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c8de7-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c8de7-167">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c8de7-167">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="c8de7-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8de7-168">See also</span></span>

- [<span data-ttu-id="c8de7-169">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="c8de7-169">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="c8de7-170">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="c8de7-170">FindFolder operation</span></span>](findfolder-operation.md)
    

