---
title: ReturnQueueEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReturnQueueEvents
api_type:
- schema
ms.assetid: 69d22417-320c-4c6f-9fb4-2020f2480bb2
description: Das ReturnQueueEvents-Element gibt an, dass die Person, die die Aufgabe ausführt, eine privilegierte Rolle besitzt.
ms.openlocfilehash: 9d07bc8c3d32f1cd532febaf4ae04e4a2d31d243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466591"
---
# <a name="returnqueueevents"></a><span data-ttu-id="2d8e4-103">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="2d8e4-103">ReturnQueueEvents</span></span>

<span data-ttu-id="2d8e4-104">Das **ReturnQueueEvents** -Element gibt an, dass die Person, die die Aufgabe ausführt, eine privilegierte Rolle besitzt.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-104">The **ReturnQueueEvents** element indicates that the person who is running the task is in a privileged role.</span></span> 
  
```XML
<ReturnQueueEvents>true | false</ReturnQueueEvents>
```

 <span data-ttu-id="2d8e4-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="2d8e4-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d8e4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2d8e4-106">Attributes and elements</span></span>

<span data-ttu-id="2d8e4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d8e4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d8e4-108">Attributes</span></span>

<span data-ttu-id="2d8e4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d8e4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d8e4-110">Child elements</span></span>

<span data-ttu-id="2d8e4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d8e4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d8e4-112">Parent elements</span></span>

|<span data-ttu-id="2d8e4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d8e4-113">**Element**</span></span>|<span data-ttu-id="2d8e4-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2d8e4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d8e4-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="2d8e4-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="2d8e4-116">Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d8e4-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="2d8e4-117">Text value</span></span>

<span data-ttu-id="2d8e4-118">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-118">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="2d8e4-119">Der Wert **true** gibt an, dass die Person, die die Aufgabe ausführt, eine privilegierte Rolle hat; der Wert **false** gibt an, dass die Person, die die Aufgabe ausführt, keine privilegierte Rolle hat.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-119">A value of **true** indicates that the person who is running the task is in a privileged role; a value of **false** indicates that the person who is running the task is not in a privileged role.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d8e4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d8e4-120">Remarks</span></span>

<span data-ttu-id="2d8e4-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2d8e4-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d8e4-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2d8e4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d8e4-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d8e4-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d8e4-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2d8e4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2d8e4-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2d8e4-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d8e4-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2d8e4-126">Validation File</span></span>  <br/> |<span data-ttu-id="2d8e4-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2d8e4-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d8e4-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2d8e4-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d8e4-129">False</span><span class="sxs-lookup"><span data-stu-id="2d8e4-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d8e4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d8e4-130">See also</span></span>



[<span data-ttu-id="2d8e4-131">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2d8e4-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="2d8e4-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2d8e4-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

