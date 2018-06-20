---
title: GetUserOofSettings-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettings
api_type:
- schema
ms.assetid: 153e4440-495b-4972-9811-2fbea740142a
description: Der Vorgang GetUserOofSettings ruft eines Postfachbenutzers Einstellungen von Office (ABWESEND) und Nachrichten ab.
ms.openlocfilehash: 75a734999842cc33c213e02dc114f23372ae51fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829691"
---
# <a name="getuseroofsettings-operation"></a><span data-ttu-id="1be4f-103">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1be4f-103">GetUserOofSettings operation</span></span>

<span data-ttu-id="1be4f-104">Der Vorgang **GetUserOofSettings** ruft eines Postfachbenutzers Einstellungen von Office (ABWESEND) und Nachrichten ab.</span><span class="sxs-lookup"><span data-stu-id="1be4f-104">The **GetUserOofSettings** operation gets a mailbox user's Out of Office (OOF) settings and messages.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="1be4f-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="1be4f-105">SOAP Headers</span></span>

<span data-ttu-id="1be4f-106">Der Vorgang **GetUserOofSettings** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1be4f-106">The **GetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="1be4f-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="1be4f-107">**Header**</span></span>|<span data-ttu-id="1be4f-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="1be4f-108">**Element**</span></span>|<span data-ttu-id="1be4f-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1be4f-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1be4f-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="1be4f-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="1be4f-111">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="1be4f-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="1be4f-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="1be4f-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="1be4f-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="1be4f-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="1be4f-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1be4f-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="1be4f-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="1be4f-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="using-the-getuseroofsettings-operation"></a><span data-ttu-id="1be4f-116">Verwenden des GetUserOofSettings-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="1be4f-116">Using the GetUserOofSettings Operation</span></span>

<span data-ttu-id="1be4f-117">Der Vorgang **GetUserOofSettings** ermöglicht den Zugriff auf die OOF Einstellungen eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1be4f-117">The **GetUserOofSettings** operation provides access to a user's OOF settings.</span></span> <span data-ttu-id="1be4f-118">Ein Benutzer wird durch die e-Mail-Adresse des Benutzers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1be4f-118">A user is identified by the user's email address.</span></span> <span data-ttu-id="1be4f-119">Wenn die Abwesenheitsnachricht null ist und OOF aktiviert ist, wird keine Abwesenheitsnachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="1be4f-119">If the OOF message is null and OOF is enabled, no OOF message is sent.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1be4f-120">Wenn die OOF Nachrichten durch MicrosoftOfficeOutlook festgelegt werden, wird dieser Vorgang die OOF Nachrichten im HTML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="1be4f-120">If the OOF messages are set by MicrosoftOfficeOutlook, this operation will return the OOF messages in HTML format.</span></span> 
  
## <a name="getuseroofsettings-request-example"></a><span data-ttu-id="1be4f-121">Anforderungsbeispiel GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="1be4f-121">GetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="1be4f-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1be4f-122">Description</span></span>

<span data-ttu-id="1be4f-123">Das folgende Beispiel zeigt eine **GetUserOofSettings** -Anforderung, die Informationen für einen Einzelbenutzer OOF abruft.</span><span class="sxs-lookup"><span data-stu-id="1be4f-123">The following example shows a **GetUserOofSettings** request that gets a single user's OOF information.</span></span> 
  
### <a name="code"></a><span data-ttu-id="1be4f-124">Code</span><span class="sxs-lookup"><span data-stu-id="1be4f-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns ="http://schemas.microsoft.com/exchange/services/2006/types">
        <Address>User1@example.com</Address>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="1be4f-125">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="1be4f-125">Request elements</span></span>

<span data-ttu-id="1be4f-126">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1be4f-126">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="1be4f-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="1be4f-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
    
