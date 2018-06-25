---
title: E-Mail (EmailAddressType)
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
description: Das E-Mail-Element darstellt, den Postfachbenutzer für eine Abfrage GetUserAvailability.
ms.openlocfilehash: 0e7848d7c4f5001ed86b06d11af1d7623b4bf1f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758153"
---
# <a name="email-emailaddresstype"></a><span data-ttu-id="b8533-103">E-Mail (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="b8533-103">Email (EmailAddressType)</span></span>

<span data-ttu-id="b8533-104">Das **E-Mail** -Element darstellt, den Postfachbenutzer für eine Abfrage GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="b8533-104">The **Email** element represents the mailbox user for a GetUserAvailability query.</span></span> 
  
- [<span data-ttu-id="b8533-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="b8533-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)  
- [<span data-ttu-id="b8533-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="b8533-106">MailboxDataArray</span></span>](mailboxdataarray.md) 
- [<span data-ttu-id="b8533-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="b8533-107">MailboxData</span></span>](mailboxdata.md) 
- [<span data-ttu-id="b8533-108">E-Mail (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="b8533-108">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
  
```xml
<Email>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Email>
```

 <span data-ttu-id="b8533-109">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="b8533-109">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8533-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b8533-110">Attributes and elements</span></span>

<span data-ttu-id="b8533-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b8533-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8533-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="b8533-112">Attributes</span></span>

<span data-ttu-id="b8533-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8533-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8533-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8533-114">Child elements</span></span>

|<span data-ttu-id="b8533-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8533-115">**Element**</span></span>|<span data-ttu-id="b8533-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8533-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8533-117">Name (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="b8533-117">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="b8533-118">Stellt den Anzeigenamen des Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="b8533-118">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="b8533-119">Adresse (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="b8533-119">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="b8533-120">Stellt die e-Mail-Adresse des Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="b8533-120">Represents the e-mail address of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="b8533-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="b8533-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="b8533-122">Stellt das routing-Protokoll für die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="b8533-122">Represents the routing protocol for the message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8533-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8533-123">Parent elements</span></span>

|<span data-ttu-id="b8533-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8533-124">**Element**</span></span>|<span data-ttu-id="b8533-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8533-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8533-126">MailboxData</span><span class="sxs-lookup"><span data-stu-id="b8533-126">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="b8533-127">Stellt eine einzelne Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8533-127">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="b8533-128">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b8533-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8533-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8533-129">Remarks</span></span>

<span data-ttu-id="b8533-130">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b8533-130">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8533-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b8533-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8533-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8533-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8533-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b8533-133">Schema Name</span></span>  <br/> |<span data-ttu-id="b8533-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b8533-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8533-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b8533-135">Validation File</span></span>  <br/> |<span data-ttu-id="b8533-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8533-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8533-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b8533-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8533-138">False</span><span class="sxs-lookup"><span data-stu-id="b8533-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8533-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8533-139">See also</span></span>

- [<span data-ttu-id="b8533-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b8533-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="b8533-141">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="b8533-141">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="b8533-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b8533-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

