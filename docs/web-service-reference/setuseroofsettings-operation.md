---
title: SetUserOofSettings-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettings
api_type:
- schema
ms.assetid: 36277ef0-18ee-4b35-9e6e-8c321d8f5433
description: Die SetUserOofSettings-Webmethode legt eines Postfachbenutzers Out of Office (OOF)-Einstellungen und Nachricht fest.
ms.openlocfilehash: 51c2f9488f38a4adb0e291c11adc2ebfe3426f25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831469"
---
# <a name="setuseroofsettings-operation"></a><span data-ttu-id="1c1c5-103">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1c1c5-103">SetUserOofSettings operation</span></span>

<span data-ttu-id="1c1c5-104">Die **SetUserOofSettings** -Webmethode legt eines Postfachbenutzers Out of Office (OOF)-Einstellungen und Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="1c1c5-104">The **SetUserOofSettings** Web method sets a mailbox user's Out of Office (OOF) settings and message.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="1c1c5-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="1c1c5-105">SOAP Headers</span></span>

<span data-ttu-id="1c1c5-106">Der Vorgang **SetUserOofSettings** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1c1c5-106">The **SetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="1c1c5-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="1c1c5-107">**Header**</span></span>|<span data-ttu-id="1c1c5-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c1c5-108">**Element**</span></span>|<span data-ttu-id="1c1c5-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c1c5-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c1c5-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="1c1c5-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="1c1c5-111">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="1c1c5-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="1c1c5-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="1c1c5-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="1c1c5-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="1c1c5-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="1c1c5-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1c1c5-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="1c1c5-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="1c1c5-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="setuseroofsettings-request-example"></a><span data-ttu-id="1c1c5-116">Anforderungsbeispiel SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="1c1c5-116">SetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="1c1c5-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c1c5-117">Description</span></span>

<span data-ttu-id="1c1c5-118">Im folgenden Beispiel wird eine Anforderung **SetUserOofSettings** legt eine OOF-Einstellung für 10 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="1c1c5-118">The following example of a **SetUserOofSettings** request sets an OOF setting for 10 days.</span></span> 
  
### <a name="code"></a><span data-ttu-id="1c1c5-119">Code</span><span class="sxs-lookup"><span data-stu-id="1c1c5-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>User1</Name>
        <Address>user1@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-10-05T00:00:00</StartTime>
          <EndTime>2006-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="1c1c5-120">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="1c1c5-120">Request elements</span></span>

<span data-ttu-id="1c1c5-121">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1c1c5-121">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="1c1c5-122">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="1c1c5-122">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
    
- [<span data-ttu-id="1c1c5-123">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="1c1c5-123">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="1c1c5-124">Name (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="1c1c5-124">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="1c1c5-125">Adresse (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="1c1c5-125">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="1c1c5-126">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="1c1c5-126">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="1c1c5-127">' UserOofSettings '</span><span class="sxs-lookup"><span data-stu-id="1c1c5-127">UserOofSettings</span></span>](useroofsettings.md)
    
- [<span data-ttu-id="1c1c5-128">OofState</span><span class="sxs-lookup"><span data-stu-id="1c1c5-128">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="1c1c5-129">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="1c1c5-129">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="1c1c5-130">Dauer (' UserOofSettings ')</span><span class="sxs-lookup"><span data-stu-id="1c1c5-130">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="1c1c5-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="1c1c5-131">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="1c1c5-132">EndTime</span><span class="sxs-lookup"><span data-stu-id="1c1c5-132">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="1c1c5-133">InternalReply</span><span class="sxs-lookup"><span data-stu-id="1c1c5-133">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="1c1c5-134">Nachricht (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="1c1c5-134">Message (Availability)</span></span>](message-availability.md)
    
- [<span data-ttu-id="1c1c5-135">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="1c1c5-135">ExternalReply</span></span>](externalreply.md)
    
## <a name="successful-setuseroofsettings-response-example"></a><span data-ttu-id="1c1c5-136">Erfolgreiche SetUserOofSettings antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="1c1c5-136">Successful SetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="1c1c5-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c1c5-137">Description</span></span>

<span data-ttu-id="1c1c5-138">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **SetUserOofSettings** .</span><span class="sxs-lookup"><span data-stu-id="1c1c5-138">The following example shows a successful response to the **SetUserOofSettings** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="1c1c5-139">Code</span><span class="sxs-lookup"><span data-stu-id="1c1c5-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" /> 
  </soap:Header>
  <soap:Body>
    <SetUserOofSettingsResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode> 
      </ResponseMessage>
    </SetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="1c1c5-140">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="1c1c5-140">Successful response elements</span></span>

<span data-ttu-id="1c1c5-141">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1c1c5-141">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="1c1c5-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1c1c5-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="1c1c5-143">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="1c1c5-143">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md)
    
- [<span data-ttu-id="1c1c5-144">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1c1c5-144">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="1c1c5-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1c1c5-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="1c1c5-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c1c5-146">See also</span></span>



- [<span data-ttu-id="1c1c5-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1c1c5-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

