---
title: Identifizieren des Kontos für Identitätswechsel
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: c7749f12-b97f-48d9-88e5-a545e108efb0
description: Informationen zur Verwendung von EWS durch Dienstanwendungen zum Identifizieren des Benutzers für den Identitätswechsel.
localization_priority: Priority
ms.openlocfilehash: 7159707abe96632aba2ed70dc0057417e087349f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527992"
---
# <a name="identify-the-account-to-impersonate"></a><span data-ttu-id="deb56-103">Identifizieren des Kontos für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="deb56-103">Identify the account to impersonate</span></span>

<span data-ttu-id="deb56-104">Informationen zur Verwendung von EWS durch Dienstanwendungen zum Identifizieren des Benutzers für den Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="deb56-104">Learn how your service application uses EWS to identify the user to impersonate.</span></span>
  
<span data-ttu-id="deb56-105">Die Dienstanwendung identifiziert das Benutzerkonto für den Identitätswechsel mithilfe eines der folgenden drei Kennungen:</span><span class="sxs-lookup"><span data-stu-id="deb56-105">Your service application identifies the user account to impersonate by using one of the following three identifiers:</span></span>
  
- <span data-ttu-id="deb56-106">Die primäre SMTP-Adresse</span><span class="sxs-lookup"><span data-stu-id="deb56-106">The primary SMTP address.</span></span>
    
- <span data-ttu-id="deb56-107">Der Benutzerprinzipalname (User Principal Name, UPN).</span><span class="sxs-lookup"><span data-stu-id="deb56-107">The user principal name (UPN).</span></span>
    
- <span data-ttu-id="deb56-108">Die Sicherheits-ID (SID)</span><span class="sxs-lookup"><span data-stu-id="deb56-108">The security identifier (SID).</span></span>
    
<span data-ttu-id="deb56-109">Die Kennung, die Sie verwenden, hängt von den Informationen ab, die Ihrer Anwendung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="deb56-109">The identifier that you use depends, of course, on the information that your application has available.</span></span>
  
## <a name="identifying-the-user-account-to-impersonate"></a><span data-ttu-id="deb56-110">Identifizieren des Benutzerkontos für den Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="deb56-110">Identifying the user account to impersonate</span></span>

<span data-ttu-id="deb56-p101">Die Anwendung kann die EWS Managed API oder EWS SOAP-Anforderungen zum Identifizieren des Benutzerkontos für einen Identitätswechsel verwenden. Die EWS Managed API verwendet die [ExchangeService.ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx)-Eigenschaft zum Identifizieren des Benutzers für den Identitätswechsel. EWS verwendet das [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)-Element, wie im folgenden XML-Ausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="deb56-p101">Your application can use either the EWS Managed API or EWS SOAP requests to identify the user account that it is impersonating. The EWS Managed API uses the [ExchangeService.ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property to identify the impersonated user. EWS uses the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) element, as shown in the following XML fragment.</span></span> 
  
```XML
<soap:Header>
    <t:ExchangeImpersonation>
        <t:ConnectingSID>
            Identifier
        </t:ConnectingSID>
    </t:ExchangeImpersonation>
</soap:Header>
```

<span data-ttu-id="deb56-114">Jeder der folgenden Abschnitte veranschaulicht jeweils die Verwendung einer Kennung.</span><span class="sxs-lookup"><span data-stu-id="deb56-114">Each of the following sections shows how to use one of the identifiers.</span></span> <span data-ttu-id="deb56-115">Ein Beispiel für die Anwendung der Identitätswechselkennung finden Sie unter [Hinzufügen von Terminen mit Exchange-Identitätswechsel](how-to-add-appointments-by-using-exchange-impersonation.md).</span><span class="sxs-lookup"><span data-stu-id="deb56-115">For an example that shows the impersonation identifier in action, see [Add appointments by using Exchange impersonation](how-to-add-appointments-by-using-exchange-impersonation.md).</span></span>
  
### <a name="use-the-smtp-email-address-to-identify-the-user-account"></a><span data-ttu-id="deb56-116">Verwenden der SMTP-E-Mail-Adresse zum Identifizieren des Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="deb56-116">Use the SMTP email address to identify the user account</span></span>

<span data-ttu-id="deb56-117">Die SMTP-E-Mail-Adresse ist die primäre E-Mail-Adresse, die mit einem Benutzerkonto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="deb56-117">The SMTP email address is the primary email address that is associated with a user account.</span></span>
  
