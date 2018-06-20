---
title: BaseFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseFolderIds
api_type:
- schema
ms.assetid: bdaa6093-f960-469a-b338-0e75aaa536c6
description: Das Element BaseFolderIds stellt die Auflistung von Ordnern, die durchsucht werden wird, um den Inhalt des ein Suchordner bestimmen.
ms.openlocfilehash: 960e4d9c1d6eb37bf988bf163e696cbba3e1ef6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757424"
---
# <a name="basefolderids"></a><span data-ttu-id="871a4-103">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="871a4-103">BaseFolderIds</span></span>

<span data-ttu-id="871a4-104">Das Element **BaseFolderIds** stellt die Auflistung von Ordnern, die durchsucht werden wird, um den Inhalt des ein Suchordner bestimmen.</span><span class="sxs-lookup"><span data-stu-id="871a4-104">The **BaseFolderIds** element represents the collection of folders that will be mined to determine the contents of a search folder.</span></span> 
  
```xml
<BaseFolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</BaseFolderIds>
```

 <span data-ttu-id="871a4-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="871a4-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="871a4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="871a4-106">Attributes and elements</span></span>

<span data-ttu-id="871a4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="871a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="871a4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="871a4-108">Attributes</span></span>

<span data-ttu-id="871a4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="871a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="871a4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="871a4-110">Child elements</span></span>

|<span data-ttu-id="871a4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="871a4-111">**Element**</span></span>|<span data-ttu-id="871a4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="871a4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="871a4-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="871a4-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="871a4-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="871a4-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="871a4-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="871a4-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="871a4-116">Identifiziert MicrosoftExchange Server 2007-Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="871a4-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="871a4-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="871a4-117">Parent elements</span></span>

|<span data-ttu-id="871a4-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="871a4-118">**Element**</span></span>|<span data-ttu-id="871a4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="871a4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="871a4-120">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="871a4-120">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="871a4-121">Stellt die Parameter, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="871a4-121">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="871a4-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="871a4-122">Remarks</span></span>

<span data-ttu-id="871a4-123">Das **BaseFolderIds** -Element muss mindestens ein [FolderId](folderid.md) oder [DistinguishedFolderId](distinguishedfolderid.md) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="871a4-123">The **BaseFolderIds** element must contain at least one [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="871a4-124">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="871a4-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="871a4-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="871a4-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="871a4-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="871a4-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="871a4-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="871a4-127">Schema name</span></span>  <br/> |<span data-ttu-id="871a4-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="871a4-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="871a4-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="871a4-129">Validation file</span></span>  <br/> |<span data-ttu-id="871a4-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="871a4-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="871a4-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="871a4-131">Can be empty</span></span>  <br/> |<span data-ttu-id="871a4-132">False</span><span class="sxs-lookup"><span data-stu-id="871a4-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="871a4-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="871a4-133">See also</span></span>



- [<span data-ttu-id="871a4-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="871a4-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

