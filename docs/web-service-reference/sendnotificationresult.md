---
title: SendNotificationResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotificationResult
api_type:
- schema
ms.assetid: fa9d6202-fa66-4f10-9858-53f4f1ce14bc
description: Das SendNotificationResult-Element enthält die Antwort von einer Clientanwendung aus auf eine Push-Benachrichtigung an.
ms.openlocfilehash: 9acaa396430cf4e06a9c996834874d19dcab50ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831350"
---
# <a name="sendnotificationresult"></a><span data-ttu-id="c68c3-103">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="c68c3-103">SendNotificationResult</span></span>

<span data-ttu-id="c68c3-104">Das **SendNotificationResult** -Element enthält die Antwort von einer Clientanwendung aus auf eine Push-Benachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="c68c3-104">The **SendNotificationResult** element contains the response of a client application to a push notification.</span></span> 
  
```xml
<SendNotificationResult>
   <SubscriptionStatus/>
</SendNotificationResult>
```

 <span data-ttu-id="c68c3-105">**SendNotificationResultType**</span><span class="sxs-lookup"><span data-stu-id="c68c3-105">**SendNotificationResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c68c3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c68c3-106">Attributes and elements</span></span>

<span data-ttu-id="c68c3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c68c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c68c3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c68c3-108">Attributes</span></span>

<span data-ttu-id="c68c3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c68c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c68c3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c68c3-110">Child elements</span></span>

|<span data-ttu-id="c68c3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c68c3-111">**Element**</span></span>|<span data-ttu-id="c68c3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c68c3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c68c3-113">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="c68c3-113">SubscriptionStatus</span></span>](subscriptionstatus.md) <br/> |<span data-ttu-id="c68c3-114">Beschreibt den Status eines Push-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c68c3-114">Describes the status of a push subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c68c3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c68c3-115">Parent elements</span></span>

<span data-ttu-id="c68c3-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="c68c3-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c68c3-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c68c3-117">Remarks</span></span>

<span data-ttu-id="c68c3-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c68c3-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c68c3-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c68c3-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c68c3-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="c68c3-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c68c3-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c68c3-121">Schema Name</span></span>  <br/> |<span data-ttu-id="c68c3-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c68c3-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c68c3-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c68c3-123">Validation File</span></span>  <br/> |<span data-ttu-id="c68c3-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c68c3-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c68c3-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c68c3-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="c68c3-126">False</span><span class="sxs-lookup"><span data-stu-id="c68c3-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c68c3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c68c3-127">See also</span></span>



- [<span data-ttu-id="c68c3-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c68c3-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

