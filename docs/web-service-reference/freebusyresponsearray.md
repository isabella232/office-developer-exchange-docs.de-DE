---
title: FreeBusyResponseArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyResponseArray
api_type:
- schema
ms.assetid: 5592a37e-cf4b-4643-8a2a-fa58c40345b9
description: Das FreeBusyResponseArray-Element enthält Informationen zur Verfügbarkeit der angeforderten Benutzer und den Antwortstatus.
ms.openlocfilehash: cc6022c28213667c40dc00b5627ed88c4f78e2f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758542"
---
# <a name="freebusyresponsearray"></a><span data-ttu-id="acaff-103">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="acaff-103">FreeBusyResponseArray</span></span>

<span data-ttu-id="acaff-104">Das **FreeBusyResponseArray** -Element enthält Informationen zur Verfügbarkeit der angeforderten Benutzer und den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="acaff-104">The **FreeBusyResponseArray** element contains the requested users' availability information and the response status.</span></span> 
  
[<span data-ttu-id="acaff-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="acaff-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="acaff-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="acaff-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
```xml
<FreeBusyResponseArray>
   <FreeBusyResponse>...</FreeBusyResponse>
</FreeBusyResponseArray>
```

 <span data-ttu-id="acaff-107">**ArrayOfFreeBusyResponse**</span><span class="sxs-lookup"><span data-stu-id="acaff-107">**ArrayOfFreeBusyResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acaff-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="acaff-108">Attributes and elements</span></span>

<span data-ttu-id="acaff-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="acaff-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acaff-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="acaff-110">Attributes</span></span>

<span data-ttu-id="acaff-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="acaff-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acaff-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="acaff-112">Child elements</span></span>

|<span data-ttu-id="acaff-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="acaff-113">**Element**</span></span>|<span data-ttu-id="acaff-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="acaff-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acaff-115">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="acaff-115">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="acaff-116">Enthält die Frei/Gebucht-Informationen für ein einzelnes Postfach-Benutzer und den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="acaff-116">Contains the free/busy information for a single mailbox user and the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="acaff-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="acaff-117">Parent elements</span></span>

|<span data-ttu-id="acaff-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="acaff-118">**Element**</span></span>|<span data-ttu-id="acaff-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="acaff-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acaff-120">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="acaff-120">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="acaff-121">Enthält die Eigenschaften, die Verfügbarkeitsinformationen für Benutzer definieren oder Besprechungsinformationen Zeit vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="acaff-121">Contains the properties that define user availability information or suggested meeting time information.</span></span>  <br/> <span data-ttu-id="acaff-122">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="acaff-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acaff-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="acaff-123">Remarks</span></span>

<span data-ttu-id="acaff-124">Dieses Element ist nicht in einer Antwort GetUserAvailability enthalten, wenn Frei/Gebucht-Informationen nicht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="acaff-124">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="acaff-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="acaff-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acaff-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="acaff-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acaff-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="acaff-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="acaff-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="acaff-128">Schema Name</span></span>  <br/> |<span data-ttu-id="acaff-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="acaff-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="acaff-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="acaff-130">Validation File</span></span>  <br/> |<span data-ttu-id="acaff-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="acaff-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="acaff-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="acaff-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="acaff-133">False</span><span class="sxs-lookup"><span data-stu-id="acaff-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="acaff-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acaff-134">See also</span></span>



[<span data-ttu-id="acaff-135">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="acaff-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="acaff-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="acaff-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="acaff-137">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="acaff-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

