---
title: NormalizedBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: Das NormalizedBodyType-Element gibt an, ob der normalisierte Text im Text-oder HTML-Format zurückgegeben wird.
ms.openlocfilehash: e5d968673403eba24a68c67175e3ebcbb35eca39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462661"
---
# <a name="normalizedbodytype"></a><span data-ttu-id="bebcb-103">NormalizedBodyType</span><span class="sxs-lookup"><span data-stu-id="bebcb-103">NormalizedBodyType</span></span>

<span data-ttu-id="bebcb-104">Das **NormalizedBodyType** -Element gibt an, ob der normalisierte Text im Text-oder HTML-Format zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bebcb-104">The **NormalizedBodyType** element specifies whether the normalized body is returned in text or HTML format.</span></span> 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 <span data-ttu-id="bebcb-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="bebcb-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bebcb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bebcb-106">Attributes and elements</span></span>

<span data-ttu-id="bebcb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bebcb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bebcb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bebcb-108">Attributes</span></span>

<span data-ttu-id="bebcb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bebcb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bebcb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bebcb-110">Child elements</span></span>

<span data-ttu-id="bebcb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bebcb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bebcb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bebcb-112">Parent elements</span></span>

[<span data-ttu-id="bebcb-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="bebcb-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="bebcb-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="bebcb-114">Text value</span></span>

<span data-ttu-id="bebcb-115">Der Textwert des **NormalizedBodyType** -Elements gibt an, in welchem Format der normalisierte Text zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bebcb-115">The text value of the **NormalizedBodyType** element indicates format the normalized body is returned in.</span></span> <span data-ttu-id="bebcb-116">In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bebcb-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="bebcb-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bebcb-117">**Value**</span></span>|<span data-ttu-id="bebcb-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bebcb-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bebcb-119">Optimal</span><span class="sxs-lookup"><span data-stu-id="bebcb-119">Best</span></span>  <br/> |<span data-ttu-id="bebcb-120">Die Antwort gibt den reichsten verfügbaren Inhalt des Textkörpers zurück.</span><span class="sxs-lookup"><span data-stu-id="bebcb-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="bebcb-121">Dies ist hilfreich, wenn unbekannt ist, ob es sich bei dem Inhalt um Text oder HTML handelt.</span><span class="sxs-lookup"><span data-stu-id="bebcb-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="bebcb-122">Der zurückgegebene Text ist Text, wenn der gespeicherte Text nur-Text ist.</span><span class="sxs-lookup"><span data-stu-id="bebcb-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="bebcb-123">Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Text im HTML-oder RTF-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="bebcb-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="bebcb-124">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="bebcb-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="bebcb-125">HTML</span><span class="sxs-lookup"><span data-stu-id="bebcb-125">HTML</span></span>  <br/> |<span data-ttu-id="bebcb-126">Die Antwort gibt einen normalisierten Text als HTML zurück.</span><span class="sxs-lookup"><span data-stu-id="bebcb-126">The response will return a normalized body as HTML.</span></span>  <br/> |
|<span data-ttu-id="bebcb-127">Text</span><span class="sxs-lookup"><span data-stu-id="bebcb-127">Text</span></span>  <br/> |<span data-ttu-id="bebcb-128">Die Antwort gibt einen normalisierten Text als nur-Text zurück.</span><span class="sxs-lookup"><span data-stu-id="bebcb-128">The response will return a normalized body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bebcb-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bebcb-129">Remarks</span></span>

<span data-ttu-id="bebcb-130">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bebcb-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="bebcb-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bebcb-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bebcb-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bebcb-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bebcb-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="bebcb-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bebcb-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bebcb-134">Schema Name</span></span>  <br/> |<span data-ttu-id="bebcb-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bebcb-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="bebcb-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bebcb-136">Validation File</span></span>  <br/> |<span data-ttu-id="bebcb-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bebcb-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bebcb-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bebcb-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="bebcb-139">True</span><span class="sxs-lookup"><span data-stu-id="bebcb-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bebcb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bebcb-140">See also</span></span>



[<span data-ttu-id="bebcb-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="bebcb-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="bebcb-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bebcb-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

