---
title: MailboxDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxDataArray
api_type:
- schema
ms.assetid: a14af788-beee-452c-b5d0-37bcb4ef02ff
description: Das MailboxDataArray-Element enthält eine Liste der Postfächer, um Informationen zur Verfügbarkeit abzufragen.
ms.openlocfilehash: b76e71ee9127dc2221e0065a27d3c781f8b5786a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830283"
---
# <a name="mailboxdataarray"></a><span data-ttu-id="dd318-103">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="dd318-103">MailboxDataArray</span></span>

<span data-ttu-id="dd318-104">Das **MailboxDataArray** -Element enthält eine Liste der Postfächer, um Informationen zur Verfügbarkeit abzufragen.</span><span class="sxs-lookup"><span data-stu-id="dd318-104">The **MailboxDataArray** element contains a list of mailboxes to query for availability information.</span></span> 
  
- [<span data-ttu-id="dd318-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="dd318-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="dd318-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="dd318-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="dd318-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="dd318-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxDataArray>
   <MailboxData>...</MailboxData>
</MailboxDataArray>
```

<span data-ttu-id="dd318-108">**ArrayOfMailboxData**</span><span class="sxs-lookup"><span data-stu-id="dd318-108">**ArrayOfMailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dd318-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dd318-109">Attributes and elements</span></span>

<span data-ttu-id="dd318-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dd318-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd318-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd318-111">Attributes</span></span>

<span data-ttu-id="dd318-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd318-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd318-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd318-113">Child elements</span></span>

|<span data-ttu-id="dd318-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd318-114">**Element**</span></span>|<span data-ttu-id="dd318-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd318-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd318-116">MailboxData</span><span class="sxs-lookup"><span data-stu-id="dd318-116">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="dd318-117">Stellt eine einzelne Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd318-117">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd318-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd318-118">Parent elements</span></span>

|<span data-ttu-id="dd318-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd318-119">**Element**</span></span>|<span data-ttu-id="dd318-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd318-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd318-121">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="dd318-121">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="dd318-122">Enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd318-122">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="dd318-123">Dies ist eine Stammelements.</span><span class="sxs-lookup"><span data-stu-id="dd318-123">This is a root element.</span></span>  <br/> <span data-ttu-id="dd318-124">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="dd318-124">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd318-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd318-125">Remarks</span></span>

<span data-ttu-id="dd318-126">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dd318-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd318-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dd318-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd318-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd318-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd318-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dd318-129">Schema Name</span></span>  <br/> |<span data-ttu-id="dd318-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dd318-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd318-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dd318-131">Validation File</span></span>  <br/> |<span data-ttu-id="dd318-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd318-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd318-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dd318-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd318-134">False</span><span class="sxs-lookup"><span data-stu-id="dd318-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd318-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd318-135">See also</span></span>

- [<span data-ttu-id="dd318-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dd318-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="dd318-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="dd318-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="dd318-138">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="dd318-138">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

