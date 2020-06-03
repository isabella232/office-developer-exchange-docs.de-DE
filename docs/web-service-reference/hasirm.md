---
title: HasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fedc04e0-cfd2-4652-a2a8-51de859ae847
description: Das HasIrm-Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und der aktuelle Ordner eine IRM-geschützte Nachricht ist.
ms.openlocfilehash: 1596610ed5f6b2bac353900624fbec9140aaa693
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462780"
---
# <a name="hasirm"></a><span data-ttu-id="d072c-103">HasIrm</span><span class="sxs-lookup"><span data-stu-id="d072c-103">HasIrm</span></span>

<span data-ttu-id="d072c-104">Das **HasIrm** -Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und der aktuelle Ordner eine IRM-geschützte Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="d072c-104">The **HasIrm** element specifies whether at least one message in the conversation and the current folder is an IRM protected message.</span></span> 
  
```XML
<HasIrm> true | false </HasIrm>
```

 <span data-ttu-id="d072c-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d072c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d072c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d072c-106">Attributes and elements</span></span>

<span data-ttu-id="d072c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d072c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d072c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d072c-108">Attributes</span></span>

<span data-ttu-id="d072c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d072c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d072c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d072c-110">Child elements</span></span>

<span data-ttu-id="d072c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d072c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d072c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d072c-112">Parent elements</span></span>

[<span data-ttu-id="d072c-113">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d072c-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="d072c-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="d072c-114">Text value</span></span>

<span data-ttu-id="d072c-115">Der Textwert des **HasIrm** -Elements ist **true** , wenn mindestens eine Nachricht in der Unterhaltung und der aktuelle Ordner über IRM verfügt.</span><span class="sxs-lookup"><span data-stu-id="d072c-115">The text value of the **HasIrm** element is **true** if at least one message in the conversation and the current folder has IRM.</span></span> <span data-ttu-id="d072c-116">Andernfalls ist der Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="d072c-116">Otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d072c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d072c-117">Remarks</span></span>

<span data-ttu-id="d072c-118">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d072c-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="d072c-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d072c-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d072c-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d072c-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d072c-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d072c-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d072c-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d072c-122">Schema Name</span></span>  <br/> |<span data-ttu-id="d072c-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d072c-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="d072c-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d072c-124">Validation File</span></span>  <br/> |<span data-ttu-id="d072c-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d072c-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d072c-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d072c-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="d072c-127">True</span><span class="sxs-lookup"><span data-stu-id="d072c-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d072c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d072c-128">See also</span></span>



[<span data-ttu-id="d072c-129">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d072c-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="d072c-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d072c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

