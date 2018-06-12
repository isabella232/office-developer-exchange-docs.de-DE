---
title: DueDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DueDate
api_type:
- schema
ms.assetid: dd9b6c43-a512-4b3b-a071-4abde02ed55f
description: DueDate-Element darstellt, das Datum, an das ein Element fällig ist.
ms.openlocfilehash: b24891972f240bc6ee5d0fe868445b96abdc089a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758111"
---
# <a name="duedate"></a><span data-ttu-id="5c554-103">DueDate</span><span class="sxs-lookup"><span data-stu-id="5c554-103">DueDate</span></span>

<span data-ttu-id="5c554-104">**DueDate** -Element darstellt, das Datum, an das ein Element fällig ist.</span><span class="sxs-lookup"><span data-stu-id="5c554-104">The **DueDate** element represents the date an item is due.</span></span> 
  
```xml
<DueDate/>
```

 <span data-ttu-id="5c554-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="5c554-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c554-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5c554-106">Attributes and elements</span></span>

<span data-ttu-id="5c554-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5c554-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c554-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c554-108">Attributes</span></span>

<span data-ttu-id="5c554-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c554-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c554-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c554-110">Child elements</span></span>

<span data-ttu-id="5c554-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c554-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c554-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c554-112">Parent elements</span></span>

|<span data-ttu-id="5c554-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c554-113">**Element**</span></span>|<span data-ttu-id="5c554-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c554-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c554-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="5c554-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="5c554-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5c554-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5c554-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5c554-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="5c554-118">Gibt ein Flag für ein Postfach-Element an.</span><span class="sxs-lookup"><span data-stu-id="5c554-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c554-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="5c554-119">Text value</span></span>

<span data-ttu-id="5c554-120">Ein Textwert, der Datum und Uhrzeit darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c554-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c554-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c554-121">Remarks</span></span>

<span data-ttu-id="5c554-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5c554-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c554-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5c554-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c554-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c554-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c554-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5c554-125">Schema name</span></span>  <br/> |<span data-ttu-id="5c554-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5c554-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c554-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5c554-127">Validation file</span></span>  <br/> |<span data-ttu-id="5c554-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c554-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c554-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5c554-129">Can be empty</span></span>  <br/> |<span data-ttu-id="5c554-130">False</span><span class="sxs-lookup"><span data-stu-id="5c554-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c554-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c554-131">See also</span></span>

- [<span data-ttu-id="5c554-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5c554-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

