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
description: Der GetUserOofSettings-Vorgang ruft die Abwesenheit (Out of Office, OOF) Einstellungen und Nachrichten eines Postfachbenutzers ab.
ms.openlocfilehash: 622faa622b0ea231a6331ff62631885d4252c1f5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457697"
---
# <a name="getuseroofsettings-operation"></a><span data-ttu-id="a9b84-103">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a9b84-103">GetUserOofSettings operation</span></span>

<span data-ttu-id="a9b84-104">Der **GetUserOofSettings** -Vorgang ruft die Abwesenheit (Out of Office, OOF) Einstellungen und Nachrichten eines Postfachbenutzers ab.</span><span class="sxs-lookup"><span data-stu-id="a9b84-104">The **GetUserOofSettings** operation gets a mailbox user's Out of Office (OOF) settings and messages.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="a9b84-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="a9b84-105">SOAP Headers</span></span>

<span data-ttu-id="a9b84-106">Der **GetUserOofSettings** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a9b84-106">The **GetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="a9b84-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="a9b84-107">**Header**</span></span>|<span data-ttu-id="a9b84-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9b84-108">**Element**</span></span>|<span data-ttu-id="a9b84-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9b84-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a9b84-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="a9b84-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="a9b84-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="a9b84-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="a9b84-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="a9b84-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="a9b84-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="a9b84-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="a9b84-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a9b84-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a9b84-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="a9b84-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="using-the-getuseroofsettings-operation"></a><span data-ttu-id="a9b84-116">Verwenden des GetUserOofSettings-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="a9b84-116">Using the GetUserOofSettings Operation</span></span>

<span data-ttu-id="a9b84-117">Der **GetUserOofSettings** -Vorgang ermöglicht den Zugriff auf die Abwesenheitseinstellungen eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a9b84-117">The **GetUserOofSettings** operation provides access to a user's OOF settings.</span></span> <span data-ttu-id="a9b84-118">Ein Benutzer wird durch die e-Mail-Adresse des Benutzers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a9b84-118">A user is identified by the user's email address.</span></span> <span data-ttu-id="a9b84-119">Wenn die Abwesenheitsnachricht NULL ist und OOF aktiviert ist, wird keine Abwesenheitsnachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="a9b84-119">If the OOF message is null and OOF is enabled, no OOF message is sent.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a9b84-120">Wenn die Abwesenheitsnachrichten von MicrosoftOfficeOutlook festgelegt werden, werden durch diesen Vorgang die Abwesenheitsnachrichten im HTML-Format zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9b84-120">If the OOF messages are set by MicrosoftOfficeOutlook, this operation will return the OOF messages in HTML format.</span></span> 
  
## <a name="getuseroofsettings-request-example"></a><span data-ttu-id="a9b84-121">GetUserOofSettings-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9b84-121">GetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="a9b84-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9b84-122">Description</span></span>

<span data-ttu-id="a9b84-123">Das folgende Beispiel zeigt eine **GetUserOofSettings** -Anforderung, die die Abwesenheitsinformationen eines einzelnen Benutzers abruft.</span><span class="sxs-lookup"><span data-stu-id="a9b84-123">The following example shows a **GetUserOofSettings** request that gets a single user's OOF information.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9b84-124">Code</span><span class="sxs-lookup"><span data-stu-id="a9b84-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns ="https://schemas.microsoft.com/exchange/services/2006/types">
        <Address>User1@example.com</Address>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="a9b84-125">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="a9b84-125">Request elements</span></span>

<span data-ttu-id="a9b84-126">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="a9b84-126">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a9b84-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="a9b84-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
    
- [<span data-ttu-id="a9b84-128">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="a9b84-128">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="a9b84-129">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="a9b84-129">Address (string)</span></span>](address-string.md)
    
## <a name="successful-getuseroofsettings-response-example"></a><span data-ttu-id="a9b84-130">Erfolgreiches GetUserOofSettings-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="a9b84-130">Successful GetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="a9b84-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9b84-131">Description</span></span>

<span data-ttu-id="a9b84-132">Das folgende Beispiel zeigt einen deaktivierten OOF-Zustand mit den OOF-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="a9b84-132">The following example shows a disabled OOF state with the OOF messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="a9b84-133">Code</span><span class="sxs-lookup"><span data-stu-id="a9b84-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserOofSettingsResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode>
      </ResponseMessage>
      <OofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="successful-getuseroofsettings-response-elements"></a><span data-ttu-id="a9b84-134">Erfolgreiche GetUserOofSettings-Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="a9b84-134">Successful GetUserOofSettings response elements</span></span>

<span data-ttu-id="a9b84-135">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="a9b84-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a9b84-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a9b84-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a9b84-137">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="a9b84-137">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
    
- [<span data-ttu-id="a9b84-138">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9b84-138">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="a9b84-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a9b84-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a9b84-140">OofSettings</span><span class="sxs-lookup"><span data-stu-id="a9b84-140">OofSettings</span></span>](oofsettings.md)
    
- [<span data-ttu-id="a9b84-141">OofState</span><span class="sxs-lookup"><span data-stu-id="a9b84-141">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="a9b84-142">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="a9b84-142">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="a9b84-143">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="a9b84-143">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="a9b84-144">StartTime</span><span class="sxs-lookup"><span data-stu-id="a9b84-144">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="a9b84-145">EndTime</span><span class="sxs-lookup"><span data-stu-id="a9b84-145">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="a9b84-146">InternalReply</span><span class="sxs-lookup"><span data-stu-id="a9b84-146">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="a9b84-147">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="a9b84-147">ExternalReply</span></span>](externalreply.md)
    
- [<span data-ttu-id="a9b84-148">Meldung</span><span class="sxs-lookup"><span data-stu-id="a9b84-148">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a9b84-149">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="a9b84-149">AllowExternalOof</span></span>](allowexternaloof.md)
    
## <a name="getuseroofsettings-error-response-example"></a><span data-ttu-id="a9b84-150">GetUserOofSettings-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9b84-150">GetUserOofSettings Error response example</span></span>

### <a name="description"></a><span data-ttu-id="a9b84-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9b84-151">Description</span></span>

<span data-ttu-id="a9b84-152">Das folgende Beispiel zeigt eine Fehlermeldung, die durch einen Versuch verursacht wurde, auf die OOF-Informationen eines anderen Benutzers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a9b84-152">The following example shows an error response caused by an attempt to access another user's OOF information.</span></span>
  
### <a name="code"></a><span data-ttu-id="a9b84-153">Code</span><span class="sxs-lookup"><span data-stu-id="a9b84-153">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <faultcode>soap:Client</faultcode>
      <faultstring>Microsoft.Exchange.Data.Storage.AccessDeniedException: User is not mailbox owner. User = S-1-5-21-3642464542-282065186-3871681729-1155, MailboxGuid = S-1-5-21-3642464542-282065186-3871681729-1156 ---> User is not mailbox owner. </faultstring>
      <faultactor>https://CAS01.example.com/EWS/Exchange.asmx</faultactor>
      <detail>
        <ErrorCode xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">-2146233088</ErrorCode>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="a9b84-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9b84-154">See also</span></span>



- [<span data-ttu-id="a9b84-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a9b84-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

