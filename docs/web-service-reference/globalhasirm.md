---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: Das GlobalHasIrm-Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützten Nachricht ist.
ms.openlocfilehash: ad3eafcb38829e7ea57cbc7535b0f5411ad595d2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829717"
---
# <a name="globalhasirm"></a><span data-ttu-id="9fbb7-103">GlobalHasIrm</span><span class="sxs-lookup"><span data-stu-id="9fbb7-103">GlobalHasIrm</span></span>

<span data-ttu-id="9fbb7-104">Das **GlobalHasIrm** -Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützten Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-104">The **GlobalHasIrm** element specifies whether at least one message in the conversation and across all folders is an IRM protected message.</span></span> 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 <span data-ttu-id="9fbb7-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fbb7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9fbb7-106">Attributes and elements</span></span>

<span data-ttu-id="9fbb7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fbb7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fbb7-108">Attributes</span></span>

<span data-ttu-id="9fbb7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fbb7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fbb7-110">Child elements</span></span>

<span data-ttu-id="9fbb7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fbb7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fbb7-112">Parent elements</span></span>

[<span data-ttu-id="9fbb7-113">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="9fbb7-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="9fbb7-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="9fbb7-114">Text value</span></span>

<span data-ttu-id="9fbb7-115">Der Textwert der **GlobalHasIrm** -Element ist **true** , wenn mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützten Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-115">The text value of the **GlobalHasIrm** element is **true** if at least one message in the conversation and across all folders is an IRM protected message.</span></span> <span data-ttu-id="9fbb7-116">Andernfalls ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-116">Otherwise the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fbb7-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fbb7-117">Remarks</span></span>

<span data-ttu-id="9fbb7-118">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9fbb7-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fbb7-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9fbb7-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fbb7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fbb7-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9fbb7-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9fbb7-122">Schema Name</span></span>  <br/> |<span data-ttu-id="9fbb7-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9fbb7-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="9fbb7-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9fbb7-124">Validation File</span></span>  <br/> |<span data-ttu-id="9fbb7-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9fbb7-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9fbb7-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9fbb7-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fbb7-127">True</span><span class="sxs-lookup"><span data-stu-id="9fbb7-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fbb7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fbb7-128">See also</span></span>



[<span data-ttu-id="9fbb7-129">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="9fbb7-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="9fbb7-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fbb7-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

