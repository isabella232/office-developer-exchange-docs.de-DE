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
description: Das Ids-Element enthält ein Array mit den IDs der Zeitzone-Definition.
ms.openlocfilehash: e4f8afb1292b3cb9f3990d4613b7461050976a59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829856"
---
# <a name="ids"></a><span data-ttu-id="4801a-103">IDs</span><span class="sxs-lookup"><span data-stu-id="4801a-103">Ids</span></span>

<span data-ttu-id="4801a-104">Das **Ids** -Element enthält ein Array mit den IDs der Zeitzone-Definition.</span><span class="sxs-lookup"><span data-stu-id="4801a-104">The **Ids** element contains an array of time zone definition identifiers.</span></span> 
  
```XML
<Ids>
   <Id/>
</Ids>
```

 <span data-ttu-id="4801a-105">**NonEmptyArrayOfTimeZoneIdType**</span><span class="sxs-lookup"><span data-stu-id="4801a-105">**NonEmptyArrayOfTimeZoneIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4801a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4801a-106">Attributes and elements</span></span>

<span data-ttu-id="4801a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4801a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4801a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4801a-108">Attributes</span></span>

<span data-ttu-id="4801a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4801a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4801a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4801a-110">Child elements</span></span>

|<span data-ttu-id="4801a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4801a-111">**Element**</span></span>|<span data-ttu-id="4801a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4801a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4801a-113">ID (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="4801a-113">Id (TimeZone)</span></span>](id-timezone.md) <br/> |<span data-ttu-id="4801a-114">Das Element, das eine einzelne Zeitzonendefinition identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4801a-114">The element that identifies a single time zone definition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4801a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4801a-115">Parent elements</span></span>

|<span data-ttu-id="4801a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4801a-116">**Element**</span></span>|<span data-ttu-id="4801a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4801a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4801a-118">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="4801a-118">GetServerTimeZones</span></span>](getservertimezones.md) <br/> |<span data-ttu-id="4801a-119">Definiert eine Anforderung zum Abrufen von Zeitzonendefinitionen vom Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="4801a-119">Defines a request to retrieve time zone definitions from the Exchange server.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="4801a-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4801a-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4801a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="4801a-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4801a-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4801a-122">Schema Name</span></span>  <br/> |<span data-ttu-id="4801a-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4801a-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4801a-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4801a-124">Validation File</span></span>  <br/> |<span data-ttu-id="4801a-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4801a-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4801a-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4801a-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="4801a-127">False</span><span class="sxs-lookup"><span data-stu-id="4801a-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4801a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4801a-128">See also</span></span>



- [<span data-ttu-id="4801a-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4801a-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

