---
title: IsInline
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInline
api_type:
- schema
ms.assetid: 5e7712c8-372a-4a16-be64-360c5ff3961a
description: Das IsInline-Element stellt dar, ob die Anlage Inline in einem Element angezeigt wird.
ms.openlocfilehash: 2b3b6392fe8867ae9782dcb7211c17f4f4d9becd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464210"
---
# <a name="isinline"></a><span data-ttu-id="9fc4c-103">IsInline</span><span class="sxs-lookup"><span data-stu-id="9fc4c-103">IsInline</span></span>

<span data-ttu-id="9fc4c-104">Das **IsInline** -Element stellt dar, ob die Anlage Inline in einem Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-104">The **IsInline** element represents whether the attachment appears inline within an item.</span></span> 
  
```xml
<IsInline>true or false</IsInline>
```

 <span data-ttu-id="9fc4c-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="9fc4c-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fc4c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9fc4c-106">Attributes and elements</span></span>

<span data-ttu-id="9fc4c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fc4c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fc4c-108">Attributes</span></span>

<span data-ttu-id="9fc4c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fc4c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fc4c-110">Child elements</span></span>

<span data-ttu-id="9fc4c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fc4c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fc4c-112">Parent elements</span></span>

|<span data-ttu-id="9fc4c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fc4c-113">**Element**</span></span>|<span data-ttu-id="9fc4c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fc4c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fc4c-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="9fc4c-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="9fc4c-116">Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9fc4c-117">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="9fc4c-117">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="9fc4c-118">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-118">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9fc4c-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="9fc4c-119">Text value</span></span>

<span data-ttu-id="9fc4c-120">Dieses Element kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-120">This element can be either **true** or **false**.</span></span> <span data-ttu-id="9fc4c-121">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fc4c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fc4c-122">Remarks</span></span>

<span data-ttu-id="9fc4c-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9fc4c-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fc4c-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9fc4c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fc4c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fc4c-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9fc4c-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9fc4c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="9fc4c-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9fc4c-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="9fc4c-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9fc4c-128">Validation File</span></span>  <br/> |<span data-ttu-id="9fc4c-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9fc4c-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9fc4c-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9fc4c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fc4c-131">False</span><span class="sxs-lookup"><span data-stu-id="9fc4c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fc4c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fc4c-132">See also</span></span>



- [<span data-ttu-id="9fc4c-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fc4c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

