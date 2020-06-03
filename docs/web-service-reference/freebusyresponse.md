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
ms.openlocfilehash: 45a3e12756f3cbf29b76b442f7103abc5fb9a833
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461926"
---
# <a name="freebusyresponse"></a><span data-ttu-id="98f20-103">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="98f20-103">FreeBusyResponse</span></span>

<span data-ttu-id="98f20-104">Das **FreeBusyResponse** -Element enthält die Frei/Gebucht-Informationen für einen einzelnen Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="98f20-104">The **FreeBusyResponse** element contains the free/busy information for a single mailbox user.</span></span> 
  
[<span data-ttu-id="98f20-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="98f20-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="98f20-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="98f20-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="98f20-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="98f20-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
```xml
<FreeBusyResponse>
   <ResponseMessage>...</ResponseMessage>
   <FreeBusyView>...</FreeBusyView>
</FreeBusyResponse>
```

 <span data-ttu-id="98f20-108">**FreeBusyResponseType**</span><span class="sxs-lookup"><span data-stu-id="98f20-108">**FreeBusyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98f20-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="98f20-109">Attributes and elements</span></span>

<span data-ttu-id="98f20-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="98f20-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98f20-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="98f20-111">Attributes</span></span>

<span data-ttu-id="98f20-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="98f20-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98f20-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="98f20-113">Child elements</span></span>

|<span data-ttu-id="98f20-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="98f20-114">**Element**</span></span>|<span data-ttu-id="98f20-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98f20-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98f20-116">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="98f20-116">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="98f20-117">Enthält beschreibende Informationen zum Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="98f20-117">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="98f20-118">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="98f20-118">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="98f20-119">Enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="98f20-119">Contains availability information for a specific user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="98f20-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="98f20-120">Parent elements</span></span>

|<span data-ttu-id="98f20-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="98f20-121">**Element**</span></span>|<span data-ttu-id="98f20-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98f20-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98f20-123">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="98f20-123">FreeBusyResponseArray</span></span>](freebusyresponsearray.md) <br/> |<span data-ttu-id="98f20-124">Enthält die Verfügbarkeitsinformationen der angeforderten Benutzer und den Antwortstatus.</span><span class="sxs-lookup"><span data-stu-id="98f20-124">Contains the requested users' availability information and the response status.</span></span>  <br/> <span data-ttu-id="98f20-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="98f20-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98f20-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98f20-126">Remarks</span></span>

<span data-ttu-id="98f20-127">Dieses Element ist nicht in einer GetUserAvailability-Antwort enthalten, wenn keine Frei/Gebucht-Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="98f20-127">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="98f20-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="98f20-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98f20-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="98f20-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98f20-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="98f20-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="98f20-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="98f20-131">Schema Name</span></span>  <br/> |<span data-ttu-id="98f20-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="98f20-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="98f20-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="98f20-133">Validation File</span></span>  <br/> |<span data-ttu-id="98f20-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="98f20-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="98f20-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="98f20-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="98f20-136">False</span><span class="sxs-lookup"><span data-stu-id="98f20-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98f20-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98f20-137">See also</span></span>



[<span data-ttu-id="98f20-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="98f20-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="98f20-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="98f20-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="98f20-140">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="98f20-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

