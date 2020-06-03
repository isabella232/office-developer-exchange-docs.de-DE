---
title: MarkAllItemsAsRead-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: Hier finden Sie Informationen zum MarkAllItemsAsRead-EWS-Vorgang.
ms.openlocfilehash: aeeacea1cd5eed723f93027dd1ef75b34605fdfd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530530"
---
# <a name="markallitemsasread-operation"></a><span data-ttu-id="4f241-103">MarkAllItemsAsRead-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4f241-103">MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="4f241-104">Hier finden Sie Informationen zum **MarkAllItemsAsRead** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4f241-104">Find information about the **MarkAllItemsAsRead** EWS operation.</span></span> 
  
<span data-ttu-id="4f241-105">Mit dem **MarkAllItemsAsRead** -Vorgang wird die [isread](isread.md) -Eigenschaft für alle Elemente in einem oder mehreren Ordnern festgelegt, um anzugeben, dass alle Elemente entweder gelesen oder ungelesen sind.</span><span class="sxs-lookup"><span data-stu-id="4f241-105">The **MarkAllItemsAsRead** operation sets the [IsRead](isread.md) property on all items, in one or more folders, to indicate that all items are either read or unread.</span></span> 
  
<span data-ttu-id="4f241-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4f241-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markallitemsasread-operation"></a><span data-ttu-id="4f241-107">Verwenden des MarkAllItemsAsRead-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="4f241-107">Using the MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="4f241-108">Mit dem **MarkAllItemsAsRead** -Vorgang kann die [isread](isread.md) -Eigenschaft für alle Elemente in Ordnern festgelegt werden, die entweder durch die Exchange-Webdienste Ordner-ID oder den Namen des Exchange-Standardordners identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4f241-108">The **MarkAllItemsAsRead** operation can set the [IsRead](isread.md) property on all items in folders identified by either the Exchange Web Services (EWS) folder identifier or the default Exchange folder name.</span></span> <span data-ttu-id="4f241-109">Der **MarkAllItemsAsRead** -Vorgang kann auch das Senden von Lesebestätigungen für Elemente unterdrücken, die als gelesen markiert sind.</span><span class="sxs-lookup"><span data-stu-id="4f241-109">The **MarkAllItemsAsRead** operation can also suppress the sending of read receipts for items marked as read.</span></span> 
  
### <a name="markallitemsasread-operation-soap-headers"></a><span data-ttu-id="4f241-110">SOAP-Header des MarkAllItemsAsRead-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="4f241-110">MarkAllItemsAsRead operation SOAP headers</span></span>

<span data-ttu-id="4f241-111">Der **MarkAllItemsAsRead** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4f241-111">The **MarkAllItemsAsRead** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="4f241-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="4f241-112">**Header name**</span></span>|<span data-ttu-id="4f241-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f241-113">**Element**</span></span>|<span data-ttu-id="4f241-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f241-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f241-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="4f241-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="4f241-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="4f241-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="4f241-117">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="4f241-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="4f241-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4f241-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4f241-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="4f241-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="4f241-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="4f241-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="4f241-121">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4f241-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="4f241-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4f241-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4f241-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="4f241-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="4f241-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4f241-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4f241-125">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="4f241-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="4f241-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4f241-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4f241-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="4f241-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="4f241-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4f241-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4f241-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="4f241-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="4f241-130">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="4f241-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a><span data-ttu-id="4f241-131">MarkAllItemsAsRead-Vorgangs Anforderungs Beispiel: Markieren aller Elemente in einem Ordner als gelesen</span><span class="sxs-lookup"><span data-stu-id="4f241-131">MarkAllItemsAsRead operation request example: Mark all items in a folder as read</span></span>

