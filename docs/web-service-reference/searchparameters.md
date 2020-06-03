---
title: SearchParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchParameters
api_type:
- schema
ms.assetid: 34602cb1-dc33-4552-a98c-3e77f614daa3
description: Das SearchParameters-Element stellt die Parameter dar, die einen Suchordner definieren.
ms.openlocfilehash: cd9f255621b17d01113392e67a0301b01b70f326
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466668"
---
# <a name="searchparameters"></a><span data-ttu-id="a553b-103">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="a553b-103">SearchParameters</span></span>

<span data-ttu-id="a553b-104">Das **SearchParameters** -Element stellt die Parameter dar, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="a553b-104">The **SearchParameters** element represents the parameters that define a search folder.</span></span> 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 <span data-ttu-id="a553b-105">**SearchParametersType**</span><span class="sxs-lookup"><span data-stu-id="a553b-105">**SearchParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a553b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a553b-106">Attributes and elements</span></span>

<span data-ttu-id="a553b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a553b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a553b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a553b-108">Attributes</span></span>

|<span data-ttu-id="a553b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a553b-109">**Attribute**</span></span>|<span data-ttu-id="a553b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a553b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a553b-111">**Traversal**</span><span class="sxs-lookup"><span data-stu-id="a553b-111">**Traversal**</span></span> <br/> |<span data-ttu-id="a553b-112">Beschreibt, wie ein Suchordner die Ordnerhierarchie durchläuft.</span><span class="sxs-lookup"><span data-stu-id="a553b-112">Describes how a search folder traverses the folder hierarchy.</span></span> <span data-ttu-id="a553b-113">Die Optionen sind sowohl für eine **Tiefe** als auch für eine **flache** Suche.</span><span class="sxs-lookup"><span data-stu-id="a553b-113">The options are for either a **Deep** or a **Shallow** search.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a553b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a553b-114">Child elements</span></span>

|<span data-ttu-id="a553b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a553b-115">**Element**</span></span>|<span data-ttu-id="a553b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a553b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a553b-117">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="a553b-117">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="a553b-118">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a553b-118">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="a553b-119">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="a553b-119">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="a553b-120">Stellt die Auflistung von Ordnern dar, die abgebaut werden, um den Inhalt eines Suchordners zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a553b-120">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a553b-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a553b-121">Parent elements</span></span>

|<span data-ttu-id="a553b-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="a553b-122">**Element**</span></span>|<span data-ttu-id="a553b-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a553b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a553b-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a553b-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="a553b-125">Stellt einen Suchordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a553b-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a553b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a553b-126">Remarks</span></span>

<span data-ttu-id="a553b-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a553b-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a553b-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a553b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a553b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a553b-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a553b-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a553b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="a553b-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a553b-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a553b-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a553b-132">Validation File</span></span>  <br/> |<span data-ttu-id="a553b-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a553b-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a553b-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a553b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a553b-135">False</span><span class="sxs-lookup"><span data-stu-id="a553b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a553b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a553b-136">See also</span></span>



- [<span data-ttu-id="a553b-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a553b-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

