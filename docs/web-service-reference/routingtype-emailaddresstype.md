---
title: Routingtype (e-mailemailtype)
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
description: Das Routing Type-Element definiert den Adresstyp für das Postfach.
ms.openlocfilehash: d4229f2857a5c99cc9bb7ff9b9b103de099a0055
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465086"
---
# <a name="routingtype-emailaddresstype"></a><span data-ttu-id="8efd6-103">Routingtype (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="8efd6-103">RoutingType (EmailAddressType)</span></span>

<span data-ttu-id="8efd6-104">Das **Routing** Type-Element definiert den Adresstyp für das Postfach.</span><span class="sxs-lookup"><span data-stu-id="8efd6-104">The **RoutingType** element defines the address type for the mailbox.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="8efd6-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="8efd6-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8efd6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8efd6-106">Attributes and elements</span></span>

<span data-ttu-id="8efd6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8efd6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8efd6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8efd6-108">Attributes</span></span>

<span data-ttu-id="8efd6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8efd6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8efd6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8efd6-110">Child elements</span></span>

<span data-ttu-id="8efd6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8efd6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8efd6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8efd6-112">Parent elements</span></span>

|<span data-ttu-id="8efd6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8efd6-113">**Element**</span></span>|<span data-ttu-id="8efd6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8efd6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8efd6-115">Actingies</span><span class="sxs-lookup"><span data-stu-id="8efd6-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="8efd6-116">Gibt an, wen der Anrufer sendet.</span><span class="sxs-lookup"><span data-stu-id="8efd6-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="8efd6-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="8efd6-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="8efd6-118">Identifiziert eine vollständig aufgelöste e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8efd6-118">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="8efd6-119">RoomList</span><span class="sxs-lookup"><span data-stu-id="8efd6-119">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="8efd6-120">Gibt eine Liste von Besprechungsräumen an.</span><span class="sxs-lookup"><span data-stu-id="8efd6-120">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8efd6-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="8efd6-121">Text value</span></span>

<span data-ttu-id="8efd6-122">Der Wert Text stellt einen Routingtyp dar.</span><span class="sxs-lookup"><span data-stu-id="8efd6-122">The text value represents a routing type.</span></span> <span data-ttu-id="8efd6-123">SMTP ist der typische Textwert für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="8efd6-123">SMTP is the typical text value for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8efd6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8efd6-124">Remarks</span></span>

<span data-ttu-id="8efd6-125">Dieses Element ist im [Post Fach](mailbox.md) Element optional.</span><span class="sxs-lookup"><span data-stu-id="8efd6-125">This element is optional in the [Mailbox](mailbox.md) element.</span></span> <span data-ttu-id="8efd6-126">Für Verfügbarkeits Vorgänge wird ein anderes [Routing Type-Element (Email)](routingtype-emailaddress.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8efd6-126">Another [RoutingType (EmailAddress)](routingtype-emailaddress.md) element is used for Availability operations.</span></span> 
  
<span data-ttu-id="8efd6-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8efd6-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8efd6-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8efd6-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8efd6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8efd6-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8efd6-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8efd6-130">Schema Name</span></span>  <br/> |<span data-ttu-id="8efd6-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8efd6-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="8efd6-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8efd6-132">Validation File</span></span>  <br/> |<span data-ttu-id="8efd6-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8efd6-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8efd6-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8efd6-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="8efd6-135">False</span><span class="sxs-lookup"><span data-stu-id="8efd6-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8efd6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8efd6-136">See also</span></span>



- [<span data-ttu-id="8efd6-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8efd6-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

