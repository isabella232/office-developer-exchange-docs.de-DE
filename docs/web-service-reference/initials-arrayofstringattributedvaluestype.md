---
title: Initials (ArrayOfStringAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 060c0cf1-c632-484c-87f5-f577017a7090
description: Das Initialen-Element gibt ein Array von Werten Initialen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: 5b9fe4062bcc0d60de828ed6b0cb08faa45b5c19
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829926"
---
# <a name="initials-arrayofstringattributedvaluestype"></a><span data-ttu-id="b08bd-103">Initials (ArrayOfStringAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="b08bd-103">Initials (ArrayOfStringAttributedValuesType)</span></span>

<span data-ttu-id="b08bd-104">Das **Initialen** -Element gibt ein Array von Werten Initialen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="b08bd-104">The **Initials** element specifies an array of initials values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Initials>
    <StringAttributedValue/>
</Initials>
```

 <span data-ttu-id="b08bd-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="b08bd-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b08bd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b08bd-106">Attributes and elements</span></span>

<span data-ttu-id="b08bd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b08bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b08bd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b08bd-108">Attributes</span></span>

<span data-ttu-id="b08bd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b08bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b08bd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b08bd-110">Child elements</span></span>

|<span data-ttu-id="b08bd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b08bd-111">**Element**</span></span>|<span data-ttu-id="b08bd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b08bd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b08bd-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="b08bd-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="b08bd-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b08bd-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b08bd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b08bd-115">Parent elements</span></span>

|<span data-ttu-id="b08bd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b08bd-116">**Element**</span></span>|<span data-ttu-id="b08bd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b08bd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b08bd-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="b08bd-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="b08bd-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b08bd-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b08bd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b08bd-120">Remarks</span></span>

<span data-ttu-id="b08bd-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b08bd-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b08bd-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b08bd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b08bd-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b08bd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b08bd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b08bd-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b08bd-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b08bd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b08bd-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="b08bd-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="b08bd-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b08bd-127">Validation File</span></span>  <br/> |<span data-ttu-id="b08bd-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b08bd-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b08bd-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b08bd-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b08bd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b08bd-130">See also</span></span>



- [<span data-ttu-id="b08bd-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b08bd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

