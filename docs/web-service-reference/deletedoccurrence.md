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
description: Das DeletedOccurrence-Element stellt ein gelöschtes Vorkommen eines wiederkehrenden Kalenderelements dar.
ms.openlocfilehash: 814a81934786963ae5e7ea3a40406834c27b64ce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457837"
---
# <a name="deletedoccurrence"></a><span data-ttu-id="b3c56-103">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="b3c56-103">DeletedOccurrence</span></span>

<span data-ttu-id="b3c56-104">Das **DeletedOccurrence** -Element stellt ein gelöschtes Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="b3c56-104">The **DeletedOccurrence** element represents a deleted occurrence of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 <span data-ttu-id="b3c56-105">**DeletedOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="b3c56-105">**DeletedOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3c56-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b3c56-106">Attributes and elements</span></span>

<span data-ttu-id="b3c56-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b3c56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3c56-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3c56-108">Attributes</span></span>

<span data-ttu-id="b3c56-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3c56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3c56-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3c56-110">Child elements</span></span>

|<span data-ttu-id="b3c56-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3c56-111">**Element**</span></span>|<span data-ttu-id="b3c56-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3c56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3c56-113">Start</span><span class="sxs-lookup"><span data-stu-id="b3c56-113">Start</span></span>](start.md) <br/> |<span data-ttu-id="b3c56-114">Stellt die Startzeit eines gelöschten Auftretens eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="b3c56-114">Represents the start time of a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3c56-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3c56-115">Parent elements</span></span>

|<span data-ttu-id="b3c56-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3c56-116">**Element**</span></span>|<span data-ttu-id="b3c56-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3c56-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3c56-118">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="b3c56-118">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="b3c56-119">Enthält ein Array von gelöschten Vorkommen eines wiederkehrenden Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="b3c56-119">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3c56-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3c56-120">Remarks</span></span>

<span data-ttu-id="b3c56-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b3c56-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3c56-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b3c56-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3c56-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3c56-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b3c56-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b3c56-124">Schema name</span></span>  <br/> |<span data-ttu-id="b3c56-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b3c56-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b3c56-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b3c56-126">Validation file</span></span>  <br/> |<span data-ttu-id="b3c56-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b3c56-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b3c56-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b3c56-128">Can be empty</span></span>  <br/> |<span data-ttu-id="b3c56-129">False</span><span class="sxs-lookup"><span data-stu-id="b3c56-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3c56-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3c56-130">See also</span></span>

- [<span data-ttu-id="b3c56-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b3c56-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="b3c56-132">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="b3c56-132">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

