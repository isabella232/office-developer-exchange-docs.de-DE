---
title: PercentComplete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PercentComplete
api_type:
- schema
ms.assetid: 58a67f8a-c4dc-42dc-97ae-a9e5cc672d2d
description: PercentComplete-Element beschreibt den Status eines Vorgangs.
ms.openlocfilehash: 18e53221ecdf60df195445ed7692c03795bdcc1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830717"
---
# <a name="percentcomplete"></a><span data-ttu-id="d89c7-103">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="d89c7-103">PercentComplete</span></span>

<span data-ttu-id="d89c7-104">**PercentComplete** -Element beschreibt den Status eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d89c7-104">The **PercentComplete** element describes the completion status of a task.</span></span> 
  
```xml
<PercentComplete/>
```

 <span data-ttu-id="d89c7-105">**Double**</span><span class="sxs-lookup"><span data-stu-id="d89c7-105">**double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d89c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d89c7-106">Attributes and elements</span></span>

<span data-ttu-id="d89c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d89c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d89c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d89c7-108">Attributes</span></span>

<span data-ttu-id="d89c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d89c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d89c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d89c7-110">Child elements</span></span>

<span data-ttu-id="d89c7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d89c7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d89c7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d89c7-112">Parent elements</span></span>

|<span data-ttu-id="d89c7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d89c7-113">**Element**</span></span>|<span data-ttu-id="d89c7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d89c7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d89c7-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="d89c7-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="d89c7-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d89c7-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d89c7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d89c7-117">Text value</span></span>

<span data-ttu-id="d89c7-118">Ein Textwert, der eine ganze Zahl zwischen 0 und 100 darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d89c7-118">A text value that represents an integer between 0 and 100 is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d89c7-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d89c7-119">Remarks</span></span>

<span data-ttu-id="d89c7-120">Wenn **PercentComplete** auf 100 hat dieselbe Wirkung wie das Festlegen des [CompleteDate](completedate.md) -Elements oder das [Status](status.md) -Element auf **abgeschlossen**festlegen.</span><span class="sxs-lookup"><span data-stu-id="d89c7-120">Setting **PercentComplete** to 100 has the same effect as setting the [CompleteDate](completedate.md) element or setting the [Status](status.md) element to **Completed**.</span></span> <span data-ttu-id="d89c7-121">In einer Anforderung, dass mindestens zwei Sätze von diesen Eigenschaften, die letzte verarbeitete-Eigenschaft den Wert bestimmt wird, der für diese Elemente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d89c7-121">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="d89c7-122">Beispielsweise wenn **PercentComplete** 100 ist, [CompleteDate](completedate.md) am 1. Januar 2007 ist und [Status](status.md) auf nicht gestartet ist und die Eigenschaften in dieser Reihenfolge gestreamt werden, werden der Effekt der [Status](status.md) des Vorgangs auf nicht gestartet, die [festgelegt "CompleteDate" darf](completedate.md) auf **null**und die **PercentComplete** auf 0.</span><span class="sxs-lookup"><span data-stu-id="d89c7-122">For example, if **PercentComplete** is 100, [CompleteDate](completedate.md) is January 1, 2007, and [Status](status.md) is NotStarted, and the properties are streamed in this order, the effect will be to set the [Status](status.md) of the task to NotStarted, the [CompleteDate](completedate.md) to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="d89c7-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d89c7-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d89c7-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d89c7-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d89c7-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d89c7-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d89c7-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d89c7-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d89c7-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d89c7-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d89c7-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d89c7-128">Validation File</span></span>  <br/> |<span data-ttu-id="d89c7-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d89c7-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d89c7-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d89c7-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d89c7-131">False</span><span class="sxs-lookup"><span data-stu-id="d89c7-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d89c7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d89c7-132">See also</span></span>



- [<span data-ttu-id="d89c7-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d89c7-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d89c7-134">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="d89c7-134">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="d89c7-135">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="d89c7-135">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

