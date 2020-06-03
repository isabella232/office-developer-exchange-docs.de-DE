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
description: Der UpdateInboxRules-Vorgang aktualisiert die Posteingangsregeln des authentifizierten Benutzers durch Anwenden der angegebenen Vorgänge. UpdateInboxRules wird verwendet, um eine Posteingangsregel zu erstellen, um eine Posteingangsregel festzulegen oder um eine Posteingangsregel zu löschen.
ms.openlocfilehash: a6ced4be25c6fe4649ad649ba01194791548bf67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44531000"
---
# <a name="updateinboxrules-operation"></a><span data-ttu-id="642fb-104">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="642fb-104">UpdateInboxRules operation</span></span>

<span data-ttu-id="642fb-105">Der UpdateInboxRules-Vorgang aktualisiert die Posteingangsregeln des authentifizierten Benutzers durch Anwenden der angegebenen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="642fb-105">The UpdateInboxRules operation updates the authenticated user's Inbox rules by applying the specified operations.</span></span> <span data-ttu-id="642fb-106">**UpdateInboxRules** wird verwendet, um eine Posteingangsregel zu erstellen, um eine Posteingangsregel festzulegen oder um eine Posteingangsregel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="642fb-106">**UpdateInboxRules** is used to create an Inbox rule, to set an Inbox rule, or to delete an Inbox rule.</span></span> 
  
<span data-ttu-id="642fb-107">Wenn Sie den **UpdateInboxRules** -Vorgang verwenden, löscht Exchange Webdienste clientseitige Sende Regeln.</span><span class="sxs-lookup"><span data-stu-id="642fb-107">When you use the **UpdateInboxRules** operation, Exchange Web Services deletes client-side send rules.</span></span> <span data-ttu-id="642fb-108">Clientseitige Sende Regeln werden auf dem Client in der FAI-Nachricht (Regel Ordner – zugeordnete Informationen) gespeichert und nirgendwo sonst.</span><span class="sxs-lookup"><span data-stu-id="642fb-108">Client-side send rules are stored on the client in the rule Folder Associated Information (FAI) Message and nowhere else.</span></span> <span data-ttu-id="642fb-109">In EWS wird diese Regel "fai" standardmäßig gelöscht, basierend auf der Erwartung, dass Outlook Sie neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="642fb-109">EWS deletes this rule FAI message by default, based on the expectation that Outlook will recreate it.</span></span> <span data-ttu-id="642fb-110">Outlook kann jedoch keine Regeln neu erstellen, die nicht auch als erweiterte Regel vorhanden sind, und clientseitige Sende Regeln sind nicht als erweiterte Regeln vorhanden.</span><span class="sxs-lookup"><span data-stu-id="642fb-110">However, Outlook can't recreate rules that don't also exist as an extended rule, and client-side send rules don't exist as extended rules.</span></span> <span data-ttu-id="642fb-111">Daher gehen diese Regeln verloren.</span><span class="sxs-lookup"><span data-stu-id="642fb-111">As a result, these rules are lost.</span></span> <span data-ttu-id="642fb-112">Wir empfehlen, dies beim Entwerfen der Lösung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="642fb-112">We suggest you consider this when designing your solution.</span></span> 
  
## <a name="updateinboxrules-create-rule-request-example"></a><span data-ttu-id="642fb-113">UpdateInboxRules (Create Rule)-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="642fb-113">UpdateInboxRules (Create Rule) request example</span></span>

<span data-ttu-id="642fb-114">Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Informationsspeicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="642fb-114">You can use Exchange Web Services to create an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="642fb-115">Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="642fb-115">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="642fb-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642fb-116">Description</span></span>

<span data-ttu-id="642fb-117">Der Client erstellt den Anforderungs-XML-Code und sendet ihn an den Server.</span><span class="sxs-lookup"><span data-stu-id="642fb-117">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="642fb-118">Code</span><span class="sxs-lookup"><span data-stu-id="642fb-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="642fb-119">Comments</span><span class="sxs-lookup"><span data-stu-id="642fb-119">Comments</span></span>

<span data-ttu-id="642fb-120">In diesem Beispiel wird eine Regel erstellt, die eine e-Mail-Nachricht in den Ordner Junk-e-Mail verschiebt, wenn der e-Mail-Betreff eine Zeichenfolge enthält, die "interessant" entspricht.</span><span class="sxs-lookup"><span data-stu-id="642fb-120">This example builds a rule that will move an e-mail message to the Junk E-mail folder if the e-mail subject contains a string that equals "Interesting".</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="642fb-121">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="642fb-121">Request elements</span></span>

<span data-ttu-id="642fb-122">Die **UpdateInboxRules** -Anforderung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="642fb-122">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="642fb-123">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="642fb-123">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="642fb-124">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="642fb-124">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="642fb-125">Operations</span><span class="sxs-lookup"><span data-stu-id="642fb-125">Operations</span></span>](operations.md)
    
