---
title: BaseOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseOffset
api_type:
- schema
ms.assetid: 0ffad7a6-8e1b-452b-9d87-8e0f6c77f0a6
description: Das BaseOffset-Element darstellt, die stündlich offset von koordinierte Weltzeit (UTC) für die aktuelle Zeitzone.
ms.openlocfilehash: 56fc136537b7d5370074a0e6d492f214da3fd960
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757435"
---
# <a name="baseoffset"></a><span data-ttu-id="461fe-103">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="461fe-103">BaseOffset</span></span>

<span data-ttu-id="461fe-104">Das **BaseOffset** -Element darstellt, die stündlich offset von koordinierte Weltzeit (UTC) für die aktuelle Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="461fe-104">The **BaseOffset** element represents the hourly offset from Coordinated Universal Time (UTC) for the current time zone.</span></span> 
  
```xml
<BaseOffset/>
```

 <span data-ttu-id="461fe-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="461fe-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="461fe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="461fe-106">Attributes and elements</span></span>

<span data-ttu-id="461fe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="461fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="461fe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="461fe-108">Attributes</span></span>

<span data-ttu-id="461fe-109">Keine</span><span class="sxs-lookup"><span data-stu-id="461fe-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="461fe-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="461fe-110">Child elements</span></span>

<span data-ttu-id="461fe-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="461fe-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="461fe-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="461fe-112">Parent elements</span></span>

|<span data-ttu-id="461fe-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="461fe-113">**Element**</span></span>|<span data-ttu-id="461fe-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="461fe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="461fe-115">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="461fe-115">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="461fe-116">Stellt die Zeitzone des Speicherorts, in die Besprechung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="461fe-116">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="461fe-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="461fe-117">Remarks</span></span>

<span data-ttu-id="461fe-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="461fe-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="461fe-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="461fe-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="461fe-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="461fe-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="461fe-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="461fe-121">Schema Name</span></span>  <br/> |<span data-ttu-id="461fe-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="461fe-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="461fe-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="461fe-123">Validation File</span></span>  <br/> |<span data-ttu-id="461fe-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="461fe-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="461fe-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="461fe-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="461fe-126">False</span><span class="sxs-lookup"><span data-stu-id="461fe-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="461fe-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="461fe-127">See also</span></span>



- [<span data-ttu-id="461fe-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="461fe-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

