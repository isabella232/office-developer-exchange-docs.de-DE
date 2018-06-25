---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: Das FolderIds-Element enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der Ordner kopieren, verschieben, abrufen, löschen oder Überwachen von Ereignissen verwendet werden.
ms.openlocfilehash: 911a74ca778ee988c270c16c67620a40656d82d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758507"
---
# <a name="folderids"></a><span data-ttu-id="a4579-103">FolderIds</span><span class="sxs-lookup"><span data-stu-id="a4579-103">FolderIds</span></span>

<span data-ttu-id="a4579-104">Das **FolderIds** -Element enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der Ordner kopieren, verschieben, abrufen, löschen oder Überwachen von Ereignissen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4579-104">The **FolderIds** element contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications.</span></span> 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 <span data-ttu-id="a4579-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="a4579-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4579-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a4579-106">Attributes and elements</span></span>

<span data-ttu-id="a4579-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a4579-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4579-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a4579-108">Attributes</span></span>

<span data-ttu-id="a4579-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a4579-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4579-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4579-110">Child elements</span></span>

|<span data-ttu-id="a4579-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4579-111">**Element**</span></span>|<span data-ttu-id="a4579-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4579-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4579-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="a4579-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a4579-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="a4579-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="a4579-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a4579-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="a4579-116">Identifiziert die Microsoft Exchange Server-Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="a4579-116">Identifies Microsoft Exchange Server folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a4579-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4579-117">Parent elements</span></span>

|<span data-ttu-id="a4579-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4579-118">**Element**</span></span>|<span data-ttu-id="a4579-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4579-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4579-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="a4579-120">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="a4579-121">Definiert eine Anforderung an einen Ordner aus dem Exchange-Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a4579-121">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="a4579-122">Es folgt der XPath-Ausdruck, der dieses Element:`/GetFolder`</span><span class="sxs-lookup"><span data-stu-id="a4579-122">The following is the XPath expression to this element:  `/GetFolder`</span></span> <br/> |
|[<span data-ttu-id="a4579-123">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="a4579-123">DeleteFolder</span></span>](deletefolder.md) <br/> |<span data-ttu-id="a4579-124">Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a4579-124">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="a4579-125">Es folgt der XPath-Ausdruck, der dieses Element:`/DeleteFolder`</span><span class="sxs-lookup"><span data-stu-id="a4579-125">The following is the XPath expression to this element:  `/DeleteFolder`</span></span> <br/> |
|[<span data-ttu-id="a4579-126">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="a4579-126">EmptyFolder</span></span>](emptyfolder.md) <br/> |<span data-ttu-id="a4579-127">Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a4579-127">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="a4579-128">Es folgt der XPath-Ausdruck, der dieses Element:`/EmptyFolder`</span><span class="sxs-lookup"><span data-stu-id="a4579-128">The following is the XPath expression to this element:  `/EmptyFolder`</span></span> <br/> |
|[<span data-ttu-id="a4579-129">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="a4579-129">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="a4579-130">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="a4579-130">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="a4579-131">Es folgt der XPath-Ausdruck, der dieses Element:`/MoveFolder`</span><span class="sxs-lookup"><span data-stu-id="a4579-131">The following is the XPath expression to this element:  `/MoveFolder`</span></span> <br/> |
|[<span data-ttu-id="a4579-132">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="a4579-132">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="a4579-133">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="a4579-133">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="a4579-134">Es folgt der XPath-Ausdruck, der dieses Element:`/CopyFolder`</span><span class="sxs-lookup"><span data-stu-id="a4579-134">The following is the XPath expression to this element:  `/CopyFolder`</span></span> <br/> |
|[<span data-ttu-id="a4579-135">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a4579-135">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="a4579-136">Stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a4579-136">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="a4579-137">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a4579-137">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="a4579-138">Stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a4579-138">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4579-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4579-139">Remarks</span></span>

<span data-ttu-id="a4579-140">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a4579-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4579-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a4579-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4579-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4579-142">Namespace</span></span>  <br/> |<span data-ttu-id="a4579-143">http://schemas.microsoft.com/exchange/services/2006/messages und http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="a4579-143">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="a4579-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a4579-144">Schema Name</span></span>  <br/> |<span data-ttu-id="a4579-145">Nachrichten-schema Typen-schema</span><span class="sxs-lookup"><span data-stu-id="a4579-145">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="a4579-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a4579-146">Validation File</span></span>  <br/> |<span data-ttu-id="a4579-147">Messages.xsd; Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a4579-147">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a4579-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a4579-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4579-149">False</span><span class="sxs-lookup"><span data-stu-id="a4579-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4579-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4579-150">See also</span></span>



[<span data-ttu-id="a4579-151">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="a4579-151">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="a4579-152">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a4579-152">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="a4579-153">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a4579-153">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="a4579-154">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a4579-154">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="a4579-155">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="a4579-155">Subscribe operation</span></span>](subscribe-operation.md)

