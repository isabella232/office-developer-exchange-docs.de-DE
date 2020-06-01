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
description: Das MessageClassifications-Element stellt die Nachrichtenklassifikationen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 63481aa8903c4e9637870130eb9154118471c3b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467970"
---
# <a name="messageclassifications"></a><span data-ttu-id="2ebcd-103">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="2ebcd-103">MessageClassifications</span></span>

<span data-ttu-id="2ebcd-104">Das **MessageClassifications** -Element stellt die Nachrichtenklassifikationen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-104">The **MessageClassifications** element represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<MessageClassifications>
    <String/>
</MessageClassifications>
```

 <span data-ttu-id="2ebcd-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="2ebcd-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ebcd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2ebcd-106">Attributes and elements</span></span>

<span data-ttu-id="2ebcd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ebcd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2ebcd-108">Attributes</span></span>

<span data-ttu-id="2ebcd-109">Keine</span><span class="sxs-lookup"><span data-stu-id="2ebcd-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ebcd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ebcd-110">Child elements</span></span>

|<span data-ttu-id="2ebcd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ebcd-111">**Element**</span></span>|<span data-ttu-id="2ebcd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ebcd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ebcd-113">String</span><span class="sxs-lookup"><span data-stu-id="2ebcd-113">String</span></span>](string.md) <br/> |<span data-ttu-id="2ebcd-114">Stellt eine Nachrichtenklassifikation dar.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-114">Represents a message classification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2ebcd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ebcd-115">Parent elements</span></span>

|<span data-ttu-id="2ebcd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ebcd-116">**Element**</span></span>|<span data-ttu-id="2ebcd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ebcd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ebcd-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="2ebcd-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="2ebcd-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="2ebcd-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="2ebcd-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="2ebcd-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2ebcd-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="2ebcd-122">Text value</span></span>

<span data-ttu-id="2ebcd-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ebcd-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ebcd-124">Remarks</span></span>

<span data-ttu-id="2ebcd-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2ebcd-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ebcd-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2ebcd-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ebcd-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ebcd-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2ebcd-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2ebcd-128">Schema Name</span></span>  <br/> |<span data-ttu-id="2ebcd-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2ebcd-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2ebcd-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2ebcd-130">Validation File</span></span>  <br/> |<span data-ttu-id="2ebcd-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2ebcd-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2ebcd-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2ebcd-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="2ebcd-133">True</span><span class="sxs-lookup"><span data-stu-id="2ebcd-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ebcd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ebcd-134">See also</span></span>



- [<span data-ttu-id="2ebcd-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2ebcd-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

