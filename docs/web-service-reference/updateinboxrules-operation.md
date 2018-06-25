---
title: UpdateInboxRules-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: f982a237-471e-45c5-a2b5-468cfc53150b
description: Der Vorgang UpdateInboxRules aktualisiert Posteingangsregeln des authentifizierten Benutzers durch die angegebenen Vorgänge anwenden. UpdateInboxRules wird verwendet, um eine Posteingangsregel zu, um eine Posteingangsregel festzulegen oder löschen Sie eine Posteingangsregel zu erstellen.
ms.openlocfilehash: 6e979421d619fed6625fe05db86c1f8c6a7418c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839367"
---
# <a name="updateinboxrules-operation"></a><span data-ttu-id="ce63b-104">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ce63b-104">UpdateInboxRules operation</span></span>

<span data-ttu-id="ce63b-105">Der Vorgang UpdateInboxRules aktualisiert Posteingangsregeln des authentifizierten Benutzers durch die angegebenen Vorgänge anwenden.</span><span class="sxs-lookup"><span data-stu-id="ce63b-105">The UpdateInboxRules operation updates the authenticated user's Inbox rules by applying the specified operations.</span></span> <span data-ttu-id="ce63b-106">**UpdateInboxRules** wird verwendet, um eine Posteingangsregel zu, um eine Posteingangsregel festzulegen oder löschen Sie eine Posteingangsregel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce63b-106">**UpdateInboxRules** is used to create an Inbox rule, to set an Inbox rule, or to delete an Inbox rule.</span></span> 
  
<span data-ttu-id="ce63b-107">Wenn Sie den Vorgang **UpdateInboxRules** verwenden, löscht Exchange-Webdienste senden mithilfe der clientseitigen Regeln.</span><span class="sxs-lookup"><span data-stu-id="ce63b-107">When you use the **UpdateInboxRules** operation, Exchange Web Services deletes client-side send rules.</span></span> <span data-ttu-id="ce63b-108">Senden clientseitige Regeln werden auf dem Client in der Regel Ordner verknüpften Informationen (FAI)-Nachricht und keiner anderen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ce63b-108">Client-side send rules are stored on the client in the rule Folder Associated Information (FAI) Message and nowhere else.</span></span> <span data-ttu-id="ce63b-109">EWS löscht diese Regel FAI Nachricht standardmäßig basierend auf der Annahme, dass Outlook wird neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ce63b-109">EWS deletes this rule FAI message by default, based on the expectation that Outlook will recreate it.</span></span> <span data-ttu-id="ce63b-110">Allerdings Outlook kann nicht erstellen Regeln, die auch als eine erweiterte Regel vorhanden, nicht erneut, und Senden mithilfe der clientseitigen Regeln nicht als erweiterte Regeln vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ce63b-110">However, Outlook can't recreate rules that don't also exist as an extended rule, and client-side send rules don't exist as extended rules.</span></span> <span data-ttu-id="ce63b-111">Daher sind diese Regeln verloren.</span><span class="sxs-lookup"><span data-stu-id="ce63b-111">As a result, these rules are lost.</span></span> <span data-ttu-id="ce63b-112">Es wird empfohlen, dass Sie dies berücksichtigen Sie beim Entwerfen Ihrer Lösung.</span><span class="sxs-lookup"><span data-stu-id="ce63b-112">We suggest you consider this when designing your solution.</span></span> 
  
## <a name="updateinboxrules-create-rule-request-example"></a><span data-ttu-id="ce63b-113">Anforderungsbeispiel UpdateInboxRules (Regel erstellen)</span><span class="sxs-lookup"><span data-stu-id="ce63b-113">UpdateInboxRules (Create Rule) request example</span></span>

<span data-ttu-id="ce63b-114">Exchange-Webdienste können Sie um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce63b-114">You can use Exchange Web Services to create an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="ce63b-115">Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce63b-115">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="ce63b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce63b-116">Description</span></span>

