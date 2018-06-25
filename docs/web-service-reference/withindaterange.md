---
title: WithinDateRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WithinDateRange
api_type:
- schema
ms.assetid: 226aeb15-016f-45ca-992a-c137ba09ca08
description: Das WithinDateRange-Element gibt den Datumsbereich, in dem eingehende Nachrichten müssen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende empfangen wurden.
ms.openlocfilehash: d85ef91c581008c2aafb06b1900c4514aebacd65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839537"
---
# <a name="withindaterange"></a><span data-ttu-id="dcecb-103">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="dcecb-103">WithinDateRange</span></span>

<span data-ttu-id="dcecb-104">Das **WithinDateRange** -Element gibt den Datumsbereich, in dem eingehende Nachrichten müssen in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="dcecb-104">The **WithinDateRange** element specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinDateRange>
     <StartDateTime/>
     <EndDateTime/>
</WithinDateRange>
```

 <span data-ttu-id="dcecb-105">**RulePredicateDateRangeType**</span><span class="sxs-lookup"><span data-stu-id="dcecb-105">**RulePredicateDateRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dcecb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dcecb-106">Attributes and elements</span></span>

<span data-ttu-id="dcecb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dcecb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcecb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dcecb-108">Attributes</span></span>

<span data-ttu-id="dcecb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dcecb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dcecb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcecb-110">Child elements</span></span>

|<span data-ttu-id="dcecb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dcecb-111">**Element**</span></span>|<span data-ttu-id="dcecb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dcecb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dcecb-113">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="dcecb-113">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="dcecb-114">Gibt die Regel Zeitraum an und gibt an, dass nach dieser Wert die Bedingung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="dcecb-114">Specifies the rule time period and indicates that the rule condition is met after this value.</span></span>  <br/> |
|[<span data-ttu-id="dcecb-115">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="dcecb-115">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="dcecb-116">Gibt die Regel Zeitraum an und gibt an, dass die regelbedingung vor dieser Wert erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="dcecb-116">Specifies the rule time period and indicates that the rule condition is met before this value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dcecb-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dcecb-117">Parent elements</span></span>

|<span data-ttu-id="dcecb-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="dcecb-118">**Element**</span></span>|<span data-ttu-id="dcecb-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dcecb-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dcecb-120">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="dcecb-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="dcecb-121">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="dcecb-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="dcecb-122">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="dcecb-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="dcecb-123">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="dcecb-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dcecb-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="dcecb-124">Text value</span></span>

<span data-ttu-id="dcecb-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="dcecb-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dcecb-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcecb-126">Remarks</span></span>

<span data-ttu-id="dcecb-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dcecb-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dcecb-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dcecb-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcecb-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcecb-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dcecb-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dcecb-130">Schema Name</span></span>  <br/> |<span data-ttu-id="dcecb-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dcecb-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dcecb-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dcecb-132">Validation File</span></span>  <br/> |<span data-ttu-id="dcecb-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dcecb-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dcecb-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dcecb-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="dcecb-135">True</span><span class="sxs-lookup"><span data-stu-id="dcecb-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcecb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcecb-136">See also</span></span>



- [<span data-ttu-id="dcecb-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dcecb-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

