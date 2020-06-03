---
title: PrincipalName
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
description: Das PrincipalName-Element stellt den Benutzerprinzipalnamen (User Principal Name, UPN) des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll.
ms.openlocfilehash: 31412c1461264e28bf8d52c957a457e8d1e847ef
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44440190"
---
# <a name="principalname"></a><span data-ttu-id="642c2-103">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="642c2-103">PrincipalName</span></span>

<span data-ttu-id="642c2-104">Das **PrincipalName** -Element stellt den Benutzerprinzipalnamen (User Principal Name, UPN) des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="642c2-104">The **PrincipalName** element represents the user principal name (UPN) of the account to be used for Exchange impersonation.</span></span> 
  
```xml
<PrincipalName/>
```

 <span data-ttu-id="642c2-105">**PrincipalNameType**</span><span class="sxs-lookup"><span data-stu-id="642c2-105">**PrincipalNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="642c2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="642c2-106">Attributes and elements</span></span>

<span data-ttu-id="642c2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="642c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="642c2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="642c2-108">Attributes</span></span>

<span data-ttu-id="642c2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="642c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="642c2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="642c2-110">Child elements</span></span>

<span data-ttu-id="642c2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="642c2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="642c2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="642c2-112">Parent elements</span></span>

|<span data-ttu-id="642c2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="642c2-113">**Element**</span></span>|<span data-ttu-id="642c2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="642c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="642c2-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="642c2-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="642c2-116">Stellt ein Konto für den Identitätswechsel dar, wenn Sie den SOAP-ExchangeImpersonation-Header verwenden.</span><span class="sxs-lookup"><span data-stu-id="642c2-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="642c2-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="642c2-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="642c2-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="642c2-118">Text value</span></span>

<span data-ttu-id="642c2-119">Der Wert Text stellt den UPN eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="642c2-119">The text value represents the UPN of a user.</span></span> <span data-ttu-id="642c2-120">Dieser Wert ist für das Benutzerobjekt im Active Directory Verzeichnisdienst vorhanden.</span><span class="sxs-lookup"><span data-stu-id="642c2-120">This value exists on the user object in the Active Directory directory service.</span></span> <span data-ttu-id="642c2-121">Dieser enthält den Benutzeranmeldenamen und einen Domänennamen, der die Domäne identifiziert, in der sich das Benutzerkonto befindet, im folgenden Format: `someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="642c2-121">This contains the user logon name and a domain name that identifies the domain in which the user account is located, in the following format:  `someone@example.com`.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="642c2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="642c2-122">Remarks</span></span>

<span data-ttu-id="642c2-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="642c2-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="642c2-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="642c2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="642c2-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="642c2-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="642c2-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="642c2-126">Schema Name</span></span>  <br/> |<span data-ttu-id="642c2-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="642c2-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="642c2-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="642c2-128">Validation File</span></span>  <br/> |<span data-ttu-id="642c2-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="642c2-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="642c2-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="642c2-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="642c2-131">False</span><span class="sxs-lookup"><span data-stu-id="642c2-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="642c2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="642c2-132">See also</span></span>



- [<span data-ttu-id="642c2-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="642c2-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="642c2-134">Server-zu-Server-Autorisierung in EWS</span><span class="sxs-lookup"><span data-stu-id="642c2-134">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

