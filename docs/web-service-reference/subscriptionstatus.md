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
description: Das SubscriptionStatus-Element beschreibt den Status eines Push-Abonnements.
ms.openlocfilehash: 195ab229380f4386b39e5c3fd48208cf66e224f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530944"
---
# <a name="subscriptionstatus"></a><span data-ttu-id="380e2-103">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="380e2-103">SubscriptionStatus</span></span>

<span data-ttu-id="380e2-104">Das **SubscriptionStatus** -Element beschreibt den Status eines Push-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="380e2-104">The **SubscriptionStatus** element describes the status of a push subscription.</span></span> 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 <span data-ttu-id="380e2-105">**SubscriptionStatusType**</span><span class="sxs-lookup"><span data-stu-id="380e2-105">**SubscriptionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="380e2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="380e2-106">Attributes and elements</span></span>

<span data-ttu-id="380e2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="380e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="380e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="380e2-108">Attributes</span></span>

<span data-ttu-id="380e2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="380e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="380e2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="380e2-110">Child elements</span></span>

<span data-ttu-id="380e2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="380e2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="380e2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="380e2-112">Parent elements</span></span>

|<span data-ttu-id="380e2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="380e2-113">**Element**</span></span>|<span data-ttu-id="380e2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="380e2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="380e2-115">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="380e2-115">SendNotificationResult</span></span>](sendnotificationresult.md) <br/> |<span data-ttu-id="380e2-116">Enthält die Antwort der Clientanwendung auf eine Push-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="380e2-116">Contains the response of the client application' to a push notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="380e2-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="380e2-117">Text value</span></span>

<span data-ttu-id="380e2-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="380e2-118">A text value is required.</span></span> <span data-ttu-id="380e2-119">Im folgenden sind die möglichen Text Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="380e2-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="380e2-120">OK</span><span class="sxs-lookup"><span data-stu-id="380e2-120">OK</span></span>
    
- <span data-ttu-id="380e2-121">Abonnement kündigen</span><span class="sxs-lookup"><span data-stu-id="380e2-121">Unsubscribe</span></span>
    
## <a name="remarks"></a><span data-ttu-id="380e2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="380e2-122">Remarks</span></span>

<span data-ttu-id="380e2-123">Dieses Element beschreibt den Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="380e2-123">This element describes the status of the subscription.</span></span> <span data-ttu-id="380e2-124">Die Push Subscription-Clientanwendung sendet den Status zurück an den Computer, auf dem Exchange 2007 ausgeführt wird, auf dem die Clientzugriffs-Serverrolle nach jeder Push-Benachrichtigung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="380e2-124">The push subscription client application sends the status back to the computer that is running Exchange 2007 that has the Client Access server role installed after each push notification.</span></span> <span data-ttu-id="380e2-125">Wenn der **SubscriptionStatus** -Wert gleich **unsubscribe**ist, wird der Client Zugriffsserver das Senden von Benachrichtigungen beenden und das Abonnement beenden.</span><span class="sxs-lookup"><span data-stu-id="380e2-125">If the **SubscriptionStatus** value equals **Unsubscribe**, the Client Access server will stop sending notifications and end the subscription.</span></span> <span data-ttu-id="380e2-126">Wenn der **SubscriptionStatus** -Wert auf **OK**entspricht, sendet der Client Zugriffsserver weiterhin Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="380e2-126">If the **SubscriptionStatus** value equals **OK**, the Client Access server will continue to send notifications.</span></span>
  
<span data-ttu-id="380e2-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="380e2-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="380e2-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="380e2-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="380e2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="380e2-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="380e2-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="380e2-130">Schema Name</span></span>  <br/> |<span data-ttu-id="380e2-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="380e2-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="380e2-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="380e2-132">Validation File</span></span>  <br/> |<span data-ttu-id="380e2-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="380e2-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="380e2-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="380e2-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="380e2-135">False</span><span class="sxs-lookup"><span data-stu-id="380e2-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="380e2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="380e2-136">See also</span></span>



- [<span data-ttu-id="380e2-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="380e2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

