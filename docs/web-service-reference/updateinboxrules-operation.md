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
# <a name="updateinboxrules-operation"></a>UpdateInboxRules-Vorgang

Der Vorgang UpdateInboxRules aktualisiert Posteingangsregeln des authentifizierten Benutzers durch die angegebenen Vorgänge anwenden. **UpdateInboxRules** wird verwendet, um eine Posteingangsregel zu, um eine Posteingangsregel festzulegen oder löschen Sie eine Posteingangsregel zu erstellen. 
  
Wenn Sie den Vorgang **UpdateInboxRules** verwenden, löscht Exchange-Webdienste senden mithilfe der clientseitigen Regeln. Senden clientseitige Regeln werden auf dem Client in der Regel Ordner verknüpften Informationen (FAI)-Nachricht und keiner anderen gespeichert. EWS löscht diese Regel FAI Nachricht standardmäßig basierend auf der Annahme, dass Outlook wird neu erstellt wird. Allerdings Outlook kann nicht erstellen Regeln, die auch als eine erweiterte Regel vorhanden, nicht erneut, und Senden mithilfe der clientseitigen Regeln nicht als erweiterte Regeln vorhanden sind. Daher sind diese Regeln verloren. Es wird empfohlen, dass Sie dies berücksichtigen Sie beim Entwerfen Ihrer Lösung. 
  
## <a name="updateinboxrules-create-rule-request-example"></a>Anforderungsbeispiel UpdateInboxRules (Regel erstellen)

Exchange-Webdienste können Sie um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Speicher zu erstellen. Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel erstellen. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt die Anforderung XML und sendet es an den Server.
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Kommentare

Dieses Beispiel erstellt eine Regel, die eine E-mail-Nachricht in den Junk-e-Mail-Ordner verschoben werden, wenn der e-Mail-Betreff eine Zeichenfolge, die enthält "Interessanter" entspricht.
  
### <a name="request-elements"></a>Anfordern von Elementen

Die Anforderung **UpdateInboxRules** umfasst die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Betrieb](operations.md)
    
Das [Vorgänge](operations.md) Element enthält das [CreateRuleOperation](createruleoperation.md) -Element, um eine Regel zu erstellen. 
  
## <a name="updateinboxrules-create-rule-response-example"></a>Antwortbeispiel UpdateInboxRules (Regel erstellen)

### <a name="description"></a>Beschreibung

Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel erstellt. 
  
### <a name="code"></a>Code

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

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a>Anforderungsbeispiel UpdateInboxRules (Rule festgelegt)

Exchange-Webdienste können Sie um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Speicher zu ändern. Verwenden Sie das [UpdateInboxRules](updateinboxrules.md) -Element in Verbindung mit dem [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt die Anforderung XML und sendet es an den Server.
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Kommentare

In diesem Beispiel wird der Anzeigename auf "(geändert) Hierbei handelt es sich um Junk-e-".
  
> [!NOTE]
> Die Werte der **Id** und **ChangeKey** Attribute des Elements [FolderId](folderid.md) wurden zur besseren Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

Die Anforderung **UpdateInboxRules** umfasst die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Betrieb](operations.md)
    
Das [Vorgänge](operations.md) Element enthält das [SetRuleOperation](setruleoperation.md) -Element, um eine Regel zu ändern. 
  
## <a name="updateinboxrules-set-rule-response-example"></a>Antwortbeispiel UpdateInboxRules (Rule festgelegt)

### <a name="description"></a>Beschreibung

Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel ändert. 
  
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

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a>Anforderungsbeispiel UpdateInboxRules (Regel löschen)

Exchange-Webdienste können Sie um eine Posteingangsregel im Postfach eines Benutzers im Exchange-Speicher zu löschen. Verwenden Sie die [UpdateInboxRules](updateinboxrules.md) in Verbindung mit dem [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen. 
  
### <a name="description"></a>Beschreibung

Der Client erstellt die Anforderung XML und sendet es an den Server.
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Kommentare

Dieses Beispiel löscht die vorhandene identifizierte Regel.
  
### <a name="request-elements"></a>Anfordern von Elementen

Die Anforderung **UpdateInboxRules** umfasst die folgenden Elemente: 
  
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
- [RemoveOutlookRuleBlob](removeoutlookruleblob.md)
    
- [Betrieb](operations.md)
    
Das [Vorgänge](operations.md) Element enthält das [DeleteRuleOperation](deleteruleoperation.md) -Element, um eine Regel zu löschen. 
  
## <a name="updateinboxrules-delete-rule-response-example"></a>Antwortbeispiel UpdateInboxRules (Regel löschen)

### <a name="description"></a>Beschreibung

Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **UpdateInboxRules** -Anforderung, die eine Regel wird gelöscht. 
  
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

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateInboxRulesResponse](updateinboxrulesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="see-also"></a>Siehe auch



[GetInboxRules-Vorgang](getinboxrules-operation.md)

