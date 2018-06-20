---
title: IsMembershipGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: Das IsMembershipGroup-Element gibt einen Boolean-Wert, der angibt, ob die Entität eine Verteilergruppe oder ein Postfach ist.
ms.openlocfilehash: 03ab0dc75d2c798b7f2afeef85aa45f0349be70a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830050"
---
# <a name="ismembershipgroup"></a><span data-ttu-id="8313c-103">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="8313c-103">IsMembershipGroup</span></span>

<span data-ttu-id="8313c-104">Das **IsMembershipGroup** -Element gibt einen Boolean-Wert, der angibt, ob die Entität eine Verteilergruppe oder ein Postfach ist.</span><span class="sxs-lookup"><span data-stu-id="8313c-104">The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox.</span></span> 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 <span data-ttu-id="8313c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8313c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8313c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8313c-106">Attributes and elements</span></span>

<span data-ttu-id="8313c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8313c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8313c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8313c-108">Attributes</span></span>

<span data-ttu-id="8313c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8313c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8313c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8313c-110">Child elements</span></span>

<span data-ttu-id="8313c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8313c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8313c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8313c-112">Parent elements</span></span>

|<span data-ttu-id="8313c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8313c-113">**Element**</span></span>|<span data-ttu-id="8313c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8313c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8313c-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="8313c-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="8313c-116">Gibt ein Postfach aus einer Anforderung **GetSearchableMailboxes** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8313c-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8313c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="8313c-117">Text value</span></span>

<span data-ttu-id="8313c-118">Der Textwert **true** für das **IsMembershipGroup** -Element gibt an, dass die Entität eine Verteilergruppe oder ein Postfach ist.</span><span class="sxs-lookup"><span data-stu-id="8313c-118">A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox.</span></span> <span data-ttu-id="8313c-119">Der Wert False gibt an, dass die Entität keine Verteilergruppe oder ein Postfach ist.</span><span class="sxs-lookup"><span data-stu-id="8313c-119">A value of false indicates that the entity is not a distribution group or a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8313c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8313c-120">Remarks</span></span>

<span data-ttu-id="8313c-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8313c-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8313c-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8313c-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8313c-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8313c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8313c-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="8313c-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8313c-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8313c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="8313c-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="8313c-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="8313c-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8313c-127">Validation File</span></span>  <br/> |<span data-ttu-id="8313c-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8313c-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8313c-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8313c-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8313c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8313c-130">See also</span></span>



- [<span data-ttu-id="8313c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8313c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

