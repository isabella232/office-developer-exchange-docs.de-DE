---
title: POX-AutoErmittlungsantwort für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 08c6c5a2-a67a-4141-a8bd-1b5d560b90a7
description: Die Antwort der AutoErmittlung enthält eine Antwort auf die AutoErmittlung-Anforderung, die eine Liste der URLs enthält, die zum Erstellen einer Bindung zu den Exchange-Webdiensten verwendet werden.
ms.openlocfilehash: 42705856a28a1b5e595e55ab3f77f78089a1ee21
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527900"
---
# <a name="pox-autodiscover-response-for-exchange"></a>POX-AutoErmittlungsantwort für Exchange

Die Antwort der AutoErmittlung enthält eine Antwort auf die AutoErmittlung-Anforderung, die eine Liste der URLs enthält, die zum Erstellen einer Bindung zu den Exchange-Webdiensten verwendet werden.
  
## <a name="autodiscover-response-example"></a>AutoErmittlung-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel ist eine erfolgreiche AutoErmittlung-Antwort dargestellt.
  
### <a name="code"></a>Code

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>First Last</DisplayName>
      <LegacyDN>/o=contoso/ou=First Administrative Group/cn=Recipients/cn=iuser885646</LegacyDN>
      <DeploymentId>644560b8-a1ce-429c-8ace-23395843f701</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>MBX-SERVER.mail.internal.contoso.com</Server>
        <ServerDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER</ServerDN>
        <ServerVersion>72008287</ServerVersion>
        <MdbDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER/cn=Microsoft Private MDB</MdbDN>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>Exchange.contoso.com</Server>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-01-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-02-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Basic">https://cas-04-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-05-server.mail.internal.contoso.com/owa</OWAUrl>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

### <a name="comments"></a>Comments

Verwenden Sie zum Erstellen einer Bindung zu den Exchange-Webdiensten die vom [ASUrl (POX)](asurl-pox.md)-Element identifizierte URL. 
  
### <a name="response-element"></a>Antwortelement

Folgende Elemente werden im Antworttext verwendet:
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
    
- [Response (POX)](response-pox.md)
    
- [Benutzer (POX)](user-pox.md)
    
- [DisplayName (POX)](displayname-pox.md)
    
- [LegacyDN (POX)](legacydn-pox.md)
    
- [DeploymentId (POX)](deploymentid-pox.md)
    
- [Konto (POX)](account-pox.md)
    
- [AccountType (POX)](accounttype-pox.md)
    
- [Aktion (POX)](action-pox.md)
    
- [Protokoll (POX)](protocol-pox.md)
    
- [Typ (POX)](type-pox.md)
    
- [Server (POX)](server-pox.md)
    
- [ServerDN (POX)](serverdn-pox.md)
    
- [ServerVersion (POX)](serverversion-pox.md)
    
- [MdbDN (POX)](mdbdn-pox.md)
    
- [ASUrl (POX)](asurl-pox.md)
    
- [OOFUrl (POX)](oofurl-pox.md)
    
- [UMUrl (POX)](umurl-pox.md)
    
- [OABUrl (POX)](oaburl-pox.md)
    
- [Interne (POX)](internal-pox.md)
    
- [OWAUrl (POX)](owaurl-pox.md)
    
## <a name="autodiscover-error-response-example"></a>Autoermittlung-Fehlerantwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel ist eine Fehlerantwort für die AutoErmittlung dargestellt.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
    <Error Time="21:25:04.8897083" Id="4130155072">
      <ErrorCode>600</ErrorCode>
      <Message>Invalid Request</Message>
      <DebugData />
    </Error>
  </Response>
</Autodiscover>
```

### <a name="error-response-element"></a>Fehlerantwortelement

In der Antwort werden folgende Elemente verwendet:
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
    
- [Response (POX)](response-pox.md)
    
- [Fehler (POX)](error-pox.md)
    
- [ErrorCode (POX)](errorcode-pox.md)
    
- [Nachricht (POX)](message-pox.md)
    
- [DebugData (POX)](debugdata-pox.md)
    
## <a name="see-also"></a>Siehe auch

- [POX-Anforderung der AutoErmittlung für Exchange](pox-autodiscover-request-for-exchange.md)
- [Referenz zum POX-AutoErmittlungwebdienst für Exchange](pox-autodiscover-web-service-reference-for-exchange.md) 
- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

