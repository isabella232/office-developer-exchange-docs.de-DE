---
title: RoutingType (EmailAddress)
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
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: Das routingtype-Element stellt das Routingprotokoll für den Empfänger dar.
ms.openlocfilehash: 2193e72c38c687669f6e052b4d2526029aa89d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459034"
---
# <a name="routingtype-emailaddress"></a><span data-ttu-id="d32e6-103">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="d32e6-103">RoutingType (EmailAddress)</span></span>

<span data-ttu-id="d32e6-104">Das **routingtype** -Element stellt das Routingprotokoll für den Empfänger dar.</span><span class="sxs-lookup"><span data-stu-id="d32e6-104">The **RoutingType** element represents the routing protocol for the recipient.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="d32e6-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d32e6-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d32e6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d32e6-106">Attributes and elements</span></span>

<span data-ttu-id="d32e6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d32e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d32e6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d32e6-108">Attributes</span></span>

<span data-ttu-id="d32e6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d32e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d32e6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d32e6-110">Child elements</span></span>

<span data-ttu-id="d32e6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d32e6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d32e6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d32e6-112">Parent elements</span></span>

|<span data-ttu-id="d32e6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d32e6-113">**Element**</span></span>|<span data-ttu-id="d32e6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d32e6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d32e6-115">E-Mail (e-Mail-Adresse)</span><span class="sxs-lookup"><span data-stu-id="d32e6-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="d32e6-116">Gibt die e-Mail-Adresse des MailboxData-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d32e6-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="d32e6-117">Dieses Element wird im GetUserAvailability- [Vorgang](getuseravailability-operation.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d32e6-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/><br/> <span data-ttu-id="d32e6-118">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d32e6-118">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="d32e6-119">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="d32e6-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="d32e6-120">Stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="d32e6-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="d32e6-121">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="d32e6-121">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d32e6-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="d32e6-122">Text value</span></span>

<span data-ttu-id="d32e6-123">Ein Textwert ist optional.</span><span class="sxs-lookup"><span data-stu-id="d32e6-123">A text value is optional.</span></span> <span data-ttu-id="d32e6-124">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d32e6-124">The following are the possible values:</span></span>

* <span data-ttu-id="d32e6-125">SMTP</span><span class="sxs-lookup"><span data-stu-id="d32e6-125">SMTP</span></span>
* <span data-ttu-id="d32e6-126">Ex</span><span class="sxs-lookup"><span data-stu-id="d32e6-126">EX</span></span>

<span data-ttu-id="d32e6-127">Wenn kein Wert angegeben wird, wird der Standardwert von SMTP verwendet.</span><span class="sxs-lookup"><span data-stu-id="d32e6-127">If no value is provided, the default value of SMTP is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d32e6-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d32e6-128">Remarks</span></span>

<span data-ttu-id="d32e6-129">Dieses Element kann höchstens einmal im [e-Mail-Element (Epost (Email Type))](email-emailaddresstype.md) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d32e6-129">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="d32e6-130">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d32e6-130">This element is not required.</span></span> <span data-ttu-id="d32e6-131">Dieses Element ist für die Integration zukünftiger Protokolle vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d32e6-131">This element exists for the inclusion of future protocols.</span></span> <span data-ttu-id="d32e6-132">Ein anderes **Routing** Type-Element wird für den Zugriff auf Elemente im Postfach eines Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="d32e6-132">Another **RoutingType** element is used for accessing items in a user's mailbox.</span></span> 
  
<span data-ttu-id="d32e6-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d32e6-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d32e6-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d32e6-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d32e6-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d32e6-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d32e6-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d32e6-136">Schema Name</span></span>  <br/> |<span data-ttu-id="d32e6-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d32e6-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="d32e6-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d32e6-138">Validation File</span></span>  <br/> |<span data-ttu-id="d32e6-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d32e6-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d32e6-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d32e6-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="d32e6-141">False</span><span class="sxs-lookup"><span data-stu-id="d32e6-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d32e6-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d32e6-142">See also</span></span>

- [<span data-ttu-id="d32e6-143">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d32e6-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="d32e6-144">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d32e6-144">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="d32e6-145">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="d32e6-145">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

