---
title: Bereich (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: Das Bereich-Element gibt den Bereich der Bericht mit der Verfolgung an.
ms.openlocfilehash: 534ed23916a60b246c7cb5be4a59d086980a7c37
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831280"
---
# <a name="scope-nonemptystringtype"></a><span data-ttu-id="ba544-103">Bereich (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="ba544-103">Scope (NonEmptyStringType)</span></span>

<span data-ttu-id="ba544-104">Das **Bereich** -Element gibt den Bereich der Bericht mit der Verfolgung an.</span><span class="sxs-lookup"><span data-stu-id="ba544-104">The **Scope** element specifies the scope of the message tracking report.</span></span> 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 <span data-ttu-id="ba544-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="ba544-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba544-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba544-106">Attributes and elements</span></span>

<span data-ttu-id="ba544-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba544-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba544-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba544-108">Attributes</span></span>

<span data-ttu-id="ba544-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba544-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba544-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba544-110">Child elements</span></span>

<span data-ttu-id="ba544-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba544-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba544-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba544-112">Parent elements</span></span>

<span data-ttu-id="ba544-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span><span class="sxs-lookup"><span data-stu-id="ba544-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ba544-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="ba544-114">Text value</span></span>

<span data-ttu-id="ba544-115">Die folgende Tabelle enthält die möglichen Werte für das Element **Bereich** .</span><span class="sxs-lookup"><span data-stu-id="ba544-115">The following table lists the possible values for the **Scope** element.</span></span> 
  
|<span data-ttu-id="ba544-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ba544-116">**Value**</span></span>|<span data-ttu-id="ba544-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba544-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba544-118">Organisation</span><span class="sxs-lookup"><span data-stu-id="ba544-118">Organization</span></span>  <br/> |<span data-ttu-id="ba544-119">Die nachrichtenverfolgung Bereiche erstreckt sich innerhalb einer Organisation.</span><span class="sxs-lookup"><span data-stu-id="ba544-119">The message tracking scopes spans across an organization.</span></span>  <br/> |
|<span data-ttu-id="ba544-120">Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="ba544-120">Forest</span></span>  <br/> |<span data-ttu-id="ba544-121">Die nachrichtenverfolgung Bereiche erstreckt sich auf einer Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="ba544-121">The message tracking scopes spans across a forest.</span></span>  <br/> |
|<span data-ttu-id="ba544-122">Website</span><span class="sxs-lookup"><span data-stu-id="ba544-122">Site</span></span>  <br/> |<span data-ttu-id="ba544-123">Die nachrichtenverfolgung Bereiche erstreckt sich auf einer Website.</span><span class="sxs-lookup"><span data-stu-id="ba544-123">The message tracking scopes spans across a site.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba544-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ba544-124">Remarks</span></span>

<span data-ttu-id="ba544-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ba544-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba544-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ba544-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba544-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba544-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ba544-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ba544-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ba544-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ba544-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ba544-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ba544-130">Validation File</span></span>  <br/> |<span data-ttu-id="ba544-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ba544-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba544-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ba544-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba544-133">False</span><span class="sxs-lookup"><span data-stu-id="ba544-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba544-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba544-134">See also</span></span>



- [<span data-ttu-id="ba544-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ba544-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

