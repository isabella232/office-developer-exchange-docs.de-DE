---
title: HasQuota
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasQuota
api_type:
- schema
ms.assetid: b6e4fef0-92a9-415f-81ae-0c5ecb7c12ad
description: Das HasQuota-Element gibt an, ob der verwaltete Ordner ein Kontingent aufweist.
ms.openlocfilehash: 6e32aa4c69943774be928339936cca5016c58d85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462752"
---
# <a name="hasquota"></a><span data-ttu-id="97c34-103">HasQuota</span><span class="sxs-lookup"><span data-stu-id="97c34-103">HasQuota</span></span>

<span data-ttu-id="97c34-104">Das **HasQuota** -Element gibt an, ob der verwaltete Ordner ein Kontingent aufweist.</span><span class="sxs-lookup"><span data-stu-id="97c34-104">The **HasQuota** element indicates whether the managed folder has a quota.</span></span> 
  
```xml
<HasQuota/>
```

 <span data-ttu-id="97c34-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="97c34-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97c34-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="97c34-106">Attributes and elements</span></span>

<span data-ttu-id="97c34-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="97c34-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97c34-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="97c34-108">Attributes</span></span>

<span data-ttu-id="97c34-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="97c34-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="97c34-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97c34-110">Child elements</span></span>

<span data-ttu-id="97c34-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="97c34-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="97c34-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97c34-112">Parent elements</span></span>

|<span data-ttu-id="97c34-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="97c34-113">**Element**</span></span>|<span data-ttu-id="97c34-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97c34-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97c34-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="97c34-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="97c34-116">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="97c34-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="97c34-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="97c34-117">Text value</span></span>

<span data-ttu-id="97c34-118">Der Wert Text stellt einen booleschen Wert dar.</span><span class="sxs-lookup"><span data-stu-id="97c34-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="97c34-119">Der Wert **true** gibt an, dass der Ordner über ein Kontingent verfügt. der Wert **false** gibt an, dass der Ordner kein Kontingent aufweist.</span><span class="sxs-lookup"><span data-stu-id="97c34-119">A value of **true** indicates that the folder has a quota; a value of **false** indicates that the folder does not have a quota.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="97c34-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97c34-120">Remarks</span></span>

<span data-ttu-id="97c34-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="97c34-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97c34-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="97c34-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97c34-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="97c34-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="97c34-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="97c34-124">Schema name</span></span>  <br/> |<span data-ttu-id="97c34-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="97c34-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="97c34-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="97c34-126">Validation file</span></span>  <br/> |<span data-ttu-id="97c34-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="97c34-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="97c34-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="97c34-128">Can be empty</span></span>  <br/> |<span data-ttu-id="97c34-129">False</span><span class="sxs-lookup"><span data-stu-id="97c34-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97c34-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97c34-130">See also</span></span>



- [<span data-ttu-id="97c34-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="97c34-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

