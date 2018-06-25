---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: Die DeletedOccurrenceStateDefinition gibt den Status für ein gelöschten Vorkommen eines Kalenderelements.
ms.openlocfilehash: ad0434d604ee78ebf1905b60857929e1af4d45f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757912"
---
# <a name="deletedoccurrencestatedefinition"></a><span data-ttu-id="88636-103">DeletedOccurrenceStateDefinition</span><span class="sxs-lookup"><span data-stu-id="88636-103">DeletedOccurrenceStateDefinition</span></span>

<span data-ttu-id="88636-104">Die **DeletedOccurrenceStateDefinition** gibt den Status für ein gelöschten Vorkommen eines Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="88636-104">The **DeletedOccurrenceStateDefinition** specifies the state for a deleted occurrence of a calendar item.</span></span> 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 <span data-ttu-id="88636-105">**DeletedOccurrenceStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="88636-105">**DeletedOccurrenceStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88636-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="88636-106">Attributes and elements</span></span>

<span data-ttu-id="88636-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="88636-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88636-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="88636-108">Attributes</span></span>

<span data-ttu-id="88636-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="88636-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88636-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88636-110">Child elements</span></span>

|<span data-ttu-id="88636-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="88636-111">**Element**</span></span>|<span data-ttu-id="88636-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88636-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88636-113">Vorkommen (Übergang Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="88636-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="88636-114">Gibt das Datum des Vorkommens ein Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="88636-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="88636-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="88636-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="88636-116">Gibt einen Boolean-Wert, der angibt, ob ein Vorkommen des Kalenderelements vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="88636-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88636-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88636-117">Parent elements</span></span>

|<span data-ttu-id="88636-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="88636-118">**Element**</span></span>|<span data-ttu-id="88636-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88636-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88636-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="88636-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="88636-121">Gibt eine Definition Zustand.</span><span class="sxs-lookup"><span data-stu-id="88636-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88636-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88636-122">Remarks</span></span>

<span data-ttu-id="88636-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="88636-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="88636-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="88636-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88636-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="88636-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88636-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="88636-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88636-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="88636-127">Schema Name</span></span>  <br/> |<span data-ttu-id="88636-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="88636-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="88636-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="88636-129">Validation File</span></span>  <br/> |<span data-ttu-id="88636-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="88636-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="88636-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="88636-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="88636-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88636-132">See also</span></span>

- [<span data-ttu-id="88636-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="88636-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

