---
title: UpdateInboxRules-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: f982a237-471e-45c5-a2b5-468cfc53150b
description: Der UpdateInboxRules-Vorgang aktualisiert die Posteingangsregeln des authentifizierten Benutzers, indem die angegebenen Vorgänge angewendet werden. UpdateInboxRules wird verwendet, um eine Posteingangsregel zu erstellen, eine Posteingangsregel festzulegen oder eine Posteingangsregel zu löschen.
ms.openlocfilehash: 08f46219bcb01f5f1c9d69cfaa8b4934e82ff5bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510715"
---
# <a name="updateinboxrules-operation"></a>UpdateInboxRules-Vorgang

Der UpdateInboxRules-Vorgang aktualisiert die Posteingangsregeln des authentifizierten Benutzers, indem die angegebenen Vorgänge angewendet werden. **UpdateInboxRules** wird verwendet, um eine Posteingangsregel zu erstellen, eine Posteingangsregel festzulegen oder eine Posteingangsregel zu löschen. 
  
Wenn Sie den **UpdateInboxRules-Vorgang** verwenden, löscht Exchange Webdienste clientseitige Senderegeln. Clientseitige Senderegeln werden auf dem Client in der FaI-Nachricht (Rule Folder Associated Information) gespeichert und andernfalls. EWS löscht diese FAI-Regelnachricht standardmäßig, basierend auf der Erwartung, dass Outlook sie neu erstellen. Outlook können jedoch keine Regeln neu erstellen, die nicht auch als erweiterte Regel vorhanden sind, und clientseitige Senderegeln sind nicht als erweiterte Regeln vorhanden. Daher gehen diese Regeln verloren. Wir empfehlen Ihnen, dies beim Entwerfen Ihrer Lösung zu berücksichtigen. 
  
## <a name="updateinboxrules-create-rule-request-example"></a>UpdateInboxRules (Create Rule)-Anforderungsbeispiel

Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange Speicher zu erstellen. Verwenden Sie das [UpdateInboxRules-Element](updateinboxrules.md) in Verbindung mit dem [CreateRuleOperation-Element,](createruleoperation.md) um eine Regel zu erstellen. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt die Anforderungs-XML und sendet sie an den Server.
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Comments

In diesem Beispiel wird eine Regel erstellt, mit der eine E-Mail-Nachricht in den Junk-E-Mail-Ordner verschoben wird, wenn der E-Mail-Betreff eine Zeichenfolge mit dem Wert "Interesting" enthält.
  
### <a name="request-elements"></a>Anfordern von Elementen

Die **UpdateInboxRules-Anforderung** enthält die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
Das [Operations-Element](operations.md) enthält das [CreateRuleOperation-Element,](createruleoperation.md) um eine Regel zu erstellen. 
  
## <a name="updateinboxrules-create-rule-response-example"></a>UpdateInboxRules (Create Rule)-Antwortbeispiel

### <a name="description"></a>Beschreibung

Der folgende SOAP-Text (Simple Object Access Protocol) zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules-Anforderung,** die eine Regel erstellt. 
  
### <a name="code"></a>Code

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

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a>UpdateInboxRules (Set Rule)-Anforderungsbeispiel

Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange Speicher zu ändern. Verwenden Sie das [UpdateInboxRules-Element](updateinboxrules.md) in Verbindung mit dem [SetRuleOperation-Element,](setruleoperation.md) um eine Regel zu ändern. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt die Anforderungs-XML und sendet sie an den Server.
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Comments

In diesem Beispiel wird der Anzeigename in "(Geändert) Dies ist Junk" geändert.
  
> [!NOTE]
> Die Werte der Attribute **"Id"** und **"ChangeKey"** des ["FolderId"-Elements](folderid.md) wurden zur besseren Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

Die **UpdateInboxRules-Anforderung** enthält die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
Das [Operations-Element](operations.md) enthält das [SetRuleOperation-Element,](setruleoperation.md) um eine Regel zu ändern. 
  
## <a name="updateinboxrules-set-rule-response-example"></a>UpdateInboxRules (Set Rule)-Antwortbeispiel

### <a name="description"></a>Beschreibung

Der folgende SOAP-Text (Simple Object Access Protocol) zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules-Anforderung,** die eine Regel ändert. 
  
### <a name="code"></a>Code

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

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a>UpdateInboxRules (Delete Rule)-Anforderungsbeispiel

Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange Zu löschen. Verwenden Sie [UpdateInboxRules](updateinboxrules.md) in Verbindung mit dem [DeleteRuleOperation-Element,](deleteruleoperation.md) um eine Regel zu löschen. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt die Anforderungs-XML und sendet sie an den Server.
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Comments

In diesem Beispiel wird die vorhandene identifizierte Regel gelöscht.
  
### <a name="request-elements"></a>Anfordern von Elementen

Die **UpdateInboxRules-Anforderung** enthält die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
Das [Operations-Element](operations.md) enthält das [DeleteRuleOperation-Element,](deleteruleoperation.md) um eine Regel zu löschen. 
  
## <a name="updateinboxrules-delete-rule-response-example"></a>UpdateInboxRules (Delete Rule)-Antwortbeispiel

### <a name="description"></a>Beschreibung

Der folgende SOAP-Textkörper (Simple Object Access Protocol) zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules-Anforderung,** die eine Regel löscht. 
  
### <a name="code"></a>Code

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

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="see-also"></a>Siehe auch



[GetInboxRules-Vorgang](getinboxrules-operation.md)

