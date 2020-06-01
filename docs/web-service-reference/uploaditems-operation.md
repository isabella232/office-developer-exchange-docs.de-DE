---
title: UploadItems-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItems
api_type:
- schema
ms.assetid: a88cbe99-7968-454d-a545-4f92c330909f
description: Der UploadItems-Vorgang lädt einen Stream von Elementen in ein Exchange-Postfach hoch.
ms.openlocfilehash: 57e722c7775baa090736875077781cee869c3b01
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468502"
---
# <a name="uploaditems-operation"></a><span data-ttu-id="2f13c-103">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2f13c-103">UploadItems operation</span></span>

<span data-ttu-id="2f13c-104">Der **UploadItems** -Vorgang lädt einen Stream von Elementen in ein Exchange-Postfach hoch.</span><span class="sxs-lookup"><span data-stu-id="2f13c-104">The **UploadItems** operation uploads a stream of items into an Exchange mailbox.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2f13c-105">Der **UploadItems** -Vorgang ist in Microsoft Exchange Server 2010 Service Pack 1 (SP1) auf eine maximale Import Nutzlast von 25 MB erhöht Base64-codierter Daten beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2f13c-105">The **UploadItems** operation is restricted in MicrosoftExchange Server 2010 Service Pack 1 (SP1) to a maximum import payload of 25MB of base64 encoded data.</span></span> <span data-ttu-id="2f13c-106">Die Einstellung kann in der Datei "Internet. config" geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2f13c-106">The setting can be altered in the web.config file.</span></span> 
  
## <a name="uploaditems-request-example"></a><span data-ttu-id="2f13c-107">UploadItems-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="2f13c-107">UploadItems request example</span></span>

### <a name="description"></a><span data-ttu-id="2f13c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f13c-108">Description</span></span>

<span data-ttu-id="2f13c-109">Im folgenden Beispiel einer **UploadItems** -Anforderung wird gezeigt, wie zwei Elemente in ein Postfach hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="2f13c-109">The following example of an **UploadItems** request shows how to upload two items into a mailbox.</span></span> <span data-ttu-id="2f13c-110">Das erste Element ist ein neues Element.</span><span class="sxs-lookup"><span data-stu-id="2f13c-110">The first item is a new item.</span></span> <span data-ttu-id="2f13c-111">Das zweite Element ist eine aktualisierte Version eines vorhandenen Elements im Postfach.</span><span class="sxs-lookup"><span data-stu-id="2f13c-111">The second item is an updated version of an existing item in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2f13c-112">Code</span><span class="sxs-lookup"><span data-stu-id="2f13c-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UploadItems>
      <m:Items>
        <t:Item CreateAction="CreateNew">
          <t:ParentFolderId Id="AQMkADhhOGIgAAAA==" ChangeKey="AQAAAA=="/>
          <t:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAA
            AAAEYAJACABAAAAAYAAAABDqSAAAACAAAAcSMAAOSECEBbAAAAL089
            RklSU1QgT1JHQU5JWkFUSU9OL09VPUVYQ0hBTkdFIEFETUlOSVNUUk
            FUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJFQ0lQSUVO
            VFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAA
            ALACMAAAADACYAAAAAAAsAKQAAAAMALgAAAAAAAwA2AAAAAACwhw4=
          </t:Data>
        </t:Item>
        <t:Item CreateAction="Update">
          <t:ParentFolderId Id="AQMkADhhOGIgAAAB==" ChangeKey="AQAAAA=="/>
          <t:ItemId Id="AAMkADhhOGU0MGM7AAA=" ChangeKey="CQAAAA=="/>
          <t:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAA
            AAAEYAJACABAAAAAYAAAABDqSAAAACAAAANiAAAOSECEBbAAAAL089
            RklSU1QgT1JHQU5JWkFUSU9OL09VPUVYQ0hBTkdFIEFETUlOSVNUUk
            FUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJFQ0lQSUVO
            VFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAA
            ALACMAAAALACkAAAADADYAAAAAALCENwAyAAAASQBuAHQAZQByAGUA
            cwB0AGkAbgBnACAALQAgAGYAcgBvAG0AIABFAFcAUwBNAEEAAABAAD
            kAgJ2chyHuygECATsAZQAAAEVYOi9PPUZJUlNUIE9SR0FOSVpBVBMO
          </t:Data>
        </t:Item>
      </m:Items>
    </m:UploadItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2f13c-113">Comments</span><span class="sxs-lookup"><span data-stu-id="2f13c-113">Comments</span></span>

