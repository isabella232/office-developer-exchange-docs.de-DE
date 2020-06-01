---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: Das PrimarySmtpAddress-Element stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für die Server-zu-Server-Autorisierung oder den Stellvertretungszugriff verwendet werden soll.
ms.openlocfilehash: eea995b3e546d7e94e65cf9b230b639a781c4928
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467963"
---
# <a name="primarysmtpaddress"></a><span data-ttu-id="6ae4d-103">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="6ae4d-103">PrimarySmtpAddress</span></span>

<span data-ttu-id="6ae4d-104">Das **PrimarySmtpAddress** -Element stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für die Server-zu-Server-Autorisierung oder den Stellvertretungszugriff verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-104">The **PrimarySmtpAddress** element represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization or delegate access.</span></span> 
  
```xml
<PrimarySmtpAddress/>
```

 <span data-ttu-id="6ae4d-105">**PrimarySmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="6ae4d-105">**PrimarySmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ae4d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6ae4d-106">Attributes and elements</span></span>

<span data-ttu-id="6ae4d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ae4d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ae4d-108">Attributes</span></span>

<span data-ttu-id="6ae4d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ae4d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ae4d-110">Child elements</span></span>

<span data-ttu-id="6ae4d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6ae4d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ae4d-112">Parent elements</span></span>

|<span data-ttu-id="6ae4d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ae4d-113">**Element**</span></span>|<span data-ttu-id="6ae4d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ae4d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ae4d-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="6ae4d-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="6ae4d-116">Stellt ein Konto für den Identitätswechsel dar, wenn Sie den SOAP-ExchangeImpersonation-Header verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="6ae4d-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="6ae4d-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="6ae4d-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="6ae4d-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="6ae4d-119">Wird im SOAP-Header für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span>  <br/> |
|[<span data-ttu-id="6ae4d-120">UserId</span><span class="sxs-lookup"><span data-stu-id="6ae4d-120">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="6ae4d-121">Identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-121">Identifies a delegate user or a user who has folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6ae4d-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="6ae4d-122">Text value</span></span>

<span data-ttu-id="6ae4d-123">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-123">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ae4d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ae4d-124">Remarks</span></span>

<span data-ttu-id="6ae4d-125">Exchange Webdienste erfordert, dass Postfächer von der primären SMTP-Adresse des Postfachs identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-125">Exchange Web Services requires that mailboxes be identified by the primary SMTP address of the mailbox.</span></span> <span data-ttu-id="6ae4d-126">Proxy-oder alternative Adressen werden nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-126">Proxy or alternative addresses are not accepted.</span></span>
  
<span data-ttu-id="6ae4d-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ae4d-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ae4d-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6ae4d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ae4d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ae4d-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6ae4d-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6ae4d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="6ae4d-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6ae4d-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="6ae4d-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6ae4d-132">Validation File</span></span>  <br/> |<span data-ttu-id="6ae4d-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6ae4d-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6ae4d-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6ae4d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ae4d-135">False</span><span class="sxs-lookup"><span data-stu-id="6ae4d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ae4d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ae4d-136">See also</span></span>



- [<span data-ttu-id="6ae4d-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6ae4d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6ae4d-138">Server-zu-Server-Autorisierung in EWS</span><span class="sxs-lookup"><span data-stu-id="6ae4d-138">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[<span data-ttu-id="6ae4d-139">Arbeiten mit Stellvertretungszugriff</span><span class="sxs-lookup"><span data-stu-id="6ae4d-139">Working with Delegate Access</span></span>](https://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

