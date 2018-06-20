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
description: Das SearchParameters-Element darstellt, Parameter, die einen Suchordner definieren.
ms.openlocfilehash: b534574a1292d78c8df99f5186990b114fc4e70a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831299"
---
# <a name="searchparameters"></a><span data-ttu-id="aed5d-103">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="aed5d-103">SearchParameters</span></span>

<span data-ttu-id="aed5d-104">Das **SearchParameters** -Element darstellt, Parameter, die einen Suchordner definieren.</span><span class="sxs-lookup"><span data-stu-id="aed5d-104">The **SearchParameters** element represents the parameters that define a search folder.</span></span> 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 <span data-ttu-id="aed5d-105">**SearchParametersType**</span><span class="sxs-lookup"><span data-stu-id="aed5d-105">**SearchParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aed5d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aed5d-106">Attributes and elements</span></span>

<span data-ttu-id="aed5d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aed5d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aed5d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="aed5d-108">Attributes</span></span>

|<span data-ttu-id="aed5d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aed5d-109">**Attribute**</span></span>|<span data-ttu-id="aed5d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aed5d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aed5d-111">**Durchqueren**</span><span class="sxs-lookup"><span data-stu-id="aed5d-111">**Traversal**</span></span> <br/> |<span data-ttu-id="aed5d-112">Beschreibt, wie ein Suchordner Ordnerhierarchie durchläuft.</span><span class="sxs-lookup"><span data-stu-id="aed5d-112">Describes how a search folder traverses the folder hierarchy.</span></span> <span data-ttu-id="aed5d-113">Die Optionen sind für die **Tiefe** oder eine **flache** Suche.</span><span class="sxs-lookup"><span data-stu-id="aed5d-113">The options are for either a **Deep** or a **Shallow** search.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aed5d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aed5d-114">Child elements</span></span>

|<span data-ttu-id="aed5d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="aed5d-115">**Element**</span></span>|<span data-ttu-id="aed5d-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aed5d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aed5d-117">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="aed5d-117">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="aed5d-118">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aed5d-118">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="aed5d-119">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="aed5d-119">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="aed5d-120">Stellt die Auflistung von Ordnern, die durchsucht werden wird, um den Inhalt des ein Suchordner bestimmen.</span><span class="sxs-lookup"><span data-stu-id="aed5d-120">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aed5d-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aed5d-121">Parent elements</span></span>

|<span data-ttu-id="aed5d-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="aed5d-122">**Element**</span></span>|<span data-ttu-id="aed5d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aed5d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aed5d-124">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="aed5d-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="aed5d-125">Stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="aed5d-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aed5d-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aed5d-126">Remarks</span></span>

<span data-ttu-id="aed5d-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="aed5d-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aed5d-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="aed5d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aed5d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="aed5d-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aed5d-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aed5d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="aed5d-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="aed5d-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="aed5d-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aed5d-132">Validation File</span></span>  <br/> |<span data-ttu-id="aed5d-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aed5d-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aed5d-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="aed5d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="aed5d-135">False</span><span class="sxs-lookup"><span data-stu-id="aed5d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aed5d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aed5d-136">See also</span></span>



- [<span data-ttu-id="aed5d-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="aed5d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

