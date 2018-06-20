---
title: AssistantNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4e69022d-1cef-4744-877c-848a0b5c4f40
description: Das AssistantNames-Element gibt ein Array von Assistent Namen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 7414caa74dc8221d0b1b471c3d5ed09552f7e200
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757387"
---
# <a name="assistantnames"></a><span data-ttu-id="7405a-103">AssistantNames</span><span class="sxs-lookup"><span data-stu-id="7405a-103">AssistantNames</span></span>

<span data-ttu-id="7405a-104">Das **AssistantNames** -Element gibt ein Array von Assistent Namen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="7405a-104">The **AssistantNames** element specifies an array of assistant names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantNames>
    <StringAttributedValue></StringAttributedValue>
</AssistantNames>
```

 <span data-ttu-id="7405a-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="7405a-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7405a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7405a-106">Attributes and elements</span></span>

<span data-ttu-id="7405a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7405a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7405a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7405a-108">Attributes</span></span>

<span data-ttu-id="7405a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7405a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7405a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7405a-110">Child elements</span></span>

|<span data-ttu-id="7405a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7405a-111">**Element**</span></span>|<span data-ttu-id="7405a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7405a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7405a-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="7405a-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="7405a-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7405a-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7405a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7405a-115">Parent elements</span></span>

|<span data-ttu-id="7405a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7405a-116">**Element**</span></span>|<span data-ttu-id="7405a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7405a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7405a-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="7405a-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="7405a-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7405a-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7405a-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7405a-120">Remarks</span></span>

<span data-ttu-id="7405a-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7405a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7405a-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7405a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7405a-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7405a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7405a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7405a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7405a-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7405a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7405a-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="7405a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="7405a-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7405a-127">Validation File</span></span>  <br/> |<span data-ttu-id="7405a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7405a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7405a-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7405a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7405a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7405a-130">See also</span></span>

- [<span data-ttu-id="7405a-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7405a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

