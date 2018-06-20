---
title: MoveFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: c7233966-6c87-4a14-8156-b1610760176d
description: MoveFolder-Vorgang Ordner aus einem angegebenen Ordner verschoben und in einem anderen Ordner verschoben.
ms.openlocfilehash: 5da6929f11ce9ba74db190db6d799f25974d2192
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830490"
---
# <a name="movefolder-operation"></a><span data-ttu-id="71524-103">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="71524-103">MoveFolder operation</span></span>

<span data-ttu-id="71524-104">MoveFolder-Vorgang Ordner aus einem angegebenen Ordner verschoben und in einem anderen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="71524-104">The MoveFolder operation moves folders from a specified folder and puts them in another folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71524-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="71524-105">Remarks</span></span>

<span data-ttu-id="71524-106">MoveFolder-Vorgang ähnelt der CopyFolder-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="71524-106">The MoveFolder operation is similar to the CopyFolder operation.</span></span> <span data-ttu-id="71524-107">Sie können nicht definierten Ordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="71524-107">You cannot move distinguished folders.</span></span> <span data-ttu-id="71524-108">Sie können gleichzeitig mehrere Ordner in den Zielordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="71524-108">You can move multiple folders at one time to the destination folder.</span></span>
  
## <a name="movefolder-request-example"></a><span data-ttu-id="71524-109">MoveFolder-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="71524-109">MoveFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="71524-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71524-110">Description</span></span>

<span data-ttu-id="71524-111">Im folgenden Beispiel wird eine Anforderung MoveFolder bilden eine Anforderung zum Verschieben eines Ordners durch die [FolderId](folderid.md) identifiziert, und legen den Ordner im Ordner "Junk-e-Mail definierten" veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="71524-111">The following example of a MoveFolder request shows how to form a request to move a folder identified by the [FolderId](folderid.md) and put the folder in the Junk E-mail distinguished folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="71524-112">Code</span><span class="sxs-lookup"><span data-stu-id="71524-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="junkemail"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AScAc"/>
      </FolderIds>
    </MoveFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="71524-113">Kommentare</span><span class="sxs-lookup"><span data-stu-id="71524-113">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="71524-114">Der Wert des ID-Attributs des Elements [FolderId](folderid.md) wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="71524-114">The value of the ID attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="71524-115">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="71524-115">Request elements</span></span>

<span data-ttu-id="71524-116">Diese MoveFolder-Anforderung enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="71524-116">This MoveFolder request includes the following elements:</span></span>
  
- [<span data-ttu-id="71524-117">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="71524-117">MoveFolder</span></span>](movefolder.md)
    
- [<span data-ttu-id="71524-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="71524-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="71524-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="71524-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="71524-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="71524-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="71524-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="71524-121">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="71524-122">Finden Sie im Schema für weitere Elemente, die Sie verwenden können, um eine Anforderung MoveFolder bilden.</span><span class="sxs-lookup"><span data-stu-id="71524-122">See the schema for additional elements that you can use to form a MoveFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="71524-123">Der Standardspeicherort des Schemas ist in das virtuelle EWS-Verzeichnis auf dem Computer, der die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="71524-123">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="successful-movefolder-response-example"></a><span data-ttu-id="71524-124">Erfolgreiche MoveFolder-Antwort-Beispiel</span><span class="sxs-lookup"><span data-stu-id="71524-124">Successful MoveFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="71524-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71524-125">Description</span></span>

<span data-ttu-id="71524-126">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung MoveFolder.</span><span class="sxs-lookup"><span data-stu-id="71524-126">The following example shows a successful response to the MoveFolder request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="71524-127">Code</span><span class="sxs-lookup"><span data-stu-id="71524-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFV" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="71524-128">Kommentare</span><span class="sxs-lookup"><span data-stu-id="71524-128">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="71524-129">Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="71524-129">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="71524-130">Die FolderId, die in der Antwort zurückgegeben wird steht für den Ordner, die wurde verschoben zu den neuen Speicherort des Ordners.</span><span class="sxs-lookup"><span data-stu-id="71524-130">The FolderId that is returned in the response represents the folder that was moved to the new the folder location.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="71524-131">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="71524-131">Response elements</span></span>

<span data-ttu-id="71524-132">Die Antwort MoveFolder umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="71524-132">The MoveFolder response includes the following elements:</span></span>
  
- [<span data-ttu-id="71524-133">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="71524-133">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="71524-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="71524-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="71524-135">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="71524-135">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="71524-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="71524-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="71524-137">Ordner</span><span class="sxs-lookup"><span data-stu-id="71524-137">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="71524-138">Folder</span><span class="sxs-lookup"><span data-stu-id="71524-138">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="71524-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="71524-139">FolderId</span></span>](folderid.md)
    
## <a name="movefolder-error-response-example"></a><span data-ttu-id="71524-140">MoveFolder-Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="71524-140">MoveFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="71524-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71524-141">Description</span></span>

<span data-ttu-id="71524-142">Das folgende Beispiel zeigt eine Fehlerantwort an, die auftritt, wenn Sie versuchen, einen definierten Ordner zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="71524-142">The following example shows an error response that occurs when you try to move a distinguished folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="71524-143">Code</span><span class="sxs-lookup"><span data-stu-id="71524-143">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot move distinguished folder.</m:MessageText>
          <m:ResponseCode>ErrorMoveDistinguishedFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="71524-144">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="71524-144">Error response elements</span></span>

<span data-ttu-id="71524-145">MoveFolder-Fehlerantwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="71524-145">The MoveFolder error response includes the following elements:</span></span>
  
- [<span data-ttu-id="71524-146">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="71524-146">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="71524-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="71524-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="71524-148">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="71524-148">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="71524-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="71524-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="71524-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="71524-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="71524-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="71524-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="71524-152">Ordner</span><span class="sxs-lookup"><span data-stu-id="71524-152">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="71524-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71524-153">See also</span></span>



[<span data-ttu-id="71524-154">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="71524-154">CopyFolder operation</span></span>](copyfolder-operation.md)

