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
description: Das Status-Element stellt den Status eines Aufgabenelements dar.
ms.openlocfilehash: 5d022827990b96fd8790ae9566ef49028ebe404c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459959"
---
# <a name="status"></a><span data-ttu-id="6fbcb-103">Status</span><span class="sxs-lookup"><span data-stu-id="6fbcb-103">Status</span></span>

<span data-ttu-id="6fbcb-104">Das **Status** -Element stellt den Status eines Aufgabenelements dar.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-104">The **Status** element represents the status of a task item.</span></span> 
  
```xml
<Status/>
```

 <span data-ttu-id="6fbcb-105">**TaskStatusType**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-105">**TaskStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6fbcb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6fbcb-106">Attributes and elements</span></span>

<span data-ttu-id="6fbcb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fbcb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fbcb-108">Attributes</span></span>

<span data-ttu-id="6fbcb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6fbcb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fbcb-110">Child elements</span></span>

<span data-ttu-id="6fbcb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6fbcb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fbcb-112">Parent elements</span></span>

|<span data-ttu-id="6fbcb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-113">**Element**</span></span>|<span data-ttu-id="6fbcb-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fbcb-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6fbcb-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="6fbcb-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6fbcb-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="6fbcb-117">Text value</span></span>

<span data-ttu-id="6fbcb-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-118">A text value is required.</span></span> <span data-ttu-id="6fbcb-119">Im folgenden sind die möglichen Text Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="6fbcb-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="6fbcb-120">NotStarted</span><span class="sxs-lookup"><span data-stu-id="6fbcb-120">NotStarted</span></span>
    
- <span data-ttu-id="6fbcb-121">InProgress</span><span class="sxs-lookup"><span data-stu-id="6fbcb-121">InProgress</span></span>
    
- <span data-ttu-id="6fbcb-122">Completed</span><span class="sxs-lookup"><span data-stu-id="6fbcb-122">Completed</span></span>
    
- <span data-ttu-id="6fbcb-123">WaitingOnOthers</span><span class="sxs-lookup"><span data-stu-id="6fbcb-123">WaitingOnOthers</span></span>
    
- <span data-ttu-id="6fbcb-124">Latenten</span><span class="sxs-lookup"><span data-stu-id="6fbcb-124">Deferred</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fbcb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fbcb-125">Remarks</span></span>

<span data-ttu-id="6fbcb-126">Das Festlegen von " [abgeschlossen](completedate.md) " hat denselben Effekt wie das Festlegen von [PercentComplete](percentcomplete.md) auf "100" oder " **Status** to **Completed**".</span><span class="sxs-lookup"><span data-stu-id="6fbcb-126">Setting [CompleteDate](completedate.md) has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or **Status** to **Completed**.</span></span> <span data-ttu-id="6fbcb-127">In einer Anforderung, die mindestens zwei dieser Eigenschaften festlegt, bestimmt die zuletzt verarbeitete Eigenschaft den Wert, der für diese Elemente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-127">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="6fbcb-128">Beispiel: Wenn **PercentComplete** 100 ist, das **Completed** -Objekt 1/1/2007 und der **Status** notstartedfestgelegt ist und die Eigenschaften in dieser Reihenfolge gestreamt werden, wird der **Status** der Aufgabe auf notstartedfestgelegt, das Endergebnis auf **null**und **PercentComplete** auf **CompleteDate** 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-128">For example, if **PercentComplete** is 100, **CompleteDate** is 1/1/2007, and **Status** is NotStarted, and the properties are streamed in this order, the effect will be to set the **Status** of the task to NotStarted, the **CompleteDate** to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="6fbcb-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6fbcb-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6fbcb-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fbcb-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fbcb-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6fbcb-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6fbcb-132">Schema Name</span></span>  <br/> |<span data-ttu-id="6fbcb-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6fbcb-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="6fbcb-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6fbcb-134">Validation File</span></span>  <br/> |<span data-ttu-id="6fbcb-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6fbcb-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6fbcb-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6fbcb-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="6fbcb-137">False</span><span class="sxs-lookup"><span data-stu-id="6fbcb-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fbcb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fbcb-138">See also</span></span>



- [<span data-ttu-id="6fbcb-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6fbcb-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6fbcb-140">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6fbcb-140">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="6fbcb-141">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="6fbcb-141">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

