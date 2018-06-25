---
title: Adresse (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: Das Address-Element stellt die e-Mail-Adresse des Postfachbenutzers an.
ms.openlocfilehash: 07c634d6166d88a8912bc66081a13671e600c801
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757241"
---
# <a name="address-string"></a><span data-ttu-id="2b97f-103">Adresse (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="2b97f-103">Address (string)</span></span>

<span data-ttu-id="2b97f-104">Das **Address** -Element stellt die e-Mail-Adresse des Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="2b97f-104">The **Address** element represents the e-mail address of the mailbox user.</span></span> 
  
```xml
<Address>...</Address>
```

 <span data-ttu-id="2b97f-105">**string**</span><span class="sxs-lookup"><span data-stu-id="2b97f-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b97f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2b97f-106">Attributes and elements</span></span>

<span data-ttu-id="2b97f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b97f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b97f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b97f-108">Attributes</span></span>

<span data-ttu-id="2b97f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b97f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b97f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b97f-110">Child elements</span></span>

<span data-ttu-id="2b97f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b97f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2b97f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b97f-112">Parent elements</span></span>

|<span data-ttu-id="2b97f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b97f-113">**Element**</span></span>|<span data-ttu-id="2b97f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b97f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b97f-115">E-Mail (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2b97f-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="2b97f-116">Gibt die e-Mail-Adresse des MailboxData-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2b97f-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="2b97f-117">Dieses Element wird in den [GetUserAvailability-Vorgang](getuseravailability-operation.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b97f-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span><br/><br/> <span data-ttu-id="2b97f-118">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="2b97f-118">The following is the XPath to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="2b97f-119">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="2b97f-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="2b97f-120">Stellt den Postfachbenutzer für eine Anforderung SetUserOofSettings oder GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="2b97f-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span><br/><br/>  <span data-ttu-id="2b97f-121">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="2b97f-121">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2b97f-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="2b97f-122">Text value</span></span>

<span data-ttu-id="2b97f-123">Ein Textwert ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b97f-123">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b97f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b97f-124">Remarks</span></span>

<span data-ttu-id="2b97f-125">Dieses Element kann höchstens einmal in das Element [E-Mail (EmailAddressType)](email-emailaddresstype.md) und das [Postfach (Verfügbarkeit)](mailbox-availability.md) Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="2b97f-125">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element and the [Mailbox (Availability)](mailbox-availability.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2b97f-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2b97f-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2b97f-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2b97f-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b97f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b97f-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b97f-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2b97f-129">Schema Name</span></span>  <br/> |<span data-ttu-id="2b97f-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2b97f-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b97f-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2b97f-131">Validation File</span></span>  <br/> |<span data-ttu-id="2b97f-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b97f-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b97f-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2b97f-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b97f-134">False</span><span class="sxs-lookup"><span data-stu-id="2b97f-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b97f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b97f-135">See also</span></span>

- [<span data-ttu-id="2b97f-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b97f-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="2b97f-137">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b97f-137">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="2b97f-138">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b97f-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="2b97f-139">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="2b97f-139">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="2b97f-140">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="2b97f-140">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
- [<span data-ttu-id="2b97f-141">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="2b97f-141">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
- [<span data-ttu-id="2b97f-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="2b97f-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

