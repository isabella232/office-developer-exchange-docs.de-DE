---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: Das UniqueBodyType-Element gibt an, ob die eindeutige Body Text oder HTML-Format zurückgegeben wird.
ms.openlocfilehash: c6eb4ec4e39a0c5355775a635db4c63efc666820
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839308"
---
# <a name="uniquebodytype"></a><span data-ttu-id="4b8c7-103">UniqueBodyType</span><span class="sxs-lookup"><span data-stu-id="4b8c7-103">UniqueBodyType</span></span>

<span data-ttu-id="4b8c7-104">Das **UniqueBodyType** -Element gibt an, ob die eindeutige Body Text oder HTML-Format zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-104">The **UniqueBodyType** element specifies whether the unique body is returned in text or HTML format.</span></span> 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 <span data-ttu-id="4b8c7-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="4b8c7-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b8c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4b8c7-106">Attributes and elements</span></span>

<span data-ttu-id="4b8c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b8c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4b8c7-108">Attributes</span></span>

<span data-ttu-id="4b8c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b8c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b8c7-110">Child elements</span></span>

<span data-ttu-id="4b8c7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4b8c7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b8c7-112">Parent elements</span></span>

[<span data-ttu-id="4b8c7-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="4b8c7-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="4b8c7-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="4b8c7-114">Text value</span></span>

<span data-ttu-id="4b8c7-115">Der Textwert des **UniqueBodyType** -Elements gibt an, dass im Format eindeutige Text zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-115">The text value of the **UniqueBodyType** element indicates format the unique body is returned in.</span></span> <span data-ttu-id="4b8c7-116">Die folgende Tabelle enthält die möglichen Werte für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="4b8c7-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4b8c7-117">**Value**</span></span>|<span data-ttu-id="4b8c7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b8c7-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4b8c7-119">Am besten</span><span class="sxs-lookup"><span data-stu-id="4b8c7-119">Best</span></span>  <br/> |<span data-ttu-id="4b8c7-120">Die Antwort wird den inhaltlich verfügbaren Inhalt des Textkörpers zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="4b8c7-121">Dies ist nützlich, wenn nicht bekannt ist, ob der Inhalt Text "oder" HTML ist.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="4b8c7-122">Der zurückgegebene Text ist Text wird, wenn der gespeicherte Text nur-Text.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="4b8c7-123">Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Textkörper in HTML oder RTF-Format ist.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="4b8c7-124">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="4b8c7-125">HTML</span><span class="sxs-lookup"><span data-stu-id="4b8c7-125">HTML</span></span>  <br/> |<span data-ttu-id="4b8c7-126">Die Antwort wird eine eindeutige Stelle im HTML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-126">The response will return a unique body as HTML.</span></span>  <br/> |
|<span data-ttu-id="4b8c7-127">Text</span><span class="sxs-lookup"><span data-stu-id="4b8c7-127">Text</span></span>  <br/> |<span data-ttu-id="4b8c7-128">Die Antwort wird ein eindeutiger Body als nur-Text zurück.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-128">The response will return a unique body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b8c7-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4b8c7-129">Remarks</span></span>

<span data-ttu-id="4b8c7-130">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="4b8c7-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4b8c7-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b8c7-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4b8c7-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b8c7-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b8c7-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4b8c7-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4b8c7-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4b8c7-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4b8c7-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4b8c7-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4b8c7-136">Validation File</span></span>  <br/> |<span data-ttu-id="4b8c7-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4b8c7-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4b8c7-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4b8c7-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b8c7-139">True</span><span class="sxs-lookup"><span data-stu-id="4b8c7-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b8c7-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b8c7-140">See also</span></span>



[<span data-ttu-id="4b8c7-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="4b8c7-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="4b8c7-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4b8c7-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

