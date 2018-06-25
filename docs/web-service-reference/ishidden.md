---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: IsHidden-Element enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll.
ms.openlocfilehash: ee20bf0af287e3cddaedb5bc6d3c63ef9a7a7006
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830032"
---
# <a name="ishidden"></a><span data-ttu-id="d23f7-103">IsHidden</span><span class="sxs-lookup"><span data-stu-id="d23f7-103">IsHidden</span></span>

<span data-ttu-id="d23f7-104">**IsHidden** -Element enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d23f7-104">The **IsHidden** element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona.</span></span> 
  
```XML
<IsHidden>true | false</IsHidden>
```

 <span data-ttu-id="d23f7-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d23f7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d23f7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d23f7-106">Attributes and elements</span></span>

<span data-ttu-id="d23f7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d23f7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d23f7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d23f7-108">Attributes</span></span>

<span data-ttu-id="d23f7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d23f7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d23f7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d23f7-110">Child elements</span></span>

<span data-ttu-id="d23f7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d23f7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d23f7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d23f7-112">Parent elements</span></span>

|<span data-ttu-id="d23f7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d23f7-113">**Element**</span></span>|<span data-ttu-id="d23f7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d23f7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d23f7-115">Zuweisung (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d23f7-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="d23f7-116">Gibt eine Instanz in ein Array von Attributen für eine **Rolle** -Element an.</span><span class="sxs-lookup"><span data-stu-id="d23f7-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d23f7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d23f7-117">Text value</span></span>

<span data-ttu-id="d23f7-118">Der Textwert **true** für das **IsHidden** -Element gibt an, dass der zugrunde liegenden Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d23f7-118">A text value of **true** for the **IsHidden** element indicates that the underlying contact should be hidden or displayed as part of the persona.</span></span> <span data-ttu-id="d23f7-119">Der Wert **false** gibt an, dass der zugrunde liegenden Kontakt nicht ausgeblendet oder als Teil der Rolle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d23f7-119">A value of **false** indicates that the underlying contact should not be hidden or displayed as part of the persona.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d23f7-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d23f7-120">Remarks</span></span>

<span data-ttu-id="d23f7-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d23f7-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d23f7-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d23f7-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d23f7-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d23f7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d23f7-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d23f7-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d23f7-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d23f7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d23f7-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="d23f7-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="d23f7-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d23f7-127">Validation File</span></span>  <br/> |<span data-ttu-id="d23f7-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d23f7-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d23f7-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d23f7-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d23f7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d23f7-130">See also</span></span>



- [<span data-ttu-id="d23f7-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d23f7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

