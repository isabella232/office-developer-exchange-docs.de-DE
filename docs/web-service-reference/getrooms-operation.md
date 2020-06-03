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
description: Der getrooms-Vorgang ruft die Räume in der angegebenen Raumliste ab.
ms.openlocfilehash: 4cb124b96637b9fcdca15595faebb2ce4d304de0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460547"
---
# <a name="getrooms-operation"></a><span data-ttu-id="8cd65-103">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8cd65-103">GetRooms operation</span></span>

<span data-ttu-id="8cd65-104">Der **getrooms** -Vorgang ruft die Räume in der angegebenen Raumliste ab.</span><span class="sxs-lookup"><span data-stu-id="8cd65-104">The **GetRooms** operation gets the rooms within the specified room list.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="8cd65-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="8cd65-105">SOAP Headers</span></span>

<span data-ttu-id="8cd65-106">Der **getrooms** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8cd65-106">The **GetRooms** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="8cd65-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="8cd65-107">**Header**</span></span>|<span data-ttu-id="8cd65-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cd65-108">**Element**</span></span>|<span data-ttu-id="8cd65-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cd65-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8cd65-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="8cd65-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="8cd65-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="8cd65-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="8cd65-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="8cd65-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="8cd65-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="8cd65-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="8cd65-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="8cd65-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="8cd65-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cd65-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="8cd65-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="8cd65-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="8cd65-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8cd65-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="8cd65-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="8cd65-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="8cd65-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="8cd65-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="8cd65-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8cd65-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="8cd65-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="8cd65-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getrooms-request-example"></a><span data-ttu-id="8cd65-122">Getrooms-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="8cd65-122">GetRooms request example</span></span>

### <a name="description"></a><span data-ttu-id="8cd65-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cd65-123">Description</span></span>

<span data-ttu-id="8cd65-124">Nachfolgend sehen Sie ein Beispiel für eine **getrooms** -Anforderung, die die Räume abruft, die einer Raumliste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8cd65-124">The following is an example of a **GetRooms** request that gets the rooms that are associated with a room list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8cd65-125">Code</span><span class="sxs-lookup"><span data-stu-id="8cd65-125">Code</span></span>

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
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>

```

### <a name="request-elements"></a><span data-ttu-id="8cd65-126">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="8cd65-126">Request elements</span></span>

<span data-ttu-id="8cd65-127">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="8cd65-127">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="8cd65-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8cd65-128">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="8cd65-129">GetRooms</span><span class="sxs-lookup"><span data-stu-id="8cd65-129">GetRooms</span></span>](getrooms.md)
    
- [<span data-ttu-id="8cd65-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="8cd65-130">RoomList</span></span>](roomlist.md)
    
- [<span data-ttu-id="8cd65-131">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="8cd65-131">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-getrooms-response-example"></a><span data-ttu-id="8cd65-132">Erfolgreiches getrooms-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="8cd65-132">Successful GetRooms response example</span></span>

### <a name="description"></a><span data-ttu-id="8cd65-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cd65-133">Description</span></span>

<span data-ttu-id="8cd65-134">Die folgende Antwort zeigt die e-Mail-Adressinformationen für die Räume, die der Raumliste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8cd65-134">The following response shows the email address information for the rooms that are associated with the room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="8cd65-135">Code</span><span class="sxs-lookup"><span data-stu-id="8cd65-135">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:Rooms xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Room xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room01</t:Name>
            <t:EmailAddress>Room01@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="successful-getrooms-response-elements"></a><span data-ttu-id="8cd65-136">Erfolgreiche getrooms-Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="8cd65-136">Successful GetRooms response elements</span></span>

<span data-ttu-id="8cd65-137">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="8cd65-137">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8cd65-138">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8cd65-138">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8cd65-139">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="8cd65-139">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="8cd65-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8cd65-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8cd65-141">Chatrooms</span><span class="sxs-lookup"><span data-stu-id="8cd65-141">Rooms</span></span>](rooms.md)
    
- [<span data-ttu-id="8cd65-142">Raum</span><span class="sxs-lookup"><span data-stu-id="8cd65-142">Room</span></span>](room.md)
    
- [<span data-ttu-id="8cd65-143">Name (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="8cd65-143">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="8cd65-144">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="8cd65-144">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="8cd65-145">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="8cd65-145">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="8cd65-146">MailboxType</span><span class="sxs-lookup"><span data-stu-id="8cd65-146">MailboxType</span></span>](mailboxtype.md)
    
## <a name="getrooms-error-response-example"></a><span data-ttu-id="8cd65-147">Getrooms-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="8cd65-147">GetRooms Error response example</span></span>

### <a name="description"></a><span data-ttu-id="8cd65-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cd65-148">Description</span></span>

<span data-ttu-id="8cd65-149">Das folgende Beispiel zeigt eine Fehlermeldung, die durch den Versuch verursacht wurde, Rauminformationen für eine nicht vorhandene Raumliste zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8cd65-149">The following example shows an error response caused by an attempt to get room information for a nonexistent room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="8cd65-150">Code</span><span class="sxs-lookup"><span data-stu-id="8cd65-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>No results were found.</MessageText>
      <ResponseCode>ErrorNameResolutionNoResults</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="getrooms-error-response-elements"></a><span data-ttu-id="8cd65-151">Getrooms-Fehlerantwort Elemente</span><span class="sxs-lookup"><span data-stu-id="8cd65-151">GetRooms Error response elements</span></span>

<span data-ttu-id="8cd65-152">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="8cd65-152">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8cd65-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8cd65-153">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8cd65-154">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="8cd65-154">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="8cd65-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="8cd65-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8cd65-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8cd65-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8cd65-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8cd65-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="8cd65-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cd65-158">See also</span></span>

- [<span data-ttu-id="8cd65-159">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="8cd65-159">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="8cd65-160">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8cd65-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

