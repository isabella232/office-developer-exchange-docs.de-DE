---
title: ErrorMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cec33a6-4b10-4259-8ac3-3f39a642b34c
description: Das ErrorMessage-Element stellt den Grund für den Validierungsfehler dar.
ms.openlocfilehash: a35dc6af12e71c8437c13024a254000e8f477a15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526193"
---
# <a name="errormessage"></a><span data-ttu-id="2d1d4-103">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="2d1d4-103">ErrorMessage</span></span>

<span data-ttu-id="2d1d4-104">Das **ErrorMessage** -Element stellt den Grund für den Validierungsfehler dar.</span><span class="sxs-lookup"><span data-stu-id="2d1d4-104">The **ErrorMessage** element represents the reason for the validation error.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="2d1d4-105">**String**</span><span class="sxs-lookup"><span data-stu-id="2d1d4-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d1d4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2d1d4-106">Attributes and elements</span></span>

<span data-ttu-id="2d1d4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d1d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d1d4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d1d4-108">Attributes</span></span>

<span data-ttu-id="2d1d4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d1d4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d1d4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d1d4-110">Child elements</span></span>

<span data-ttu-id="2d1d4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d1d4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d1d4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d1d4-112">Parent elements</span></span>

|<span data-ttu-id="2d1d4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d1d4-113">**Element**</span></span>|<span data-ttu-id="2d1d4-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2d1d4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d1d4-115">Fehler</span><span class="sxs-lookup"><span data-stu-id="2d1d4-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="2d1d4-116">Stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar.</span><span class="sxs-lookup"><span data-stu-id="2d1d4-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d1d4-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="2d1d4-117">Text value</span></span>

<span data-ttu-id="2d1d4-118">Die Fehlermeldung, die dem Regel Validierungsfehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2d1d4-118">The error message associated with the rule validation error.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d1d4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d1d4-119">Remarks</span></span>

<span data-ttu-id="2d1d4-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2d1d4-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d1d4-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2d1d4-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d1d4-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d1d4-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d1d4-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2d1d4-123">Schema Name</span></span>  <br/> |<span data-ttu-id="2d1d4-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2d1d4-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d1d4-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2d1d4-125">Validation File</span></span>  <br/> |<span data-ttu-id="2d1d4-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2d1d4-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d1d4-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2d1d4-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d1d4-128">True</span><span class="sxs-lookup"><span data-stu-id="2d1d4-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d1d4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d1d4-129">See also</span></span>



- [<span data-ttu-id="2d1d4-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2d1d4-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

