---
title: GetDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegateResponse
api_type:
- schema
ms.assetid: 71a418a5-5652-40e1-8f84-fe4f7c9f86af
description: Das GetDelegateResponse-Element enthält den Status und das Ergebnis einer GetDelegate Vorgang Anforderung.
ms.openlocfilehash: 52731ea66420c21cf3fb8d19082aef65551c2af2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758628"
---
# <a name="getdelegateresponse"></a><span data-ttu-id="d5d65-103">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="d5d65-103">GetDelegateResponse</span></span>

<span data-ttu-id="d5d65-104">Das **GetDelegateResponse** -Element enthält den Status und das Ergebnis einer Anforderung [GetDelegate Vorgang](getdelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d5d65-104">The **GetDelegateResponse** element contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span> 
  
```xml
<GetDelegateResponse>
   <DeliverMeetingRequests/>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</GetDelegateResponse>
```

 <span data-ttu-id="d5d65-105">**GetDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d5d65-105">**GetDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5d65-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5d65-106">Attributes and elements</span></span>

<span data-ttu-id="d5d65-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5d65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5d65-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5d65-108">Attributes</span></span>

<span data-ttu-id="d5d65-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5d65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5d65-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5d65-110">Child elements</span></span>

|<span data-ttu-id="d5d65-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5d65-111">**Element**</span></span>|<span data-ttu-id="d5d65-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5d65-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5d65-113">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="d5d65-113">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="d5d65-114">Definiert, wie Besprechungsanfragen zwischen den Delegaten und dem Prinzipalnamen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d5d65-114">Defines how meeting requests are handled between the delegate and the principal.</span></span>  <br/> |
|[<span data-ttu-id="d5d65-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="d5d65-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="d5d65-116">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Delegaten Management-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d5d65-116">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="d5d65-117">MessageText</span><span class="sxs-lookup"><span data-stu-id="d5d65-117">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d5d65-118">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d5d65-118">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d5d65-119">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d5d65-119">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d5d65-120">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="d5d65-120">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d5d65-121">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d5d65-121">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d5d65-122">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d5d65-122">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="d5d65-123">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="d5d65-123">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d5d65-124">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d5d65-124">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d5d65-125">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d5d65-125">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5d65-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5d65-126">Parent elements</span></span>

<span data-ttu-id="d5d65-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5d65-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5d65-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5d65-128">Remarks</span></span>

<span data-ttu-id="d5d65-129">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d5d65-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5d65-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d5d65-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5d65-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5d65-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5d65-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d5d65-132">Schema Name</span></span>  <br/> |<span data-ttu-id="d5d65-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d5d65-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d5d65-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d5d65-134">Validation File</span></span>  <br/> |<span data-ttu-id="d5d65-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d5d65-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5d65-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d5d65-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5d65-137">False</span><span class="sxs-lookup"><span data-stu-id="d5d65-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5d65-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5d65-138">See also</span></span>



[<span data-ttu-id="d5d65-139">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5d65-139">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="d5d65-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d5d65-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

