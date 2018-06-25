---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: Das Element SubscriptionStatus beschreibt den Status eines Push-Abonnements.
ms.openlocfilehash: 1f6de15f7a3b07714899aef2ff74a8d556f8ca1d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839131"
---
# <a name="subscriptionstatus"></a><span data-ttu-id="93fd0-103">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="93fd0-103">SubscriptionStatus</span></span>

<span data-ttu-id="93fd0-104">Das Element **SubscriptionStatus** beschreibt den Status eines Push-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="93fd0-104">The **SubscriptionStatus** element describes the status of a push subscription.</span></span> 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 <span data-ttu-id="93fd0-105">**SubscriptionStatusType**</span><span class="sxs-lookup"><span data-stu-id="93fd0-105">**SubscriptionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="93fd0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="93fd0-106">Attributes and elements</span></span>

<span data-ttu-id="93fd0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="93fd0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93fd0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="93fd0-108">Attributes</span></span>

<span data-ttu-id="93fd0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="93fd0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93fd0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93fd0-110">Child elements</span></span>

<span data-ttu-id="93fd0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="93fd0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="93fd0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93fd0-112">Parent elements</span></span>

|<span data-ttu-id="93fd0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="93fd0-113">**Element**</span></span>|<span data-ttu-id="93fd0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93fd0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93fd0-115">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="93fd0-115">SendNotificationResult</span></span>](sendnotificationresult.md) <br/> |<span data-ttu-id="93fd0-116">Enthält die Antwort der Clientanwendung ' auf einer Push-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="93fd0-116">Contains the response of the client application' to a push notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="93fd0-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="93fd0-117">Text value</span></span>

<span data-ttu-id="93fd0-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="93fd0-118">A text value is required.</span></span> <span data-ttu-id="93fd0-119">Es folgen die möglichen Textwerte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="93fd0-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="93fd0-120">OK</span><span class="sxs-lookup"><span data-stu-id="93fd0-120">OK</span></span>
    
- <span data-ttu-id="93fd0-121">Kündigen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="93fd0-121">Unsubscribe</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93fd0-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93fd0-122">Remarks</span></span>

<span data-ttu-id="93fd0-123">Dieses Element beschreibt den Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="93fd0-123">This element describes the status of the subscription.</span></span> <span data-ttu-id="93fd0-124">Die Push-Abonnement-Clientanwendung gesendet, der den Status wieder auf dem Computer, auf dem Exchange 2007 ausgeführt werden, die Clientzugriffsserverrolle nach einzelnen Push Notification installiert hat.</span><span class="sxs-lookup"><span data-stu-id="93fd0-124">The push subscription client application sends the status back to the computer that is running Exchange 2007 that has the Client Access server role installed after each push notification.</span></span> <span data-ttu-id="93fd0-125">Wenn der Wert **SubscriptionStatus** **kündigen**gleich ist, wird der Clientzugriffsserver Senden von Benachrichtigungen beenden und beenden Sie das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93fd0-125">If the **SubscriptionStatus** value equals **Unsubscribe**, the Client Access server will stop sending notifications and end the subscription.</span></span> <span data-ttu-id="93fd0-126">Wenn der Wert **SubscriptionStatus** **OK**gleich ist, wird der Clientzugriffsserver weiterhin Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="93fd0-126">If the **SubscriptionStatus** value equals **OK**, the Client Access server will continue to send notifications.</span></span>
  
<span data-ttu-id="93fd0-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="93fd0-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93fd0-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="93fd0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93fd0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="93fd0-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="93fd0-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="93fd0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="93fd0-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="93fd0-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="93fd0-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="93fd0-132">Validation File</span></span>  <br/> |<span data-ttu-id="93fd0-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="93fd0-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="93fd0-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="93fd0-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="93fd0-135">False</span><span class="sxs-lookup"><span data-stu-id="93fd0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93fd0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93fd0-136">See also</span></span>



- [<span data-ttu-id="93fd0-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="93fd0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

