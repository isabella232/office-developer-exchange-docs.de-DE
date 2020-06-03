---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: Das UniqueBodyType-Element gibt an, ob der eindeutige Text im Text-oder HTML-Format zurückgegeben wird.
ms.openlocfilehash: 7e6c4631ef589555ce4d5da747c200ffe956f3a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459440"
---
# <a name="uniquebodytype"></a><span data-ttu-id="7a6fc-103">UniqueBodyType</span><span class="sxs-lookup"><span data-stu-id="7a6fc-103">UniqueBodyType</span></span>

<span data-ttu-id="7a6fc-104">Das **UniqueBodyType** -Element gibt an, ob der eindeutige Text im Text-oder HTML-Format zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-104">The **UniqueBodyType** element specifies whether the unique body is returned in text or HTML format.</span></span> 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 <span data-ttu-id="7a6fc-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="7a6fc-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a6fc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a6fc-106">Attributes and elements</span></span>

<span data-ttu-id="7a6fc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a6fc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a6fc-108">Attributes</span></span>

<span data-ttu-id="7a6fc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a6fc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a6fc-110">Child elements</span></span>

<span data-ttu-id="7a6fc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a6fc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a6fc-112">Parent elements</span></span>

[<span data-ttu-id="7a6fc-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="7a6fc-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="7a6fc-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="7a6fc-114">Text value</span></span>

<span data-ttu-id="7a6fc-115">Der Textwert des **UniqueBodyType** -Elements gibt an, in welchem Format der eindeutige Textkörper zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-115">The text value of the **UniqueBodyType** element indicates format the unique body is returned in.</span></span> <span data-ttu-id="7a6fc-116">In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="7a6fc-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7a6fc-117">**Value**</span></span>|<span data-ttu-id="7a6fc-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a6fc-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a6fc-119">Optimal</span><span class="sxs-lookup"><span data-stu-id="7a6fc-119">Best</span></span>  <br/> |<span data-ttu-id="7a6fc-120">Die Antwort gibt den reichsten verfügbaren Inhalt des Textkörpers zurück.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="7a6fc-121">Dies ist hilfreich, wenn unbekannt ist, ob es sich bei dem Inhalt um Text oder HTML handelt.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="7a6fc-122">Der zurückgegebene Text ist Text, wenn der gespeicherte Text nur-Text ist.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="7a6fc-123">Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Text im HTML-oder RTF-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="7a6fc-124">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="7a6fc-125">HTML</span><span class="sxs-lookup"><span data-stu-id="7a6fc-125">HTML</span></span>  <br/> |<span data-ttu-id="7a6fc-126">Die Antwort gibt einen eindeutigen Text im HTML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-126">The response will return a unique body as HTML.</span></span>  <br/> |
|<span data-ttu-id="7a6fc-127">Text</span><span class="sxs-lookup"><span data-stu-id="7a6fc-127">Text</span></span>  <br/> |<span data-ttu-id="7a6fc-128">Die Antwort gibt einen eindeutigen Text im Klartext zurück.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-128">The response will return a unique body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a6fc-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a6fc-129">Remarks</span></span>

<span data-ttu-id="7a6fc-130">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="7a6fc-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7a6fc-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a6fc-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7a6fc-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a6fc-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a6fc-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a6fc-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a6fc-134">Schema Name</span></span>  <br/> |<span data-ttu-id="7a6fc-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7a6fc-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a6fc-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a6fc-136">Validation File</span></span>  <br/> |<span data-ttu-id="7a6fc-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a6fc-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a6fc-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7a6fc-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a6fc-139">True</span><span class="sxs-lookup"><span data-stu-id="7a6fc-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a6fc-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a6fc-140">See also</span></span>



[<span data-ttu-id="7a6fc-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="7a6fc-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="7a6fc-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a6fc-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

