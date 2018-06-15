---
title: UmEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UmEnabled
api_type:
- schema
ms.assetid: 87382d9b-0c02-49ec-85dc-3f5918df3195
description: Das UmEnabled-Element gibt an, ob für ein Konto Unified Messaging aktiviert ist.
ms.openlocfilehash: 8324e02136adc6704bc0badb77131e9671ee569f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19839281"
---
# <a name="umenabled"></a><span data-ttu-id="55d45-103">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="55d45-103">UmEnabled</span></span>

<span data-ttu-id="55d45-104">Das **UmEnabled** -Element gibt an, ob für ein Konto Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="55d45-104">The **UmEnabled** element indicates whether Unified Messaging is enabled for an account.</span></span> 
  
```XML
<UmEnabled>true | false</UmEnabled>
```

 <span data-ttu-id="55d45-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="55d45-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55d45-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="55d45-106">Attributes and elements</span></span>

<span data-ttu-id="55d45-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="55d45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55d45-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="55d45-108">Attributes</span></span>

<span data-ttu-id="55d45-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="55d45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55d45-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55d45-110">Child elements</span></span>

<span data-ttu-id="55d45-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="55d45-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="55d45-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55d45-112">Parent elements</span></span>

|<span data-ttu-id="55d45-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="55d45-113">**Element**</span></span>|<span data-ttu-id="55d45-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55d45-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55d45-115">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="55d45-115">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="55d45-116">Service-Konfigurationsinformationen für die Unified Messaging-Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="55d45-116">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="55d45-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="55d45-117">Text value</span></span>

<span data-ttu-id="55d45-118">Der Textwert der **UmEnabled** -Element ist **true** , wenn für das Konto Unified Messaging aktiviert ist; Andernfalls ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="55d45-118">The text value of the **UmEnabled** element is **true** if Unified Messaging is enabled for the account; otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55d45-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55d45-119">Remarks</span></span>

<span data-ttu-id="55d45-120">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="55d45-120">This element is required.</span></span>
  
<span data-ttu-id="55d45-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="55d45-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55d45-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="55d45-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55d45-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="55d45-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="55d45-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="55d45-124">Schema Name</span></span>  <br/> |<span data-ttu-id="55d45-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="55d45-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="55d45-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="55d45-126">Validation File</span></span>  <br/> |<span data-ttu-id="55d45-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="55d45-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="55d45-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="55d45-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="55d45-129">False</span><span class="sxs-lookup"><span data-stu-id="55d45-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55d45-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55d45-130">See also</span></span>



- [<span data-ttu-id="55d45-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="55d45-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

