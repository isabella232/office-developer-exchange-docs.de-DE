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
description: Das Element RoutingType stellt das routing-Protokoll für den Empfänger.
ms.openlocfilehash: a0a6cf312bcb1d4b4818a82bc8d8d3e3f33ad6f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831255"
---
# <a name="routingtype-emailaddress"></a><span data-ttu-id="a9b23-103">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="a9b23-103">RoutingType (EmailAddress)</span></span>

<span data-ttu-id="a9b23-104">Das Element **RoutingType** stellt das routing-Protokoll für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="a9b23-104">The **RoutingType** element represents the routing protocol for the recipient.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="a9b23-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a9b23-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9b23-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a9b23-106">Attributes and elements</span></span>

<span data-ttu-id="a9b23-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a9b23-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9b23-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9b23-108">Attributes</span></span>

<span data-ttu-id="a9b23-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9b23-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9b23-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9b23-110">Child elements</span></span>

<span data-ttu-id="a9b23-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9b23-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9b23-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9b23-112">Parent elements</span></span>

|<span data-ttu-id="a9b23-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9b23-113">**Element**</span></span>|<span data-ttu-id="a9b23-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9b23-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9b23-115">E-Mail (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="a9b23-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="a9b23-116">Gibt die e-Mail-Adresse des MailboxData-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a9b23-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="a9b23-117">Dieses Element wird in den [GetUserAvailability-Vorgang](getuseravailability-operation.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9b23-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/><br/> <span data-ttu-id="a9b23-118">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a9b23-118">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="a9b23-119">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="a9b23-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="a9b23-120">Stellt den Postfachbenutzer für eine Anforderung SetUserOofSettings oder GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="a9b23-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="a9b23-121">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="a9b23-121">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9b23-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="a9b23-122">Text value</span></span>

<span data-ttu-id="a9b23-123">Ein Textwert ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9b23-123">A text value is optional.</span></span> <span data-ttu-id="a9b23-124">Der einzige gültige Wert ist SMTP.</span><span class="sxs-lookup"><span data-stu-id="a9b23-124">The only valid value is SMTP.</span></span> <span data-ttu-id="a9b23-125">Wenn kein Wert angegeben ist, wird der Standardwert der SMTP-verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9b23-125">If no value is provided, the default value of SMTP is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9b23-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9b23-126">Remarks</span></span>

<span data-ttu-id="a9b23-127">Dieses Element kann höchstens einmal im Element [E-Mail (EmailAddressType)](email-emailaddresstype.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="a9b23-127">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="a9b23-128">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9b23-128">This element is not required.</span></span> <span data-ttu-id="a9b23-129">Dieses Element ist für die Aufnahme der zukünftigen Protokolle vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a9b23-129">This element exists for the inclusion of future protocols.</span></span> <span data-ttu-id="a9b23-130">Eine andere **RoutingType** -Element wird für den Zugriff auf Elemente im Postfach des Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9b23-130">Another **RoutingType** element is used for accessing items in a user's mailbox.</span></span> 
  
<span data-ttu-id="a9b23-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a9b23-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9b23-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a9b23-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9b23-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9b23-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9b23-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a9b23-134">Schema Name</span></span>  <br/> |<span data-ttu-id="a9b23-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a9b23-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9b23-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a9b23-136">Validation File</span></span>  <br/> |<span data-ttu-id="a9b23-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9b23-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9b23-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a9b23-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9b23-139">False</span><span class="sxs-lookup"><span data-stu-id="a9b23-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9b23-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9b23-140">See also</span></span>

- [<span data-ttu-id="a9b23-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a9b23-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="a9b23-142">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="a9b23-142">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="a9b23-143">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a9b23-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

