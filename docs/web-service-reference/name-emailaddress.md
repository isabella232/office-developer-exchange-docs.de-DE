---
title: Name (e-mailemail)
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
description: Das Name-Element stellt den Anzeigenamen des Postfachbenutzers dar.
ms.openlocfilehash: 2c6b29f1b069f9cc72ac84e7aebfff99437e630a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466955"
---
# <a name="name-emailaddress"></a><span data-ttu-id="6841c-103">Name (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="6841c-103">Name (EmailAddress)</span></span>

<span data-ttu-id="6841c-104">Das **Name** -Element stellt den Anzeigenamen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="6841c-104">The **Name** element represents the display name of the mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="6841c-105">**String**</span><span class="sxs-lookup"><span data-stu-id="6841c-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6841c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6841c-106">Attributes and elements</span></span>

<span data-ttu-id="6841c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6841c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6841c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6841c-108">Attributes</span></span>

<span data-ttu-id="6841c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6841c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6841c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6841c-110">Child elements</span></span>

<span data-ttu-id="6841c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6841c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6841c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6841c-112">Parent elements</span></span>

|<span data-ttu-id="6841c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6841c-113">**Element**</span></span>|<span data-ttu-id="6841c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6841c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6841c-115">E-Mail (e-Mail-Adresse)</span><span class="sxs-lookup"><span data-stu-id="6841c-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="6841c-116">Stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="6841c-116">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> <br/><span data-ttu-id="6841c-117">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="6841c-117">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="6841c-118">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="6841c-118">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="6841c-119">Stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="6841c-119">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="6841c-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="6841c-120">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6841c-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="6841c-121">Text value</span></span>

<span data-ttu-id="6841c-122">Wenn dieses Element verwendet wird, ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6841c-122">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6841c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6841c-123">Remarks</span></span>

<span data-ttu-id="6841c-124">Dieses Element kann höchstens einmal im [e-Mail-Element (Epost (Email Type))](email-emailaddresstype.md) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="6841c-124">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="6841c-125">Dieses Element ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6841c-125">This element is not required.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6841c-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6841c-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6841c-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6841c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6841c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6841c-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6841c-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6841c-129">Schema Name</span></span>  <br/> |<span data-ttu-id="6841c-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6841c-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="6841c-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6841c-131">Validation File</span></span>  <br/> |<span data-ttu-id="6841c-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6841c-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6841c-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6841c-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="6841c-134">False</span><span class="sxs-lookup"><span data-stu-id="6841c-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6841c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6841c-135">See also</span></span>

- [<span data-ttu-id="6841c-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6841c-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="6841c-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="6841c-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="6841c-138">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="6841c-138">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

