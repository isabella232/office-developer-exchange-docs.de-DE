---
title: NormalizedBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: Das NormalizedBodyType-Element gibt an, ob die normalisierte Body Text oder HTML-Format zurückgegeben wird.
ms.openlocfilehash: 33575594b22f972a9eb762dfac884fa91459f04a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830554"
---
# <a name="normalizedbodytype"></a><span data-ttu-id="97e75-103">NormalizedBodyType</span><span class="sxs-lookup"><span data-stu-id="97e75-103">NormalizedBodyType</span></span>

<span data-ttu-id="97e75-104">Das **NormalizedBodyType** -Element gibt an, ob die normalisierte Body Text oder HTML-Format zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="97e75-104">The **NormalizedBodyType** element specifies whether the normalized body is returned in text or HTML format.</span></span> 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 <span data-ttu-id="97e75-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="97e75-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97e75-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="97e75-106">Attributes and elements</span></span>

<span data-ttu-id="97e75-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="97e75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97e75-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="97e75-108">Attributes</span></span>

<span data-ttu-id="97e75-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="97e75-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="97e75-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97e75-110">Child elements</span></span>

<span data-ttu-id="97e75-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="97e75-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="97e75-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97e75-112">Parent elements</span></span>

[<span data-ttu-id="97e75-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="97e75-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="97e75-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="97e75-114">Text value</span></span>

<span data-ttu-id="97e75-115">Der Textwert des **NormalizedBodyType** -Elements gibt an, dass den normalisierten Textkörper Format zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="97e75-115">The text value of the **NormalizedBodyType** element indicates format the normalized body is returned in.</span></span> <span data-ttu-id="97e75-116">Die folgende Tabelle enthält die möglichen Werte für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="97e75-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="97e75-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="97e75-117">**Value**</span></span>|<span data-ttu-id="97e75-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97e75-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97e75-119">Am besten</span><span class="sxs-lookup"><span data-stu-id="97e75-119">Best</span></span>  <br/> |<span data-ttu-id="97e75-120">Die Antwort wird den inhaltlich verfügbaren Inhalt des Textkörpers zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="97e75-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="97e75-121">Dies ist nützlich, wenn nicht bekannt ist, ob der Inhalt Text "oder" HTML ist.</span><span class="sxs-lookup"><span data-stu-id="97e75-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="97e75-122">Der zurückgegebene Text ist Text wird, wenn der gespeicherte Text nur-Text.</span><span class="sxs-lookup"><span data-stu-id="97e75-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="97e75-123">Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Textkörper in HTML oder RTF-Format ist.</span><span class="sxs-lookup"><span data-stu-id="97e75-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="97e75-124">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="97e75-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="97e75-125">HTML</span><span class="sxs-lookup"><span data-stu-id="97e75-125">HTML</span></span>  <br/> |<span data-ttu-id="97e75-126">Die Antwort wird eine normalisierte Stelle im HTML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="97e75-126">The response will return a normalized body as HTML.</span></span>  <br/> |
|<span data-ttu-id="97e75-127">Text</span><span class="sxs-lookup"><span data-stu-id="97e75-127">Text</span></span>  <br/> |<span data-ttu-id="97e75-128">Die Antwort wird ein normalisierte Body als nur-Text zurück.</span><span class="sxs-lookup"><span data-stu-id="97e75-128">The response will return a normalized body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97e75-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97e75-129">Remarks</span></span>

<span data-ttu-id="97e75-130">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="97e75-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="97e75-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="97e75-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97e75-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="97e75-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97e75-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="97e75-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="97e75-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="97e75-134">Schema Name</span></span>  <br/> |<span data-ttu-id="97e75-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="97e75-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="97e75-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="97e75-136">Validation File</span></span>  <br/> |<span data-ttu-id="97e75-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="97e75-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="97e75-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="97e75-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="97e75-139">True</span><span class="sxs-lookup"><span data-stu-id="97e75-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97e75-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97e75-140">See also</span></span>



[<span data-ttu-id="97e75-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="97e75-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="97e75-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="97e75-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

