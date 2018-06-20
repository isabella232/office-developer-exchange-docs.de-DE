---
title: RemoveDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegateResponse
api_type:
- schema
ms.assetid: eef56c53-d0a7-4342-9ce6-4dbb6b1a1369
description: Das RemoveDelegateResponse-Element enthält den Status und das Ergebnis einer RemoveDelegate Vorgang Anforderung.
ms.openlocfilehash: 45d0bcfaeb4d453f50cce8449f5cb7fdb70512a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831092"
---
# <a name="removedelegateresponse"></a><span data-ttu-id="76243-103">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="76243-103">RemoveDelegateResponse</span></span>

<span data-ttu-id="76243-104">Das **RemoveDelegateResponse** -Element enthält den Status und das Ergebnis einer Anforderung [RemoveDelegate Vorgang](removedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="76243-104">The **RemoveDelegateResponse** element contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span> 
  
```xml
<RemoveDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RemoveDelegateResponse>
```

 <span data-ttu-id="76243-105">**RemoveDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="76243-105">**RemoveDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76243-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="76243-106">Attributes and elements</span></span>

<span data-ttu-id="76243-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="76243-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76243-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="76243-108">Attributes</span></span>

<span data-ttu-id="76243-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="76243-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76243-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76243-110">Child elements</span></span>

|<span data-ttu-id="76243-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="76243-111">**Element**</span></span>|<span data-ttu-id="76243-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76243-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76243-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="76243-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="76243-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Delegaten Management-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="76243-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="76243-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="76243-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="76243-116">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="76243-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="76243-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="76243-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="76243-118">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="76243-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="76243-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="76243-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="76243-120">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="76243-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="76243-121">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="76243-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="76243-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="76243-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="76243-123">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="76243-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76243-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76243-124">Parent elements</span></span>

<span data-ttu-id="76243-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="76243-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76243-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76243-126">Remarks</span></span>

<span data-ttu-id="76243-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="76243-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76243-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="76243-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76243-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="76243-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76243-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="76243-130">Schema Name</span></span>  <br/> |<span data-ttu-id="76243-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="76243-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="76243-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="76243-132">Validation File</span></span>  <br/> |<span data-ttu-id="76243-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="76243-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76243-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="76243-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="76243-135">False</span><span class="sxs-lookup"><span data-stu-id="76243-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76243-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76243-136">See also</span></span>



[<span data-ttu-id="76243-137">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="76243-137">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="76243-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="76243-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

