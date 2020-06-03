---
title: MakeItemImmutable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: Das MakeItemImmutable-Element gibt einen booleschen Wert an, der angibt, ob ein Element als schreibgeschützt festgelegt werden soll.
ms.openlocfilehash: 05c6e3343b8ba892048174ad98c9d31fe8da685b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465863"
---
# <a name="makeitemimmutable"></a><span data-ttu-id="2ab0e-103">MakeItemImmutable</span><span class="sxs-lookup"><span data-stu-id="2ab0e-103">MakeItemImmutable</span></span>

<span data-ttu-id="2ab0e-104">Das **MakeItemImmutable** -Element gibt einen booleschen Wert an, der angibt, ob ein Element als schreibgeschützt festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-104">The **MakeItemImmutable** element specifies a Boolean value that indicates whether an item should be made read-only.</span></span> 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 <span data-ttu-id="2ab0e-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="2ab0e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ab0e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2ab0e-106">Attributes and elements</span></span>

<span data-ttu-id="2ab0e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ab0e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2ab0e-108">Attributes</span></span>

<span data-ttu-id="2ab0e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ab0e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ab0e-110">Child elements</span></span>

<span data-ttu-id="2ab0e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2ab0e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ab0e-112">Parent elements</span></span>

[<span data-ttu-id="2ab0e-113">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="2ab0e-113">UpdateItemInRecoverableItems</span></span>](updateiteminrecoverableitems.md)
  
## <a name="text-value"></a><span data-ttu-id="2ab0e-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="2ab0e-114">Text value</span></span>

<span data-ttu-id="2ab0e-115">Der Textwert **true** für das **MakeItemImmutable** -Element gibt an, dass das Element als schreibgeschützt festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-115">A text value of **true** for the **MakeItemImmutable** element indicates that the item should be made read-only.</span></span> <span data-ttu-id="2ab0e-116">Der Wert **false** gibt an, dass das Element Lese-/Schreibzugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-116">A value of **false** indicates that the item allows read-write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2ab0e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ab0e-117">Remarks</span></span>

<span data-ttu-id="2ab0e-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2ab0e-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2ab0e-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ab0e-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2ab0e-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ab0e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ab0e-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2ab0e-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2ab0e-122">Schema name</span></span>  <br/> |<span data-ttu-id="2ab0e-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2ab0e-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2ab0e-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2ab0e-124">Validation file</span></span>  <br/> |<span data-ttu-id="2ab0e-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2ab0e-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2ab0e-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2ab0e-126">Can be empty</span></span>  <br/> ||
   

