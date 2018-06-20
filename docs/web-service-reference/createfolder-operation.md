---
title: CreateFolder Operation
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
description: Der CreateFolder-Vorgang erstellt Ordner, Kalenderordnern, Kontakteordner, Aufgaben Ordner und Suche Ordner.
ms.openlocfilehash: 97156d4a3747cacbdcf9563d21d93a0aa44c3358
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757758"
---
# <a name="createfolder-operation"></a><span data-ttu-id="8ea1f-103">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8ea1f-103">CreateFolder operation</span></span>

<span data-ttu-id="8ea1f-104">Der CreateFolder-Vorgang erstellt Ordner, Kalenderordnern, Kontakteordner, Aufgaben Ordner und Suche Ordner.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-104">The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders.</span></span>
  
## <a name="createfolder-request-example"></a><span data-ttu-id="8ea1f-105">CreateFolder-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="8ea1f-105">CreateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="8ea1f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ea1f-106">Description</span></span>

<span data-ttu-id="8ea1f-107">Im folgenden Beispiel wird eine Anforderung CreateFolder veranschaulicht eine Anforderung zum Erstellen von zwei neue Ordner im Stamm Postfach bilden.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-107">The following example of a CreateFolder request shows how to form a request to create two new folders in the mailbox root.</span></span>
  
### <a name="code"></a><span data-ttu-id="8ea1f-108">Code</span><span class="sxs-lookup"><span data-stu-id="8ea1f-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="request-elements"></a><span data-ttu-id="8ea1f-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="8ea1f-109">Request elements</span></span>

<span data-ttu-id="8ea1f-110">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ea1f-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="8ea1f-111">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="8ea1f-111">CreateFolder</span></span>](createfolder.md)
    
- [<span data-ttu-id="8ea1f-112">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="8ea1f-112">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="8ea1f-113">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="8ea1f-113">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="8ea1f-114">Ordner</span><span class="sxs-lookup"><span data-stu-id="8ea1f-114">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8ea1f-115">Folder</span><span class="sxs-lookup"><span data-stu-id="8ea1f-115">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="8ea1f-116">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="8ea1f-116">DisplayName (string)</span></span>](displayname-string.md)
    
> [!NOTE]
> <span data-ttu-id="8ea1f-117">Das Schema, das diese Elemente beschreibt, befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-117">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="8ea1f-118">Um weitere Optionen für die Anforderung an die CreateFolder-Operation zu suchen, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-118">To find other options for the request message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="8ea1f-119">Starten Sie die [CreateFolder](createfolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-119">Start at the [CreateFolder](createfolder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8ea1f-120">Wenn Sie einen Suchordner mit einer Einschränkung mithilfe der **Kalender: Organizer** -Eigenschaft erstellen, zurückgegebenen Gespräch Ordner nachfolgende Get die Einschränkung wieder mit der **Nachricht: aus** -Eigenschaft in seine Position.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-120">If you create a search folder with a restriction by using the **calendar:Organizer** property, a subsequent get folder call will return the restriction with the **message:from** property in its place.</span></span> <span data-ttu-id="8ea1f-121">Diese beiden Eigenschaften zuordnen der gleichen zugrunde liegenden MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-121">These two properties map to the same underlying MAPI property.</span></span> 
  
<span data-ttu-id="8ea1f-122">Die CreateFolder-Operation unterstützt die Erstellung einer benutzerdefinierten Ordner-Klasse nur, wenn Sie des Ordners erstellen mithilfe eine generische Ordner "Type"-Element und das **FolderClass** -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-122">The CreateFolder operation supports the creation of a custom folder class only when you create the folder by using a generic folder type element and set the **FolderClass** element.</span></span> 
  
## <a name="successful-createfolder-response-example"></a><span data-ttu-id="8ea1f-123">Erfolgreiche CreateFolder-Antwort-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ea1f-123">Successful CreateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="8ea1f-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ea1f-124">Description</span></span>

<span data-ttu-id="8ea1f-125">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-125">The following example shows a successful response to the CreateFolder request.</span></span> <span data-ttu-id="8ea1f-126">In diesem Beispiel gibt die Antwort den IDs der neuen Ordner.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-126">In this example, the response returns the identifiers of the new folders.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8ea1f-127">Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-127">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8ea1f-128">Code</span><span class="sxs-lookup"><span data-stu-id="8ea1f-128">Code</span></span>

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
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="8ea1f-129">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="8ea1f-129">Successful response elements</span></span>

<span data-ttu-id="8ea1f-130">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ea1f-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8ea1f-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8ea1f-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8ea1f-132">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="8ea1f-132">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="8ea1f-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8ea1f-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8ea1f-134">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8ea1f-134">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="8ea1f-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8ea1f-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8ea1f-136">Ordner</span><span class="sxs-lookup"><span data-stu-id="8ea1f-136">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8ea1f-137">Folder</span><span class="sxs-lookup"><span data-stu-id="8ea1f-137">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="8ea1f-138">FolderId</span><span class="sxs-lookup"><span data-stu-id="8ea1f-138">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="8ea1f-139">Wenn andere Optionen für die Antwortnachricht des Vorgangs CreateFolder suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-139">To find other options for the response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="8ea1f-140">Starten Sie das [CreateFolderResponse](createfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-140">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="createfolder-error-response"></a><span data-ttu-id="8ea1f-141">CreateFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="8ea1f-141">CreateFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="8ea1f-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ea1f-142">Description</span></span>

<span data-ttu-id="8ea1f-143">Das folgende Beispiel zeigt eine Fehlerantwort an eine CreateFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-143">The following example shows an error response to a CreateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="8ea1f-144">Code</span><span class="sxs-lookup"><span data-stu-id="8ea1f-144">Code</span></span>

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
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="8ea1f-145">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="8ea1f-145">Error response elements</span></span>

<span data-ttu-id="8ea1f-146">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="8ea1f-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="8ea1f-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8ea1f-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8ea1f-148">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="8ea1f-148">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="8ea1f-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8ea1f-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8ea1f-150">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8ea1f-150">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="8ea1f-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="8ea1f-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8ea1f-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8ea1f-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8ea1f-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8ea1f-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="8ea1f-154">Ordner</span><span class="sxs-lookup"><span data-stu-id="8ea1f-154">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="8ea1f-155">Wenn andere Optionen für die Fehlermeldung Antwort des Vorgangs CreateFolder suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-155">To find other options for the error response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="8ea1f-156">Starten Sie das [CreateFolderResponse](createfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-156">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ea1f-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ea1f-157">See also</span></span>



[<span data-ttu-id="8ea1f-158">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8ea1f-158">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="8ea1f-159">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8ea1f-159">FindFolder operation</span></span>](findfolder-operation.md)
  
 <span data-ttu-id="8ea1f-160">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="8ea1f-160">**CreateFolderType**</span></span>


- [<span data-ttu-id="8ea1f-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8ea1f-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="8ea1f-162">Erstellen von Ordnern (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="8ea1f-162">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

