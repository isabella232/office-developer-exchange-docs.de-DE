---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: Das ItemHoldPeriod-Element gibt den Zeitraum an, in dem Inhalte aufbewahrt werden sollen, die mit der Post Fach Abfrage übereinstimmen.
ms.openlocfilehash: 185666b72cc96dd88605b7baa6433d070e7ebc91
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452286"
---
# <a name="itemholdperiod"></a><span data-ttu-id="361a8-103">ItemHoldPeriod</span><span class="sxs-lookup"><span data-stu-id="361a8-103">ItemHoldPeriod</span></span>

<span data-ttu-id="361a8-104">Das **ItemHoldPeriod** -Element gibt den Zeitraum an, in dem Inhalte aufbewahrt werden sollen, die mit der Post Fach Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="361a8-104">The **ItemHoldPeriod** element specifies the amount of time to hold content that matches the mailbox query.</span></span> 
  
```XML
<ItemHoldPeriod/>
```

 <span data-ttu-id="361a8-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="361a8-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="361a8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="361a8-106">Attributes and elements</span></span>

<span data-ttu-id="361a8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="361a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="361a8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="361a8-108">Attributes</span></span>

<span data-ttu-id="361a8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="361a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="361a8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="361a8-110">Child elements</span></span>

<span data-ttu-id="361a8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="361a8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="361a8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="361a8-112">Parent elements</span></span>

[<span data-ttu-id="361a8-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="361a8-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="361a8-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="361a8-114">Text value</span></span>

<span data-ttu-id="361a8-115">Der Textwert kann "unbegrenzt" oder der Zeichenfolgenwert eines beliebigen [TimeSpan](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx) -Werts sein.</span><span class="sxs-lookup"><span data-stu-id="361a8-115">The text value can be "Unlimited" or the string value of any [Timespan](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx) value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="361a8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="361a8-116">Remarks</span></span>

<span data-ttu-id="361a8-117">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="361a8-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="361a8-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="361a8-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="361a8-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="361a8-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="361a8-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="361a8-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="361a8-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="361a8-121">Schema Name</span></span>  <br/> |<span data-ttu-id="361a8-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="361a8-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="361a8-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="361a8-123">Validation File</span></span>  <br/> |<span data-ttu-id="361a8-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="361a8-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="361a8-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="361a8-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="361a8-126">True</span><span class="sxs-lookup"><span data-stu-id="361a8-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="361a8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="361a8-127">See also</span></span>



[<span data-ttu-id="361a8-128">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="361a8-128">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)


- [<span data-ttu-id="361a8-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="361a8-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

