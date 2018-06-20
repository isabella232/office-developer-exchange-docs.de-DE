---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: SID-Element stellt Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID) für das Konto für den Identitätswechsel verwenden oder Stellvertretungszugriff dar.
ms.openlocfilehash: efcea42c12ec1d26ea31fdb8de337c37a2338a96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831492"
---
# <a name="sid"></a><span data-ttu-id="5fc78-103">SID</span><span class="sxs-lookup"><span data-stu-id="5fc78-103">SID</span></span>

<span data-ttu-id="5fc78-104">**SID** -Element stellt Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID) für das Konto für den Identitätswechsel verwenden oder Stellvertretungszugriff dar.</span><span class="sxs-lookup"><span data-stu-id="5fc78-104">The **SID** element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access.</span></span> 
  
```xml
<SID/>
```

 <span data-ttu-id="5fc78-105">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="5fc78-105">**SIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5fc78-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5fc78-106">Attributes and elements</span></span>

<span data-ttu-id="5fc78-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5fc78-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5fc78-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5fc78-108">Attributes</span></span>

<span data-ttu-id="5fc78-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5fc78-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5fc78-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5fc78-110">Child elements</span></span>

<span data-ttu-id="5fc78-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5fc78-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5fc78-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5fc78-112">Parent elements</span></span>

|<span data-ttu-id="5fc78-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fc78-113">**Element**</span></span>|<span data-ttu-id="5fc78-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5fc78-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fc78-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="5fc78-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="5fc78-116">Gibt ein Konto Identitätswechsel bei Verwendung des "ExchangeImpersonation" SOAP-Headers.</span><span class="sxs-lookup"><span data-stu-id="5fc78-116">Represents an account to impersonate when using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="5fc78-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="5fc78-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="5fc78-118">Benutzer-ID</span><span class="sxs-lookup"><span data-stu-id="5fc78-118">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="5fc78-119">Identifiziert ein Stellvertreter oder von einem Benutzer mit Zugriffsberechtigungen für Ordner.</span><span class="sxs-lookup"><span data-stu-id="5fc78-119">Identifies a delegate user or a user with folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5fc78-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="5fc78-120">Text value</span></span>

<span data-ttu-id="5fc78-121">Der Textwert ist eine zeichenfolgendendarstellung einer SID.</span><span class="sxs-lookup"><span data-stu-id="5fc78-121">The text value is a string representation of a SID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fc78-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5fc78-122">Remarks</span></span>

<span data-ttu-id="5fc78-123">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fc78-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5fc78-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5fc78-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fc78-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fc78-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5fc78-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5fc78-126">Schema Name</span></span>  <br/> |<span data-ttu-id="5fc78-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5fc78-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="5fc78-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5fc78-128">Validation File</span></span>  <br/> |<span data-ttu-id="5fc78-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5fc78-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5fc78-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5fc78-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="5fc78-131">False</span><span class="sxs-lookup"><span data-stu-id="5fc78-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fc78-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fc78-132">See also</span></span>



- [<span data-ttu-id="5fc78-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5fc78-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

