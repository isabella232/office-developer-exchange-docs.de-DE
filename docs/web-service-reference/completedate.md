---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: Das Completed-Element stellt das Datum dar, an dem ein Element abgeschlossen wurde.
ms.openlocfilehash: fff3d5d3105bf63c9cdd34cbcf828d57ca287b86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461422"
---
# <a name="completedate"></a><span data-ttu-id="d7b76-103">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="d7b76-103">CompleteDate</span></span>

<span data-ttu-id="d7b76-104">Das **Completed** -Element stellt das Datum dar, an dem ein Element abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d7b76-104">The **CompleteDate** element represents the date on which an item was completed.</span></span> 
  
```xml
<CompleteDate/>
```

 <span data-ttu-id="d7b76-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="d7b76-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7b76-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d7b76-106">Attributes and elements</span></span>

<span data-ttu-id="d7b76-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d7b76-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7b76-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d7b76-108">Attributes</span></span>

<span data-ttu-id="d7b76-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d7b76-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7b76-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7b76-110">Child elements</span></span>

<span data-ttu-id="d7b76-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d7b76-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d7b76-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7b76-112">Parent elements</span></span>

|<span data-ttu-id="d7b76-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7b76-113">**Element**</span></span>|<span data-ttu-id="d7b76-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7b76-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7b76-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="d7b76-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="d7b76-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d7b76-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d7b76-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d7b76-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="d7b76-118">Gibt ein Flag für ein Postfachelement an.</span><span class="sxs-lookup"><span data-stu-id="d7b76-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d7b76-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="d7b76-119">Text value</span></span>

<span data-ttu-id="d7b76-120">Ein Textwert, der das Datum und die Uhrzeit darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7b76-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7b76-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7b76-121">Remarks</span></span>

<span data-ttu-id="d7b76-122">Das Festlegen von " **abgeschlossen** " hat denselben Effekt wie das Festlegen von [PercentComplete](percentcomplete.md) auf "100" oder " [Status](status.md) to **Completed**".</span><span class="sxs-lookup"><span data-stu-id="d7b76-122">Setting **CompleteDate** has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or [Status](status.md) to **Completed**.</span></span> <span data-ttu-id="d7b76-123">In einer Anforderung, die mindestens zwei dieser Eigenschaften festlegt, bestimmt die zuletzt verarbeitete Eigenschaft den Wert, der für diese Elemente festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d7b76-123">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="d7b76-124">Wenn beispielsweise [PercentComplete](percentcomplete.md) 100 ist, das **Completed** -Objekt vom 1. Januar 2007 und [Status](status.md) der Status **notstartedfestgelegt**ist und die Eigenschaften in dieser Reihenfolge gestreamt werden, wird der [Status](status.md) des Vorgangs auf **notstartedfestgelegt** [, das](completedate.md) Endergebnis auf **null**und [PercentComplete](percentcomplete.md) auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7b76-124">For example, if [PercentComplete](percentcomplete.md) is 100, **CompleteDate** is January 1, 2007, and [Status](status.md) is **NotStarted**, and the properties are streamed in that order, the effect will be to set the [Status](status.md) of the task to **NotStarted**, the [CompleteDate](completedate.md) to **null**, and [PercentComplete](percentcomplete.md) to 0.</span></span> 
  
<span data-ttu-id="d7b76-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d7b76-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7b76-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d7b76-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7b76-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7b76-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7b76-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d7b76-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d7b76-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d7b76-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d7b76-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d7b76-130">Validation File</span></span>  <br/> |<span data-ttu-id="d7b76-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d7b76-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7b76-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d7b76-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7b76-133">False</span><span class="sxs-lookup"><span data-stu-id="d7b76-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7b76-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7b76-134">See also</span></span>



- [<span data-ttu-id="d7b76-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d7b76-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d7b76-136">Erstellen von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="d7b76-136">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="d7b76-137">Deleting Tasks</span><span class="sxs-lookup"><span data-stu-id="d7b76-137">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