<span data-ttu-id="ce63b-117">Der Client erstellt die Anforderung XML und sendet es an den Server.</span><span class="sxs-lookup"><span data-stu-id="ce63b-117">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="ce63b-118">Code</span><span class="sxs-lookup"><span data-stu-id="ce63b-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:CreateRuleOperation>
            <t:Rule>
              <t:DisplayName>MoveInterestingToJunk</t:DisplayName>
              <t:Priority>1</t:Priority>
              <t:IsEnabled>true</t:IsEnabled>
              <t:Conditions>
                <t:ContainsSubjectStrings>
                  <t:String>Interesting</t:String>
                </t:ContainsSubjectStrings>
              </t:Conditions>
              <t:Exceptions />
              <t:Actions>
                <t:MoveToFolder>
                  <t:DistinguishedFolderId Id="junkemail" />
                </t:MoveToFolder>
              </t:Actions>
            </t:Rule>
          </t:CreateRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="ce63b-119">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ce63b-119">Comments</span></span>

<span data-ttu-id="ce63b-120">Dieses Beispiel erstellt eine Regel, die eine E-mail-Nachricht in den Junk-e-Mail-Ordner verschoben werden, wenn der e-Mail-Betreff eine Zeichenfolge, die enthält "Interessanter" entspricht.</span><span class="sxs-lookup"><span data-stu-id="ce63b-120">This example builds a rule that will move an e-mail message to the Junk E-mail folder if the e-mail subject contains a string that equals "Interesting".</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ce63b-121">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="ce63b-121">Request elements</span></span>

<span data-ttu-id="ce63b-122">Die Anforderung **UpdateInboxRules** umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ce63b-122">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ce63b-123">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ce63b-123">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="ce63b-124">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="ce63b-124">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="ce63b-125">Betrieb</span><span class="sxs-lookup"><span data-stu-id="ce63b-125">Operations</span></span>](operations.md)
    
