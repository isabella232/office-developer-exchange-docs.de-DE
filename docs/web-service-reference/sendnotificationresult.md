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
description: Das SendNotificationResult-Element enthält die Antwort einer Clientanwendung auf eine Push-Benachrichtigung.
ms.openlocfilehash: 4ee9a0dda3d887f8fbfa2c2b34a9a077e7af37ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464889"
---
# <a name="sendnotificationresult"></a><span data-ttu-id="4c397-103">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="4c397-103">SendNotificationResult</span></span>

<span data-ttu-id="4c397-104">Das **SendNotificationResult** -Element enthält die Antwort einer Clientanwendung auf eine Push-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="4c397-104">The **SendNotificationResult** element contains the response of a client application to a push notification.</span></span> 
  
```xml
<SendNotificationResult>
   <SubscriptionStatus/>
</SendNotificationResult>
```

 <span data-ttu-id="4c397-105">**SendNotificationResultType**</span><span class="sxs-lookup"><span data-stu-id="4c397-105">**SendNotificationResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c397-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4c397-106">Attributes and elements</span></span>

<span data-ttu-id="4c397-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4c397-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c397-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4c397-108">Attributes</span></span>

<span data-ttu-id="4c397-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4c397-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c397-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c397-110">Child elements</span></span>

|<span data-ttu-id="4c397-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4c397-111">**Element**</span></span>|<span data-ttu-id="4c397-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4c397-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c397-113">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4c397-113">SubscriptionStatus</span></span>](subscriptionstatus.md) <br/> |<span data-ttu-id="4c397-114">Beschreibt den Status eines Push-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="4c397-114">Describes the status of a push subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4c397-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c397-115">Parent elements</span></span>

<span data-ttu-id="4c397-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="4c397-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c397-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c397-117">Remarks</span></span>

<span data-ttu-id="4c397-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4c397-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c397-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4c397-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c397-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c397-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4c397-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4c397-121">Schema Name</span></span>  <br/> |<span data-ttu-id="4c397-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4c397-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4c397-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4c397-123">Validation File</span></span>  <br/> |<span data-ttu-id="4c397-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4c397-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4c397-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4c397-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c397-126">False</span><span class="sxs-lookup"><span data-stu-id="4c397-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c397-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c397-127">See also</span></span>



- [<span data-ttu-id="4c397-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4c397-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

