---
title: GetRooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 82a737c7-da41-4777-8ad8-89851a0b602b
description: Das getrooms-Element ist das Stammelement in einer Anforderung zum Abrufen einer Liste von Räumen in einer bestimmten Raumliste.
ms.openlocfilehash: 77fde5980a03d4c0509344933b0901cb21ab7197
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458593"
---
# <a name="getrooms"></a><span data-ttu-id="9080b-103">GetRooms</span><span class="sxs-lookup"><span data-stu-id="9080b-103">GetRooms</span></span>

<span data-ttu-id="9080b-104">Das **getrooms** -Element ist das Stammelement in einer Anforderung zum Abrufen einer Liste von Räumen in einer bestimmten Raumliste.</span><span class="sxs-lookup"><span data-stu-id="9080b-104">The **GetRooms** element is the root element in a request to get a list of rooms within a particular room list.</span></span> 
  
```XML
<GetRooms>
   <RoomList/>
</GetRooms>
```

 <span data-ttu-id="9080b-105">**Getroomtype**</span><span class="sxs-lookup"><span data-stu-id="9080b-105">**GetRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9080b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9080b-106">Attributes and elements</span></span>

<span data-ttu-id="9080b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9080b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9080b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9080b-108">Attributes</span></span>

<span data-ttu-id="9080b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9080b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9080b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9080b-110">Child elements</span></span>

|<span data-ttu-id="9080b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9080b-111">**Element**</span></span>|<span data-ttu-id="9080b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9080b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9080b-113">RoomList</span><span class="sxs-lookup"><span data-stu-id="9080b-113">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="9080b-114">Stellt eine e-Mail-Adresse dar, die eine Liste von Besprechungsräumen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9080b-114">Represents an e-mail address that identifies a list of meeting rooms</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9080b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9080b-115">Parent elements</span></span>

<span data-ttu-id="9080b-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="9080b-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9080b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="9080b-117">Text value</span></span>

<span data-ttu-id="9080b-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="9080b-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9080b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9080b-119">Remarks</span></span>

<span data-ttu-id="9080b-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9080b-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9080b-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9080b-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9080b-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9080b-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9080b-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9080b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="9080b-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9080b-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9080b-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9080b-125">Validation File</span></span>  <br/> |<span data-ttu-id="9080b-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9080b-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9080b-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9080b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="9080b-128">False</span><span class="sxs-lookup"><span data-stu-id="9080b-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9080b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9080b-129">See also</span></span>



- [<span data-ttu-id="9080b-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9080b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

