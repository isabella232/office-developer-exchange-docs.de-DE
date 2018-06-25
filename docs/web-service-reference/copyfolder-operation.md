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
description: CopyFolder-Vorgang kopiert Ordner in einem Postfach.
ms.openlocfilehash: a83444ff0927a3c8fe075c79d44d02357a737773
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757719"
---
# <a name="copyfolder-operation"></a><span data-ttu-id="a0a93-103">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0a93-103">CopyFolder operation</span></span>

<span data-ttu-id="a0a93-104">CopyFolder-Vorgang kopiert Ordner in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="a0a93-104">The CopyFolder operation copies folders in a mailbox.</span></span>
  
## <a name="using-the-copyfolder-operation"></a><span data-ttu-id="a0a93-105">Verwenden des CopyFolder-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="a0a93-105">Using the CopyFolder operation</span></span>

<span data-ttu-id="a0a93-106">Der Vorgang CopyFolder ähnelt der [MoveFolder-Vorgang](movefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a0a93-106">The CopyFolder operation is similar to the [MoveFolder operation](movefolder-operation.md).</span></span> <span data-ttu-id="a0a93-107">Kopiert die angegebene Ordnern und gibt die **Id** und **ChangeKey** der kopierten Ordner.</span><span class="sxs-lookup"><span data-stu-id="a0a93-107">It copies identified folders and returns the **Id** and **ChangeKey** of the copied folders.</span></span> 
  
## <a name="copyfolder-request-example"></a><span data-ttu-id="a0a93-108">CopyFolder-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="a0a93-108">CopyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="a0a93-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0a93-109">Description</span></span>

<span data-ttu-id="a0a93-110">Im folgenden Beispiel wird eine Anforderung CopyFolder veranschaulicht, wie Ordner in den Ordner Posteingang zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="a0a93-110">The following example of a CopyFolder request shows how to copy folders into the Inbox folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a0a93-111">Der Wert des **Id** -Attributs des Elements [FolderId](folderid.md) wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="a0a93-111">The value of the **Id** attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a0a93-112">Code</span><span class="sxs-lookup"><span data-stu-id="a0a93-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="a0a93-113">Kommentare</span><span class="sxs-lookup"><span data-stu-id="a0a93-113">Comments</span></span>

<span data-ttu-id="a0a93-114">Ordner können durch das [DistinguishedFolderId](distinguishedfolderid.md) -Element oder das [FolderId](folderid.md) -Element für die Verwendung in entweder die [ToFolderId](tofolderid.md) oder die [FolderIds](folderids.md) Elemente identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a0a93-114">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in either the [ToFolderId](tofolderid.md) or the [FolderIds](folderids.md) elements.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="a0a93-115">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="a0a93-115">Request elements</span></span>

<span data-ttu-id="a0a93-116">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="a0a93-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a0a93-117">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="a0a93-117">CopyFolder</span></span>](copyfolder.md)
    
- [<span data-ttu-id="a0a93-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="a0a93-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="a0a93-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a0a93-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="a0a93-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="a0a93-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="a0a93-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="a0a93-121">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="a0a93-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a0a93-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="a0a93-123">Wenn andere Optionen für die Anforderungsnachricht des Vorgangs CopyFolder suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="a0a93-123">To find other options for the request message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a0a93-124">Starten Sie das [CopyFolder](copyfolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a0a93-124">Start at the [CopyFolder](copyfolder.md) element.</span></span> 
  
## <a name="successful-copyfolder-response"></a><span data-ttu-id="a0a93-125">Erfolgreiche CopyFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="a0a93-125">Successful CopyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="a0a93-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0a93-126">Description</span></span>

<span data-ttu-id="a0a93-127">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="a0a93-127">The following example shows a successful response to the CopyFolder request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a0a93-128">Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0a93-128">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a0a93-129">Code</span><span class="sxs-lookup"><span data-stu-id="a0a93-129">Code</span></span>

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
    <CopyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="a0a93-130">Comment</span><span class="sxs-lookup"><span data-stu-id="a0a93-130">Comment</span></span>

<span data-ttu-id="a0a93-131">Das [FolderId](folderid.md) -Element, das in der Antwort zurückgegeben wird steht für den Ordner, der in den neuen Ordnerspeicherort kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a0a93-131">The [FolderId](folderid.md) element that is returned in the response represents the folder that was copied in the new folder location.</span></span> 
  
### <a name="response-elements"></a><span data-ttu-id="a0a93-132">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="a0a93-132">Response elements</span></span>

<span data-ttu-id="a0a93-133">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="a0a93-133">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a0a93-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a0a93-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a0a93-135">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a0a93-135">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="a0a93-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a0a93-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a0a93-137">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a0a93-137">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="a0a93-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a0a93-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a0a93-139">Ordner</span><span class="sxs-lookup"><span data-stu-id="a0a93-139">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a0a93-140">Folder</span><span class="sxs-lookup"><span data-stu-id="a0a93-140">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="a0a93-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="a0a93-141">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="a0a93-142">Wenn andere Optionen für die Antwortnachricht des Vorgangs CopyFolder suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="a0a93-142">To find other options for the response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a0a93-143">Starten Sie das [CopyFolderResponse](copyfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a0a93-143">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="copyfolder-error-response"></a><span data-ttu-id="a0a93-144">CopyFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="a0a93-144">CopyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="a0a93-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0a93-145">Description</span></span>

<span data-ttu-id="a0a93-146">Das folgende Beispiel zeigt eine Fehlerantwort an eine CopyFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a0a93-146">The following example shows an error response to a CopyFolder request.</span></span> <span data-ttu-id="a0a93-147">Der Fehler aufgetreten, weil ein Ordner mit dem gleichen Anzeigenamen bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a0a93-147">The error occurred because a folder with the same display name already exists.</span></span>
  
### <a name="code"></a><span data-ttu-id="a0a93-148">Code</span><span class="sxs-lookup"><span data-stu-id="a0a93-148">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="a0a93-149">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="a0a93-149">Error response elements</span></span>

<span data-ttu-id="a0a93-150">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="a0a93-150">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="a0a93-151">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a0a93-151">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="a0a93-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a0a93-152">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a0a93-153">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a0a93-153">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="a0a93-154">MessageText</span><span class="sxs-lookup"><span data-stu-id="a0a93-154">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a0a93-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a0a93-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a0a93-156">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a0a93-156">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="a0a93-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="a0a93-157">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="a0a93-158">Wenn andere Optionen für die Fehlermeldung Antwort des Vorgangs CopyFolder suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="a0a93-158">To find other options for the error response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a0a93-159">Starten Sie das [CopyFolderResponse](copyfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="a0a93-159">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0a93-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0a93-160">See also</span></span>

- [<span data-ttu-id="a0a93-161">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0a93-161">MoveFolder operation</span></span>](movefolder-operation.md)
- [<span data-ttu-id="a0a93-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a0a93-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

