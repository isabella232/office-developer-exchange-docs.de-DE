---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: Das IsHidden-Element enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll.
ms.openlocfilehash: a22628e9ab4a46de04fe395f2d6c1b70083a5c77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464238"
---
# <a name="ishidden"></a><span data-ttu-id="d399b-103">IsHidden</span><span class="sxs-lookup"><span data-stu-id="d399b-103">IsHidden</span></span>

<span data-ttu-id="d399b-104">Das **IsHidden** -Element enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d399b-104">The **IsHidden** element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona.</span></span> 
  
```XML
<IsHidden>true | false</IsHidden>
```

 <span data-ttu-id="d399b-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d399b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d399b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d399b-106">Attributes and elements</span></span>

<span data-ttu-id="d399b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d399b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d399b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d399b-108">Attributes</span></span>

<span data-ttu-id="d399b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d399b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d399b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d399b-110">Child elements</span></span>

<span data-ttu-id="d399b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d399b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d399b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d399b-112">Parent elements</span></span>

|<span data-ttu-id="d399b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d399b-113">**Element**</span></span>|<span data-ttu-id="d399b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d399b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d399b-115">Attribution (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="d399b-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="d399b-116">Gibt eine Instanz in einem Array von Attributen für ein **Persona** -Element an.</span><span class="sxs-lookup"><span data-stu-id="d399b-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d399b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="d399b-117">Text value</span></span>

<span data-ttu-id="d399b-118">Der Textwert **true** für das **IsHidden** -Element gibt an, dass der zugrunde liegende Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d399b-118">A text value of **true** for the **IsHidden** element indicates that the underlying contact should be hidden or displayed as part of the persona.</span></span> <span data-ttu-id="d399b-119">Der Wert **false** gibt an, dass der zugrunde liegende Kontakt nicht ausgeblendet oder als Teil der Rolle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d399b-119">A value of **false** indicates that the underlying contact should not be hidden or displayed as part of the persona.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d399b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d399b-120">Remarks</span></span>

<span data-ttu-id="d399b-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d399b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d399b-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d399b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d399b-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d399b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d399b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d399b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d399b-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d399b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d399b-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="d399b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="d399b-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d399b-127">Validation File</span></span>  <br/> |<span data-ttu-id="d399b-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d399b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d399b-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d399b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d399b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d399b-130">See also</span></span>



- [<span data-ttu-id="d399b-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d399b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