<span data-ttu-id="4f241-132">Im folgenden Beispiel einer **MarkAllItemsAsRead** -Vorgangsanforderung wird gezeigt, wie die [isread](isread.md) -Eigenschaft, die auch als Lese-Flag bezeichnet wird, auf **true** für alle Elemente in einem Ordner festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4f241-132">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property, which is also called the read flag, to **true** on all items in a folder.</span></span> <span data-ttu-id="4f241-133">In diesem Beispiel wird außerdem gezeigt, dass Lesebestätigungen nicht als Reaktion auf Lese Bestätigungsanforderungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f241-133">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4f241-134">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4f241-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="4f241-135">Für diesen Vorgang sind keine Änderungsschlüssel erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f241-135">Change keys are not required for this operation.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="4f241-136">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="4f241-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4f241-137">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="4f241-137">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="4f241-138">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="4f241-138">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="4f241-139">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="4f241-139">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="4f241-140">FolderIds</span><span class="sxs-lookup"><span data-stu-id="4f241-140">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="4f241-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="4f241-141">FolderId</span></span>](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a><span data-ttu-id="4f241-142">Erfolgreiche Reaktion des MarkAllItemsAsRead-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="4f241-142">Successful MarkAllItemsAsRead operation response</span></span>

<span data-ttu-id="4f241-143">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MarkAllItemsAsRead** -Vorgangsanforderung, um alle Elemente in einem Ordner als gelesen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="4f241-143">The following example shows a successful response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="4f241-144">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="4f241-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4f241-145">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="4f241-145">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="4f241-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4f241-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="4f241-147">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4f241-147">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="4f241-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4f241-148">ResponseCode</span></span>](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a><span data-ttu-id="4f241-149">MarkAllItemsAsRead-Vorgangs Anforderungs Beispiel: Markieren aller Elemente in einem Ordner als ungelesen</span><span class="sxs-lookup"><span data-stu-id="4f241-149">MarkAllItemsAsRead operation request example: Mark all items in a folder as unread</span></span>

<span data-ttu-id="4f241-150">Im folgenden Beispiel einer **MarkAllItemsAsRead** -Vorgangsanforderung wird gezeigt, wie die [isread](isread.md) -Eigenschaft für alle Elemente in einem Ordner auf **false** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4f241-150">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property to **false** on all items in a folder.</span></span> <span data-ttu-id="4f241-151">In diesem Beispiel wird außerdem gezeigt, dass Lesebestätigungen nicht als Reaktion auf Lese Bestätigungsanforderungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f241-151">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="4f241-152">Eine erfolgreiche Antwort auf eine Anforderung zum Markieren aller Elemente als gelesen entspricht der Antwort auf eine Anforderung, alle Elemente als ungelesen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="4f241-152">A successful response to a request to mark all items as read is the same as the response to a request to mark all items as unread.</span></span>
  
<span data-ttu-id="4f241-153">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="4f241-153">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4f241-154">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="4f241-154">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="4f241-155">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="4f241-155">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="4f241-156">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="4f241-156">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="4f241-157">FolderIds</span><span class="sxs-lookup"><span data-stu-id="4f241-157">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="4f241-158">FolderId</span><span class="sxs-lookup"><span data-stu-id="4f241-158">FolderId</span></span>](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a><span data-ttu-id="4f241-159">Fehlerantwort des MarkAllItemsAsRead-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="4f241-159">MarkAllItemsAsRead operation error response</span></span>

<span data-ttu-id="4f241-160">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **MarkAllItemsAsRead** -Vorgangsanforderung, um alle Elemente in einem Ordner als gelesen oder ungelesen zu markieren, wenn der Ordner nicht im Postfach vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4f241-160">The following example shows an error response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read or unread when the folder does not exist in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="4f241-161">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="4f241-161">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4f241-162">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="4f241-162">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="4f241-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4f241-163">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="4f241-164">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4f241-164">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="4f241-165">MessageText</span><span class="sxs-lookup"><span data-stu-id="4f241-165">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="4f241-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4f241-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4f241-167">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4f241-167">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="4f241-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f241-168">See also</span></span>

- [<span data-ttu-id="4f241-169">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f241-169">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="4f241-170">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4f241-170">FindFolder operation</span></span>](findfolder-operation.md)
    

