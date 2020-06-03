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
# <a name="updateinboxrules-operation"></a>UpdateInboxRules-Vorgang

Der UpdateInboxRules-Vorgang aktualisiert die Posteingangsregeln des authentifizierten Benutzers durch Anwenden der angegebenen Vorgänge. **UpdateInboxRules** wird verwendet, um eine Posteingangsregel zu erstellen, um eine Posteingangsregel festzulegen oder um eine Posteingangsregel zu löschen. 
  
Wenn Sie den **UpdateInboxRules** -Vorgang verwenden, löscht Exchange Webdienste clientseitige Sende Regeln. Clientseitige Sende Regeln werden auf dem Client in der FAI-Nachricht (Regel Ordner – zugeordnete Informationen) gespeichert und nirgendwo sonst. In EWS wird diese Regel "fai" standardmäßig gelöscht, basierend auf der Erwartung, dass Outlook Sie neu erstellt. Outlook kann jedoch keine Regeln neu erstellen, die nicht auch als erweiterte Regel vorhanden sind, und clientseitige Sende Regeln sind nicht als erweiterte Regeln vorhanden. Daher gehen diese Regeln verloren. Wir empfehlen, dies beim Entwerfen der Lösung zu berücksichtigen. 
  
## <a name="updateinboxrules-create-rule-request-example"></a>UpdateInboxRules (Create Rule)-Anforderungs Beispiel

Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Informationsspeicher zu erstellen. Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel zu erstellen. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt den Anforderungs-XML-Code und sendet ihn an den Server.
  
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

In diesem Beispiel wird eine Regel erstellt, die eine e-Mail-Nachricht in den Ordner Junk-e-Mail verschiebt, wenn der e-Mail-Betreff eine Zeichenfolge enthält, die "interessant" entspricht.
  
### <a name="request-elements"></a>Anfordern von Elementen

Die **UpdateInboxRules** -Anforderung umfasst die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
Das [Operations](operations.md) -Element enthält das [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel zu erstellen. 
  
## <a name="updateinboxrules-create-rule-response-example"></a>UpdateInboxRules (Create Rule)-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel erstellt. 
  
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
    
## <a name="updateinboxrules-set-rule-request-example"></a>UpdateInboxRules (Regel festlegen)-Anforderungs Beispiel

Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Informationsspeicher zu ändern. Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt den Anforderungs-XML-Code und sendet ihn an den Server.
  
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

In diesem Beispiel wird der Anzeigename in "(geändert) this is Junk" geändert.
  
> [!NOTE]
> Die Werte der Attribute **ID** und **ChangeKey** des [Folder](folderid.md) -Elements wurden zur Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

Die **UpdateInboxRules** -Anforderung umfasst die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
Das [Operations](operations.md) -Element enthält das [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern. 
  
## <a name="updateinboxrules-set-rule-response-example"></a>UpdateInboxRules (Regel festlegen)-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel ändert. 
  
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
    
## <a name="updateinboxrules-delete-rule-request-example"></a>UpdateInboxRules (Delete Rule)-Anforderungs Beispiel

Sie können Exchange Webdienste verwenden, um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Informationsspeicher zu löschen. Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) in Verbindung mit dem [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt den Anforderungs-XML-Code und sendet ihn an den Server.
  
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

In diesem Beispiel wird die vorhandene angegebene Regel gelöscht.
  
### <a name="request-elements"></a>Anfordern von Elementen

Die **UpdateInboxRules** -Anforderung umfasst die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Operations](operations.md)
    
Das [Operations](operations.md) -Element enthält das [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen. 
  
## <a name="updateinboxrules-delete-rule-response-example"></a>UpdateInboxRules (Delete Rule)-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Simple Object Access Protocol (SOAP) Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel löscht. 
  
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

