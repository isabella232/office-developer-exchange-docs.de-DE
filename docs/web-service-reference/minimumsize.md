---
title: Minimum Size
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: Das Minimum Size-Element stellt die minimale Größe dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: b43a8b5916747c4e3e4ca9b66cf8b9d73f5f8942
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44464203"
---
# <a name="minimumsize"></a><span data-ttu-id="89149-103">Minimum Size</span><span class="sxs-lookup"><span data-stu-id="89149-103">MinimumSize</span></span>

<span data-ttu-id="89149-104">Das **Minimum Size** -Element stellt die minimale Größe dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="89149-104">The **MinimumSize** element represents the minimum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<MinimumSize/>
```

 <span data-ttu-id="89149-105">**int**</span><span class="sxs-lookup"><span data-stu-id="89149-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89149-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="89149-106">Attributes and elements</span></span>

<span data-ttu-id="89149-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="89149-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89149-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="89149-108">Attributes</span></span>

<span data-ttu-id="89149-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="89149-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89149-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89149-110">Child elements</span></span>

<span data-ttu-id="89149-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="89149-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89149-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89149-112">Parent elements</span></span>

|<span data-ttu-id="89149-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="89149-113">**Element**</span></span>|<span data-ttu-id="89149-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="89149-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89149-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="89149-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="89149-116">Gibt die Mindest-und Höchstgröße an, die eingehende Nachrichten aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="89149-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89149-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="89149-117">Text value</span></span>

<span data-ttu-id="89149-118">Der Textwert ist eine ganze Zahl, die die minimale Größe der Nachricht in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="89149-118">The text value is an integer that identifies the minimum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89149-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89149-119">Remarks</span></span>

<span data-ttu-id="89149-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="89149-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89149-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="89149-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89149-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="89149-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="89149-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="89149-123">Schema Name</span></span>  <br/> |<span data-ttu-id="89149-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="89149-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="89149-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="89149-125">Validation File</span></span>  <br/> |<span data-ttu-id="89149-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="89149-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="89149-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="89149-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="89149-128">True</span><span class="sxs-lookup"><span data-stu-id="89149-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89149-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89149-129">See also</span></span>



[<span data-ttu-id="89149-130">MaximumSize</span><span class="sxs-lookup"><span data-stu-id="89149-130">MaximumSize</span></span>](maximumsize.md)


- [<span data-ttu-id="89149-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="89149-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

