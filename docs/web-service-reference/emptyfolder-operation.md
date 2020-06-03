---
title: EmptyFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98161486-e2f2-480f-8d5d-708ba81b208a
description: Der EmptyFolder-Vorgang leert Ordner in einem Postfach. Optional können Sie mit diesem Vorgang die Unterordner des angegebenen Ordners löschen. Wenn ein Unterordner gelöscht wird, werden der Unterordner und die Nachrichten innerhalb des Unterordners gelöscht.
ms.openlocfilehash: 1913db74d33f1e6750cd158df5870f257d0e7839
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530684"
---
# <a name="emptyfolder-operation"></a><span data-ttu-id="de842-105">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="de842-105">EmptyFolder operation</span></span>

<span data-ttu-id="de842-106">Der **EmptyFolder** -Vorgang leert Ordner in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="de842-106">The **EmptyFolder** operation empties folders in a mailbox.</span></span> <span data-ttu-id="de842-107">Optional können Sie mit diesem Vorgang die Unterordner des angegebenen Ordners löschen.</span><span class="sxs-lookup"><span data-stu-id="de842-107">Optionally, this operation enables you to delete the subfolders of the specified folder.</span></span> <span data-ttu-id="de842-108">Wenn ein Unterordner gelöscht wird, werden der Unterordner und die Nachrichten innerhalb des Unterordners gelöscht.</span><span class="sxs-lookup"><span data-stu-id="de842-108">When a subfolder is deleted, the subfolder and the messages within the subfolder are deleted.</span></span> 
  
## <a name="emptyfolder-request-example"></a><span data-ttu-id="de842-109">EmptyFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="de842-109">EmptyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="de842-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de842-110">Description</span></span>

<span data-ttu-id="de842-111">Im folgenden Beispiel einer **EmptyFolder** -Anforderung wird gezeigt, wie Sie eine Anforderung zum leeren eines Ordners bilden.</span><span class="sxs-lookup"><span data-stu-id="de842-111">This following example of an **EmptyFolder** request shows how to form a request to empty a folder.</span></span> <span data-ttu-id="de842-112">In diesem Beispiel werden alle Unterordner des angegebenen Ordners gelöscht.</span><span class="sxs-lookup"><span data-stu-id="de842-112">This example deletes all subfolders of the identified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="de842-113">Die Werte der ID-und der **ChangeKey** -Attribute des [Folder](folderid.md) **-ID** -Elements wurden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="de842-113">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="de842-114">Code</span><span class="sxs-lookup"><span data-stu-id="de842-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="de842-115">Comments</span><span class="sxs-lookup"><span data-stu-id="de842-115">Comments</span></span>

<span data-ttu-id="de842-116">In diesem Beispiel wird ein harter Löschvorgang für den Ordner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de842-116">This example performs a hard delete on the folder.</span></span>
  
<span data-ttu-id="de842-117">Ordner können entweder durch das [DistinguishedFolderId](distinguishedfolderid.md) -Element oder das [Folder](folderid.md) -Element für die Verwendung im [FolderIds](folderids.md) -Element identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="de842-117">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in the [FolderIds](folderids.md) element.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="de842-118">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="de842-118">Request elements</span></span>

<span data-ttu-id="de842-119">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="de842-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="de842-120">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="de842-120">EmptyFolder</span></span>](emptyfolder.md)
    
- [<span data-ttu-id="de842-121">FolderIds</span><span class="sxs-lookup"><span data-stu-id="de842-121">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="de842-122">FolderId</span><span class="sxs-lookup"><span data-stu-id="de842-122">FolderId</span></span>](folderid.md)
    
## <a name="successful-emptyfolder-response"></a><span data-ttu-id="de842-123">Erfolgreiche EmptyFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="de842-123">Successful EmptyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="de842-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de842-124">Description</span></span>

<span data-ttu-id="de842-125">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **EmptyFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="de842-125">The following example shows a successful response to the **EmptyFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="de842-126">Code</span><span class="sxs-lookup"><span data-stu-id="de842-126">Code</span></span>

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
    <m:EmptyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:EmptyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:EmptyFolderResponseMessage>
      </m:ResponseMessages>
    </m:EmptyFolderResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="de842-127">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="de842-127">Successful response elements</span></span>

<span data-ttu-id="de842-128">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="de842-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="de842-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="de842-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="de842-130">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="de842-130">EmptyFolderResponse</span></span>](emptyfolderresponse.md)
    
- [<span data-ttu-id="de842-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="de842-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="de842-132">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="de842-132">EmptyFolderResponseMessage</span></span>](emptyfolderresponsemessage.md)
    
- [<span data-ttu-id="de842-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="de842-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="emptyfolder-error-response"></a><span data-ttu-id="de842-134">EmptyFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="de842-134">EmptyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="de842-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de842-135">Description</span></span>

<span data-ttu-id="de842-136">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **EmptyFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="de842-136">The following example shows an error response to an **Emptyfolder** request.</span></span> <span data-ttu-id="de842-137">Der Fehler wurde erstellt, da der Vorgang versucht hat, einen Ordner zu leeren, der nicht im Exchange-Informationsspeicher gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="de842-137">The error was created because the operation tried to empty a folder that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="de842-138">Code</span><span class="sxs-lookup"><span data-stu-id="de842-138">Code</span></span>

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
            xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse 
          xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="error-response-elements"></a><span data-ttu-id="de842-139">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="de842-139">Error response elements</span></span>

<span data-ttu-id="de842-140">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="de842-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="de842-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="de842-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="de842-142">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="de842-142">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="de842-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="de842-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="de842-144">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="de842-144">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="de842-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="de842-145">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="de842-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="de842-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="de842-147">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="de842-147">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="de842-148">Ordner</span><span class="sxs-lookup"><span data-stu-id="de842-148">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="de842-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de842-149">See also</span></span>

- [<span data-ttu-id="de842-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="de842-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

