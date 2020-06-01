---
title: MaximumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: Das MaximumSize-Element stellt die maximale Größe dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 250e0c6aed37b934f5cf6eaed9d93b9f56159d93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461751"
---
# <a name="maximumsize"></a><span data-ttu-id="fd283-103">MaximumSize</span><span class="sxs-lookup"><span data-stu-id="fd283-103">MaximumSize</span></span>

<span data-ttu-id="fd283-104">Das **MaximumSize** -Element stellt die maximale Größe dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fd283-104">The **MaximumSize** element represents the maximum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<Maximum/>
```

 <span data-ttu-id="fd283-105">**int**</span><span class="sxs-lookup"><span data-stu-id="fd283-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd283-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fd283-106">Attributes and elements</span></span>

<span data-ttu-id="fd283-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fd283-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd283-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd283-108">Attributes</span></span>

<span data-ttu-id="fd283-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fd283-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd283-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd283-110">Child elements</span></span>

<span data-ttu-id="fd283-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fd283-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd283-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd283-112">Parent elements</span></span>

|<span data-ttu-id="fd283-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd283-113">**Element**</span></span>|<span data-ttu-id="fd283-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd283-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd283-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="fd283-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="fd283-116">Gibt die Mindest-und Höchstgröße an, die eingehende Nachrichten aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="fd283-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fd283-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="fd283-117">Text value</span></span>

<span data-ttu-id="fd283-118">Der Textwert ist eine ganze Zahl, die die maximale Größe der Nachricht in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="fd283-118">The text value is an integer that identifies the maximum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd283-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd283-119">Remarks</span></span>

<span data-ttu-id="fd283-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fd283-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd283-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fd283-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd283-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd283-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fd283-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fd283-123">Schema Name</span></span>  <br/> |<span data-ttu-id="fd283-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fd283-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fd283-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fd283-125">Validation File</span></span>  <br/> |<span data-ttu-id="fd283-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fd283-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fd283-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fd283-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd283-128">True</span><span class="sxs-lookup"><span data-stu-id="fd283-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd283-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd283-129">See also</span></span>



[<span data-ttu-id="fd283-130">Minimum Size</span><span class="sxs-lookup"><span data-stu-id="fd283-130">MinimumSize</span></span>](minimumsize.md)


- [<span data-ttu-id="fd283-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd283-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

