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
description: Das Content-ID-Element stellt einen Bezeichner für den Inhalt einer Anlage dar. Die Inhalts-Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können mithilfe von Content-ID eigene Identifikations Mechanismen implementieren.
ms.openlocfilehash: ca89c8790e839326412003f26b738ad1ee956211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529266"
---
# <a name="contentid"></a><span data-ttu-id="a6ed7-105">ContentId</span><span class="sxs-lookup"><span data-stu-id="a6ed7-105">ContentId</span></span>

<span data-ttu-id="a6ed7-106">Das **Content** -ID-Element stellt einen Bezeichner für den Inhalt einer Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-106">The **ContentId** element represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="a6ed7-107">Die **Inhalts** -Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-107">**ContentId** can be set to any string value.</span></span> <span data-ttu-id="a6ed7-108">Anwendungen können mithilfe von **Content** -ID eigene Identifikations Mechanismen implementieren.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-108">Applications can use **ContentId** to implement their own identification mechanisms.</span></span> 
  
```xml
<ContentId/>
```

 <span data-ttu-id="a6ed7-109">**String**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-109">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6ed7-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a6ed7-110">Attributes and elements</span></span>

<span data-ttu-id="a6ed7-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6ed7-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6ed7-112">Attributes</span></span>

<span data-ttu-id="a6ed7-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6ed7-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6ed7-114">Child elements</span></span>

<span data-ttu-id="a6ed7-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6ed7-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6ed7-116">Parent elements</span></span>

|<span data-ttu-id="a6ed7-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-117">**Element**</span></span>|<span data-ttu-id="a6ed7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6ed7-119">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="a6ed7-119">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="a6ed7-120">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-120">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="a6ed7-121">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="a6ed7-121">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="a6ed7-122">Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-122">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6ed7-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="a6ed7-123">Text value</span></span>

<span data-ttu-id="a6ed7-124">Der String-Wert stellt den Bezeichner für den Inhalt einer Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-124">The string value represents the identifier to the contents of an attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6ed7-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6ed7-125">Remarks</span></span>

<span data-ttu-id="a6ed7-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6ed7-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a6ed7-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6ed7-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6ed7-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6ed7-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a6ed7-129">Schema name</span></span>  <br/> |<span data-ttu-id="a6ed7-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a6ed7-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6ed7-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a6ed7-131">Validation file</span></span>  <br/> |<span data-ttu-id="a6ed7-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6ed7-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6ed7-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a6ed7-133">Can be empty</span></span>  <br/> |<span data-ttu-id="a6ed7-134">False</span><span class="sxs-lookup"><span data-stu-id="a6ed7-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6ed7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6ed7-135">See also</span></span>



- [<span data-ttu-id="a6ed7-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a6ed7-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

