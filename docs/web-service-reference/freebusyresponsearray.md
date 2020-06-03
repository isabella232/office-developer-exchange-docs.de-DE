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
description: Das FreeBusyResponseArray-Element enthält die Verfügbarkeitsinformationen der angeforderten Benutzer und den Antwortstatus.
ms.openlocfilehash: b45938c19b76a377fca125fb6a19f9d712718db6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457809"
---
# <a name="freebusyresponsearray"></a><span data-ttu-id="034d0-103">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="034d0-103">FreeBusyResponseArray</span></span>

<span data-ttu-id="034d0-104">Das **FreeBusyResponseArray** -Element enthält die Verfügbarkeitsinformationen der angeforderten Benutzer und den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="034d0-104">The **FreeBusyResponseArray** element contains the requested users' availability information and the response status.</span></span> 
  
[<span data-ttu-id="034d0-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="034d0-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="034d0-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="034d0-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
```xml
<FreeBusyResponseArray>
   <FreeBusyResponse>...</FreeBusyResponse>
</FreeBusyResponseArray>
```

 <span data-ttu-id="034d0-107">**ArrayOfFreeBusyResponse**</span><span class="sxs-lookup"><span data-stu-id="034d0-107">**ArrayOfFreeBusyResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="034d0-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="034d0-108">Attributes and elements</span></span>

<span data-ttu-id="034d0-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="034d0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="034d0-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="034d0-110">Attributes</span></span>

<span data-ttu-id="034d0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="034d0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="034d0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="034d0-112">Child elements</span></span>

|<span data-ttu-id="034d0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="034d0-113">**Element**</span></span>|<span data-ttu-id="034d0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="034d0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="034d0-115">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="034d0-115">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="034d0-116">Enthält die Frei/Gebucht-Informationen für einen einzelnen Postfachbenutzer und den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="034d0-116">Contains the free/busy information for a single mailbox user and the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="034d0-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="034d0-117">Parent elements</span></span>

|<span data-ttu-id="034d0-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="034d0-118">**Element**</span></span>|<span data-ttu-id="034d0-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="034d0-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="034d0-120">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="034d0-120">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="034d0-121">Enthält die Eigenschaften, mit denen Benutzer Verfügbarkeitsinformationen oder vorgeschlagene Besprechungszeit Informationen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="034d0-121">Contains the properties that define user availability information or suggested meeting time information.</span></span>  <br/> <span data-ttu-id="034d0-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="034d0-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="034d0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="034d0-123">Remarks</span></span>

<span data-ttu-id="034d0-124">Dieses Element ist nicht in einer GetUserAvailability-Antwort enthalten, wenn keine Frei/Gebucht-Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="034d0-124">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="034d0-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="034d0-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="034d0-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="034d0-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="034d0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="034d0-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="034d0-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="034d0-128">Schema Name</span></span>  <br/> |<span data-ttu-id="034d0-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="034d0-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="034d0-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="034d0-130">Validation File</span></span>  <br/> |<span data-ttu-id="034d0-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="034d0-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="034d0-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="034d0-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="034d0-133">False</span><span class="sxs-lookup"><span data-stu-id="034d0-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="034d0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="034d0-134">See also</span></span>



[<span data-ttu-id="034d0-135">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="034d0-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="034d0-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="034d0-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="034d0-137">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="034d0-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

