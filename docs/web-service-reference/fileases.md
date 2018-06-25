---
title: FileAses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81efc37-bb70-4d52-a614-cec87d1b0f04
description: Das FileAses-Element gibt ein Array von StringAttributedValue-Elementen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: e660c74135dca9a2eb58b3486e0d2e19f85e012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758416"
---
# <a name="fileases"></a><span data-ttu-id="2ebbd-103">FileAses</span><span class="sxs-lookup"><span data-stu-id="2ebbd-103">FileAses</span></span>

<span data-ttu-id="2ebbd-104">Das **FileAses** -Element gibt ein Array von **StringAttributedValue** -Elementen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="2ebbd-104">The **FileAses** element specifies an array of **StringAttributedValue** elements and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<FileAses>
    <StringAttributedValue/>
</FileAses>
```

 <span data-ttu-id="2ebbd-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="2ebbd-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ebbd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2ebbd-106">Attributes and elements</span></span>

<span data-ttu-id="2ebbd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2ebbd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ebbd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2ebbd-108">Attributes</span></span>

<span data-ttu-id="2ebbd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2ebbd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ebbd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ebbd-110">Child elements</span></span>

|<span data-ttu-id="2ebbd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ebbd-111">**Element**</span></span>|<span data-ttu-id="2ebbd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ebbd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ebbd-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2ebbd-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="2ebbd-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2ebbd-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2ebbd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ebbd-115">Parent elements</span></span>

|<span data-ttu-id="2ebbd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ebbd-116">**Element**</span></span>|<span data-ttu-id="2ebbd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ebbd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ebbd-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="2ebbd-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2ebbd-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2ebbd-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ebbd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2ebbd-120">Remarks</span></span>

<span data-ttu-id="2ebbd-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2ebbd-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2ebbd-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2ebbd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ebbd-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2ebbd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ebbd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ebbd-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2ebbd-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2ebbd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2ebbd-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="2ebbd-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2ebbd-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2ebbd-127">Validation File</span></span>  <br/> |<span data-ttu-id="2ebbd-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2ebbd-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2ebbd-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2ebbd-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2ebbd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ebbd-130">See also</span></span>



- [<span data-ttu-id="2ebbd-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2ebbd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
