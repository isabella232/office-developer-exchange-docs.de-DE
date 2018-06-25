---
title: GetDelegate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 849b2c9e-4685-4bd1-9adb-aba0fcc52650
description: Der Vorgang GetDelegate werden die Stellvertretung Einstellungen für ein angegebenes Postfach abgerufen.
ms.openlocfilehash: bd1a0add54ee5fd1c23b4ba09a921a9061afa394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758626"
---
# <a name="getdelegate-operation"></a><span data-ttu-id="7e644-103">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7e644-103">GetDelegate operation</span></span>

<span data-ttu-id="7e644-104">Der Vorgang **GetDelegate** werden die Stellvertretung Einstellungen für ein angegebenes Postfach abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7e644-104">The **GetDelegate** operation retrieves the delegate settings for a specified mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="7e644-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="7e644-105">SOAP Headers</span></span>

<span data-ttu-id="7e644-106">Der Vorgang **GetDelegate** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7e644-106">The **GetDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="7e644-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="7e644-107">**Header**</span></span>|<span data-ttu-id="7e644-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="7e644-108">**Element**</span></span>|<span data-ttu-id="7e644-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e644-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7e644-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="7e644-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="7e644-111">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="7e644-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="7e644-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="7e644-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="7e644-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="7e644-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="7e644-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="7e644-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="7e644-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e644-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="7e644-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="7e644-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="7e644-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="7e644-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="7e644-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="7e644-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="7e644-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="7e644-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="7e644-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7e644-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="7e644-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="7e644-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getdelegate-request-example"></a><span data-ttu-id="7e644-122">Anforderungsbeispiel GetDelegate</span><span class="sxs-lookup"><span data-stu-id="7e644-122">GetDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="7e644-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e644-123">Description</span></span>

<span data-ttu-id="7e644-124">Im folgenden Codebeispiel wird veranschaulicht, wie die Stellvertretung Einstellungen für alle Delegaten abgerufen, die für die user3 Postfach festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7e644-124">The following code example shows how to retrieve the delegate settings for all the delegates that are set on user3's mailbox.</span></span> <span data-ttu-id="7e644-125">Alle Berechtigungen für jeden Benutzer werden in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e644-125">All the permissions for each user are returned in the response.</span></span>
  
### <a name="code"></a><span data-ttu-id="7e644-126">Code</span><span class="sxs-lookup"><span data-stu-id="7e644-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <GetDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                 IncludePermissions="true">
      <Mailbox>
        <t:EmailAddress>user3@example.com</t:EmailAddress>
      </Mailbox>
    </GetDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7e644-127">Kommentare</span><span class="sxs-lookup"><span data-stu-id="7e644-127">Comments</span></span>

<span data-ttu-id="7e644-128">[UserId](userid.md) -Element können Sie einzelne Benutzer anstelle von Zurückgeben aller Benutzer mit Berechtigungen der Stellvertretung Zugriff auf das Postfach angeben.</span><span class="sxs-lookup"><span data-stu-id="7e644-128">You can use the [UserId](userid.md) element to specify individual users instead of returning all users who have delegate access permissions on the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7e644-129">Verwalten von Stellvertretungen für Gruppe unterstützt Exchange-Webdienste (EWS) nicht.</span><span class="sxs-lookup"><span data-stu-id="7e644-129">Exchange Web Services (EWS) does not support managing group delegates.</span></span> <span data-ttu-id="7e644-130">EWS gibt einen Fehler zurück, wenn der Vorgang **GetDelegate** für einen Prinzipal aufgerufen wird, die eine Sicherheit Gruppe Stellvertretung hat.</span><span class="sxs-lookup"><span data-stu-id="7e644-130">EWS will return an error if the **GetDelegate** operation is called for a principal that has a security group delegate.</span></span> 
  
## <a name="getdelegate-response-example"></a><span data-ttu-id="7e644-131">GetDelegate antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="7e644-131">GetDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="7e644-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e644-132">Description</span></span>

<span data-ttu-id="7e644-133">Das folgende Beispiel einer Antwort **GetDelegate** zeigt eine erfolgreiche Antwort auf eine Anforderung **GetDelegate** .</span><span class="sxs-lookup"><span data-stu-id="7e644-133">The following example of a **GetDelegate** response shows a successful response to a **GetDelegate** request.</span></span> <span data-ttu-id="7e644-134">Die Antwort enthält Informationen zu den Berechtigungen der Stellvertretung Zugriff Sie, ob der Delegat private Elemente anzeigen kann, ob die Stellvertretung Kopien von besprechungsvorschlägen Nachrichten und an wen meeting empfängt Anfragen zugestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7e644-134">The response contains information about the delegate access permissions, whether the delegate can view private items, whether the delegate receives copies of meeting messages, and to whom meeting requests were delivered.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7e644-135">Code</span><span class="sxs-lookup"><span data-stu-id="7e644-135">Code</span></span>

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
    <m:GetDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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
              <t:DelegatePermissions>
                <t:CalendarFolderPermissionLevel>Author</t:CalendarFolderPermissionLevel>
                <t:ContactsFolderPermissionLevel>Reviewer</t:ContactsFolderPermissionLevel>
              </t:DelegatePermissions>
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
          </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      <m:DeliverMeetingRequests>DelegatesAndMe</m:DeliverMeetingRequests>
      </m:GetDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="7e644-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e644-136">See also</span></span>



- [<span data-ttu-id="7e644-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e644-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

