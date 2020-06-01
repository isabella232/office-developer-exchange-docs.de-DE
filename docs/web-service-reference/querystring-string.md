---
title: QueryString (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: Das QueryString-Element gibt eine Gruppe von Werten an, die zurückgegeben werden sollen, die mit der Abfragezeichenfolge in einer FindPeople-Vorgangsanforderung übereinstimmen. Bei einer Suche ohne QueryString-Angabe werden alle Elemente aus dem angegebenen Ordner zurückgegeben.
ms.openlocfilehash: ec025f86d3e6fb74810e9c539eba102d05adbb93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465324"
---
# <a name="querystring-string"></a><span data-ttu-id="bd1eb-104">QueryString (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="bd1eb-104">QueryString (String)</span></span>

<span data-ttu-id="bd1eb-105">Das **QueryString** -Element gibt eine Gruppe von Werten an, die zurückgegeben werden sollen, die mit der Abfragezeichenfolge in einer [FindPeople-Vorgangs](findpeople-operation.md) Anforderung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-105">The **QueryString** element specifies a set of values to be returned that match the query string in a [FindPeople operation](findpeople-operation.md) request.</span></span> <span data-ttu-id="bd1eb-106">Bei einer Suche ohne **QueryString** -Angabe werden alle Elemente aus dem angegebenen Ordner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-106">A search with no **QueryString** specified returns all items from the specified folder.</span></span> 
  
```XML
<QueryString/> 
```

 <span data-ttu-id="bd1eb-107">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd1eb-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd1eb-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bd1eb-108">Attributes and elements</span></span>

<span data-ttu-id="bd1eb-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd1eb-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="bd1eb-110">Attributes</span></span>

<span data-ttu-id="bd1eb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd1eb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd1eb-112">Child elements</span></span>

<span data-ttu-id="bd1eb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bd1eb-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd1eb-114">Parent elements</span></span>

|<span data-ttu-id="bd1eb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd1eb-115">**Element**</span></span>|<span data-ttu-id="bd1eb-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd1eb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd1eb-117">FindPeople</span><span class="sxs-lookup"><span data-stu-id="bd1eb-117">FindPeople</span></span>](findpeople.md) <br/> |<span data-ttu-id="bd1eb-118">Enthält die Argumente für eine [FindPeople-Vorgangs](findpeople-operation.md) Suche.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-118">Contains the arguments for a [FindPeople operation](findpeople-operation.md) search.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bd1eb-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="bd1eb-119">Text value</span></span>

<span data-ttu-id="bd1eb-120">Der **QueryString** -Textwert stellt eine Post Fach Abfrage dar, die mithilfe einer Teilmenge der [erweiterten Abfrage Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-120">The **QueryString** text value represents a mailbox query made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="bd1eb-121">Informationen zur Syntax dieses Elements finden Sie unter [QueryString (querystringtype)](querystring-querystringtype.md).</span><span class="sxs-lookup"><span data-stu-id="bd1eb-121">For information about the syntax for this element, see [QueryString (QueryStringType)](querystring-querystringtype.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd1eb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd1eb-122">Remarks</span></span>

<span data-ttu-id="bd1eb-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bd1eb-123">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd1eb-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bd1eb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd1eb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd1eb-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bd1eb-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bd1eb-126">Schema name</span></span>  <br/> |<span data-ttu-id="bd1eb-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bd1eb-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bd1eb-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bd1eb-128">Validation file</span></span>  <br/> |<span data-ttu-id="bd1eb-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bd1eb-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bd1eb-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bd1eb-130">Can be empty</span></span>  <br/> |<span data-ttu-id="bd1eb-131">False</span><span class="sxs-lookup"><span data-stu-id="bd1eb-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd1eb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd1eb-132">See also</span></span>



[<span data-ttu-id="bd1eb-133">FindPeople-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bd1eb-133">FindPeople operation</span></span>](findpeople-operation.md)


- [<span data-ttu-id="bd1eb-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bd1eb-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

