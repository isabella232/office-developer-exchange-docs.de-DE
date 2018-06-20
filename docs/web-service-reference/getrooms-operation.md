---
title: GetRooms-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 5501ddc0-3bfa-4da6-8e15-4223ca5499a3
description: Der Vorgang GetRooms Ruft die Räume innerhalb der angegebenen Raumliste ab.
ms.openlocfilehash: 3718c476881ae8aa538646464e7c61845d849562
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758792"
---
# <a name="getrooms-operation"></a><span data-ttu-id="bbcbb-103">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bbcbb-103">GetRooms operation</span></span>

<span data-ttu-id="bbcbb-104">Der Vorgang **GetRooms** Ruft die Räume innerhalb der angegebenen Raumliste ab.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-104">The **GetRooms** operation gets the rooms within the specified room list.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="bbcbb-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="bbcbb-105">SOAP Headers</span></span>

<span data-ttu-id="bbcbb-106">Der Vorgang **GetRooms** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-106">The **GetRooms** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="bbcbb-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="bbcbb-107">**Header**</span></span>|<span data-ttu-id="bbcbb-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="bbcbb-108">**Element**</span></span>|<span data-ttu-id="bbcbb-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bbcbb-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bbcbb-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="bbcbb-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="bbcbb-111">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="bbcbb-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="bbcbb-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="bbcbb-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="bbcbb-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="bbcbb-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="bbcbb-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="bbcbb-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="bbcbb-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="bbcbb-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="bbcbb-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="bbcbb-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="bbcbb-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="bbcbb-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="bbcbb-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="bbcbb-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bbcbb-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="bbcbb-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getrooms-request-example"></a><span data-ttu-id="bbcbb-122">Anforderungsbeispiel GetRooms</span><span class="sxs-lookup"><span data-stu-id="bbcbb-122">GetRooms request example</span></span>

### <a name="description"></a><span data-ttu-id="bbcbb-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbcbb-123">Description</span></span>

<span data-ttu-id="bbcbb-124">Es folgt ein Beispiel für eine **GetRooms** -Anforderung, die die Räume versehen werden, die eine Raumliste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-124">The following is an example of a **GetRooms** request that gets the rooms that are associated with a room list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bbcbb-125">Code</span><span class="sxs-lookup"><span data-stu-id="bbcbb-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>

```

### <a name="request-elements"></a><span data-ttu-id="bbcbb-126">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="bbcbb-126">Request elements</span></span>

<span data-ttu-id="bbcbb-127">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="bbcbb-127">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="bbcbb-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="bbcbb-128">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="bbcbb-129">GetRooms</span><span class="sxs-lookup"><span data-stu-id="bbcbb-129">GetRooms</span></span>](getrooms.md)
    
- [<span data-ttu-id="bbcbb-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="bbcbb-130">RoomList</span></span>](roomlist.md)
    
- [<span data-ttu-id="bbcbb-131">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="bbcbb-131">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-getrooms-response-example"></a><span data-ttu-id="bbcbb-132">Erfolgreiche GetRooms antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="bbcbb-132">Successful GetRooms response example</span></span>

### <a name="description"></a><span data-ttu-id="bbcbb-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbcbb-133">Description</span></span>

<span data-ttu-id="bbcbb-134">Die folgende Antwort zeigt die e-Mail-Adressinformationen für die Chatrooms, die die Raumliste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-134">The following response shows the email address information for the rooms that are associated with the room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="bbcbb-135">Code</span><span class="sxs-lookup"><span data-stu-id="bbcbb-135">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:Rooms xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Room xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room01</t:Name>
            <t:EmailAddress>Room01@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room02</t:Name>
            <t:EmailAddress>Room02@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
      </m:Rooms>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="successful-getrooms-response-elements"></a><span data-ttu-id="bbcbb-136">Erfolgreiche GetRooms Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="bbcbb-136">Successful GetRooms response elements</span></span>

<span data-ttu-id="bbcbb-137">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="bbcbb-137">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="bbcbb-138">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bbcbb-138">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bbcbb-139">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="bbcbb-139">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="bbcbb-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bbcbb-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bbcbb-141">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="bbcbb-141">Rooms</span></span>](rooms.md)
    
- [<span data-ttu-id="bbcbb-142">Raum</span><span class="sxs-lookup"><span data-stu-id="bbcbb-142">Room</span></span>](room.md)
    
- [<span data-ttu-id="bbcbb-143">Name (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="bbcbb-143">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="bbcbb-144">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="bbcbb-144">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="bbcbb-145">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="bbcbb-145">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="bbcbb-146">MailboxType</span><span class="sxs-lookup"><span data-stu-id="bbcbb-146">MailboxType</span></span>](mailboxtype.md)
    
## <a name="getrooms-error-response-example"></a><span data-ttu-id="bbcbb-147">Antwortbeispiel GetRooms-Fehler</span><span class="sxs-lookup"><span data-stu-id="bbcbb-147">GetRooms Error response example</span></span>

### <a name="description"></a><span data-ttu-id="bbcbb-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbcbb-148">Description</span></span>

<span data-ttu-id="bbcbb-149">Das folgende Beispiel zeigt eine Fehlerantwort durch den Versuch zum Abrufen von Informationen für eine nicht vorhandene Raumliste Raum verursacht.</span><span class="sxs-lookup"><span data-stu-id="bbcbb-149">The following example shows an error response caused by an attempt to get room information for a nonexistent room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="bbcbb-150">Code</span><span class="sxs-lookup"><span data-stu-id="bbcbb-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>No results were found.</MessageText>
      <ResponseCode>ErrorNameResolutionNoResults</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="getrooms-error-response-elements"></a><span data-ttu-id="bbcbb-151">Antwortelemente GetRooms Fehler</span><span class="sxs-lookup"><span data-stu-id="bbcbb-151">GetRooms Error response elements</span></span>

<span data-ttu-id="bbcbb-152">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="bbcbb-152">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="bbcbb-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bbcbb-153">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bbcbb-154">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="bbcbb-154">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="bbcbb-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="bbcbb-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="bbcbb-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bbcbb-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bbcbb-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bbcbb-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="bbcbb-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbcbb-158">See also</span></span>

- [<span data-ttu-id="bbcbb-159">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="bbcbb-159">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="bbcbb-160">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bbcbb-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

