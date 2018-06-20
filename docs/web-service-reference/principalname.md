---
title: "' PrincipalName '"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrincipalName
api_type:
- schema
ms.assetid: 88c142d4-0bc7-43ea-a997-d7200664d900
description: Das Element ' PrincipalName ' stellt den Benutzerprinzipalnamen (UPN) des Kontos, das für den Exchange-Identitätswechsel verwendet werden.
ms.openlocfilehash: d8557ce0435a11a5602372517db1f576028a9c97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830882"
---
# <a name="principalname"></a><span data-ttu-id="6da89-103">' PrincipalName '</span><span class="sxs-lookup"><span data-stu-id="6da89-103">PrincipalName</span></span>

<span data-ttu-id="6da89-104">Das Element **' PrincipalName '** stellt den Benutzerprinzipalnamen (UPN) des Kontos, das für den Exchange-Identitätswechsel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6da89-104">The **PrincipalName** element represents the user principal name (UPN) of the account to be used for Exchange impersonation.</span></span> 
  
```xml
<PrincipalName/>
```

 <span data-ttu-id="6da89-105">**PrincipalNameType**</span><span class="sxs-lookup"><span data-stu-id="6da89-105">**PrincipalNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6da89-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6da89-106">Attributes and elements</span></span>

<span data-ttu-id="6da89-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6da89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6da89-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6da89-108">Attributes</span></span>

<span data-ttu-id="6da89-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6da89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6da89-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6da89-110">Child elements</span></span>

<span data-ttu-id="6da89-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6da89-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6da89-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6da89-112">Parent elements</span></span>

|<span data-ttu-id="6da89-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6da89-113">**Element**</span></span>|<span data-ttu-id="6da89-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6da89-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6da89-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="6da89-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="6da89-116">Gibt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="6da89-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="6da89-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="6da89-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6da89-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="6da89-118">Text value</span></span>

<span data-ttu-id="6da89-119">Der Textwert stellt den UPN eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="6da89-119">The text value represents the UPN of a user.</span></span> <span data-ttu-id="6da89-120">Dieser Wert auf das Benutzerobjekt in Active Directory-Verzeichnisdienst vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6da89-120">This value exists on the user object in the Active Directory directory service.</span></span> <span data-ttu-id="6da89-121">Dieses Webpart enthält den Benutzeranmeldenamen und einen Domänennamen, die die Domäne gibt an, in dem das Benutzerkonto befindet sich im folgenden Format: `someone@example.com`.</span><span class="sxs-lookup"><span data-stu-id="6da89-121">This contains the user logon name and a domain name that identifies the domain in which the user account is located, in the following format:  `someone@example.com`.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6da89-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6da89-122">Remarks</span></span>

<span data-ttu-id="6da89-123">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6da89-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6da89-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6da89-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6da89-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6da89-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6da89-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6da89-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6da89-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6da89-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6da89-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6da89-128">Validation File</span></span>  <br/> |<span data-ttu-id="6da89-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6da89-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6da89-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6da89-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6da89-131">False</span><span class="sxs-lookup"><span data-stu-id="6da89-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6da89-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6da89-132">See also</span></span>



- [<span data-ttu-id="6da89-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6da89-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6da89-134">Server-zu-Server-Autorisierung in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6da89-134">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

