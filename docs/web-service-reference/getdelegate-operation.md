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
description: Der getdelegate-Vorgang ruft die Stell Vertretungs Einstellungen für ein angegebenes Postfach ab.
ms.openlocfilehash: 400bf5d1cafcbb789aaa749c62c7a908622d4ddb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461065"
---
# <a name="getdelegate-operation"></a><span data-ttu-id="1deca-103">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1deca-103">GetDelegate operation</span></span>

<span data-ttu-id="1deca-104">Der **getdelegate** -Vorgang ruft die Stell Vertretungs Einstellungen für ein angegebenes Postfach ab.</span><span class="sxs-lookup"><span data-stu-id="1deca-104">The **GetDelegate** operation retrieves the delegate settings for a specified mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="1deca-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="1deca-105">SOAP Headers</span></span>

<span data-ttu-id="1deca-106">Der **getdelegate** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1deca-106">The **GetDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="1deca-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="1deca-107">**Header**</span></span>|<span data-ttu-id="1deca-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="1deca-108">**Element**</span></span>|<span data-ttu-id="1deca-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1deca-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1deca-110">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="1deca-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="1deca-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="1deca-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="1deca-112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="1deca-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="1deca-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="1deca-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="1deca-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="1deca-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="1deca-115">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1deca-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="1deca-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="1deca-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="1deca-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="1deca-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="1deca-118">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="1deca-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="1deca-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="1deca-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="1deca-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1deca-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="1deca-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="1deca-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getdelegate-request-example"></a><span data-ttu-id="1deca-122">Getdelegate-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="1deca-122">GetDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="1deca-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1deca-123">Description</span></span>

<span data-ttu-id="1deca-124">Im folgenden Codebeispiel wird veranschaulicht, wie die Stell Vertretungs Einstellungen für alle Delegaten abgerufen werden, die für das user3's-Postfach festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1deca-124">The following code example shows how to retrieve the delegate settings for all the delegates that are set on user3's mailbox.</span></span> <span data-ttu-id="1deca-125">Alle Berechtigungen für jeden Benutzer werden in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1deca-125">All the permissions for each user are returned in the response.</span></span>
  
### <a name="code"></a><span data-ttu-id="1deca-126">Code</span><span class="sxs-lookup"><span data-stu-id="1deca-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <GetDelegate xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                 IncludePermissions="true">
      <Mailbox>
        <t:EmailAddress>user3@example.com</t:EmailAddress>
      </Mailbox>
    </GetDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="1deca-127">Comments</span><span class="sxs-lookup"><span data-stu-id="1deca-127">Comments</span></span>

<span data-ttu-id="1deca-128">Sie können das [UserID](userid.md) -Element verwenden, um einzelne Benutzer anzugeben, anstatt alle Benutzer mit Stell Vertretungs Zugriffsberechtigungen für das Postfach zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1deca-128">You can use the [UserId](userid.md) element to specify individual users instead of returning all users who have delegate access permissions on the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1deca-129">Das Verwalten von Gruppen Delegaten wird von Exchange-Webdienste nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1deca-129">Exchange Web Services (EWS) does not support managing group delegates.</span></span> <span data-ttu-id="1deca-130">EWS gibt einen Fehler zurück, wenn der **getdelegate** -Vorgang für einen Prinzipal mit einem Sicherheitsgruppen Delegaten aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1deca-130">EWS will return an error if the **GetDelegate** operation is called for a principal that has a security group delegate.</span></span> 
  
## <a name="getdelegate-response-example"></a><span data-ttu-id="1deca-131">Getdelegate-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="1deca-131">GetDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="1deca-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1deca-132">Description</span></span>

<span data-ttu-id="1deca-133">Das folgende Beispiel einer **getdelegate** -Antwort zeigt eine erfolgreiche Antwort auf eine **getdelegate** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1deca-133">The following example of a **GetDelegate** response shows a successful response to a **GetDelegate** request.</span></span> <span data-ttu-id="1deca-134">Die Antwort enthält Informationen zu den Zugriffsberechtigungen für Stellvertretungen, unabhängig davon, ob die Stellvertretung private Elemente anzeigen kann, ob die Stellvertretung Kopien von Besprechungsnachrichten empfängt und an wen Besprechungsanfragen übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="1deca-134">The response contains information about the delegate access permissions, whether the delegate can view private items, whether the delegate receives copies of meeting messages, and to whom meeting requests were delivered.</span></span> 
  
### <a name="code"></a><span data-ttu-id="1deca-135">Code</span><span class="sxs-lookup"><span data-stu-id="1deca-135">Code</span></span>

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
    <m:GetDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

## <a name="see-also"></a><span data-ttu-id="1deca-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1deca-136">See also</span></span>



- [<span data-ttu-id="1deca-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1deca-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

