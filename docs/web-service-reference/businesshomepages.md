---
title: BusinessHomePages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9961c0c2-7cac-4af1-84ac-0eafdce0a6ab
description: Das BusinessHomePages-Element gibt ein Array von Geschäfts Homepages und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.
ms.openlocfilehash: f0e85e0b3c857e44d94bd42c6d3ea757d015eb25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465912"
---
# <a name="businesshomepages"></a><span data-ttu-id="70d68-103">BusinessHomePages</span><span class="sxs-lookup"><span data-stu-id="70d68-103">BusinessHomePages</span></span>

<span data-ttu-id="70d68-104">Das **BusinessHomePages** -Element gibt ein Array von Geschäfts Homepages und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.</span><span class="sxs-lookup"><span data-stu-id="70d68-104">The **BusinessHomePages** element specifies an array of business home pages and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessHomePages>
    <StringAttributedValue></StringAttributedValue>
</BusinessHomePages>
```

 <span data-ttu-id="70d68-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="70d68-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70d68-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="70d68-106">Attributes and elements</span></span>

<span data-ttu-id="70d68-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="70d68-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70d68-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="70d68-108">Attributes</span></span>

<span data-ttu-id="70d68-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="70d68-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70d68-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70d68-110">Child elements</span></span>

|<span data-ttu-id="70d68-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="70d68-111">**Element**</span></span>|<span data-ttu-id="70d68-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70d68-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70d68-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="70d68-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="70d68-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="70d68-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70d68-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70d68-115">Parent elements</span></span>

|<span data-ttu-id="70d68-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="70d68-116">**Element**</span></span>|<span data-ttu-id="70d68-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70d68-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70d68-118">Persona</span><span class="sxs-lookup"><span data-stu-id="70d68-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="70d68-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70d68-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70d68-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70d68-120">Remarks</span></span>

<span data-ttu-id="70d68-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="70d68-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="70d68-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="70d68-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70d68-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="70d68-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70d68-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="70d68-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70d68-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="70d68-125">Schema Name</span></span>  <br/> |<span data-ttu-id="70d68-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="70d68-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="70d68-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="70d68-127">Validation File</span></span>  <br/> |<span data-ttu-id="70d68-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="70d68-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="70d68-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="70d68-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="70d68-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70d68-130">See also</span></span>



- [<span data-ttu-id="70d68-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="70d68-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

