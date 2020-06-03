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
description: Das ConnectingSID-Element stellt ein Konto für den Identitätswechsel dar, wenn Sie den ExchangeImpersonation-SOAP-Header verwenden.
ms.openlocfilehash: f4edf63f129fc769f4a2d710a505b40da4057fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459279"
---
# <a name="connectingsid"></a><span data-ttu-id="574de-103">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="574de-103">ConnectingSID</span></span>

<span data-ttu-id="574de-104">Das **ConnectingSID** -Element stellt ein Konto für den Identitätswechsel dar, wenn Sie den ExchangeImpersonation-SOAP-Header verwenden.</span><span class="sxs-lookup"><span data-stu-id="574de-104">The **ConnectingSID** element represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span> 
  
- [<span data-ttu-id="574de-105">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="574de-105">ExchangeImpersonation</span></span>](exchangeimpersonation.md) 
- [<span data-ttu-id="574de-106">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="574de-106">ConnectingSID</span></span>](connectingsid.md)
  
```xml
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

```xml
<ConnectingSID>
   <SmtpAddress/>
</ConnectingSID>
```

```xml
<ConnectingSID>
    <SID/> 
</ConnectingSID>
```

```xml
<ConnectingSID>
   <PrimarySmtpAddress/>
</ConnectingSID>
```

<span data-ttu-id="574de-107">**ConnectingSIDType**</span><span class="sxs-lookup"><span data-stu-id="574de-107">**ConnectingSIDType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="574de-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="574de-108">Attributes and elements</span></span>

<span data-ttu-id="574de-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="574de-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="574de-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="574de-110">Attributes</span></span>

<span data-ttu-id="574de-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="574de-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="574de-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="574de-112">Child elements</span></span>

|<span data-ttu-id="574de-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="574de-113">**Element**</span></span>|<span data-ttu-id="574de-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574de-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574de-115">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="574de-115">PrincipalName</span></span>](principalname.md) <br/> |<span data-ttu-id="574de-116">Stellt den Benutzerprinzipalnamen (User Principal Name, UPN) des Kontos dar, das für den Identitätswechsel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="574de-116">Represents the user principal name (UPN) of the account to use for impersonation.</span></span> <span data-ttu-id="574de-117">Dies sollte der UPN für die Domäne sein, in der das Benutzerkonto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="574de-117">This should be the UPN for the domain where the user account exists.</span></span>  <br/> |
|[<span data-ttu-id="574de-118">SID</span><span class="sxs-lookup"><span data-stu-id="574de-118">SID</span></span>](sid.md) <br/> |<span data-ttu-id="574de-119">Stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) für das Konto dar, das für den Identitätswechsel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="574de-119">Represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation.</span></span>  <br/> |
|[<span data-ttu-id="574de-120">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="574de-120">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="574de-121">Stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="574de-121">Represents the primary Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange impersonation.</span></span> <span data-ttu-id="574de-122">Wenn die primäre SMTP-Adresse angegeben wird, kostet Sie eine zusätzliche Active Directory Verzeichnisdienstsuche, um die SID des Benutzers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="574de-122">If the primary SMTP address is supplied, it will cost an extra Active Directory directory service lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="574de-123">Es wird empfohlen, die SID oder den UPN zu verwenden, wenn diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="574de-123">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
|[<span data-ttu-id="574de-124">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="574de-124">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="574de-125">Stellt die Simple Mail Transfer Protocol (SMTP) Adresse des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="574de-125">Represents the Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange Impersonation.</span></span> <span data-ttu-id="574de-126">Wenn die SMTP-Adresse angegeben wird, kostet Sie eine zusätzliche Active Directory Suche, um die SID des Benutzers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="574de-126">If the SMTP address is supplied, it will cost an extra Active Directory lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="574de-127">Es wird empfohlen, die SID oder den UPN zu verwenden, wenn diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="574de-127">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="574de-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="574de-128">Parent elements</span></span>

|<span data-ttu-id="574de-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="574de-129">**Element**</span></span>|<span data-ttu-id="574de-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574de-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574de-131">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="574de-131">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="574de-132">Wird im SOAP-Header einer Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="574de-132">Used in the SOAP header of a request.</span></span> <span data-ttu-id="574de-133">Wenn dieses Element vorhanden ist, versucht der Aufrufer, das im **ExchangeImpersonation** -Element enthaltene Konto zu imitieren.</span><span class="sxs-lookup"><span data-stu-id="574de-133">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span>  <br/> <span data-ttu-id="574de-134">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="574de-134">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="574de-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="574de-135">Remarks</span></span>

<span data-ttu-id="574de-136">Das Anruf Konto muss über das Recht **MS-Wechsel-Wechsel** auf dem Client Zugriffsserver und das **MS-MayImpersonate** direkt in der Postfachdatenbank, die das Postfach enthält, den Identitätswechsel oder das Active Directory Benutzer-oder Kontaktobjekt aufweisen.</span><span class="sxs-lookup"><span data-stu-id="574de-136">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory user or contact object.</span></span> 
  
<span data-ttu-id="574de-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="574de-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="574de-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="574de-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="574de-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="574de-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="574de-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="574de-140">Schema name</span></span>  <br/> |<span data-ttu-id="574de-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="574de-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="574de-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="574de-142">Validation file</span></span>  <br/> |<span data-ttu-id="574de-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="574de-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="574de-144">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="574de-144">Can be empty</span></span>  <br/> |<span data-ttu-id="574de-145">False</span><span class="sxs-lookup"><span data-stu-id="574de-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="574de-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="574de-146">See also</span></span>

- [<span data-ttu-id="574de-147">Server-zu-Server-Autorisierung in EWS</span><span class="sxs-lookup"><span data-stu-id="574de-147">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

