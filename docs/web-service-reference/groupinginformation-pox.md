---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: Das GroupingInformation-Element enthält einen Wert, der verwendet wird, um das Postfach des Benutzers zu gruppieren, um die Affinität beizubehalten, wenn Benachrichtigungen über mehrere Postfächer abonniert werden.
ms.openlocfilehash: 7cab5d68f7dd5ec1f6caded5b9da6cfee03f3a67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530078"
---
# <a name="groupinginformation-pox"></a><span data-ttu-id="aea4a-103">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="aea4a-103">GroupingInformation (POX)</span></span>

<span data-ttu-id="aea4a-104">Das **GroupingInformation** -Element enthält einen Wert, der verwendet wird, um das Postfach des Benutzers zu gruppieren, um die [Affinität beizubehalten](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) , wenn Benachrichtigungen über mehrere Postfächer abonniert werden.</span><span class="sxs-lookup"><span data-stu-id="aea4a-104">The **GroupingInformation** element contains a value that is used to group the user's mailbox to [maintain affinity](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) when subscribing to notifications across multiple mailboxes.</span></span> 
  
[<span data-ttu-id="aea4a-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="aea4a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="aea4a-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="aea4a-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="aea4a-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="aea4a-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="aea4a-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="aea4a-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="aea4a-109">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="aea4a-109">GroupingInformation (POX)</span></span>](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="aea4a-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aea4a-110">Attributes and elements</span></span>

<span data-ttu-id="aea4a-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aea4a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aea4a-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="aea4a-112">Attributes</span></span>

<span data-ttu-id="aea4a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="aea4a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aea4a-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aea4a-114">Child elements</span></span>

<span data-ttu-id="aea4a-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="aea4a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aea4a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aea4a-116">Parent elements</span></span>

|<span data-ttu-id="aea4a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="aea4a-117">**Element**</span></span>|<span data-ttu-id="aea4a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aea4a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aea4a-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="aea4a-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="aea4a-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="aea4a-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aea4a-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="aea4a-121">Text value</span></span>

<span data-ttu-id="aea4a-122">Der Textwert wird mit dem Wert des **GroupingInformation** -Elements für andere Postfächer verglichen.</span><span class="sxs-lookup"><span data-stu-id="aea4a-122">The text value is compared to the value of the **GroupingInformation** element for other mailboxes.</span></span> <span data-ttu-id="aea4a-123">Postfächer, die denselben Wert aufweisen und denselben Exchange-Webdienste-Endpunkt verwenden, können zusammen gruppiert werden, um die Affinität beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="aea4a-123">Mailboxes that have the same value and use the same Exchange Web Services (EWS) endpoint can be grouped together to maintain affinity.</span></span> <span data-ttu-id="aea4a-124">Weitere Informationen finden Sie unter [MAINTAIN Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aea4a-124">For more details, see [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aea4a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aea4a-125">Remarks</span></span>

<span data-ttu-id="aea4a-126">Das **GroupingInformation** -Element gilt nur für **Protokoll** Elemente, die über ein untergeordnetes [Type (POX)-](type-pox.md) Element mit dem Wert "expr" verfügen.</span><span class="sxs-lookup"><span data-stu-id="aea4a-126">The **GroupingInformation** element is only applicable to **Protocol** elements that have a [Type (POX)](type-pox.md) child element with a value of "EXPR".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aea4a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aea4a-127">See also</span></span>

- [<span data-ttu-id="aea4a-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="aea4a-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
- [<span data-ttu-id="aea4a-129">Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange</span><span class="sxs-lookup"><span data-stu-id="aea4a-129">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

