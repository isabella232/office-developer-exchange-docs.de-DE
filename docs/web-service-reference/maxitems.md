---
title: MaxItems wird
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4ddba6b8-0f38-42cd-96a1-0d4283f6375b
description: Das MaxItems wird-Element gibt die maximale Anzahl von Elementen an, die in der Anforderung zurückgegeben werden sollen.
ms.openlocfilehash: f16e9d46b59c0f562aabd5383f7f445d93414f68
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461744"
---
# <a name="maxitems"></a><span data-ttu-id="51f1e-103">MaxItems wird</span><span class="sxs-lookup"><span data-stu-id="51f1e-103">MaxItems</span></span>

<span data-ttu-id="51f1e-104">Das **MaxItems wird** -Element gibt die maximale Anzahl von Elementen an, die in der Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51f1e-104">The **MaxItems** element specifies the maximum number of items to return in the request.</span></span> 
  
```XML
<MaxItems/>
```

 <span data-ttu-id="51f1e-105">**int**</span><span class="sxs-lookup"><span data-stu-id="51f1e-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="51f1e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="51f1e-106">Attributes and elements</span></span>

<span data-ttu-id="51f1e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="51f1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51f1e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="51f1e-108">Attributes</span></span>

<span data-ttu-id="51f1e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="51f1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51f1e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51f1e-110">Child elements</span></span>

<span data-ttu-id="51f1e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="51f1e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="51f1e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51f1e-112">Parent elements</span></span>

[<span data-ttu-id="51f1e-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="51f1e-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="51f1e-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="51f1e-114">Text value</span></span>

<span data-ttu-id="51f1e-115">Der Textwert des **MaxItems wird** -Elements ist die maximale Anzahl von Elementen, die in der Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51f1e-115">The text value of the **MaxItems** element is the maximum number of items to return in the request.</span></span> <span data-ttu-id="51f1e-116">Diese Zahl darf nicht kleiner als 0 (null) oder größer als 200 sein.</span><span class="sxs-lookup"><span data-stu-id="51f1e-116">This number cannot be less than zero or greater than 200.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="51f1e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51f1e-117">Remarks</span></span>

<span data-ttu-id="51f1e-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="51f1e-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="51f1e-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="51f1e-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51f1e-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="51f1e-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51f1e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="51f1e-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="51f1e-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="51f1e-122">Schema Name</span></span>  <br/> |<span data-ttu-id="51f1e-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="51f1e-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="51f1e-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="51f1e-124">Validation File</span></span>  <br/> |<span data-ttu-id="51f1e-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="51f1e-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="51f1e-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="51f1e-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="51f1e-127">False</span><span class="sxs-lookup"><span data-stu-id="51f1e-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51f1e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51f1e-128">See also</span></span>



[<span data-ttu-id="51f1e-129">GetReminders</span><span class="sxs-lookup"><span data-stu-id="51f1e-129">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="51f1e-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="51f1e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

