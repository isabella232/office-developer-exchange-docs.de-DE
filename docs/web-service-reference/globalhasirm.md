---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: Das GlobalHasIrm-Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützte Nachricht ist.
ms.openlocfilehash: 10b99c9a6421a89a549b69e918087f3e542ffa09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459469"
---
# <a name="globalhasirm"></a><span data-ttu-id="7cb02-103">GlobalHasIrm</span><span class="sxs-lookup"><span data-stu-id="7cb02-103">GlobalHasIrm</span></span>

<span data-ttu-id="7cb02-104">Das **GlobalHasIrm** -Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützte Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="7cb02-104">The **GlobalHasIrm** element specifies whether at least one message in the conversation and across all folders is an IRM protected message.</span></span> 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 <span data-ttu-id="7cb02-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="7cb02-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cb02-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7cb02-106">Attributes and elements</span></span>

<span data-ttu-id="7cb02-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7cb02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cb02-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7cb02-108">Attributes</span></span>

<span data-ttu-id="7cb02-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cb02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cb02-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cb02-110">Child elements</span></span>

<span data-ttu-id="7cb02-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cb02-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7cb02-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cb02-112">Parent elements</span></span>

[<span data-ttu-id="7cb02-113">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="7cb02-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="7cb02-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="7cb02-114">Text value</span></span>

<span data-ttu-id="7cb02-115">Der Textwert des **GlobalHasIrm** -Elements ist **true** , wenn mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützte Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="7cb02-115">The text value of the **GlobalHasIrm** element is **true** if at least one message in the conversation and across all folders is an IRM protected message.</span></span> <span data-ttu-id="7cb02-116">Andernfalls ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="7cb02-116">Otherwise the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7cb02-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cb02-117">Remarks</span></span>

<span data-ttu-id="7cb02-118">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7cb02-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="7cb02-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7cb02-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cb02-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7cb02-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cb02-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="7cb02-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7cb02-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7cb02-122">Schema Name</span></span>  <br/> |<span data-ttu-id="7cb02-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7cb02-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="7cb02-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7cb02-124">Validation File</span></span>  <br/> |<span data-ttu-id="7cb02-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7cb02-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7cb02-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7cb02-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="7cb02-127">True</span><span class="sxs-lookup"><span data-stu-id="7cb02-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cb02-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cb02-128">See also</span></span>



[<span data-ttu-id="7cb02-129">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="7cb02-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="7cb02-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7cb02-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

