---
title: GetInboxRules-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: b4b2701a-4a23-4acc-8c75-19f7955ad7ae
description: Der GetInboxRules-Vorgang verwendet Exchange Webdienste, um Posteingangsregeln im Postfach des identifizierten Benutzers abzurufen.
ms.openlocfilehash: 3e312ed08494b92c212595d081454b5f2ca6117e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546252"
---
# <a name="getinboxrules-operation"></a>GetInboxRules-Vorgang

Der **GetInboxRules-Vorgang** verwendet Exchange Webdienste, um Posteingangsregeln im Postfach des identifizierten Benutzers abzurufen. 
  
## <a name="getinboxrules-request-example"></a>GetInboxRules-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt den Anforderungs-XML-Code, den der Client an den Server sendet. Die Anforderung identifiziert den Benutzer im [MailboxSmtpAddress-Element.](mailboxsmtpaddress.md) Alle Posteingangsregeln für den identifizierten Benutzer müssen in der Antwort zurückgegeben werden. 
  
### <a name="code"></a>Code

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

### <a name="request-elements"></a>Anfordern von Elementen

Die Anforderung enthält das folgende optionale Element:
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a>Beispiel für erfolgreiche GetInboxRules-Antwort

### <a name="description"></a>Beschreibung

Der folgende SOAP-Text (Simple Object Access Protocol) zeigt eine erfolgreiche Antwort auf die **GetInboxRules-Anforderung.** In diesem Beispiel enthält die Antwort eine Regel. 
  
> [!NOTE]
> Die Werte der Attribute **"Id"** und **"ChangeKey"** des ["FolderId"-Elements](folderid.md) wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="code"></a>Code

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

### <a name="response-elements"></a>Antwortelemente

Die folgenden Elemente sind in der Antwort enthalten:
  
- [GetInboxRulesResponse](getinboxrulesresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [OutlookRuleBlobExists](outlookruleblobexists.md)
    
- [InboxRules](inboxrules.md)
    
## <a name="see-also"></a>Siehe auch



[UpdateInboxRules-Vorgang](updateinboxrules-operation.md)

