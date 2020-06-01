---
title: Raum
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Room
api_type:
- schema
ms.assetid: a2cde8b8-2d31-4ebf-8171-f4dfd650d079
description: Das Room-Element stellt einen Besprechungsraum dar.
ms.openlocfilehash: 3d5d587853e435016fdff6b9d268892a35fea825
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460533"
---
# <a name="room"></a><span data-ttu-id="40850-103">Raum</span><span class="sxs-lookup"><span data-stu-id="40850-103">Room</span></span>

<span data-ttu-id="40850-104">Das **Room** -Element stellt einen Besprechungsraum dar.</span><span class="sxs-lookup"><span data-stu-id="40850-104">The **Room** element represents a meeting room.</span></span> 
  
[<span data-ttu-id="40850-105">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="40850-105">Rooms</span></span>](rooms.md)
  
[<span data-ttu-id="40850-106">Raum</span><span class="sxs-lookup"><span data-stu-id="40850-106">Room</span></span>](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 <span data-ttu-id="40850-107">**Zimmertyp**</span><span class="sxs-lookup"><span data-stu-id="40850-107">**RoomType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40850-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="40850-108">Attributes and elements</span></span>

<span data-ttu-id="40850-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="40850-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40850-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="40850-110">Attributes</span></span>

<span data-ttu-id="40850-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="40850-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40850-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40850-112">Child elements</span></span>

|<span data-ttu-id="40850-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="40850-113">**Element**</span></span>|<span data-ttu-id="40850-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40850-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40850-115">ID (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="40850-115">Id (EmailAddressType)</span></span>](id-emailaddresstype.md) <br/> |<span data-ttu-id="40850-116">Ein Bezeichner, der eine e-Mail-Adresse und einen Anzeigenamen enthält, der den Besprechungsraum darstellt.</span><span class="sxs-lookup"><span data-stu-id="40850-116">An identifier that contains an email address and display name that represents the meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="40850-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40850-117">Parent elements</span></span>

|<span data-ttu-id="40850-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="40850-118">**Element**</span></span>|<span data-ttu-id="40850-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40850-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40850-120">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="40850-120">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="40850-121">Definiert eine Liste von Besprechungsräumen, die einem gemeinsamen Feature zugeordnet sind, beispielsweise sich im selben Gebäude befinden.</span><span class="sxs-lookup"><span data-stu-id="40850-121">Defines a list of meeting rooms associated with a common feature, such as being located in the same building.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40850-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40850-122">Remarks</span></span>

<span data-ttu-id="40850-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="40850-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40850-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="40850-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40850-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="40850-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40850-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="40850-126">Schema Name</span></span>  <br/> |<span data-ttu-id="40850-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="40850-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="40850-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="40850-128">Validation File</span></span>  <br/> |<span data-ttu-id="40850-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40850-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40850-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="40850-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="40850-131">False</span><span class="sxs-lookup"><span data-stu-id="40850-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40850-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40850-132">See also</span></span>



[<span data-ttu-id="40850-133">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="40850-133">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="40850-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="40850-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

