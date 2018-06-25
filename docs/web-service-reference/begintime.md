---
title: BeginTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2a60c89c-9c21-4041-9593-b244ac1608ef
description: BeginTime-Element gibt den Beginn des Zeitraums Abfrage Erinnerungen.
ms.openlocfilehash: c6204dc0395e012cf511e6183856215b0d5ea6da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757440"
---
# <a name="begintime"></a><span data-ttu-id="cb30c-103">BeginTime</span><span class="sxs-lookup"><span data-stu-id="cb30c-103">BeginTime</span></span>

<span data-ttu-id="cb30c-104">**BeginTime** -Element gibt den Beginn des Zeitraums Abfrage Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="cb30c-104">The **BeginTime** element specifies the beginning of the time span to query for reminders.</span></span> 
  
```XML
<BeginTime/>
```

 <span data-ttu-id="cb30c-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="cb30c-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb30c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cb30c-106">Attributes and elements</span></span>

<span data-ttu-id="cb30c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cb30c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb30c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cb30c-108">Attributes</span></span>

<span data-ttu-id="cb30c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb30c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb30c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb30c-110">Child elements</span></span>

<span data-ttu-id="cb30c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb30c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb30c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb30c-112">Parent elements</span></span>

[<span data-ttu-id="cb30c-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="cb30c-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="cb30c-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="cb30c-114">Text value</span></span>

<span data-ttu-id="cb30c-115">Der Textwert des **BeginTime** -Elements ist, dass die Anfangszeit des Elements die Erinnerung für ist.</span><span class="sxs-lookup"><span data-stu-id="cb30c-115">The text value of the **BeginTime** element is the beginning time of the item the reminder is for.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cb30c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb30c-116">Remarks</span></span>

<span data-ttu-id="cb30c-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cb30c-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cb30c-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cb30c-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb30c-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cb30c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb30c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb30c-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb30c-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cb30c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="cb30c-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cb30c-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb30c-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cb30c-123">Validation File</span></span>  <br/> |<span data-ttu-id="cb30c-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cb30c-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb30c-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cb30c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb30c-126">False</span><span class="sxs-lookup"><span data-stu-id="cb30c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb30c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb30c-127">See also</span></span>



[<span data-ttu-id="cb30c-128">GetReminders</span><span class="sxs-lookup"><span data-stu-id="cb30c-128">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="cb30c-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cb30c-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

