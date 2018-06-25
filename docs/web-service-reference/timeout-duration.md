---
title: Timeout (Dauer)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: Das Timeout-Element gibt die Zeitdauer, bevor ein Pullabonnement vom Server ein Timeout aufgetreten ist.
ms.openlocfilehash: 23b210dcdd87f2388aecec246068f12ec6c69a78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839186"
---
# <a name="timeout-duration"></a><span data-ttu-id="de6b2-103">Timeout (Dauer)</span><span class="sxs-lookup"><span data-stu-id="de6b2-103">Timeout (duration)</span></span>

<span data-ttu-id="de6b2-104">Das **Timeout** -Element gibt die Zeitdauer, bevor ein Pullabonnement vom Server ein Timeout aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="de6b2-104">The **Timeout** element specifies the length of time before a pull subscription is timed out by the server.</span></span> 
  
```XML
<Timeout></Timeout>
```

 <span data-ttu-id="de6b2-105">**SubscriptionTimeoutType**</span><span class="sxs-lookup"><span data-stu-id="de6b2-105">**SubscriptionTimeoutType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de6b2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="de6b2-106">Attributes and elements</span></span>

<span data-ttu-id="de6b2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="de6b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de6b2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="de6b2-108">Attributes</span></span>

<span data-ttu-id="de6b2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="de6b2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de6b2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de6b2-110">Child elements</span></span>

<span data-ttu-id="de6b2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="de6b2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="de6b2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de6b2-112">Parent elements</span></span>

[<span data-ttu-id="de6b2-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="de6b2-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
## <a name="text-value"></a><span data-ttu-id="de6b2-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="de6b2-114">Text value</span></span>

<span data-ttu-id="de6b2-115">Der Textwert der **Timeout** -Element ist die Zeitdauer in Minuten ein, bevor ein Pullabonnement vom Server ein Timeout aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="de6b2-115">The text value of the **Timeout** element is the length of time, in minutes, before a pull subscription is timed out by the server.</span></span> <span data-ttu-id="de6b2-116">Der Mindestwert ist 1. Der Höchstwert ist 1440.</span><span class="sxs-lookup"><span data-stu-id="de6b2-116">The minimum value is 1; the maximum value is 1440.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de6b2-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de6b2-117">Remarks</span></span>

<span data-ttu-id="de6b2-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="de6b2-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="de6b2-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="de6b2-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de6b2-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="de6b2-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de6b2-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="de6b2-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de6b2-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="de6b2-122">Schema name</span></span>  <br/> |<span data-ttu-id="de6b2-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="de6b2-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="de6b2-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="de6b2-124">Validation file</span></span>  <br/> |<span data-ttu-id="de6b2-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="de6b2-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de6b2-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="de6b2-126">Can be empty</span></span>  <br/> ||
   

