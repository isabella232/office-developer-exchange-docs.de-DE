---
title: Companies
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Companies
api_type:
- schema
ms.assetid: 5d9ea76f-e14d-4424-8842-0c3cc3305119
description: Das Unternehmen Element stellt die Auflistung der Unternehmen, die einen Kontakt oder eine Aufgabe zugeordnet sind.
ms.openlocfilehash: 5b8ac20d4a02017881f941d12380fe29078f51cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757574"
---
# <a name="companies"></a><span data-ttu-id="617a9-103">Companies</span><span class="sxs-lookup"><span data-stu-id="617a9-103">Companies</span></span>

<span data-ttu-id="617a9-104">Das **Unternehmen** Element stellt die Auflistung der Unternehmen, die einen Kontakt oder eine Aufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="617a9-104">The **Companies** element represents the collection of companies that are associated with a contact or task.</span></span> 
  
```xml
<Companies>
   <String/>
</Companies>
```

 <span data-ttu-id="617a9-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="617a9-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="617a9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="617a9-106">Attributes and elements</span></span>

<span data-ttu-id="617a9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="617a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="617a9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="617a9-108">Attributes</span></span>

<span data-ttu-id="617a9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="617a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="617a9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="617a9-110">Child elements</span></span>

|<span data-ttu-id="617a9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="617a9-111">**Element**</span></span>|<span data-ttu-id="617a9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="617a9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="617a9-113">String</span><span class="sxs-lookup"><span data-stu-id="617a9-113">String</span></span>](string.md) <br/> |<span data-ttu-id="617a9-114">Stellt den Namen eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="617a9-114">Represents the name of a company.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="617a9-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="617a9-115">Parent elements</span></span>

|<span data-ttu-id="617a9-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="617a9-116">**Element**</span></span>|<span data-ttu-id="617a9-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="617a9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="617a9-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="617a9-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="617a9-119">Stellt einen Kontakt in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="617a9-119">Represents a contact in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="617a9-120">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="617a9-120">Task</span></span>](task.md) <br/> |<span data-ttu-id="617a9-121">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="617a9-121">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="617a9-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="617a9-122">Remarks</span></span>

<span data-ttu-id="617a9-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="617a9-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="617a9-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="617a9-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="617a9-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="617a9-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="617a9-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="617a9-126">Schema name</span></span>  <br/> |<span data-ttu-id="617a9-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="617a9-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="617a9-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="617a9-128">Validation file</span></span>  <br/> |<span data-ttu-id="617a9-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="617a9-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="617a9-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="617a9-130">Can be empty</span></span>  <br/> |<span data-ttu-id="617a9-131">False</span><span class="sxs-lookup"><span data-stu-id="617a9-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="617a9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="617a9-132">See also</span></span>



- [<span data-ttu-id="617a9-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="617a9-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

