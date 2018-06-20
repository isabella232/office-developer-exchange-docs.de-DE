---
title: BodyContentAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f99e9590-8388-4203-ac30-1ea394f351a6
description: Das BodyContentAttributedValue-Element gibt den Textkörperinhalt eines Elements an.
ms.openlocfilehash: f5b8f0a19b77ce550b1d7f1c415cc8ee4340863a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757482"
---
# <a name="bodycontentattributedvalue"></a><span data-ttu-id="07ce3-103">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="07ce3-103">BodyContentAttributedValue</span></span>

<span data-ttu-id="07ce3-104">Das **BodyContentAttributedValue** -Element gibt den Textkörperinhalt eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="07ce3-104">The **BodyContentAttributedValue** element specifies the body content of an item.</span></span> 
  
```XML
<BodyContentAttributedValue>
   <Value></Value>
   <Attributions></Attributions>
</ BodyContentAttributedValue>
```

 <span data-ttu-id="07ce3-105">**BodyContentAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="07ce3-105">**BodyContentAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07ce3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="07ce3-106">Attributes and elements</span></span>

<span data-ttu-id="07ce3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="07ce3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07ce3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="07ce3-108">Attributes</span></span>

<span data-ttu-id="07ce3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="07ce3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07ce3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07ce3-110">Child elements</span></span>

|<span data-ttu-id="07ce3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="07ce3-111">**Element**</span></span>|<span data-ttu-id="07ce3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07ce3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07ce3-113">Wert (BodyContentType)</span><span class="sxs-lookup"><span data-stu-id="07ce3-113">Value (BodyContentType)</span></span>](value-bodycontenttype.md) <br/> |<span data-ttu-id="07ce3-114">Gibt den Wert eines **BodyContentAttributedValue** -Elements.</span><span class="sxs-lookup"><span data-stu-id="07ce3-114">Specifies the value of a **BodyContentAttributedValue** element.</span></span>  <br/> |
|[<span data-ttu-id="07ce3-115">Hinweise (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="07ce3-115">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="07ce3-116">Gibt ein Array von Informationen für eine oder mehrere Kontakte oder active Directory-Empfänger in der zugeordneten Rolle aggregiert.</span><span class="sxs-lookup"><span data-stu-id="07ce3-116">Specifies an array of attribution information for one or more of the contacts or active directory recipients aggregated into the associated persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07ce3-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07ce3-117">Parent elements</span></span>

|<span data-ttu-id="07ce3-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="07ce3-118">**Element**</span></span>|<span data-ttu-id="07ce3-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07ce3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07ce3-120">Texte</span><span class="sxs-lookup"><span data-stu-id="07ce3-120">Bodies</span></span>](bodies.md) <br/> |<span data-ttu-id="07ce3-121">Gibt ein Array von **BodyContentAttributedValue** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="07ce3-121">Specifies an array of **BodyContentAttributedValue** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07ce3-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="07ce3-122">Remarks</span></span>

<span data-ttu-id="07ce3-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="07ce3-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="07ce3-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="07ce3-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07ce3-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="07ce3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07ce3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="07ce3-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07ce3-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="07ce3-127">Schema Name</span></span>  <br/> |<span data-ttu-id="07ce3-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="07ce3-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="07ce3-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="07ce3-129">Validation File</span></span>  <br/> |<span data-ttu-id="07ce3-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07ce3-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="07ce3-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="07ce3-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="07ce3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07ce3-132">See also</span></span>



- [<span data-ttu-id="07ce3-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="07ce3-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

