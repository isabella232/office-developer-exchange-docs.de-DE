---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: Das ItemHoldPeriod-Element gibt die Zeitspanne für Inhalte, die die Postfach-Abfrage entspricht.
ms.openlocfilehash: 212d765aa3f0493dd4f3051de483fa08a6fa8ac7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830144"
---
# <a name="itemholdperiod"></a><span data-ttu-id="7987a-103">ItemHoldPeriod</span><span class="sxs-lookup"><span data-stu-id="7987a-103">ItemHoldPeriod</span></span>

<span data-ttu-id="7987a-104">Das **ItemHoldPeriod** -Element gibt die Zeitspanne für Inhalte, die die Postfach-Abfrage entspricht.</span><span class="sxs-lookup"><span data-stu-id="7987a-104">The **ItemHoldPeriod** element specifies the amount of time to hold content that matches the mailbox query.</span></span> 
  
```XML
<ItemHoldPeriod/>
```

 <span data-ttu-id="7987a-105">**string**</span><span class="sxs-lookup"><span data-stu-id="7987a-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7987a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7987a-106">Attributes and elements</span></span>

<span data-ttu-id="7987a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7987a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7987a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7987a-108">Attributes</span></span>

<span data-ttu-id="7987a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7987a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7987a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7987a-110">Child elements</span></span>

<span data-ttu-id="7987a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7987a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7987a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7987a-112">Parent elements</span></span>

[<span data-ttu-id="7987a-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="7987a-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="7987a-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="7987a-114">Text value</span></span>

<span data-ttu-id="7987a-115">Der Textwert kann "Unbegrenzt" oder den Zeichenfolgenwert, der einen beliebigen Wert [Timespan](http://msdn.microsoft.com/en-us/library/1ecy8h51%28v=vs.110%29.aspx) sein.</span><span class="sxs-lookup"><span data-stu-id="7987a-115">The text value can be "Unlimited" or the string value of any [Timespan](http://msdn.microsoft.com/en-us/library/1ecy8h51%28v=vs.110%29.aspx) value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7987a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7987a-116">Remarks</span></span>

<span data-ttu-id="7987a-117">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7987a-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="7987a-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7987a-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7987a-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7987a-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7987a-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="7987a-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7987a-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7987a-121">Schema Name</span></span>  <br/> |<span data-ttu-id="7987a-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7987a-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7987a-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7987a-123">Validation File</span></span>  <br/> |<span data-ttu-id="7987a-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7987a-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7987a-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7987a-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="7987a-126">True</span><span class="sxs-lookup"><span data-stu-id="7987a-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7987a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7987a-127">See also</span></span>



[<span data-ttu-id="7987a-128">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="7987a-128">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)


- [<span data-ttu-id="7987a-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7987a-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

