---
title: MessageClassifications
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageClassifications
api_type:
- schema
ms.assetid: 041b3d48-8f43-47f3-869f-72b66bef372a
description: Das MessageClassifications-Element darstellt, die Nachrichtenklassifikationen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen.
ms.openlocfilehash: 402377907efbc9bb63d875f3f66b314dfc4b788d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830471"
---
# <a name="messageclassifications"></a><span data-ttu-id="ec45f-103">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="ec45f-103">MessageClassifications</span></span>

<span data-ttu-id="ec45f-104">Das **MessageClassifications** -Element darstellt, die Nachrichtenklassifikationen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen.</span><span class="sxs-lookup"><span data-stu-id="ec45f-104">The **MessageClassifications** element represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<MessageClassifications>
    <String/>
</MessageClassifications>
```

 <span data-ttu-id="ec45f-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="ec45f-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec45f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec45f-106">Attributes and elements</span></span>

<span data-ttu-id="ec45f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec45f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec45f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec45f-108">Attributes</span></span>

<span data-ttu-id="ec45f-109">Keine</span><span class="sxs-lookup"><span data-stu-id="ec45f-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec45f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec45f-110">Child elements</span></span>

|<span data-ttu-id="ec45f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec45f-111">**Element**</span></span>|<span data-ttu-id="ec45f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec45f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec45f-113">String</span><span class="sxs-lookup"><span data-stu-id="ec45f-113">String</span></span>](string.md) <br/> |<span data-ttu-id="ec45f-114">Stellt eine Nachrichtenklassifikation an.</span><span class="sxs-lookup"><span data-stu-id="ec45f-114">Represents a message classification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec45f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec45f-115">Parent elements</span></span>

|<span data-ttu-id="ec45f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec45f-116">**Element**</span></span>|<span data-ttu-id="ec45f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec45f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec45f-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="ec45f-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="ec45f-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ec45f-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="ec45f-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="ec45f-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="ec45f-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="ec45f-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec45f-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="ec45f-122">Text value</span></span>

<span data-ttu-id="ec45f-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec45f-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec45f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec45f-124">Remarks</span></span>

<span data-ttu-id="ec45f-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ec45f-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec45f-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ec45f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec45f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec45f-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec45f-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec45f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ec45f-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ec45f-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ec45f-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec45f-130">Validation File</span></span>  <br/> |<span data-ttu-id="ec45f-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec45f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec45f-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec45f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec45f-133">True</span><span class="sxs-lookup"><span data-stu-id="ec45f-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec45f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec45f-134">See also</span></span>



- [<span data-ttu-id="ec45f-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec45f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

