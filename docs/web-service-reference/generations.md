---
title: Generationen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 637560b5-2b08-4787-a5d8-e0467f83acca
description: Das Generationen-Element gibt ein Array von Werten Generation und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: dda15b80304618e5376f2a9bbf39780e52842955
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758564"
---
# <a name="generations"></a><span data-ttu-id="67935-103">Generationen</span><span class="sxs-lookup"><span data-stu-id="67935-103">Generations</span></span>

<span data-ttu-id="67935-104">Das **Generationen** -Element gibt ein Array von Werten Generation und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="67935-104">The **Generations** element specifies an array of generation values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Generations>
    <StringAttributedValue/>
</Generations>
```

 <span data-ttu-id="67935-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="67935-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67935-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="67935-106">Attributes and elements</span></span>

<span data-ttu-id="67935-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="67935-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67935-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="67935-108">Attributes</span></span>

<span data-ttu-id="67935-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="67935-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67935-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67935-110">Child elements</span></span>

|<span data-ttu-id="67935-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="67935-111">**Element**</span></span>|<span data-ttu-id="67935-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67935-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67935-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="67935-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="67935-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67935-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67935-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67935-115">Parent elements</span></span>

|<span data-ttu-id="67935-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="67935-116">**Element**</span></span>|<span data-ttu-id="67935-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67935-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67935-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="67935-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="67935-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67935-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67935-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67935-120">Remarks</span></span>

<span data-ttu-id="67935-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="67935-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="67935-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="67935-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67935-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="67935-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67935-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="67935-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67935-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="67935-125">Schema Name</span></span>  <br/> |<span data-ttu-id="67935-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="67935-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="67935-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="67935-127">Validation File</span></span>  <br/> |<span data-ttu-id="67935-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67935-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="67935-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="67935-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="67935-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67935-130">See also</span></span>



- [<span data-ttu-id="67935-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="67935-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

