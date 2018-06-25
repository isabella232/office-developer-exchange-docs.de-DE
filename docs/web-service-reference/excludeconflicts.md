---
title: ExcludeConflicts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExcludeConflicts
api_type:
- schema
ms.assetid: ec33ef23-8537-41eb-8d89-7eb906a1fad7
description: Das ExcludeConflicts-Element gibt an, ob vorgeschlagenen zurückgeben Zeiten für Kalender Versuche, die auf der Teilnehmerliste in Konflikt stehen.
ms.openlocfilehash: 66b69d57246942e551de2f683949870823e2e4e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758302"
---
# <a name="excludeconflicts"></a><span data-ttu-id="11e34-103">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="11e34-103">ExcludeConflicts</span></span>

<span data-ttu-id="11e34-104">Das **ExcludeConflicts** -Element gibt an, ob vorgeschlagenen zurückgeben Zeiten für Kalender Versuche, die auf der Teilnehmerliste in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="11e34-104">The **ExcludeConflicts** element specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span> 
  
[<span data-ttu-id="11e34-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="11e34-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="11e34-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="11e34-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
[<span data-ttu-id="11e34-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="11e34-107">MailboxData</span></span>](mailboxdata.md)
  
[<span data-ttu-id="11e34-108">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="11e34-108">ExcludeConflicts</span></span>](excludeconflicts.md)
  
```xml
<ExcludeConflicts>true or false</ExcludeConflicts>
```

 <span data-ttu-id="11e34-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="11e34-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11e34-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="11e34-110">Attributes and elements</span></span>

<span data-ttu-id="11e34-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="11e34-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11e34-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="11e34-112">Attributes</span></span>

<span data-ttu-id="11e34-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="11e34-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11e34-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11e34-114">Child elements</span></span>

<span data-ttu-id="11e34-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="11e34-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="11e34-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11e34-116">Parent elements</span></span>

|<span data-ttu-id="11e34-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="11e34-117">**Element**</span></span>|<span data-ttu-id="11e34-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11e34-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11e34-119">MailboxData</span><span class="sxs-lookup"><span data-stu-id="11e34-119">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="11e34-120">Stellt eine einzelne Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="11e34-120">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="11e34-121">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="11e34-121">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="11e34-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="11e34-122">Text value</span></span>

<span data-ttu-id="11e34-123">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="11e34-123">A text value is required.</span></span> <span data-ttu-id="11e34-124">Die möglichen Werte sind einen booleschen Wert **true** oder **false**.</span><span class="sxs-lookup"><span data-stu-id="11e34-124">The possible values are a Boolean **true** or **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11e34-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11e34-125">Remarks</span></span>

<span data-ttu-id="11e34-126">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="11e34-126">This element is required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="11e34-127">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="11e34-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="11e34-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="11e34-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11e34-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="11e34-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11e34-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="11e34-130">Schema Name</span></span>  <br/> |<span data-ttu-id="11e34-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="11e34-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="11e34-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="11e34-132">Validation File</span></span>  <br/> |<span data-ttu-id="11e34-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="11e34-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11e34-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="11e34-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="11e34-135">False</span><span class="sxs-lookup"><span data-stu-id="11e34-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11e34-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11e34-136">See also</span></span>



[<span data-ttu-id="11e34-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="11e34-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="11e34-138">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="11e34-138">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)


[<span data-ttu-id="11e34-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="11e34-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

