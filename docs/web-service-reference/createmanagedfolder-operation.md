---
title: CreateManagedFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: Der Vorgang CreateManagedFolder erstellt einen verwalteten Ordner im Exchange-Speicher.
ms.openlocfilehash: 2c2af53dc5dbe1e6fcbc7f3b1174a856e51e4905
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757793"
---
# <a name="createmanagedfolder-operation"></a><span data-ttu-id="61dd2-103">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="61dd2-103">CreateManagedFolder operation</span></span>

<span data-ttu-id="61dd2-104">Der Vorgang CreateManagedFolder erstellt einen verwalteten Ordner im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="61dd2-104">The CreateManagedFolder operation creates a managed folder in the Exchange store.</span></span>
  
## <a name="using-the-createmanagedfolder-operation"></a><span data-ttu-id="61dd2-105">Verwenden des CreateManagedFolder-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="61dd2-105">Using the CreateManagedFolder Operation</span></span>

<span data-ttu-id="61dd2-106">Der Vorgang CreateManagedFolder hinzugefügt Postfach eines Benutzers einen verwalteten benutzerdefinierten Ordner.</span><span class="sxs-lookup"><span data-stu-id="61dd2-106">The CreateManagedFolder operation adds a managed custom folder to a user's mailbox.</span></span> <span data-ttu-id="61dd2-107">Das Exchange-Verwaltungsshell **Get-ManagedFolder** -Cmdlet können Sie die verfügbaren verwalteten Ordner hinzufügen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="61dd2-107">You can use the Exchange Management Shell **Get-ManagedFolder** cmdlet to find available managed folders to add.</span></span> <span data-ttu-id="61dd2-108">Obwohl dieses Cmdlet verwalteten benutzerdefinierten Ordnern und verwalteten Standardordnern nur verwalteten benutzerdefinierten zurückgibt, können Ordner hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="61dd2-108">Although this cmdlet returns both managed custom folders and managed default folders, only managed custom folders can be added.</span></span> <span data-ttu-id="61dd2-109">Verwaltete benutzerdefinierte Ordnern werden durch den Ordnertyp ManagedCustomFolder identifiziert.</span><span class="sxs-lookup"><span data-stu-id="61dd2-109">Managed custom folders are identified by the ManagedCustomFolder folder type.</span></span> <span data-ttu-id="61dd2-110">Der System.DirectoryServices-Namespace enthält auch Typen, die verwendet werden können, um die Namen der verfügbaren verwaltete Ordner zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="61dd2-110">The System.DirectoryServices namespace also includes types that can be used to discover the names of available managed folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="61dd2-111">Exchange-Webdienste können Sie die Namen der verfügbaren verwalteten Ordner hinzufügen zu einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="61dd2-111">You cannot use Exchange Web Services to find the names of available managed folders to add to a mailbox.</span></span> 
  
<span data-ttu-id="61dd2-112">Die FindFolder und GetFolder Vorgänge können Sie verwaltete Ordner zugreifen.</span><span class="sxs-lookup"><span data-stu-id="61dd2-112">You can use the FindFolder and GetFolder operations to access managed folders.</span></span> <span data-ttu-id="61dd2-113">FindFolder wird verwendet, um nach Ordnern in einem angegebenen übergeordneten Ordner suchen.</span><span class="sxs-lookup"><span data-stu-id="61dd2-113">FindFolder is used to search for folders in a specified parent folder.</span></span> <span data-ttu-id="61dd2-114">Dies kann verwendet werden, damit verwaltete Ordner ermittelt werden können in einem Ordner vor dem Hinzufügen, dass ein Duplikat benutzerdefinierten Ordner in dasselbe Verzeichnis verwaltet.</span><span class="sxs-lookup"><span data-stu-id="61dd2-114">This can be used so that managed folders can be discovered in a folder before trying to add a duplicate managed custom folder to the same directory.</span></span> <span data-ttu-id="61dd2-115">GetFolder wird nach der Operation FindFolder verwendet, um weitere Informationen zu einem verwalteten benutzerdefinierten Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="61dd2-115">GetFolder is used after the FindFolder operation to get more information about a managed custom folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61dd2-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61dd2-116">Remarks</span></span>

