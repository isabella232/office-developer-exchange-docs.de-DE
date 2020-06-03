---
title: ContentType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentType
api_type:
- schema
ms.assetid: f91ff0df-0d8a-43ea-a188-d80f0e885f19
description: Das ContentType-Element beschreibt den Multipurpose Internet Mail Extensions (MIME) Typ des Anlage Inhalts.
ms.openlocfilehash: cb326bb761ea28e0e9f77501bf754c7c1f0318fb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455226"
---
# <a name="contenttype"></a><span data-ttu-id="19f77-103">ContentType</span><span class="sxs-lookup"><span data-stu-id="19f77-103">ContentType</span></span>

<span data-ttu-id="19f77-104">Das **ContentType** -Element beschreibt den Multipurpose Internet Mail Extensions (MIME) Typ des Anlage Inhalts.</span><span class="sxs-lookup"><span data-stu-id="19f77-104">The **ContentType** element describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span> 
  
```xml
<ContentType/>
```

 <span data-ttu-id="19f77-105">**String**</span><span class="sxs-lookup"><span data-stu-id="19f77-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19f77-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="19f77-106">Attributes and elements</span></span>

<span data-ttu-id="19f77-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="19f77-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19f77-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="19f77-108">Attributes</span></span>

<span data-ttu-id="19f77-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="19f77-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19f77-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19f77-110">Child elements</span></span>

<span data-ttu-id="19f77-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="19f77-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19f77-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19f77-112">Parent elements</span></span>

|<span data-ttu-id="19f77-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="19f77-113">**Element**</span></span>|<span data-ttu-id="19f77-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19f77-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19f77-115">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="19f77-115">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="19f77-116">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="19f77-116">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="19f77-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="19f77-117">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="19f77-118">Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="19f77-118">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19f77-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="19f77-119">Text value</span></span>

<span data-ttu-id="19f77-120">Der Text-Wert ist ein String-Wert, der den Inhaltstyp der Anlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="19f77-120">The text value is a string value that represents the content type of the attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19f77-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19f77-121">Remarks</span></span>

<span data-ttu-id="19f77-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="19f77-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19f77-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="19f77-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19f77-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="19f77-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19f77-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="19f77-125">Schema name</span></span>  <br/> |<span data-ttu-id="19f77-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="19f77-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="19f77-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="19f77-127">Validation file</span></span>  <br/> |<span data-ttu-id="19f77-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19f77-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19f77-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="19f77-129">Can be empty</span></span>  <br/> |<span data-ttu-id="19f77-130">False</span><span class="sxs-lookup"><span data-stu-id="19f77-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19f77-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19f77-131">See also</span></span>



- [<span data-ttu-id="19f77-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="19f77-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

