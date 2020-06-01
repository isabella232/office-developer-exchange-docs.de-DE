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
description: Die SetUserOofSettings-Webmethode legt die Abwesenheit (Out of Office, OOF) Einstellungen und die Nachricht eines Postfachbenutzers fest.
ms.openlocfilehash: 88b5475dd2f0fe6d334bad51a0fe8d0beb767634
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463153"
---
# <a name="setuseroofsettings-operation"></a><span data-ttu-id="29835-103">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="29835-103">SetUserOofSettings operation</span></span>

<span data-ttu-id="29835-104">Die **SetUserOofSettings** -Webmethode legt die Abwesenheit (Out of Office, OOF) Einstellungen und die Nachricht eines Postfachbenutzers fest.</span><span class="sxs-lookup"><span data-stu-id="29835-104">The **SetUserOofSettings** Web method sets a mailbox user's Out of Office (OOF) settings and message.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="29835-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="29835-105">SOAP Headers</span></span>

<span data-ttu-id="29835-106">Der **SetUserOofSettings** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="29835-106">The **SetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="29835-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="29835-107">**Header**</span></span>|<span data-ttu-id="29835-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="29835-108">**Element**</span></span>|<span data-ttu-id="29835-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29835-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="29835-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="29835-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="29835-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="29835-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="29835-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="29835-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="29835-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="29835-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="29835-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="29835-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="29835-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="29835-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="setuseroofsettings-request-example"></a><span data-ttu-id="29835-116">SetUserOofSettings-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="29835-116">SetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="29835-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29835-117">Description</span></span>

<span data-ttu-id="29835-118">Im folgenden Beispiel einer **SetUserOofSettings** -Anforderung wird eine Abwesenheitseinstellung für 10 Tage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29835-118">The following example of a **SetUserOofSettings** request sets an OOF setting for 10 days.</span></span> 
  
### <a name="code"></a><span data-ttu-id="29835-119">Code</span><span class="sxs-lookup"><span data-stu-id="29835-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>User1</Name>
        <Address>user1@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="request-elements"></a><span data-ttu-id="29835-120">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="29835-120">Request elements</span></span>

<span data-ttu-id="29835-121">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="29835-121">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="29835-122">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="29835-122">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
    
- [<span data-ttu-id="29835-123">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="29835-123">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="29835-124">Name (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="29835-124">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="29835-125">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="29835-125">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="29835-126">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="29835-126">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="29835-127">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="29835-127">UserOofSettings</span></span>](useroofsettings.md)
    
- [<span data-ttu-id="29835-128">OofState</span><span class="sxs-lookup"><span data-stu-id="29835-128">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="29835-129">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="29835-129">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="29835-130">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="29835-130">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="29835-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="29835-131">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="29835-132">EndTime</span><span class="sxs-lookup"><span data-stu-id="29835-132">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="29835-133">InternalReply</span><span class="sxs-lookup"><span data-stu-id="29835-133">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="29835-134">Message (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="29835-134">Message (Availability)</span></span>](message-availability.md)
    
- [<span data-ttu-id="29835-135">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="29835-135">ExternalReply</span></span>](externalreply.md)
    
## <a name="successful-setuseroofsettings-response-example"></a><span data-ttu-id="29835-136">Erfolgreiches SetUserOofSettings-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="29835-136">Successful SetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="29835-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29835-137">Description</span></span>

<span data-ttu-id="29835-138">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **SetUserOofSettings** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="29835-138">The following example shows a successful response to the **SetUserOofSettings** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="29835-139">Code</span><span class="sxs-lookup"><span data-stu-id="29835-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" /> 
  </soap:Header>
  <soap:Body>
    <SetUserOofSettingsResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode> 
      </ResponseMessage>
    </SetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="29835-140">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="29835-140">Successful response elements</span></span>

<span data-ttu-id="29835-141">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="29835-141">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="29835-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="29835-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="29835-143">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="29835-143">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md)
    
- [<span data-ttu-id="29835-144">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="29835-144">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="29835-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="29835-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="29835-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29835-146">See also</span></span>



- [<span data-ttu-id="29835-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="29835-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

