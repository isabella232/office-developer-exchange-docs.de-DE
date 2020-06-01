---
title: AssistantNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4e69022d-1cef-4744-877c-848a0b5c4f40
description: Das AssistantNames-Element gibt ein Array von Assistenten Namen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: cb3722e07da97ed472f9ae50180d61ed761413c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461541"
---
# <a name="assistantnames"></a><span data-ttu-id="1c282-103">AssistantNames</span><span class="sxs-lookup"><span data-stu-id="1c282-103">AssistantNames</span></span>

<span data-ttu-id="1c282-104">Das **AssistantNames** -Element gibt ein Array von Assistenten Namen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="1c282-104">The **AssistantNames** element specifies an array of assistant names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantNames>
    <StringAttributedValue></StringAttributedValue>
</AssistantNames>
```

 <span data-ttu-id="1c282-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="1c282-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c282-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1c282-106">Attributes and elements</span></span>

<span data-ttu-id="1c282-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1c282-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c282-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c282-108">Attributes</span></span>

<span data-ttu-id="1c282-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c282-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c282-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c282-110">Child elements</span></span>

|<span data-ttu-id="1c282-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c282-111">**Element**</span></span>|<span data-ttu-id="1c282-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c282-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c282-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="1c282-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="1c282-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1c282-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1c282-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c282-115">Parent elements</span></span>

|<span data-ttu-id="1c282-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c282-116">**Element**</span></span>|<span data-ttu-id="1c282-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c282-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c282-118">Persona</span><span class="sxs-lookup"><span data-stu-id="1c282-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="1c282-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1c282-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c282-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c282-120">Remarks</span></span>

<span data-ttu-id="1c282-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1c282-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1c282-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1c282-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c282-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1c282-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c282-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c282-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c282-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1c282-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1c282-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="1c282-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="1c282-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1c282-127">Validation File</span></span>  <br/> |<span data-ttu-id="1c282-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1c282-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c282-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1c282-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1c282-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c282-130">See also</span></span>

- [<span data-ttu-id="1c282-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1c282-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

