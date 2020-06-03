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
description: Das WithinDateRange-Element gibt den Datumsbereich an, in dem eingehende Nachrichten empfangen werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: ef5fb15b64ee4f7060f907818c4ebd4367ced5e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461849"
---
# <a name="withindaterange"></a><span data-ttu-id="ac164-103">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="ac164-103">WithinDateRange</span></span>

<span data-ttu-id="ac164-104">Das **WithinDateRange** -Element gibt den Datumsbereich an, in dem eingehende Nachrichten empfangen werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="ac164-104">The **WithinDateRange** element specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinDateRange>
     <StartDateTime/>
     <EndDateTime/>
</WithinDateRange>
```

 <span data-ttu-id="ac164-105">**RulePredicateDateRangeType**</span><span class="sxs-lookup"><span data-stu-id="ac164-105">**RulePredicateDateRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac164-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac164-106">Attributes and elements</span></span>

<span data-ttu-id="ac164-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac164-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac164-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac164-108">Attributes</span></span>

<span data-ttu-id="ac164-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac164-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac164-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac164-110">Child elements</span></span>

|<span data-ttu-id="ac164-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac164-111">**Element**</span></span>|<span data-ttu-id="ac164-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac164-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac164-113">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="ac164-113">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="ac164-114">Gibt den Regel Zeitraum an und gibt an, dass die Regelbedingung nach diesem Wert erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="ac164-114">Specifies the rule time period and indicates that the rule condition is met after this value.</span></span>  <br/> |
|[<span data-ttu-id="ac164-115">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="ac164-115">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="ac164-116">Gibt den Regel Zeitraum an und gibt an, dass die Regelbedingung vor diesem Wert erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ac164-116">Specifies the rule time period and indicates that the rule condition is met before this value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac164-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac164-117">Parent elements</span></span>

|<span data-ttu-id="ac164-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac164-118">**Element**</span></span>|<span data-ttu-id="ac164-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac164-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac164-120">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="ac164-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="ac164-121">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ac164-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="ac164-122">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="ac164-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="ac164-123">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="ac164-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ac164-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="ac164-124">Text value</span></span>

<span data-ttu-id="ac164-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac164-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac164-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac164-126">Remarks</span></span>

<span data-ttu-id="ac164-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ac164-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac164-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ac164-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac164-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac164-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac164-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac164-130">Schema Name</span></span>  <br/> |<span data-ttu-id="ac164-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ac164-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ac164-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac164-132">Validation File</span></span>  <br/> |<span data-ttu-id="ac164-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ac164-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac164-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac164-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac164-135">True</span><span class="sxs-lookup"><span data-stu-id="ac164-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac164-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac164-136">See also</span></span>



- [<span data-ttu-id="ac164-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ac164-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

