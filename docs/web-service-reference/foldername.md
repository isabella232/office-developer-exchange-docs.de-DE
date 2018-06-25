---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: FolderName-Element gibt einen einzelnen verwalteten benutzerdefinierten Ordner ein Postfach hinzu.
ms.openlocfilehash: 56a7a7d256624c5103c88a333222807519d21501
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758513"
---
# <a name="foldername"></a><span data-ttu-id="ffab4-103">FolderName</span><span class="sxs-lookup"><span data-stu-id="ffab4-103">FolderName</span></span>

<span data-ttu-id="ffab4-104">**FolderName** -Element gibt einen einzelnen verwalteten benutzerdefinierten Ordner ein Postfach hinzu.</span><span class="sxs-lookup"><span data-stu-id="ffab4-104">The **FolderName** element identifies a single managed custom folder to add to a mailbox.</span></span> 
  
[<span data-ttu-id="ffab4-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="ffab4-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="ffab4-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="ffab4-106">FolderNames</span></span>](foldernames.md)
  
[<span data-ttu-id="ffab4-107">Ordnername</span><span class="sxs-lookup"><span data-stu-id="ffab4-107">FolderName</span></span>](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 <span data-ttu-id="ffab4-108">**string**</span><span class="sxs-lookup"><span data-stu-id="ffab4-108">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffab4-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ffab4-109">Attributes and elements</span></span>

<span data-ttu-id="ffab4-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ffab4-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffab4-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ffab4-111">Attributes</span></span>

<span data-ttu-id="ffab4-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="ffab4-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ffab4-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffab4-113">Child elements</span></span>

<span data-ttu-id="ffab4-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="ffab4-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ffab4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffab4-115">Parent elements</span></span>

|<span data-ttu-id="ffab4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffab4-116">**Element**</span></span>|<span data-ttu-id="ffab4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffab4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffab4-118">FolderNames</span><span class="sxs-lookup"><span data-stu-id="ffab4-118">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="ffab4-119">Enthält ein Array von benannten verwalteten benutzerdefinierten Ordnern an ein Postfach hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ffab4-119">Contains an array of named managed custom folders to add to a mailbox.</span></span>  <br/> <span data-ttu-id="ffab4-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="ffab4-120">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ffab4-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="ffab4-121">Text value</span></span>

<span data-ttu-id="ffab4-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ffab4-122">A text value is required.</span></span> <span data-ttu-id="ffab4-123">Der Textwert stellt einen Ordnernamen.</span><span class="sxs-lookup"><span data-stu-id="ffab4-123">The text value represents a folder name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffab4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffab4-124">Remarks</span></span>

<span data-ttu-id="ffab4-125">Obwohl Sie Exchange-Webdienste zum Hinzufügen von verwalteter benutzerdefinierter Ordnern mit einem Postfach verwenden können, können die gleiche Technologie Sie die Liste der verfügbaren verwalteten benutzerdefinierten Ordnern zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ffab4-125">Although you can use Exchange Web Services to add managed custom folders to a mailbox, you cannot use the same technology to access the list of available managed custom folders.</span></span> <span data-ttu-id="ffab4-126">Sie können eine Liste der verwalteten benutzerdefinierten Ordnern abrufen, mit einer Exchange-Verwaltungsshell-Befehl oder mithilfe einer API, die Schnittstellen mit dem Active Directory-Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="ffab4-126">You can obtain a list of managed custom folders by using an Exchange Management Shell command or by using an API that interfaces with the Active Directory directory service.</span></span> <span data-ttu-id="ffab4-127">Der Name des Ordners ist der Name des entsprechenden Active Directory-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ffab4-127">The folder name is the name of the corresponding Active Directory object.</span></span>
  
<span data-ttu-id="ffab4-128">Die [FindFolder Vorgang](findfolder-operation.md) können Sie verwaltete benutzerdefinierte Ordnern suchen.</span><span class="sxs-lookup"><span data-stu-id="ffab4-128">You can use the [FindFolder operation](findfolder-operation.md) to find managed custom folders.</span></span> <span data-ttu-id="ffab4-129">Verwendung der [DeleteFolder-Vorgang](deletefolder-operation.md) zum Löschen verwalteten benutzerdefinierte Ordnern.</span><span class="sxs-lookup"><span data-stu-id="ffab4-129">Use the [DeleteFolder operation](deletefolder-operation.md) to delete managed custom folders.</span></span> 
  
<span data-ttu-id="ffab4-130">Es ist wichtig, beachten Sie, dass der **Ordnername** der Name eines vorhandenen verwalteten benutzerdefinierten Ordners in der Organisation ist.</span><span class="sxs-lookup"><span data-stu-id="ffab4-130">It is important to note that **FolderName** is the name of an existing managed custom folder in the organization.</span></span> <span data-ttu-id="ffab4-131">Sie versuchen, einen Ordner hinzuzufügen, der nicht in der Organisation ist führt eine Fehlerantwort.</span><span class="sxs-lookup"><span data-stu-id="ffab4-131">An attempt to add a folder that is not in the organization will result in an error response.</span></span> 
  
<span data-ttu-id="ffab4-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ffab4-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffab4-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ffab4-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffab4-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffab4-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ffab4-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ffab4-135">Schema Name</span></span>  <br/> |<span data-ttu-id="ffab4-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ffab4-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="ffab4-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ffab4-137">Validation File</span></span>  <br/> |<span data-ttu-id="ffab4-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ffab4-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ffab4-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ffab4-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="ffab4-140">False</span><span class="sxs-lookup"><span data-stu-id="ffab4-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffab4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffab4-141">See also</span></span>



[<span data-ttu-id="ffab4-142">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="ffab4-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="ffab4-143">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="ffab4-143">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="ffab4-144">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="ffab4-144">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