<span data-ttu-id="ce63b-126">Das [Vorgänge](operations.md) Element enthält das [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce63b-126">The [Operations](operations.md) element contains the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
## <a name="updateinboxrules-create-rule-response-example"></a><span data-ttu-id="ce63b-127">Antwortbeispiel UpdateInboxRules (Regel erstellen)</span><span class="sxs-lookup"><span data-stu-id="ce63b-127">UpdateInboxRules (Create Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="ce63b-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce63b-128">Description</span></span>

<span data-ttu-id="ce63b-129">Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce63b-129">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that creates a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ce63b-130">Code</span><span class="sxs-lookup"><span data-stu-id="ce63b-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="ce63b-131">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="ce63b-131">Successful response elements</span></span>

<span data-ttu-id="ce63b-132">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ce63b-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ce63b-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ce63b-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ce63b-134">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ce63b-134">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="ce63b-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ce63b-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ce63b-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ce63b-136">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a><span data-ttu-id="ce63b-137">Anforderungsbeispiel UpdateInboxRules (Rule festgelegt)</span><span class="sxs-lookup"><span data-stu-id="ce63b-137">UpdateInboxRules (Set Rule) request example</span></span>

<span data-ttu-id="ce63b-138">Exchange-Webdienste können Sie um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Speicher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ce63b-138">You can use Exchange Web Services to modify an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="ce63b-139">Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ce63b-139">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="ce63b-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce63b-140">Description</span></span>

<span data-ttu-id="ce63b-141">Der Client erstellt die Anforderung XML und sendet es an den Server.</span><span class="sxs-lookup"><span data-stu-id="ce63b-141">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="ce63b-142">Code</span><span class="sxs-lookup"><span data-stu-id="ce63b-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <Rule>
              <RuleId>Nh8AAAAwW/w=</RuleId>
              <DisplayName>(Modified) This is Junk</DisplayName>
              <Priority>1</Priority>
              <IsEnabled>true</IsEnabled>
              <Conditions>
                <ContainsSubjectStrings>
                  <String>Interesting</String>
                </ContainsSubjectStrings>
              </Conditions>
              <Actions>
                <MoveToFolder>
                  <FolderId Id="AAMkADQ1YTE1" ChangeKey="AQAAAA==" />
                </MoveToFolder>
              </Actions>
            </Rule>
          </SetRuleOperation>
        </Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="ce63b-143">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ce63b-143">Comments</span></span>

<span data-ttu-id="ce63b-144">In diesem Beispiel wird der Anzeigename auf "(geändert) Hierbei handelt es sich um Junk-e-".</span><span class="sxs-lookup"><span data-stu-id="ce63b-144">This example changes the display name to "(Modified) This is Junk".</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce63b-145">Die Werte der **Id** und **ChangeKey** Attribute des Elements [FolderId](folderid.md) wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="ce63b-145">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="ce63b-146">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="ce63b-146">Request elements</span></span>

<span data-ttu-id="ce63b-147">Die Anforderung **UpdateInboxRules** umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ce63b-147">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ce63b-148">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ce63b-148">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="ce63b-149">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="ce63b-149">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="ce63b-150">Betrieb</span><span class="sxs-lookup"><span data-stu-id="ce63b-150">Operations</span></span>](operations.md)
    
<span data-ttu-id="ce63b-151">Das [Vorgänge](operations.md) Element enthält das [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ce63b-151">The [Operations](operations.md) element contains the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
## <a name="updateinboxrules-set-rule-response-example"></a><span data-ttu-id="ce63b-152">Antwortbeispiel UpdateInboxRules (Rule festgelegt)</span><span class="sxs-lookup"><span data-stu-id="ce63b-152">UpdateInboxRules (Set Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="ce63b-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce63b-153">Description</span></span>

<span data-ttu-id="ce63b-154">Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel ändert.</span><span class="sxs-lookup"><span data-stu-id="ce63b-154">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that modifies a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ce63b-155">Code</span><span class="sxs-lookup"><span data-stu-id="ce63b-155">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="ce63b-156">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="ce63b-156">Successful response elements</span></span>

<span data-ttu-id="ce63b-157">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ce63b-157">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ce63b-158">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ce63b-158">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ce63b-159">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ce63b-159">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="ce63b-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ce63b-160">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ce63b-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ce63b-161">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a><span data-ttu-id="ce63b-162">Anforderungsbeispiel UpdateInboxRules (Regel löschen)</span><span class="sxs-lookup"><span data-stu-id="ce63b-162">UpdateInboxRules (Delete Rule) request example</span></span>

<span data-ttu-id="ce63b-163">Exchange-Webdienste können Sie um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Speicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ce63b-163">You can use Exchange Web Services to delete an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="ce63b-164">Verwenden Sie die [UpdateInboxRules](updateinboxrules.md) in Verbindung mit dem [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ce63b-164">Use the [UpdateInboxRules](updateinboxrules.md) in conjunction with the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="ce63b-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce63b-165">Description</span></span>

<span data-ttu-id="ce63b-166">Der Client erstellt die Anforderung XML und sendet es an den Server.</span><span class="sxs-lookup"><span data-stu-id="ce63b-166">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="ce63b-167">Code</span><span class="sxs-lookup"><span data-stu-id="ce63b-167">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:DeleteRuleOperation>
            <t:RuleId>Nh8AAAAwW/U=</t:RuleId>
          </t:DeleteRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="ce63b-168">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ce63b-168">Comments</span></span>

<span data-ttu-id="ce63b-169">Dieses Beispiel löscht die vorhandene identifizierte Regel.</span><span class="sxs-lookup"><span data-stu-id="ce63b-169">This example deletes the existing identified rule.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ce63b-170">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="ce63b-170">Request elements</span></span>

<span data-ttu-id="ce63b-171">Die Anforderung **UpdateInboxRules** umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ce63b-171">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ce63b-172">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ce63b-172">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="ce63b-173">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="ce63b-173">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="ce63b-174">Betrieb</span><span class="sxs-lookup"><span data-stu-id="ce63b-174">Operations</span></span>](operations.md)
    
<span data-ttu-id="ce63b-175">Das [Vorgänge](operations.md) Element enthält das [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ce63b-175">The [Operations](operations.md) element contains the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
## <a name="updateinboxrules-delete-rule-response-example"></a><span data-ttu-id="ce63b-176">Antwortbeispiel UpdateInboxRules (Regel löschen)</span><span class="sxs-lookup"><span data-stu-id="ce63b-176">UpdateInboxRules (Delete Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="ce63b-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce63b-177">Description</span></span>

<span data-ttu-id="ce63b-178">Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ce63b-178">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that deletes a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ce63b-179">Code</span><span class="sxs-lookup"><span data-stu-id="ce63b-179">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="ce63b-180">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="ce63b-180">Successful response elements</span></span>

<span data-ttu-id="ce63b-181">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ce63b-181">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ce63b-182">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ce63b-182">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ce63b-183">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ce63b-183">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="ce63b-184">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ce63b-184">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ce63b-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ce63b-185">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="ce63b-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce63b-186">See also</span></span>



[<span data-ttu-id="ce63b-187">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ce63b-187">GetInboxRules operation</span></span>](getinboxrules-operation.md)

