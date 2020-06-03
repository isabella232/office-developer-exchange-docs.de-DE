---
title: GetPasswordExpirationDate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: Der GetPasswordExpirationDate-Vorgang stellt das Ablaufdatum des e-Mail-Kontokennworts für den aktuellen Benutzer bereit.
ms.openlocfilehash: 4184092cf98161e4c2f74446cef5439722ae71a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457893"
---
# <a name="getpasswordexpirationdate-operation"></a>GetPasswordExpirationDate-Vorgang

Der **GetPasswordExpirationDate** -Vorgang stellt das Ablaufdatum des e-Mail-Kontokennworts für den aktuellen Benutzer bereit. 
  
Dieser Vorgang wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>SOAP-Header des GetPasswordExpirationDate-Vorgangs

Der **GetPasswordExpirationDate** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen. Dies gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt das Schema für die Vorgangsanforderung an. Dies gilt für eine Anforderung. Dies gilt für eine Anforderung.  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>GetPasswordExpirationDate-Vorgangsanforderung (Beispiel)

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **GetPasswordExpirationDate** -Vorgangsanforderung wird gezeigt, wie das Kennwortablaufdatum für ein e-Mail-Konto abgerufen wird. 
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetPasswordExpirationDate](getpasswordexpirationdate.md)
    
- [MailboxSmtpAddress](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>Erfolgreiche Reaktion des GetPasswordExpirationDate-Vorgangs

In der Antwort werden folgende Elemente verwendet:
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    

