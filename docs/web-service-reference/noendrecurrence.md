---
title: NoEndRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NoEndRecurrence
api_type:
- schema
ms.assetid: ab2ebd9c-388e-45f1-abf9-56e293ef123b
description: Das NoEndRecurrence-Element beschreibt das Startdatum eines Element Serienmusters, das kein definiertes Enddatum aufweist.
ms.openlocfilehash: 31a3bd6ae2d7ce94debbeebc4fd4f536447433a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466794"
---
# <a name="noendrecurrence"></a><span data-ttu-id="5628b-103">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="5628b-103">NoEndRecurrence</span></span>

<span data-ttu-id="5628b-104">Das **NoEndRecurrence** -Element beschreibt das Startdatum eines Element Serienmusters, das kein definiertes Enddatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="5628b-104">The **NoEndRecurrence** element describes the start date of an item recurrence pattern that does not have a defined end date.</span></span> 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 <span data-ttu-id="5628b-105">**NoEndRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="5628b-105">**NoEndRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5628b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5628b-106">Attributes and elements</span></span>

<span data-ttu-id="5628b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5628b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5628b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5628b-108">Attributes</span></span>

<span data-ttu-id="5628b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5628b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5628b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5628b-110">Child elements</span></span>

|<span data-ttu-id="5628b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5628b-111">**Element**</span></span>|<span data-ttu-id="5628b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5628b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5628b-113">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="5628b-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="5628b-114">Stellt das Startdatum eines periodischen Vorgangs oder Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="5628b-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5628b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5628b-115">Parent elements</span></span>

|<span data-ttu-id="5628b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5628b-116">**Element**</span></span>|<span data-ttu-id="5628b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5628b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5628b-118">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="5628b-118">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="5628b-119">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="5628b-119">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="5628b-120">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="5628b-120">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="5628b-121">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="5628b-121">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5628b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5628b-122">Remarks</span></span>

<span data-ttu-id="5628b-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5628b-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5628b-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5628b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5628b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5628b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5628b-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5628b-126">Schema name</span></span>  <br/> |<span data-ttu-id="5628b-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5628b-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="5628b-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5628b-128">Validation file</span></span>  <br/> |<span data-ttu-id="5628b-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5628b-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5628b-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5628b-130">Can be empty</span></span>  <br/> |<span data-ttu-id="5628b-131">False</span><span class="sxs-lookup"><span data-stu-id="5628b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5628b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5628b-132">See also</span></span>



- [<span data-ttu-id="5628b-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5628b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