<span data-ttu-id="deb56-118">Geben Sie in einer EWS Managed API-Anwendung die SMTP-E-Mail-Adresse zusammen mit dem [ConnectingIdType.SMTP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)-Enumerationswert an.</span><span class="sxs-lookup"><span data-stu-id="deb56-118">In an EWS Managed API application, you specify the SMTP email address along with the [ConnectingIdType.SMTP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SMTP, "alisa@contoso.com");
```

<span data-ttu-id="deb56-119">In einer EWS SOAP-Anwendung enthält das [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx)-Element die E-Mail-Adresse für das Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="deb56-119">In an EWS SOAP request, the [PrimarySmtpAddress](https://msdn.microsoft.com/library/eee79904-9412-4e61-b9b8-aff0ce25fade%28Office.15%29.aspx) element contains the email address for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrimarySmtpAddress>alisa@contoso.com</t: PrimarySmtpAddress>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-upn-to-identify-the-user-account"></a><span data-ttu-id="deb56-120">Verwenden des Benutzerprinzipalnamens zum Identifizieren des Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="deb56-120">Use the UPN to identify the user account</span></span>

<span data-ttu-id="deb56-121">Der Benutzerprinzipalname enthält den vollqualifizierten Domänenname (FQDN) für den Speicherort des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="deb56-121">The UPN contains the fully qualified domain name (FQDN) for the location of the user account.</span></span> <span data-ttu-id="deb56-122">Dies ist nicht notwendigerweise die Postfachdomäne des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="deb56-122">This is not necessarily the user's mailbox domain.</span></span> <span data-ttu-id="deb56-123">Das **userPrincipalName** -Attribut muss für das Benutzerkonto in Active Directory-Domänendienste (AD DS) ordnungsgemäß festgelegt sein, damit die Benutzersuche erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="deb56-123">The **UserPrincipalName** attribute must be set correctly on the user account in Active Directory Domain Services (AD DS) for the user lookup to succeed.</span></span> 
  
<span data-ttu-id="deb56-124">In einer verwaltete EWS-API Anwendung geben Sie den UPN zusammen mit dem Aufzählungswert [ConnectingIdType. PrincipalName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) an.</span><span class="sxs-lookup"><span data-stu-id="deb56-124">In an EWS Managed API application, you specify the UPN along with the [ConnectingIdType.PrincipalName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.PrincipalName, "alias@billing.contoso.com");
```

<span data-ttu-id="deb56-125">In einer EWS SOAP-Anwendung enthält das [PrincipalName element (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md)-Element den Benutzerprinzipalnamen für das Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="deb56-125">In an EWS SOAP request, the [PrincipalName element (ConnectingSIDType complexType) (EWS)](../web-service-reference/principalname.md) element contains the UPN for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:PrincipalName>alisa@billing.contoso.com</t:PrincipalName>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

### <a name="use-the-sid-to-identify-the-user-account"></a><span data-ttu-id="deb56-126">Verwenden der SID zum Identifizieren des Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="deb56-126">Use the SID to identify the user account</span></span>

<span data-ttu-id="deb56-127">Die SID ist die ID des Kontos, dessen Identität angenommen wird, im SDDL-Format (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="deb56-127">The SID is the identifier of the account to be impersonated in security descriptor definition language (SDDL) form.</span></span>
  
<span data-ttu-id="deb56-128">Geben Sie in einer EWS Managed API-Anwendung die SID zusammen mit dem [ConnectingIdType.SID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx)-Enumerationswert an.</span><span class="sxs-lookup"><span data-stu-id="deb56-128">In an EWS Managed API application, you specify the SID along with the [ConnectingIdType.SID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.connectingidtype.aspx) enumeration value.</span></span> 
  
```cs
exchangeServiceInstance.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SID, "S-1-5-21-1493619105-1843311271-3936346804-1118");
```

<span data-ttu-id="deb56-129">In einer EWS SOAP-Anforderung enthält das [SID](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx)-Element die SID für das Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="deb56-129">In an EWS SOAP request, the [SID](https://msdn.microsoft.com/library/2f33b29b-163b-4106-a74d-6fb76ec38951%28Office.15%29.aspx) element contains the SID for the user account.</span></span> 
  
```XML
<soap:Header>
  <t:ExchangeImpersonation>
    <t:ConnectingSID>
      <t:SID>S-1-5-21-1493619105-1843311271-3936346804-1118</t:SID>
    </t:ConnectingSID>
  </t:ExchangeImpersonation>
</soap:Header>
```

## <a name="see-also"></a><span data-ttu-id="deb56-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="deb56-130">See also</span></span>


- [<span data-ttu-id="deb56-131">Identitätswechsel und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="deb56-131">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="deb56-132">Hinzufügen von Terminen mit Exchange-Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="deb56-132">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
- [<span data-ttu-id="deb56-133">ExchangeService-Klasse</span><span class="sxs-lookup"><span data-stu-id="deb56-133">ExchangeService class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx)
    
- [<span data-ttu-id="deb56-134">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="deb56-134">ExchangeImpersonation</span></span>](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)
    

