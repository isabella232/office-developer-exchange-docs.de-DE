---
title: Companynames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 615fa52d-86ff-4630-b188-5fdb9391eee2
description: Das companynames-Element enthält ein Array von Firmennamen und die Bezeichner der Quell Zuweisungen für die zugeordnete Persona.
ms.openlocfilehash: 25daa43873fe00837004217e3f814a7201638450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463258"
---
# <a name="companynames"></a><span data-ttu-id="4f3ad-103">Companynames</span><span class="sxs-lookup"><span data-stu-id="4f3ad-103">CompanyNames</span></span>

<span data-ttu-id="4f3ad-104">Das **companynames** -Element enthält ein Array von Firmennamen und die Bezeichner der Quell Zuweisungen für die zugeordnete Persona.</span><span class="sxs-lookup"><span data-stu-id="4f3ad-104">The **CompanyNames** element contains an array of company names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CompanyNames>
    <StringAttributedValue></StringAttributedValue>
</CompanyNames>
```

 <span data-ttu-id="4f3ad-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="4f3ad-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f3ad-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f3ad-106">Attributes and elements</span></span>

<span data-ttu-id="4f3ad-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f3ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f3ad-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f3ad-108">Attributes</span></span>

<span data-ttu-id="4f3ad-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f3ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f3ad-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f3ad-110">Child elements</span></span>

|<span data-ttu-id="4f3ad-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f3ad-111">**Element**</span></span>|<span data-ttu-id="4f3ad-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f3ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f3ad-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="4f3ad-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="4f3ad-114">Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="4f3ad-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f3ad-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f3ad-115">Parent elements</span></span>

|<span data-ttu-id="4f3ad-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f3ad-116">**Element**</span></span>|<span data-ttu-id="4f3ad-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f3ad-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f3ad-118">Persona</span><span class="sxs-lookup"><span data-stu-id="4f3ad-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="4f3ad-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f3ad-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f3ad-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f3ad-120">Remarks</span></span>

<span data-ttu-id="4f3ad-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4f3ad-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4f3ad-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4f3ad-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f3ad-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4f3ad-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f3ad-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f3ad-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f3ad-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f3ad-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4f3ad-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="4f3ad-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="4f3ad-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f3ad-127">Validation File</span></span>  <br/> |<span data-ttu-id="4f3ad-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4f3ad-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f3ad-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4f3ad-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4f3ad-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f3ad-130">See also</span></span>



- [<span data-ttu-id="4f3ad-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f3ad-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

