---
title: GetDelegate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 849b2c9e-4685-4bd1-9adb-aba0fcc52650
description: Der GetDelegate-Vorgang ruft die Stellvertretungseinstellungen für ein angegebenes Postfach ab.
ms.openlocfilehash: ce11838944d30021f65b51eae817a6b3543e3ae8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544978"
---
# <a name="getdelegate-operation"></a>GetDelegate-Vorgang

Der **GetDelegate-Vorgang** ruft die Stellvertretungseinstellungen für ein angegebenes Postfach ab. 
  
## <a name="soap-headers"></a>SOAP-Header

Der **GetDelegate-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben sind. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Identitätswechsel  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.  <br/> |
   
## <a name="getdelegate-request-example"></a>GetDelegate-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt, wie Sie die Stellvertretungseinstellungen für alle Stellvertretungen abrufen, die für das Postfach von Benutzer3 festgelegt sind. Alle Berechtigungen für jeden Benutzer werden in der Antwort zurückgegeben.
  
### <a name="code"></a>Code

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

### <a name="comments"></a>Comments

Sie können das [UserId-Element](userid.md) verwenden, um einzelne Benutzer anzugeben, anstatt alle Benutzer zurückzugeben, die über Stellvertretungszugriffsberechtigungen für das Postfach verfügen. 
  
> [!NOTE]
> Exchange Web Services (EWS) unterstützt das Verwalten von Gruppendelegats nicht. EWS gibt einen Fehler zurück, wenn der **GetDelegate-Vorgang** für einen Prinzipal aufgerufen wird, der über einen Sicherheitsgruppendelegat verfügt. 
  
## <a name="getdelegate-response-example"></a>GetDelegate-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **GetDelegate-Antwort** zeigt eine erfolgreiche Antwort auf eine **GetDelegate-Anforderung.** Die Antwort enthält Informationen über die Stellvertretungszugriffsberechtigungen, ob der Stellvertreter private Elemente anzeigen kann, ob die Stellvertretung Kopien von Besprechungsnachrichten empfängt und an wen Besprechungsanfragen übermittelt wurden. 
  
### <a name="code"></a>Code

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

## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

