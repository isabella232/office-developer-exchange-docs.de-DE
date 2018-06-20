---
title: CanRenameOrMove
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanRenameOrMove
api_type:
- schema
ms.assetid: fe0cdb04-5f2b-4f1d-9d12-7ace0883cd86
description: Das CanRenameOrMove-Element gibt an, ob ein verwalteter Ordner umbenannt oder durch den Kunden verschoben werden kann.
ms.openlocfilehash: 0303499f5cd54d4a52222e43c2c5f0b389fbcf53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757555"
---
# <a name="canrenameormove"></a><span data-ttu-id="7e93f-103">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="7e93f-103">CanRenameOrMove</span></span>

<span data-ttu-id="7e93f-104">Das **CanRenameOrMove** -Element gibt an, ob ein verwalteter Ordner umbenannt oder durch den Kunden verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e93f-104">The **CanRenameOrMove** element indicates whether a managed folder can be renamed or moved by the customer.</span></span> 
  
```xml
<CanRenameOrMove/>
```

 <span data-ttu-id="7e93f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7e93f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e93f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7e93f-106">Attributes and elements</span></span>

<span data-ttu-id="7e93f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7e93f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e93f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7e93f-108">Attributes</span></span>

<span data-ttu-id="7e93f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7e93f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e93f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7e93f-110">Child elements</span></span>

<span data-ttu-id="7e93f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7e93f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7e93f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7e93f-112">Parent elements</span></span>

|<span data-ttu-id="7e93f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7e93f-113">**Element**</span></span>|<span data-ttu-id="7e93f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e93f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e93f-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="7e93f-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="7e93f-116">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e93f-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7e93f-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="7e93f-117">Text value</span></span>

<span data-ttu-id="7e93f-118">Der Textwert stellt einen Boolean-Wert.</span><span class="sxs-lookup"><span data-stu-id="7e93f-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="7e93f-119">Der Wert **true** gibt an, dass der Ordner umbenannt oder verschoben werden kann; der Wert **false** gibt an, dass der Ordner umbenannte oder verschobene ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="7e93f-119">A value of **true** indicates that the folder can be renamed or moved; a value of **false** indicates that the folder cannot be renamed or moved.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7e93f-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e93f-120">Remarks</span></span>

<span data-ttu-id="7e93f-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7e93f-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e93f-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7e93f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e93f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e93f-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7e93f-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7e93f-124">Schema name</span></span>  <br/> |<span data-ttu-id="7e93f-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7e93f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="7e93f-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7e93f-126">Validation file</span></span>  <br/> |<span data-ttu-id="7e93f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7e93f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7e93f-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7e93f-128">Can be empty</span></span>  <br/> |<span data-ttu-id="7e93f-129">False</span><span class="sxs-lookup"><span data-stu-id="7e93f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e93f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e93f-130">See also</span></span>



- [<span data-ttu-id="7e93f-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e93f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

