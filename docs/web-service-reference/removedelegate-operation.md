---
title: RemoveDelegate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: 1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a
description: Der Vorgang RemoveDelegate entfernt eine oder mehrere Stellvertretungen aus dem Postfach eines Benutzers.
ms.openlocfilehash: 6f3371d19bd8a7fd967d4959d85037ae6b51f6aa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831088"
---
# <a name="removedelegate-operation"></a><span data-ttu-id="e5d06-103">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e5d06-103">RemoveDelegate operation</span></span>

<span data-ttu-id="e5d06-104">Der Vorgang **RemoveDelegate** entfernt eine oder mehrere Stellvertretungen aus dem Postfach eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e5d06-104">The **RemoveDelegate** operation removes one or more delegates from a user's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="e5d06-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="e5d06-105">SOAP Headers</span></span>

<span data-ttu-id="e5d06-106">Der Vorgang **RemoveDelegate** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5d06-106">The **RemoveDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="e5d06-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="e5d06-107">**Header**</span></span>|<span data-ttu-id="e5d06-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5d06-108">**Element**</span></span>|<span data-ttu-id="e5d06-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5d06-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5d06-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="e5d06-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="e5d06-111">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="e5d06-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="e5d06-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="e5d06-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="e5d06-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="e5d06-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="e5d06-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="e5d06-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="e5d06-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5d06-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="e5d06-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="e5d06-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="e5d06-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e5d06-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e5d06-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="e5d06-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="e5d06-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="e5d06-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="e5d06-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e5d06-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e5d06-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="e5d06-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="removedelegate-request-example"></a><span data-ttu-id="e5d06-122">Anforderungsbeispiel RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="e5d06-122">RemoveDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="e5d06-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5d06-123">Description</span></span>

<span data-ttu-id="e5d06-124">Im folgenden Codebeispiel wird veranschaulicht, wie zwei Delegaten von Benutzer1 Postfach zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e5d06-124">The following code example shows how to remove two delegates from user1's mailbox.</span></span> <span data-ttu-id="e5d06-125">In diesem Beispiel wird eine Stellvertretung mithilfe der Stellvertretung primäre SMTP-Adresse entfernt, und anderen wird mithilfe der Stellvertretung Sicherheits-ID (SID) entfernt.</span><span class="sxs-lookup"><span data-stu-id="e5d06-125">In this example, one delegate is removed by using the delegate's primary SMTP address, and the other one is removed by using the delegate's security identifier (SID).</span></span>
  
### <a name="code"></a><span data-ttu-id="e5d06-126">Code</span><span class="sxs-lookup"><span data-stu-id="e5d06-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <RemoveDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>user1@example.com</t:EmailAddress>
      </Mailbox>
      <UserIds>
        <t:UserId>
          <t:PrimarySmtpAddress>user2@example.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:SID>S-1-5-21-1333220396-2200287332-232816053-1118</t:SID>
        </t:UserId>
      </UserIds>
    </RemoveDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="e5d06-127">Kommentare</span><span class="sxs-lookup"><span data-stu-id="e5d06-127">Comments</span></span>

<span data-ttu-id="e5d06-128">Der Vorgang **RemoveDelegate** erfordert keinen den angegebenen Delegaten Benutzer über ein Postfach verfügen oder in den Active Directory-Verzeichnisdienst vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e5d06-128">The **RemoveDelegate** operation does not require the specified delegate user to have a mailbox or to exist in the Active Directory directory service.</span></span> <span data-ttu-id="e5d06-129">Der Vorgang **RemoveDelegate** erfolgreich, wenn der Eintrag Delegaten verwaist ist.</span><span class="sxs-lookup"><span data-stu-id="e5d06-129">The **RemoveDelegate** operation will succeed if the delegate entry is orphaned.</span></span> 
  
## <a name="removedelegate-response-example"></a><span data-ttu-id="e5d06-130">RemoveDelegate antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="e5d06-130">RemoveDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="e5d06-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5d06-131">Description</span></span>

<span data-ttu-id="e5d06-132">Das folgende Beispiel einer Antwort **RemoveDelegate** zeigt eine erfolgreiche Antwort auf eine Anforderung **RemoveDelegate** .</span><span class="sxs-lookup"><span data-stu-id="e5d06-132">The following example of a **RemoveDelegate** response shows a successful response to a **RemoveDelegate** request.</span></span> <span data-ttu-id="e5d06-133">Die Antwort enthält ein **DelegateUserResponseMessageType** -Element für jeden Delegaten, die aus dem Postfach entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e5d06-133">The response contains a **DelegateUserResponseMessageType** element for each delegate that is removed from the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e5d06-134">Code</span><span class="sxs-lookup"><span data-stu-id="e5d06-134">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" 
                         MinorVersion="1" 
                         MajorBuildNumber="206" 
                         MinorBuildNumber="0" 
                         Version="Exchange2007_SP1" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              ResponseClass="Success" 
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:RemoveDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="removedelegate-error-response-example"></a><span data-ttu-id="e5d06-135">Antwortbeispiel RemoveDelegate-Fehler</span><span class="sxs-lookup"><span data-stu-id="e5d06-135">RemoveDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="e5d06-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5d06-136">Description</span></span>

<span data-ttu-id="e5d06-137">Im folgenden Beispiel wird eine Fehlerantwort **RemoveDelegate** zeigt die Ergebnisse einer Anforderung für eine Stellvertretung entfernen möchten, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e5d06-137">The following example of a **RemoveDelegate** error response shows the results of a request to remove a delegate that does not exist.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e5d06-138">Code</span><span class="sxs-lookup"><span data-stu-id="e5d06-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8"
                         MinorVersion="1"
                         MajorBuildNumber="206"
                         MinorBuildNumber="0"
                         Version="Exchange2007_SP1"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is not a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorNotDelegate</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:RemoveDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="e5d06-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5d06-139">See also</span></span>



- [<span data-ttu-id="e5d06-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e5d06-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

