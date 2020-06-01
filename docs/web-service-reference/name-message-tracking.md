---
title: Name (Nachrichtenverfolgung)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: a1669f6d-53f3-4849-9b30-56909aaeac82
description: Das Name-Element stellt den Eigenschaftennamen für einen Nachrichtenverfolgungsbericht dar.
ms.openlocfilehash: 86f049c0a90dbeb55418a5eee58079adf17e5ded
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466899"
---
# <a name="name-message-tracking"></a><span data-ttu-id="06804-103">Name (Nachrichtenverfolgung)</span><span class="sxs-lookup"><span data-stu-id="06804-103">Name (Message Tracking)</span></span>

<span data-ttu-id="06804-104">Das **Name** -Element stellt den Eigenschaftennamen für einen Nachrichtenverfolgungsbericht dar.</span><span class="sxs-lookup"><span data-stu-id="06804-104">The **Name** element represents the property name for a message tracking report.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="06804-105">**String**</span><span class="sxs-lookup"><span data-stu-id="06804-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="06804-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="06804-106">Attributes and elements</span></span>

<span data-ttu-id="06804-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="06804-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06804-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="06804-108">Attributes</span></span>

<span data-ttu-id="06804-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="06804-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06804-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06804-110">Child elements</span></span>

<span data-ttu-id="06804-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="06804-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="06804-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="06804-112">Parent elements</span></span>

|<span data-ttu-id="06804-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="06804-113">**Element**</span></span>|<span data-ttu-id="06804-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="06804-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06804-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="06804-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="06804-116">Stellt ein Name-Wert-Paar von Zeichenfolgen dar, das zum Erstellen von Eigenschaften für Nachrichtenverfolgungsberichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06804-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="06804-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="06804-117">Text value</span></span>

<span data-ttu-id="06804-118">Wenn dieses Element verwendet wird, ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="06804-118">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06804-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06804-119">Remarks</span></span>

<span data-ttu-id="06804-120">Dieses Element kann im [TrackingPropertyType](trackingpropertytype.md) -Element höchstens einmal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="06804-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="06804-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="06804-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06804-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="06804-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06804-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="06804-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06804-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="06804-124">Schema Name</span></span>  <br/> |<span data-ttu-id="06804-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="06804-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="06804-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="06804-126">Validation File</span></span>  <br/> |<span data-ttu-id="06804-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06804-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06804-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="06804-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="06804-129">False</span><span class="sxs-lookup"><span data-stu-id="06804-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06804-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06804-130">See also</span></span>

- [<span data-ttu-id="06804-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="06804-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

