---
title: DeleteFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: b0f92682-4895-4bcf-a4a1-e4c2e8403979
description: DeleteFolder-Vorgang Ordnern aus einem Postfach gelöscht.
ms.openlocfilehash: 0fd7c9d4b04a706dcdb83f41087eaa4f3d45f129
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757917"
---
# <a name="deletefolder-operation"></a><span data-ttu-id="2432a-103">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2432a-103">DeleteFolder operation</span></span>

<span data-ttu-id="2432a-104">**DeleteFolder** -Vorgang Ordnern aus einem Postfach gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2432a-104">The **DeleteFolder** operation deletes folders from a mailbox.</span></span> 
  
## <a name="deletefolder-request-example"></a><span data-ttu-id="2432a-105">DeleteFolder-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="2432a-105">DeleteFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="2432a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2432a-106">Description</span></span>

<span data-ttu-id="2432a-107">Im folgenden Beispiel eine Anforderung **DeleteFolder** veranschaulicht eine Anforderung zum Löschen eines Ordners bilden.</span><span class="sxs-lookup"><span data-stu-id="2432a-107">This following example of a **DeleteFolder** request shows how to form a request to delete a folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2432a-108">Code</span><span class="sxs-lookup"><span data-stu-id="2432a-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                  DeleteType="HardDelete" >
      <FolderIds>
        <t:FolderId Id="AS4AUnVz=" />
      </FolderIds>
    </DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2432a-109">Kommentare</span><span class="sxs-lookup"><span data-stu-id="2432a-109">Comments</span></span>

<span data-ttu-id="2432a-110">In diesem Beispiel werden ein harte löschen für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="2432a-110">This example performs a hard delete on the folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2432a-111">Die Ordner-ID wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2432a-111">The folder ID has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="2432a-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="2432a-112">Request elements</span></span>

<span data-ttu-id="2432a-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="2432a-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="2432a-114">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="2432a-114">DeleteFolder</span></span>](deletefolder.md)
    
- [<span data-ttu-id="2432a-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="2432a-115">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="2432a-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="2432a-116">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="2432a-117">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2432a-117">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="2432a-118">Wenn andere Optionen für die Anforderungsnachricht des Vorgangs **DeleteFolder** suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="2432a-118">To find other options for the request message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="2432a-119">Starten Sie das [DeleteFolder](deletefolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="2432a-119">Start at the [DeleteFolder](deletefolder.md) element.</span></span> 
  
## <a name="successful-deletefolder-response"></a><span data-ttu-id="2432a-120">Erfolgreiche DeleteFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="2432a-120">Successful DeleteFolder response</span></span>

### <a name="description"></a><span data-ttu-id="2432a-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2432a-121">Description</span></span>

<span data-ttu-id="2432a-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **DeleteFolder** .</span><span class="sxs-lookup"><span data-stu-id="2432a-122">The following example shows a successful response to the **DeleteFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2432a-123">Code</span><span class="sxs-lookup"><span data-stu-id="2432a-123">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="2432a-124">Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="2432a-124">Response elements</span></span>

<span data-ttu-id="2432a-125">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="2432a-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="2432a-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2432a-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2432a-127">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="2432a-127">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="2432a-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2432a-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2432a-129">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2432a-129">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="2432a-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2432a-130">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="2432a-131">Wenn andere Optionen für die Antwortnachricht des Vorgangs **DeleteFolder** suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="2432a-131">To find other options for the response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="2432a-132">Starten Sie das [DeleteFolderResponse](deletefolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="2432a-132">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="deletefolder-error-response"></a><span data-ttu-id="2432a-133">DeleteFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="2432a-133">DeleteFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="2432a-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2432a-134">Description</span></span>

<span data-ttu-id="2432a-135">Das folgende Beispiel zeigt eine Fehlerantwort an eine **DeleteFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2432a-135">The following example shows an error response to a **DeleteFolder** request.</span></span> <span data-ttu-id="2432a-136">Der Fehler wurde durch eine Anforderung an einen Ordner löschen, der nicht im Postfach vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="2432a-136">The error was caused by a request to delete a folder that was not present in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2432a-137">Code</span><span class="sxs-lookup"><span data-stu-id="2432a-137">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2432a-138">Kommentare</span><span class="sxs-lookup"><span data-stu-id="2432a-138">Comments</span></span>

<span data-ttu-id="2432a-139">**DeleteFolder** -Vorgang kann nicht auf definierte Ordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2432a-139">The **DeleteFolder** operation cannot be used on distinguished folders.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="2432a-140">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="2432a-140">Error response elements</span></span>

<span data-ttu-id="2432a-141">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="2432a-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="2432a-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2432a-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2432a-143">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="2432a-143">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="2432a-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2432a-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="2432a-145">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2432a-145">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="2432a-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="2432a-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2432a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2432a-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2432a-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2432a-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="2432a-149">Wenn andere Optionen für die Fehlermeldung Antwort des Vorgangs **DeleteFolder** suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="2432a-149">To find other options for the error response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="2432a-150">Starten Sie das [DeleteFolderResponse](deletefolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="2432a-150">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2432a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2432a-151">See also</span></span>

- [<span data-ttu-id="2432a-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2432a-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="2432a-153">Löschen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="2432a-153">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

