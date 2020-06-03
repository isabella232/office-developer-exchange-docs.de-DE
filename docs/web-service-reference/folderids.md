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
description: Das FolderIds-Element enthält ein Array von Ordner Bezeichnern, mit denen Ordner identifiziert werden, die zum Kopieren, verlegen, abrufen, löschen oder Überwachen von Ereignisbenachrichtigungen verwendet werden.
ms.openlocfilehash: ff0476f72c7da088bd2b39f58ab560dcc82197e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530993"
---
# <a name="folderids"></a><span data-ttu-id="cc64a-103">FolderIds</span><span class="sxs-lookup"><span data-stu-id="cc64a-103">FolderIds</span></span>

<span data-ttu-id="cc64a-104">Das **FolderIds** -Element enthält ein Array von Ordner Bezeichnern, mit denen Ordner identifiziert werden, die zum Kopieren, verlegen, abrufen, löschen oder Überwachen von Ereignisbenachrichtigungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc64a-104">The **FolderIds** element contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications.</span></span> 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 <span data-ttu-id="cc64a-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="cc64a-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc64a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cc64a-106">Attributes and elements</span></span>

<span data-ttu-id="cc64a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cc64a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc64a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc64a-108">Attributes</span></span>

<span data-ttu-id="cc64a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc64a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc64a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc64a-110">Child elements</span></span>

|<span data-ttu-id="cc64a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc64a-111">**Element**</span></span>|<span data-ttu-id="cc64a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc64a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc64a-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="cc64a-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="cc64a-114">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="cc64a-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="cc64a-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="cc64a-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="cc64a-116">Identifiziert Exchange Server Ordner, auf die über den Namen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc64a-116">Identifies Microsoft Exchange Server folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cc64a-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc64a-117">Parent elements</span></span>

|<span data-ttu-id="cc64a-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc64a-118">**Element**</span></span>|<span data-ttu-id="cc64a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc64a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc64a-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="cc64a-120">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="cc64a-121">Definiert eine Anforderung zum Abrufen eines Ordners aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cc64a-121">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="cc64a-122">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/GetFolder`</span><span class="sxs-lookup"><span data-stu-id="cc64a-122">The following is the XPath expression to this element:  `/GetFolder`</span></span> <br/> |
|[<span data-ttu-id="cc64a-123">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="cc64a-123">DeleteFolder</span></span>](deletefolder.md) <br/> |<span data-ttu-id="cc64a-124">Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cc64a-124">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="cc64a-125">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/DeleteFolder`</span><span class="sxs-lookup"><span data-stu-id="cc64a-125">The following is the XPath expression to this element:  `/DeleteFolder`</span></span> <br/> |
|[<span data-ttu-id="cc64a-126">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="cc64a-126">EmptyFolder</span></span>](emptyfolder.md) <br/> |<span data-ttu-id="cc64a-127">Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cc64a-127">Defines a request to delete folders from the Exchange store.</span></span>  <br/> <span data-ttu-id="cc64a-128">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/EmptyFolder`</span><span class="sxs-lookup"><span data-stu-id="cc64a-128">The following is the XPath expression to this element:  `/EmptyFolder`</span></span> <br/> |
|[<span data-ttu-id="cc64a-129">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="cc64a-129">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="cc64a-130">Definiert eine Anforderung zum Migrieren eines Ordners in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cc64a-130">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="cc64a-131">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/MoveFolder`</span><span class="sxs-lookup"><span data-stu-id="cc64a-131">The following is the XPath expression to this element:  `/MoveFolder`</span></span> <br/> |
|[<span data-ttu-id="cc64a-132">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="cc64a-132">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="cc64a-133">Definiert eine Anforderung zum Kopieren eines Ordners in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cc64a-133">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="cc64a-134">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/CopyFolder`</span><span class="sxs-lookup"><span data-stu-id="cc64a-134">The following is the XPath expression to this element:  `/CopyFolder`</span></span> <br/> |
|[<span data-ttu-id="cc64a-135">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="cc64a-135">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="cc64a-136">Stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="cc64a-136">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="cc64a-137">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="cc64a-137">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="cc64a-138">Stellt ein Abonnement für ein Pull-basiertes Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="cc64a-138">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc64a-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc64a-139">Remarks</span></span>

<span data-ttu-id="cc64a-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cc64a-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc64a-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cc64a-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc64a-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc64a-142">Namespace</span></span>  <br/> |<span data-ttu-id="cc64a-143">https://schemas.microsoft.com/exchange/services/2006/messages und https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="cc64a-143">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="cc64a-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cc64a-144">Schema Name</span></span>  <br/> |<span data-ttu-id="cc64a-145">Nachrichtenschema; Typenschema</span><span class="sxs-lookup"><span data-stu-id="cc64a-145">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="cc64a-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cc64a-146">Validation File</span></span>  <br/> |<span data-ttu-id="cc64a-147">Messages. xsd; Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cc64a-147">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc64a-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cc64a-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc64a-149">False</span><span class="sxs-lookup"><span data-stu-id="cc64a-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc64a-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc64a-150">See also</span></span>



[<span data-ttu-id="cc64a-151">GetFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cc64a-151">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="cc64a-152">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cc64a-152">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="cc64a-153">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cc64a-153">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="cc64a-154">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cc64a-154">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="cc64a-155">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="cc64a-155">Subscribe operation</span></span>](subscribe-operation.md)

