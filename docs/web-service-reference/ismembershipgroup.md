---
title: Ismembershipgroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: Das ismembershipgroup-Element gibt einen booleschen Wert an, der angibt, ob es sich bei der Entität um eine Verteilergruppe oder ein Postfach handelt.
ms.openlocfilehash: ed79961c6d13ab226c0b489103ef3d2c4a08668d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459286"
---
# <a name="ismembershipgroup"></a><span data-ttu-id="0f494-103">Ismembershipgroup</span><span class="sxs-lookup"><span data-stu-id="0f494-103">IsMembershipGroup</span></span>

<span data-ttu-id="0f494-104">Das **ismembershipgroup** -Element gibt einen booleschen Wert an, der angibt, ob es sich bei der Entität um eine Verteilergruppe oder ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="0f494-104">The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox.</span></span> 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 <span data-ttu-id="0f494-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="0f494-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0f494-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0f494-106">Attributes and elements</span></span>

<span data-ttu-id="0f494-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0f494-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f494-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0f494-108">Attributes</span></span>

<span data-ttu-id="0f494-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0f494-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0f494-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f494-110">Child elements</span></span>

<span data-ttu-id="0f494-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0f494-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0f494-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f494-112">Parent elements</span></span>

|<span data-ttu-id="0f494-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f494-113">**Element**</span></span>|<span data-ttu-id="0f494-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f494-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f494-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="0f494-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="0f494-116">Gibt ein Postfach an, das von einer **GetSearchableMailboxes** -Anforderung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0f494-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0f494-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="0f494-117">Text value</span></span>

<span data-ttu-id="0f494-118">Der Textwert **true** für das **ismembershipgroup** -Element gibt an, dass es sich bei der Entität um eine Verteilergruppe oder um ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="0f494-118">A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox.</span></span> <span data-ttu-id="0f494-119">Der Wert false gibt an, dass es sich bei der Entität nicht um eine Verteilergruppe oder um ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="0f494-119">A value of false indicates that the entity is not a distribution group or a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0f494-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f494-120">Remarks</span></span>

<span data-ttu-id="0f494-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0f494-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0f494-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0f494-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f494-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0f494-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f494-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f494-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0f494-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0f494-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0f494-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="0f494-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="0f494-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0f494-127">Validation File</span></span>  <br/> |<span data-ttu-id="0f494-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0f494-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0f494-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0f494-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0f494-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f494-130">See also</span></span>



- [<span data-ttu-id="0f494-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0f494-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

