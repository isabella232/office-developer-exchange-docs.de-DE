---
title: Name (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: c719c55f-d625-4e64-846f-50ac91881443
description: Das Name-Element stellt den Anzeigenamen des Postfachbenutzers an.
ms.openlocfilehash: 6d30f06c3bfd77d2715798349ab084cdf81f21a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830505"
---
# <a name="name-emailaddress"></a><span data-ttu-id="306ad-103">Name (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="306ad-103">Name (EmailAddress)</span></span>

<span data-ttu-id="306ad-104">Das **Name** -Element stellt den Anzeigenamen des Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="306ad-104">The **Name** element represents the display name of the mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="306ad-105">**String**</span><span class="sxs-lookup"><span data-stu-id="306ad-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="306ad-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="306ad-106">Attributes and elements</span></span>

<span data-ttu-id="306ad-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="306ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="306ad-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="306ad-108">Attributes</span></span>

<span data-ttu-id="306ad-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="306ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="306ad-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="306ad-110">Child elements</span></span>

<span data-ttu-id="306ad-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="306ad-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="306ad-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="306ad-112">Parent elements</span></span>

|<span data-ttu-id="306ad-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="306ad-113">**Element**</span></span>|<span data-ttu-id="306ad-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="306ad-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="306ad-115">E-Mail (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="306ad-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="306ad-116">Stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="306ad-116">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> <br/><span data-ttu-id="306ad-117">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="306ad-117">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="306ad-118">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="306ad-118">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="306ad-119">Stellt den Postfachbenutzer für eine Anforderung SetUserOofSettings oder GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="306ad-119">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="306ad-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="306ad-120">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="306ad-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="306ad-121">Text value</span></span>

<span data-ttu-id="306ad-122">Ein Textwert ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="306ad-122">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="306ad-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="306ad-123">Remarks</span></span>

<span data-ttu-id="306ad-124">Dieses Element kann höchstens einmal im Element [E-Mail (EmailAddressType)](email-emailaddresstype.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="306ad-124">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="306ad-125">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="306ad-125">This element is not required.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="306ad-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="306ad-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="306ad-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="306ad-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="306ad-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="306ad-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="306ad-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="306ad-129">Schema Name</span></span>  <br/> |<span data-ttu-id="306ad-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="306ad-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="306ad-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="306ad-131">Validation File</span></span>  <br/> |<span data-ttu-id="306ad-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="306ad-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="306ad-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="306ad-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="306ad-134">False</span><span class="sxs-lookup"><span data-stu-id="306ad-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="306ad-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="306ad-135">See also</span></span>

- [<span data-ttu-id="306ad-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="306ad-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="306ad-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="306ad-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="306ad-138">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="306ad-138">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

