---
title: Timeout (Dauer)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: Das Timeout-Element gibt die Zeitdauer vor dem Timeout eines Pullabonnements durch den Server an.
ms.openlocfilehash: b5b0e77d794080cd8e0da1e14acf4cb059b80b08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460281"
---
# <a name="timeout-duration"></a><span data-ttu-id="0c909-103">Timeout (Dauer)</span><span class="sxs-lookup"><span data-stu-id="0c909-103">Timeout (duration)</span></span>

<span data-ttu-id="0c909-104">Das **Timeout** -Element gibt die Zeitdauer vor dem Timeout eines Pullabonnements durch den Server an.</span><span class="sxs-lookup"><span data-stu-id="0c909-104">The **Timeout** element specifies the length of time before a pull subscription is timed out by the server.</span></span> 
  
```XML
<Timeout></Timeout>
```

 <span data-ttu-id="0c909-105">**SubscriptionTimeoutType**</span><span class="sxs-lookup"><span data-stu-id="0c909-105">**SubscriptionTimeoutType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c909-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c909-106">Attributes and elements</span></span>

<span data-ttu-id="0c909-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0c909-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c909-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c909-108">Attributes</span></span>

<span data-ttu-id="0c909-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c909-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c909-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c909-110">Child elements</span></span>

<span data-ttu-id="0c909-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c909-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0c909-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c909-112">Parent elements</span></span>

[<span data-ttu-id="0c909-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="0c909-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
## <a name="text-value"></a><span data-ttu-id="0c909-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="0c909-114">Text value</span></span>

<span data-ttu-id="0c909-115">Der Textwert des **Timeout** -Elements ist die Zeitdauer in Minuten, bevor ein Pullabonnement vom Server überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="0c909-115">The text value of the **Timeout** element is the length of time, in minutes, before a pull subscription is timed out by the server.</span></span> <span data-ttu-id="0c909-116">Der Minimalwert ist 1; der Höchstwert ist 1440.</span><span class="sxs-lookup"><span data-stu-id="0c909-116">The minimum value is 1; the maximum value is 1440.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c909-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c909-117">Remarks</span></span>

<span data-ttu-id="0c909-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0c909-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0c909-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0c909-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c909-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0c909-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c909-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c909-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c909-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0c909-122">Schema name</span></span>  <br/> |<span data-ttu-id="0c909-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0c909-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="0c909-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0c909-124">Validation file</span></span>  <br/> |<span data-ttu-id="0c909-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0c909-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c909-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0c909-126">Can be empty</span></span>  <br/> ||
   

