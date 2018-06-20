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
description: Das Räume-Element ist eine Liste von einem oder mehreren Elementen, die Besprechungsräumen darstellen.
ms.openlocfilehash: e95112d3d565da29c309e45710ffc0ea9b4d5064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831249"
---
# <a name="rooms"></a><span data-ttu-id="ef511-103">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="ef511-103">Rooms</span></span>

<span data-ttu-id="ef511-104">Das **Räume** -Element ist eine Liste von einem oder mehreren Elementen, die Besprechungsräumen darstellen.</span><span class="sxs-lookup"><span data-stu-id="ef511-104">The **Rooms** element is a list of one or more elements that represent meeting rooms.</span></span> 
  
[<span data-ttu-id="ef511-105">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="ef511-105">GetRoomsResponse</span></span>](getroomsresponse.md)
  
[<span data-ttu-id="ef511-106">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="ef511-106">Rooms</span></span>](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 <span data-ttu-id="ef511-107">**ArrayOfRoomsType**</span><span class="sxs-lookup"><span data-stu-id="ef511-107">**ArrayOfRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef511-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef511-108">Attributes and elements</span></span>

<span data-ttu-id="ef511-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef511-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef511-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef511-110">Attributes</span></span>

<span data-ttu-id="ef511-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef511-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef511-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef511-112">Child elements</span></span>

|<span data-ttu-id="ef511-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef511-113">**Element**</span></span>|<span data-ttu-id="ef511-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef511-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef511-115">Raum</span><span class="sxs-lookup"><span data-stu-id="ef511-115">Room</span></span>](room.md) <br/> |<span data-ttu-id="ef511-116">Definiert eine e-Mail-Adresse und den Anzeigenamen, die einen Besprechungsraum darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef511-116">Defines an e-mail address and display name that represents a meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef511-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef511-117">Parent elements</span></span>

|<span data-ttu-id="ef511-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef511-118">**Element**</span></span>|<span data-ttu-id="ef511-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef511-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef511-120">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="ef511-120">GetRoomsResponse</span></span>](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a><span data-ttu-id="ef511-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef511-121">Remarks</span></span>

<span data-ttu-id="ef511-122">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef511-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef511-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ef511-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef511-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef511-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef511-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef511-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ef511-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ef511-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef511-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef511-127">Validation File</span></span>  <br/> |<span data-ttu-id="ef511-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef511-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef511-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ef511-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef511-130">False</span><span class="sxs-lookup"><span data-stu-id="ef511-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef511-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef511-131">See also</span></span>



[<span data-ttu-id="ef511-132">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ef511-132">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="ef511-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ef511-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

