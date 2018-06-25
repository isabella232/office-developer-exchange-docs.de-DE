---
title: Status
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 80121e41-291b-4fc0-a55e-6f677d4b5fb5
description: Status-Element, das den Status eines Aufgabenelements darstellt.
ms.openlocfilehash: 224b61913a5ae8e5b4aa0d756a9f2488df2741bd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831584"
---
# <a name="status"></a><span data-ttu-id="1f117-103">Status</span><span class="sxs-lookup"><span data-stu-id="1f117-103">Status</span></span>

<span data-ttu-id="1f117-104">**Status** -Element, das den Status eines Aufgabenelements darstellt.</span><span class="sxs-lookup"><span data-stu-id="1f117-104">The **Status** element represents the status of a task item.</span></span> 
  
```xml
<Status/>
```

 <span data-ttu-id="1f117-105">**TaskStatusType**</span><span class="sxs-lookup"><span data-stu-id="1f117-105">**TaskStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f117-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f117-106">Attributes and elements</span></span>

<span data-ttu-id="1f117-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f117-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f117-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f117-108">Attributes</span></span>

<span data-ttu-id="1f117-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f117-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f117-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f117-110">Child elements</span></span>

<span data-ttu-id="1f117-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f117-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f117-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f117-112">Parent elements</span></span>

|<span data-ttu-id="1f117-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f117-113">**Element**</span></span>|<span data-ttu-id="1f117-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f117-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f117-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1f117-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="1f117-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1f117-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f117-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f117-117">Text value</span></span>

<span data-ttu-id="1f117-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1f117-118">A text value is required.</span></span> <span data-ttu-id="1f117-119">Es folgen die möglichen Textwerte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1f117-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="1f117-120">Nicht gestartet</span><span class="sxs-lookup"><span data-stu-id="1f117-120">NotStarted</span></span>
    
- <span data-ttu-id="1f117-121">InProgress</span><span class="sxs-lookup"><span data-stu-id="1f117-121">InProgress</span></span>
    
- <span data-ttu-id="1f117-122">Completed</span><span class="sxs-lookup"><span data-stu-id="1f117-122">Completed</span></span>
    
- <span data-ttu-id="1f117-123">WaitingOnOthers</span><span class="sxs-lookup"><span data-stu-id="1f117-123">WaitingOnOthers</span></span>
    
- <span data-ttu-id="1f117-124">Zurückgestellt</span><span class="sxs-lookup"><span data-stu-id="1f117-124">Deferred</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f117-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f117-125">Remarks</span></span>

<span data-ttu-id="1f117-126">Festlegen von [CompleteDate](completedate.md) hat die gleiche Auswirkung wie das [PercentComplete](percentcomplete.md) auf 100 oder **Status** auf **abgeschlossen**festlegen.</span><span class="sxs-lookup"><span data-stu-id="1f117-126">Setting [CompleteDate](completedate.md) has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or **Status** to **Completed**.</span></span> <span data-ttu-id="1f117-127">In einer Anforderung, dass mindestens zwei Sätze von diesen Eigenschaften, die letzte verarbeitete-Eigenschaft den Wert bestimmt wird, der für diese Elemente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1f117-127">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="1f117-128">Beispielsweise **PercentComplete** 100 **CompleteDate** ist, 1/1/2007 und **Status** ist nicht gestartet, und die Eigenschaften in dieser Reihenfolge gestreamt werden, der Effekt wird der **Status** des Vorgangs auf nicht gestartet, die **CompleteDate festgelegt werden **auf **null**und die **PercentComplete** auf 0.</span><span class="sxs-lookup"><span data-stu-id="1f117-128">For example, if **PercentComplete** is 100, **CompleteDate** is 1/1/2007, and **Status** is NotStarted, and the properties are streamed in this order, the effect will be to set the **Status** of the task to NotStarted, the **CompleteDate** to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="1f117-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1f117-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f117-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1f117-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f117-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f117-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f117-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f117-132">Schema Name</span></span>  <br/> |<span data-ttu-id="1f117-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1f117-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1f117-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f117-134">Validation File</span></span>  <br/> |<span data-ttu-id="1f117-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f117-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f117-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f117-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f117-137">False</span><span class="sxs-lookup"><span data-stu-id="1f117-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f117-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f117-138">See also</span></span>



- [<span data-ttu-id="1f117-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f117-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1f117-140">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="1f117-140">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="1f117-141">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="1f117-141">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

