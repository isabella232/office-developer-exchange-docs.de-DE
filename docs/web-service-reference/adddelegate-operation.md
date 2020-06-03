---
title: AddDelegate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegate
api_type:
- schema
ms.assetid: 012d8cc5-648c-4ba0-a155-15c422b1e994
description: Mit dem AddDelegate-Vorgang werden dem Postfach eines Prinzipals mindestens eine Stellvertretung hinzugefügt, und es werden bestimmte Zugriffsberechtigungen festgelegt.
ms.openlocfilehash: 80adbe71d69be1025dc9593c6a9002bc68fdcb76
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466514"
---
# <a name="adddelegate-operation"></a><span data-ttu-id="d94a3-103">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d94a3-103">AddDelegate operation</span></span>

<span data-ttu-id="d94a3-104">Mit dem **AddDelegate** -Vorgang werden dem Postfach eines Prinzipals mindestens eine Stellvertretung hinzugefügt, und es werden bestimmte Zugriffsberechtigungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d94a3-104">The **AddDelegate** operation adds one or more delegates to a principal's mailbox and sets specific access permissions.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="d94a3-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="d94a3-105">SOAP headers</span></span>

<span data-ttu-id="d94a3-106">Der **AddDelegate** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d94a3-106">The **AddDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="d94a3-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="d94a3-107">**Header**</span></span>|<span data-ttu-id="d94a3-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="d94a3-108">**Element**</span></span>|<span data-ttu-id="d94a3-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d94a3-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d94a3-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="d94a3-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="d94a3-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d94a3-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d94a3-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="d94a3-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="d94a3-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d94a3-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="d94a3-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d94a3-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d94a3-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d94a3-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="d94a3-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="d94a3-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="d94a3-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d94a3-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d94a3-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="d94a3-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="d94a3-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="d94a3-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="d94a3-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d94a3-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d94a3-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="d94a3-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="adddelegate-request-example"></a><span data-ttu-id="d94a3-122">AddDelegate-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="d94a3-122">AddDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="d94a3-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d94a3-123">Description</span></span>

<span data-ttu-id="d94a3-124">Im folgenden Beispiel einer **AddDelegate** -Anforderung wird versucht, user1 Stellvertretungsberechtigungen für Ordner zu erteilen, die Benutzer2 gehören.</span><span class="sxs-lookup"><span data-stu-id="d94a3-124">The following example of an **AddDelegate** request shows an attempt to give user1 delegate permissions on folders that are owned by user2.</span></span> <span data-ttu-id="d94a3-125">User1 erhält Berechtigungen auf Autor Ebene zum Benutzer2 von Kalenderordner-und Prüferberechtigungen auf Benutzer2 Kontakteordner.</span><span class="sxs-lookup"><span data-stu-id="d94a3-125">User1 is given Author-level permissions to user2's Calendar folder and Reviewer-level permissions to user2's Contacts folder.</span></span> <span data-ttu-id="d94a3-126">User1 empfängt keine Kopien von Besprechungsnachrichten und kann keine privaten Elemente im Benutzer2-Postfach anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d94a3-126">User1 will not receive copies of meeting messages and will be unable to view private items in user2's mailbox.</span></span> <span data-ttu-id="d94a3-127">Besprechungsanfragen werden sowohl an user1 als auch an Benutzer2 gesendet.</span><span class="sxs-lookup"><span data-stu-id="d94a3-127">Meeting requests will be sent to both user1 and user2.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d94a3-128">Code</span><span class="sxs-lookup"><span data-stu-id="d94a3-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <AddDelegate>
      <Mailbox>
        <t:EmailAddress>user2@example.com</t:EmailAddress>
      </Mailbox>
      <DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user1@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>Author</t:CalendarFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>Reviewer</t:ContactsFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
      </DelegateUsers>
      <DeliverMeetingRequests>DelegatesAndMe</DeliverMeetingRequests>
    </AddDelegate>
  </soap:Body>
</soap:Envelope>
```

## <a name="adddelegate-response-example"></a><span data-ttu-id="d94a3-129">Beispiel für eine AddDelegate-Antwort</span><span class="sxs-lookup"><span data-stu-id="d94a3-129">AddDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="d94a3-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d94a3-130">Description</span></span>

<span data-ttu-id="d94a3-131">Das folgende Beispiel einer **AddDelegate** -Antwort zeigt eine erfolgreiche Antwort auf eine **AddDelegate** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d94a3-131">The following example of an **AddDelegate** response shows a successful response to an **AddDelegate** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d94a3-132">Code</span><span class="sxs-lookup"><span data-stu-id="d94a3-132">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           ResponseClass="Success" 
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
              <t:UserId>
                <t:SID>S-1-5-21-1333220396-2200287332-232816053-1116</t:SID>
                <t:PrimarySmtpAddress>User1@example.com</t:PrimarySmtpAddress>
                <t:DisplayName>User1</t:DisplayName>
              </t:UserId>
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:AddDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="adddelegate-error-response-example"></a><span data-ttu-id="d94a3-133">Beispiel für eine AddDelegate-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="d94a3-133">AddDelegate error response example</span></span>

### <a name="description"></a><span data-ttu-id="d94a3-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d94a3-134">Description</span></span>

<span data-ttu-id="d94a3-135">Im folgenden Beispiel wird die Antwort auf eine Anforderung zum Hinzufügen einer Stellvertretung gezeigt, die dem Postfach des Prinzipals bereits hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d94a3-135">The following example shows the response to a request to add a delegate who has already been added to the principal's mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="d94a3-136">Code</span><span class="sxs-lookup"><span data-stu-id="d94a3-136">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                           ResponseClass="Success"
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is already a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorDelegateAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:AddDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="d94a3-137">Comments</span><span class="sxs-lookup"><span data-stu-id="d94a3-137">Comments</span></span>

<span data-ttu-id="d94a3-138">Wenn der ErrorDelegateAlreadyExists-Antwortcode zurückgegeben wird, wenn Sie versuchen, eine Stellvertretung hinzuzufügen, verwenden Sie den [getdelegate-Vorgang](getdelegate-operation.md) , um alle aktuellen Berechtigungen für die Stellvertretung abzurufen, und verwenden Sie dann den [UpdateDelegate-Vorgang](updatedelegate-operation.md) , um die neuen Berechtigungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d94a3-138">If the ErrorDelegateAlreadyExists response code is returned when you try to add a delegate, use the [GetDelegate operation](getdelegate-operation.md) to get all the current permissions for the delegate, and then use the [UpdateDelegate operation](updatedelegate-operation.md) to set the new permissions.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d94a3-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d94a3-139">See also</span></span>

- [<span data-ttu-id="d94a3-140">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="d94a3-140">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

