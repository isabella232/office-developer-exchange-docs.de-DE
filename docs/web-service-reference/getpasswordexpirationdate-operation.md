---
title: GetPasswordExpirationDate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: Der GetPasswordExpirationDate-Vorgang stellt das Ablaufdatum des Kennworts für das E-Mail-Konto für den aktuellen Benutzer bereit.
ms.openlocfilehash: 07928fd3e6fca410a292d6cd74f1240d8e81c42f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524238"
---
# <a name="getpasswordexpirationdate-operation"></a>GetPasswordExpirationDate-Vorgang

Der **GetPasswordExpirationDate-Vorgang** stellt das Ablaufdatum des Kennworts für das E-Mail-Konto für den aktuellen Benutzer bereit. 
  
Dieser Vorgang wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>SOAP-Header des GetPasswordExpirationDate-Vorgangs

Der **GetPasswordExpirationDate-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dies gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifiziert das Schema für die Vorgangsanforderung. Dies gilt für eine Anforderung. Dies gilt für eine Anforderung.  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>GetPasswordExpirationDate-Vorgangsanforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer **GetPasswordExpirationDate-Vorgangsanforderung** zeigt, wie das Kennwortablaufdatum für ein E-Mail-Konto abgerufen wird. 
  
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
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>Erfolgreiche GetPasswordExpirationDate-Vorgangsantwort

In der Antwort werden folgende Elemente verwendet:
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    

