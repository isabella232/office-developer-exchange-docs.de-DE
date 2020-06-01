---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: Das AggregationRestriction-Element gibt einen Wert an, der auf eine Gruppe von Persona-Eigenschaften angewendet wird, die sich aus einer FindPeople-Anforderung ergeben, und filtert das Ergebnis entsprechend der angegebenen Einschränkung.
ms.openlocfilehash: f07e54235cf13b43da26ed1c56596d3c7c357bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463524"
---
# <a name="aggregationrestriction"></a><span data-ttu-id="fa715-103">AggregationRestriction</span><span class="sxs-lookup"><span data-stu-id="fa715-103">AggregationRestriction</span></span>

<span data-ttu-id="fa715-104">Das **AggregationRestriction** -Element gibt einen Wert an, der auf eine Gruppe von Persona-Eigenschaften angewendet wird, die sich aus einer FindPeople-Anforderung ergeben, und filtert das Ergebnis entsprechend der angegebenen Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="fa715-104">The **AggregationRestriction** element specifies a value that is applied to a set of Persona properties resulting from a FindPeople request and filters the result according to the specified restriction.</span></span> 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 <span data-ttu-id="fa715-105">**Restrictiontype**</span><span class="sxs-lookup"><span data-stu-id="fa715-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa715-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fa715-106">Attributes and elements</span></span>

<span data-ttu-id="fa715-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa715-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa715-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fa715-108">Attributes</span></span>

<span data-ttu-id="fa715-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa715-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa715-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa715-110">Child elements</span></span>

[<span data-ttu-id="fa715-111">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="fa715-111">SearchExpression</span></span>](searchexpression.md)
  
### <a name="parent-elements"></a><span data-ttu-id="fa715-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa715-112">Parent elements</span></span>

[<span data-ttu-id="fa715-113">FindPeople</span><span class="sxs-lookup"><span data-stu-id="fa715-113">FindPeople</span></span>](findpeople.md)
  
## <a name="remarks"></a><span data-ttu-id="fa715-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa715-114">Remarks</span></span>

<span data-ttu-id="fa715-115">Das **AggregationRestriction** -Element kann ein beliebiges untergeordnetes Element enthalten, das die **Such** Satz Ersetzungsgruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa715-115">The **AggregationRestriction** element can contain any child element that uses the **SearchExpression** substitution group.</span></span> <span data-ttu-id="fa715-116">Die Elemente, die Bestandteil der Substitutions Gruppe für die **Suche** sind, sind: [Contains](contains.md), [excludes](excludes.md), [EXISTS](exists.md), [Not](not.md), [or](or.md), [and](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [isgreaterthan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)und [IsLessThanOrEqualTo](islessthanorequalto.md).</span><span class="sxs-lookup"><span data-stu-id="fa715-116">The elements that are a part of the **SearchExpression** substitution group are: [Contains](contains.md), [Excludes](excludes.md), [Exists](exists.md), [Not](not.md), [Or](or.md), [And](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md), and [IsLessThanOrEqualTo](islessthanorequalto.md).</span></span>
  
<span data-ttu-id="fa715-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fa715-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa715-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fa715-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa715-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fa715-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa715-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa715-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa715-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fa715-121">Schema name</span></span>  <br/> |<span data-ttu-id="fa715-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fa715-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fa715-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fa715-123">Validation file</span></span>  <br/> |<span data-ttu-id="fa715-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fa715-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa715-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fa715-125">Can be empty</span></span>  <br/> |<span data-ttu-id="fa715-126">false</span><span class="sxs-lookup"><span data-stu-id="fa715-126">false</span></span>  <br/> |
   

