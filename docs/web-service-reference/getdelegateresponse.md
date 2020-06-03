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
description: Das GetDelegateResponse-Element enthält den Status und das Ergebnis einer getdelegate-Vorgangsanforderung.
ms.openlocfilehash: 81c5033cd67b79baa131d71ea0b866c788ae5e82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462024"
---
# <a name="getdelegateresponse"></a><span data-ttu-id="73685-103">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="73685-103">GetDelegateResponse</span></span>

<span data-ttu-id="73685-104">Das **GetDelegateResponse** -Element enthält den Status und das Ergebnis einer [getdelegate-Vorgangs](getdelegate-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="73685-104">The **GetDelegateResponse** element contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="73685-105">**GetDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="73685-105">**GetDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73685-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73685-106">Attributes and elements</span></span>

<span data-ttu-id="73685-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="73685-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73685-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="73685-108">Attributes</span></span>

<span data-ttu-id="73685-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="73685-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73685-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73685-110">Child elements</span></span>

|<span data-ttu-id="73685-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="73685-111">**Element**</span></span>|<span data-ttu-id="73685-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73685-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73685-113">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="73685-113">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="73685-114">Definiert, wie Besprechungsanfragen zwischen der Stellvertretung und dem Prinzipal verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="73685-114">Defines how meeting requests are handled between the delegate and the principal.</span></span>  <br/> |
|[<span data-ttu-id="73685-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="73685-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="73685-116">Enthält die Antwortnachrichten für eine Verwaltungsanforderung für Exchange Webdienste Delegate.</span><span class="sxs-lookup"><span data-stu-id="73685-116">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="73685-117">MessageText</span><span class="sxs-lookup"><span data-stu-id="73685-117">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="73685-118">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="73685-118">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="73685-119">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="73685-119">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="73685-120">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="73685-120">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="73685-121">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="73685-121">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="73685-122">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="73685-122">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="73685-123">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="73685-123">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="73685-124">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="73685-124">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="73685-125">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="73685-125">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73685-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73685-126">Parent elements</span></span>

<span data-ttu-id="73685-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="73685-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73685-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73685-128">Remarks</span></span>

<span data-ttu-id="73685-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="73685-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73685-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="73685-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73685-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="73685-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="73685-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="73685-132">Schema Name</span></span>  <br/> |<span data-ttu-id="73685-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="73685-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="73685-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="73685-134">Validation File</span></span>  <br/> |<span data-ttu-id="73685-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="73685-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="73685-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="73685-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="73685-137">False</span><span class="sxs-lookup"><span data-stu-id="73685-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73685-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73685-138">See also</span></span>



[<span data-ttu-id="73685-139">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="73685-139">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="73685-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="73685-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

