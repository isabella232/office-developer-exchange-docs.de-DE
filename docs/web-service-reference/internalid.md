---
title: Interne-Nr
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternalId
api_type:
- schema
ms.assetid: c179db1a-95c9-40da-bd3f-0bed548c0325
description: Das Internal-ID-Element stellt einen ganzzahligen Wert für die Ereignis Identifikation dar.
ms.openlocfilehash: 66d5852e104de843911b46a225154ebd991e2220
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459938"
---
# <a name="internalid"></a><span data-ttu-id="e67fc-103">Interne-Nr</span><span class="sxs-lookup"><span data-stu-id="e67fc-103">InternalId</span></span>

<span data-ttu-id="e67fc-104">Das **internal** -ID-Element stellt einen ganzzahligen Wert für die Ereignis Identifikation dar.</span><span class="sxs-lookup"><span data-stu-id="e67fc-104">The **InternalId** element represents an integer value for the event identification.</span></span> 
  
```XML
<InternalId/>
```

 <span data-ttu-id="e67fc-105">**nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e67fc-105">**nonNegativeInteger**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e67fc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e67fc-106">Attributes and elements</span></span>

<span data-ttu-id="e67fc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e67fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e67fc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e67fc-108">Attributes</span></span>

<span data-ttu-id="e67fc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e67fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e67fc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e67fc-110">Child elements</span></span>

<span data-ttu-id="e67fc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e67fc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e67fc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e67fc-112">Parent elements</span></span>

|<span data-ttu-id="e67fc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e67fc-113">**Element**</span></span>|<span data-ttu-id="e67fc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e67fc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e67fc-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="e67fc-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="e67fc-116">Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="e67fc-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e67fc-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e67fc-117">Text value</span></span>

<span data-ttu-id="e67fc-118">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e67fc-118">A text value that represents an integer is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e67fc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e67fc-119">Remarks</span></span>

<span data-ttu-id="e67fc-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e67fc-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e67fc-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e67fc-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e67fc-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="e67fc-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e67fc-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e67fc-123">Schema Name</span></span>  <br/> |<span data-ttu-id="e67fc-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e67fc-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="e67fc-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e67fc-125">Validation File</span></span>  <br/> |<span data-ttu-id="e67fc-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e67fc-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e67fc-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e67fc-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="e67fc-128">False</span><span class="sxs-lookup"><span data-stu-id="e67fc-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e67fc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e67fc-129">See also</span></span>



- [<span data-ttu-id="e67fc-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e67fc-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

