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
description: Der Vorgang AddDelegate Fügt eine oder mehrere Stellvertretungen des Prinzipals Postfach und bestimmte Zugriffsberechtigungen festgelegt.
ms.openlocfilehash: 28d4ded2625efc3d6eade44f5fafc06c2ffca7ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757217"
---
# <a name="adddelegate-operation"></a><span data-ttu-id="26663-103">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="26663-103">AddDelegate operation</span></span>

<span data-ttu-id="26663-104">Der Vorgang **AddDelegate** Fügt eine oder mehrere Stellvertretungen des Prinzipals Postfach und bestimmte Zugriffsberechtigungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26663-104">The **AddDelegate** operation adds one or more delegates to a principal's mailbox and sets specific access permissions.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="26663-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="26663-105">SOAP headers</span></span>

<span data-ttu-id="26663-106">Der Vorgang **AddDelegate** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="26663-106">The **AddDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="26663-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="26663-107">**Header**</span></span>|<span data-ttu-id="26663-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="26663-108">**Element**</span></span>|<span data-ttu-id="26663-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26663-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26663-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="26663-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="26663-111">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="26663-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="26663-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="26663-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="26663-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="26663-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="26663-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="26663-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="26663-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26663-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="26663-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="26663-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="26663-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="26663-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="26663-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="26663-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="26663-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="26663-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="26663-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="26663-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="26663-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="26663-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="adddelegate-request-example"></a><span data-ttu-id="26663-122">AddDelegate anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="26663-122">AddDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="26663-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26663-123">Description</span></span>

<span data-ttu-id="26663-124">Im folgenden Beispiel wird einer Anforderung **AddDelegate** Versuch user1 Stellvertretungsberechtigungen für Ordner erteilen, der von Benutzer2 gehören veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="26663-124">The following example of an **AddDelegate** request shows an attempt to give user1 delegate permissions on folders that are owned by user2.</span></span> <span data-ttu-id="26663-125">Benutzer1 erhält Berechtigungsstufe Berechtigungen von Benutzer2 Kalenderordner und Berechtigungen von Benutzer2 Kontakteordner Reviewer-Ebene.</span><span class="sxs-lookup"><span data-stu-id="26663-125">User1 is given Author-level permissions to user2's Calendar folder and Reviewer-level permissions to user2's Contacts folder.</span></span> <span data-ttu-id="26663-126">Benutzer1 Kopien der Besprechungsnachrichten, die wird nicht angezeigt und können keine privaten Elemente im Postfach von Benutzer2 anzeigen.</span><span class="sxs-lookup"><span data-stu-id="26663-126">User1 will not receive copies of meeting messages and will be unable to view private items in user2's mailbox.</span></span> <span data-ttu-id="26663-127">Besprechungsanfragen werden user1 und user2 versendet.</span><span class="sxs-lookup"><span data-stu-id="26663-127">Meeting requests will be sent to both user1 and user2.</span></span> 
  
### <a name="code"></a><span data-ttu-id="26663-128">Code</span><span class="sxs-lookup"><span data-stu-id="26663-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="adddelegate-response-example"></a><span data-ttu-id="26663-129">AddDelegate antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="26663-129">AddDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="26663-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26663-130">Description</span></span>

<span data-ttu-id="26663-131">Das folgende Beispiel für eine Antwort **AddDelegate** zeigt eine erfolgreiche Antwort auf eine Anforderung **AddDelegate** .</span><span class="sxs-lookup"><span data-stu-id="26663-131">The following example of an **AddDelegate** response shows a successful response to an **AddDelegate** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="26663-132">Code</span><span class="sxs-lookup"><span data-stu-id="26663-132">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           ResponseClass="Success" 
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="adddelegate-error-response-example"></a><span data-ttu-id="26663-133">AddDelegate Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="26663-133">AddDelegate error response example</span></span>

### <a name="description"></a><span data-ttu-id="26663-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26663-134">Description</span></span>

<span data-ttu-id="26663-135">Das folgende Beispiel zeigt die Antwort auf eine Anforderung an eine Stellvertretung hinzuzufügen, die den Prinzipal Postfach bereits hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="26663-135">The following example shows the response to a request to add a delegate who has already been added to the principal's mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="26663-136">Code</span><span class="sxs-lookup"><span data-stu-id="26663-136">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                           ResponseClass="Success"
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="26663-137">Kommentare</span><span class="sxs-lookup"><span data-stu-id="26663-137">Comments</span></span>

<span data-ttu-id="26663-138">Wenn ErrorDelegateAlreadyExists Antwortcodes zurückgegeben wird, wenn Sie versuchen, eine Stellvertretung hinzuzufügen, verwenden Sie die [GetDelegate Vorgang](getdelegate-operation.md) zum Abrufen der aktuellen Berechtigungen für die Stellvertretung, und klicken Sie dann verwenden Sie den [Vorgang UpdateDelegate](updatedelegate-operation.md) , um die neuen Berechtigungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="26663-138">If the ErrorDelegateAlreadyExists response code is returned when you try to add a delegate, use the [GetDelegate operation](getdelegate-operation.md) to get all the current permissions for the delegate, and then use the [UpdateDelegate operation](updatedelegate-operation.md) to set the new permissions.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26663-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26663-139">See also</span></span>

- [<span data-ttu-id="26663-140">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="26663-140">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

