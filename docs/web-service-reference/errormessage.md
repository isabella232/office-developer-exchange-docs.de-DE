---
title: ErrorMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cec33a6-4b10-4259-8ac3-3f39a642b34c
description: ErrorMessage-Element stellt den Grund für die Überprüfungsfehler.
ms.openlocfilehash: d1869041254ef7c661fb2acb7c9c2ccaf628b394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758274"
---
# <a name="errormessage"></a><span data-ttu-id="44fbe-103">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="44fbe-103">ErrorMessage</span></span>

<span data-ttu-id="44fbe-104">**ErrorMessage** -Element stellt den Grund für die Überprüfungsfehler.</span><span class="sxs-lookup"><span data-stu-id="44fbe-104">The **ErrorMessage** element represents the reason for the validation error.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="44fbe-105">**String**</span><span class="sxs-lookup"><span data-stu-id="44fbe-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44fbe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="44fbe-106">Attributes and elements</span></span>

<span data-ttu-id="44fbe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="44fbe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44fbe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="44fbe-108">Attributes</span></span>

<span data-ttu-id="44fbe-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="44fbe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44fbe-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44fbe-110">Child elements</span></span>

<span data-ttu-id="44fbe-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="44fbe-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="44fbe-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44fbe-112">Parent elements</span></span>

|<span data-ttu-id="44fbe-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="44fbe-113">**Element**</span></span>|<span data-ttu-id="44fbe-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44fbe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44fbe-115">Fehler</span><span class="sxs-lookup"><span data-stu-id="44fbe-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="44fbe-116">Stellt einen einzelnen Gültigkeitsprüfungsfehler auf eine bestimmte Regel Eigenschaftswert, Prädikat Eigenschaftswert oder Aktionswert-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="44fbe-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44fbe-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="44fbe-117">Text value</span></span>

<span data-ttu-id="44fbe-118">Die Fehlermeldung, die die Regel Überprüfungsfehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="44fbe-118">The error message associated with the rule validation error.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44fbe-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44fbe-119">Remarks</span></span>

<span data-ttu-id="44fbe-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="44fbe-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44fbe-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="44fbe-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44fbe-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="44fbe-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="44fbe-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="44fbe-123">Schema Name</span></span>  <br/> |<span data-ttu-id="44fbe-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="44fbe-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="44fbe-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="44fbe-125">Validation File</span></span>  <br/> |<span data-ttu-id="44fbe-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="44fbe-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="44fbe-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="44fbe-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="44fbe-128">True</span><span class="sxs-lookup"><span data-stu-id="44fbe-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44fbe-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44fbe-129">See also</span></span>



- [<span data-ttu-id="44fbe-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="44fbe-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

