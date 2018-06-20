---
title: EmptyFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98161486-e2f2-480f-8d5d-708ba81b208a
description: Der Vorgang EmptyFolder leert Ordner in einem Postfach. Optional können Sie können diesen Vorgang die Unterordnern des angegebenen Ordners zu löschen. Wenn ein Unterordner gelöscht wird, werden die Unterordner und die Nachrichten innerhalb der Unterordner gelöscht.
ms.openlocfilehash: 0192744516c5a6d24b95915452bfcffecc2d92b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758210"
---
# <a name="emptyfolder-operation"></a><span data-ttu-id="f6a64-105">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f6a64-105">EmptyFolder operation</span></span>

<span data-ttu-id="f6a64-106">Der Vorgang **EmptyFolder** leert Ordner in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="f6a64-106">The **EmptyFolder** operation empties folders in a mailbox.</span></span> <span data-ttu-id="f6a64-107">Optional können Sie können diesen Vorgang die Unterordnern des angegebenen Ordners zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f6a64-107">Optionally, this operation enables you to delete the subfolders of the specified folder.</span></span> <span data-ttu-id="f6a64-108">Wenn ein Unterordner gelöscht wird, werden die Unterordner und die Nachrichten innerhalb der Unterordner gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f6a64-108">When a subfolder is deleted, the subfolder and the messages within the subfolder are deleted.</span></span> 
  
## <a name="emptyfolder-request-example"></a><span data-ttu-id="f6a64-109">Beispiel für EmptyFolder-Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6a64-109">EmptyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="f6a64-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6a64-110">Description</span></span>

<span data-ttu-id="f6a64-111">Im folgenden Beispiel einer **EmptyFolder** -Anforderung veranschaulicht eine Anforderung an einen Ordner leeren bilden.</span><span class="sxs-lookup"><span data-stu-id="f6a64-111">This following example of an **EmptyFolder** request shows how to form a request to empty a folder.</span></span> <span data-ttu-id="f6a64-112">Dieses Beispiel löscht alle Unterordner des angegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="f6a64-112">This example deletes all subfolders of the identified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f6a64-113">Die Werte der **Id** und die **ChangeKey** Attribute des Elements [FolderId](folderid.md) wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="f6a64-113">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f6a64-114">Code</span><span class="sxs-lookup"><span data-stu-id="f6a64-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
    </soap:Header>
    <soap:Body>
      <m:EmptyFolder DeleteType="HardDelete" DeleteSubFolders="true">
        <m:FolderIds>
          <t:FolderId Id="AQMkADhhOGU0"  ChangeKey="AQAAABYAAABsMB" />
        </m:FolderIds>
      </m:EmptyFolder>
    </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="f6a64-115">Kommentare</span><span class="sxs-lookup"><span data-stu-id="f6a64-115">Comments</span></span>

<span data-ttu-id="f6a64-116">In diesem Beispiel werden ein harte löschen für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="f6a64-116">This example performs a hard delete on the folder.</span></span>
  
<span data-ttu-id="f6a64-117">Ordner können durch das [DistinguishedFolderId](distinguishedfolderid.md) -Element oder das [FolderId](folderid.md) -Element für die Verwendung im [FolderIds](folderids.md) -Element identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f6a64-117">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in the [FolderIds](folderids.md) element.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="f6a64-118">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="f6a64-118">Request elements</span></span>

<span data-ttu-id="f6a64-119">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="f6a64-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="f6a64-120">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="f6a64-120">EmptyFolder</span></span>](emptyfolder.md)
    
- [<span data-ttu-id="f6a64-121">FolderIds</span><span class="sxs-lookup"><span data-stu-id="f6a64-121">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="f6a64-122">FolderId</span><span class="sxs-lookup"><span data-stu-id="f6a64-122">FolderId</span></span>](folderid.md)
    
## <a name="successful-emptyfolder-response"></a><span data-ttu-id="f6a64-123">Erfolgreiche EmptyFolder Antwort</span><span class="sxs-lookup"><span data-stu-id="f6a64-123">Successful EmptyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="f6a64-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6a64-124">Description</span></span>

<span data-ttu-id="f6a64-125">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **EmptyFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f6a64-125">The following example shows a successful response to the **EmptyFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f6a64-126">Code</span><span class="sxs-lookup"><span data-stu-id="f6a64-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:EmptyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:EmptyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:EmptyFolderResponseMessage>
      </m:ResponseMessages>
    </m:EmptyFolderResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="f6a64-127">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="f6a64-127">Successful response elements</span></span>

<span data-ttu-id="f6a64-128">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="f6a64-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="f6a64-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f6a64-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="f6a64-130">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="f6a64-130">EmptyFolderResponse</span></span>](emptyfolderresponse.md)
    
- [<span data-ttu-id="f6a64-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f6a64-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f6a64-132">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f6a64-132">EmptyFolderResponseMessage</span></span>](emptyfolderresponsemessage.md)
    
- [<span data-ttu-id="f6a64-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f6a64-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="emptyfolder-error-response"></a><span data-ttu-id="f6a64-134">EmptyFolder Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="f6a64-134">EmptyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="f6a64-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6a64-135">Description</span></span>

<span data-ttu-id="f6a64-136">Das folgende Beispiel zeigt eine Fehlerantwort an **Emptyfolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f6a64-136">The following example shows an error response to an **Emptyfolder** request.</span></span> <span data-ttu-id="f6a64-137">Der Fehler erstellt wurde, da der Vorgang haben versucht, einen Ordner zu leeren, die nicht gefunden wurde im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="f6a64-137">The error was created because the operation tried to empty a folder that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="f6a64-138">Code</span><span class="sxs-lookup"><span data-stu-id="f6a64-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
            MinorVersion="1" 
            MajorBuildNumber="164" 
            MinorBuildNumber="0" 
            Version="Exchange2010_SP1" 
            xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse 
          xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="f6a64-139">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="f6a64-139">Error response elements</span></span>

<span data-ttu-id="f6a64-140">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="f6a64-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="f6a64-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f6a64-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="f6a64-142">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="f6a64-142">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="f6a64-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f6a64-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f6a64-144">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f6a64-144">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="f6a64-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="f6a64-145">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f6a64-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f6a64-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f6a64-147">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f6a64-147">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="f6a64-148">Ordner</span><span class="sxs-lookup"><span data-stu-id="f6a64-148">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="f6a64-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6a64-149">See also</span></span>

- [<span data-ttu-id="f6a64-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f6a64-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

