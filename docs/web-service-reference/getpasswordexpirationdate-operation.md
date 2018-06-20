---
title: GetPasswordExpirationDate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: Der Vorgang GetPasswordExpirationDate enthält das Ablaufdatum des e-Mail-Konto ein Kennwort für den aktuellen Benutzer.
ms.openlocfilehash: c57942c88b09a910e2d529a12ea279bb2da5d693
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758758"
---
# <a name="getpasswordexpirationdate-operation"></a>GetPasswordExpirationDate-Vorgang

Der Vorgang **GetPasswordExpirationDate** enthält das Ablaufdatum des e-Mail-Konto ein Kennwort für den aktuellen Benutzer. 
  
Dieser Vorgang wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a>GetPasswordExpirationDate Vorgang SOAP-Header

Der Vorgang **GetPasswordExpirationDate** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Dies gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Das Schema für die Anforderung Vorgang identifiziert. Dies gilt für eine Anforderung. Dies gilt für eine Anforderung.  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a>GetPasswordExpirationDate Vorgang anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine **GetPasswordExpirationDate** Vorgang Anforderung veranschaulicht, wie das Ablaufdatum Kennwort für ein e-Mail-Konto abrufen. 
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a>Erfolgreiche GetPasswordExpirationDate Vorgangsantwort

In der Antwort werden folgende Elemente verwendet:
  
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
    
- [PasswordExpirationDate](passwordexpirationdate.md)
    

