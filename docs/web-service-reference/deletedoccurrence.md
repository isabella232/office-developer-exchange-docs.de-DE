---
title: DeletedOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedOccurrence
api_type:
- schema
ms.assetid: ff24ea15-0cd7-407d-a378-73ec16451870
description: Das Element DeletedOccurrence stellt eine gelöschte Vorkommen eines sich wiederholenden Kalenderelements.
ms.openlocfilehash: f12a2ba20f87f7803e492d8422b68c8ecdf9d797
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757910"
---
# <a name="deletedoccurrence"></a><span data-ttu-id="c8ae1-103">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="c8ae1-103">DeletedOccurrence</span></span>

<span data-ttu-id="c8ae1-104">Das Element **DeletedOccurrence** stellt eine gelöschte Vorkommen eines sich wiederholenden Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-104">The **DeletedOccurrence** element represents a deleted occurrence of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 <span data-ttu-id="c8ae1-105">**DeletedOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-105">**DeletedOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8ae1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ae1-106">Attributes and elements</span></span>

<span data-ttu-id="c8ae1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8ae1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c8ae1-108">Attributes</span></span>

<span data-ttu-id="c8ae1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8ae1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ae1-110">Child elements</span></span>

|<span data-ttu-id="c8ae1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-111">**Element**</span></span>|<span data-ttu-id="c8ae1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8ae1-113">Start</span><span class="sxs-lookup"><span data-stu-id="c8ae1-113">Start</span></span>](start.md) <br/> |<span data-ttu-id="c8ae1-114">Die Anfangszeit der einen gelöschten Vorkommen eines wiederkehrenden Kalenderelements darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-114">Represents the start time of a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8ae1-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ae1-115">Parent elements</span></span>

|<span data-ttu-id="c8ae1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-116">**Element**</span></span>|<span data-ttu-id="c8ae1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8ae1-118">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="c8ae1-118">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="c8ae1-119">Enthält ein Array von gelöschten Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-119">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8ae1-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8ae1-120">Remarks</span></span>

<span data-ttu-id="c8ae1-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8ae1-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c8ae1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8ae1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ae1-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8ae1-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c8ae1-124">Schema name</span></span>  <br/> |<span data-ttu-id="c8ae1-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c8ae1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8ae1-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c8ae1-126">Validation file</span></span>  <br/> |<span data-ttu-id="c8ae1-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8ae1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8ae1-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c8ae1-128">Can be empty</span></span>  <br/> |<span data-ttu-id="c8ae1-129">False</span><span class="sxs-lookup"><span data-stu-id="c8ae1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8ae1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ae1-130">See also</span></span>

- [<span data-ttu-id="c8ae1-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c8ae1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="c8ae1-132">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="c8ae1-132">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

