---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: Das ConnectingSID-Element stellt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.
ms.openlocfilehash: 6e0bb90e197ce22bcd982a6d51954a88f3a2cf03
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757604"
---
# <a name="connectingsid"></a><span data-ttu-id="f6dec-103">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="f6dec-103">ConnectingSID</span></span>

<span data-ttu-id="f6dec-104">Das **ConnectingSID** -Element stellt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="f6dec-104">The **ConnectingSID** element represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span> 
  
[<span data-ttu-id="f6dec-105">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="f6dec-105">ExchangeImpersonation</span></span>](exchangeimpersonation.md)
  
[<span data-ttu-id="f6dec-106">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="f6dec-106">ConnectingSID</span></span>](connectingsid.md)
  
```xml
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

 <span data-ttu-id="f6dec-107">**ConnectingSIDType**</span><span class="sxs-lookup"><span data-stu-id="f6dec-107">**ConnectingSIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6dec-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f6dec-108">Attributes and elements</span></span>

<span data-ttu-id="f6dec-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f6dec-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6dec-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f6dec-110">Attributes</span></span>

<span data-ttu-id="f6dec-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6dec-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6dec-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6dec-112">Child elements</span></span>

|<span data-ttu-id="f6dec-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6dec-113">**Element**</span></span>|<span data-ttu-id="f6dec-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6dec-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6dec-115">' PrincipalName '</span><span class="sxs-lookup"><span data-stu-id="f6dec-115">PrincipalName</span></span>](principalname.md) <br/> |<span data-ttu-id="f6dec-116">Stellt den Benutzerprinzipalnamen (UPN) des Kontos, das für den Identitätswechsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dec-116">Represents the user principal name (UPN) of the account to use for impersonation.</span></span> <span data-ttu-id="f6dec-117">Dies sollte dem UPN für die Domäne sein, wenn das Benutzerkonto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f6dec-117">This should be the UPN for the domain where the user account exists.</span></span>  <br/> |
|[<span data-ttu-id="f6dec-118">SID</span><span class="sxs-lookup"><span data-stu-id="f6dec-118">SID</span></span>](sid.md) <br/> |<span data-ttu-id="f6dec-119">Stellt Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID) für das Konto für den Identitätswechsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dec-119">Represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation.</span></span>  <br/> |
|[<span data-ttu-id="f6dec-120">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="f6dec-120">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="f6dec-121">Stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse des Kontos, das für den Exchange-Identitätswechsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dec-121">Represents the primary Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange impersonation.</span></span> <span data-ttu-id="f6dec-122">Wenn die primäre SMTP-Adresse angegeben ist, wird es keinen zusätzlichen Active Directory Directory Service Nachschlagen Kosten, um die SID des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f6dec-122">If the primary SMTP address is supplied, it will cost an extra Active Directory directory service lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="f6dec-123">Es wird empfohlen, dass Sie die SID- oder UPN verwenden, sofern er verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f6dec-123">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
|[<span data-ttu-id="f6dec-124">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="f6dec-124">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="f6dec-125">Stellt die Simple Mail Transfer Protocol (SMTP)-Adresse des Kontos, das für den Exchange-Identitätswechsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6dec-125">Represents the Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange Impersonation.</span></span> <span data-ttu-id="f6dec-126">Wenn die SMTP-Adresse angegeben ist, wird es eine zusätzliche Active Directory-Suche, um die SID des Benutzers abzurufen Kosten.</span><span class="sxs-lookup"><span data-stu-id="f6dec-126">If the SMTP address is supplied, it will cost an extra Active Directory lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="f6dec-127">Es wird empfohlen, dass Sie die SID- oder UPN verwenden, sofern er verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f6dec-127">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f6dec-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6dec-128">Parent elements</span></span>

|<span data-ttu-id="f6dec-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6dec-129">**Element**</span></span>|<span data-ttu-id="f6dec-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6dec-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6dec-131">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="f6dec-131">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f6dec-132">In den SOAP-Header einer Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6dec-132">Used in the SOAP header of a request.</span></span> <span data-ttu-id="f6dec-133">Wenn dieses Element vorhanden ist, versucht der Aufrufer, das Benutzerkonto zu imitieren, das in der **"ExchangeImpersonation"** -Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f6dec-133">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span>  <br/> <span data-ttu-id="f6dec-134">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f6dec-134">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6dec-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6dec-135">Remarks</span></span>

<span data-ttu-id="f6dec-136">Das aufrufende Konto muss die **ms-Exch-Impersonation** direkt auf dem Clientzugriffsserver und das **ms-Exch-MayImpersonate** Recht auf entweder haben die Postfachdatenbank, die das Postfach Identität enthält oder den Active Directory-Benutzer oder Kontakt -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f6dec-136">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory user or contact object.</span></span> 
  
<span data-ttu-id="f6dec-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f6dec-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6dec-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f6dec-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6dec-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6dec-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6dec-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f6dec-140">Schema name</span></span>  <br/> |<span data-ttu-id="f6dec-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f6dec-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="f6dec-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f6dec-142">Validation file</span></span>  <br/> |<span data-ttu-id="f6dec-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f6dec-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6dec-144">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f6dec-144">Can be empty</span></span>  <br/> |<span data-ttu-id="f6dec-145">False</span><span class="sxs-lookup"><span data-stu-id="f6dec-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6dec-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6dec-146">See also</span></span>



[<span data-ttu-id="f6dec-147">Server-zu-Server-Autorisierung in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="f6dec-147">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

