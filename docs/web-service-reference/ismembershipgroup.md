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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459286"
---
# <a name="ismembershipgroup"></a><span data-ttu-id="a2844-103">Ismembershipgroup</span><span class="sxs-lookup"><span data-stu-id="a2844-103">IsMembershipGroup</span></span>

<span data-ttu-id="a2844-104">Das **ismembershipgroup** -Element gibt einen booleschen Wert an, der angibt, ob es sich bei der Entität um eine Verteilergruppe oder ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="a2844-104">The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox.</span></span> 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 <span data-ttu-id="a2844-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="a2844-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2844-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a2844-106">Attributes and elements</span></span>

<span data-ttu-id="a2844-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a2844-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2844-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a2844-108">Attributes</span></span>

<span data-ttu-id="a2844-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a2844-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a2844-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2844-110">Child elements</span></span>

<span data-ttu-id="a2844-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a2844-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a2844-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a2844-112">Parent elements</span></span>

|<span data-ttu-id="a2844-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a2844-113">**Element**</span></span>|<span data-ttu-id="a2844-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a2844-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2844-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="a2844-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="a2844-116">Gibt ein Postfach an, das von einer **GetSearchableMailboxes** -Anforderung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a2844-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a2844-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="a2844-117">Text value</span></span>

<span data-ttu-id="a2844-118">Der Textwert **true** für das **ismembershipgroup** -Element gibt an, dass es sich bei der Entität um eine Verteilergruppe oder um ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="a2844-118">A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox.</span></span> <span data-ttu-id="a2844-119">Der Wert false gibt an, dass es sich bei der Entität nicht um eine Verteilergruppe oder um ein Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="a2844-119">A value of false indicates that the entity is not a distribution group or a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a2844-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2844-120">Remarks</span></span>

<span data-ttu-id="a2844-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a2844-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a2844-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a2844-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2844-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a2844-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2844-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2844-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a2844-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a2844-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a2844-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="a2844-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="a2844-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a2844-127">Validation File</span></span>  <br/> |<span data-ttu-id="a2844-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a2844-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a2844-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a2844-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a2844-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2844-130">See also</span></span>



- [<span data-ttu-id="a2844-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a2844-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

