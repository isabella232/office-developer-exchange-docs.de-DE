---
title: FreeBusyResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyResponse
api_type:
- schema
ms.assetid: 3038d106-9ac9-4ac7-bb43-96c783edbef5
description: Das FreeBusyResponse-Element enthält die Frei/Gebucht-Informationen für einen einzelnen Postfachbenutzer.
ms.openlocfilehash: 73e3972bb53d6bf59e5156098bad06bcde5f0155
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758539"
---
# <a name="freebusyresponse"></a><span data-ttu-id="9fe0f-103">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="9fe0f-103">FreeBusyResponse</span></span>

<span data-ttu-id="9fe0f-104">Das **FreeBusyResponse** -Element enthält die Frei/Gebucht-Informationen für einen einzelnen Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-104">The **FreeBusyResponse** element contains the free/busy information for a single mailbox user.</span></span> 
  
[<span data-ttu-id="9fe0f-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9fe0f-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="9fe0f-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="9fe0f-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="9fe0f-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="9fe0f-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
```xml
<FreeBusyResponse>
   <ResponseMessage>...</ResponseMessage>
   <FreeBusyView>...</FreeBusyView>
</FreeBusyResponse>
```

 <span data-ttu-id="9fe0f-108">**FreeBusyResponseType**</span><span class="sxs-lookup"><span data-stu-id="9fe0f-108">**FreeBusyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fe0f-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9fe0f-109">Attributes and elements</span></span>

<span data-ttu-id="9fe0f-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fe0f-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fe0f-111">Attributes</span></span>

<span data-ttu-id="9fe0f-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fe0f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fe0f-113">Child elements</span></span>

|<span data-ttu-id="9fe0f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fe0f-114">**Element**</span></span>|<span data-ttu-id="9fe0f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fe0f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fe0f-116">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9fe0f-116">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="9fe0f-117">Enthält beschreibende Informationen über den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-117">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="9fe0f-118">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="9fe0f-118">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="9fe0f-119">Enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-119">Contains availability information for a specific user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9fe0f-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fe0f-120">Parent elements</span></span>

|<span data-ttu-id="9fe0f-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fe0f-121">**Element**</span></span>|<span data-ttu-id="9fe0f-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fe0f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fe0f-123">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="9fe0f-123">FreeBusyResponseArray</span></span>](freebusyresponsearray.md) <br/> |<span data-ttu-id="9fe0f-124">Enthält Informationen zur Verfügbarkeit der angeforderten Benutzer und den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-124">Contains the requested users' availability information and the response status.</span></span>  <br/> <span data-ttu-id="9fe0f-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9fe0f-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fe0f-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fe0f-126">Remarks</span></span>

<span data-ttu-id="9fe0f-127">Dieses Element ist nicht in einer Antwort GetUserAvailability enthalten, wenn Frei/Gebucht-Informationen nicht angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-127">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="9fe0f-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9fe0f-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fe0f-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9fe0f-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fe0f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fe0f-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9fe0f-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9fe0f-131">Schema Name</span></span>  <br/> |<span data-ttu-id="9fe0f-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9fe0f-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9fe0f-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9fe0f-133">Validation File</span></span>  <br/> |<span data-ttu-id="9fe0f-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9fe0f-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9fe0f-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9fe0f-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fe0f-136">False</span><span class="sxs-lookup"><span data-stu-id="9fe0f-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fe0f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fe0f-137">See also</span></span>



[<span data-ttu-id="9fe0f-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9fe0f-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="9fe0f-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9fe0f-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="9fe0f-140">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="9fe0f-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

