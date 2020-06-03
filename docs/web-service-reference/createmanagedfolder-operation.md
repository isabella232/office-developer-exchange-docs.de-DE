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
description: Mit dem CreateManagedFolder-Vorgang wird ein verwalteter Ordner im Exchange-Informationsspeicher erstellt.
ms.openlocfilehash: 779c730b55b9b441644108a6837f9e22d39cc2f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44444593"
---
# <a name="createmanagedfolder-operation"></a><span data-ttu-id="ff0e6-103">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ff0e6-103">CreateManagedFolder operation</span></span>

<span data-ttu-id="ff0e6-104">Mit dem CreateManagedFolder-Vorgang wird ein verwalteter Ordner im Exchange-Informationsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-104">The CreateManagedFolder operation creates a managed folder in the Exchange store.</span></span>
  
## <a name="using-the-createmanagedfolder-operation"></a><span data-ttu-id="ff0e6-105">Verwenden des CreateManagedFolder-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ff0e6-105">Using the CreateManagedFolder Operation</span></span>

<span data-ttu-id="ff0e6-106">Mit dem CreateManagedFolder-Vorgang wird dem Postfach eines Benutzers ein verwalteter benutzerdefinierter Ordner hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-106">The CreateManagedFolder operation adds a managed custom folder to a user's mailbox.</span></span> <span data-ttu-id="ff0e6-107">Mit dem Cmdlet Exchange-Verwaltungsshell **Get-ManagedFolder** können Sie nach verfügbaren verwalteten Ordnern suchen, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-107">You can use the Exchange Management Shell **Get-ManagedFolder** cmdlet to find available managed folders to add.</span></span> <span data-ttu-id="ff0e6-108">Dieses Cmdlet gibt zwar sowohl verwaltete benutzerdefinierte Ordner als auch verwaltete Standardordner zurück, nur verwaltete benutzerdefinierte Ordner können hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-108">Although this cmdlet returns both managed custom folders and managed default folders, only managed custom folders can be added.</span></span> <span data-ttu-id="ff0e6-109">Verwaltete benutzerdefinierte Ordner werden anhand des ManagedCustomFolder-Ordnertyps identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-109">Managed custom folders are identified by the ManagedCustomFolder folder type.</span></span> <span data-ttu-id="ff0e6-110">Der System. DirectoryServices-Namespace enthält auch Typen, die zum Ermitteln der Namen von verfügbaren verwalteten Ordnern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-110">The System.DirectoryServices namespace also includes types that can be used to discover the names of available managed folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ff0e6-111">Sie können Exchange Webdienste nicht verwenden, um die Namen der verfügbaren verwalteten Ordner zu finden, die einem Postfach hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-111">You cannot use Exchange Web Services to find the names of available managed folders to add to a mailbox.</span></span> 
  
<span data-ttu-id="ff0e6-112">Sie können die FindFolder-und GetFolder-Vorgänge verwenden, um auf verwaltete Ordner zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-112">You can use the FindFolder and GetFolder operations to access managed folders.</span></span> <span data-ttu-id="ff0e6-113">FindFolder wird verwendet, um nach Ordnern in einem angegebenen übergeordneten Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-113">FindFolder is used to search for folders in a specified parent folder.</span></span> <span data-ttu-id="ff0e6-114">Dies kann verwendet werden, damit verwaltete Ordner in einem Ordner erkannt werden können, bevor ein doppelter verwalteter benutzerdefinierter Ordner demselben Verzeichnis hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-114">This can be used so that managed folders can be discovered in a folder before trying to add a duplicate managed custom folder to the same directory.</span></span> <span data-ttu-id="ff0e6-115">GetFolder wird nach dem FindFolder-Vorgang verwendet, um weitere Informationen zu einem verwalteten benutzerdefinierten Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-115">GetFolder is used after the FindFolder operation to get more information about a managed custom folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff0e6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff0e6-116">Remarks</span></span>

