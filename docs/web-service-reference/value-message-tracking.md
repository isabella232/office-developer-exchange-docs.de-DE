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
description: Das Value-Element darstellt, den Eigenschaftswert für eine Nachricht Bericht nachverfolgen.
ms.openlocfilehash: 152e4fe61a4cff8013ae02900bd84bf244ae84a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839484"
---
# <a name="value-message-tracking"></a><span data-ttu-id="2eaaf-103">Wert (Nachrichtenverfolgung)</span><span class="sxs-lookup"><span data-stu-id="2eaaf-103">Value (Message Tracking)</span></span>

<span data-ttu-id="2eaaf-104">Das **Value** -Element darstellt, den Eigenschaftswert für eine Nachricht Bericht nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-104">The **Value** element represents the property value for a message tracking report.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="2eaaf-105">**String**</span><span class="sxs-lookup"><span data-stu-id="2eaaf-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2eaaf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2eaaf-106">Attributes and elements</span></span>

<span data-ttu-id="2eaaf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2eaaf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2eaaf-108">Attributes</span></span>

<span data-ttu-id="2eaaf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2eaaf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2eaaf-110">Child elements</span></span>

<span data-ttu-id="2eaaf-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2eaaf-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2eaaf-112">Parent elements</span></span>

|<span data-ttu-id="2eaaf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2eaaf-113">**Element**</span></span>|<span data-ttu-id="2eaaf-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2eaaf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2eaaf-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="2eaaf-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="2eaaf-116">Stellt ein Name-Wert-Paar von Zeichenfolgen, die zum Erstellen von Eigenschaften für nachrichtenverfolgungsberichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2eaaf-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="2eaaf-117">Text value</span></span>

<span data-ttu-id="2eaaf-118">Der Textwert ist optional.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-118">The text value is optional.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2eaaf-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2eaaf-119">Remarks</span></span>

<span data-ttu-id="2eaaf-120">Dieses Element kann höchstens einmal im [TrackingPropertyType](trackingpropertytype.md) -Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="2eaaf-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2eaaf-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2eaaf-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2eaaf-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2eaaf-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2eaaf-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2eaaf-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2eaaf-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2eaaf-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2eaaf-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="2eaaf-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2eaaf-126">Validation File</span></span>  <br/> |<span data-ttu-id="2eaaf-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2eaaf-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2eaaf-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2eaaf-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="2eaaf-129">False</span><span class="sxs-lookup"><span data-stu-id="2eaaf-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2eaaf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2eaaf-130">See also</span></span>

- [<span data-ttu-id="2eaaf-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2eaaf-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

