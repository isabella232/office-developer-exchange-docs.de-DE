---
title: GetRoomLists-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomLists
api_type:
- schema
ms.assetid: 55d451f9-547f-44ac-872e-9cb220ea7b7c
description: Mit dem GetRoomLists-Vorgang werden die Raumlisten abgerufen, die in der Exchange-Organisation zur Verfügung stehen.
ms.openlocfilehash: d1393a6a5e99b7e0a7e354d2b7dd035d04356ec2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458278"
---
# <a name="getroomlists-operation"></a><span data-ttu-id="18a24-103">GetRoomLists-Vorgang</span><span class="sxs-lookup"><span data-stu-id="18a24-103">GetRoomLists operation</span></span>

<span data-ttu-id="18a24-104">Mit dem **GetRoomLists** -Vorgang werden die Raumlisten abgerufen, die in der Exchange-Organisation zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="18a24-104">The **GetRoomLists** operation gets the room lists that are available within the Exchange organization.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="18a24-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="18a24-105">SOAP Headers</span></span>

<span data-ttu-id="18a24-106">Der **GetRoomLists** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="18a24-106">The **GetRoomLists** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="18a24-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="18a24-107">**Header**</span></span>|<span data-ttu-id="18a24-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="18a24-108">**Element**</span></span>|<span data-ttu-id="18a24-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18a24-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18a24-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="18a24-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="18a24-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="18a24-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="18a24-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="18a24-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="18a24-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="18a24-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="18a24-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="18a24-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="18a24-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18a24-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="18a24-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="18a24-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="18a24-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="18a24-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="18a24-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="18a24-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="18a24-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="18a24-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="18a24-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="18a24-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="18a24-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="18a24-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getroomlists-request-example"></a><span data-ttu-id="18a24-122">GetRoomLists-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="18a24-122">GetRoomLists request example</span></span>

### <a name="description"></a><span data-ttu-id="18a24-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18a24-123">Description</span></span>

<span data-ttu-id="18a24-124">Im folgenden finden Sie ein Beispiel für eine **GetRoomLists** -Anforderung, die die auf dem Server verfügbaren Raumlisten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="18a24-124">The following is an example of a **GetRoomLists** request that returns the room lists that are available on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="18a24-125">Code</span><span class="sxs-lookup"><span data-stu-id="18a24-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="18a24-126">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="18a24-126">Request elements</span></span>

<span data-ttu-id="18a24-127">Das folgende Element wird in der Anforderung verwendet:</span><span class="sxs-lookup"><span data-stu-id="18a24-127">The following element is used in the request:</span></span>
  
- [<span data-ttu-id="18a24-128">GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="18a24-128">GetRoomLists</span></span>](getroomlists.md)
    
## <a name="successful-getroomlists-response-example"></a><span data-ttu-id="18a24-129">Erfolgreiches GetRoomLists-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="18a24-129">Successful GetRoomLists response example</span></span>

### <a name="description"></a><span data-ttu-id="18a24-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18a24-130">Description</span></span>

<span data-ttu-id="18a24-131">Im folgenden finden Sie ein Beispiel für eine Antwort auf eine **GetRoomLists** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="18a24-131">The following is an example of a response to a **GetRoomLists** request.</span></span> <span data-ttu-id="18a24-132">Diese Antwort zeigt eine Raumliste auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="18a24-132">This response shows one room list on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="18a24-133">Code</span><span class="sxs-lookup"><span data-stu-id="18a24-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Address xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Name>Room List</t:Name>
          <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-getroomlists-response-elements"></a><span data-ttu-id="18a24-134">Erfolgreiche GetRoomLists-Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="18a24-134">Successful GetRoomLists response elements</span></span>

<span data-ttu-id="18a24-135">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="18a24-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="18a24-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="18a24-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="18a24-137">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="18a24-137">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="18a24-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="18a24-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="18a24-139">RoomLists</span><span class="sxs-lookup"><span data-stu-id="18a24-139">RoomLists</span></span>](roomlists.md)
    
- [<span data-ttu-id="18a24-140">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="18a24-140">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="18a24-141">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="18a24-141">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="18a24-142">MailboxType</span><span class="sxs-lookup"><span data-stu-id="18a24-142">MailboxType</span></span>](mailboxtype.md)
    
### <a name="getroomlists-error-response-example"></a><span data-ttu-id="18a24-143">GetRoomLists-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="18a24-143">GetRoomLists Error response example</span></span>

#### <a name="description"></a><span data-ttu-id="18a24-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18a24-144">Description</span></span>

<span data-ttu-id="18a24-145">Das folgende Beispiel zeigt die Antwort auf einen Versuch, Raumlisten von einem Server zu erhalten, auf dem keine Raumlisten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="18a24-145">The following example shows the response to an attempt to get room lists from a server that does not have any room lists defined.</span></span>
  
#### <a name="code"></a><span data-ttu-id="18a24-146">Code</span><span class="sxs-lookup"><span data-stu-id="18a24-146">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"/>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

#### <a name="getroomlists-error-response-elements"></a><span data-ttu-id="18a24-147">GetRoomLists-Fehlerantwort Elemente</span><span class="sxs-lookup"><span data-stu-id="18a24-147">GetRoomLists Error response elements</span></span>

<span data-ttu-id="18a24-148">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="18a24-148">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="18a24-149">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="18a24-149">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="18a24-150">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="18a24-150">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="18a24-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="18a24-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="18a24-152">RoomLists</span><span class="sxs-lookup"><span data-stu-id="18a24-152">RoomLists</span></span>](roomlists.md)
    
## <a name="see-also"></a><span data-ttu-id="18a24-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18a24-153">See also</span></span>



[<span data-ttu-id="18a24-154">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="18a24-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="18a24-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="18a24-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