<span data-ttu-id="ff0e6-117">Informationen zum Einrichten der Messaging-Datensatzverwaltung (MRM)-Richtlinie finden Sie unter [Erstellen einer Postfachrichtlinie für verwalteten Ordner](https://go.microsoft.com/fwlink/?LinkId=100975).</span><span class="sxs-lookup"><span data-stu-id="ff0e6-117">For information about how to set up messaging records management (MRM) policy, see [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).</span></span>
  
<span data-ttu-id="ff0e6-118">Informationen zum Entfernen verwalteter benutzerdefinierter Ordner aus einem Postfach finden Sie unter [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).</span><span class="sxs-lookup"><span data-stu-id="ff0e6-118">For information about how to remove managed custom folders from a mailbox, see [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).</span></span>
  
## <a name="createmanagedfolder-request-example"></a><span data-ttu-id="ff0e6-119">CreateManagedFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff0e6-119">CreateManagedFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="ff0e6-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff0e6-120">Description</span></span>

<span data-ttu-id="ff0e6-121">Im folgenden Beispiel einer CreateManagedFolder-Anforderung wird gezeigt, wie einem Postfach ein verwalteter Ordner mit dem Namen "Test Managed Folder" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-121">The following example of a CreateManagedFolder request shows how to add a managed folder named Test Managed Folder to a mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ff0e6-122">Sie können auch den Stellvertretungszugriff zum Hinzufügen verwalteter benutzerdefinierter Ordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-122">You can also use delegate access to add managed custom folders.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ff0e6-123">Code</span><span class="sxs-lookup"><span data-stu-id="ff0e6-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="ff0e6-124">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="ff0e6-124">Request elements</span></span>

<span data-ttu-id="ff0e6-125">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ff0e6-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ff0e6-126">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="ff0e6-126">CreateManagedFolder</span></span>](createmanagedfolder.md)
    
- [<span data-ttu-id="ff0e6-127">FolderNames</span><span class="sxs-lookup"><span data-stu-id="ff0e6-127">FolderNames</span></span>](foldernames.md)
    
- [<span data-ttu-id="ff0e6-128">FolderName</span><span class="sxs-lookup"><span data-stu-id="ff0e6-128">FolderName</span></span>](foldername.md)
    
<span data-ttu-id="ff0e6-129">Um andere Optionen für die Anforderungsnachricht des CreateManagedFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-129">To find other options for the request message of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="ff0e6-130">Beginnen Sie mit dem [CreateManagedFolder](createmanagedfolder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-130">Start at the [CreateManagedFolder](createmanagedfolder.md) element.</span></span> 
  
## <a name="successful-createmanagedfolder-response"></a><span data-ttu-id="ff0e6-131">Erfolgreiche CreateManagedFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="ff0e6-131">Successful CreateManagedFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="ff0e6-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff0e6-132">Description</span></span>

<span data-ttu-id="ff0e6-133">Das folgende Codebeispiel zeigt eine erfolgreiche Antwort auf eine CreateManagedFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-133">The following code example shows a successful response to a CreateManagedFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ff0e6-134">Die **ID** -und **ChangeKey** -Attributwerte wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-134">The **Id** and **ChangeKey** attribute values have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ff0e6-135">Code</span><span class="sxs-lookup"><span data-stu-id="ff0e6-135">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="ff0e6-136">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="ff0e6-136">Successful response elements</span></span>

<span data-ttu-id="ff0e6-137">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ff0e6-137">The following elements are used in the response:</span></span> 
  
- [<span data-ttu-id="ff0e6-138">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ff0e6-138">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="ff0e6-139">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ff0e6-139">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ff0e6-140">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ff0e6-140">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="ff0e6-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff0e6-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff0e6-142">Ordner</span><span class="sxs-lookup"><span data-stu-id="ff0e6-142">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ff0e6-143">Ordner</span><span class="sxs-lookup"><span data-stu-id="ff0e6-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="ff0e6-144">FolderId</span><span class="sxs-lookup"><span data-stu-id="ff0e6-144">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="ff0e6-145">Um andere Optionen für die Antwortnachrichten des CreateManagedFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-145">To find other options for the response messages of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="ff0e6-146">Beginnen Sie mit dem [CreateManagedFolderResponse](createmanagedfolderresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-146">Start at the [CreateManagedFolderResponse](createmanagedfolderresponse.md) element.</span></span> 
  
## <a name="createmanagedfolder-error-response"></a><span data-ttu-id="ff0e6-147">CreateManagedFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="ff0e6-147">CreateManagedFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="ff0e6-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff0e6-148">Description</span></span>

<span data-ttu-id="ff0e6-149">Das folgende Codebeispiel zeigt eine Fehlerantwort auf eine CreateManagedFolder-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ff0e6-149">The following code example shows an error response to a CreateManagedFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="ff0e6-150">Code</span><span class="sxs-lookup"><span data-stu-id="ff0e6-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="ff0e6-151">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="ff0e6-151">Error response elements</span></span>

<span data-ttu-id="ff0e6-152">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="ff0e6-152">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="ff0e6-153">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ff0e6-153">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="ff0e6-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ff0e6-154">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ff0e6-155">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ff0e6-155">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="ff0e6-156">MessageText</span><span class="sxs-lookup"><span data-stu-id="ff0e6-156">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ff0e6-157">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff0e6-157">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff0e6-158">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ff0e6-158">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="ff0e6-159">Ordner</span><span class="sxs-lookup"><span data-stu-id="ff0e6-159">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="ff0e6-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff0e6-160">See also</span></span>



[<span data-ttu-id="ff0e6-161">GetFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ff0e6-161">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="ff0e6-162">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ff0e6-162">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="ff0e6-163">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="ff0e6-163">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="ff0e6-164">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="ff0e6-164">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

