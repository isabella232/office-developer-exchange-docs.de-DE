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
description: Das PercentComplete-Element beschreibt den Abschlussstatus einer Aufgabe.
ms.openlocfilehash: b7dd2f18bd3ef6addeb6d3a7b004510f35b9cb3d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456885"
---
# <a name="percentcomplete"></a><span data-ttu-id="ef6e0-103">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="ef6e0-103">PercentComplete</span></span>

<span data-ttu-id="ef6e0-104">Das **PercentComplete** -Element beschreibt den Abschlussstatus einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-104">The **PercentComplete** element describes the completion status of a task.</span></span> 
  
```xml
<PercentComplete/>
```

 <span data-ttu-id="ef6e0-105">**Doppel**</span><span class="sxs-lookup"><span data-stu-id="ef6e0-105">**double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef6e0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef6e0-106">Attributes and elements</span></span>

<span data-ttu-id="ef6e0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef6e0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef6e0-108">Attributes</span></span>

<span data-ttu-id="ef6e0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef6e0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef6e0-110">Child elements</span></span>

<span data-ttu-id="ef6e0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef6e0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef6e0-112">Parent elements</span></span>

|<span data-ttu-id="ef6e0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef6e0-113">**Element**</span></span>|<span data-ttu-id="ef6e0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef6e0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef6e0-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ef6e0-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="ef6e0-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ef6e0-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="ef6e0-117">Text value</span></span>

<span data-ttu-id="ef6e0-118">Ein Textwert, der eine ganze Zahl zwischen 0 und 100 darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-118">A text value that represents an integer between 0 and 100 is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef6e0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef6e0-119">Remarks</span></span>

<span data-ttu-id="ef6e0-120">Das Festlegen von **PercentComplete** auf 100 hat dieselbe Auswirkung wie das [Completed](completedate.md) -Element festlegen oder das [Status](status.md) -Element auf **Completed**festlegen.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-120">Setting **PercentComplete** to 100 has the same effect as setting the [CompleteDate](completedate.md) element or setting the [Status](status.md) element to **Completed**.</span></span> <span data-ttu-id="ef6e0-121">In einer Anforderung, die mindestens zwei dieser Eigenschaften festlegt, bestimmt die zuletzt verarbeitete Eigenschaft den Wert, der für diese Elemente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-121">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="ef6e0-122">Wenn beispielsweise **PercentComplete** 100 ist, das [Completed](completedate.md) -Objekt vom 1. Januar 2007 und [der Status](status.md) notstartedfestgelegt ist und die Eigenschaften in dieser Reihenfolge gestreamt werden, wird der [Status](status.md) des Vorgangs auf notstartedfestgelegt, das Endergebnis [auf](completedate.md) **null**und **PercentComplete** auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-122">For example, if **PercentComplete** is 100, [CompleteDate](completedate.md) is January 1, 2007, and [Status](status.md) is NotStarted, and the properties are streamed in this order, the effect will be to set the [Status](status.md) of the task to NotStarted, the [CompleteDate](completedate.md) to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="ef6e0-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ef6e0-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef6e0-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ef6e0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef6e0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef6e0-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef6e0-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef6e0-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ef6e0-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ef6e0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef6e0-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef6e0-128">Validation File</span></span>  <br/> |<span data-ttu-id="ef6e0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef6e0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef6e0-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ef6e0-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef6e0-131">False</span><span class="sxs-lookup"><span data-stu-id="ef6e0-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef6e0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef6e0-132">See also</span></span>



- [<span data-ttu-id="ef6e0-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ef6e0-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ef6e0-134">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ef6e0-134">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="ef6e0-135">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="ef6e0-135">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

