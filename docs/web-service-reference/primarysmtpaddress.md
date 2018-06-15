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
description: PrimarySmtpAddress-Element stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos Stellvertretungszugriff oder für die Server-zu-Server-Autorisierung verwendet werden.
ms.openlocfilehash: d33bf22af4ddf6b2f6d8d8d434168264acfaea7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19830881"
---
# <a name="primarysmtpaddress"></a><span data-ttu-id="9e370-103">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="9e370-103">PrimarySmtpAddress</span></span>

<span data-ttu-id="9e370-104">**PrimarySmtpAddress** -Element stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos Stellvertretungszugriff oder für die Server-zu-Server-Autorisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e370-104">The **PrimarySmtpAddress** element represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization or delegate access.</span></span> 
  
```xml
<PrimarySmtpAddress/>
```

 <span data-ttu-id="9e370-105">**PrimarySmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="9e370-105">**PrimarySmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e370-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9e370-106">Attributes and elements</span></span>

<span data-ttu-id="9e370-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e370-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e370-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e370-108">Attributes</span></span>

<span data-ttu-id="9e370-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e370-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e370-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e370-110">Child elements</span></span>

<span data-ttu-id="9e370-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e370-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9e370-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e370-112">Parent elements</span></span>

|<span data-ttu-id="9e370-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e370-113">**Element**</span></span>|<span data-ttu-id="9e370-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e370-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e370-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="9e370-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="9e370-116">Gibt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="9e370-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="9e370-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9e370-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="9e370-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="9e370-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="9e370-119">In den SOAP-Header verwendet für tokenserialisierung für Server-zu-Server-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9e370-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span>  <br/> |
|[<span data-ttu-id="9e370-120">Benutzer-ID</span><span class="sxs-lookup"><span data-stu-id="9e370-120">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="9e370-121">Identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner.</span><span class="sxs-lookup"><span data-stu-id="9e370-121">Identifies a delegate user or a user who has folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9e370-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="9e370-122">Text value</span></span>

<span data-ttu-id="9e370-123">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e370-123">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e370-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e370-124">Remarks</span></span>

<span data-ttu-id="9e370-125">Exchange Web Services erfordert, dass durch die primäre SMTP-Adresse des Postfachs Postfächer identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9e370-125">Exchange Web Services requires that mailboxes be identified by the primary SMTP address of the mailbox.</span></span> <span data-ttu-id="9e370-126">Proxy oder alternative Adressen werden nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9e370-126">Proxy or alternative addresses are not accepted.</span></span>
  
<span data-ttu-id="9e370-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e370-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e370-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9e370-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e370-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e370-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e370-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9e370-130">Schema Name</span></span>  <br/> |<span data-ttu-id="9e370-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9e370-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e370-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9e370-132">Validation File</span></span>  <br/> |<span data-ttu-id="9e370-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9e370-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e370-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9e370-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="9e370-135">False</span><span class="sxs-lookup"><span data-stu-id="9e370-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e370-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e370-136">See also</span></span>



- [<span data-ttu-id="9e370-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e370-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="9e370-138">Server-zu-Server-Autorisierung in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="9e370-138">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[<span data-ttu-id="9e370-139">Arbeiten mit Delegieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="9e370-139">Working with Delegate Access</span></span>](http://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

