---
title: RoutingType (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: Das RoutingType-Element definiert den Adresstyp für das Postfach.
ms.openlocfilehash: a02c3b5711a657311428d67cccabd9c8c231db67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831256"
---
# <a name="routingtype-emailaddresstype"></a><span data-ttu-id="01314-103">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="01314-103">RoutingType (EmailAddressType)</span></span>

<span data-ttu-id="01314-104">Das **RoutingType** -Element definiert den Adresstyp für das Postfach.</span><span class="sxs-lookup"><span data-stu-id="01314-104">The **RoutingType** element defines the address type for the mailbox.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="01314-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="01314-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01314-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="01314-106">Attributes and elements</span></span>

<span data-ttu-id="01314-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="01314-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01314-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="01314-108">Attributes</span></span>

<span data-ttu-id="01314-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="01314-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01314-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01314-110">Child elements</span></span>

<span data-ttu-id="01314-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="01314-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01314-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01314-112">Parent elements</span></span>

|<span data-ttu-id="01314-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="01314-113">**Element**</span></span>|<span data-ttu-id="01314-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01314-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01314-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="01314-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="01314-116">Identifiziert, die der Anrufer als sendet.</span><span class="sxs-lookup"><span data-stu-id="01314-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="01314-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="01314-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="01314-118">Identifiziert eine vollständig aufgelöster E-mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="01314-118">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="01314-119">RoomList</span><span class="sxs-lookup"><span data-stu-id="01314-119">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="01314-120">Eine Liste der Besprechungsräumen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="01314-120">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01314-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="01314-121">Text value</span></span>

<span data-ttu-id="01314-122">Der Textwert darstellt einen routing Typ.</span><span class="sxs-lookup"><span data-stu-id="01314-122">The text value represents a routing type.</span></span> <span data-ttu-id="01314-123">SMTP ist der typische Textwert für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="01314-123">SMTP is the typical text value for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01314-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01314-124">Remarks</span></span>

<span data-ttu-id="01314-125">Dieses Element ist optional im [Postfach](mailbox.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="01314-125">This element is optional in the [Mailbox](mailbox.md) element.</span></span> <span data-ttu-id="01314-126">Ein anderes [RoutingType (EmailAddress)](routingtype-emailaddress.md) -Element wird für Verfügbarkeit Operationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="01314-126">Another [RoutingType (EmailAddress)](routingtype-emailaddress.md) element is used for Availability operations.</span></span> 
  
<span data-ttu-id="01314-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="01314-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01314-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="01314-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01314-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="01314-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01314-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="01314-130">Schema Name</span></span>  <br/> |<span data-ttu-id="01314-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="01314-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="01314-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="01314-132">Validation File</span></span>  <br/> |<span data-ttu-id="01314-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01314-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01314-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="01314-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="01314-135">False</span><span class="sxs-lookup"><span data-stu-id="01314-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01314-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01314-136">See also</span></span>



- [<span data-ttu-id="01314-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="01314-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

