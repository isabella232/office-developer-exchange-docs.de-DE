---
title: WeeklyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRegeneration
api_type:
- schema
ms.assetid: f128fdaa-ca3d-4614-8e55-f25e76a67b6c
description: Das WeeklyRegeneration-Element beschreibt die Häufigkeit in Wochen, in der eine Aufgabe neu generiert wird.
ms.openlocfilehash: dc333e051fd2213942e629a3f2764c72abfaeba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459749"
---
# <a name="weeklyregeneration"></a><span data-ttu-id="f7003-103">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="f7003-103">WeeklyRegeneration</span></span>

<span data-ttu-id="f7003-104">Das **WeeklyRegeneration** -Element beschreibt die Häufigkeit in Wochen, in der eine Aufgabe neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f7003-104">The **WeeklyRegeneration** element describes the frequency, in weeks, in which a task is regenerated.</span></span> 
  
```xml
<WeeklyRegeneration>
   <Interval/>
</WeeklyRegeneration>
```

 <span data-ttu-id="f7003-105">**WeeklyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="f7003-105">**WeeklyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7003-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f7003-106">Attributes and elements</span></span>

<span data-ttu-id="f7003-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7003-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7003-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f7003-108">Attributes</span></span>

<span data-ttu-id="f7003-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7003-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7003-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7003-110">Child elements</span></span>

|<span data-ttu-id="f7003-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7003-111">**Element**</span></span>|<span data-ttu-id="f7003-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7003-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7003-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="f7003-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="f7003-114">Definiert das Intervall in Wochen, seit der Vorgang abgeschlossen wurde, nach dem eine neue Aufgabe neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f7003-114">Defines the interval, in weeks, since the task was completed, after which a new task is regenerated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f7003-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7003-115">Parent elements</span></span>

|<span data-ttu-id="f7003-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7003-116">**Element**</span></span>|<span data-ttu-id="f7003-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7003-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7003-118">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="f7003-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="f7003-119">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="f7003-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7003-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7003-120">Remarks</span></span>

<span data-ttu-id="f7003-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f7003-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7003-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f7003-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7003-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7003-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f7003-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f7003-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f7003-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f7003-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f7003-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f7003-126">Validation File</span></span>  <br/> |<span data-ttu-id="f7003-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f7003-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f7003-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f7003-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7003-129">False</span><span class="sxs-lookup"><span data-stu-id="f7003-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7003-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7003-130">See also</span></span>



- [<span data-ttu-id="f7003-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f7003-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

