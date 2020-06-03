---
title: BeginTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2a60c89c-9c21-4041-9593-b244ac1608ef
description: Das BeginTime-Element gibt den Anfang der Zeitspanne an, für die Erinnerungen abgefragt werden sollen.
ms.openlocfilehash: 4f926b8e4931c187cd4d5b97d6182d609bc15a1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463377"
---
# <a name="begintime"></a><span data-ttu-id="3fa29-103">BeginTime</span><span class="sxs-lookup"><span data-stu-id="3fa29-103">BeginTime</span></span>

<span data-ttu-id="3fa29-104">Das **BeginTime** -Element gibt den Anfang der Zeitspanne an, für die Erinnerungen abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3fa29-104">The **BeginTime** element specifies the beginning of the time span to query for reminders.</span></span> 
  
```XML
<BeginTime/>
```

 <span data-ttu-id="3fa29-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="3fa29-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3fa29-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3fa29-106">Attributes and elements</span></span>

<span data-ttu-id="3fa29-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3fa29-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fa29-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3fa29-108">Attributes</span></span>

<span data-ttu-id="3fa29-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fa29-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3fa29-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fa29-110">Child elements</span></span>

<span data-ttu-id="3fa29-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fa29-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3fa29-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fa29-112">Parent elements</span></span>

[<span data-ttu-id="3fa29-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="3fa29-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="3fa29-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="3fa29-114">Text value</span></span>

<span data-ttu-id="3fa29-115">Der Textwert des **BeginTime** -Elements ist die Anfangszeit des Elements, für das die Erinnerung gilt.</span><span class="sxs-lookup"><span data-stu-id="3fa29-115">The text value of the **BeginTime** element is the beginning time of the item the reminder is for.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3fa29-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fa29-116">Remarks</span></span>

<span data-ttu-id="3fa29-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3fa29-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3fa29-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3fa29-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3fa29-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3fa29-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fa29-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fa29-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3fa29-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3fa29-121">Schema Name</span></span>  <br/> |<span data-ttu-id="3fa29-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3fa29-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3fa29-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3fa29-123">Validation File</span></span>  <br/> |<span data-ttu-id="3fa29-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3fa29-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3fa29-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3fa29-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="3fa29-126">False</span><span class="sxs-lookup"><span data-stu-id="3fa29-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fa29-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fa29-127">See also</span></span>



[<span data-ttu-id="3fa29-128">GetReminders</span><span class="sxs-lookup"><span data-stu-id="3fa29-128">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="3fa29-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3fa29-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

