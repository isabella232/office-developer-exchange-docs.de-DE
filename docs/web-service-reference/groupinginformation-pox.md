---
title: Werten "groupinginformation" (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: Das Werten "groupinginformation"-Element enthält einen Wert, der das Postfach des Benutzers zum Affinität verwalten, wenn Sie über mehrere Postfächer auf Benachrichtigungen abonnieren gruppiert verwendet wird.
ms.openlocfilehash: bcde002c794ac79d9515befc0755c1f954ee8706
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829781"
---
# <a name="groupinginformation-pox"></a><span data-ttu-id="f78e1-103">Werten "groupinginformation" (POX)</span><span class="sxs-lookup"><span data-stu-id="f78e1-103">GroupingInformation (POX)</span></span>

<span data-ttu-id="f78e1-104">Das **Werten "groupinginformation"** -Element enthält einen Wert, der verwendet wird, um das Postfach des Benutzers zum [Aufrechterhalten der Affinität](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) beim Abonnieren von Benachrichtigungen über mehrere Postfächer zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f78e1-104">The **GroupingInformation** element contains a value that is used to group the user's mailbox to [maintain affinity](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) when subscribing to notifications across multiple mailboxes.</span></span> 
  
[<span data-ttu-id="f78e1-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="f78e1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="f78e1-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="f78e1-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="f78e1-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="f78e1-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="f78e1-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="f78e1-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="f78e1-109">Werten "groupinginformation" (POX)</span><span class="sxs-lookup"><span data-stu-id="f78e1-109">GroupingInformation (POX)</span></span>](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f78e1-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f78e1-110">Attributes and elements</span></span>

<span data-ttu-id="f78e1-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f78e1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f78e1-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="f78e1-112">Attributes</span></span>

<span data-ttu-id="f78e1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f78e1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f78e1-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f78e1-114">Child elements</span></span>

<span data-ttu-id="f78e1-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="f78e1-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f78e1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f78e1-116">Parent elements</span></span>

|<span data-ttu-id="f78e1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f78e1-117">**Element**</span></span>|<span data-ttu-id="f78e1-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f78e1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f78e1-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="f78e1-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f78e1-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="f78e1-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f78e1-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="f78e1-121">Text value</span></span>

<span data-ttu-id="f78e1-122">Der Textwert wird auf den Wert des Elements für andere Postfächer **Werten "groupinginformation"** verglichen.</span><span class="sxs-lookup"><span data-stu-id="f78e1-122">The text value is compared to the value of the **GroupingInformation** element for other mailboxes.</span></span> <span data-ttu-id="f78e1-123">Postfächer, die den gleichen Wert und verwenden den gleichen Exchange-Webdienste (EWS) Endpunkt können gruppiert werden, um die Affinität verwalten.</span><span class="sxs-lookup"><span data-stu-id="f78e1-123">Mailboxes that have the same value and use the same Exchange Web Services (EWS) endpoint can be grouped together to maintain affinity.</span></span> <span data-ttu-id="f78e1-124">Weitere Informationen finden Sie unter [Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange verwalten](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f78e1-124">For more details, see [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f78e1-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f78e1-125">Remarks</span></span>

<span data-ttu-id="f78e1-126">Das Element **Werten "groupinginformation"** gilt nur für **Protokoll** -Elemente, die ein untergeordnetes Element [Typ (POX)](type-pox.md) , mit dem Wert "AUSDR" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f78e1-126">The **GroupingInformation** element is only applicable to **Protocol** elements that have a [Type (POX)](type-pox.md) child element with a value of "EXPR".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f78e1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f78e1-127">See also</span></span>

- [<span data-ttu-id="f78e1-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="f78e1-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
- [<span data-ttu-id="f78e1-129">Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange</span><span class="sxs-lookup"><span data-stu-id="f78e1-129">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

