---
title: CompanyNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 615fa52d-86ff-4630-b188-5fdb9391eee2
description: Das CompanyNames-Element enthält ein Array von Firmennamen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.
ms.openlocfilehash: b9024b08cb46d2ccbfcc7b07acb4645894cc5f4c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757576"
---
# <a name="companynames"></a><span data-ttu-id="f1296-103">CompanyNames</span><span class="sxs-lookup"><span data-stu-id="f1296-103">CompanyNames</span></span>

<span data-ttu-id="f1296-104">Das **CompanyNames** -Element enthält ein Array von Firmennamen und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="f1296-104">The **CompanyNames** element contains an array of company names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CompanyNames>
    <StringAttributedValue></StringAttributedValue>
</CompanyNames>
```

 <span data-ttu-id="f1296-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="f1296-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1296-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f1296-106">Attributes and elements</span></span>

<span data-ttu-id="f1296-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1296-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1296-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1296-108">Attributes</span></span>

<span data-ttu-id="f1296-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1296-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1296-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1296-110">Child elements</span></span>

|<span data-ttu-id="f1296-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1296-111">**Element**</span></span>|<span data-ttu-id="f1296-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1296-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1296-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="f1296-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="f1296-114">Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f1296-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f1296-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1296-115">Parent elements</span></span>

|<span data-ttu-id="f1296-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1296-116">**Element**</span></span>|<span data-ttu-id="f1296-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1296-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1296-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="f1296-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f1296-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f1296-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1296-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1296-120">Remarks</span></span>

<span data-ttu-id="f1296-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f1296-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f1296-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f1296-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1296-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f1296-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1296-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1296-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f1296-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f1296-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f1296-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="f1296-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f1296-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f1296-127">Validation File</span></span>  <br/> |<span data-ttu-id="f1296-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f1296-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1296-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f1296-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f1296-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1296-130">See also</span></span>



- [<span data-ttu-id="f1296-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f1296-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

