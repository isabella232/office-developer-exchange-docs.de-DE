---
title: Identifizieren Sie das Konto Identität
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c7749f12-b97f-48d9-88e5-a545e108efb0
description: Informationen zur Verwendung von EWS durch Dienstanwendungen zum Identifizieren des Benutzers für den Identitätswechsel.
ms.openlocfilehash: 78df4b511a9947d4d815b2802a53ab178b14622b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756899"
---
# <a name="identify-the-account-to-impersonate"></a>Identifizieren Sie das Konto Identität

Informationen zur Verwendung von EWS durch Dienstanwendungen zum Identifizieren des Benutzers für den Identitätswechsel.
  
Die Dienstanwendung identifiziert das Benutzerkonto für den Identitätswechsel mithilfe eines der folgenden drei Kennungen:
  
- Die primäre SMTP-Adresse
    
- Der Benutzerprinzipalname (User Principle Name, UPN)
    
- Die Sicherheits-ID (SID)
    
Die Kennung, die Sie verwenden, hängt von den Informationen ab, die Ihrer Anwendung zur Verfügung stehen.
  
## <a name="identifying-the-user-account-to-impersonate"></a>Identifizieren des Benutzerkontos für den Identitätswechsel

Die Anwendung kann die EWS Managed API oder EWS SOAP-Anforderungen zum Identifizieren des Benutzerkontos für einen Identitätswechsel verwenden. Die EWS Managed API verwendet die [ExchangeService.ImpersonatedUserId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)-Eigenschaft zum Identifizieren des Benutzers für den Identitätswechsel. EWS verwendet das [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)-Element, wie im folgenden XML-Ausschnitt dargestellt. 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

Jeder der folgenden Abschnitte veranschaulicht jeweils die Verwendung einer Kennung. Ein Beispiel, das den Bezeichner des Identitätswechsels in der Praxis anzeigt, finden Sie unter [Hinzufügen von Terminen mithilfe der Exchange-Identitätswechsel](how-to-add-appointments-by-using-exchange-impersonation.md).
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a>Verwenden der SMTP-E-Mail-Adresse zum Identifizieren des Benutzerkontos

Die SMTP-E-Mail-Adresse ist die primäre E-Mail-Adresse, die mit einem Benutzerkonto verknüpft ist.
  
Geben Sie in einer EWS Managed API-Anwendung die SMTP-E-Mail-Adresse zusammen mit dem [ConnectingIdType.SMTP](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)-Enumerationswert an. 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

In einer EWS SOAP-Anwendung enthält das [PrimarySmtpAddress](http://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx)-Element die E-Mail-Adresse für das Benutzerkonto. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a>Verwenden des Benutzerprinzipalnamens zum Identifizieren des Benutzerkontos

Der Benutzerprinzipalname enthält den vollqualifizierten Domänenname (FQDN) für den Speicherort des Benutzerkontos. Dies ist nicht notwendigerweise die Postfachdomäne des Benutzers. Das **UserPrincipleName**-Attribut muss korrekt auf das Benutzerkonto in Active Directory-Domänendiensten (AD DS) festgelegt werden, damit die Benutzersuche erfolgreich ausgeführt werden kann. 
  
Geben Sie in einer EWS Managed API-Anwendung den Benutzerprinzipalnamen zusammen mit dem [ConnectingIdType.PrincipleName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)-Enumerationswert an. 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipleName, "alias@billing.contoso.com");
```

In einer EWS SOAP-Anwendung enthält das [PrincipalName element (ConnectingSIDType complexType) (EWS)](http://msdn.microsoft.com/library/6aac5388-c971-817b-b0bb-095a2639c6de%28Office.15%29.aspx)-Element den Benutzerprinzipalnamen für das Benutzerkonto. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a>Verwenden der SID zum Identifizieren des Benutzerkontos

Die SID ist die ID des Kontos, dessen Identität angenommen wird, im SDDL-Format (Security Descriptor Definition Language).
  
Geben Sie in einer EWS Managed API-Anwendung die SID zusammen mit dem [ConnectingIdType.SID](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.connectingidtype.aspx)-Enumerationswert an. 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

In einer EWS SOAP-Anforderung enthält das [SID](http://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx)-Element die SID für das Benutzerkonto. 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a>Siehe auch


- [Identitätswechsel und EWS in Exchange](impersonation-and-ews-in-exchange.md)
    
- [Hinzufügen von Terminen mithilfe der Exchange-Identitätswechsel](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [ExchangeService-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- ["ExchangeImpersonation"](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    

