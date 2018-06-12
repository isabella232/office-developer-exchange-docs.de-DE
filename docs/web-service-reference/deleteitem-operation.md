---
title: DeleteItem-Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 3e26c416-fa12-476e-bfd2-5c1f4bb7b348
description: Über den DeleteItem-Vorgang können Elemente im Exchange-Speicher gelöscht werden.
ms.openlocfilehash: 87d7853daa5db0cd87b3f6469c228a584b4d9caf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757927"
---
# <a name="deleteitem-operation"></a><span data-ttu-id="8be24-103">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="8be24-103">DeleteItem operation</span></span>

<span data-ttu-id="8be24-104">Über den **DeleteItem**-Vorgang können Elemente im Exchange-Speicher gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8be24-104">The **DeleteItem** operation deletes items in the Exchange store.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8be24-p101">[!HINWEIS] Für einen **DeleteItem**-Vorgang wird eine Fehlerantwort inklusive des ErrorCannotDeleteObject-Fehlercodes zurückgegeben, wenn ein Stellvertreter versucht, ein Element im Postfach eines Prinzipals zu löschen, indem er für DisposalType MoveToDeletedItems festlegt. Zum Löschen eines Elements durch Verschieben in den Ordner „Gelöschte Elemente" muss ein Stellvertreter die [MoveItem Operation](moveitem-operation.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="8be24-p101">An error response that includes the ErrorCannotDeleteObject error code will be returned for a **DeleteItem** operation when a delegate tries to delete an item in the principal's mailbox by setting the DisposalType to MoveToDeletedItems. To delete an item by moving it to the Deleted Items folder, a delegate must use the [MoveItem operation](moveitem-operation.md).</span></span> 
  
## <a name="deleteitem-request-example"></a><span data-ttu-id="8be24-107">DeleteItem anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="8be24-107">DeleteItem request example</span></span>

### <a name="description"></a><span data-ttu-id="8be24-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8be24-108">Description</span></span>

<span data-ttu-id="8be24-109">Im folgenden Beispiel einer **DeleteItem**-Anforderung wird veranschaulicht, wie ein Element endgültig aus einem Postfach gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="8be24-109">The following example of a **DeleteItem** request shows how to perform a hard delete of an item from a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8be24-110">[!HINWEIS] Die Element-ID wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="8be24-110">The item ID has been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8be24-111">Code</span><span class="sxs-lookup"><span data-stu-id="8be24-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="8be24-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="8be24-112">Request elements</span></span>

<span data-ttu-id="8be24-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="8be24-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="8be24-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="8be24-114">DeleteItem</span></span>](deleteitem.md)
    
- [<span data-ttu-id="8be24-115">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="8be24-115">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="8be24-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="8be24-116">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="8be24-p102">Zum Suchen nach Optionen für die Antwortnachricht des **DeleteItem**-Vorgangs können Sie die Schemahierarchie durchsuchen. Beginnen Sie bei dem [DeleteItem](deleteitem.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="8be24-p102">To find other options for the request message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItem](deleteitem.md) element.</span></span> 
  
## <a name="successful-deleteitem-response"></a><span data-ttu-id="8be24-119">Erfolgreiche DeleteItem Antwort</span><span class="sxs-lookup"><span data-stu-id="8be24-119">Successful DeleteItem response</span></span>

### <a name="description"></a><span data-ttu-id="8be24-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8be24-120">Description</span></span>

<span data-ttu-id="8be24-121">Im folgenden Beispiel wird eine erfolgreiche Antwort auf eine **DeleteItem**-Anforderung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8be24-121">The following example shows a successful response to the **DeleteItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8be24-122">Code</span><span class="sxs-lookup"><span data-stu-id="8be24-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="8be24-123">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="8be24-123">Successful response elements</span></span>

<span data-ttu-id="8be24-124">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="8be24-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8be24-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8be24-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8be24-126">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="8be24-126">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="8be24-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8be24-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8be24-128">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8be24-128">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="8be24-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8be24-129">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="8be24-p103">Andere Optionen für die Antwortnachricht des **DeleteItem**-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie beim [DeleteItemResponse](deleteitemresponse.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="8be24-p103">To find other options for the response message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="deleteitem-error-response"></a><span data-ttu-id="8be24-132">DeleteItem Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="8be24-132">DeleteItem error response</span></span>

### <a name="description"></a><span data-ttu-id="8be24-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8be24-133">Description</span></span>

<span data-ttu-id="8be24-p104">Im folgenden Beispiel wird eine Fehlerantwort auf eine **DeleteItem**-Anforderung veranschaulicht. Der Fehler wurde ausgegeben, da der Vorgang versucht hat, ein Element zu löschen, das im Exchange-Speicher nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="8be24-p104">The following example shows an error response to a **DeleteItem** request. The error was created because the operation tried to delete an item that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8be24-136">Code</span><span class="sxs-lookup"><span data-stu-id="8be24-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="8be24-137">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="8be24-137">Error response elements</span></span>

<span data-ttu-id="8be24-138">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="8be24-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="8be24-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8be24-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8be24-140">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="8be24-140">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="8be24-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8be24-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8be24-142">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8be24-142">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="8be24-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="8be24-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8be24-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8be24-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8be24-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8be24-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="8be24-p105">Andere Optionen für die Fehlerantwortnachricht des **DeleteItem**-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie beim [DeleteItemResponse](deleteitemresponse.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="8be24-p105">To find other options for the error response message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8be24-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8be24-148">See also</span></span>

- [<span data-ttu-id="8be24-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8be24-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8be24-150">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="8be24-150">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [<span data-ttu-id="8be24-151">Deleting E-mail Messages</span><span class="sxs-lookup"><span data-stu-id="8be24-151">Deleting E-mail Messages</span></span>](http://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [<span data-ttu-id="8be24-152">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="8be24-152">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)
