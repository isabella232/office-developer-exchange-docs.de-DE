---
title: Chatrooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rooms
api_type:
- schema
ms.assetid: 57b6079a-3d83-4429-861e-c551e9e1a991
description: Das Rooms-Element ist eine Liste mit einem oder mehreren Elementen, die Besprechungsräume darstellen.
ms.openlocfilehash: f8b60a9680f6abba459ebecc96613abfdd93766d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466185"
---
# <a name="rooms"></a><span data-ttu-id="50ac1-103">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="50ac1-103">Rooms</span></span>

<span data-ttu-id="50ac1-104">Das **rooms** -Element ist eine Liste mit einem oder mehreren Elementen, die Besprechungsräume darstellen.</span><span class="sxs-lookup"><span data-stu-id="50ac1-104">The **Rooms** element is a list of one or more elements that represent meeting rooms.</span></span> 
  
[<span data-ttu-id="50ac1-105">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="50ac1-105">GetRoomsResponse</span></span>](getroomsresponse.md)
  
[<span data-ttu-id="50ac1-106">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="50ac1-106">Rooms</span></span>](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 <span data-ttu-id="50ac1-107">**ArrayOfRoomsType**</span><span class="sxs-lookup"><span data-stu-id="50ac1-107">**ArrayOfRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50ac1-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50ac1-108">Attributes and elements</span></span>

<span data-ttu-id="50ac1-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50ac1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50ac1-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="50ac1-110">Attributes</span></span>

<span data-ttu-id="50ac1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="50ac1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50ac1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50ac1-112">Child elements</span></span>

|<span data-ttu-id="50ac1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="50ac1-113">**Element**</span></span>|<span data-ttu-id="50ac1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50ac1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50ac1-115">Raum</span><span class="sxs-lookup"><span data-stu-id="50ac1-115">Room</span></span>](room.md) <br/> |<span data-ttu-id="50ac1-116">Definiert eine e-Mail-Adresse und einen Anzeigenamen, der einen Besprechungsraum darstellt.</span><span class="sxs-lookup"><span data-stu-id="50ac1-116">Defines an e-mail address and display name that represents a meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50ac1-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50ac1-117">Parent elements</span></span>

|<span data-ttu-id="50ac1-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="50ac1-118">**Element**</span></span>|<span data-ttu-id="50ac1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50ac1-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50ac1-120">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="50ac1-120">GetRoomsResponse</span></span>](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a><span data-ttu-id="50ac1-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50ac1-121">Remarks</span></span>

<span data-ttu-id="50ac1-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="50ac1-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50ac1-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="50ac1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50ac1-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="50ac1-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="50ac1-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50ac1-125">Schema Name</span></span>  <br/> |<span data-ttu-id="50ac1-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="50ac1-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="50ac1-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50ac1-127">Validation File</span></span>  <br/> |<span data-ttu-id="50ac1-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="50ac1-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="50ac1-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="50ac1-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="50ac1-130">False</span><span class="sxs-lookup"><span data-stu-id="50ac1-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50ac1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50ac1-131">See also</span></span>



[<span data-ttu-id="50ac1-132">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="50ac1-132">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="50ac1-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="50ac1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