<span data-ttu-id="642fb-126">Das [Operations](operations.md) -Element enthält das [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="642fb-126">The [Operations](operations.md) element contains the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
## <a name="updateinboxrules-create-rule-response-example"></a><span data-ttu-id="642fb-127">UpdateInboxRules (Create Rule)-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="642fb-127">UpdateInboxRules (Create Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="642fb-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642fb-128">Description</span></span>

<span data-ttu-id="642fb-129">Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel erstellt.</span><span class="sxs-lookup"><span data-stu-id="642fb-129">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that creates a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="642fb-130">Code</span><span class="sxs-lookup"><span data-stu-id="642fb-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="642fb-131">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="642fb-131">Successful response elements</span></span>

<span data-ttu-id="642fb-132">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="642fb-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="642fb-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="642fb-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="642fb-134">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="642fb-134">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="642fb-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="642fb-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="642fb-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="642fb-136">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a><span data-ttu-id="642fb-137">UpdateInboxRules (Regel festlegen)-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="642fb-137">UpdateInboxRules (Set Rule) request example</span></span>

<span data-ttu-id="642fb-138">Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Informationsspeicher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="642fb-138">You can use Exchange Web Services to modify an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="642fb-139">Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern.</span><span class="sxs-lookup"><span data-stu-id="642fb-139">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="642fb-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642fb-140">Description</span></span>

<span data-ttu-id="642fb-141">Der Client erstellt den Anforderungs-XML-Code und sendet ihn an den Server.</span><span class="sxs-lookup"><span data-stu-id="642fb-141">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="642fb-142">Code</span><span class="sxs-lookup"><span data-stu-id="642fb-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="642fb-143">Comments</span><span class="sxs-lookup"><span data-stu-id="642fb-143">Comments</span></span>

<span data-ttu-id="642fb-144">In diesem Beispiel wird der Anzeigename in "(geändert) this is Junk" geändert.</span><span class="sxs-lookup"><span data-stu-id="642fb-144">This example changes the display name to "(Modified) This is Junk".</span></span>
  
> [!NOTE]
> <span data-ttu-id="642fb-145">Die Werte der Attribute **ID** und **ChangeKey** des [Folder](folderid.md) -Elements wurden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="642fb-145">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="642fb-146">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="642fb-146">Request elements</span></span>

<span data-ttu-id="642fb-147">Die **UpdateInboxRules** -Anforderung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="642fb-147">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="642fb-148">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="642fb-148">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="642fb-149">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="642fb-149">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="642fb-150">Operations</span><span class="sxs-lookup"><span data-stu-id="642fb-150">Operations</span></span>](operations.md)
    
<span data-ttu-id="642fb-151">Das [Operations](operations.md) -Element enthält das [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern.</span><span class="sxs-lookup"><span data-stu-id="642fb-151">The [Operations](operations.md) element contains the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
## <a name="updateinboxrules-set-rule-response-example"></a><span data-ttu-id="642fb-152">UpdateInboxRules (Regel festlegen)-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="642fb-152">UpdateInboxRules (Set Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="642fb-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642fb-153">Description</span></span>

<span data-ttu-id="642fb-154">Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel ändert.</span><span class="sxs-lookup"><span data-stu-id="642fb-154">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that modifies a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="642fb-155">Code</span><span class="sxs-lookup"><span data-stu-id="642fb-155">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="642fb-156">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="642fb-156">Successful response elements</span></span>

<span data-ttu-id="642fb-157">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="642fb-157">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="642fb-158">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="642fb-158">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="642fb-159">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="642fb-159">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="642fb-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="642fb-160">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="642fb-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="642fb-161">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a><span data-ttu-id="642fb-162">UpdateInboxRules (Delete Rule)-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="642fb-162">UpdateInboxRules (Delete Rule) request example</span></span>

<span data-ttu-id="642fb-163">Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Informationsspeicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="642fb-163">You can use Exchange Web Services to delete an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="642fb-164">Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) in Verbindung mit dem [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="642fb-164">Use the [UpdateInboxRules](updateinboxrules.md) in conjunction with the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="642fb-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642fb-165">Description</span></span>

<span data-ttu-id="642fb-166">Der Client erstellt den Anforderungs-XML-Code und sendet ihn an den Server.</span><span class="sxs-lookup"><span data-stu-id="642fb-166">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="642fb-167">Code</span><span class="sxs-lookup"><span data-stu-id="642fb-167">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="642fb-168">Comments</span><span class="sxs-lookup"><span data-stu-id="642fb-168">Comments</span></span>

<span data-ttu-id="642fb-169">In diesem Beispiel wird die vorhandene angegebene Regel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="642fb-169">This example deletes the existing identified rule.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="642fb-170">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="642fb-170">Request elements</span></span>

<span data-ttu-id="642fb-171">Die **UpdateInboxRules** -Anforderung umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="642fb-171">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="642fb-172">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="642fb-172">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="642fb-173">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="642fb-173">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="642fb-174">Operations</span><span class="sxs-lookup"><span data-stu-id="642fb-174">Operations</span></span>](operations.md)
    
<span data-ttu-id="642fb-175">Das [Operations](operations.md) -Element enthält das [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="642fb-175">The [Operations](operations.md) element contains the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
## <a name="updateinboxrules-delete-rule-response-example"></a><span data-ttu-id="642fb-176">UpdateInboxRules (Delete Rule)-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="642fb-176">UpdateInboxRules (Delete Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="642fb-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642fb-177">Description</span></span>

<span data-ttu-id="642fb-178">Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel löscht.</span><span class="sxs-lookup"><span data-stu-id="642fb-178">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that deletes a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="642fb-179">Code</span><span class="sxs-lookup"><span data-stu-id="642fb-179">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="642fb-180">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="642fb-180">Successful response elements</span></span>

<span data-ttu-id="642fb-181">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="642fb-181">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="642fb-182">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="642fb-182">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="642fb-183">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="642fb-183">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="642fb-184">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="642fb-184">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="642fb-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="642fb-185">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="642fb-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="642fb-186">See also</span></span>



[<span data-ttu-id="642fb-187">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="642fb-187">GetInboxRules operation</span></span>](getinboxrules-operation.md)

