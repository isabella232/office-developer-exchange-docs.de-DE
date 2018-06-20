---
title: ContentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentId
api_type:
- schema
ms.assetid: bc59100d-6079-414b-a6e0-7c15feaa3184
description: Das Element ContentId stellt einen Bezeichner für den Inhalt einer Anlage. ContentId kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können ContentId um eigene Kennung Mechanismen zu implementieren.
ms.openlocfilehash: dc46ae4b33d435f5d47eb7deb39e92fd0170194b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757679"
---
# <a name="contentid"></a><span data-ttu-id="fa1a8-105">ContentId</span><span class="sxs-lookup"><span data-stu-id="fa1a8-105">ContentId</span></span>

<span data-ttu-id="fa1a8-106">Das Element **ContentId** stellt einen Bezeichner für den Inhalt einer Anlage.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-106">The **ContentId** element represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="fa1a8-107">**ContentId** kann auf einen beliebigen Zeichenfolgenwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-107">**ContentId** can be set to any string value.</span></span> <span data-ttu-id="fa1a8-108">Anwendungen können **ContentId** um eigene Kennung Mechanismen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-108">Applications can use **ContentId** to implement their own identification mechanisms.</span></span> 
  
```xml
<ContentId/>
```

 <span data-ttu-id="fa1a8-109">**String**</span><span class="sxs-lookup"><span data-stu-id="fa1a8-109">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa1a8-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fa1a8-110">Attributes and elements</span></span>

<span data-ttu-id="fa1a8-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa1a8-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="fa1a8-112">Attributes</span></span>

<span data-ttu-id="fa1a8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa1a8-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa1a8-114">Child elements</span></span>

<span data-ttu-id="fa1a8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa1a8-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa1a8-116">Parent elements</span></span>

|<span data-ttu-id="fa1a8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa1a8-117">**Element**</span></span>|<span data-ttu-id="fa1a8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa1a8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa1a8-119">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="fa1a8-119">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="fa1a8-120">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-120">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="fa1a8-121">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="fa1a8-121">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="fa1a8-122">Stellt eine Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-122">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa1a8-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="fa1a8-123">Text value</span></span>

<span data-ttu-id="fa1a8-124">String-Wert stellt den Bezeichner der Inhalt einer Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-124">The string value represents the identifier to the contents of an attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa1a8-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa1a8-125">Remarks</span></span>

<span data-ttu-id="fa1a8-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="fa1a8-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa1a8-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fa1a8-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa1a8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa1a8-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa1a8-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fa1a8-129">Schema name</span></span>  <br/> |<span data-ttu-id="fa1a8-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fa1a8-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa1a8-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fa1a8-131">Validation file</span></span>  <br/> |<span data-ttu-id="fa1a8-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa1a8-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa1a8-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fa1a8-133">Can be empty</span></span>  <br/> |<span data-ttu-id="fa1a8-134">False</span><span class="sxs-lookup"><span data-stu-id="fa1a8-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa1a8-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa1a8-135">See also</span></span>



- [<span data-ttu-id="fa1a8-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fa1a8-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

