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
description: Der UpdateDelegate-Vorgang aktualisiert Stellvertretungsberechtigungen für das Postfach eines Prinzipals.
ms.openlocfilehash: b7cf5325d925f8d6588115a8657a2077e940f9d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468558"
---
# <a name="updatedelegate-operation"></a><span data-ttu-id="c09b3-103">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c09b3-103">UpdateDelegate operation</span></span>

<span data-ttu-id="c09b3-104">Der **UpdateDelegate** -Vorgang aktualisiert Stellvertretungsberechtigungen für das Postfach eines Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="c09b3-104">The **UpdateDelegate** operation updates delegate permissions on a principal's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="c09b3-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="c09b3-105">SOAP Headers</span></span>

<span data-ttu-id="c09b3-106">Der **UpdateDelegate** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c09b3-106">The **UpdateDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="c09b3-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="c09b3-107">**Header**</span></span>|<span data-ttu-id="c09b3-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="c09b3-108">**Element**</span></span>|<span data-ttu-id="c09b3-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c09b3-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c09b3-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="c09b3-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="c09b3-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c09b3-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c09b3-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="c09b3-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="c09b3-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c09b3-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="c09b3-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c09b3-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c09b3-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c09b3-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="c09b3-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="c09b3-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="c09b3-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c09b3-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c09b3-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c09b3-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="c09b3-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="c09b3-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="c09b3-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c09b3-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c09b3-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c09b3-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="updatedelegate-request-example"></a><span data-ttu-id="c09b3-122">UpdateDelegate-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="c09b3-122">UpdateDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="c09b3-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c09b3-123">Description</span></span>

<span data-ttu-id="c09b3-124">Im folgenden Beispiel einer **UpdateDelegate** -Anforderung wird gezeigt, wie Sie Stellvertretungsberechtigungen für das von Benutzer1-Konto aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c09b3-124">The following example of an **UpdateDelegate** request shows you how to update delegate permissions on user1's account.</span></span> <span data-ttu-id="c09b3-125">Benutzer2 wird die Berechtigungsstufe None für den Ordner Aufgaben erteilt, und es wird die Berechtigung zum Anzeigen privater Elemente erteilt.</span><span class="sxs-lookup"><span data-stu-id="c09b3-125">User2 is granted the None permission level for the Tasks folder and is granted permission to view private items.</span></span> <span data-ttu-id="c09b3-126">User3 werden Prüferberechtigungen für den Journal Ordner erteilt.</span><span class="sxs-lookup"><span data-stu-id="c09b3-126">User3 is granted Reviewer permissions for the Journal folder.</span></span> <span data-ttu-id="c09b3-127">Besprechungsanfragen werden an die Stellvertretungen gesendet, und Informationen zu der Anforderung werden an user1 gesendet.</span><span class="sxs-lookup"><span data-stu-id="c09b3-127">Meeting requests are sent to the delegates, and information about the request is sent to User1.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c09b3-128">Code</span><span class="sxs-lookup"><span data-stu-id="c09b3-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <UpdateDelegate xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="c09b3-129">Comments</span><span class="sxs-lookup"><span data-stu-id="c09b3-129">Comments</span></span>

<span data-ttu-id="c09b3-130">Für die [UpdateDelegate](updatedelegate.md) -Anforderung müssen keine Updates auf Stellvertretungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c09b3-130">The [UpdateDelegate](updatedelegate.md) request does not require that updates be applied to delegates.</span></span> <span data-ttu-id="c09b3-131">Clients können nur die **DeliverMeetingMessage** -Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="c09b3-131">Clients can change only the **DeliverMeetingMessage** setting.</span></span> 
  
## <a name="updatedelegate-response-example"></a><span data-ttu-id="c09b3-132">UpdateDelegate-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="c09b3-132">UpdateDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="c09b3-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c09b3-133">Description</span></span>

<span data-ttu-id="c09b3-134">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf einen **UpdateDelegate** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c09b3-134">The following example shows a successful response to an **UpdateDelegate** operation.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c09b3-135">Code</span><span class="sxs-lookup"><span data-stu-id="c09b3-135">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:UpdateDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="updatedelegate-error-response-example"></a><span data-ttu-id="c09b3-136">UpdateDelegate-Fehlerantwort Beispiel</span><span class="sxs-lookup"><span data-stu-id="c09b3-136">UpdateDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="c09b3-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c09b3-137">Description</span></span>

<span data-ttu-id="c09b3-138">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **UpdateDelegate** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c09b3-138">The following example shows an error response to an **UpdateDelegate** request.</span></span> <span data-ttu-id="c09b3-139">Der Fehler wurde generiert, da die Stellvertretung nicht in der Stell Vertretungsliste des Prinzipals vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c09b3-139">The error was generated because the delegate does not exist in the principal's delegate list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c09b3-140">Code</span><span class="sxs-lookup"><span data-stu-id="c09b3-140">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:UpdateDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              ResponseClass="Success" 
                              xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="see-also"></a><span data-ttu-id="c09b3-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c09b3-141">See also</span></span>



- [<span data-ttu-id="c09b3-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c09b3-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

