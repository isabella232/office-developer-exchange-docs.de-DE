---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: Das AggregationRestriction-Element gibt einen Wert, der einen Satz von Persona Eigenschaften entsteht eine Anforderung FindPeople angewendet wird, und das Ergebnis entsprechend der angegebenen Einschränkung filtert.
ms.openlocfilehash: 8b4d5952dedb4de0201d2ecf2219c69f65f7dc09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757251"
---
# <a name="aggregationrestriction"></a><span data-ttu-id="6e791-103">AggregationRestriction</span><span class="sxs-lookup"><span data-stu-id="6e791-103">AggregationRestriction</span></span>

<span data-ttu-id="6e791-104">Das **AggregationRestriction** -Element gibt einen Wert, der einen Satz von Persona Eigenschaften entsteht eine Anforderung FindPeople angewendet wird, und das Ergebnis entsprechend der angegebenen Einschränkung filtert.</span><span class="sxs-lookup"><span data-stu-id="6e791-104">The **AggregationRestriction** element specifies a value that is applied to a set of Persona properties resulting from a FindPeople request and filters the result according to the specified restriction.</span></span> 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 <span data-ttu-id="6e791-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="6e791-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e791-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6e791-106">Attributes and elements</span></span>

<span data-ttu-id="6e791-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6e791-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e791-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e791-108">Attributes</span></span>

<span data-ttu-id="6e791-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e791-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e791-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e791-110">Child elements</span></span>

[<span data-ttu-id="6e791-111">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="6e791-111">SearchExpression</span></span>](searchexpression.md)
  
### <a name="parent-elements"></a><span data-ttu-id="6e791-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e791-112">Parent elements</span></span>

[<span data-ttu-id="6e791-113">FindPeople</span><span class="sxs-lookup"><span data-stu-id="6e791-113">FindPeople</span></span>](findpeople.md)
  
## <a name="remarks"></a><span data-ttu-id="6e791-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e791-114">Remarks</span></span>

<span data-ttu-id="6e791-115">Das **AggregationRestriction** -Element kann ein untergeordnetes Element enthalten, die die Ersetzungsgruppe **SearchExpression** verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e791-115">The **AggregationRestriction** element can contain any child element that uses the **SearchExpression** substitution group.</span></span> <span data-ttu-id="6e791-116">Sind die Elemente, die Teil der Ersetzungsgruppe **SearchExpression** sind: [enthält](contains.md), [ausgeschlossen](excludes.md), [Exists](exists.md), [nicht](not.md), [oder](or.md), [und](and.md), ["IsEqualTo"](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan ](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)und [IsLessThanOrEqualTo](islessthanorequalto.md).</span><span class="sxs-lookup"><span data-stu-id="6e791-116">The elements that are a part of the **SearchExpression** substitution group are: [Contains](contains.md), [Excludes](excludes.md), [Exists](exists.md), [Not](not.md), [Or](or.md), [And](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md), and [IsLessThanOrEqualTo](islessthanorequalto.md).</span></span>
  
<span data-ttu-id="6e791-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6e791-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6e791-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6e791-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e791-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6e791-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e791-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e791-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6e791-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6e791-121">Schema name</span></span>  <br/> |<span data-ttu-id="6e791-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6e791-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6e791-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6e791-123">Validation file</span></span>  <br/> |<span data-ttu-id="6e791-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6e791-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6e791-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6e791-125">Can be empty</span></span>  <br/> |<span data-ttu-id="6e791-126">false</span><span class="sxs-lookup"><span data-stu-id="6e791-126">false</span></span>  <br/> |
   

