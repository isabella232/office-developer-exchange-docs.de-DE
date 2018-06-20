---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: Das Element MinimumSize stellt die Mindestgröße, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.
ms.openlocfilehash: 4f80bac3b9226019ec3d726cd2d6430e02cac423
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830480"
---
# <a name="minimumsize"></a><span data-ttu-id="3c5a2-103">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="3c5a2-103">MinimumSize</span></span>

<span data-ttu-id="3c5a2-104">Das Element **MinimumSize** stellt die Mindestgröße, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="3c5a2-104">The **MinimumSize** element represents the minimum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<MinimumSize/>
```

 <span data-ttu-id="3c5a2-105">**int**</span><span class="sxs-lookup"><span data-stu-id="3c5a2-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c5a2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c5a2-106">Attributes and elements</span></span>

<span data-ttu-id="3c5a2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c5a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c5a2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c5a2-108">Attributes</span></span>

<span data-ttu-id="3c5a2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c5a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c5a2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c5a2-110">Child elements</span></span>

<span data-ttu-id="3c5a2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c5a2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3c5a2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c5a2-112">Parent elements</span></span>

|<span data-ttu-id="3c5a2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c5a2-113">**Element**</span></span>|<span data-ttu-id="3c5a2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c5a2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c5a2-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="3c5a2-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="3c5a2-116">Gibt die minimale und maximale Größe, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3c5a2-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3c5a2-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="3c5a2-117">Text value</span></span>

<span data-ttu-id="3c5a2-118">Der Textwert ist eine ganze Zahl, die die minimale Größe der Nachricht in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="3c5a2-118">The text value is an integer that identifies the minimum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c5a2-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c5a2-119">Remarks</span></span>

<span data-ttu-id="3c5a2-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3c5a2-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c5a2-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3c5a2-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c5a2-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c5a2-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3c5a2-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c5a2-123">Schema Name</span></span>  <br/> |<span data-ttu-id="3c5a2-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3c5a2-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3c5a2-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c5a2-125">Validation File</span></span>  <br/> |<span data-ttu-id="3c5a2-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3c5a2-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3c5a2-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3c5a2-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c5a2-128">True</span><span class="sxs-lookup"><span data-stu-id="3c5a2-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c5a2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c5a2-129">See also</span></span>



[<span data-ttu-id="3c5a2-130">Max</span><span class="sxs-lookup"><span data-stu-id="3c5a2-130">MaximumSize</span></span>](maximumsize.md)


- [<span data-ttu-id="3c5a2-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3c5a2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

