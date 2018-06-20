---
title: MaxItems wird
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4ddba6b8-0f38-42cd-96a1-0d4283f6375b
description: Das Element "MaxItems" gibt die maximale Anzahl von Elementen, die in der Anforderung zurückgeben.
ms.openlocfilehash: dffb9ba4e29915a65fe2a57b6e7a7b4468028fa1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830384"
---
# <a name="maxitems"></a><span data-ttu-id="b2695-103">MaxItems wird</span><span class="sxs-lookup"><span data-stu-id="b2695-103">MaxItems</span></span>

<span data-ttu-id="b2695-104">Das Element **"MaxItems"** gibt die maximale Anzahl von Elementen, die in der Anforderung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b2695-104">The **MaxItems** element specifies the maximum number of items to return in the request.</span></span> 
  
```XML
<MaxItems/>
```

 <span data-ttu-id="b2695-105">**int**</span><span class="sxs-lookup"><span data-stu-id="b2695-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2695-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b2695-106">Attributes and elements</span></span>

<span data-ttu-id="b2695-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b2695-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2695-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b2695-108">Attributes</span></span>

<span data-ttu-id="b2695-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2695-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2695-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2695-110">Child elements</span></span>

<span data-ttu-id="b2695-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2695-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b2695-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2695-112">Parent elements</span></span>

[<span data-ttu-id="b2695-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="b2695-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="b2695-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="b2695-114">Text value</span></span>

<span data-ttu-id="b2695-115">Der Textwert des Elements **"MaxItems"** ist die maximale Anzahl von Elementen, die in der Anforderung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b2695-115">The text value of the **MaxItems** element is the maximum number of items to return in the request.</span></span> <span data-ttu-id="b2695-116">Diese Nummer darf nicht kleiner als 0 (null) oder größer als 200 sein.</span><span class="sxs-lookup"><span data-stu-id="b2695-116">This number cannot be less than zero or greater than 200.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b2695-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b2695-117">Remarks</span></span>

<span data-ttu-id="b2695-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b2695-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b2695-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b2695-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2695-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b2695-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2695-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2695-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b2695-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b2695-122">Schema Name</span></span>  <br/> |<span data-ttu-id="b2695-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b2695-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b2695-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b2695-124">Validation File</span></span>  <br/> |<span data-ttu-id="b2695-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b2695-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b2695-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b2695-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="b2695-127">False</span><span class="sxs-lookup"><span data-stu-id="b2695-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2695-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2695-128">See also</span></span>



[<span data-ttu-id="b2695-129">GetReminders</span><span class="sxs-lookup"><span data-stu-id="b2695-129">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="b2695-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b2695-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

