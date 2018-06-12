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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757574"
---
# <a name="companies"></a><span data-ttu-id="e6400-103">Companies</span><span class="sxs-lookup"><span data-stu-id="e6400-103">Companies</span></span>

<span data-ttu-id="e6400-104">Das **Unternehmen** Element stellt die Auflistung der Unternehmen, die einen Kontakt oder eine Aufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e6400-104">The **Companies** element represents the collection of companies that are associated with a contact or task.</span></span> 
  
```xml
<Companies>
   <String/>
</Companies>
```

 <span data-ttu-id="e6400-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="e6400-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6400-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e6400-106">Attributes and elements</span></span>

<span data-ttu-id="e6400-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e6400-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6400-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6400-108">Attributes</span></span>

<span data-ttu-id="e6400-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6400-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6400-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6400-110">Child elements</span></span>

|<span data-ttu-id="e6400-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6400-111">**Element**</span></span>|<span data-ttu-id="e6400-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6400-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6400-113">String</span><span class="sxs-lookup"><span data-stu-id="e6400-113">String</span></span>](string.md) <br/> |<span data-ttu-id="e6400-114">Stellt den Namen eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="e6400-114">Represents the name of a company.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6400-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6400-115">Parent elements</span></span>

|<span data-ttu-id="e6400-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6400-116">**Element**</span></span>|<span data-ttu-id="e6400-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6400-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6400-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="e6400-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e6400-119">Stellt einen Kontakt in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e6400-119">Represents a contact in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6400-120">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e6400-120">Task</span></span>](task.md) <br/> |<span data-ttu-id="e6400-121">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e6400-121">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6400-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6400-122">Remarks</span></span>

<span data-ttu-id="e6400-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e6400-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6400-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e6400-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6400-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6400-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6400-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e6400-126">Schema name</span></span>  <br/> |<span data-ttu-id="e6400-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e6400-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6400-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e6400-128">Validation file</span></span>  <br/> |<span data-ttu-id="e6400-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6400-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6400-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e6400-130">Can be empty</span></span>  <br/> |<span data-ttu-id="e6400-131">False</span><span class="sxs-lookup"><span data-stu-id="e6400-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6400-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6400-132">See also</span></span>



- [<span data-ttu-id="e6400-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e6400-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

