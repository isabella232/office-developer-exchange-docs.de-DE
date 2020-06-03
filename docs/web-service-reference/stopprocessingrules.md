---
title: StopProcessingRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StopProcessingRules
api_type:
- schema
ms.assetid: 5b89a2cb-ab26-444d-b3dd-2b3858872d63
description: Das StopProcessingRules -Element gibt an, ob nachfolgende Regeln sind ausgewertet werden soll.
ms.openlocfilehash: 9f068fd6290a39bbab6e3c1e29066c4fefefc64b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467900"
---
# <a name="stopprocessingrules"></a><span data-ttu-id="bb9ec-103">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="bb9ec-103">StopProcessingRules</span></span>

<span data-ttu-id="bb9ec-104">Das **StopProcessingRules** -Element gibt an, ob nachfolgende Regeln sind ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-104">The **StopProcessingRules** element indicates whether subsequent rules are to be evaluated.</span></span> 
  
```XML
<StopProcessingRules>true | false</StopProcessingRules>
```

 <span data-ttu-id="bb9ec-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb9ec-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bb9ec-106">Attributes and elements</span></span>

<span data-ttu-id="bb9ec-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb9ec-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb9ec-108">Attributes</span></span>

<span data-ttu-id="bb9ec-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb9ec-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb9ec-110">Child elements</span></span>

<span data-ttu-id="bb9ec-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb9ec-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb9ec-112">Parent elements</span></span>

|<span data-ttu-id="bb9ec-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-113">**Element**</span></span>|<span data-ttu-id="bb9ec-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb9ec-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb9ec-115">Aktionen</span><span class="sxs-lookup"><span data-stu-id="bb9ec-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="bb9ec-116">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb9ec-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="bb9ec-117">Text value</span></span>

<span data-ttu-id="bb9ec-p101">Der Textwert **true** gibt an, dass nachfolgende Regeln nicht verarbeitet werden soll. Der Wert **false** gibt an, dass nachfolgende Regeln ausgewertet wird fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-p101">A text value of **true** indicates that subsequent rules should not be processed. A value of **false** indicates that subsequent rules should continue to be evaluated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bb9ec-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb9ec-120">Remarks</span></span>

<span data-ttu-id="bb9ec-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bb9ec-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb9ec-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bb9ec-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb9ec-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb9ec-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb9ec-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bb9ec-124">Schema Name</span></span>  <br/> |<span data-ttu-id="bb9ec-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bb9ec-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bb9ec-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bb9ec-126">Validation File</span></span>  <br/> |<span data-ttu-id="bb9ec-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bb9ec-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb9ec-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bb9ec-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb9ec-129">True</span><span class="sxs-lookup"><span data-stu-id="bb9ec-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb9ec-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb9ec-130">See also</span></span>



- [<span data-ttu-id="bb9ec-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bb9ec-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

