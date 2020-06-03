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
description: Das CreateManagedFolder-Element definiert eine Anforderung zum Hinzufügen verwalteter benutzerdefinierter Ordner zu einem Postfach.
ms.openlocfilehash: 01fe8b7341c38ad33089c56271434ad3f9a4e5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458362"
---
# <a name="createmanagedfolder"></a><span data-ttu-id="359d0-103">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="359d0-103">CreateManagedFolder</span></span>

<span data-ttu-id="359d0-104">Das **CreateManagedFolder** -Element definiert eine Anforderung zum Hinzufügen verwalteter benutzerdefinierter Ordner zu einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="359d0-104">The **CreateManagedFolder** element defines a request to add managed custom folders to a mailbox.</span></span> 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 <span data-ttu-id="359d0-105">**CreateManagedFolderRequestType**</span><span class="sxs-lookup"><span data-stu-id="359d0-105">**CreateManagedFolderRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="359d0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="359d0-106">Attributes and elements</span></span>

<span data-ttu-id="359d0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="359d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="359d0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="359d0-108">Attributes</span></span>

<span data-ttu-id="359d0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="359d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="359d0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="359d0-110">Child elements</span></span>

|<span data-ttu-id="359d0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="359d0-111">**Element**</span></span>|<span data-ttu-id="359d0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="359d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="359d0-113">FolderNames</span><span class="sxs-lookup"><span data-stu-id="359d0-113">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="359d0-114">Enthält ein Array benannter verwalteter Ordner, die einem Postfach hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="359d0-114">Contains an array of named managed folders to add to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="359d0-115">Postfach</span><span class="sxs-lookup"><span data-stu-id="359d0-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="359d0-116">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="359d0-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="359d0-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="359d0-117">Parent elements</span></span>

<span data-ttu-id="359d0-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="359d0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="359d0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="359d0-119">Remarks</span></span>

<span data-ttu-id="359d0-120">Das Konto der Person, die die Anforderung macht, muss über FullAccess-Berechtigungen für das Postfach verfügen, in dem die verwalteten Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="359d0-120">The account of the person who is making the request must have FullAccess permissions on the mailbox where the managed folders are created.</span></span> <span data-ttu-id="359d0-121">Sie können den _-AccessRights _-Parameter mit dem Exchange-Verwaltungsshell **Add-MailboxPermission-** Cmdlet verwenden, um die FullAccess-Berechtigung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="359d0-121">You can use the _ -AccessRights _ parameter with the Exchange Management Shell **Add-MailboxPermission** cmdlet to assign the FullAccess permission.</span></span> 
  
<span data-ttu-id="359d0-122">Obwohl Sie Exchange Webdienste verwenden können, um einem Postfach verwaltete Ordner hinzuzufügen, können Sie Exchange Webdienste nicht verwenden, um auf die Liste der verfügbaren verwalteten Ordner zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="359d0-122">Although you can use Exchange Web Services to add managed folders to a mailbox, you cannot use Exchange Web Services to access the list of managed folders that are available.</span></span> <span data-ttu-id="359d0-123">Um eine Liste der verfügbaren verwalteten Ordner zu erhalten, verwenden Sie das Cmdlet **Get-ManagedFolder** Exchange-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="359d0-123">To obtain a list of available managed folders, use the **get-managedfolder** Exchange Management Shell cmdlet.</span></span> <span data-ttu-id="359d0-124">Die Liste, die vom **Cmdlet Get-ManagedFolder** zurückgegeben wird, enthält sowohl verwaltete benutzerdefinierte Ordner als auch verwaltete Standardordner.</span><span class="sxs-lookup"><span data-stu-id="359d0-124">The list that is returned by the **get-managedfolder cmdlet** will contain both managed custom folders and managed default folders.</span></span> <span data-ttu-id="359d0-125">Sie können dem Postfach nur Ordner vom Typ **ManagedCustomFolder** hinzufügen, indem Sie den CreateManagedFolder-Vorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="359d0-125">You can only add folders of type **managedcustomfolder** to the mailbox by using the CreateManagedFolder operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="359d0-126">Sie können auch eine Liste der verwalteten Ordner abrufen, indem Sie die DirectoryServices-API des Microsoft .NET Framework verwenden.</span><span class="sxs-lookup"><span data-stu-id="359d0-126">You can also get a list of managed folders by using the DirectoryServices API of the Microsoft .NET Framework.</span></span> 
  
<span data-ttu-id="359d0-127">Sie können den [FindFolder-Vorgang](findfolder-operation.md) verwenden, um verwaltete Ordner in einem Postfach zu suchen.</span><span class="sxs-lookup"><span data-stu-id="359d0-127">You can use the [FindFolder operation](findfolder-operation.md) to find managed folders in a mailbox.</span></span> <span data-ttu-id="359d0-128">Verwaltete Ordner können unterschieden werden, indem das [BaseShape](baseshape.md) -Element auf allproperties in der Anforderung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="359d0-128">Managed folders can be distinguished by setting the [BaseShape](baseshape.md) element to AllProperties in the request.</span></span> <span data-ttu-id="359d0-129">Die Antwort enthält ein [ManagedFolderInformation](managedfolderinformation.md) -Element, um die verwalteten Ordner von den Exchange-Informationsspeicher Ordnern zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="359d0-129">The response will contain a [ManagedFolderInformation](managedfolderinformation.md) element to distinguish the managed folders from the Exchange store folders.</span></span> <span data-ttu-id="359d0-130">Sie können verwaltete Ordner auf die gleiche Weise löschen, wie Sie andere Ordnertypen löschen.</span><span class="sxs-lookup"><span data-stu-id="359d0-130">You can delete managed folders in the same manner that you delete other folder types.</span></span> 
  
<span data-ttu-id="359d0-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="359d0-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="359d0-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="359d0-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="359d0-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="359d0-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="359d0-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="359d0-134">Schema Name</span></span>  <br/> |<span data-ttu-id="359d0-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="359d0-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="359d0-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="359d0-136">Validation File</span></span>  <br/> |<span data-ttu-id="359d0-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="359d0-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="359d0-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="359d0-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="359d0-139">False</span><span class="sxs-lookup"><span data-stu-id="359d0-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="359d0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="359d0-140">See also</span></span>



[<span data-ttu-id="359d0-141">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="359d0-141">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
  
[<span data-ttu-id="359d0-142">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="359d0-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="359d0-143">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="359d0-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="359d0-144">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="359d0-144">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

