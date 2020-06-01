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
description: Das MailboxDataArray-Element enthält eine Liste von Postfächern, um Verfügbarkeitsinformationen abzufragen.
ms.openlocfilehash: 894bf97a0d633d7eef0434331ccf1580fcba386e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468194"
---
# <a name="mailboxdataarray"></a><span data-ttu-id="126dd-103">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="126dd-103">MailboxDataArray</span></span>

<span data-ttu-id="126dd-104">Das **MailboxDataArray** -Element enthält eine Liste von Postfächern, um Verfügbarkeitsinformationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="126dd-104">The **MailboxDataArray** element contains a list of mailboxes to query for availability information.</span></span> 
  
- [<span data-ttu-id="126dd-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="126dd-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="126dd-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="126dd-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="126dd-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="126dd-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxDataArray>
   <MailboxData>...</MailboxData>
</MailboxDataArray>
```

<span data-ttu-id="126dd-108">**ArrayOfMailboxData**</span><span class="sxs-lookup"><span data-stu-id="126dd-108">**ArrayOfMailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="126dd-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="126dd-109">Attributes and elements</span></span>

<span data-ttu-id="126dd-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="126dd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="126dd-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="126dd-111">Attributes</span></span>

<span data-ttu-id="126dd-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="126dd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="126dd-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="126dd-113">Child elements</span></span>

|<span data-ttu-id="126dd-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="126dd-114">**Element**</span></span>|<span data-ttu-id="126dd-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="126dd-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="126dd-116">MailboxData</span><span class="sxs-lookup"><span data-stu-id="126dd-116">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="126dd-117">Stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="126dd-117">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="126dd-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="126dd-118">Parent elements</span></span>

|<span data-ttu-id="126dd-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="126dd-119">**Element**</span></span>|<span data-ttu-id="126dd-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="126dd-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="126dd-121">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="126dd-121">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="126dd-122">Enthält die Argumente, die zum Abrufen von Informationen zur Benutzerverfügbarkeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="126dd-122">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="126dd-123">Dies ist ein Stammelement.</span><span class="sxs-lookup"><span data-stu-id="126dd-123">This is a root element.</span></span>  <br/> <span data-ttu-id="126dd-124">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="126dd-124">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="126dd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="126dd-125">Remarks</span></span>

<span data-ttu-id="126dd-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="126dd-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="126dd-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="126dd-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="126dd-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="126dd-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="126dd-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="126dd-129">Schema Name</span></span>  <br/> |<span data-ttu-id="126dd-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="126dd-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="126dd-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="126dd-131">Validation File</span></span>  <br/> |<span data-ttu-id="126dd-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="126dd-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="126dd-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="126dd-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="126dd-134">False</span><span class="sxs-lookup"><span data-stu-id="126dd-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="126dd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="126dd-135">See also</span></span>

- [<span data-ttu-id="126dd-136">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="126dd-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="126dd-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="126dd-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="126dd-138">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="126dd-138">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

