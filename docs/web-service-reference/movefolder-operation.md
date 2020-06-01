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
description: Der MoveFolder-Vorgang verschiebt Ordner aus einem angegebenen Ordner und fügt Sie in einen anderen Ordner ein.
ms.openlocfilehash: dc572130ca3b2f2b152abbb4a8b68cc6f67790e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460582"
---
# <a name="movefolder-operation"></a><span data-ttu-id="bf13b-103">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bf13b-103">MoveFolder operation</span></span>

<span data-ttu-id="bf13b-104">Der MoveFolder-Vorgang verschiebt Ordner aus einem angegebenen Ordner und fügt Sie in einen anderen Ordner ein.</span><span class="sxs-lookup"><span data-stu-id="bf13b-104">The MoveFolder operation moves folders from a specified folder and puts them in another folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf13b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf13b-105">Remarks</span></span>

<span data-ttu-id="bf13b-106">Der MoveFolder-Vorgang ähnelt dem CopyFolder-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bf13b-106">The MoveFolder operation is similar to the CopyFolder operation.</span></span> <span data-ttu-id="bf13b-107">Sie können keine Distinguished Folders migrieren.</span><span class="sxs-lookup"><span data-stu-id="bf13b-107">You cannot move distinguished folders.</span></span> <span data-ttu-id="bf13b-108">Sie können mehrere Ordner gleichzeitig in den Zielordner umlegen.</span><span class="sxs-lookup"><span data-stu-id="bf13b-108">You can move multiple folders at one time to the destination folder.</span></span>
  
## <a name="movefolder-request-example"></a><span data-ttu-id="bf13b-109">MoveFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="bf13b-109">MoveFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="bf13b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf13b-110">Description</span></span>

<span data-ttu-id="bf13b-111">Im folgenden Beispiel einer MoveFolder-Anforderung wird gezeigt, wie eine Anforderung zum Verschieben eines Ordners, der durch die [Ordner](folderid.md) -Nr identifiziert wird, und dem Ordner in den definierten Junk-e-Mail-Ordner gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf13b-111">The following example of a MoveFolder request shows how to form a request to move a folder identified by the [FolderId](folderid.md) and put the folder in the Junk E-mail distinguished folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bf13b-112">Code</span><span class="sxs-lookup"><span data-stu-id="bf13b-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="bf13b-113">Comments</span><span class="sxs-lookup"><span data-stu-id="bf13b-113">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="bf13b-114">Der Wert des ID-Attributs des [Folder](folderid.md) -ID-Elements wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="bf13b-114">The value of the ID attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="bf13b-115">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="bf13b-115">Request elements</span></span>

<span data-ttu-id="bf13b-116">Diese MoveFolder-Anforderung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="bf13b-116">This MoveFolder request includes the following elements:</span></span>
  
- [<span data-ttu-id="bf13b-117">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="bf13b-117">MoveFolder</span></span>](movefolder.md)
    
- [<span data-ttu-id="bf13b-118">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="bf13b-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="bf13b-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="bf13b-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="bf13b-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="bf13b-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="bf13b-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="bf13b-121">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="bf13b-122">Weitere Elemente, die Sie zum Erstellen einer MoveFolder-Anforderung verwenden können, finden Sie im Schema.</span><span class="sxs-lookup"><span data-stu-id="bf13b-122">See the schema for additional elements that you can use to form a MoveFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bf13b-123">Der Standardspeicherort des Schemas befindet sich im virtuellen Verzeichnis EWS auf dem Computer, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bf13b-123">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="successful-movefolder-response-example"></a><span data-ttu-id="bf13b-124">Erfolgreiches MoveFolder-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="bf13b-124">Successful MoveFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="bf13b-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf13b-125">Description</span></span>

<span data-ttu-id="bf13b-126">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die MoveFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bf13b-126">The following example shows a successful response to the MoveFolder request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bf13b-127">Code</span><span class="sxs-lookup"><span data-stu-id="bf13b-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="bf13b-128">Comments</span><span class="sxs-lookup"><span data-stu-id="bf13b-128">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="bf13b-129">Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bf13b-129">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="bf13b-130">Die in der Antwort zurückgegebene Ordner-Nr stellt den Ordner dar, der an den neuen Speicherort des Ordners verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="bf13b-130">The FolderId that is returned in the response represents the folder that was moved to the new the folder location.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="bf13b-131">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="bf13b-131">Response elements</span></span>

<span data-ttu-id="bf13b-132">Die MoveFolder-Antwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="bf13b-132">The MoveFolder response includes the following elements:</span></span>
  
- [<span data-ttu-id="bf13b-133">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="bf13b-133">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="bf13b-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bf13b-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bf13b-135">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bf13b-135">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="bf13b-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bf13b-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bf13b-137">Ordner</span><span class="sxs-lookup"><span data-stu-id="bf13b-137">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="bf13b-138">Folder</span><span class="sxs-lookup"><span data-stu-id="bf13b-138">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="bf13b-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="bf13b-139">FolderId</span></span>](folderid.md)
    
## <a name="movefolder-error-response-example"></a><span data-ttu-id="bf13b-140">MoveFolder-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="bf13b-140">MoveFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="bf13b-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf13b-141">Description</span></span>

<span data-ttu-id="bf13b-142">Das folgende Beispiel zeigt eine Fehlermeldung, die auftritt, wenn Sie versuchen, einen Distinguished Folder zu verlagern.</span><span class="sxs-lookup"><span data-stu-id="bf13b-142">The following example shows an error response that occurs when you try to move a distinguished folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="bf13b-143">Code</span><span class="sxs-lookup"><span data-stu-id="bf13b-143">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="bf13b-144">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="bf13b-144">Error response elements</span></span>

<span data-ttu-id="bf13b-145">Die MoveFolder-Fehlerantwort umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="bf13b-145">The MoveFolder error response includes the following elements:</span></span>
  
- [<span data-ttu-id="bf13b-146">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="bf13b-146">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="bf13b-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bf13b-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bf13b-148">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bf13b-148">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="bf13b-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="bf13b-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="bf13b-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bf13b-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bf13b-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bf13b-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="bf13b-152">Ordner</span><span class="sxs-lookup"><span data-stu-id="bf13b-152">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="bf13b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf13b-153">See also</span></span>



[<span data-ttu-id="bf13b-154">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bf13b-154">CopyFolder operation</span></span>](copyfolder-operation.md)

