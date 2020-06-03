---
title: IDs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Ids
api_type:
- schema
ms.assetid: c54cdeaf-6761-4d1a-a329-fb279f0e2a64
description: Das IDs-Element enthält ein Array von Zeit Zonen Definitions Bezeichnern.
ms.openlocfilehash: 1c5a6974c8d3abc318ff122f3db09d8c3472dc65
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457620"
---
# <a name="ids"></a><span data-ttu-id="363c4-103">IDs</span><span class="sxs-lookup"><span data-stu-id="363c4-103">Ids</span></span>

<span data-ttu-id="363c4-104">Das **IDs** -Element enthält ein Array von Zeit Zonen Definitions Bezeichnern.</span><span class="sxs-lookup"><span data-stu-id="363c4-104">The **Ids** element contains an array of time zone definition identifiers.</span></span> 
  
```XML
<Ids>
   <Id/>
</Ids>
```

 <span data-ttu-id="363c4-105">**NonEmptyArrayOfTimeZoneIdType**</span><span class="sxs-lookup"><span data-stu-id="363c4-105">**NonEmptyArrayOfTimeZoneIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="363c4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="363c4-106">Attributes and elements</span></span>

<span data-ttu-id="363c4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="363c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="363c4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="363c4-108">Attributes</span></span>

<span data-ttu-id="363c4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="363c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="363c4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="363c4-110">Child elements</span></span>

|<span data-ttu-id="363c4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="363c4-111">**Element**</span></span>|<span data-ttu-id="363c4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="363c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="363c4-113">ID (Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="363c4-113">Id (TimeZone)</span></span>](id-timezone.md) <br/> |<span data-ttu-id="363c4-114">Das-Element, das eine einzelne Zeitzonendefinition identifiziert.</span><span class="sxs-lookup"><span data-stu-id="363c4-114">The element that identifies a single time zone definition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="363c4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="363c4-115">Parent elements</span></span>

|<span data-ttu-id="363c4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="363c4-116">**Element**</span></span>|<span data-ttu-id="363c4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="363c4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="363c4-118">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="363c4-118">GetServerTimeZones</span></span>](getservertimezones.md) <br/> |<span data-ttu-id="363c4-119">Definiert eine Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="363c4-119">Defines a request to retrieve time zone definitions from the Exchange server.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="363c4-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="363c4-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="363c4-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="363c4-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="363c4-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="363c4-122">Schema Name</span></span>  <br/> |<span data-ttu-id="363c4-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="363c4-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="363c4-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="363c4-124">Validation File</span></span>  <br/> |<span data-ttu-id="363c4-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="363c4-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="363c4-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="363c4-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="363c4-127">False</span><span class="sxs-lookup"><span data-stu-id="363c4-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="363c4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="363c4-128">See also</span></span>



- [<span data-ttu-id="363c4-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="363c4-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

