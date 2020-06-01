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
description: Das FolderName-Element identifiziert einen einzelnen verwalteten benutzerdefinierten Ordner, der einem Postfach hinzugefügt werden soll.
ms.openlocfilehash: 1bb63e50c06e81337d1142a6624213fb2db12457
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461352"
---
# <a name="foldername"></a><span data-ttu-id="38d3e-103">FolderName</span><span class="sxs-lookup"><span data-stu-id="38d3e-103">FolderName</span></span>

<span data-ttu-id="38d3e-104">Das **FolderName** -Element identifiziert einen einzelnen verwalteten benutzerdefinierten Ordner, der einem Postfach hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38d3e-104">The **FolderName** element identifies a single managed custom folder to add to a mailbox.</span></span> 
  
[<span data-ttu-id="38d3e-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="38d3e-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="38d3e-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="38d3e-106">FolderNames</span></span>](foldernames.md)
  
[<span data-ttu-id="38d3e-107">FolderName</span><span class="sxs-lookup"><span data-stu-id="38d3e-107">FolderName</span></span>](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 <span data-ttu-id="38d3e-108">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="38d3e-108">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38d3e-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="38d3e-109">Attributes and elements</span></span>

<span data-ttu-id="38d3e-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="38d3e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38d3e-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="38d3e-111">Attributes</span></span>

<span data-ttu-id="38d3e-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="38d3e-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38d3e-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38d3e-113">Child elements</span></span>

<span data-ttu-id="38d3e-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="38d3e-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38d3e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38d3e-115">Parent elements</span></span>

|<span data-ttu-id="38d3e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="38d3e-116">**Element**</span></span>|<span data-ttu-id="38d3e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38d3e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38d3e-118">FolderNames</span><span class="sxs-lookup"><span data-stu-id="38d3e-118">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="38d3e-119">Enthält ein Array benannter verwalteter benutzerdefinierter Ordner, die einem Postfach hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="38d3e-119">Contains an array of named managed custom folders to add to a mailbox.</span></span>  <br/> <span data-ttu-id="38d3e-120">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="38d3e-120">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="38d3e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="38d3e-121">Text value</span></span>

<span data-ttu-id="38d3e-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="38d3e-122">A text value is required.</span></span> <span data-ttu-id="38d3e-123">Der Wert Text stellt einen Ordnernamen dar.</span><span class="sxs-lookup"><span data-stu-id="38d3e-123">The text value represents a folder name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38d3e-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38d3e-124">Remarks</span></span>

<span data-ttu-id="38d3e-125">Obwohl Sie Exchange Webdienste verwenden können, um einem Postfach verwaltete benutzerdefinierte Ordner hinzuzufügen, können Sie nicht dieselbe Technologie für den Zugriff auf die Liste der verfügbaren verwalteten benutzerdefinierten Ordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="38d3e-125">Although you can use Exchange Web Services to add managed custom folders to a mailbox, you cannot use the same technology to access the list of available managed custom folders.</span></span> <span data-ttu-id="38d3e-126">Sie können eine Liste verwalteter benutzerdefinierter Ordner abrufen, indem Sie einen Exchange-Verwaltungsshell-Befehl verwenden oder eine API verwenden, die mit dem Active Directory-Verzeichnisdienst Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="38d3e-126">You can obtain a list of managed custom folders by using an Exchange Management Shell command or by using an API that interfaces with the Active Directory directory service.</span></span> <span data-ttu-id="38d3e-127">Der Ordnername ist der Name des entsprechenden Active Directory-Objekts.</span><span class="sxs-lookup"><span data-stu-id="38d3e-127">The folder name is the name of the corresponding Active Directory object.</span></span>
  
<span data-ttu-id="38d3e-128">Sie können den [FindFolder-Vorgang](findfolder-operation.md) verwenden, um verwaltete benutzerdefinierte Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="38d3e-128">You can use the [FindFolder operation](findfolder-operation.md) to find managed custom folders.</span></span> <span data-ttu-id="38d3e-129">Verwenden Sie den [DeleteFolder-Vorgang](deletefolder-operation.md) , um verwaltete benutzerdefinierte Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="38d3e-129">Use the [DeleteFolder operation](deletefolder-operation.md) to delete managed custom folders.</span></span> 
  
<span data-ttu-id="38d3e-130">Es ist wichtig zu beachten, dass **FolderName** der Name eines vorhandenen verwalteten benutzerdefinierten Ordners in der Organisation ist.</span><span class="sxs-lookup"><span data-stu-id="38d3e-130">It is important to note that **FolderName** is the name of an existing managed custom folder in the organization.</span></span> <span data-ttu-id="38d3e-131">Ein Versuch, einen Ordner hinzuzufügen, der nicht in der Organisation liegt, führt zu einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="38d3e-131">An attempt to add a folder that is not in the organization will result in an error response.</span></span> 
  
<span data-ttu-id="38d3e-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="38d3e-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38d3e-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="38d3e-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38d3e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="38d3e-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38d3e-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="38d3e-135">Schema Name</span></span>  <br/> |<span data-ttu-id="38d3e-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="38d3e-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="38d3e-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="38d3e-137">Validation File</span></span>  <br/> |<span data-ttu-id="38d3e-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38d3e-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38d3e-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="38d3e-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="38d3e-140">False</span><span class="sxs-lookup"><span data-stu-id="38d3e-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38d3e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38d3e-141">See also</span></span>



[<span data-ttu-id="38d3e-142">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="38d3e-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="38d3e-143">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="38d3e-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="38d3e-144">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="38d3e-144">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

