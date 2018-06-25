---
title: Max
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: Max-Element stellt die maximale Größe, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.
ms.openlocfilehash: 37e3d377b105534fe34b54e262bd47bc450706da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830387"
---
# <a name="maximumsize"></a><span data-ttu-id="f0013-103">Max</span><span class="sxs-lookup"><span data-stu-id="f0013-103">MaximumSize</span></span>

<span data-ttu-id="f0013-104">**Max** -Element stellt die maximale Größe, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f0013-104">The **MaximumSize** element represents the maximum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<Maximum/>
```

 <span data-ttu-id="f0013-105">**int**</span><span class="sxs-lookup"><span data-stu-id="f0013-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0013-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f0013-106">Attributes and elements</span></span>

<span data-ttu-id="f0013-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f0013-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0013-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f0013-108">Attributes</span></span>

<span data-ttu-id="f0013-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f0013-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0013-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0013-110">Child elements</span></span>

<span data-ttu-id="f0013-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f0013-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f0013-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f0013-112">Parent elements</span></span>

|<span data-ttu-id="f0013-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0013-113">**Element**</span></span>|<span data-ttu-id="f0013-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0013-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0013-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="f0013-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="f0013-116">Gibt die minimale und maximale Größe, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f0013-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f0013-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="f0013-117">Text value</span></span>

<span data-ttu-id="f0013-118">Der Textwert ist eine ganze Zahl, die die maximale Größe der Nachricht in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="f0013-118">The text value is an integer that identifies the maximum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0013-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0013-119">Remarks</span></span>

<span data-ttu-id="f0013-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f0013-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0013-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f0013-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0013-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0013-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f0013-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f0013-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f0013-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f0013-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f0013-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f0013-125">Validation File</span></span>  <br/> |<span data-ttu-id="f0013-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f0013-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f0013-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f0013-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0013-128">True</span><span class="sxs-lookup"><span data-stu-id="f0013-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0013-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0013-129">See also</span></span>



[<span data-ttu-id="f0013-130">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="f0013-130">MinimumSize</span></span>](minimumsize.md)


- [<span data-ttu-id="f0013-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f0013-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