<span data-ttu-id="61dd2-117">Informationen zum Einrichten von messaging Records Management (MRM) Richtlinie finden Sie unter [Gewusst wie: Erstellen einer Postfachrichtlinie für verwaltete Ordner](http://go.microsoft.com/fwlink/?LinkId=100975).</span><span class="sxs-lookup"><span data-stu-id="61dd2-117">For information about how to set up messaging records management (MRM) policy, see [How to Create a Managed Folder Mailbox Policy](http://go.microsoft.com/fwlink/?LinkId=100975).</span></span>
  
<span data-ttu-id="61dd2-118">Informationen zum Entfernen von verwaltete benutzerdefinierte Ordnern aus einem Postfach finden Sie unter [Remove-ManagedFolder](http://go.microsoft.com/fwlink/?LinkId=100976).</span><span class="sxs-lookup"><span data-stu-id="61dd2-118">For information about how to remove managed custom folders from a mailbox, see [Remove-ManagedFolder](http://go.microsoft.com/fwlink/?LinkId=100976).</span></span>
  
## <a name="createmanagedfolder-request-example"></a><span data-ttu-id="61dd2-119">Anforderungsbeispiel CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="61dd2-119">CreateManagedFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="61dd2-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61dd2-120">Description</span></span>

<span data-ttu-id="61dd2-121">Im folgenden Beispiel wird eine Anforderung CreateManagedFolder veranschaulicht das Hinzufügen eines verwalteten Ordners mit der Bezeichnung Test verwaltete Ordner an ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="61dd2-121">The following example of a CreateManagedFolder request shows how to add a managed folder named Test Managed Folder to a mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61dd2-122">Delegieren des Zugriffs können auch verwaltete benutzerdefinierte Ordnern hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="61dd2-122">You can also use delegate access to add managed custom folders.</span></span> 
  
### <a name="code"></a><span data-ttu-id="61dd2-123">Code</span><span class="sxs-lookup"><span data-stu-id="61dd2-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="61dd2-124">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="61dd2-124">Request elements</span></span>

<span data-ttu-id="61dd2-125">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="61dd2-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="61dd2-126">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="61dd2-126">CreateManagedFolder</span></span>](createmanagedfolder.md)
    
- [<span data-ttu-id="61dd2-127">FolderNames</span><span class="sxs-lookup"><span data-stu-id="61dd2-127">FolderNames</span></span>](foldernames.md)
    
- [<span data-ttu-id="61dd2-128">Ordnername</span><span class="sxs-lookup"><span data-stu-id="61dd2-128">FolderName</span></span>](foldername.md)
    
<span data-ttu-id="61dd2-129">Wenn andere Optionen für die Anforderungsnachricht des Vorgangs CreateManagedFolder suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="61dd2-129">To find other options for the request message of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="61dd2-130">Starten Sie das [CreateManagedFolder](createmanagedfolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="61dd2-130">Start at the [CreateManagedFolder](createmanagedfolder.md) element.</span></span> 
  
## <a name="successful-createmanagedfolder-response"></a><span data-ttu-id="61dd2-131">Erfolgreiche CreateManagedFolder Antwort</span><span class="sxs-lookup"><span data-stu-id="61dd2-131">Successful CreateManagedFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="61dd2-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61dd2-132">Description</span></span>

<span data-ttu-id="61dd2-133">Das folgende Codebeispiel zeigt eine erfolgreiche Antwort auf eine Anforderung CreateManagedFolder.</span><span class="sxs-lookup"><span data-stu-id="61dd2-133">The following code example shows a successful response to a CreateManagedFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61dd2-134">Attributwerte **-Id** und **ChangeKey** wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61dd2-134">The **Id** and **ChangeKey** attribute values have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="61dd2-135">Code</span><span class="sxs-lookup"><span data-stu-id="61dd2-135">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="61dd2-136">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="61dd2-136">Successful response elements</span></span>

<span data-ttu-id="61dd2-137">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="61dd2-137">The following elements are used in the response:</span></span> 
  
- [<span data-ttu-id="61dd2-138">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="61dd2-138">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="61dd2-139">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61dd2-139">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="61dd2-140">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61dd2-140">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="61dd2-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="61dd2-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="61dd2-142">Ordner</span><span class="sxs-lookup"><span data-stu-id="61dd2-142">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="61dd2-143">Folder</span><span class="sxs-lookup"><span data-stu-id="61dd2-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="61dd2-144">FolderId</span><span class="sxs-lookup"><span data-stu-id="61dd2-144">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="61dd2-145">Wenn andere Optionen für die Antwortnachrichten des Vorgangs CreateManagedFolder suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="61dd2-145">To find other options for the response messages of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="61dd2-146">Starten Sie das [CreateManagedFolderResponse](createmanagedfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="61dd2-146">Start at the [CreateManagedFolderResponse](createmanagedfolderresponse.md) element.</span></span> 
  
## <a name="createmanagedfolder-error-response"></a><span data-ttu-id="61dd2-147">Fehlerantwort CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="61dd2-147">CreateManagedFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="61dd2-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61dd2-148">Description</span></span>

<span data-ttu-id="61dd2-149">Das folgende Codebeispiel zeigt eine Fehlerantwort an eine CreateManagedFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="61dd2-149">The following code example shows an error response to a CreateManagedFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="61dd2-150">Code</span><span class="sxs-lookup"><span data-stu-id="61dd2-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="61dd2-151">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="61dd2-151">Error response elements</span></span>

<span data-ttu-id="61dd2-152">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="61dd2-152">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="61dd2-153">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="61dd2-153">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="61dd2-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61dd2-154">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="61dd2-155">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61dd2-155">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="61dd2-156">MessageText</span><span class="sxs-lookup"><span data-stu-id="61dd2-156">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="61dd2-157">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="61dd2-157">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="61dd2-158">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="61dd2-158">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="61dd2-159">Ordner</span><span class="sxs-lookup"><span data-stu-id="61dd2-159">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="61dd2-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61dd2-160">See also</span></span>



[<span data-ttu-id="61dd2-161">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="61dd2-161">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="61dd2-162">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="61dd2-162">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="61dd2-163">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="61dd2-163">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="61dd2-164">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="61dd2-164">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