- [<span data-ttu-id="1be4f-128">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="1be4f-128">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="1be4f-129">Adresse (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="1be4f-129">Address (string)</span></span>](address-string.md)
    
## <a name="successful-getuseroofsettings-response-example"></a><span data-ttu-id="1be4f-130">Erfolgreiche GetUserOofSettings antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="1be4f-130">Successful GetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="1be4f-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1be4f-131">Description</span></span>

<span data-ttu-id="1be4f-132">Das folgende Beispiel zeigt OOF deaktiviert mit OOF-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1be4f-132">The following example shows a disabled OOF state with the OOF messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="1be4f-133">Code</span><span class="sxs-lookup"><span data-stu-id="1be4f-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserOofSettingsResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode>
      </ResponseMessage>
      <OofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Disabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-11-03T23:00:00</StartTime>
          <EndTime>2006-11-04T23:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office. This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </OofSettings>
      <AllowExternalOof>All</AllowExternalOof>
    </GetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-getuseroofsettings-response-elements"></a><span data-ttu-id="1be4f-134">Erfolgreiche GetUserOofSettings Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="1be4f-134">Successful GetUserOofSettings response elements</span></span>

<span data-ttu-id="1be4f-135">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1be4f-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="1be4f-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1be4f-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="1be4f-137">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="1be4f-137">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
    
- [<span data-ttu-id="1be4f-138">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1be4f-138">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="1be4f-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1be4f-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1be4f-140">OofSettings</span><span class="sxs-lookup"><span data-stu-id="1be4f-140">OofSettings</span></span>](oofsettings.md)
    
- [<span data-ttu-id="1be4f-141">OofState</span><span class="sxs-lookup"><span data-stu-id="1be4f-141">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="1be4f-142">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="1be4f-142">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="1be4f-143">Dauer (' UserOofSettings ')</span><span class="sxs-lookup"><span data-stu-id="1be4f-143">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="1be4f-144">StartTime</span><span class="sxs-lookup"><span data-stu-id="1be4f-144">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="1be4f-145">EndTime</span><span class="sxs-lookup"><span data-stu-id="1be4f-145">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="1be4f-146">InternalReply</span><span class="sxs-lookup"><span data-stu-id="1be4f-146">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="1be4f-147">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="1be4f-147">ExternalReply</span></span>](externalreply.md)
    
- [<span data-ttu-id="1be4f-148">Message</span><span class="sxs-lookup"><span data-stu-id="1be4f-148">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="1be4f-149">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="1be4f-149">AllowExternalOof</span></span>](allowexternaloof.md)
    
## <a name="getuseroofsettings-error-response-example"></a><span data-ttu-id="1be4f-150">Antwortbeispiel GetUserOofSettings-Fehler</span><span class="sxs-lookup"><span data-stu-id="1be4f-150">GetUserOofSettings Error response example</span></span>

### <a name="description"></a><span data-ttu-id="1be4f-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1be4f-151">Description</span></span>

<span data-ttu-id="1be4f-152">Das folgende Beispiel zeigt eine Fehlerantwort verursacht ein Versuch, einen anderen Benutzer OOF Informationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1be4f-152">The following example shows an error response caused by an attempt to access another user's OOF information.</span></span>
  
### <a name="code"></a><span data-ttu-id="1be4f-153">Code</span><span class="sxs-lookup"><span data-stu-id="1be4f-153">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <faultcode>soap:Client</faultcode>
      <faultstring>Microsoft.Exchange.Data.Storage.AccessDeniedException: User is not mailbox owner. User = S-1-5-21-3642464542-282065186-3871681729-1155, MailboxGuid = S-1-5-21-3642464542-282065186-3871681729-1156 ---> User is not mailbox owner. </faultstring>
      <faultactor>https://CAS01.example.com/EWS/Exchange.asmx</faultactor>
      <detail>
        <ErrorCode xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">-2146233088</ErrorCode>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="1be4f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1be4f-154">See also</span></span>



- [<span data-ttu-id="1be4f-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1be4f-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

