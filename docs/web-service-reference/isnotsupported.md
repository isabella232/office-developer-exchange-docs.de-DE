---
title: IsNotSupported
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNotSupported
api_type:
- schema
ms.assetid: 4db469ae-1515-47ea-9905-6aabf199febd
description: Das IsNotSupported-Element gibt an, ob die Regel mithilfe des verwalteten Codes-APIs nicht geändert werden kann.
ms.openlocfilehash: 2468d47dbfdcaf1a28ed1a4afb1e7ea60147d1dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830057"
---
# <a name="isnotsupported"></a><span data-ttu-id="7413e-103">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="7413e-103">IsNotSupported</span></span>

<span data-ttu-id="7413e-104">Das **IsNotSupported** -Element gibt an, ob die Regel mithilfe des verwalteten Codes-APIs nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7413e-104">The **IsNotSupported** element indicates whether the rule cannot be modified by using the managed code APIs.</span></span> 
  
```XML
<IsNotSupported/>
```

 <span data-ttu-id="7413e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7413e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7413e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7413e-106">Attributes and elements</span></span>

<span data-ttu-id="7413e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7413e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7413e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7413e-108">Attributes</span></span>

<span data-ttu-id="7413e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7413e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7413e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7413e-110">Child elements</span></span>

<span data-ttu-id="7413e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7413e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7413e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7413e-112">Parent elements</span></span>

|<span data-ttu-id="7413e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7413e-113">**Element**</span></span>|<span data-ttu-id="7413e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7413e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7413e-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="7413e-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="7413e-116">Stellt eine Regel in das Postfach des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="7413e-116">Represents a rule in the user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7413e-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="7413e-117">Text value</span></span>

<span data-ttu-id="7413e-118">Der Textwert **true** gibt an, dass die Regel mithilfe des verwalteten Codes-APIs nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7413e-118">A text value of **true** indicates that the rule cannot be modified by using the managed code APIs.</span></span> <span data-ttu-id="7413e-119">Der Wert **false** gibt an, dass die Regel mithilfe von verwaltetem Code APIs geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7413e-119">A value of **false** indicates that the rule can be modified by using the managed code APIs.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7413e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7413e-120">Remarks</span></span>

<span data-ttu-id="7413e-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7413e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7413e-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7413e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7413e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7413e-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7413e-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7413e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7413e-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7413e-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7413e-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7413e-126">Validation File</span></span>  <br/> |<span data-ttu-id="7413e-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7413e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7413e-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7413e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7413e-129">True</span><span class="sxs-lookup"><span data-stu-id="7413e-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7413e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7413e-130">See also</span></span>



- [<span data-ttu-id="7413e-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7413e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

