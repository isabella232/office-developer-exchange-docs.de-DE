---
title: CreateManagedFolder
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
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: Das CreateManagedFolder-Element definiert eine Anforderung zum Hinzufügen von verwalteter benutzerdefinierter Ordnern mit einem Postfach.
ms.openlocfilehash: 4acc931de2a8665db092c3b309d914f0a3c67558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757792"
---
# <a name="createmanagedfolder"></a><span data-ttu-id="8470d-103">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="8470d-103">CreateManagedFolder</span></span>

<span data-ttu-id="8470d-104">Das **CreateManagedFolder** -Element definiert eine Anforderung zum Hinzufügen von verwalteter benutzerdefinierter Ordnern mit einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="8470d-104">The **CreateManagedFolder** element defines a request to add managed custom folders to a mailbox.</span></span> 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 <span data-ttu-id="8470d-105">**CreateManagedFolderRequestType**</span><span class="sxs-lookup"><span data-stu-id="8470d-105">**CreateManagedFolderRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8470d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8470d-106">Attributes and elements</span></span>

<span data-ttu-id="8470d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8470d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8470d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8470d-108">Attributes</span></span>

<span data-ttu-id="8470d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8470d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8470d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8470d-110">Child elements</span></span>

|<span data-ttu-id="8470d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8470d-111">**Element**</span></span>|<span data-ttu-id="8470d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8470d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8470d-113">FolderNames</span><span class="sxs-lookup"><span data-stu-id="8470d-113">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="8470d-114">Enthält ein Array von benannten verwaltete Ordner ein Postfach hinzu.</span><span class="sxs-lookup"><span data-stu-id="8470d-114">Contains an array of named managed folders to add to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8470d-115">Postfach</span><span class="sxs-lookup"><span data-stu-id="8470d-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="8470d-116">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8470d-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8470d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8470d-117">Parent elements</span></span>

<span data-ttu-id="8470d-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="8470d-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8470d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8470d-119">Remarks</span></span>

<span data-ttu-id="8470d-120">Das Konto der Person ein, die die Anforderung stellt, muss FullAccess Berechtigungen für das Postfach verfügen, in dem die verwalteten Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8470d-120">The account of the person who is making the request must have FullAccess permissions on the mailbox where the managed folders are created.</span></span> <span data-ttu-id="8470d-121">Parameters _ _ - AccessRights können mit dem Exchange-Verwaltungsshell- **Add-MailboxPermission** -Cmdlet Sie die Berechtigung FullAccess zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8470d-121">You can use the _ -AccessRights _ parameter with the Exchange Management Shell **Add-MailboxPermission** cmdlet to assign the FullAccess permission.</span></span> 
  
<span data-ttu-id="8470d-122">Obwohl Sie Exchange-Webdienste Hinzufügens von verwalteten Ordnern mit einem Postfach verwenden können, können Exchange-Webdienste Sie die Liste der verwalteten Ordner zugreifen, die verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8470d-122">Although you can use Exchange Web Services to add managed folders to a mailbox, you cannot use Exchange Web Services to access the list of managed folders that are available.</span></span> <span data-ttu-id="8470d-123">Um eine Liste der verfügbaren verwalteten Ordner erhalten möchten, verwenden Sie das Cmdlet **Get-Managedfolder** Exchange-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="8470d-123">To obtain a list of available managed folders, use the **get-managedfolder** Exchange Management Shell cmdlet.</span></span> <span data-ttu-id="8470d-124">Verwalteten benutzerdefinierten Ordnern und verwalteten Standardordnern enthält die Liste, die vom **Cmdlet "Get-Managedfolder"** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8470d-124">The list that is returned by the **get-managedfolder cmdlet** will contain both managed custom folders and managed default folders.</span></span> <span data-ttu-id="8470d-125">Sie können nur Ordner des Typs **Managedcustomfolder** an das Postfach mit der Operation CreateManagedFolder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8470d-125">You can only add folders of type **managedcustomfolder** to the mailbox by using the CreateManagedFolder operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8470d-126">Eine Liste der verwalteten Ordner erhalten mithilfe der API Verzeichnisdienste von Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8470d-126">You can also get a list of managed folders by using the DirectoryServices API of the Microsoft .NET Framework.</span></span> 
  
<span data-ttu-id="8470d-127">Die [FindFolder Vorgang](findfolder-operation.md) können Sie verwaltete Ordner in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="8470d-127">You can use the [FindFolder operation](findfolder-operation.md) to find managed folders in a mailbox.</span></span> <span data-ttu-id="8470d-128">Verwaltete Ordner können unterschieden werden, indem Sie das [BaseShape](baseshape.md) -Element in der Anforderung auf AllProperties festlegen.</span><span class="sxs-lookup"><span data-stu-id="8470d-128">Managed folders can be distinguished by setting the [BaseShape](baseshape.md) element to AllProperties in the request.</span></span> <span data-ttu-id="8470d-129">Die Antwort enthält ein [ManagedFolderInformation](managedfolderinformation.md) -Element, um die verwalteten Ordner aus der Exchange-Speicherordner zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="8470d-129">The response will contain a [ManagedFolderInformation](managedfolderinformation.md) element to distinguish the managed folders from the Exchange store folders.</span></span> <span data-ttu-id="8470d-130">Sie können verwaltete Ordnern auf dieselbe Weise löschen, andere Ordnertypen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8470d-130">You can delete managed folders in the same manner that you delete other folder types.</span></span> 
  
<span data-ttu-id="8470d-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8470d-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8470d-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8470d-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8470d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8470d-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8470d-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8470d-134">Schema Name</span></span>  <br/> |<span data-ttu-id="8470d-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8470d-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8470d-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8470d-136">Validation File</span></span>  <br/> |<span data-ttu-id="8470d-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8470d-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8470d-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8470d-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="8470d-139">False</span><span class="sxs-lookup"><span data-stu-id="8470d-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8470d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8470d-140">See also</span></span>



[<span data-ttu-id="8470d-141">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8470d-141">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
  
[<span data-ttu-id="8470d-142">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8470d-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="8470d-143">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="8470d-143">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="8470d-144">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="8470d-144">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

