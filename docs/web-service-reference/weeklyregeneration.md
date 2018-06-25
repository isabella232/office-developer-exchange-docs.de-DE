---
title: WeeklyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRegeneration
api_type:
- schema
ms.assetid: f128fdaa-ca3d-4614-8e55-f25e76a67b6c
description: Das WeeklyRegeneration-Element beschreibt die Häufigkeit in Wochen, in denen eine Aufgabe neu erstellt wird.
ms.openlocfilehash: 36cd3cc5c180f2b2cf53708e7787d0595f518def
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839535"
---
# <a name="weeklyregeneration"></a><span data-ttu-id="70ae5-103">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="70ae5-103">WeeklyRegeneration</span></span>

<span data-ttu-id="70ae5-104">Das **WeeklyRegeneration** -Element beschreibt die Häufigkeit in Wochen, in denen eine Aufgabe neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="70ae5-104">The **WeeklyRegeneration** element describes the frequency, in weeks, in which a task is regenerated.</span></span> 
  
```xml
<WeeklyRegeneration>
   <Interval/>
</WeeklyRegeneration>
```

 <span data-ttu-id="70ae5-105">**WeeklyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="70ae5-105">**WeeklyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70ae5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="70ae5-106">Attributes and elements</span></span>

<span data-ttu-id="70ae5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="70ae5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70ae5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="70ae5-108">Attributes</span></span>

<span data-ttu-id="70ae5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="70ae5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70ae5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70ae5-110">Child elements</span></span>

|<span data-ttu-id="70ae5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="70ae5-111">**Element**</span></span>|<span data-ttu-id="70ae5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70ae5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70ae5-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="70ae5-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="70ae5-114">Definiert das Intervall in Wochen, da der Vorgang abgeschlossen wurde, nach dem eine neue Aufgabe neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="70ae5-114">Defines the interval, in weeks, since the task was completed, after which a new task is regenerated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70ae5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70ae5-115">Parent elements</span></span>

|<span data-ttu-id="70ae5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="70ae5-116">**Element**</span></span>|<span data-ttu-id="70ae5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70ae5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70ae5-118">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="70ae5-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="70ae5-119">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="70ae5-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70ae5-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70ae5-120">Remarks</span></span>

<span data-ttu-id="70ae5-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="70ae5-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70ae5-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="70ae5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70ae5-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="70ae5-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70ae5-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="70ae5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="70ae5-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="70ae5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="70ae5-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="70ae5-126">Validation File</span></span>  <br/> |<span data-ttu-id="70ae5-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70ae5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70ae5-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="70ae5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="70ae5-129">False</span><span class="sxs-lookup"><span data-stu-id="70ae5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70ae5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70ae5-130">See also</span></span>



- [<span data-ttu-id="70ae5-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="70ae5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

