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
description: Das BaseFolderIds-Element stellt die Auflistung von Ordnern dar, die abgebaut werden, um den Inhalt eines Suchordners zu bestimmen.
ms.openlocfilehash: 97159ec1ded685e63aafedfaf90a06eff39adaab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460267"
---
# <a name="basefolderids"></a><span data-ttu-id="44aaa-103">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="44aaa-103">BaseFolderIds</span></span>

<span data-ttu-id="44aaa-104">Das **BaseFolderIds** -Element stellt die Auflistung von Ordnern dar, die abgebaut werden, um den Inhalt eines Suchordners zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="44aaa-104">The **BaseFolderIds** element represents the collection of folders that will be mined to determine the contents of a search folder.</span></span> 
  
```xml
<BaseFolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</BaseFolderIds>
```

 <span data-ttu-id="44aaa-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="44aaa-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44aaa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="44aaa-106">Attributes and elements</span></span>

<span data-ttu-id="44aaa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="44aaa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44aaa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="44aaa-108">Attributes</span></span>

<span data-ttu-id="44aaa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="44aaa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44aaa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44aaa-110">Child elements</span></span>

|<span data-ttu-id="44aaa-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="44aaa-111">**Element**</span></span>|<span data-ttu-id="44aaa-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44aaa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44aaa-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="44aaa-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="44aaa-114">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="44aaa-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="44aaa-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="44aaa-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="44aaa-116">Identifiziert Microsoft Exchange Server 2007-Ordner, auf die über den Namen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="44aaa-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44aaa-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44aaa-117">Parent elements</span></span>

|<span data-ttu-id="44aaa-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="44aaa-118">**Element**</span></span>|<span data-ttu-id="44aaa-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44aaa-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44aaa-120">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="44aaa-120">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="44aaa-121">Stellt die Parameter dar, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="44aaa-121">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44aaa-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44aaa-122">Remarks</span></span>

<span data-ttu-id="44aaa-123">Das **BaseFolderIds** -Element muss mindestens ein [Folder](folderid.md) -oder [DistinguishedFolderId](distinguishedfolderid.md) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="44aaa-123">The **BaseFolderIds** element must contain at least one [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="44aaa-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="44aaa-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44aaa-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="44aaa-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44aaa-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="44aaa-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44aaa-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="44aaa-127">Schema name</span></span>  <br/> |<span data-ttu-id="44aaa-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="44aaa-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="44aaa-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="44aaa-129">Validation file</span></span>  <br/> |<span data-ttu-id="44aaa-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="44aaa-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44aaa-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="44aaa-131">Can be empty</span></span>  <br/> |<span data-ttu-id="44aaa-132">False</span><span class="sxs-lookup"><span data-stu-id="44aaa-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44aaa-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44aaa-133">See also</span></span>



- [<span data-ttu-id="44aaa-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="44aaa-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

