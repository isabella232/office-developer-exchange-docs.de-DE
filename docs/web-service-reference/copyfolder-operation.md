---
title: CopyFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: c7ea0d68-9793-4144-b378-d99536776db9
description: Der CopyFolder-Vorgang kopiert Ordner in einem Postfach.
ms.openlocfilehash: 1f9a7a3f3ede2d3cf8f9d41677d8ce0487266f17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468894"
---
# <a name="copyfolder-operation"></a><span data-ttu-id="25659-103">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="25659-103">CopyFolder operation</span></span>

<span data-ttu-id="25659-104">Der CopyFolder-Vorgang kopiert Ordner in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="25659-104">The CopyFolder operation copies folders in a mailbox.</span></span>
  
## <a name="using-the-copyfolder-operation"></a><span data-ttu-id="25659-105">Verwenden des CopyFolder-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="25659-105">Using the CopyFolder operation</span></span>

<span data-ttu-id="25659-106">Der CopyFolder-Vorgang ähnelt dem [MoveFolder-Vorgang](movefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="25659-106">The CopyFolder operation is similar to the [MoveFolder operation](movefolder-operation.md).</span></span> <span data-ttu-id="25659-107">Er kopiert identifizierte Ordner und gibt die **ID** -und **ChangeKey** der kopierten Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="25659-107">It copies identified folders and returns the **Id** and **ChangeKey** of the copied folders.</span></span> 
  
## <a name="copyfolder-request-example"></a><span data-ttu-id="25659-108">CopyFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="25659-108">CopyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="25659-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25659-109">Description</span></span>

<span data-ttu-id="25659-110">Im folgenden Beispiel einer CopyFolder-Anforderung wird gezeigt, wie Ordner in den Ordner Posteingang kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="25659-110">The following example of a CopyFolder request shows how to copy folders into the Inbox folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="25659-111">Der Wert des ID-Attributs des [Folder](folderid.md) **-ID-** Elements wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="25659-111">The value of the **Id** attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="25659-112">Code</span><span class="sxs-lookup"><span data-stu-id="25659-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AS4A=" ChangeKey="fsVU4=="/>
        <t:FolderId Id="AS4AU=" ChangeKey="fsVU4o=="/>
      </FolderIds>
    </CopyFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="25659-113">Comments</span><span class="sxs-lookup"><span data-stu-id="25659-113">Comments</span></span>

<span data-ttu-id="25659-114">Ordner können entweder durch das [DistinguishedFolderId](distinguishedfolderid.md) -Element oder das [Folder](folderid.md) -Element für die Verwendung in den [tofolder](tofolderid.md) -oder [FolderIds](folderids.md) -Elementen identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="25659-114">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in either the [ToFolderId](tofolderid.md) or the [FolderIds](folderids.md) elements.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="25659-115">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="25659-115">Request elements</span></span>

<span data-ttu-id="25659-116">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="25659-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="25659-117">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="25659-117">CopyFolder</span></span>](copyfolder.md)
    
- [<span data-ttu-id="25659-118">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="25659-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="25659-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="25659-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="25659-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="25659-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="25659-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="25659-121">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="25659-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="25659-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="25659-123">Um andere Optionen für die Anforderungsnachricht des CopyFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="25659-123">To find other options for the request message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="25659-124">Beginnen Sie mit dem [CopyFolder](copyfolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="25659-124">Start at the [CopyFolder](copyfolder.md) element.</span></span> 
  
## <a name="successful-copyfolder-response"></a><span data-ttu-id="25659-125">Erfolgreiche CopyFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="25659-125">Successful CopyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="25659-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25659-126">Description</span></span>

<span data-ttu-id="25659-127">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CopyFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="25659-127">The following example shows a successful response to the CopyFolder request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="25659-128">Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="25659-128">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="25659-129">Code</span><span class="sxs-lookup"><span data-stu-id="25659-129">Code</span></span>

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
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn=" ChangeKey="fsVU4o==" />
            </t:Folder>
          </m:Folders>
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="25659-130">Kommentar</span><span class="sxs-lookup"><span data-stu-id="25659-130">Comment</span></span>

<span data-ttu-id="25659-131">Das [folderin](folderid.md) -Element, das in der Antwort zurückgegeben wird, stellt den Ordner dar, der an den neuen Ordnerspeicherort kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="25659-131">The [FolderId](folderid.md) element that is returned in the response represents the folder that was copied in the new folder location.</span></span> 
  
### <a name="response-elements"></a><span data-ttu-id="25659-132">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="25659-132">Response elements</span></span>

<span data-ttu-id="25659-133">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="25659-133">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="25659-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="25659-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="25659-135">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="25659-135">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="25659-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="25659-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="25659-137">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="25659-137">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="25659-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="25659-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="25659-139">Ordner</span><span class="sxs-lookup"><span data-stu-id="25659-139">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="25659-140">Folder</span><span class="sxs-lookup"><span data-stu-id="25659-140">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="25659-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="25659-141">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="25659-142">Um andere Optionen für die Antwortnachricht des CopyFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="25659-142">To find other options for the response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="25659-143">Beginnen Sie mit dem [CopyFolderResponse](copyfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="25659-143">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="copyfolder-error-response"></a><span data-ttu-id="25659-144">CopyFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="25659-144">CopyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="25659-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25659-145">Description</span></span>

<span data-ttu-id="25659-146">Das folgende Beispiel zeigt eine Fehlerantwort auf eine CopyFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="25659-146">The following example shows an error response to a CopyFolder request.</span></span> <span data-ttu-id="25659-147">Der Fehler ist aufgetreten, da bereits ein Ordner mit dem gleichen Anzeigenamen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="25659-147">The error occurred because a folder with the same display name already exists.</span></span>
  
### <a name="code"></a><span data-ttu-id="25659-148">Code</span><span class="sxs-lookup"><span data-stu-id="25659-148">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The move or copy operation failed.</m:MessageText>
          <m:ResponseCode>ErrorMoveCopyFailed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="25659-149">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="25659-149">Error response elements</span></span>

<span data-ttu-id="25659-150">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="25659-150">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="25659-151">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="25659-151">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="25659-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="25659-152">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="25659-153">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="25659-153">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="25659-154">MessageText</span><span class="sxs-lookup"><span data-stu-id="25659-154">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="25659-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="25659-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="25659-156">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="25659-156">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="25659-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="25659-157">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="25659-158">Weitere Optionen für die Fehlerantwort Meldung des CopyFolder-Vorgangs finden Sie unter Durchsuchen der Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="25659-158">To find other options for the error response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="25659-159">Beginnen Sie mit dem [CopyFolderResponse](copyfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="25659-159">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25659-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25659-160">See also</span></span>

- [<span data-ttu-id="25659-161">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="25659-161">MoveFolder operation</span></span>](movefolder-operation.md)
- [<span data-ttu-id="25659-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="25659-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

