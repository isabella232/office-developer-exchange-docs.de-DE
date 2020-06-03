---
title: DailyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRegeneration
api_type:
- schema
ms.assetid: cafb57e4-c518-45e0-b565-2babd0dab1df
description: Das DailyRegeneration-Element beschreibt die Häufigkeit in Tagen, in der eine Aufgabe neu generiert wird.
ms.openlocfilehash: 518e4666031131f4a5fc80cc72c28a2110b468c5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462164"
---
# <a name="dailyregeneration"></a><span data-ttu-id="c1c4a-103">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="c1c4a-103">DailyRegeneration</span></span>

<span data-ttu-id="c1c4a-104">Das **DailyRegeneration** -Element beschreibt die Häufigkeit in Tagen, in der eine Aufgabe neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c1c4a-104">The **DailyRegeneration** element describes the frequency, in days, in which a task is regenerated.</span></span> 
  
```xml
<DailyRegeneration>
   <Interval/>
</DailyRegeneration>
```

<span data-ttu-id="c1c4a-105">**DailyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="c1c4a-105">**DailyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c1c4a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1c4a-106">Attributes and elements</span></span>

<span data-ttu-id="c1c4a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1c4a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1c4a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1c4a-108">Attributes</span></span>

<span data-ttu-id="c1c4a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1c4a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1c4a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1c4a-110">Child elements</span></span>

|<span data-ttu-id="c1c4a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1c4a-111">**Element**</span></span>|<span data-ttu-id="c1c4a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1c4a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1c4a-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="c1c4a-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="c1c4a-114">Definiert das Intervall in Tagen zwischen zwei aufeinander folgenden wiederkehrenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="c1c4a-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="c1c4a-115">Der Wert muss im Bereich von 1 bis 999 liegen.</span><span class="sxs-lookup"><span data-stu-id="c1c4a-115">The value must be in the range of 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1c4a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1c4a-116">Parent elements</span></span>

|<span data-ttu-id="c1c4a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1c4a-117">**Element**</span></span>|<span data-ttu-id="c1c4a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1c4a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1c4a-119">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c1c4a-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="c1c4a-120">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c1c4a-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1c4a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1c4a-121">Remarks</span></span>

<span data-ttu-id="c1c4a-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c1c4a-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1c4a-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c1c4a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1c4a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1c4a-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1c4a-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1c4a-125">Schema name</span></span>  <br/> |<span data-ttu-id="c1c4a-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c1c4a-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1c4a-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1c4a-127">Validation file</span></span>  <br/> |<span data-ttu-id="c1c4a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1c4a-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1c4a-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c1c4a-129">Can be empty</span></span>  <br/> |<span data-ttu-id="c1c4a-130">False</span><span class="sxs-lookup"><span data-stu-id="c1c4a-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1c4a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1c4a-131">See also</span></span>

- [<span data-ttu-id="c1c4a-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1c4a-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

