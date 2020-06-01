---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: Die DeletedOccurrenceStateDefinition gibt den Status für ein gelöschtes Vorkommen eines Kalenderelements an.
ms.openlocfilehash: ff8ad1d9c35d7bab3f6fe2cd1896bb16384c18e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458796"
---
# <a name="deletedoccurrencestatedefinition"></a><span data-ttu-id="73b81-103">DeletedOccurrenceStateDefinition</span><span class="sxs-lookup"><span data-stu-id="73b81-103">DeletedOccurrenceStateDefinition</span></span>

<span data-ttu-id="73b81-104">Die **DeletedOccurrenceStateDefinition** gibt den Status für ein gelöschtes Vorkommen eines Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="73b81-104">The **DeletedOccurrenceStateDefinition** specifies the state for a deleted occurrence of a calendar item.</span></span> 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 <span data-ttu-id="73b81-105">**DeletedOccurrenceStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="73b81-105">**DeletedOccurrenceStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73b81-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73b81-106">Attributes and elements</span></span>

<span data-ttu-id="73b81-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="73b81-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73b81-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="73b81-108">Attributes</span></span>

<span data-ttu-id="73b81-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="73b81-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73b81-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73b81-110">Child elements</span></span>

|<span data-ttu-id="73b81-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="73b81-111">**Element**</span></span>|<span data-ttu-id="73b81-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73b81-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73b81-113">Vorkommen (Zeitzonenübergang)</span><span class="sxs-lookup"><span data-stu-id="73b81-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="73b81-114">Gibt das Datum des Auftretens eines Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="73b81-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="73b81-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="73b81-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="73b81-116">Gibt einen booleschen Wert an, der angibt, ob ein Vorkommen des Kalenderelements vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="73b81-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73b81-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73b81-117">Parent elements</span></span>

|<span data-ttu-id="73b81-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="73b81-118">**Element**</span></span>|<span data-ttu-id="73b81-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73b81-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73b81-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="73b81-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="73b81-121">Gibt eine Statusdefinition an.</span><span class="sxs-lookup"><span data-stu-id="73b81-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b81-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73b81-122">Remarks</span></span>

<span data-ttu-id="73b81-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73b81-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="73b81-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="73b81-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73b81-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="73b81-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73b81-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="73b81-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73b81-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="73b81-127">Schema Name</span></span>  <br/> |<span data-ttu-id="73b81-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="73b81-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="73b81-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="73b81-129">Validation File</span></span>  <br/> |<span data-ttu-id="73b81-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="73b81-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="73b81-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="73b81-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="73b81-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73b81-132">See also</span></span>

- [<span data-ttu-id="73b81-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="73b81-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

