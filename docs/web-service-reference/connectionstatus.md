---
title: Den ConnectionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionStatus
api_type:
- schema
ms.assetid: 4300f9d6-8bf9-48c2-9f07-d80197864e17
description: Das den ConnectionStatus-Element enthält eine Textbeschreibung des Status eines Streaming-Abonnements.
ms.openlocfilehash: 928537201041950011ae06444e3c412228d252ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462717"
---
# <a name="connectionstatus"></a><span data-ttu-id="397c7-103">Den ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="397c7-103">ConnectionStatus</span></span>

<span data-ttu-id="397c7-104">Das **den ConnectionStatus** -Element enthält eine Textbeschreibung des Status eines Streaming-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="397c7-104">The **ConnectionStatus** element provides a text description of the status of a streaming subscription.</span></span> 
  
```xml
<ConnectionStatus>OK or Closed</ConnectionStatus>
```

 <span data-ttu-id="397c7-105">**ConnectionStatusType**</span><span class="sxs-lookup"><span data-stu-id="397c7-105">**ConnectionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="397c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="397c7-106">Attributes and elements</span></span>

<span data-ttu-id="397c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="397c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="397c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="397c7-108">Attributes</span></span>

<span data-ttu-id="397c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="397c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="397c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="397c7-110">Child elements</span></span>

<span data-ttu-id="397c7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="397c7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="397c7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="397c7-112">Parent elements</span></span>

|<span data-ttu-id="397c7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="397c7-113">**Element**</span></span>|<span data-ttu-id="397c7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="397c7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="397c7-115">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="397c7-115">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="397c7-116">Enthält den Status und das Ergebnis einer einzelnen [GetStreamingEvents-Vorgangs](getstreamingevents-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="397c7-116">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="397c7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="397c7-117">Text value</span></span>

<span data-ttu-id="397c7-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="397c7-118">A text value is required.</span></span> <span data-ttu-id="397c7-119">Im folgenden sind die möglichen Text Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="397c7-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="397c7-120">OK</span><span class="sxs-lookup"><span data-stu-id="397c7-120">OK</span></span>
    
- <span data-ttu-id="397c7-121">Geschlossen</span><span class="sxs-lookup"><span data-stu-id="397c7-121">Closed</span></span>
    
## <a name="remarks"></a><span data-ttu-id="397c7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="397c7-122">Remarks</span></span>

<span data-ttu-id="397c7-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="397c7-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="397c7-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="397c7-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="397c7-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="397c7-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="397c7-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="397c7-126">Schema Name</span></span>  <br/> |<span data-ttu-id="397c7-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="397c7-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="397c7-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="397c7-128">Validation File</span></span>  <br/> |<span data-ttu-id="397c7-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="397c7-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="397c7-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="397c7-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="397c7-131">False</span><span class="sxs-lookup"><span data-stu-id="397c7-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="397c7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="397c7-132">See also</span></span>



[<span data-ttu-id="397c7-133">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="397c7-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="397c7-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="397c7-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

