---
title: MonthlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MonthlyRegeneration
api_type:
- schema
ms.assetid: 9a52ca97-a663-41fe-b61a-61d8c53833ca
description: Das MonthlyRegeneration-Element beschreibt die Häufigkeit in Monaten, für die die Aufgabe neu generiert wird.
ms.openlocfilehash: c941bc2606790646d2797df27c854996901c0bc6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462738"
---
# <a name="monthlyregeneration"></a><span data-ttu-id="ad88c-103">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="ad88c-103">MonthlyRegeneration</span></span>

<span data-ttu-id="ad88c-104">Das **MonthlyRegeneration** -Element beschreibt die Häufigkeit in Monaten, für die die Aufgabe neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad88c-104">The **MonthlyRegeneration** element describes the frequency, in months, of which task is regenerated.</span></span> 
  
```xml
<MonthlyRegeneration>
   <Interval/>
</MonthlyRegeneration>
```

 <span data-ttu-id="ad88c-105">**MonthlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="ad88c-105">**MonthlyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad88c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ad88c-106">Attributes and elements</span></span>

<span data-ttu-id="ad88c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad88c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad88c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad88c-108">Attributes</span></span>

<span data-ttu-id="ad88c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad88c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad88c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad88c-110">Child elements</span></span>

|<span data-ttu-id="ad88c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad88c-111">**Element**</span></span>|<span data-ttu-id="ad88c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad88c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad88c-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="ad88c-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="ad88c-114">Definiert das Intervall zwischen zwei aufeinander folgenden wiederkehrenden Elementen in Monaten.</span><span class="sxs-lookup"><span data-stu-id="ad88c-114">Defines the interval, in months, between two consecutive recurring items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad88c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad88c-115">Parent elements</span></span>

|<span data-ttu-id="ad88c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad88c-116">**Element**</span></span>|<span data-ttu-id="ad88c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad88c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad88c-118">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="ad88c-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="ad88c-119">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ad88c-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad88c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad88c-120">Remarks</span></span>

<span data-ttu-id="ad88c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ad88c-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad88c-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ad88c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad88c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad88c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad88c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ad88c-124">Schema name</span></span>  <br/> |<span data-ttu-id="ad88c-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ad88c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ad88c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ad88c-126">Validation file</span></span>  <br/> |<span data-ttu-id="ad88c-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ad88c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad88c-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ad88c-128">Can be empty</span></span>  <br/> |<span data-ttu-id="ad88c-129">False</span><span class="sxs-lookup"><span data-stu-id="ad88c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad88c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad88c-130">See also</span></span>



- [<span data-ttu-id="ad88c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ad88c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

