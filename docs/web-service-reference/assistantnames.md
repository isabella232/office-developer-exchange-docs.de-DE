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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461541"
---
# <a name="assistantnames"></a><span data-ttu-id="af440-103">AssistantNames</span><span class="sxs-lookup"><span data-stu-id="af440-103">AssistantNames</span></span>

<span data-ttu-id="af440-104">Das **AssistantNames** -Element gibt ein Array von Assistenten Namen und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="af440-104">The **AssistantNames** element specifies an array of assistant names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantNames>
    <StringAttributedValue></StringAttributedValue>
</AssistantNames>
```

 <span data-ttu-id="af440-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="af440-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af440-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af440-106">Attributes and elements</span></span>

<span data-ttu-id="af440-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af440-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af440-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="af440-108">Attributes</span></span>

<span data-ttu-id="af440-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="af440-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af440-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af440-110">Child elements</span></span>

|<span data-ttu-id="af440-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="af440-111">**Element**</span></span>|<span data-ttu-id="af440-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af440-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af440-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="af440-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="af440-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="af440-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af440-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af440-115">Parent elements</span></span>

|<span data-ttu-id="af440-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="af440-116">**Element**</span></span>|<span data-ttu-id="af440-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af440-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af440-118">Persona</span><span class="sxs-lookup"><span data-stu-id="af440-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="af440-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="af440-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af440-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af440-120">Remarks</span></span>

<span data-ttu-id="af440-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="af440-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="af440-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="af440-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af440-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="af440-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af440-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="af440-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af440-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="af440-125">Schema Name</span></span>  <br/> |<span data-ttu-id="af440-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="af440-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="af440-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="af440-127">Validation File</span></span>  <br/> |<span data-ttu-id="af440-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="af440-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="af440-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="af440-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="af440-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af440-130">See also</span></span>

- [<span data-ttu-id="af440-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="af440-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