<span data-ttu-id="2f13c-114">Bezeichner und Elementdaten wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2f13c-114">Identifiers and the item data have been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="2f13c-115">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="2f13c-115">Request elements</span></span>

<span data-ttu-id="2f13c-116">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="2f13c-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="2f13c-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2f13c-117">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="2f13c-118">UploadItems</span><span class="sxs-lookup"><span data-stu-id="2f13c-118">UploadItems</span></span>](uploaditems.md)
    
- [<span data-ttu-id="2f13c-119">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="2f13c-119">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
    
- [<span data-ttu-id="2f13c-120">Element (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="2f13c-120">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
    
- [<span data-ttu-id="2f13c-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="2f13c-121">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="2f13c-122">Data (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="2f13c-122">Data (base64Binary)</span></span>](data-base64binary.md)
    
- [<span data-ttu-id="2f13c-123">ItemId</span><span class="sxs-lookup"><span data-stu-id="2f13c-123">ItemId</span></span>](itemid.md)
    
## <a name="successful-uploaditems-response-example"></a><span data-ttu-id="2f13c-124">Erfolgreiches UploadItems-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="2f13c-124">Successful UploadItems response example</span></span>

### <a name="description"></a><span data-ttu-id="2f13c-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f13c-125">Description</span></span>

<span data-ttu-id="2f13c-126">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **UploadItems** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2f13c-126">The following example shows a successful response to the **UploadItems** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2f13c-127">Code</span><span class="sxs-lookup"><span data-stu-id="2f13c-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
                         MinorVersion="1"
                         MajorBuildNumber="164"
                         MinorBuildNumber="0"
                         Version="Exchange2010_SP1"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UploadItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhUFZ/AAA=" ChangeKey="CQAAABYAAABsMBS3hrihS7voMf0GPIQeAAAAULQm"/>
        </m:UploadItemsResponseMessage>
        <m:UploadItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhOGZ7AAA=" ChangeKey="CQAAABYAAABsMBS3hrihS7voMf0GPIQeAAAAULQn"/>
        </m:UploadItemsResponseMessage>
      </m:ResponseMessages>
    </m:UploadItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2f13c-128">Comments</span><span class="sxs-lookup"><span data-stu-id="2f13c-128">Comments</span></span>

<span data-ttu-id="2f13c-129">Element-IDs wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2f13c-129">Item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="2f13c-130">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="2f13c-130">Response elements</span></span>

<span data-ttu-id="2f13c-131">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="2f13c-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="2f13c-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2f13c-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2f13c-133">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="2f13c-133">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="2f13c-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2f13c-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2f13c-135">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2f13c-135">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="2f13c-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2f13c-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2f13c-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="2f13c-137">ItemId</span></span>](itemid.md)
    
## <a name="uploaditems-error-response-example"></a><span data-ttu-id="2f13c-138">UploadItems-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="2f13c-138">UploadItems Error response example</span></span>

### <a name="description"></a><span data-ttu-id="2f13c-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f13c-139">Description</span></span>

<span data-ttu-id="2f13c-140">Das folgende Beispiel zeigt eine Antwort auf die **UploadItems** -Anforderung, die einen Fehler enthält, der durch einen Versuch verursacht wurde, ein Element zu aktualisieren, das im Postfach nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="2f13c-140">The following example shows a response to the **UploadItems** request that contains an error caused by an attempt to update an item that cannot be found in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2f13c-141">Code</span><span class="sxs-lookup"><span data-stu-id="2f13c-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UploadItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UploadItemsResponseMessage>
      </m:ResponseMessages>
    </m:UploadItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="2f13c-142">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="2f13c-142">Error response elements</span></span>

<span data-ttu-id="2f13c-143">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="2f13c-143">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="2f13c-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2f13c-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2f13c-145">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="2f13c-145">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="2f13c-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2f13c-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2f13c-147">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2f13c-147">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="2f13c-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="2f13c-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2f13c-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2f13c-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2f13c-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2f13c-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="2f13c-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f13c-151">See also</span></span>



[<span data-ttu-id="2f13c-152">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2f13c-152">ExportItems operation</span></span>](exportitems-operation.md)


[<span data-ttu-id="2f13c-153">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f13c-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="2f13c-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f13c-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

