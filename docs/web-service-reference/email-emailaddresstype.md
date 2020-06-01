---
title: E-Mail (e-Mail-Adresse)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Email
api_type:
- schema
ms.assetid: dfffa1d5-2c3c-4f56-af63-5853df462e58
description: Das e-Mail-Element stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.
ms.openlocfilehash: 2ed8de9c011a385ec6c4ebd2f8d1d47304343a0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459230"
---
# <a name="email-emailaddresstype"></a><span data-ttu-id="478f4-103">E-Mail (e-Mail-Adresse)</span><span class="sxs-lookup"><span data-stu-id="478f4-103">Email (EmailAddressType)</span></span>

<span data-ttu-id="478f4-104">Das **e-Mail-** Element stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="478f4-104">The **Email** element represents the mailbox user for a GetUserAvailability query.</span></span> 
  
- [<span data-ttu-id="478f4-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="478f4-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)  
- [<span data-ttu-id="478f4-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="478f4-106">MailboxDataArray</span></span>](mailboxdataarray.md) 
- [<span data-ttu-id="478f4-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="478f4-107">MailboxData</span></span>](mailboxdata.md) 
- [<span data-ttu-id="478f4-108">E-Mail (e-Mail-Adresse)</span><span class="sxs-lookup"><span data-stu-id="478f4-108">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
  
```xml
<Email>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Email>
```

 <span data-ttu-id="478f4-109">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="478f4-109">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="478f4-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="478f4-110">Attributes and elements</span></span>

<span data-ttu-id="478f4-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="478f4-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="478f4-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="478f4-112">Attributes</span></span>

<span data-ttu-id="478f4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="478f4-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="478f4-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="478f4-114">Child elements</span></span>

|<span data-ttu-id="478f4-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="478f4-115">**Element**</span></span>|<span data-ttu-id="478f4-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="478f4-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="478f4-117">Name (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="478f4-117">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="478f4-118">Stellt den Anzeigenamen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="478f4-118">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="478f4-119">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="478f4-119">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="478f4-120">Stellt die e-Mail-Adresse des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="478f4-120">Represents the e-mail address of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="478f4-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="478f4-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="478f4-122">Stellt das Routingprotokoll für die Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="478f4-122">Represents the routing protocol for the message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="478f4-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="478f4-123">Parent elements</span></span>

|<span data-ttu-id="478f4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="478f4-124">**Element**</span></span>|<span data-ttu-id="478f4-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="478f4-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="478f4-126">MailboxData</span><span class="sxs-lookup"><span data-stu-id="478f4-126">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="478f4-127">Stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="478f4-127">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="478f4-128">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="478f4-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="478f4-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="478f4-129">Remarks</span></span>

<span data-ttu-id="478f4-130">Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers mit Microsoft Exchange Server 2007, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="478f4-130">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="478f4-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="478f4-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="478f4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="478f4-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="478f4-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="478f4-133">Schema Name</span></span>  <br/> |<span data-ttu-id="478f4-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="478f4-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="478f4-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="478f4-135">Validation File</span></span>  <br/> |<span data-ttu-id="478f4-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="478f4-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="478f4-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="478f4-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="478f4-138">False</span><span class="sxs-lookup"><span data-stu-id="478f4-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="478f4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="478f4-139">See also</span></span>

- [<span data-ttu-id="478f4-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="478f4-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="478f4-141">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="478f4-141">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="478f4-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="478f4-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

