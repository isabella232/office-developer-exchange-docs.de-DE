---
title: RoomLists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomLists
api_type:
- schema
ms.assetid: 2b190823-b11e-4635-97e4-3aba5865fd05
description: Das RoomLists-Element ist eine Liste mit einer oder mehreren Adressen, die eine Liste von Besprechungsräumen darstellen.
ms.openlocfilehash: 8f6393b617331e5878e48113c94ca3546cba095e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459048"
---
# <a name="roomlists"></a><span data-ttu-id="848d9-103">RoomLists</span><span class="sxs-lookup"><span data-stu-id="848d9-103">RoomLists</span></span>

<span data-ttu-id="848d9-104">Das **RoomLists** -Element ist eine Liste mit einer oder mehreren Adressen, die eine Liste von Besprechungsräumen darstellen.</span><span class="sxs-lookup"><span data-stu-id="848d9-104">The **RoomLists** element is a list of one or more addresses that represent a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="848d9-105">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="848d9-105">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
[<span data-ttu-id="848d9-106">RoomLists</span><span class="sxs-lookup"><span data-stu-id="848d9-106">RoomLists</span></span>](roomlists.md)
  
```xml
<RoomLists>   <Address/></RoomLists>
```

 <span data-ttu-id="848d9-107">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="848d9-107">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="848d9-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="848d9-108">Attributes and elements</span></span>

<span data-ttu-id="848d9-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="848d9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="848d9-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="848d9-110">Attributes</span></span>

<span data-ttu-id="848d9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="848d9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="848d9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="848d9-112">Child elements</span></span>

|<span data-ttu-id="848d9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="848d9-113">**Element**</span></span>|<span data-ttu-id="848d9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="848d9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="848d9-115">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="848d9-115">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="848d9-116">Definiert die e-Mail-Adresse und den Anzeigenamen, der die Raumliste darstellt.</span><span class="sxs-lookup"><span data-stu-id="848d9-116">Defines the e-mail address and display name that represents the room list.</span></span> <span data-ttu-id="848d9-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="848d9-117">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="848d9-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="848d9-118">Parent elements</span></span>

|<span data-ttu-id="848d9-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="848d9-119">**Element**</span></span>|<span data-ttu-id="848d9-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="848d9-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="848d9-121">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="848d9-121">GetRoomListsResponse</span></span>](getroomlistsresponse.md) <br/> |<span data-ttu-id="848d9-122">Enthält den Status und das Ergebnis einer [GetRoomLists-Vorgangs](getroomlists-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="848d9-122">Contains the status and result of a [GetRoomLists operation](getroomlists-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="848d9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="848d9-123">Remarks</span></span>

<span data-ttu-id="848d9-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="848d9-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="848d9-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="848d9-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="848d9-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="848d9-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="848d9-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="848d9-127">Schema Name</span></span>  <br/> |<span data-ttu-id="848d9-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="848d9-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="848d9-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="848d9-129">Validation File</span></span>  <br/> |<span data-ttu-id="848d9-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="848d9-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="848d9-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="848d9-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="848d9-132">False</span><span class="sxs-lookup"><span data-stu-id="848d9-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="848d9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="848d9-133">See also</span></span>



[<span data-ttu-id="848d9-134">GetRoomLists-Vorgang</span><span class="sxs-lookup"><span data-stu-id="848d9-134">GetRoomLists operation</span></span>](getroomlists-operation.md)


- [<span data-ttu-id="848d9-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="848d9-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

