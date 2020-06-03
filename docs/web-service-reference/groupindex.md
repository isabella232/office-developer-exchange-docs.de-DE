---
title: GroupIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIndex
api_type:
- schema
ms.assetid: 7a596ff7-6cc3-4626-a52c-538a92202337
description: Das GroupIndex-Element stellt den Eigenschaftswert dar, der zum Gruppieren von Elementen für die aktuelle Gruppe von Elementen in einem FindItem-Vorgangsaufruf verwendet wird.
ms.openlocfilehash: 05f303be92885a15dddf85c85251af04910d835c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530268"
---
# <a name="groupindex"></a><span data-ttu-id="f43c7-103">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="f43c7-103">GroupIndex</span></span>

<span data-ttu-id="f43c7-104">Das **GroupIndex** -Element stellt den Eigenschaftswert dar, der zum Gruppieren von Elementen für die aktuelle Gruppe von Elementen in einem [FindItem-Vorgangs](finditem-operation.md) Aufruf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f43c7-104">The **GroupIndex** element represents the property value that is used to group items for the current group of items in a [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="f43c7-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="f43c7-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="f43c7-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f43c7-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="f43c7-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f43c7-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="f43c7-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="f43c7-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="f43c7-109">Groups</span><span class="sxs-lookup"><span data-stu-id="f43c7-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="f43c7-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="f43c7-110">GroupedItems</span></span>](groupeditems.md)
  
[<span data-ttu-id="f43c7-111">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="f43c7-111">GroupIndex</span></span>](groupindex.md)
  
```xml
<GroupIndex/>
```

 <span data-ttu-id="f43c7-112">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f43c7-112">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f43c7-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f43c7-113">Attributes and elements</span></span>

<span data-ttu-id="f43c7-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f43c7-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f43c7-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="f43c7-115">Attributes</span></span>

<span data-ttu-id="f43c7-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="f43c7-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f43c7-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f43c7-117">Child elements</span></span>

<span data-ttu-id="f43c7-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="f43c7-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f43c7-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f43c7-119">Parent elements</span></span>

|<span data-ttu-id="f43c7-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="f43c7-120">**Element**</span></span>|<span data-ttu-id="f43c7-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f43c7-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f43c7-122">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="f43c7-122">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="f43c7-123">Stellt eine Auflistung von Elementen dar, die das Ergebnis eines Aufrufs einer gruppierten [FindItem-Operation](finditem-operation.md) sind.</span><span class="sxs-lookup"><span data-stu-id="f43c7-123">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> <span data-ttu-id="f43c7-124">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="f43c7-124">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItemResponse/ResponseMessages/FindItemResponseMessage/RootFolder/Groups/GroupedItems[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f43c7-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="f43c7-125">Text value</span></span>

<span data-ttu-id="f43c7-126">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f43c7-126">A text value is required.</span></span> <span data-ttu-id="f43c7-127">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f43c7-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f43c7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f43c7-128">Remarks</span></span>

<span data-ttu-id="f43c7-129">Dieses Element tritt nur in einer [FindItem-Vorgangs](finditem-operation.md) Antwort auf.</span><span class="sxs-lookup"><span data-stu-id="f43c7-129">This element only occurs in a [FindItem operation](finditem-operation.md) response.</span></span> 
  
<span data-ttu-id="f43c7-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f43c7-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f43c7-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f43c7-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f43c7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f43c7-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f43c7-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f43c7-133">Schema name</span></span>  <br/> |<span data-ttu-id="f43c7-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f43c7-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f43c7-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f43c7-135">Validation file</span></span>  <br/> |<span data-ttu-id="f43c7-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f43c7-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f43c7-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f43c7-137">Can be empty</span></span>  <br/> |<span data-ttu-id="f43c7-138">False</span><span class="sxs-lookup"><span data-stu-id="f43c7-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f43c7-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f43c7-139">See also</span></span>



[<span data-ttu-id="f43c7-140">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f43c7-140">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="f43c7-141">Suchen von Elementen</span><span class="sxs-lookup"><span data-stu-id="f43c7-141">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

