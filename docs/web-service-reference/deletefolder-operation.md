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
description: Der DeleteFolder-Vorgang löscht Ordner aus einem Postfach.
ms.openlocfilehash: e9bb9199027c2af2cbbb664ef7ad4fa70b7ef718
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455744"
---
# <a name="deletefolder-operation"></a><span data-ttu-id="17441-103">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="17441-103">DeleteFolder operation</span></span>

<span data-ttu-id="17441-104">Der **DeleteFolder** -Vorgang löscht Ordner aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="17441-104">The **DeleteFolder** operation deletes folders from a mailbox.</span></span> 
  
## <a name="deletefolder-request-example"></a><span data-ttu-id="17441-105">DeleteFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="17441-105">DeleteFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="17441-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17441-106">Description</span></span>

<span data-ttu-id="17441-107">Im folgenden Beispiel einer **DeleteFolder** -Anforderung wird gezeigt, wie Sie eine Anforderung zum Löschen eines Ordners bilden.</span><span class="sxs-lookup"><span data-stu-id="17441-107">This following example of a **DeleteFolder** request shows how to form a request to delete a folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="17441-108">Code</span><span class="sxs-lookup"><span data-stu-id="17441-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                  DeleteType="HardDelete" >
      <FolderIds>
        <t:FolderId Id="AS4AUnVz=" />
      </FolderIds>
    </DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="17441-109">Comments</span><span class="sxs-lookup"><span data-stu-id="17441-109">Comments</span></span>

<span data-ttu-id="17441-110">In diesem Beispiel wird ein harter Löschvorgang für den Ordner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17441-110">This example performs a hard delete on the folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="17441-111">Die Ordner-ID wurde verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="17441-111">The folder ID has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="17441-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="17441-112">Request elements</span></span>

<span data-ttu-id="17441-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="17441-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="17441-114">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="17441-114">DeleteFolder</span></span>](deletefolder.md)
    
- [<span data-ttu-id="17441-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="17441-115">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="17441-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="17441-116">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="17441-117">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="17441-117">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="17441-118">Um andere Optionen für die Anforderungsnachricht des **DeleteFolder** -Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="17441-118">To find other options for the request message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="17441-119">Beginnen Sie mit dem [DeleteFolder](deletefolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="17441-119">Start at the [DeleteFolder](deletefolder.md) element.</span></span> 
  
## <a name="successful-deletefolder-response"></a><span data-ttu-id="17441-120">Erfolgreiche DeleteFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="17441-120">Successful DeleteFolder response</span></span>

### <a name="description"></a><span data-ttu-id="17441-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17441-121">Description</span></span>

<span data-ttu-id="17441-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **DeleteFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="17441-122">The following example shows a successful response to the **DeleteFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="17441-123">Code</span><span class="sxs-lookup"><span data-stu-id="17441-123">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="17441-124">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="17441-124">Response elements</span></span>

<span data-ttu-id="17441-125">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="17441-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="17441-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="17441-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="17441-127">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="17441-127">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="17441-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="17441-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="17441-129">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="17441-129">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="17441-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="17441-130">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="17441-131">Um andere Optionen für die Antwortnachricht des **DeleteFolder** -Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="17441-131">To find other options for the response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="17441-132">Beginnen Sie mit dem [DeleteFolderResponse](deletefolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="17441-132">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="deletefolder-error-response"></a><span data-ttu-id="17441-133">DeleteFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="17441-133">DeleteFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="17441-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17441-134">Description</span></span>

<span data-ttu-id="17441-135">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **DeleteFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="17441-135">The following example shows an error response to a **DeleteFolder** request.</span></span> <span data-ttu-id="17441-136">Der Fehler wurde durch eine Anforderung zum Löschen eines Ordners verursacht, der nicht im Postfach vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="17441-136">The error was caused by a request to delete a folder that was not present in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="17441-137">Code</span><span class="sxs-lookup"><span data-stu-id="17441-137">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="17441-138">Comments</span><span class="sxs-lookup"><span data-stu-id="17441-138">Comments</span></span>

<span data-ttu-id="17441-139">Der **DeleteFolder** -Vorgang kann nicht für Distinguished Folders verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17441-139">The **DeleteFolder** operation cannot be used on distinguished folders.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="17441-140">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="17441-140">Error response elements</span></span>

<span data-ttu-id="17441-141">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="17441-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="17441-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="17441-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="17441-143">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="17441-143">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="17441-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="17441-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="17441-145">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="17441-145">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="17441-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="17441-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="17441-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="17441-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="17441-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="17441-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="17441-149">Weitere Optionen für die Fehlerantwort Meldung des **DeleteFolder** -Vorgangs finden Sie unter Durchsuchen der Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="17441-149">To find other options for the error response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="17441-150">Beginnen Sie mit dem [DeleteFolderResponse](deletefolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="17441-150">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17441-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17441-151">See also</span></span>

- [<span data-ttu-id="17441-152">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="17441-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="17441-153">Löschen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="17441-153">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

