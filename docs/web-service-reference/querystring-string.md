---
title: QueryString (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: Das QueryString-Element gibt einen Satz von Werten, die die Abfragezeichenfolge in einer FindPeople Vorgang Anforderung entsprechen zurückgegeben werden soll. Eine Suche mit keine angegebenen QueryString gibt alle Elemente aus dem angegebenen Ordner zurück.
ms.openlocfilehash: 9c5c733adcec1496e36986fd720b56b0a0274593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830935"
---
# <a name="querystring-string"></a><span data-ttu-id="48871-104">QueryString (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="48871-104">QueryString (String)</span></span>

<span data-ttu-id="48871-105">Das **QueryString** -Element gibt einen Satz von Werten, die die Abfragezeichenfolge in einer Anforderung [FindPeople Vorgang](findpeople-operation.md) entsprechen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="48871-105">The **QueryString** element specifies a set of values to be returned that match the query string in a [FindPeople operation](findpeople-operation.md) request.</span></span> <span data-ttu-id="48871-106">Eine Suche mit keine **QueryString** angegeben gibt alle Elemente aus dem angegebenen Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="48871-106">A search with no **QueryString** specified returns all items from the specified folder.</span></span> 
  
```XML
<QueryString/> 
```

 <span data-ttu-id="48871-107">**string**</span><span class="sxs-lookup"><span data-stu-id="48871-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48871-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="48871-108">Attributes and elements</span></span>

<span data-ttu-id="48871-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="48871-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48871-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="48871-110">Attributes</span></span>

<span data-ttu-id="48871-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="48871-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48871-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48871-112">Child elements</span></span>

<span data-ttu-id="48871-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="48871-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="48871-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48871-114">Parent elements</span></span>

|<span data-ttu-id="48871-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="48871-115">**Element**</span></span>|<span data-ttu-id="48871-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48871-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48871-117">FindPeople</span><span class="sxs-lookup"><span data-stu-id="48871-117">FindPeople</span></span>](findpeople.md) <br/> |<span data-ttu-id="48871-118">Enthält die Argumente für eine Suche [FindPeople Vorgang](findpeople-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="48871-118">Contains the arguments for a [FindPeople operation](findpeople-operation.md) search.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="48871-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="48871-119">Text value</span></span>

<span data-ttu-id="48871-120">Der Textwert **QueryString** stellt eine Abfrage Postfach mithilfe einer Teilmenge der [(Erweiterte Query Syntax, AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="48871-120">The **QueryString** text value represents a mailbox query made by using a subset of [Advanced Query Syntax (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="48871-121">Informationen zur Syntax für dieses Elements finden Sie unter [QueryString (QueryStringType)](querystring-querystringtype.md).</span><span class="sxs-lookup"><span data-stu-id="48871-121">For information about the syntax for this element, see [QueryString (QueryStringType)](querystring-querystringtype.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48871-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48871-122">Remarks</span></span>

<span data-ttu-id="48871-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="48871-123">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48871-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="48871-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48871-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="48871-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="48871-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="48871-126">Schema name</span></span>  <br/> |<span data-ttu-id="48871-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="48871-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="48871-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="48871-128">Validation file</span></span>  <br/> |<span data-ttu-id="48871-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="48871-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="48871-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="48871-130">Can be empty</span></span>  <br/> |<span data-ttu-id="48871-131">False</span><span class="sxs-lookup"><span data-stu-id="48871-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48871-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48871-132">See also</span></span>



[<span data-ttu-id="48871-133">FindPeople-Vorgang</span><span class="sxs-lookup"><span data-stu-id="48871-133">FindPeople operation</span></span>](findpeople-operation.md)


- [<span data-ttu-id="48871-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="48871-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

