---
title: UpdateDelegate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: 03f618ac-ad1a-4772-9b81-c5bb0f12d6ab
description: Der Vorgang UpdateDelegate aktualisiert Berechtigungen der Stellvertretung für einen Prinzipal Postfach.
ms.openlocfilehash: 9f69d784617d10d8902a260bbf6639703dd33b6d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839341"
---
# <a name="updatedelegate-operation"></a><span data-ttu-id="2db74-103">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2db74-103">UpdateDelegate operation</span></span>

<span data-ttu-id="2db74-104">Der Vorgang **UpdateDelegate** aktualisiert Berechtigungen der Stellvertretung für einen Prinzipal Postfach.</span><span class="sxs-lookup"><span data-stu-id="2db74-104">The **UpdateDelegate** operation updates delegate permissions on a principal's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="2db74-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="2db74-105">SOAP Headers</span></span>

<span data-ttu-id="2db74-106">Der Vorgang **UpdateDelegate** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2db74-106">The **UpdateDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="2db74-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="2db74-107">**Header**</span></span>|<span data-ttu-id="2db74-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="2db74-108">**Element**</span></span>|<span data-ttu-id="2db74-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2db74-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2db74-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="2db74-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="2db74-111">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="2db74-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2db74-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="2db74-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="2db74-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2db74-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="2db74-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2db74-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="2db74-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2db74-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="2db74-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="2db74-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="2db74-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2db74-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2db74-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="2db74-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="2db74-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="2db74-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="2db74-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2db74-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2db74-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="2db74-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="updatedelegate-request-example"></a><span data-ttu-id="2db74-122">Anforderungsbeispiel UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="2db74-122">UpdateDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="2db74-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2db74-123">Description</span></span>

<span data-ttu-id="2db74-124">Im folgenden Beispiel wird einer Anforderung **UpdateDelegate** zeigt, wie die Berechtigungen der Stellvertretung für das Konto von Benutzer1 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2db74-124">The following example of an **UpdateDelegate** request shows you how to update delegate permissions on user1's account.</span></span> <span data-ttu-id="2db74-125">Benutzer2 erhält keine Berechtigungen für den Ordner Aufgaben Ebene und erhält die Berechtigung zum Anzeigen der private Elemente.</span><span class="sxs-lookup"><span data-stu-id="2db74-125">User2 is granted the None permission level for the Tasks folder and is granted permission to view private items.</span></span> <span data-ttu-id="2db74-126">User3 wird Leseberechtigungen für den Ordner "Journal" erteilt.</span><span class="sxs-lookup"><span data-stu-id="2db74-126">User3 is granted Reviewer permissions for the Journal folder.</span></span> <span data-ttu-id="2db74-127">Besprechungsanfragen an die Stellvertretungen gesendet werden, und Informationen über die Anforderung an die User1 gesendet.</span><span class="sxs-lookup"><span data-stu-id="2db74-127">Meeting requests are sent to the delegates, and information about the request is sent to User1.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2db74-128">Code</span><span class="sxs-lookup"><span data-stu-id="2db74-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <UpdateDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>user1@example.com</t:EmailAddress>
      </Mailbox>
      <DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user2@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ViewPrivateItems>true</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user3@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:JournalFolderPermissionLevel>Reviewer</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
        </t:DelegateUser>
      </DelegateUsers>
      <DeliverMeetingRequests>DelegatesAndSendInformationToMe</DeliverMeetingRequests>
    </UpdateDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2db74-129">Kommentare</span><span class="sxs-lookup"><span data-stu-id="2db74-129">Comments</span></span>

<span data-ttu-id="2db74-130">Die [UpdateDelegate](updatedelegate.md) -Anforderung erfordert nicht, dass Updates auf Delegaten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2db74-130">The [UpdateDelegate](updatedelegate.md) request does not require that updates be applied to delegates.</span></span> <span data-ttu-id="2db74-131">Clients können nur die Einstellung der **DeliverMeetingMessage** ändern.</span><span class="sxs-lookup"><span data-stu-id="2db74-131">Clients can change only the **DeliverMeetingMessage** setting.</span></span> 
  
## <a name="updatedelegate-response-example"></a><span data-ttu-id="2db74-132">UpdateDelegate antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="2db74-132">UpdateDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="2db74-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2db74-133">Description</span></span>

<span data-ttu-id="2db74-134">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **UpdateDelegate** -Operation.</span><span class="sxs-lookup"><span data-stu-id="2db74-134">The following example shows a successful response to an **UpdateDelegate** operation.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2db74-135">Code</span><span class="sxs-lookup"><span data-stu-id="2db74-135">Code</span></span>

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
    <m:UpdateDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1117</t:SID>
              <t:PrimarySmtpAddress>User2@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User2</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>true</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1118</t:SID>
              <t:PrimarySmtpAddress>User3@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User3</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="updatedelegate-error-response-example"></a><span data-ttu-id="2db74-136">Antwortbeispiel UpdateDelegate-Fehler</span><span class="sxs-lookup"><span data-stu-id="2db74-136">UpdateDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="2db74-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2db74-137">Description</span></span>

<span data-ttu-id="2db74-138">Das folgende Beispiel zeigt eine Fehlerantwort an eine **UpdateDelegate** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2db74-138">The following example shows an error response to an **UpdateDelegate** request.</span></span> <span data-ttu-id="2db74-139">Der Fehler wurde generiert, da die Stellvertretung in der Principal-Delegatliste nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2db74-139">The error was generated because the delegate does not exist in the principal's delegate list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2db74-140">Code</span><span class="sxs-lookup"><span data-stu-id="2db74-140">Code</span></span>

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
    <m:UpdateDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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
      </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="2db74-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2db74-141">See also</span></span>



- [<span data-ttu-id="2db74-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2db74-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

