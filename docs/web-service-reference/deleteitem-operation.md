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
ms.openlocfilehash: f068e08ef0d0f590c9ed8274f77d4dae9f942995
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526935"
---
# <a name="deleteitem-operation"></a><span data-ttu-id="d7f6f-103">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="d7f6f-103">DeleteItem operation</span></span>

<span data-ttu-id="d7f6f-104">Über den **DeleteItem**-Vorgang können Elemente im Exchange-Speicher gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-104">The **DeleteItem** operation deletes items in the Exchange store.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d7f6f-p101">Für einen **DeleteItem**-Vorgang wird eine Fehlerantwort inklusive des ErrorCannotDeleteObject-Fehlercodes zurückgegeben, wenn ein Stellvertreter versucht, ein Element im Postfach eines Prinzipals zu löschen, indem er für DisposalType MoveToDeletedItems festlegt. Zum Löschen eines Elements durch Verschieben in den Ordner „Gelöschte Elemente" muss ein Stellvertreter die [MoveItem Operation](moveitem-operation.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-p101">An error response that includes the ErrorCannotDeleteObject error code will be returned for a **DeleteItem** operation when a delegate tries to delete an item in the principal's mailbox by setting the DisposalType to MoveToDeletedItems. To delete an item by moving it to the Deleted Items folder, a delegate must use the [MoveItem operation](moveitem-operation.md).</span></span> 
  
## <a name="deleteitem-request-example"></a><span data-ttu-id="d7f6f-107">DeleteItem-Anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="d7f6f-107">DeleteItem request example</span></span>

### <a name="description"></a><span data-ttu-id="d7f6f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7f6f-108">Description</span></span>

<span data-ttu-id="d7f6f-109">Im folgenden Beispiel einer **DeleteItem**-Anforderung wird veranschaulicht, wie ein Element endgültig aus einem Postfach gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-109">The following example of a **DeleteItem** request shows how to perform a hard delete of an item from a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d7f6f-110">Die Element-ID wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-110">The item ID has been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d7f6f-111">Code</span><span class="sxs-lookup"><span data-stu-id="d7f6f-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="d7f6f-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="d7f6f-112">Request elements</span></span>

<span data-ttu-id="d7f6f-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="d7f6f-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d7f6f-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="d7f6f-114">DeleteItem</span></span>](deleteitem.md)
    
- [<span data-ttu-id="d7f6f-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d7f6f-115">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="d7f6f-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="d7f6f-116">ItemId</span></span>](itemid.md)
    
<span data-ttu-id="d7f6f-p102">Um weitere Optionen für die Anforderungsnachricht des **DeleteItem**-Vorgangs zu finden, sehen Sie sich die Schemahierarchie an. Beginnen Sie beim [DeleteItem](deleteitem.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-p102">To find other options for the request message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItem](deleteitem.md) element.</span></span> 
  
## <a name="successful-deleteitem-response"></a><span data-ttu-id="d7f6f-119">Erfolgreiche DeleteItem-Antwort</span><span class="sxs-lookup"><span data-stu-id="d7f6f-119">Successful DeleteItem response</span></span>

### <a name="description"></a><span data-ttu-id="d7f6f-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7f6f-120">Description</span></span>

<span data-ttu-id="d7f6f-121">Im folgenden Beispiel wird eine erfolgreiche Antwort auf eine **DeleteItem**-Anforderung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-121">The following example shows a successful response to the **DeleteItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d7f6f-122">Code</span><span class="sxs-lookup"><span data-stu-id="d7f6f-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="d7f6f-123">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="d7f6f-123">Successful response elements</span></span>

<span data-ttu-id="d7f6f-124">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="d7f6f-124">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d7f6f-125">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d7f6f-125">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d7f6f-126">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="d7f6f-126">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="d7f6f-127">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d7f6f-127">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d7f6f-128">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d7f6f-128">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="d7f6f-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d7f6f-129">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="d7f6f-p103">Um weitere Optionen für die Antwortnachricht des **DeleteItem**-Vorgangs zu finden, sehen Sie sich die Schemahierarchie an. Beginnen Sie beim [DeleteItemResponse](deleteitemresponse.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-p103">To find other options for the response message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="deleteitem-error-response"></a><span data-ttu-id="d7f6f-132">DeleteItem-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="d7f6f-132">DeleteItem error response</span></span>

### <a name="description"></a><span data-ttu-id="d7f6f-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7f6f-133">Description</span></span>

<span data-ttu-id="d7f6f-p104">Im folgenden Beispiel wird eine Fehlerantwort auf eine **DeleteItem**-Anforderung veranschaulicht. Der Fehler wurde ausgegeben, da der Vorgang versucht hat, ein Element zu löschen, das im Exchange-Speicher nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-p104">The following example shows an error response to a **DeleteItem** request. The error was created because the operation tried to delete an item that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d7f6f-136">Code</span><span class="sxs-lookup"><span data-stu-id="d7f6f-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="d7f6f-137">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="d7f6f-137">Error response elements</span></span>

<span data-ttu-id="d7f6f-138">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="d7f6f-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="d7f6f-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d7f6f-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d7f6f-140">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="d7f6f-140">DeleteItemResponse</span></span>](deleteitemresponse.md)
    
- [<span data-ttu-id="d7f6f-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d7f6f-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d7f6f-142">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d7f6f-142">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
    
- [<span data-ttu-id="d7f6f-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="d7f6f-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d7f6f-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d7f6f-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d7f6f-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d7f6f-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="d7f6f-p105">Andere Optionen für die Fehlerantwortnachricht des **DeleteItem**-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie beim [DeleteItemResponse](deleteitemresponse.md)-Element.</span><span class="sxs-lookup"><span data-stu-id="d7f6f-p105">To find other options for the error response message of the **DeleteItem** operation, explore the schema hierarchy. Start at the [DeleteItemResponse](deleteitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7f6f-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7f6f-148">See also</span></span>

- [<span data-ttu-id="d7f6f-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d7f6f-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="d7f6f-150">Löschen von Kontakten</span><span class="sxs-lookup"><span data-stu-id="d7f6f-150">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [<span data-ttu-id="d7f6f-151">Deleting E-mail Messages</span><span class="sxs-lookup"><span data-stu-id="d7f6f-151">Deleting E-mail Messages</span></span>](https://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [<span data-ttu-id="d7f6f-152">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="d7f6f-152">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

