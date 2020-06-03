---
title: CreateFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 6f6c334c-b190-4e55-8f0a-38f2a018d1b3
description: Der CreateFolder-Vorgang erstellt Ordner, Kalenderordner, Kontakteordner, Aufgabenordner und Suchordner.
ms.openlocfilehash: 125a6d212e5eaf85ace71c048de809f3a05ba9b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457550"
---
# <a name="createfolder-operation"></a><span data-ttu-id="cf452-103">CreateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf452-103">CreateFolder operation</span></span>

<span data-ttu-id="cf452-104">Der CreateFolder-Vorgang erstellt Ordner, Kalenderordner, Kontakteordner, Aufgabenordner und Suchordner.</span><span class="sxs-lookup"><span data-stu-id="cf452-104">The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders.</span></span>
  
## <a name="createfolder-request-example"></a><span data-ttu-id="cf452-105">CreateFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="cf452-105">CreateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="cf452-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf452-106">Description</span></span>

<span data-ttu-id="cf452-107">Im folgenden Beispiel einer CreateFolder-Anforderung wird gezeigt, wie eine Anforderung zum Erstellen von zwei neuen Ordnern im Postfachstamm Formular erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf452-107">The following example of a CreateFolder request shows how to form a request to create two new folders in the mailbox root.</span></span>
  
### <a name="code"></a><span data-ttu-id="cf452-108">Code</span><span class="sxs-lookup"><span data-stu-id="cf452-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ParentFolderId>
        <t:DistinguishedFolderId Id="msgfolderroot"/>
      </ParentFolderId>
      <Folders>
        <t:Folder>
          <t:DisplayName>Folder1</t:DisplayName>
        </t:Folder>
        <t:Folder>
          <t:DisplayName>Folder2</t:DisplayName>
        </t:Folder>
      </Folders>
    </CreateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="cf452-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="cf452-109">Request elements</span></span>

<span data-ttu-id="cf452-110">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="cf452-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="cf452-111">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="cf452-111">CreateFolder</span></span>](createfolder.md)
    
- [<span data-ttu-id="cf452-112">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="cf452-112">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="cf452-113">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="cf452-113">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="cf452-114">Ordner</span><span class="sxs-lookup"><span data-stu-id="cf452-114">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="cf452-115">Ordner</span><span class="sxs-lookup"><span data-stu-id="cf452-115">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="cf452-116">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="cf452-116">DisplayName (string)</span></span>](displayname-string.md)
    
> [!NOTE]
> <span data-ttu-id="cf452-117">Das Schema, in dem diese Elemente beschrieben werden, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cf452-117">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="cf452-118">Um andere Optionen für die Anforderungsnachricht des CreateFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="cf452-118">To find other options for the request message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="cf452-119">Beginnen Sie mit dem [CreateFolder](createfolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="cf452-119">Start at the [CreateFolder](createfolder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cf452-120">Wenn Sie einen Suchordner mit einer Einschränkung mithilfe der **Calendar: Organizer** -Eigenschaft erstellen, wird durch einen nachfolgenden Aufruf des Get-Ordners die Einschränkung mit der **Message: from** -Eigenschaft an ihrer Stelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf452-120">If you create a search folder with a restriction by using the **calendar:Organizer** property, a subsequent get folder call will return the restriction with the **message:from** property in its place.</span></span> <span data-ttu-id="cf452-121">Diese beiden Eigenschaften sind der gleichen zugrunde liegenden MAPI-Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cf452-121">These two properties map to the same underlying MAPI property.</span></span> 
  
<span data-ttu-id="cf452-122">Der CreateFolder-Vorgang unterstützt die Erstellung einer benutzerdefinierten ordnerklasse nur, wenn Sie den Ordner mithilfe eines generischen Folder Type-Elements erstellen und das **FolderClass** -Element festlegen.</span><span class="sxs-lookup"><span data-stu-id="cf452-122">The CreateFolder operation supports the creation of a custom folder class only when you create the folder by using a generic folder type element and set the **FolderClass** element.</span></span> 
  
## <a name="successful-createfolder-response-example"></a><span data-ttu-id="cf452-123">Erfolgreiches Beispiel für CreateFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="cf452-123">Successful CreateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="cf452-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf452-124">Description</span></span>

<span data-ttu-id="cf452-125">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cf452-125">The following example shows a successful response to the CreateFolder request.</span></span> <span data-ttu-id="cf452-126">In diesem Beispiel gibt die Antwort die Bezeichner der neuen Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="cf452-126">In this example, the response returns the identifiers of the new folders.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf452-127">Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf452-127">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cf452-128">Code</span><span class="sxs-lookup"><span data-stu-id="cf452-128">Code</span></span>

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
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="cf452-129">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="cf452-129">Successful response elements</span></span>

<span data-ttu-id="cf452-130">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="cf452-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="cf452-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cf452-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="cf452-132">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="cf452-132">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="cf452-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf452-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="cf452-134">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf452-134">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="cf452-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf452-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="cf452-136">Ordner</span><span class="sxs-lookup"><span data-stu-id="cf452-136">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="cf452-137">Ordner</span><span class="sxs-lookup"><span data-stu-id="cf452-137">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="cf452-138">FolderId</span><span class="sxs-lookup"><span data-stu-id="cf452-138">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="cf452-139">Um andere Optionen für die Antwortnachricht des CreateFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="cf452-139">To find other options for the response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="cf452-140">Beginnen Sie mit dem [CreateFolderResponse](createfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="cf452-140">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="createfolder-error-response"></a><span data-ttu-id="cf452-141">CreateFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="cf452-141">CreateFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="cf452-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf452-142">Description</span></span>

<span data-ttu-id="cf452-143">Das folgende Beispiel zeigt eine Fehlerantwort auf eine CreateFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cf452-143">The following example shows an error response to a CreateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="cf452-144">Code</span><span class="sxs-lookup"><span data-stu-id="cf452-144">Code</span></span>

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
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A folder with the specified name already exists.</m:MessageText>
          <m:ResponseCode>ErrorFolderExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="cf452-145">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="cf452-145">Error response elements</span></span>

<span data-ttu-id="cf452-146">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="cf452-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="cf452-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cf452-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="cf452-148">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="cf452-148">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="cf452-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf452-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="cf452-150">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf452-150">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="cf452-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="cf452-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="cf452-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf452-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="cf452-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cf452-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="cf452-154">Ordner</span><span class="sxs-lookup"><span data-stu-id="cf452-154">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="cf452-155">Um andere Optionen für die Fehlerantwort Meldung des CreateFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="cf452-155">To find other options for the error response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="cf452-156">Beginnen Sie mit dem [CreateFolderResponse](createfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="cf452-156">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf452-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf452-157">See also</span></span>



[<span data-ttu-id="cf452-158">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf452-158">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="cf452-159">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cf452-159">FindFolder operation</span></span>](findfolder-operation.md)
  
 <span data-ttu-id="cf452-160">**Createfoldertype**</span><span class="sxs-lookup"><span data-stu-id="cf452-160">**CreateFolderType**</span></span>


- [<span data-ttu-id="cf452-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cf452-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="cf452-162">Erstellen von Ordnern (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="cf452-162">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

