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
description: Das UmEnabled-Element gibt an, ob Unified Messaging für ein Konto aktiviert ist.
ms.openlocfilehash: 7ba7be69868cb439177702f74ff4a2f12875b7ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468355"
---
# <a name="umenabled"></a><span data-ttu-id="ce2d1-103">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="ce2d1-103">UmEnabled</span></span>

<span data-ttu-id="ce2d1-104">Das **UmEnabled** -Element gibt an, ob Unified Messaging für ein Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-104">The **UmEnabled** element indicates whether Unified Messaging is enabled for an account.</span></span> 
  
```XML
<UmEnabled>true | false</UmEnabled>
```

 <span data-ttu-id="ce2d1-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="ce2d1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce2d1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ce2d1-106">Attributes and elements</span></span>

<span data-ttu-id="ce2d1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce2d1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce2d1-108">Attributes</span></span>

<span data-ttu-id="ce2d1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce2d1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce2d1-110">Child elements</span></span>

<span data-ttu-id="ce2d1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce2d1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce2d1-112">Parent elements</span></span>

|<span data-ttu-id="ce2d1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce2d1-113">**Element**</span></span>|<span data-ttu-id="ce2d1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce2d1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce2d1-115">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce2d1-115">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="ce2d1-116">Enthält Dienstkonfigurationsinformationen für den Unified Messaging-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-116">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ce2d1-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="ce2d1-117">Text value</span></span>

<span data-ttu-id="ce2d1-118">Der Textwert des **UmEnabled** -Elements ist **true** , wenn Unified Messaging für das Konto aktiviert ist; Andernfalls ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-118">The text value of the **UmEnabled** element is **true** if Unified Messaging is enabled for the account; otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce2d1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce2d1-119">Remarks</span></span>

<span data-ttu-id="ce2d1-120">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-120">This element is required.</span></span>
  
<span data-ttu-id="ce2d1-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ce2d1-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce2d1-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ce2d1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce2d1-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce2d1-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce2d1-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ce2d1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ce2d1-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ce2d1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce2d1-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ce2d1-126">Validation File</span></span>  <br/> |<span data-ttu-id="ce2d1-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ce2d1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce2d1-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ce2d1-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce2d1-129">False</span><span class="sxs-lookup"><span data-stu-id="ce2d1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce2d1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce2d1-130">See also</span></span>



- [<span data-ttu-id="ce2d1-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ce2d1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

