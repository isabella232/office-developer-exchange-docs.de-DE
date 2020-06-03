---
title: Wert (Nachrichtenverfolgung)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: cb2f228f-775a-4c7d-82e7-41c7c953c808
description: Das Value-Element stellt den Eigenschaftswert für einen Nachrichtenverfolgungsbericht dar.
ms.openlocfilehash: 4f6b5cb9d82a35bbe010b36e409cdc9f3a70173d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465008"
---
# <a name="value-message-tracking"></a><span data-ttu-id="451fb-103">Wert (Nachrichtenverfolgung)</span><span class="sxs-lookup"><span data-stu-id="451fb-103">Value (Message Tracking)</span></span>

<span data-ttu-id="451fb-104">Das **value** -Element stellt den Eigenschaftswert für einen Nachrichtenverfolgungsbericht dar.</span><span class="sxs-lookup"><span data-stu-id="451fb-104">The **Value** element represents the property value for a message tracking report.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="451fb-105">**String**</span><span class="sxs-lookup"><span data-stu-id="451fb-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="451fb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="451fb-106">Attributes and elements</span></span>

<span data-ttu-id="451fb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="451fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="451fb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="451fb-108">Attributes</span></span>

<span data-ttu-id="451fb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="451fb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="451fb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="451fb-110">Child elements</span></span>

<span data-ttu-id="451fb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="451fb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="451fb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="451fb-112">Parent elements</span></span>

|<span data-ttu-id="451fb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="451fb-113">**Element**</span></span>|<span data-ttu-id="451fb-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="451fb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="451fb-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="451fb-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="451fb-116">Stellt ein Name-Wert-Paar von Zeichenfolgen dar, das zum Erstellen von Eigenschaften für Nachrichtenverfolgungsberichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="451fb-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="451fb-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="451fb-117">Text value</span></span>

<span data-ttu-id="451fb-118">Der Textwert ist optional.</span><span class="sxs-lookup"><span data-stu-id="451fb-118">The text value is optional.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="451fb-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="451fb-119">Remarks</span></span>

<span data-ttu-id="451fb-120">Dieses Element kann im [TrackingPropertyType](trackingpropertytype.md) -Element höchstens einmal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="451fb-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="451fb-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="451fb-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="451fb-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="451fb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="451fb-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="451fb-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="451fb-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="451fb-124">Schema Name</span></span>  <br/> |<span data-ttu-id="451fb-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="451fb-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="451fb-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="451fb-126">Validation File</span></span>  <br/> |<span data-ttu-id="451fb-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="451fb-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="451fb-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="451fb-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="451fb-129">False</span><span class="sxs-lookup"><span data-stu-id="451fb-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="451fb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="451fb-130">See also</span></span>

- [<span data-ttu-id="451fb-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="451fb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

