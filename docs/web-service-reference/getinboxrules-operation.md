---
title: GetInboxRules-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: b4b2701a-4a23-4acc-8c75-19f7955ad7ae
description: Der GetInboxRules-Vorgang verwendet Exchange Webdienste zum Abrufen von Posteingangsregeln im Postfach des identifizierten Benutzers.
ms.openlocfilehash: f4c4c03f55c9f32be4a067024f4387888edd5fe9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457935"
---
# <a name="getinboxrules-operation"></a><span data-ttu-id="07013-103">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="07013-103">GetInboxRules operation</span></span>

<span data-ttu-id="07013-104">Der **GetInboxRules** -Vorgang verwendet Exchange Webdienste zum Abrufen von Posteingangsregeln im Postfach des identifizierten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="07013-104">The **GetInboxRules** operation uses Exchange Web Services to retrieve Inbox rules in the identified user's mailbox.</span></span> 
  
## <a name="getinboxrules-request-example"></a><span data-ttu-id="07013-105">GetInboxRules-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="07013-105">GetInboxRules request example</span></span>

### <a name="description"></a><span data-ttu-id="07013-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07013-106">Description</span></span>

<span data-ttu-id="07013-107">Das folgende Beispiel zeigt den Anforderungs-XML-Code, den der Client an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="07013-107">The following example shows the request XML that the client sends to the server.</span></span> <span data-ttu-id="07013-108">Die Anforderung identifiziert den Benutzer im [MailboxSmtpAddress](mailboxsmtpaddress.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="07013-108">The request identifies the user in the [MailboxSmtpAddress](mailboxsmtpaddress.md) element.</span></span> <span data-ttu-id="07013-109">Alle Posteingangsregeln für den identifizierten Benutzer werden in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="07013-109">All Inbox rules for the identified user are to be returned in the response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="07013-110">Code</span><span class="sxs-lookup"><span data-stu-id="07013-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetInboxRules>
      <m:MailboxSmtpAddress>User1@Contoso.com</m:MailboxSmtpAddress>
    </m:GetInboxRules>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="07013-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="07013-111">Request elements</span></span>

<span data-ttu-id="07013-112">Die Anforderung enthält das folgende optionale Element:</span><span class="sxs-lookup"><span data-stu-id="07013-112">The request includes the following optional element:</span></span>
  
- [<span data-ttu-id="07013-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="07013-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a><span data-ttu-id="07013-114">Erfolgreiches GetInboxRules-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="07013-114">Successful GetInboxRules response example</span></span>

### <a name="description"></a><span data-ttu-id="07013-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07013-115">Description</span></span>

<span data-ttu-id="07013-116">Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **GetInboxRules** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="07013-116">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetInboxRules** request.</span></span> <span data-ttu-id="07013-117">In diesem Beispiel enthält die Antwort eine Regel.</span><span class="sxs-lookup"><span data-stu-id="07013-117">In this example, the response includes one rule.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="07013-118">Die Werte der ID und der **ChangeKey** -Attribute des [Folder](folderid.md) **-ID** -Elements wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="07013-118">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="07013-119">Code</span><span class="sxs-lookup"><span data-stu-id="07013-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
        MinorVersion="1" MajorBuildNumber="139"
        MinorBuildNumber="0"
        Version="Exchange2010_SP1"
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetInboxRulesResponse ResponseClass="Success"
        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <OutlookRuleBlobExists>true</OutlookRuleBlobExists>
      <InboxRules>
        <Rule xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <RuleId>dCsAAABjzvA=</RuleId>
          <DisplayName>MoveInterestingToJunk</DisplayName>
          <Priority>1</Priority>
          <IsEnabled>true</IsEnabled>
          <Conditions>
            <ContainsSubjectStrings>
              <String>Interesting</String>
            </ContainsSubjectStrings>
          </Conditions>
          <Actions>
            <MoveToFolder>
              <FolderId ChangeKey="AQAAAA==" Id="AAMkAGYzZjZm" />
            </MoveToFolder>
          </Actions>
        </Rule>
      </InboxRules>
    </GetInboxRulesResponse>
  </s:Body>
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="07013-120">Response-Elemente</span><span class="sxs-lookup"><span data-stu-id="07013-120">Response elements</span></span>

<span data-ttu-id="07013-121">Die Antwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="07013-121">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="07013-122">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="07013-122">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
    
- [<span data-ttu-id="07013-123">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="07013-123">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="07013-124">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="07013-124">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
    
- [<span data-ttu-id="07013-125">InboxRules</span><span class="sxs-lookup"><span data-stu-id="07013-125">InboxRules</span></span>](inboxrules.md)
    
## <a name="see-also"></a><span data-ttu-id="07013-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07013-126">See also</span></span>



[<span data-ttu-id="07013-127">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="07013-127">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)

